---
created: 2024-12-10T21:41:16
modified: '"2024-12-10 21:44", "2tc/G12T+6"'
type: 
aliases: 
tags:
  - obsidian
  - git
---

Cree un script con ayuda de ChatGPT para sincronizar el repositorio que contiene el Vault de Obsidian. 

Primero verifica cambios en el remoto y hace pull y luego sube los cambios en el local y hace push.

Esto es en sustitución al plugin de Git de Obsidian el cual soporta la aplicaciones de Android pero me ha dado problemas de conflictos. 

El script es el siguiente :

```
#!/bin/bash

# Configura el directorio del Vault
VAULT_DIR=~/storage/documents/my_productivity_brain_2025

# Cambiar al directorio del Vault
cd "$VAULT_DIR" || { echo "Error: No se pudo acceder al directorio del Vault."; exit 1; }

# Verificar si es un repositorio Git
if [ ! -d ".git" ]; then
  echo "Error: Este directorio no es un repositorio Git."
  exit 1
fi

# Descargar cambios remotos
echo "📥 Descargando cambios del remoto..."
git fetch origin

# Verificar si hay cambios en el remoto
LOCAL=$(git rev-parse HEAD)
REMOTE=$(git rev-parse @{u})
BASE=$(git merge-base HEAD @{u})

if [ "$LOCAL" = "$REMOTE" ]; then
  echo "✅ El repositorio local está sincronizado con el remoto."
elif [ "$LOCAL" = "$BASE" ]; then
  echo "📥 Hay cambios en el remoto. Actualizando el repositorio local..."
  git pull || { echo "Error: No se pudo actualizar desde el remoto."; exit 1; }
elif [ "$REMOTE" = "$BASE" ]; then
  echo "📤 Hay cambios locales. Preparando para subirlos al remoto..."
else
  echo "❌ Hay conflictos entre el local y el remoto. Resolución manual necesaria."
  exit 1
fi

# Verificar si hay cambios locales
echo "🔍 Buscando cambios locales..."
if [ -n "$(git status --porcelain)" ]; then
  echo "📤 Cambios locales encontrados. Subiéndolos al remoto..."
  git add .
  git commit -m "Sincronización automática del Vault" || echo "⚠️ No hay cambios que confirmar."
  git push || { echo "Error: No se pudo subir los cambios al remoto."; exit 1; }
else
  echo "✅ No hay cambios locales para enviar al remoto."
fi

echo "🚀 Sincronización completada exitosamente."

read -p "Presiona Enter para salir..."
```
El siguiente paso es hacer una especie de crontab para que lo haga cierto tiempo automáticamente desde el teléfono. 


--- 
 **Notas relacionadas:**
[[2024-12-09 My Obsidian Setup]]
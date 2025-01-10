---
modified: '"2025-01-10 10:28", "5tc/G1T+6"'
created: '"2025-01-10 10:27", "5tc/G1T+6"'
---
# Haciendo pruebas para gestionar los Follow ups


## Que?
Estoy buscando una forma de unificar en solo lugar las cosas que anoto como followups de los proyectos, ya sea que los ponga en forma de bullets o en forma de tarea, o incluso como una linea normal

### Datos de Ejemplo

- ejemplo lista #followup #id12345
 ejemplo nada #followup #id12345 
- [ ] dfa #followup #id12345 
otro ejemplo nada con un tag adicional  #followup #id12345 #testtag1 
- ejemplo sin un tag #id12345


### Prueba 1
This query searches for lines containing both `#followup` and `#id12345` within lists or tasks across all your notes and displays them as a bullet list.

```dataviewjs
dv.paragraph(dv.pages()
  .where(p => p.file.lists)
  .flatMap(p => p.file.lists)
  .filter(l => l.text.includes("#followup") && l.text.includes("#id12345"))
  .map(l => `- ${l.text}`)
  .join("\n"));
```
#### Este approach no me sirve por que:
- No puedo ir rápidamente a la nota origen

### Prueba 2

```dataview
LIST
FROM #followup AND #id10854
```


### Pruebas 3
```dataview
TASK WHERE contains(tags, "#id11065") AND contains(tags, "#followup")
```

**Con Tasks**


```tasks
(tag include #followup)
not done
group by tags
```

## Conclusion




# Otras pruebas para ordenar mis minutas


```dataview
table file.name as "Nota", type as "Tipo"
from "2 Areas/21 Work@Escala24x7/213 Minutas"
where !contains(type, "minuta")
```

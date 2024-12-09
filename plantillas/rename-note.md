<%*
const iso8601 = tp.date.now("YYYY-MM-DDTHHmmss");
const title = await tp.system.prompt("Escribe el título de la nota:");
const newName = `${iso8601} - ${title}`;
await tp.file.rename(newName);
%>
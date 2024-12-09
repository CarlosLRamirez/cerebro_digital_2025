<%*
const iso8601 = tp.date.now("YYYY-MM-DDTHH:mm:ss");
const newName = iso8601;
await tp.file.rename(newName);
%>
<%*
const iso8601 = tp.date.now("YYYY-MM-DDTHHmmss");
const newName = iso8601;
await tp.file.rename(newName);
%>
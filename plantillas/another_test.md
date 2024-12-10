

File creation: [[<% (await tp.file.create_new(
`## Nice header

Some text stuff...


Today is: ${ tp.date.now("YYYY-MM-DD HHmmss") }, but what's in a date? 
`,  tp.date.now("YYYY-MM-DD HHmmss"))).basename %>]]

## vim

### Vim tricks

| **command** | **explanation** |
| :---| :-------------------------------------|
| hjkl | left, down, up, right 
| 2h/j/k/l | move 2 lines in that direction (j) |
| .  | repeat the last command |
| yi( | copy everything between `()` |
| ya( | copy everything between `()` including the delimiter `()` |
| das | delete the sentence and the delimiter |
| dis | delete the sentence without the delimiter |
| fr  | go to the first `r` on the line |
| dw  | delete the word from the cursor including the delimiter |
| daw | delete the word and the delimiter no matter where the cursor is |
| diw | delete the word without the delimiter no matter where the cursor is |
| da[/( | delete everything between the `[]`/`()` including the delimiter `[]`/`()`|
| dap | delete a paragraph with the delimiter (blank line)|
| dip | delete a paragraph without the delimeter (blank line) |
| cw  | delete the word from the cursor and enter in INSERT mode |
| ciw | delete the word and enters in INSERT mode no matter where the cursor is |
| ci[/( | deletes everything between the `[]`/`()` and enters in INSERT mode |
| ca[/( | deletes everything between the `[]`/`()` including the delimiter `[]`/`()` and enters in INSERT mode |
| cit | deletes everything between the tags (ex. `<p> </p>`) and enters in INSERT mode |
| cat | deletes everything between the tags (ex. `<p> </p>`) including the tags and enters in INSERT mode |
| cib | deletes everything in the block (ex. `{ NEWLINES }`) and enters in INSERT mode |
| cab | deletes everything in the block (ex. `{ NEWLINES }`) including the block `{ NEWLINES }` and enters in INSERT mode || 
| :reg " | view the unnamed register |
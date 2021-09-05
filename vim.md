## vim

## Vim tricks

| **Common** | |
| :---| :---|
| `u`| undo the last change |
| `Ctrl-r`| redo the last undo |
| `:w`| save the file |
| `:q`| exit the file (there will be a prompt if there is a change)|
| `:q!`| exit the file without saving (no prompt)|
| `:wq`/`:x`/`ZZ` | save and exit the file |
| `.`  | repeat the last command |
| "" | unnamed register, holds `d`,`c`, `s`, `x` and `y` operations |
| "0 | holds last `y` |
| "1 | holds last `d` and `c` |
| "_ | blackhole register, every operation is gone |
| `:reg` | view all registers |
| `:reg "` | view the unnamed register |
| `{operation}{motion}` | ex. `{delete}{word}`|
| `[count]{operation}{motion}` | ex. `[repeat]{delete}{word}`|
| `{operation}{a}{object}` | ex. `{delete}{a}{sentence}`|
| `{operation}{i}{object}` | ex. `{change}{inner}{word}`|

| **Navigation**| |
| :---| :---|
| `hjkl` | left, down, up, right 
| `2hj` | move 2 lines in that direction (j) |
| `Ctrl-f` | Move forward in the file (PgDn)|
| `Ctrl-b` | Move backward in the file (PgUp)|
| `G` | Move at the end of the file (End)|
| `5G`| Move to the fifth line in the file |
| `gg` | Move at the beginning of the file (Home)|
| `w` | Move to the next word (the punctuation counts as a word)|
| `W` | Move to the next word (the punctuation doesn't count as a word)|
| `b` | Move to the previous word (the punctuation counts as a word)|
| `B` | Move to the previous word (the punctuation counts as a word)|
| `$` | Move to the end of the current line |
| `0` | Move to the beginning of current the line (including TAB)|
| `^` | Move to the first character in the current line |
| `fr` | go forward to the first matched `r` on the line |
| `Fr` | go backward to the first matched `r` on the line |
| `Ctrl-g` | Display the current position in the file |
| `zz` | Center the screen to the cursor position |
| `zEnter` | Puts the screen with the cursor position at the top |

| **Cut / Copy / Paste** | |
| :---| :---|
| `yy` | yank (copy) the entire line including the \n |
| `"ayy` | yank the line to the the register "a |
| `"Ayy` | yank the line and append it to the the register "a |
| `4yy` | yank four lines |
| `y$` | yank from the cursor to the end of the line without \n |
| `y0` | yank from the cursor to the beginning of the line (including the \t)|
| `y^` | yank from the cursor to the first character at the beginning of the line |
| `yw` | yank the current word no matter the cursor position |
| `2yw`/`y2w` | yank two words to the left |
| `yap` | yank the current paragraph |
| `p` | put (paste) after the cursor |
| `P` | put before the cursor |
| `yi(` | copy everything between `()` |
| `ya(` | copy everything between `()` including the delimiter `()` |
| `"4p` | put the text in the register "4 | 


| **Delete / Change**| |
| :---| :---|
| `x`/`dl` | delete (cut) the character under the cursor, saves it in the register |
| `X` | delete the character before the cursor |
| `dw` | delete the word from the cursor including the delimiter |
| `d$`/`D` | delete from the cursor to the end of the line |
| `d0` | delete from the cursor to the beginning of the line |
| `dd` | delete the whole line no matter the cursor position |
| `3dd` | delete whole 3 lines no matter the cursor position |
| `d3w` | delete 3 words from the cursor |
| `"_dd`| delete the line and send it to the blackhole register |
| `"2dd`| delete the line and send it to the register 2 |
| `cw` | delete the word from the cursor and enter in INSERT mode (change) |
| `c$`/`C` | delete from the cursor to the end of the line and enter in INSERT mode (change) |
| `c0` | delete from the cursor to the beginning of the line and enter in INSERT mode (change) |
| `cc` | delete the whole line no matter the cursor position and enter in INSERT mode (change) |
| `das` | delete the sentence and the delimiter |
| `dis` | delete the sentence without the delimiter |
| `daw` | delete the word and the delimiter no matter where the cursor is |
| `diw` | delete the word without the delimiter no matter where the cursor is |
| `da[/(` | delete everything between the `[]`/`()` including the delimiter `[]`/`()`|
| `dap` | delete a paragraph with the delimiter (blank line)|
| `dip` | delete a paragraph without the delimiter (blank line) |
| `ciw` | delete the word and enters in INSERT mode no matter where the cursor is |
| `ci[/(` | deletes everything between the `[]`/`()` and enters in INSERT mode |
| `ca[/(` | deletes everything between the `[]`/`()` including the delimiter `[]`/`()` and enters in INSERT mode |
| `cit` | deletes everything between the tags (ex. `<p> </p>`) and enters in INSERT mode |
| `cat` | deletes everything between the tags (ex. `<p> </p>`) including the tags and enters in INSERT mode |
| `cib` | deletes everything in the block (ex. `{ NEWLINES }`) and enters in INSERT mode |
| `cab` | deletes everything in the block (ex. `{ NEWLINES }`) including the block `{ NEWLINES }` and enters in INSERT mode || 
| `s` | substitute a character, enter INSERT mode  |
| `r` | replace a character |
| `Shift-~` | change the character case (upper, lower) |
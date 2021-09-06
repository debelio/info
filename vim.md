## vim

## Vim tricks

**Common**
| Command | Explanation |
| :---| :---|
| `u`| Undo the last change |
| `Ctrl-r`| Redo the last undo |
| `:w`| Save the file |
| `:q`| Exit the file (there will be a prompt if there is a change)|
| `:q!`| Exit the file without saving (no prompt)|
| `:wq`/`:x`/`ZZ` | Save and exit the file |
| `.`  | Repeat the last command |
| "" | Unnamed register, holds `d`,`c`, `s`, `x` and `y` operations |
| "0 | Holds last `y` |
| "1 | Holds last `d` and `c` |
| "_ | Blackhole register, every operation is gone |
| `:reg` | View all registers |
| `:reg "` | View the unnamed register |
| `{operation}{motion}` | ex. `{delete}{word}`|
| `[count]{operation}{motion}` | ex. `[repeat]{delete}{word}`|
| `{operation}{a}{object}` | ex. `{delete}{a}{sentence}`|
| `{operation}{i}{object}` | ex. `{change}{inner}{word}`|
| `v` | visual mode characterwise, press `o` to select both sides |
| `V` | visual mode linewise |
| `Ctrl-v` | visual mode blockwise, press `O` to move to the other side of the line |
| in V-mode | `~` - switch case, `c` - change, `d` - delete, `y` - yank, `r` - replace, `x` -delete, `I` - insert, `A` - append, `J` - join, `u` - make lowercase, `U` - make uppercase, `>` - shift right, `<` - shift left 

**Navigation**
| Command | Explanation |
| :---| :---|
| `hjkl` | Left, down, up, right |
| `Enter` | Move one line down to the first character |
| `2hj` | Move 2 lines in that direction (j) |
| `Ctrl-f` | Move forward in the file (PgDn)|
| `Ctrl-b` | Move backward in the file (PgUp)|
| `G` | Move at the end of the file (End)|
| `5G`| Move to the fifth line in the file |
| `gg` | Move at the beginning of the file (Home)|
| `w` | Move to the next word (the punctuation counts as a word)|
| `W` | Move to the next word (the punctuation doesn't count as a word)|
| `b` | Move to the previous word (the punctuation counts as a word)|
| `B` | Move to the previous word (the punctuation doesn't count as a word)|
| `$` | Move to the end of the current line |
| `0` | Move to the beginning of current the line (including TAB)|
| `^` | Move to the first character in the current line |
| `fr` | Go forward to the first matched `r` on the line |
| `Fr` | Go backward to the first matched `r` on the line |
| `Ctrl-g` | Display the current position in the file |
| `zz` | Center the screen to the cursor position |
| `zEnter` | Puts the screen with the cursor position at the top |
| `{` | One paragraph backward |
| `}` | One paragraph forward |
| `-` | Up one line on the first character |
| `+` | Down one line on the first character |

**Append / Edit**
| Command | Explanation |
| :---| :---|
| `a` | Append text after the cursor |
| `A` | Append text at the end of the line |
| `i` | Insert text before the cursor |
| `I` | Insert text at the beginning of the line |
| `s` | Substitute (delete and insert) the character |
| `S` | Substitute (delete and insert) the whole line |
| `r` | Replace the character without insert |
| `R` | Replace all characters in secession until `ESC` |
| `J` | Join the bottom line with the current one |
| `:center 80` | center the line 80 characters to the right |
| `:left` | realign the text to the left | 

**Cut / Copy / Paste**
| Command | Explanation |
| :---| :---|
| `yy` | Yank (copy) the entire line including the \n |
| `"ayy` | Yank the line to the the register "a |
| `"Ayy` | Yank the line and append it to the the register "a |
| `4yy` | Yank four lines |
| `y$` | Yank from the cursor to the end of the line without \n |
| `y0` | Yank from the cursor to the beginning of the line (including the \t)|
| `y^` | Yank from the cursor to the first character at the beginning of the line |
| `yw` | Yank the current word no matter the cursor position |
| `2yw`/`y2w` | Yank two words to the left |
| `yap` | Yank the current paragraph |
| `p` | Put (paste) after the cursor |
| `P` | Put before the cursor |
| `yi(` | Copy everything between `()` |
| `ya(` | Copy everything between `()` including the delimiter `()` |
| `"4p` | Put the text in the register "4 | 

**Delete / Change**
| Command | Explanation |
| :---| :---|
| `x`/`dl` | Delete (cut) the character under the cursor, saves it in the register |
| `X` | Delete the character before the cursor |
| `dw` | Delete the word from the cursor including the delimiter |
| `d$`/`D` | Delete from the cursor to the end of the line |
| `d0` | Delete from the cursor to the beginning of the line |
| `dd` | Delete the whole line no matter the cursor position |
| `3dd` | Delete whole 3 lines no matter the cursor position |
| `d3w` | Delete 3 words from the cursor |
| `"_dd`| Delete the line and send it to the blackhole register |
| `"2dd`| Delete the line and send it to the register 2 |
| `cw` | Delete the word from the cursor and enter in INSERT mode (change) |
| `c$`/`C` | Delete from the cursor to the end of the line and enter in INSERT mode (change) |
| `c0` | Delete from the cursor to the beginning of the line and enter in INSERT mode (change) |
| `cc` | Delete the whole line no matter the cursor position and enter in INSERT mode (change) |
| `das` | Delete the sentence and the delimiter |
| `dis` | Delete the sentence without the delimiter |
| `daw` | Delete the word and the delimiter no matter where the cursor is |
| `diw` | Delete the word without the delimiter no matter where the cursor is |
| `da[/(` | Delete everything between the `[]`/`()` including the delimiter `[]`/`()`|
| `dap` | Delete a paragraph with the delimiter (blank line)|
| `dip` | Delete a paragraph without the delimiter (blank line) |
| `ciw` | Delete the word and enters in INSERT mode no matter where the cursor is |
| `ci[/(` | Deletes everything between the `[]`/`()` and enters in INSERT mode |
| `ca[/(` | Deletes everything between the `[]`/`()` including the delimiter `[]`/`()` and enters in INSERT mode |
| `cit` | Deletes everything between the tags (ex. `<p> </p>`) and enters in INSERT mode |
| `cat` | Deletes everything between the tags (ex. `<p> </p>`) including the tags and enters in INSERT mode |
| `cib` | Deletes everything in the block (ex. `{ NEWLINES }`) and enters in INSERT mode |
| `cab` | Deletes everything in the block (ex. `{ NEWLINES }`) including the block `{ NEWLINES }` and enters in INSERT mode |
| `Shift-~` | Change the character case (upper, lower) |
| `Ctrl-a` | Add 1 to the number and replace it (from 3 to 4) |
| `Ctrl-x` | Subtract 1 from the number and replace it (from 3 to 2) |

**Macros**
| Command | Explanation |
| :---| :---|
| `qa` | Start recording a macro in the `a` register, start with `0`, end with `j`. After you finish press `q` again |
| `qA` | Append to the `a` macro |
| `@a` | Execute the `a` macro |
| `@@` | Execute the most recent macro |
| `:reg a` | See the recorded macro `a` |
| `:27,35normal @a` | Execute the macro `a` to the lines 27 until 35 |
| `:.,$normal @a` | Execute the macro `a` from the first to the last line |
| `"ap` | Copy the register in the file so you can change and save it again with `"ay$` |
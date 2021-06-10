## Bash tricks
| **command**                       | **explanation**                             |
| :-------------------------------- | :------------------------------------------ |
| sudo !!                           | execute the last command with sudo |
| alt + . or !$                     | use the last non-expanded argument of the previous command |
| alt + _ or $_                     | use the last expanded argument of the previous command |
| ctrl + r                          | search through bash history |
| ctrl + l                          | clear screen |
| ctrl + x AND ctrl + e             | edit the line in $EDITOR | 
| <(some command)                   | executes the command and creates a temporary named pipe with the output. ex. tail -f <(zcat log.txt.gz) |
| .inputrc                          | https://github.com/dannycolin/dotfiles/blob/master/user/console/.inputrc |
| PYTHONUNBUFFERED=1 python test.py | overwrite environment variable |
| curl cheat.sh/command             | summary of the command usage |
| ctrl + a                          | go to  the beginning of the line |
| ctrl + e                          | go to  the end of the line |
| ctrl + _                          | undo |
| ctrl + u                          | delete before the cursor |
| ctrl + k                          | delete after the cursor |

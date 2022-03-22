# 🐚 bash-shell

### <mark style="color:green;">Bash Nav Shortcuts:</mark>

`Ctrl`+`U`- Cut everything to the left &#x20;

`Ctrl`+`W`- Cut one word to the left

`Ctrl`+`Y`- Paste a line cut with Ctrl+U&#x20;

`Ctrl`+`L`- Clear the screen and redraw the current line&#x20;

`Ctrl`+`G`- Get a new line and abandon the current one

`Ctrl`+`R`- Reverse search history

`Alt`+`F`- Go forward by one word

`Alt`+`B`- Go backward by one word

`Ctrl`+`A`- Go to the beginning of a line

`Ctrl`+`E`- Go to the end of a line

### <mark style="color:purple;">Bash Command Execution:</mark>

`#!/usr/bin/sudo /bin/bash` - Execute entire shell script as sudo (This line replaces shabang line in shell script

`sudo !!` - Execute the last command as root

`!whatever:p` - Find the last command that begins with `whatever`, but avoid running it

`&lt;space>command` - Execute a command without saving it in history

### <mark style="color:yellow;">Spelling errors bash</mark>&#x20;

`!!:gs/foo/bar` <mark style="color:yellow;"></mark> - run the previous command, replace every foo with bar

`^ehco^echo` - Run the previous command, replace first occurence of echo with echo


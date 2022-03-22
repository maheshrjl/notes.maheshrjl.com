# 🔎 file & dir operations

### <mark style="color:blue;">Creating files</mark>

`> file.txt` - Empty `file.txt` or create a new file

### <mark style="color:purple;">Storage Usage</mark>

`du -h --max-depth=1` - Show the size of all sub folders in the current directory

### <mark style="color:orange;">Permission</mark>

`chmod --reference file1 file2` - Makes the permissions of file2 the same as file1, also works with chgrp & chown

### <mark style="color:yellow;">Easy copy/backup</mark>

`cp filename{,.bak}` - Quickly backup or copy a file, copies filename to a file named filename.bak

`rename 'y/ /_/' *` - Replace spaces in filename with underscores

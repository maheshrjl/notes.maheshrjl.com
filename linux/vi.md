# 📼 vi-editor

`:w !sudo tee %`  -  Save a file that is opened without sudo

### VI Navigation

`$` -  Positions cursor at end of line

`^` -  Positions cursor at beginning of line

`w` - One word forward

`b` - back one word&#x20;

### Deletion commands VI

`dd` - Delete current line

_`n`_`dd` - Delete _n_ lines of buffer

### Undo VI

`u` - Undo last change

`U` - Undo all changes on line



### Search & Replace in VI

Syntax: `:[address]s/old_text/new_text/`

<details>

<summary>Address components</summary>

* `.` Current line&#x20;
* `n` - Line number&#x20;
* `n.+m` - Current line plus m lines&#x20;
* `$` - Last line&#x20;
* `/string/` - A line that contains "string"&#x20;
* `%`- Entire file&#x20;
* `[addr1],[addr2]` - Specifies a range

</details>

### VI Parameters

`:set number` - Show line numbers

`:set list` - Show invisible characters

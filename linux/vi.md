# 📼 vi-editor

`:w !sudo tee %`  -  Save a file that is opened without sudo

### <mark style="color:blue;">VI Navigation</mark>

`$` -  Positions cursor at end of line

`^` -  Positions cursor at beginning of line

`w` - One word forward

`b` - back one word&#x20;

`gg` - Go to first line in file

`G` - Go to last line in file

### <mark style="color:orange;">Append in VI</mark>

`a` - Append after the cursor

`i` - Append before the cursor

`I` - Append at the beginning of a line

`A` - Append at the end of a line

`o` - Create new line under the cursor

`O` - Create new line above the cursor

### <mark style="color:green;">Deletion commands VI</mark>

`dd` - Delete current line

_`n`_`dd` - Delete _n_ lines of buffer

### <mark style="color:yellow;">Undo VI</mark>

`u` - Undo last change

`U` - Undo all changes on line

### <mark style="color:purple;">Search & Replace in VI</mark>

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

|   :s/foo/bar/  | replace the first match of 'foo' with 'bar' on the current line only          |
| :------------: | ----------------------------------------------------------------------------- |
|  :s/foo/bar/g  | replace all matches (\`g\` flag) of 'foo' with 'bar' on the current line only |
|  :%s/foo/bar/g | replace all matches of 'foo' with 'bar' in the entire file (\`:%s\`)          |
| :%s/foo/bar/gc | ask to manually confirm (\`c\` flag) each replacement                         |

### VI Parameters

`:set number` - Show line numbers

`:set list` - Show invisible characters

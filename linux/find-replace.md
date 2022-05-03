# 🔍 find & replace

### <mark style="color:blue;">Find text in files:</mark>

`grep '^.' filename` - Get all lines that start with a dot or period

`grep -rnw '/path/' -e 'pattern'`&#x20;

* `-r` or `-R` is recursive,
* `-n` is line number, and
* `-w` stands for match the whole word.
* `-l` (lower-case L) can be added to just give the file name of matching files.
* `-e` is the pattern used during the search

Along with these, `--exclude`, `--include`, `--exclude-dir` flags could be used for efficient searching:

* This will only search through those files which have .c or .h extensions:

`grep --include=*.{c,h} -rnw '/path/to/somewhere/' -e "pattern"`

* This will exclude searching all the files ending with .o extension:

`grep --exclude=*.o -rnw '/path/to/somewhere/' -e "pattern"`

* For directories it's possible to exclude one or more directories using the `--exclude-dir` parameter. For example, this will exclude the dirs dir1/, dir2/ and all of them matching \*.dst/

`grep --exclude-dir={dir1,dir2,*.dst} -rnw '/path/to/somewhere/' -e "pattern"`

### <mark style="color:purple;">Find based on file content</mark>

`find . -type f -exec grep "forinstance" '{}' ; -print`&#x20;

### <mark style="color:orange;">Find SUID/GUID and Sticky bit Files</mark>

`find . -perm /4000` - SUID

`find . -perm /2000` - GUID

`find . -perm /1000` - Sticky Bit

`find . -perm /6000` - Search for both SUID & GUID

### Find files based on modified time

`find -mmin 5` - Find files modified exactly 5 minute ago (In that minute only)

`find -mmin -5` - List all files modified in the last 5 minutes

`find -mmin +5` - Find all files modified more than 5 minutes ago

{% hint style="info" %}
`mtime` is used to find files modified more than 24 hours ago, `ctime` can be used to search by file change times, `size` can also be used.&#x20;

Operators like -o for or and -not can also be used (and is the default operator)
{% endhint %}

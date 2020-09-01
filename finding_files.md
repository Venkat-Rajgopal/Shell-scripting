# Finding files through bash

Here `.` after `find` indicates **current folder**. Type indicates the type of file/directory. 

`find` has many different parameters. Here we can give path to the directory starting with 

```bash
find . -path '**/Python*.py' -type f
```

Similary finding changes in a file. 

```bash
find . -mtime -1
```

# Find and remove. 

Find all the files ending with .tmp. 
```bash
find . -name '*.tmp' -exec rm {} \;
```

Find files ending with `csv`
```bash
$ find . -name '*.csv'
```

# Grep
Grep is also another common technique to find in files. 

```bash
grep foobar ./Shell-scripting/mcd.sh
```


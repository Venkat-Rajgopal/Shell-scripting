
# Control flow techniques 

As with most programming languages, bash supports control flow techniques including if, case, while and for. Similarly, bash has functions that take arguments and can operate with them. Here is an example of a function that creates a directory and cds into it.

Here `$1` is the first argument to the script/function.

`$0` - Name of the script
`$1` to `$9` - Arguments to the script. $1 is the first argument and so on.
`$@` - All the arguments
`$#` - Number of arguments
`$?` - Return code of the previous command
`$$` - Process identification number (PID) for the current script
`!!` - Entire last command, including arguments


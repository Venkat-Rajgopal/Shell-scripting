# About `cd`

To get to the root, 
```bash
cd /
```

If you want to toggle between two directories you can simply do `cd -`. `cd -` takes you to the previous directory. 
```bash
cd -
```

One hand trick is the tilde character `~` always directs to the *home directory*. i.e simply doing `cd ~/` will take to the home directory. 

# Getting help
You can always lookup the ls helpcenter for aliases and its usage. Simply run, 

```bash
ls --help
```

For example `ls -l` not just prints out all information but also lists extra information of the directory. 

```bash 
$ ls -l

total 9
-rw-r--r-- 1 AzureAD+User 4096 1330 Jul 21 15:55 bash_essentials.md
-rw-r--r-- 1 AzureAD+User 4096  242 Aug 10 16:44 README.md
-rw-r--r-- 1 AzureAD+User 4096  585 Aug 11 11:33 shell_overview.md
```

Here the abbrevations `rw` refers to read, write. 


# Moving, Copying, Remove and Make
1. `mv` command allows you to move around a file. Move lets you rename or move a file. For example if i want to rename i simply need to do, 

```bash
mv oldfilename.extn newfilename.extn
```

If you give a path to the filenames it will move the files from one dir to another. 

```bash
mv /path/to/file /newpath/to/file
```

2. `cp` allows you to simply copy a file from one dir to another. 
Note: It need not be in the same directory. You can always use `../` to jump directories.

```bash
$ cp shell_overview.md ../Notes/
```

3. Similary `rm` is to remove a file. 
Remove is y default not-recursive. So cant remove a directory. 

```bash
$ rm /n/test/

rm: cannot remove '/n/test/': Is a directory
```
To remove recursively we need. 

```bash
$ rm -r /n/test/
```
Alternatively `rmdir` removes directory only if it is empty. So this acts as a ood safety mechanism. 

4. Finally `mkdir` will create a directory. Important to note that not to have space between dir names. Else it will create two directories. 

```bash
$ mkdir my files
```
This will create two directories 'my' and 'files'. To make spaced files use quotes. "" 

```bash
$ mkdir "my files"
```


# Manual
You can read a manual of a command by doing 

```bash 
man ls
```


# `<` , `>`, `>>` in Shell
Angle bracket signs 

1. `<` indicates: rewire the inputs of this file to be the contents of this file. 
2. `>` indicates: rewire the output of preceeing program into this file. 

Lets see an example. 

`echo` allows you to print something. So in this case we echo hello into the hello.txt file using `>` operator. 
```bash 
echo hello > hello.txt
```
So this creates a txt file with `hello` written in it. Notice noting prints into the output. It just takes it into a new file. 


We can verify this using `cat`. `cat` prints the output of a file. So when you do

```bash 
cat hello.txt
```
it will print the output on the terminal. 

`cat` also supports wiring. So `cat < hello.txt` takes input from hello.txt. So this is a combonation of Shell operator `<` and `cat`.

We can rewire this using `>` so that it simply moves the ouput to a new file. We do this by, 

```bash 
cat < hello.txt > hello_again.txt
```

3. `>>` is just append instead of overwrite. 

``` bash
$ cat < hello.txt  >> hello2.txt

$ cat hello2.txt

hello
hello
```

# Pipe `|`
`|` means : Take the ouput from the program to the left and use it as an input for the program to the left. 

`tail` shows the last n files. So here, we can use `ls -l` and pipe `|` it using the tail command. 

```bash
$ ls -l / | tail -n1

drwxr-xr-x  1 AzureAD+RajgopalVenkatramani 4096       0 Apr 16 10:51 usr/
```
The pipe is what wires ls and tail together. And this we can wire it back to a file with `>` as below. 

```bash
$ ls -l / | tail -n1 > ls.txt
```

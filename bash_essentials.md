# Bash Essentials

This post will cover some usefulful tricks with bash that can automatize lots of daily routine. 


## Setting up new alias
Say you want to create a bash shortcut/alias that can directly jump `cd` to your working directory.  That is instead of typing everytime `cd n:/Project_dir` you create a short alias that will direct to the folder. 

First lets create a the alias. This needs to be done at your `.bashrc` so that it can load automatically each time. 

1. Go to `bashrc` or `bash_aliases` in your terminal. 
```bash
vi ~/.bashrc
```

2. Append desired alias. I am calling it as `cdproj`
```bash
alias cdproj='cd /path/to/proj'
```

3. Load aliases
```bash
source ~/.bash_aliases
```

That"s it. Now you can see the aliases in the list. 

```bash
$ alias
```


## File scraping from Terminal 
Some quick and dirty command line shortcuts are essentials for day to day data analysis. 

1. Count the number of files in a directory

At the target directory enter,
```bash
ls -F | wc -l
```

2. List only top 10 (n) files from a directory
```bash
ls -U | head -10
```


3. Unzip zip files from command line. 

```bash
unzip file.zip
```


3. Move files from one directory to another. 

```bash
mv /path/to/source /path/to/destination
```


## 




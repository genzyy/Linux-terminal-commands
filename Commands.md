<div align=center>
  <h1>Commands</h1>
</div>

# Commands

## df

- The `df` command gives you a breakdown of entire storage systems that are connected to the host device.

## du

- The `du` command gives the size of the files in the current working directory.

## head

- The `head` command prints first 10 lines of the file by default.
- If we want to give a custom number, then we can do that by running

```zsh
$   head -n 5 <file-name>
```

## tail
- The `tail` command prints last 10 lines of the file.
- Same as `head` we can pass a custom number of lines to that are needed to be printed by running

```zsh
$   tail -n 5 <file-name>
```

## diff

- The diff command gives difference of text lines between the two files passed as an argument.

## locate

- We can use this command to locate a file on the host storage.
- On linux there are two packages available, `plocate` and `mlocate`. The latter one is more secure as it only shows user accessible files, and the first one shows everything.

## find

- We use this command to find files and directories in the current or directory passed as an argument.
- To find only directories, run

```zsh
$     find . -type f
```

- To find only files, run

```zsh
$     find . -type f
```

- To find a file with some name, run

```zsh
$     find . -type f -name "*.txt"
```

- The above commands are case-sensitive. If we want to make it non case-sensitive

```zsh
$     find . -iname "*.txt"
```

- To find all the files that were modified 20 mins before,

```zsh
$     find . -type f -mmin -20
```

- To find all the files that were modified more that 15 mins ago.

```zsh
$     find . -type f -mmin +15
```

- If we want to find files according to a date, run

```zsh
$     find . -type f -mtime -10
```

- Search files by their size

```zsh
$ find . -size +1k
```

- Find empty files by running

```zsh
$   find . -empty
```

- To find files with their permissions, run

```zsh
$   find . -type f -perm 777
```

- Find files and then do something with them

```zsh
$   find . -type f -name "*.txt" -exec rm -rf {} +
```

## grep

- `grep` means global regular expression print.
- This command is case-sensitive.

- To find a word in the file,

```zsh
$   grep "<word-here>" <file-name>
```

- To find exact word in the file,

```zsh
$   grep -w "<word-here>" <file-name>
```

- To make the search non case-sensitive,

```zsh
$   grep -i "<word-here>" <file-name>
```

- To find the line number of the given word (if exists) in the file,

```zsh
$   grep -n "<word-here>" <file-name>
```

- To show previous three lines that are before the given word (if exists) in the file,

```zsh
$   grep -B 3 "<word-here>" <file-name>
```

- To find the given word in current directory, run

```zsh
$   grep -win "<word-here>" ./*.txt 
```

- We can use recursive tag here to search in the directories inside the current directory

```zsh
$   grep -rwin "<word-here>" <file-name>
```

- To get the filenames which contain the given word, run

```zsh
$   grep -wirl "<word-here>" <file-name>
```

- To get the count of how many times the given word appears in a file in the directory,

```zsh
$   grep -wirc "<word-here>" <file-name>
```

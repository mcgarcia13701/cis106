# Notes Lecture 04 | Manipulating files and directories

## Managing files and directories
* Commands are often followed by **options** that modify/enhance their 
behavior.
* Commands are also followed by **arguments** which are the items open which the command acts on.
![options](../notes/option.png)

### Creating Directories
#### The mkdir command
* **mkdir** - is used to make directories
* To create a directory with mkdir type: **mkdir + the name of the directory**.
* To create multiple directories, you will need a space in between
* **mkdir directory/** to make a directory within a directory
* You can create directories in the present working directory or in a different directory by using an absolute path or relative path.
* Directories are case sensitive
* Directory name with quotes will allow a space in the name of the directory
* **mkdir -p** to create a directory with a parent directory at the same time

### Creating Files
#### The touch command
* **touch** - is used to create files
* **touch list**
* To create several files in one command you will need a space in between

### Deleting files and directories
#### The rm command
* **rm** - is used to remove files
* **rmdir** - to remove empty directories
* **rm -r** - to remove nonempty directories

### Moving files and directories
#### The mv command
* **mv** - moves and renames files/directories
* **mv + source + destination** - to move files and directories
* **mv + file/directory to rename + new name** - renaming files/directories

### Copying files and directories
#### The cp command
* **cp** -  copies files/directories from a source to a destination
* **cp + files to copy + destination** - to copy files from a source to the destination
* **cp -r + directory to copy + destination** - to copy directories 

###Working with Links
#### Inodes(index files)
* **Inode** - a data structure that contains all the info about a file excpet its file name and its content
* Every file in the file system has an inode number
* An inode number references as entry in the inode table
* To view a files inode number, use the ls -l command
* To display the inode data on a file or directory use the stat command
* Each partition on a hard drive has its own inode table and every file has a unique inode number

#### Hard Links
* Hard links are files that point to data on the hard drive
* When you create a file, it’s automatically linked to the data stored in the hard drive and it is assigned an inode number
* When you create a hard link to any file it does not create a copy of the data
* Hard links must be created on the same partition
* Because hard links point to the same data they share the same inode number
* Data on a hard drive is not deleted until every link is deleted
* If you change data on any link, all hard links are changed because the data on the hard drive was changed
* To create a hard link: ln file ~/Downloads/fileHL 

#### Soft Links
* **Symbolic links (soft links)** are a special type of file that point to other files instead of data in the hard drive
* Soft links do not share the same inode number as hard link do
* If you modify a soft link, the original is edited too
* To create a symbolic link: **ln -s file fileSL**

### Getting Help!
* **Man (manual)** pages are documentation files that describe Linux shell commands, executable programs, system calls, special files, and so forth. 
* To view the manual of a command type: **man + command**. 
  * Ex: *man ls*
* To exit the man page press letter “**q**”

### Using Wildcards / File Globbing
* **Wildcard** represents letters and characters used to specify a filename for searches. 
* **File globbing** is the processing of pattern matching using wildcards. 
* The wildcards are officially called metacharacter wildcards.

#### The * Wildcard
* The main wildcard is the * character
* A star alone matches anything,nothing and matches any number of characters
* Example: ls *.txt will match all files that end in .txt regardless of the size of the file name.
* Examples for when you use the * wildcard:
  * When you want to list all files with a particular file extension
  * When you do not remember a file name.

#### The ? Wildcard
* The ? wildcard metacharacter matches precisely one character. You might need it to minimize a long list of files names down to a few.
* Useful for working with hidden files
* If you want to list all hidden files you can use: ls .??* which will match all files that start with a . or .. and have any character after it.

#### The [ ] Wildcard
* The brackets wildcard is used to match a single character in a range
* The brackets use the exclamation mark to reverse the match.
  * Ex: match everything except
vowels [!aeiou] or any character except numbers [!0-9]
  * Ex: To match all files that have a vowel after letter " f ": 
    * **ls f[aeiou]***

#### Brace Expansion
* **Brace expansion {}** is not a wildcard but another feature of bash that allows you to generate arbitrary strings to use with commands.
* To create a whole directory structure in a single command:
  * **mkdir -p music/{jazz,rock}/{mp3files,vidoes,oggfiles}/new{1..3}**
* To create a N number of files use:
  * **touch website{1..5}.html**
* Remove multiple files in a single directory
  * **rm -r {dir1,dir2,dir3,file.txt,file.py}**





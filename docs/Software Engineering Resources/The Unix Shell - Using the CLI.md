> **Resources**
> - [The Unix Shell](https://swcarpentry.github.io/shell-novice/)
> - [Conquering the Command Line](https://www.softcover.io/read/fc6c09de/unix_commands/basics#uid31)

People can interact with computers using graphical user interface (GUI), giving instructions to the computer by clicking a mouse, typing on the keyboard, and using menu driven interactions. 

Another way we can give instructions to the computer is utilizing [***Unix Shell***](https://swcarpentry.github.io/shell-novice/01-intro.html), which is both a *command-line interface (CLI)* and a *scripting language*. 
### Note:
* A ***shell*** is a program whose primary purpose is to read commands and communicate with the Operating System to executing those commands and run programs. 
* You work with the Unix Shell when you write commands in the command-line prompt on your computer's Terminal (which is a type of CLI).
* The most popular Unix Shell is ***Bash***, there is also ***Zsh***, an extended shell more user-friendly enhancements over Bash. 
* The shell's main advantages over GUI are:
	* high action-to-keystrokes ratio
	* its support for automating repetitive tasks
	* its capacity to access networked machines
* The disadvantages to using the shell is knowing what commands need to be run and how to run them. 

# Basic Commands & Options
### General Syntax of a Shell Command
![](https://i.imgur.com/oOT7kF9.png)
### 1. Commands 
1.  `↑` and `↓` : helps you scroll through the command lines you used in your terminal.
2. `whoami`: returns the computer's user name. 
3. `ls`: short for listing. By itself, this command lists the contents of the current directory. 
	* You can specify a directory path (that exists in your current directory). `ls [path]` will list all the files/directories inside that specified directory. 
		* *Example*: `ls Desktop/web-development-path` → all the files inside of `web-development-path` directory will be listed.
	* `ls -F`: tells `ls` to add a marker to the listed file and directory names to indicate what they are. *Example*: `ls -F User/Desktop/web-development` → lists all the files and directories in `web-development` with indicative marker. 
		* a trailing `/` indicates that this is a directory
		* `@` indicates a link
		* `*` indicates an executable
	* `ls -F -a` = `ls -Fa`: show all directories and files, including hidden files
	* `ls -R`: list all nested subdirectories within a directory.  ^d3f56e
1. `pwd`: short for print working directory. This command returns the path to the current directory you are in. 
2. `cd`: by itself,  it navigates user back to the home directory. If we specify a path, `cd [path]` takes us from the current directory to the directory we’d specify in the path. The directory we specify to move to must be visible from our current directory. 

The image shows the file system organization. 
![](https://i.imgur.com/DAaiMvZ.png)

 *  *Example*: `cd Users/nelle` → we go inside `nelle` directory.
* `cd ..` → we go back up a directory level in the system, if we were at `Users/nelle` we’re now at `Users`. If we`cd ../../` → we go back up two levels in the system. 
* `cd -` → go back to the directory we were previous at.
* `cd ~` → go straight to the user’s home directory. 
* `cd /` → go straight to the user’s root directory. 
6.  `man`: a command you can add to the start of any command to read that command's manual. 
	* *Example*: `man ls`

### 2. Options
Options can either start with a single dash (-), known as **short options**, or start with (–-), known as the **long options**. There’s always space between the command and the options. 
1.  `--help`: an option that can be added to the end of any command to displays more information on how to use that command. 
	* *Example*: `ls --help`. 
	* *Note: this option may not be supported with zsh*
2. `-a`: stands for all.
3. `-i`: when used with a command, it prompts the user for confirmation before executing the action, adding a layer of safety to prevent unintentional execution.  ^6eb1b9
4. `-r`: stands for recursive, used to remove/copy the entire directory and their sub content → removes a directory even when it contains other content. 

Note that in most command line tools, multiple options can be combined with a single `-` and no spaces between the options; `ls -F -a` is equivalent to `ls -Fa`, `ls -F -R` = `ls -FR`

# Working with Files and Directories
### Creating and Removing Files/Directories
1. `mkdir [/path/to/directory]`: make a ***directory*** in the current working directory/specified directory path.
	* You can make more than 1 directory, `mkdir directory1 directory2`
	* `mkdir -p [directory_name/nested_directory_name]`: make a directory with *subdirectories* nested inside. *Example*: `mkdir -p my_directory/nested_directory1/nested_directory2`
	* Using [[The Unix Shell - Using the CLI#^d3f56e|ls-R]] can help to list all the subdirectories. 
 2. `nano [/path/to/text_file.txt]`: opens the specified file in the nano text editor. If the file doesn’t exist, the command will create a *text file* at the current directory/specified directory path. *Example*: `nano document.txt`. 
	 * An editor window will pop-up with instructions allowing you to write to/save content to the text file you’ve created. Usually, you use `ctrl + O` to write the data to the file and `ctrl + X` to quit the editor and return to the shell.  
3. `touch [/path/to/file]`: create a new *empty, blank* file in the current directory/specified directory path. *Example*: `touch index.js`. You can specify any filename extension for the file (eg: .pdf, .html, etc.) when using `touch`. 
4. `rm [/path/to/file]`: remove the file specified from the current directory/specified directory path.
	* `rm -r [path/to/directory`: removes specified directory and its content.
5. `rmdir [/path/to/directory]`: remove the directory specified from the current directory/specified directory path.. If the directory has files/subdirectories, this command will not remove it. 

Note: Unix Shell doesn’t have a trash bin for recovering deleted files like when we delete files with GUI. When we delete files, they are permanently deleted and unlinked from the file system. 
→ We can add the [[The Unix Shell - Using the CLI#^6eb1b9|-i]] option to prompt Y/N before deletion for better confirmation. 
*Example*: `rm -i [path/to/file]`
### Moving Files/Directories
`mv`: move and/or rename files and directories.
* `mv [file/directory_name] [/path/to/new/destination]`: move files/directories to a new directory. 
	* *Example*: `mv document.txt nested_directory1` → the file `document.txt` will be moved to directory `nexted_directory1`
	* You can move more than 1 file/directory at the same time to a new destination directory. *Example:* `mv document1.txt document2.txt /Desktop/my_directory` → move 2 files to `my_directory`.
* `mv [old_file_name] [new_file_name]`: rename a file/directory to the new name in the same directory. *Example*: `mv old_document.txt new_document.txt`.
* `mv [/path/to/old_file_name] [/path/to/new_file_name]`: moves **and** renames the file from the source directory to the destination directory. *Example*: `mv /my_folder/old_document.txt /new_folder/new_document.txt`

While you can move/rename many files/directories in one command, doing so can cause confusion and accidental mistakes. 
### Copying Files/Directories
`cp`: copies files/directories instead of moving it, `cp [path/of/old_file] [path/of/new_file_name]`
* `cp original.txt copy.txt` 
	* →  If `copy.txt` doesn’t exist, it creates a new file that’s a copy of the `original.txt`. 
	* → If `copy.txt` exists, it overwrites the data in `copy.txt` with the data of `original.txt`.
* You can copy more than 1 file to a specified directory. *Example:* `cp document1.txt document2.txt /Desktop/my_document` → the two .txt files will be copied to `my_document` directory.*** In this case, the last argument for the command must be a directory.*** 
* `cp -r [my_directory] [backup_directory]`: does the same thing above, but for directories. 

# Wildcards
1. `*`: represent zero/more other characters. 
* `ls *.pdf`: lists all the files ending with `.pdf`
* `ls hello*`: lists all the files starting with `hello`
* `ls h*o`: list all the files containing a word starting with `h` and ending with `o`.
2. `?`: works similar to `*` but represents exactly one character. 

# Pipes and Filters

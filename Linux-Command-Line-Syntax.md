[\<\-Back](http://euclid.nmu.edu:3000/ovoisine/CS326/wiki/Linux)<br>
Page is Subject to Frequent Updates<br>

# Linux Command Line Syntax, or BASH
To be used in a Linux command line environment, such as Windows Subsystem for Linux, Ubuntu, and more.<br>
The general format for Linux command goes command > dash > augmentation letters > additional arguments<br>
For this particular format, `-_` represents a dash followed by multiple, single character command augmentations, of which useful or relevant {or ones that I care about} will be listed below<br>
`--help` can be used as an argument with any command to print information on that command<br>

### A note on Scripts
A shell script is typically denoted using the .sh extention, but they can have no extention if desired. What denotes them as a shell sceipt is the shebang in the first line of the file, for example `#!/bin/bash`, which both informs the shell that when it runs the file, it should be executed as a shell script, as well as provides a path to the bash interperater. Adding the `set -x` on the line after the shebang will let your script enter debugging mode. These scripts are simply a way to automate shell commands, and other than the fact that they are kept in a file rather than entered manually, are no different than entering these commands manually. As an aside, comments in scripts, otherwise useless in the shell, are declared with \#.<br>
Scripts can be run in mutiple ways as seeen below.<br>
**sh \_\_**<br>
**bash \_\_**<br>
**./\_\_**<br>

## Operators and Coding Functionality

### Varables
When being set, varables are repersented as `__=___`, or as a new name. When being referanced, varables are repersented as `$__`. Varables are case sensetive, begin with a letter or underscore, and should not contain whitespace or special characters.<br>
`+=` and `-=` can be used to incriment and decriment values respectively.<br>
for example: `person_name=$name_of_user`<br>
Command line arguments are automatically set as $0, $1, $2, $3, and so on. $0 is always the name of the program being run and the rest is each subsiquent argument.<br>
A special varable knows as an exit code can be set by the program to indicate errors. This can be referanced with `$?`. If this exit code is 0, the program had no error. The `set -e` option can also be used to exit a script at any pointif the script fails.<br>

### Inputing and outputing to file
The files can be written to and read from using specific operators.<br>
`<`<br>
`echo "___" > __` writing text over a file.<br>
`echo "___" >> __` appending text to a file.<br>

### Logical Operators
When writing a condition, special logical operators can be used to compare or relate values.<br>
 **-a** and<br>
 **-o** or<br>
 **-gt** greater than<br>
 **-lt** less than<br>

### Loops and Conditions

#### While
While condition is true, execute this code.<br>
`while [___]; do ___ done`<br>

#### For
For each item in this set, execute this code. In this case, a set can be n array of numbers, for example `{1..3}` will run 3 times with the items 1, 2 and 3. A set can also be an array of items, in which case the code will be exicuted on each.<br>
`for __ in ___; do ___ done`<br>

#### Do
Do executes code within a container.<br>
`do ___ done`<br>

### If, Elif, and Else
Will decide to execute code based on a condition, or with the use of subsiquent elif's, mutiple conditions.<br>
```
if [___]; then ___
elif [___]; then ___
else
	___
fi
```
<br>

### Case Statments
Will decide to execute code based on a whether a specific input matches a number of cases. Is used as a shorthand for having mutiple, lenghtly if statments. A final pattern can be given containing only an *, meaning that it will execute if no other conditions were reached.<br>
```
case ___ in
	___)
		___
	;;
	___)
		___
	;;
	*)
		___
	;;
esac
```
<br>


## Commands

**bg %\_\_**(incorrect, needs more work)<br>
Moves a process to background, given by a number after a percent. This number can be determined using the jobs command.<br>

**cat \_\_**<br>
denotes opening a file stream for reading or writing to a file<br>
{somewhat complicated command that I don't know how to use yet}<br>

**cd \_\_**<br>
denotes moving the user to a different directory that is reachable from the current directory when given the path as an argument<br>
additional arguments include...<br>
~ or left empty for the user's home directory<br>
.. for going back one directory<br>
\\ for the root directory<br>

**chmod u+x \_\_**<br>
modifies the ownership of a file, given as an argument, to the current user with addition to the execution rights, given as the argument u+x. (`u` for the user, `+x` for the excution rights)

**clear**<br>
denotes clearing the current terminal of text<br>

**cp __**<br>
Copy a file or directory, given as an argument.<br>

**df**<br>
Display the ammount of disk space available.<br>

**echo __**<br>
Print something to terminal, given as an argument.<br>

**grep**<br>
Search for a pattern in a file.<br>

**history**<br>
shows a list of previously run commands.<br>

**jobs**<br>
Shows a list of ongoing or paused threads<br>

**kill -9 \_**<br>
Will kill a process given a process number as an argument<br>
-9 means just kill, no letting the process shut off like it wants or asking the process to shut off.<br>
I can't end the processes of others unless root, only mine.<br>
{I have found that if the process number has a 0 in it, you need to wrap the process number in ""}<br>

**ls \-\_**<br>
Returns a list of files and directories in the current directory<br>
-a show all, including hidden items<br>
-l show detailed view<br>

**mkdir \_\_\_**<br>
Create a directory in the current directory at the new path (or just name) given as an argument.<br>

**more \_\_**<br>
Display a text file page by page, hitting enter displays the next page.<br>

**mv __**<br>
Move or rename a file or direcotry, with the file given as an argument.<br>

**nano \_\_**<br>
denotes entering the nano editor, taking a file to to open with as an argument<br>
with no file name provided, it will open a blank editor<br>
{make sure to save the file after done editing, otherwise a new file will not be made and a old file will not be updated}<br>

**pm**<br>
Writes the status of the active processes.<br>
-m displays the associated kernel threads to standard output.<br> 
-o displays extra thread-related columns.<br>

**ps**<br>
Shows a list of running processes.<br>

**pwd**<br>
returns the path for the current directory<br>

**read \_\_**<br>
takes in the next user input ans sets it to a varable given as an argument.<br>

**rm \_\_**<br>
Delete a current file and directory, the path to which (or just name) is given as an argument, directories are not targeted by default.<br>
Multiple paths can be added with additional arguments
\* denotes all files from the end of that path
\*.\_ with a given file extension denotes deleting all of that file type.  With a "?" will delete all with an extension of one character in 
length.<br>
-i causes a warning prompt before each file is deleted<br>
-f causes any warnings that may pop up before a file is deleted to be ignored<br>
-d targets empty directories for deletion<br>
-r targets directories and all of their content for deletion<br>


**sleep \_\_\_**<br>
Pause the thread for a number of seconds.<br>

**ssh \_\_**<br>
allows a user access to a remote server by inputting a web server address as parameter one<br>
unless set up beforehand, it will likely need a username and password to login to the server<br>

**sudo ___**<br>
Run a command with administrative privlages, likely will have to provide a password for the machine you are using. This password is usually invisible so as to decrease the likelyhood of shoulder-peeking issues.<br>

**top**<br>
Shows a constantly updating list of ongoing processes and all associated information, including process names<br>

**touch \_\_\_**<br>
Create a file in the current directory with the new path (or just name) given as an argument.<br>

**uname -a**<br>
returns the user's system information<br>
{there are other possible augmentation letters but `-a` means all so unless you are trying not to clutter your screen you don't really need any others}<br>

**which bash**<br>
returns the location of the interpreter and .<br>

**whoami \_**<br>
returns the logged in user's name<br>
with `--version` as an argument, it will print the user's terminal information<br>

## Key Shortcuts
**ctrl+c**<br>
escapes a program awaiting an input<br>

**ctrl+u**<br>
clears the current line on input<br>

**ctrl+z**<br>
pauses the current thread<br>
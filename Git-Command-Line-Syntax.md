[\<\-Back](http://euclid.nmu.edu:3000/ovoisine/CS326/wiki/GIT)<br>
**Page is Subject to Frequent Updates**<br>

# Git Command Line Syntax
Git has different graphical user interfaces for ease of use. However people will often still use commands for text based interfaces for convenience and the potential for automation.<br>
Git commands are used in a Linux, Unix, Windows, or other supported OS text based interfaces that support git.<br>

**git \_**<br> 
denotes a command that will affect the current repository<br>
this is an essential piece of syntax that is typed in front of all following git commands<br>

## Commands

**add \_\_**<br>
denotes adding a file to be tracked with the current repository and branch as an argument<br>
this is used on every file that has changes before you use git commit<br>
https://git-scm.com/docs/git-add<br>

**commit -m "\_\_\_"**<br>
denotes committing all changes in all files to the current repository and branch<br>
should include, but does not strictly require, a message describing changes as an argument after -m<br>
https://git-scm.com/docs/git-commit<br>

**branch**<br>
shows a list of branches and which one is currently being used when argument is not given<br>
\_\_\_ creates a new branch with the name given as an argument<br>
-d \_\_ deletes an existing branch with the name given as an argument<br>

**rm \_\_**<br>
denotes removing a file from being tracked with the current repository as an argument<br>
https://git-scm.com/docs/git-rm<br>

**clone \_\_**<br>
denotes making a copy of a repository given as an argument with the new directory's name being the name of the .git file given<br>
for example, 
```
$ git clone https://github.com/A-Scientist/elusive-goat.git
Cloning into 'elusive-goat'...
```
https://git-scm.com/docs/git-clone<br>
    
**push**<br>
denotes taking changes made to the current local repository and branch and making them to the corresponding remote repository and branch<br>
--set-upstream origin \_\_ creates a branch on the server that matches the local branch whose name is given as an argument. is only necessary when the server does not have a branch that matches the one being used locally.<br>
https://git-scm.com/docs/git-push<br>
--set-upstream origin???<br>
    
**pull**<br>
denotes taking changes made to the corresponding repository and branch and making them to the local repository and branch<br>
origin \_\_ denotes pulling changes from the server branch and not the local branch<br>
https://git-scm.com/docs/git-pull<br>
    
**merge**<br>
"Join two or more development histories together" not entirely sure<br>
https://git-scm.com/docs/git-merge<br>
    
**status**<br>
displays all untracked files in the current repository and branch<br>
https://git-scm.com/docs/git-merge<br>

**checkout \_\_**<br>
switch to a branch whose name is given as an argument<br>
https://git-scm.com/docs/git-checkout<br>

**reset --hard**<br>
forces the current branch to ignore changes you have made when about about to pull from a repo.<br>

**rm**<br>
remove files from the working tree and index<br>
-rf?<br>
https://git-scm.com/docs/git-rm<br>


**clean**<br>

## Key Shortcuts

## Definitions

### States
Files are typically in one of three states
<ul>
<li>Modified means that you have changed the file but have not committed it to your database yet.</li>
<li>Staged means that you have marked a modified file in its current version to go into your next commit snapshot.</li>
<li>Committed means that the data is safely stored in your local database.</li>
</ul>

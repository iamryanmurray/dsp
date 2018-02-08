# Learn command line

Please follow and complete the free online [Bash Scripting Tutorial](https://ryanstutorials.net/bash-scripting-tutorial/) or [Codecademy's Learn the Command Line](https://www.codecademy.com/learn/learn-the-command-line). These are helpful tutorials. You should be able to go through these in a couple of hours.

**Note:** Bash is not installed on a PC. Rather, PC users must install Cygwin. Once Cygwin has been installed, the command line interface witll _emulate_ bash. You can find all information regarding Cygwin [here](https://www.cygwin.com/).

---

### Q1.  Cheat Sheet of Commands  

Here's a list of items with which you should be familiar:  
* show current working directory path
* creating a directory
* deleting a directory
* creating a file using `touch` command
* deleting a file
* renaming a file
* listing hidden files
* copying a file from one directory to another

Make a cheat sheet for yourself: a list of at least **ten** commands and what they do.  (Use the 8 items above and add a couple of your own.)  

> > 

* show current working directory path: pwd
* creating a directory: mkdir new_directory
* deleting a directory: rm -r directory
* creating a file using `touch` command: touch new_file
* deleting a file: rm filename
* renaming a file: mv old_name new_name
* listing hidden files: ls -
* copying a file from one directory to another: cp source_file destination
* run command with super user priveleges: sudo command
* change to directory one level up: cd ../

---

### Q2.  List Files in Unix   

What do the following commands do:  
`ls`  
`ls -a`  
`ls -l`  
`ls -lh`  
`ls -lah`  
`ls -t`  
`ls -Glp`  

> > 
ls: short listing  
ls -a: listing including hidden files  
ls -l: long listing  
ls -lh: long listing with human readable file sizes  
ls -lah: long listing including hidden files with human readable file sizes  
ls - t: sort by modification time, newest first  
ls - Glp: long listing, don't print group names, append / indicator to directories  


---

### Q3.  More List Files in Unix  

Explore these other [ls options](http://www.techonthenet.com/unix/basic/ls.php) and pick 5 of your favorites:

> > 

ls -q: display all nonprinting characters as **?**  
ls -R: display subdirectories as well  
ls -1: display each entry on a line  
ls -u: display the files by file access time  
ls -f: interprets each name as a directory, not a file  

---

### Q4.  Xargs   

What does `xargs` do? Give an example of how to use it.

> > The xargs command allows one to build an execution pipeline from standard input.  It allows tools like rm and mkdir to accept standard input as arguments.  

An example of xargs use is with the find command:  

`find /tmp -mtime +14 | xargs rm`

This take any files in the temp folder older than two weeks and pipe them to the rm command with xargs.

 


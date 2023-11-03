## File Perms
3 users
	Owner
	Group
	Other
3 types of access
	read
	write
	execute
To view perms on a file ```ls -l```
char 0 = filetype
chars 1-9 = file perms
(-)(---)(---)(---)
file type - owner - group - everyone
r = read
w = write
x = execute
o = others
g = group
u = user (you)

change perms with ```chmod``` command
```chmod (user group)(+ to give or - to remove)(access) (file)``` 

## Processes
```ps -f``` lists processes, -f option shows more info
PID = process id #
PPID = process parent id #
Ctrl C kills process
Ctrl Z suspends process
```jobs``` shows status
```kill -9 pid``` kills suspended processes
## Aliases
add in ~/.bashrc (or other file for it to read)
create an alias in terminal ```alias dog='echo dog'```

## Bash Scripting
$ - used to designate a variable
$(0-9) arguments 0 through 9


## Sed
Used to find matches in a string
by default 

## Gawk
OFS = output field seperator
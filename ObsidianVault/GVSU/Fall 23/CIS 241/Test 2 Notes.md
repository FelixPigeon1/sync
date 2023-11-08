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

```c
#! /usr/bin/env gawk -f
BEGIN {
    FS="\t"
    OFS=","
    SUM=0
    CNTNEW=0
}
#Look for regex pattern matches field 3 then perform the actions in the {}
#these in the middle are for every record in the file
$3 ~ /200[0-9]/ {
    SUM+=$5
    CNTNEW += 1
}
#for every line, makes of first field increment by one
{makes[$1] += 1}
{print NR, toupper($2)}
END {
    print SUM, CNTNEW
    #for key in makes, print key and number of makes
    for (key in makes) print key, makes[key]
}
```
BEGIN {} - this is where to initialize variables
$(n) - the nth field on a given record
	Record - rows
	Field - columns
~ - look for regex
(field to pull from) (equal or ~ for regex ) (pattern to match) {(Actions to perform on said field)}

functions:
	length(str) = # of chars
	int(num) = integer portion of num

- **NR:** NR command keeps a current count of the number of input records. Remember that records are usually lines. Awk command performs the pattern/action statements once for each record in a file. 
- **NF:** NF command keeps a count of the number of fields within the current input record. 
- **FS:** FS command contains the field separator character which is used to divide fields on the input line. The default is “white space”, meaning space and tab characters. FS can be reassigned to another character (typically in BEGIN) to change the field separator. 
- **RS:** RS command stores the current record separator character. Since, by default, an input line is the input record, the default record separator character is a newline. 
- **OFS:** OFS command stores the output field separator, which separates the fields when Awk prints them. The default is a blank space. Whenever print has several parameters separated with commas, it will print the value of OFS in between each parameter. 
- **ORS:** ORS command stores the output record separator, which separates the output lines when Awk prints them. The default is a newline character. print automatically outputs the contents of ORS at the end of whatever it is given to print.
# LinuxCommandCheetsheet

1. alias your_cmd_name = [a command sequence]
```
alias cls = clear

alias pf="ps -e | grep $1"
    usage: pf shutter
```

2. cat filename --> List the content of the files to terminal window
```
cat .bash_logout

cat .bashrc | less
```

3. chmod 777 example.txt
```
-rwxrwxrwx: 
    0th: - is a file ; d is a directory
    123: File permisions of the owner
    456: File permission of the group
    789: File permission of the others
```

4. chown owner:group example.txt --> Change the owner/group of a file
```
sudo chown dave:marry example.txt     // Dave as owner, marry as group owner
sudo chown marry:marry example.txt    // change both owner and group to marry
```

5. curl url   --> to retrieve information and files from URLs
```
curl -s https://raw.githubusercontent.com/torvalds/linux/master/kernel/events/core.c -o core.c
```

6. df      --> shows the size, used space and available space on the mounted filesystem of the computer
```
-h: human readable
-x: exclude
```

7. diff    --> compare two text files and shows the differences between them
```
-y: side by side
-w: max line width to use to avoid wraparound lines.
--suppress-common-lines: prevents diff from listing the matching lines.
```

8. echo $PATH   --> Print a string of text to the terminal

9. find [scope] -name [pattern]
```
find . -name *ones
```

10. finger user     --> give information about a user
```
finger marry
```

11. free     --> summary of the memory usage
```
-h: human readable
free -h
```

12. grep      --> searches for lines which contains a search pattern
```
grep train *.txt
```

13. groups user  --> tells you which groups a user is a member of
```
groups dave
```

14. gzip file     --> compress files
```
-k: keep both the original file and the compressed file

gzip -k core.c
```

15. head     --> list the first 10 lines of a file
```
-n: number of lines you want to see

head -n 5 core.c
```

16. history    --> command history list, can call by !num
```
history
!20
!!   // repeat the previous command
```

17. kill processId   --> kill process
```
kill 1234
```

18. less filename    --> allows you to view files without opening an editor. 
```
less core.c

ls -R / | less
```

19. top     --> shows the real-time display of the data
```
us: value is the CPU time the CPU spends executing processes for users, in “user space”
sy: value is the CPU time spent on running system “kernel space” processes
ni: value is the CPU time spent on executing processes with a manually set nice value
id: is the amount of CPU idle time
wa: value is the time the CPU spends waiting for I/O to complete
hi: The CPU time spent servicing hardware interrupts
si: The CPU time spent servicing software interrupts
st: The CPU time lost due to running virtual machines (“steal time”)


PID: Process ID
USER: Name of the owner of the process
PR: Process priority
NI: The nice value of the process
VIRT: Virtual memory used by the process
RES: Resident memory used by the process
SHR: Shared memory used by the process
S: Status of the process. See the list below of the values this field can take
%CPU: the share of CPU time used by the process since last update
%MEM: share of physical memory used
TIME+: total CPU time used by the task in hundredths of a second
COMMAND: command name or command line (name + options)


The status of the process can be one of:
    D: Uninterruptible sleep
    R: Running
    S: Sleeping
    T: Traced (stopped)
    Z: Zombie
```

11. uname        --> system information regarding Linux computer
```
uname -a : see everying
uname -s : see kernal name
uname -r : see release
uname -v : see version
```

12. w      --> list the currently logged in user
```
w
```

13. whoami
```
whoami
```

14. dirs, pushd, popd
```
>> pushd /a/b/c
>> popd +1
https://www.tecmint.com/pushd-and-popd-linux-filesystem-navigation/
```

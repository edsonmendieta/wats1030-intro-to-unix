# *nix Scavenger Hunt

Complete the following challenges using the command-line interface on your favorite
Unix or Linux operating system. You are welcome and encouraged to consult any
additional documentation online or in books.

Please add your answers/responses/text pastes to the document after each prompt.

Note: For some of the challenges you will need to reference files included with
this repository, so you will need to fork the repo into your own Github account
and then clone it to your development environment.

## The Challenges

### Navigating the Filesystem

* Get an idea of where you are in the operating system. Use the `pwd` command to find your "path to working directory"--your current location in the filesystem of your devbox. *Paste the output of the `pwd` command here:* /home/cabox/workspace


* Discover more about this filesystem. Use `ls` (the "list" command)to see what is in this directory. *What directories and files do you see when you run `ls`?* LICENSE  README.md  challenge_files  nix_scavenger_hunt.md  nix_scavenger_hunt_stretch.md


* You can use *options* to modify how a command runs. Try using `ls -alh` to see the contents of your current directory. *How are the results different when you use the `-alh` options?* Instead of just listing the files in the directory, for each file, it shows: if it's a directory, the permisions (owner, group, and world), number of links, the owner and group, size, and time and date of last modification.


* The `man` ("manual") command tells you more about how any given command works. (*WARNING:* CodeAnywhere does not support the man command. You can click the following link to complete this task: http://linux.die.net/man/)Run `man` to see instructions about how to use `man`. Then use `man` to learn what the `a`, `l`, and `h` options mean when used with the `ls` command. *Write down what those options do?* 
a: includes directory entries whose name begins with  a "." 
l: lists in long format (like what you get when you use "ls -alh") and a total sum of all file sizes is output on a line before the long format listings. The output is one entry per line. 
h: When used with a long format option, uses unit suffixes for file sizes in order to reduce number of digits used.


* Commands can also take *arguments*, which are usually the names of files or locations that you want the command to work with. Try running `ls /` to see what files are in the *root* directory of the filesystem. *What files and directories do you see listed?*
bin  boot  dev  etc  fastboot  home  lib  lib64  media  mnt  opt  proc  root  run  sbin  srv  sys  tmp  usr  var 


* A Unix filesystem has a few special shortcuts to refer to specific locations. `/` indicates the *root* of the filesystem, meaning the top-most directory in the filesystem hierarchy. Use the `cd` ("change directory") command to move to the root directory. (Hint: Use `man` to look up the `cd` command if you have any issues) *Then run `pwd` and paste the output here:*
/home/cabox (by using: "cd .." I was able to get to /home, but I'm not sure if that's what task is asking for.)


* Another special shortcut in Unix is the `~` location. This indicates the *user root* directory, meaning the top-most directory in the hierarchy that comes below your user account. Use `cd` to move to `~`. *Run `pwd` and paste the response here:*
/home/cabox



* Change directory into the `challenge_files` directory. Use `ls` to find only the files with a `.demo` pattern. *How many files do you find?* 
3 files 
(I orignally tried to use "ls .demo*" which didn't work since the ".demo" is at the end of the file name. So, I ended up using "ls | grep .demo" which worked great since it searches all instances of the pattern and not just the start, middle, or end. That said: "ls *.demo works but you have to have an idea of the pattern's placement in the name. )



* Use the `cd` command to move "up" one directory. *Where are you in the filesystem now?*
/home/cabox/workspace


* Press the up arrow on your keyboard. *What just happened?*
It showed me my last command input: "pwd".



* Use the `cd` command to move "up" one directory. *Where are you in the filesystem now?*
/home/cabox

​

* Press the up arrow on your keyboard. *What just happened?*
Showed me my last command input: "pwd".
​

* Press the up arrow a few more times. *What do you see?*
The command I inputed 3 commands ago: "cd ..".
​

* Run the `history` command. *What do you see?*
All of the commands I have inputed in chronological order from my current session in the terminal. 
​

### Observing the System

​

* Discover what account you are logged into using the `whoami` command. *What username are you currently using?*
cabox

* Discover who else is on your system with the `who` command. *Are any other users using your system? If so, list them here:*
No.

* How long has your system been running? Use `uptime` to see, and *paste the result here:*
 20:13:52 up  2:40,  1 user,  load average: 0.00, 0.00, 0.00  


* Run `ps aux` and review the results. (Hint: Use `man` to learn more about the `ps` command and options.) *How do you interpret what you see here?*
USER-Shows the user associated with each process (the owner of the process).
PID- Process ID
%CPU- CPU time used divided by time process has been running.
%MEM- Ratio of process's size to pyshical memory on machine.
VSZ- virtural memory usage of entire process.
RSS- Resident Set Size: non-swapped physical memory a task has used in Kb. 
TTY- Controlling terminal.
STAT- multicharacter process state. 
START- start time of process.
TIME- cumulative CPU time.
COMMAND- command + all its arguments.


* Run `top` and review the results. (Hint: You may need to use `ctrl-c` to get out of this app.) *How do you interpret what you see here?*
This is a real-time view of the running system and its process.
Row1: server uptime from last reboot, current logged in users, and cpu load on server.
Row2: Number of proccessess running on server and associated state. 
Row3: CPU utilization status on server. 
Row4: Memory utilization on server. 
Row5: Swap memory utilization on server. 
Row 6.Similar real-time/updating version of what is seen with "ps aux" command.
​

### Finding and Viewing Files

​

* Make sure you are in the `challenge_files` directory. Use the `*` wildcard to find all the files that have the word "credit" in the filename. *How many files did you find?*
2


* Use the `more` command to view one of the `credit_cards` files you just discovered. (Hint: Type `q` to quit viewing the file. Press the `spacebar` to page down. Use your keyboard arrows to move up/down.) *What is the date in the file you have viewed?*
1-15-2015


* Use the `find` command to search for files more effectively. Search the sub-directories under `challenge_files` to find the location of the file named `modi_laboriosam.txt`. *Where is that file located?*
Inside the tmp directory.



* Use the `grep` command to search for text within a file. Use `grep` on all the `.user` files in `challenge_files` to find which files contain "WA" (the abbreviation for Washington state). *How many files did you find?*
2



* Use the `-r` option of `grep` to *recursively* find the text "Waldo" hidden in a file somewhere under the `challenge_files` directory. *Paste the result showing the file and line where the word "Waldo" shows up.*
serial-numbers/eaque_molestiae.txt:Ut est maiores quia autem. Nisi modi Waldo sed corporis s
it explicabo ut est. Et est placeat ea sunt sunt consectetur sunt incidunt. Explicabo vel es
se blanditiis dolorem culpa non quia.

​

* Press the up arrow a few more times. *What do you see?*
My command input: "grep "WA" *.user


* Run the `history` command. *What do you see?*
All my command inputs in chronological order from my current session in the terminal.



### Pipes and Connecting Commands

* Sometimes it's useful to output the results of a command to a text file for further analysis, reference, or processing. Try running `ls > files.txt`. Notice that the file `files.txt` was created. View that file using `more`. *What do you see in the `files.txt` file?*
The files in the "challege_files" directory.


* Notice that if you run `ls -alh` in the `challenge_files` directory, the files scroll by very quickly. Sometimes it would be better to get the results in a paginated format. Try running `ls -alh | more`. *Describe what you see when you run `ls -alh | more`.*
The same output from the previous command but limited to displaying on page length at a time. I can view more by using the space bar. 


* Earlier, when you viewed the list of active processes on your devbox using `ps aux`, the list was probably really long. You can make this list more manageable by using the pipe (`|`) to filter the results of `ps` using `grep`. Run `ps aux | grep <your_username>` to see what processes are running for your specific user. *Paste the list of processes that reference your username here:*

root       522  0.0  0.6  63876  3336 ?        Ss   12:55   0:00 sshd: cabox [priv]         
cabox      524  0.0  0.2  64172  1524 ?        S    12:55   0:00 sshd: cabox@notty          
cabox      525  0.0  0.1  12924   960 ?        Ss   12:55   0:00 /usr/lib/openssh/sftp-serve
r                                                                                           
root       526  0.0  0.6  63876  3492 ?        Ss   12:56   0:00 sshd: cabox [priv]         
cabox      528  0.0  0.2  64008  1488 ?        S    12:56   0:00 sshd: cabox@pts/0          
cabox      529  0.0  0.3  18148  2060 pts/0    Ss   12:56   0:00 -bash                      
root       554  0.0  0.6  63876  3340 ?        Ss   13:04   0:00 sshd: cabox [priv]         
cabox      556  0.0  0.2  64012  1512 ?        S    13:04   0:00 sshd: cabox@notty          
cabox      557  0.0  0.2  13828  1516 ?        Ss   13:04   0:00 /usr/lib/openssh/sftp-serve
r                                                                                           
cabox      572  0.0  0.2  15520  1140 pts/0    R+   13:35   0:00 ps aux                     
cabox      573  0.0  0.1   8816   764 pts/0    S+   13:35   0:00 grep --color=auto cabo



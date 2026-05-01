| touch | touch          | Create file                  |
| ----- | -------------- | ---------------------------- |
| mkdir | make directory | Create a folder              |
| cp    | copy           | Copy a file or folder        |
| mv    | move           | Move a file or folder        |
| rm    | remove         | Remove a file or folder      |
| file  | file           | Determine the type of a file |

File permissions

| Section | Applies To | Example |
| ------- | ---------- | ------- |
| First 3 | Owner      | `rwx`   |
| Next 3  | Group      | `rwx`   |
| Last 3  | Others     | `rwx`   |
r = read
w = write
x = execute

| Permission    | Value |
| ------------- | ----- |
| Read (`r`)    | 4     |
| Write (`w`)   | 2     |
| Execute (`x`) | 1     |

| Group       | Permissions | Calculation                                          | Value |
| ----------- | ----------- | ---------------------------------------------------- | ----- |
| Owner       | `rwx`       | 4 + 2 + 1                                            | 7     |
| Group       | `rwx`       | 4 + 2 + 1                                            | 7     |
| Others      | `rwx`       | 4 + 2 + 1                                            | 7     |
|             |             |                                                      |       |
| `rwxr-xr-x` | 755         | Owner can do everything, others can read and execute |       |
| `rw-r--r--` | 644         | Owner can read/write, others can only read           |       |
| `rwx------` | 700         | Only the owner has access                            |       |
rwxrwxrwx = 777


SCP - secure copy allows to transfer files between two   computers using the SSH  
Source and Destination  
wget - download files from web via HTTP   
used python3 -m http.server with ssh to download files  from one vm to other via wget and HTTP  
ps - check your user system processes in terminal  
ps aux - check but all users  
top - real-time statistics about processes  
- SIGTERM - Kill the process, but allow it to do some cleanup tasks beforehand  
- SIGKILL - Kill the process - doesn't do any cleanup after the fact  
- SIGSTOP - Stop/suspend a process  

`systemctl [option] [service]` -  interact with the systemd process/daemon  
 
options:  
- Start  
- Stop  
- Enable  
- Disable  
- Status  


Crontab is one of the processes that is started during boot, which is responsible for facilitating and managing cron jobs.  
crontab -e  - edit crontab  

| Value | Description                               |
| ----- | ----------------------------------------- |
| MIN   | What minute to execute at                 |
| HOUR  | What hour to execute at                   |
| DOM   | What day of the month to execute at       |
| MON   | What month of the year to execute at      |
| DOW   | What day of the week to execute at        |
| CMD   | The actual command that will be executed. |
https://crontab-generator.org/ - makes crontab easier  

remember : ls -l -> long listing format - shows files with permission  

`iwconfig` - wireless network devices

`echo $SHELL` - check current shell

`cat /etc/shells` - check available shells for your OS

type the shell name you want to switch to, eg. :
-  `zsh` 
- `rbash`
-  `sh` 

to permamently change default shell:
`chsh -s /usr/bin/nameofshell` 

[[BASH - Bourne Again Shell]]
[[FISH - Friendly Interactive Shell]] 
[[ZSH - Z Shell]] 

[[Scripting in shell]] 
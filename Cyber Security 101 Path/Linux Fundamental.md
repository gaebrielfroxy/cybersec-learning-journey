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
crontabs - Crontab is one of the processes that is started during boot, which is responsible for facilitating and managing cron jobs.

| Value | Description                               |
| ----- | ----------------------------------------- |
| MIN   | What minute to execute at                 |
| HOUR  | What hour to execute at                   |
| DOM   | What day of the month to execute at       |
| MON   | What month of the year to execute at      |
| DOW   | What day of the week to execute at        |
| CMD   | The actual command that will be executed. |
https://crontab-generator.org/ - makes crontab easier
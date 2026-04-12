**CMD commands** 

`netstat` - display protocol statistics and current connections  
`/? / `help by the command - manual  
`systeminfo` - list various information about the system  
`more` - view long list page by page  
`driverquery` - Enables an administrator to display a list   of installed device drivers  
`help` before command - manual  
`cls` - clear cmd  
`ipconfig /all` - more info about ipconfig
view DNS servers and confirm that DHCP is enabled
`ping target_name` - send a specific ICMP packet and listen for a response
`tracert` - trace route
`tracert target_name` - trace the network route traversed to reach the target
`nslookup` - look up host or domain and returns its IP address
`nslookup example.com` - look up `example.com` using the default name server
`nslookup example.com 1.1.1.1` - look up usimg name server
`netstat` - displays current network connections and listening ports:
-  `-h` displays help
-  `-a` displays all established connections and listening ports
-  `-b` shows the program associated with each listening port and established connection
-  `-o` reveals the process ID (PID) associated with the connection
-  `-n` uses a numerical form for addresses and port numbers
- `-abon` - all options above
`tasklist` - processes list:
- `/FI` set filter
- `/FI "imagename eq example.exe"` - search task related to example.exe 
`taskkill /PID target_pid(e.g. 2115)` - kill process

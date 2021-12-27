# linux-command

~~~
LINUX file Editir :

line delete >> dd
Line copy   >> yy   :if want to copy 5 line , then set the coursor top of the line with in line five.
line paste  >> p    : if you want to repeat paste, type p more time.
line undu   >> u
top line    >> gg
last line   >> shift + G
start line end    >> shif + A
line break and inser mode >> o
specific line move >> 10G         : line number 10 we want to move .



ps -ef/ ps -aux	List currently running process in full format
ps -ax	List currently running process
ps -u <username>	List process for specific user
ps -C <command>	List process for given command
ps -p <PID>	List process with given PID
ps -ppid <PPID>	List process with given ppid
pstree	Show process in hierarchy
ps -L	List all threads for a particular process
ps --sort pmem	Find memory leak
ps -eo	Show security information
ps -U root -u root u	Show process running by root


info >> you will be seeing all the man page command 
evn  >> all information about your vm.

default LAN Interface directory locaion 
/etc/udev/rules.d/70-persistent-net.rules

Dhcpd lease location
/var/lib/dhclient
~~~

# linux-command
~~~
Linux Details

1.About Linux
Linux kernel name vmlinuz.
2.4.20 kernel version.
Linux tovalds
Finanland -  Helsinkey – 90/90 shal er dikay
HDD 0
C:dos	/dev/hda1
Swap	/dev/hda2
/boot	/dev/hda3
Extended	/home
	/var
	/etc

Windows	Linux	Scasi
Primary Master : HDD0	Had	Sda
Primary Slave : HDD1	Hdb	Sdb
Secondary Master : HDD2	Hdc	Sdc
Secondary Slave : HDD3	Hdd	sdd


Linxu er file system ext3
When we are going to install linux os then we have to do 3 partition.
/boot -> this is approximately 100MB
/swap -> we fixed space double of ram 
/ -> this is root directory
* running anaconda -> this is service that’s are detect hardware.
Inode -> have file information
Superblock ->
Root (/)  include all directory


/bin	Contains user related all commands
/boot	Contains linux kernel and boot file information.
/dev	All device related information contains this directory
/etc	All system server configuration related file contains this directory
/home	This directory contains all user information
/lib	Contains library file with share library.
/mnt	Contains system mounting information
/opt	Contain install third party packages such as office
/proc	A virtual file system that contains system information used by creating programs. Memory , cpu all information contains this directory.
/root	This is administrator home directory.
/sbin	Location of many system commands such as shutdown, /usr/sbin also contain many system command.
/tmp	Contains temporary file and directory
/usr	Contains file and directories directly relating to user of the system
/var	All log file (mail, proxy,apache etc) contain this directory. 
/lost+found	Used by fack to place file whose names cannot be found during file system repair. After scanning system it will store all bad in this directory
2.1 User/ Group Creation:
#adduser nabin				//username nabin
#useradd nabin
#useradd –G itgroup nabin		//nabin user create to itgroup
#groupadd itgroup
#passwd nabin
#adduser nabin –p test123      		// user and password same way command.
#grep nabin /etc/passwd		//user nabin information show
#grep itgroup /etc/group		//group itgroup information show
# id nabin				//user id and group id bydefault same.
#id itgroup
2.2 User/ Group Delete:
# userdel nabin    			//username nabin.
#userdel –r nabin			//user delete from all folder
#deluser nabin
#groupdel –r itgroup			// itgroup group name
2.3 Add User to Group
#usermod –G itgroup nabin		//add nabin user in itgroup
#usermod –G itgroup,cse,bba nabin 	//single user add in multiple group.
2.4 Change User and Group Name:
#usermod –l khan nabin			//nabin username change to khan
#groupmod –n newgroup itgroup	//itgroup groupname change to newgroup
2.5 User name , shell, and information check:
#finger nabin 				//nabin user details show
#chfn nabin				//extra information adding
#chsh nabin			              //use for user shell change
#vi /etc/passwd
nabin:x:502:502::/home/nabin:/bin/bash
description: username:passwd:user-id:group-id:(Information add):(/home/nabin:/bin/bash)user informaiton
2.6 User default shell and change default shell:
#vi /etc/shells
#vi /etc/default/useradd
SHELL=/bin/bash
2.7 New user default Shell Add:
#touch /bin/ppp
#vi /bin/ppp
Echo “this is Restricted Zone also Password Changing program”
Echo “Please Type your Confidential password”
Passwd						//for changing password
exit
:x
#chmod 755 /bin/ppp
#vi /etc/default/useradd
SHELL=/bin/ppp
:x

2.9 User Lock/Unlock:
#passwd –l nabin              //for lock nabin 
#usermod –L nabin	 //for lock nabin
#passwd –u nabin	//For unlock nabin
#usermod –U nabin	//For unlock
2.10 User Date Expire, Warning, Inactive, maximum and minimum days set:
#usermod –e 2009-06-01 nabin   // nabin user password expired on 01-06-09
#chage –w 5 nabin		// use getting warning to change password on 5th day.
#chage –I 0 nabin		//user inactive
#chage –m 5 nabin   		// nabin user password change min 5 days
#chage  -M 5 nabin		// password must be change within 5 days otherwise user disabled. 
2.11 Login Details/show user/groups:
#who				//who login computer 
#who –q 			//how many user’s login computer
#whoami			//find out who are you(user). Only information about user
#users				//how many users login same time
#w				//show detail login user information
#last 				//last login user with all login user details.
#last -5				//last 5 login user showing.
#finger 				//user information lookup
#groups			//which group you belong to
#id				//user and group id show
2.12 Operating System Check
#uname			//Operating System name
#uname –a			//Operating system name with kernel version.
#uname –I			//Show Architecture
#uname –n			//show host name and domain name 
#uname –m 			//show host system cpu type
#uname –r 			//Show kernel version
2.13 Boot Disk Creation
#mkbootdisk --device /dev/fd0 kernel_version	//Boot disk creation.




3. Details about files and directories
3.1 Change Directory:
#cd /etc/squid/abc			//entire absolute path parameter
# cd abc				//relative parameter
#cd ..					//to directory one level up
#cd .					//current directory
#cd 					//to move your root directory
#cd ~nabin				//change user nabin home directory
3.2 Show Directory Content and read file:
#ls					//show directory content
#ls –l					//show list of directory content
#ls  -a 					//show directory content with hidden file 
#ls –F 					//show file type 
#ls –ld					//show with content
#ls –R					//show directory recursively
#cat /etc/file
#cat /etc/file | more or | less
#less /etc/file
3.3 File / Directory Creation:
#touch filename			
#mkdir directory
#mkdir –p /root/dis/path/robi		//recursively directory creation.
3.4 Remove File/ Directory:
#rm filename
#rm –i filename				//remove forever.
#rm –R directory 
#rm –r directory			//Recursively delete directory
#rm –rf directory			//force with recursively directory delete. 	
3.5 Copy File and Directory:
#cp /etc/passwd /home/passwd
#cp –r /var/www/html /root/		//copy all content of directory
3.6 Move File and Directory:
#mv /etc/file /home
#mv –f /etc/dir	/home
3.7 File and Directory Rename:
#mv /etc/file	/etc/changefile		//file change to changefile name.
#mv /etc/mydir /etc/yourdir		//mydir change to yourdir

3.7 absolute pathnames & relative pathnames
# cd /var/www/html			//absoulate path
#pwd					//Print Working Directory
#cd /var				// Relatives path
#cd www
#cd html


~~~
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

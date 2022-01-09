#Overview of Linux (DAY 1)

#Ques. Features of kernel?
Ans. 
Memory management: Keep track of how much memory is used to store what, and where
Process management: Determine which processes can use the central processing unit (CPU), when, and for how long
Device drivers: Act as mediator/interpreter between the hardware and processes
System calls and security: Receive requests for service from the processes

#Ques. DIFFERENCE b/w LInux, unix and Windows?
Ans.  
Linux
Linux is open source . Linux is free to use.Linux is used in wide varieties from desktop, servers, smartphones to mainframes. Example- Ubuntu, Debian GNU, Arch Linux, etc.
Unix
Unix was developed by AT&T Bell labs and is not open source.Unix is licensed OS.Unix is mostly used on servers, workstations or Pcs. Example- SunOS, Solaris, SCO UNIX, AIX, HP/UX, ULTRIX etc.
Windows 
Windows is Close source. It is costly. Provides less security than linux.

#Ques. What do you mean by opensource?

Ans.  Open source software is code that is designed to be publicly accessible—anyone can see, modify, and distribute the code as they see fit.


#Ques. Explain the output of "ls -l" command.

Ans. The output from ls -l summarizes all the most important information about the file on one line. ... It precedes this list with a status line that indicates the total number of file system blocks occupied by the files in that directory.


#Ques. How does your OS know about the command functionality?

Ans. 
 
#Ques. How to create multipple files with single command.

Ans. Touch command can be used to create the multiple numbers of files at the same time. These files would be empty while creation.
     Syntax:
      touch File1_name File2_name File3_name 

#Ques. Where are unit files located?

Ans. Unit files are stored in the /usr/lib/systemd directory and its subdirectories, while the /etc/systemd/ directory and its subdirectories contain symbolic links to the unit files necessary to the local configuration of this host.

#Ques. Create a service file for nginx.

Ans. 

Save this file as /lib/systemd/system/nginx.service


[Unit]
Description=The NGINX HTTP and reverse proxy server
After=syslog.target network-online.target remote-fs.target nss-lookup.target
Wants=network-online.target

[Service]
Type=forking
PIDFile=/run/nginx.pid
ExecStartPre=/usr/sbin/nginx -t
ExecStart=/usr/sbin/nginx
ExecReload=/usr/sbin/nginx -s reload
ExecStop=/bin/kill -s QUIT $MAINPID
PrivateTmp=true

[Install]
WantedBy=multi-user.target

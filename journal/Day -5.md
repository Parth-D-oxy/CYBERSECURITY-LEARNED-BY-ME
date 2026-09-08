Level 18-19

task:- The password for the next level is stored in a file readme in the homedirectory. Unfortunately, someone has modified .bashrc to log you out when you log in with SSH.

step3:- ssh bandit18@bandit.labs.overwire.org -p 2200 cat readme 


problem i faced:- genuinely there was no problem in this level 

Level 19-20

task:-To gain access to the next level, you should use the setuid binary in the homedirectory. Execute it without arguments to find out how to use it. The password for this level can be found in the usual place (/etc/bandit_pass), after you have used the setuid binary

step3 - ls -la
step4 - ./badit20-do
step5 - ./bandit20-do cat /etc/bandit_pass

problem i faced :- i thought the i have to use setuid command but it only wanted me execute and learn the how to set uo binary account  


Level 20-21

task:- There is a setuid binary in the homedirectory that does the following: it makes a connection to localhost on the port you specify as a commandline argument. It then reads a line of text from the connection and compares it to the password in the previous level (bandit20). If the password is correct, it will transmit the password for the next level (bandit21).

step3 - ls -la
step4 - ./suconnect
step5 - nc -lvp 12345 [it was already in use any number above 1024 usually work you can use any number like 44444]
step6 - nc -lvp 64325 [if it wants this level password give it and it will give you level21 password]
[now on different terminal login bandit 20 and write this]
step 7:- ./suconnect 64325


problem i faced :- i only knew nc -p -l version -v version which means verbose which basically means be more talkative after manual checking the nc i did eventually figure it out 

Level 21-22

task:- A program is running automatically at regular intervals from cron, the time-based job scheduler. Look in /etc/cron.d/ for the configuration and see what command is being executed.

step3 - ls -la
step4 - ls /etc/cron.d
step5 - cat /etc/cron.d/cronjob_bandit22 [always check bin mostly that will be found in the bin]
step6 - cat /usr/bin/cronjob_bandit22.sh
step7 - cat /tmp/filename

problem i faced :- nothing just did not what cron was but still this level didn't use any fancy commands just basic ones

Level 22-23

task:- A program is running automatically at regular intervals from cron, the time-based job scheduler. Look in /etc/cron.d/ for the configuration and see what command is being executed.

NOTE: Looking at shell scripts written by other people is a very useful skill. The script for this level is intentionally made easy to read. If you are having problems understanding what it does, try executing it to see the debug information it prints.

step3 - ls -la
step4 - ls /etc/cron.d/
step5 - ls /etc/cron.d/cronjob_bandit23
step6 - cat /etc/cron.d/cronjob_bandit23
step7 - cat /usr/bin/cronjob_bandit23.sh
step8 - cat /etc/bandit_pass/$myname [cat: /etc/bandit_pass/: Is a directory]
step9 - echo I am user bandit23 | md5sum | cut -d ' ' -f 1 [8ca319486bfbbc3663ea0fbe81326349]
step 10 -  cat /tmp/8ca319486bfbbc3663ea0fbe81326349


problem i faced :- it is that i totally use ai for this methd after step 8 cause i cant figure it out at that time so i used ai it did tell em how did it work and how it is used 


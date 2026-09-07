Level 13-14

task:- The password for the next level is stored in /etc/bandit_pass/bandit14 and can only be read by user bandit14. For this level, you don’t get the next password, but you get a private SSH key that can be used to log into the next level. Look at the commands that logged you into previous bandit levels, and find out how to use the key for this level.
If you need help with this level: a hint file can be found in the home directory.
Make sure to read the error messages as they are informative.

step3 - ls -la 
step4 - cat sshkey.private
step5 - pwd 
step6 - exit 
step7 - scp -p 2200 bandit13@bandit.labs.overwire.org /home/bandit13/sshkey.private .
step8 - paste the password of 13 
step9 - chmod 600 sshkey.private
step10 - ssh -i sshkey.private bandit14@bandit.labs.overwire.org -p 2200
step11 - cat /etc/bandit_pass/bandit14

problem i faced:- the scp was new to me so i panicked quite a bit i will explain what and whata re use of step7 [scp] command [-p 2200] port [bandit13@bandit.labs.overwire.org]user name [/home/bandit13] directory name and address [/sshkey.private]file or key name [chmod 600]means change the file permission to read and write only b owner which is me [-ssh -i] the i is for for identify it is specifically used for private key to login without password 

Level 14-15

task:- The password for the next level can be retrieved by submitting the password of the current level to port 30000 on localhost.

step3 - ls -la
step4 - nc localhost 30000 [paste the current password]

problem i faced:- first i learn about  The  nc  (or  netcat) utility is used for just about anything under the sun involving TCP, UDP
it scans the ports 

Level 15-16
 
task:- The password for the next level can be retrieved by submitting the password of the current level to port 30001 on localhost using SSL/TLS encryption.

step3 :- ls -la
step4:- openssl s_client -connect localhost:30001 [paste the previous password]

problem i faced:- i am fairly new to Linux i dont know most commands but i am learning them bit by bit so after researching about openssl i knew what to do in this i will explain what happened in step4 first [openssl] it is a command [s_client]that means to treat it as a client [-connect localhost:30001]it means to connect to localhost of port30001 after that paste the password let just say it  took few tries for me to get it right 

Level 16-17

task:- The credentials for the next level can be retrieved by submitting the password of the current level to a port on localhost in the range 31000 to 32000. First find out which of these ports have a server listening on them. Then find out which of those speak SSL/TLS and which don’t. There is only 1 server that will give the next credentials, the others will simply send back to you whatever you send to it.

Helpful note: Getting “DONE”, “RENEGOTIATING” or “KEYUPDATE”? Read the “CONNECTED COMMANDS” section in the manpage.

step3 - ls -la
step4 - nmap -p31000-3200 localhost
step5 - nc local <port> [many of them just echo back whatever you send ones that don't will be your port]
step6 - openssl s_client -connect localhost:<port>
step7 - cat /etc/bandit_pass/bandit16 | openssl s_client -connect localhost:<port> -quiet[this will give you an sshkey.private]
step8 - exit
step9:- [there are two ways to do it with scp or copy paste  will use copy paste cuz its easy copy the sshkey.private to your private file ]
step10 - touch sshkey,private
step11 - nano sshkey,private [ctrls=save ctrlx=exit][note:- i use ubuntu in wsl so your could be different]
step12:- chmod 600 sshkey.private
step13:- ssh -i sshkey.private bandit17@bandit.labs.overwire.org -p 2200

problem i faced :- is with ssh key some online blogs says you can login from inside bandit16 to bandit 17 that was false for my case but could be true for your case for my case specially i have to copy the ssh key my device to use chmod cause whatever i did bandit did not let me use chmod cause of permission issue i took me 20 min to figure it out so yeah i faced quite trouble on this level 


level 17-18 

task:- There are 2 files in the homedirectory: passwords.old and passwords.new. The password for the next level is in passwords.new and is the only line that has been changed between passwords.old and passwords.new

NOTE: if you have solved this level and see ‘Byebye!’ when trying to log into bandit18, this is related to the next level, bandit19

step3 - ls-la
step4 - cat passwords.new 
step5 - diff passwords.old password.new

problem i faced :- frankly i did face any issue just learn diff command 

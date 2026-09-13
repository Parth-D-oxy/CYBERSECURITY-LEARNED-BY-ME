Level 25 -26

task:- Logging in to bandit26 from bandit25 should be fairly easy… The shell for user bandit26 is not /bin/bash, but something else. Find out what it is, how it works and how to break out of i

step3 - ls -la
step4 - cat /etc/passwd | grep bandit26
step5 - cat /usr/bin/showtext
step6 - stty rows 5
step7 - ssh -i bandit26.sshkey -p 2220 bandit26@bandit.labs.overthewire.org
step8 - --More-- press v to open vim
step8 - press esc
step9 - :set shell=/bin/bash
step10 - :shell
step11 - cat /etc/bandit_pass/bandit26


problem i faced:- i did not know anything about stty rows 5 it makes the terminal shirt and interactive to use to let us see more option
frankly it was one of the most difficult for me becuz of wsl i needed to use ai for this


Level 26-27 

task:- Good job getting a shell! Now hurry and grab the password for bandit27!

step3 - ssh -i bandit26.sshkey -p 2220 bandit26@bandit.labs.overthewire.org
step4 - --More-- press v to open vim
step5 - press esc
step6 - :set shell=/bin/bash
step7 - :shell
step8 - ./bandit27-do cat /etc/bandit_pass/bandit27

problem i faced:- mainly nothing just a tad bit of prblm cuz of my wsl i recommend to try wsl before shifiting to  full Linux 

Level 27-28

task:- There is a git repository at ssh://bandit27-git@bandit.labs.overthewire.org/home/bandit27-git/repo via the port 2220. The password for the user bandit27-git is the same as for the user bandit27.

From your local machine (not the OverTheWire machine!), clone the repository and find the password for the next level. This needs git installed locally on your machine.

step1-mkdir /tmp/parth27
step2 - cd /tmp/parth27
step3 - ssh://bandit27-git@bandit.labs.overthewire.org/home/bandit27-git/repo[give level 27 password]
step4- cd repo
step5 - ls -la
step6- cat README

problem i faced :- nothing of sort this was fairly easy everything was given  

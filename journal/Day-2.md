Level 5-6

task:-The password for the next level is stored in a file somewhere under the inhere directory and has all of the following properties:
human-readable,1033 bytes in size ,not executable
  
step3 - ls 
step4 - cd inhere
step5 - find . -type f -size 1033c ! -executable
step6 - file filename
step7 - cat filename

problem i faced :- The find command gave me somewhat problem bcuz of its somewhat wide variety of use after figuring it out for reference i tried grep first bt it gave me bunch of file that have same value so than i used [find] command [.] means  current directory [- type f]
is used to only specifically choose files [-size 1033c] it used to find a size of file c=bytes and [! -executable] (!)means not and all of it together means not executable


Level 6-7

task:- The password for the next level is stored somewhere on the server and has all of the following properties: owned by user bandit7
owned by group bandit6 ,33 bytes in size

step3 - ls -la
step4 - find . -user bandit7 -group bandit6  -size 33c 
step5 - find . -user bandit7 -group bandit6 -size 33c 2</dev/null
step6 - cat filename 

problem i faced :- the first find that i gave had many permission denied but it had the answer that just took some time to find so i researched about how it doesn't show things that didn't show result more like a filter so [2</dev/null] that hides permission errors

Level 7-8 

task:- he password for the next level is stored in the file data.txt next to the word millionth

step3 - ls -la
step4 - grep millionth data.txt


problem i faced:- like a beginner i cat the whole file it dumped the whole file in my terminal so i had to reset my terminal and it was a mistake after that i used grep command 

Level 8-9

task:- The password for the next level is stored in the file data.txt and is the only line of text that occurs only once

step3 - ls -la 
step4 - sort data.txt | uniq -u

problem i faced :- at first i used uniq -u data.txt but it dumped the whole file again because it only adjacent duplicates after that i used [sort] to sort out the file [|] means pipeline and [-u] is used for line that appear only once

Level 9-10

task:- The password for the next level is stored in the file data.txt in one of the few human-readable strings, preceded by several ‘=’ characters.

step3 - ls -la
step4 - strings data.txt
step4 - strings data.txt | grep '='

problem i faced :- the first string i used did printed everything and i can stil did found my password in that but than i used grep to make it better 

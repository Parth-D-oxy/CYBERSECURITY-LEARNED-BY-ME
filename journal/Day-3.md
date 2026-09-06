Level 10-11

task:- The password for the next level is stored in the file data.txt, which contains base64 encoded data

step3 - ls -la
step4 - base64 -d data.txt

problem i faced:- i didn't know about base64 which is binary-to-text-encoding that uses 64 printable character so after i man base64 i read and went forward with this command 

Level 11-12

task:- The password for the next level is stored in the file data.txt, where all lowercase (a-z) and uppercase (A-Z) letters have been rotated by 13 positions

step3 - ls -la
step4 - cat data.txt
step5 - cat data.txt | tr 'A-Za-z' 'N-ZA-Mn-za-m'

problem i faced :- i didn't know how rot 13 would work after a through reading i knew for security purpose every letter is switched at 13 place in alphanumeric order and the [tr] is used for translating or delete characters ['A-Za-z'] this means capital A to small letter matches and ['N-ZA-Mn-Za-m'] this means it maps each letter 13 characters away

Level 12-13

task:- The password for the next level is stored in the file data.txt, which is a hexdump of a file that has been repeatedly compressed. For this level it may be useful to create a directory under /tmp in which you can work. Use mkdir with a hard to guess directory name. Or better, use the command “mktemp -d”. Then copy the datafile using cp, and rename it using mv (read the manpages!)

step3 - ls -la
step4 - mtemp -d 
step5 - cd temp/filelocation
step6 - cp ~/data.txt .
step7 - ls -la 
step8 - man xxd 
step9 - xxd -r data.txt data.bin 
step10 - file data.bin [if its is gzip use step11(1) to step12(1)]
step11(1) - mv data.bin data.gz
step12(1) - gunzip data.gz
step11(2) - mv data.bin data.bz2 
step12(2) - bunzip2 data.bz2
step11(3) - mv data.bin data.tar
step12(3) - tar-xf data.tar 
step13 - cat final-file

[decompress the file until it says ASCII in its file command always make sur with ls that file exist and file to know how to decompress the file ]

problem i faced :- i researched about tar bz2 and gz and hexdump file and how to decompress it and the main problem i faced after decompressing with tar it gives us file name like data5.bin i didn't knew what to do so i searched it 

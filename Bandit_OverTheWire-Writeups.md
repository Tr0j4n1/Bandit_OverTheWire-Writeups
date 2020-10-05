# Bandit_OverTheWire-WriteUps

These are the write-ups for the levels 1-15 of OverTheWire-Bandit


#### Bandit: Level 0->1

- Type command `ssh bandit0@bandit.labs.overthewire.org -p 2220`
- Type the password : `bandit0`
- See the files in the server by command `ls`
- Open the readme using command `cat readme`
- Copy the password `boJ9jbbUNNfktd78OOpsqOltutMc3MY1`
- Type `exit` to return to your local server

#### Bandit: Level 1->2
- Type command ssh bandit1@bandit.labs.overthewire.org -p 2220
- Type the password obtained from previous challenge : boJ9jbbUNNfktd78OOpsqOltutMc3MY1
- Type cat ./- or cat <- to read the dashed file
- Copy the password CV1DtqXWVFXTvM2F0k09SHz0YwRINYA9
- Type `exit'

#### Bandit: Level 2->3
- Type command ssh bandit2@bandit.labs.overthewire.org -p 2220
- Type the password CV1DtqXWVFXTvM2F0k09SHz0YwRINYA9
- Type cat 'spaces in this filename' or cat spaces\in\this\filename
- Copy the password UmHadQclWmgdLOKQ3YNgjWxGoRMb5luK
- Type exit

#### Bandit: Level 3->4
- Type command ssh bandit3@bandit.labs.overthewire.org -p 2220
- Type the password UmHadQclWmgdLOKQ3YNgjWxGoRMb5luK
- Type cd inhere`to get into the directory `inhere
- Type ls -a to see including hidden files
- To read the file type cat ./.hidden
- Copy the password pIwrPrtPN36QITSp3EQaw936yaFoFgAB
- Type exit

#### Bandit: Level 4->5
- Type command ssh bandit4@bandit.labs.overthewire.org -p 2220
- Type the password pIwrPrtPN36QITSp3EQaw936yaFoFgAB
- Type cd inhere`to get into the directory `inhere
- To read contents of all the files type cat ./*
- Copy the password koReBOKuIDDepwhWk7jZC0RTdopnAYKh
- Type exit

#### Bandit: Level 5->6
- Type command ssh bandit5@bandit.labs.overthewire.org -p 2220
- Type the password koReBOKuIDDepwhWk7jZC0RTdopnAYKh
- Type cd inhere`to get into the directory `inhere
- To find the files satisfing the given conditions type find -size 1033c ! -executable
- Open the file using command cat ./.file2
- Copy the password DXjZPULLxYr17uwoI01bNLQbtFemEgo7
- Type exit

#### Bandit: Level 6->7
- Type command ssh bandit6@bandit.labs.overthewire.org -p 2220
- Type the password DXjZPULLxYr17uwoI01bNLQbtFemEgo7
- Find the file satisfying given conditions typing find / -user bandit7 -group bandit6 -size 33c
- Read the password file by typing cat /var/lib/dpkg/info/bandit7.password
- Copy the password HKBPTKQnIay4Fw76bEy8PVxKEDQRKTzs
- Type exit

#### Bandit: Level 7->8
- Type command ssh bandit7@bandit.labs.overthewire.org -p 2220
- Type the password HKBPTKQnIay4Fw76bEy8PVxKEDQRKTzs
- Type cat data.txt | grep "millionth" for getting the password
- Copy the password cvX2JJa4CFALtqS87jk27qwqGhBM9plV
- Type exit

#### Bandit: Level 8->9
- Type command ssh bandit8@bandit.labs.overthewire.org -p 2220
- Type the password cvX2JJa4CFALtqS87jk27qwqGhBM9plV
- Type cat data.txt | sort | uniq -c to find the lines that are unique
- Copy the lines of which the count is 1 i.e, UsvVyFSfZZWbi6wgC7dAFyFuR6jQQUhR
- Type exit

#### Bandit: Level 9->10
- Type command ssh bandit9@bandit.labs.overthewire.org -p 2220
- Type the password UsvVyFSfZZWbi6wgC7dAFyFuR6jQQUhR
- Type `strings data.txt`for getting the readable lines from the file
- Copy the password truKLdjsbJ5g7yyJ2X2R0o3a5HQJFuLk
- Type exit

#### Bandit: Level 10->11
- Type command ssh bandit10bandit.labs.overthewire.org -p 2220
- Type the password truKLdjsbJ5g7yyJ2X2R0o3a5HQJFuLk
- Type cat.txt to read the contents of the file
- Copy the base64 encoded string from the output
- Decode the string using the command echo 'VGhlIHBhc3N3b3JkIGlzIElGdWt3S0dzRlc4TU9xM0lSRnFyeEUxaHhUTkViVVBSCg==' | base64 -d
- Copy the decoded output which is the password IFukwKGsFW8MOq3IRFqrxE1hxTNEbUPR
- Type exit

#### Bandit: Level 11->12
- Type command ssh bandit11@bandit.labs.overthewire.org -p 2220
- Type the password IFukwKGsFW8MOq3IRFqrxE1hxTNEbUPR
- Type cat data.txt to read the contents of the file. Copy the output
- Use the command echo 'Gur cnffjbeq vf 5Gr8L4qetPEsPk8htqjhRK8XSP6x2RHh' | tr [N-ZA-Mn-za-m] [A-Za-z] to decode the rot13 encoded string
- Copy the decoded output that has the password 5Te8Y4drgCRfCx8ugdwuEX8KFC6k2EUu
Type exit

#### Bandit: Level 12->13
- Type command ssh bandit12@bandit.labs.overthewire.org -p 2220
- Type the password 5Te8Y4drgCRfCx8ugdwuEX8KFC6k2EUu
- Type cat data.txt to read the contents of the file
- The provided data.txt file is a hex dump, so convert it back to it original binary form by xxd -r data.txt
- A highly compressed file called data will be obtained
- We cannot decompress the file from the root directory, so we copy the file to another by mkdir /tmp/myname123  and cp data.txt /tmp/myname123
- Change the directory to the newly created directory by cd /tmp/myname123
- Check the file type of the file file <filename>
- Rename the file to the default extension by mv <filename> <filename.fileformat>
To decompress :
- For tar compressed tar xvf <filename.tar>
- For gz compressed gzip <filename.gz>
- for bz2 compressed bzip2 <filename.bz2>

- Continue the steps again and again till you get a file named 'data8'
- Copy the password `8ZjyCRiBWFYkneahHwxCv3wb2a1ORpYL`from the file
- Type exit

#### Bandit: Level 13->14
- Type command ssh bandit13@bandit.labs.overthewire.org -p 2220
- Type the password 8ZjyCRiBWFYkneahHwxCv3wb2a1ORpYL
- You will be provided an ssh privatekey
- Log into localhost with username bandit14 by command ssh bandit14@localhost -i sshkey.private
- Copy the password 4wcYUJFw0k0XLShlDzztnTBHiqxU3b3e from the address given in the description ofn= the challenge
- Type exit

#### Bandit: Level 14->15
- Type command ssh bandit14@bandit.labs.overthewire.org -p 2220
- Type the password 4wcYUJFw0k0XLShlDzztnTBHiqxU3b3e
- Submit the password to the localhost using command echo '4wcYUJFw0k0XLShlDzztnTBHiqxU3b3e' | nc localhost 30000
- Type exit


And You've cracked it all ! Thanks for checking out ;)

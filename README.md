# OS-Linux-commands-Shell-scripting
Operating systems Lab exercise
# Linux commands-Shell scripting
Linux commands-Shell scripting

# AIM:
To practice Linux Commands and Shell Scripting

# DESIGN STEPS:

### Step 1:

Navigate to any Linux environment installed on the system or installed inside a virtual environment like virtual box/vmware or online linux JSLinux (https://bellard.org/jslinux/vm.html?url=alpine-x86.cfg&mem=192) or docker.

### Step 2:

Execute the following commands

### Step 3:

Testing the commands for the desired output. 

# COMMANDS:
### Create the following files file1, file2 as follows:
cat > file1
```
chanchal singhvi
c.k. shukla
s.n. dasgupta
sumit chakrobarty
^d
```
cat > file2
```
anil aggarwal
barun sengupta
c.k. shukla
lalit chowdury
s.n. dasgupta
^d
```
### Display the content of the files
cat < file1
## OUTPUT
![image](https://github.com/NAVEEN23013059/OS-Linux-commands-Shell-script/assets/150319555/6096471f-19a3-435d-866d-52e3da6d4af9)




cat < file2
## OUTPUT
![image](https://github.com/NAVEEN23013059/OS-Linux-commands-Shell-script/assets/150319555/0a5d47fa-5c5c-4967-9212-706ec8576813)



# Comparing Files
cmp file1 file2
## OUTPUT
![image](https://github.com/NAVEEN23013059/OS-Linux-commands-Shell-script/assets/150319555/a7e18904-b0d0-413c-9653-66b917936487)

 
comm file1 file2
 ## OUTPUT
 ![image](https://github.com/NAVEEN23013059/OS-Linux-commands-Shell-script/assets/150319555/54dcd23c-e358-43d5-a073-f1e929994649)


 
diff file1 file2
## OUTPUT
![image](https://github.com/NAVEEN23013059/OS-Linux-commands-Shell-script/assets/150319555/79bc344e-37c5-4aa1-b73c-42198fa2e2ff)



#Filters

### Create the following files file11, file22 as follows:

cat > file11
```
Hello world
This is my world
^d
```
cat > file22
```
1001 | Ram | 10000 | HR
1002 | tom |  5000 | Admin
1003 | Joe |  7000 | Developer
^d
```


cut -c1-3 file11
## OUTPUT
![image](https://github.com/NAVEEN23013059/OS-Linux-commands-Shell-script/assets/150319555/c2afa04e-cf40-46bb-8c7a-41d6aeed8778)





cut -d "|" -f 1 file22
## OUTPUT
![image](https://github.com/NAVEEN23013059/OS-Linux-commands-Shell-script/assets/150319555/e4b3a26c-783f-4348-87f6-49aa450bd047)



cut -d "|" -f 2 file22
## OUTPUT
![image](https://github.com/NAVEEN23013059/OS-Linux-commands-Shell-script/assets/150319555/0e88113a-e4b3-47a0-a75e-1f2f95010df9)


cat < newfile 
```
Hello world
hello world
^d
````
cat > newfile 
Hello world
hello world
 
grep Hello newfile 
## OUTPUT



grep hello newfile 
## OUTPUT

![image](https://github.com/NAVEEN23013059/OS-Linux-commands-Shell-script/assets/150319555/eb86274e-366f-43fd-af6f-7e257da792bc)



grep -v hello newfile 
## OUTPUT

![image](https://github.com/NAVEEN23013059/OS-Linux-commands-Shell-script/assets/150319555/7ca9140a-b703-4490-b150-e8ef10d60910)


cat newfile | grep -i "hello"
## OUTPUT

![image](https://github.com/NAVEEN23013059/OS-Linux-commands-Shell-script/assets/150319555/6df303d7-39d9-47d1-9f45-2ba471bd1f6d)


grep -R ubuntu /etc
## OUTPUT
![image](https://github.com/NAVEEN23013059/OS-Linux-commands-Shell-script/assets/150319555/c47bdcd0-d183-4109-afa5-7c215099fae7)



grep -w -n world newfile   
## OUTPUT

![image](https://github.com/NAVEEN23013059/OS-Linux-commands-Shell-script/assets/150319555/1332313e-80b2-4acd-b49a-168ff11a488a)

cat < newfile 
```
Hello world
hello world
Linux is world number 1
Unix is predecessor
Linux is best in this World
^d
```

cat > newfile
```
Hello world
hello world
Linux is world number 1
Unix is predecessor
Linux is best in this World
^d
 ```
egrep -w 'Hello|hello' newfile 
## OUTPUT

![image](https://github.com/NAVEEN23013059/OS-Linux-commands-Shell-script/assets/150319555/f3aec520-09e2-45a0-b049-ddb68ac7458e)



egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT


![image](https://github.com/NAVEEN23013059/OS-Linux-commands-Shell-script/assets/150319555/b341227c-91b3-4ad9-9807-08b80aa2f9ba)


egrep '(^hello)' newfile 
## OUTPUT
![image](https://github.com/NAVEEN23013059/OS-Linux-commands-Shell-script/assets/150319555/8c63549c-d7be-4741-9878-85dc4f75e5f5)



egrep '(world$)' newfile 
## OUTPUT
![image](https://github.com/NAVEEN23013059/OS-Linux-commands-Shell-script/assets/150319555/7a28cc50-eb38-4a82-a14f-037e74546a16)



egrep '(World$)' newfile 
## OUTPUT
![image](https://github.com/NAVEEN23013059/OS-Linux-commands-Shell-script/assets/150319555/942500aa-fc3e-48d6-88bc-a377ef4e6cfe)


egrep '((W|w)orld$)' newfile 
## OUTPUT

![image](https://github.com/NAVEEN23013059/OS-Linux-commands-Shell-script/assets/150319555/4fa22089-822d-4e70-a684-facb7980cb35)


egrep '[1-9]' newfile 
## OUTPUT


![image](https://github.com/NAVEEN23013059/OS-Linux-commands-Shell-script/assets/150319555/a4b4762f-9f6f-4bb5-a8b5-8fc230b0368d)

egrep 'Linux.*world' newfile 
## OUTPUT

![image](https://github.com/NAVEEN23013059/OS-Linux-commands-Shell-script/assets/150319555/0f8cc3e5-f598-43b4-a8fc-4a44b9c80752)

egrep 'Linux.*World' newfile 
## OUTPUT
![image](https://github.com/NAVEEN23013059/OS-Linux-commands-Shell-script/assets/150319555/838b24a4-6f88-4776-a750-c816c9d7e327)


egrep l{2} newfile
## OUTPUT

![image](https://github.com/NAVEEN23013059/OS-Linux-commands-Shell-script/assets/150319555/e5a37f2c-ebb8-4ed6-a57d-8bb06433ddf6)


cat > file23
```
1001 | Ram | 10000 | HR
1001 | Ram | 10000 | HR
1002 | tom |  5000 | Admin
1003 | Joe |  7000 | Developer
1005 | Sam |  5000 | HR
1004 | Sit |  7000 | Dev
1003 | Joe |  7000 | Developer
1001 | Ram | 10000 | HR
^d
```


sed -n -e '3p' file23
## OUTPUT

![image](https://github.com/NAVEEN23013059/OS-Linux-commands-Shell-script/assets/150319555/2b199aa1-7bbd-4b01-ae4e-9bdd6cdf9c9e)


sed -n -e '$p' file23
## OUTPUT

![image](https://github.com/NAVEEN23013059/OS-Linux-commands-Shell-script/assets/150319555/8257cc8d-4bb9-4ee9-b662-6dc5b81644fd)


sed  -e 's/Ram/Sita/' file23
## OUTPUT

![image](https://github.com/NAVEEN23013059/OS-Linux-commands-Shell-script/assets/150319555/1a23e554-a239-438f-aae4-ceb8ec54a79b)


sed  -e '2s/Ram/Sita/' file23
## OUTPUT

![image](https://github.com/NAVEEN23013059/OS-Linux-commands-Shell-script/assets/150319555/4e570829-0cdf-4166-97df-7f8f81ea5f98)


sed  '/tom/s/5000/6000/' file23
## OUTPUT

![image](https://github.com/NAVEEN23013059/OS-Linux-commands-Shell-script/assets/150319555/128e64e6-a82f-4734-ab82-976057dffb63)


sed -n -e '1,5p' file23
## OUTPUT

![image](https://github.com/NAVEEN23013059/OS-Linux-commands-Shell-script/assets/150319555/bfef0a33-a602-4b8c-8063-73ed44d00c0b)


sed -n -e '2,/Joe/p' file23
## OUTPUT


![image](https://github.com/NAVEEN23013059/OS-Linux-commands-Shell-script/assets/150319555/e7dabfa4-d493-4b80-852f-a20972d0329a)


sed -n -e '/tom/,/Joe/p' file23
## OUTPUT

![image](https://github.com/NAVEEN23013059/OS-Linux-commands-Shell-script/assets/150319555/0448f417-1aa2-469b-8568-06445f93be7d)


seq 10 
## OUTPUT
![316713574-54f8d127-13a8-4be8-b927-350f520a22d1](https://github.com/NAVEEN23013059/OS-Linux-commands-Shell-script/assets/150319555/d648e371-d3cc-45ca-af8b-b5b5f51f17b5)



seq 10 | sed -n '4,6p'
## OUTPUT

![316713537-22cad363-02c5-4af1-9a77-b2a7bb7e6334](https://github.com/NAVEEN23013059/OS-Linux-commands-Shell-script/assets/150319555/a41bdfec-c0fe-4c13-ab5e-6504e31dde08)


seq 10 | sed -n '2,~4p'
## OUTPUT

![316713506-73b9508a-edd9-4bc2-bc69-c81ebabce313](https://github.com/NAVEEN23013059/OS-Linux-commands-Shell-script/assets/150319555/a860c6fe-6274-4642-a549-a0a1bd3876d6)


seq 3 | sed '2a hello'
## OUTPUT

![316713455-a049eaf8-3be2-4178-9aba-bb43fc297bd3](https://github.com/NAVEEN23013059/OS-Linux-commands-Shell-script/assets/150319555/3b38cc50-3788-4cfc-9e24-987a052f289d)


seq 2 | sed '2i hello'
## OUTPUT
![316713441-2172476a-9496-4731-8a00-4aa66e508025](https://github.com/NAVEEN23013059/OS-Linux-commands-Shell-script/assets/150319555/d57e450c-e56b-431e-92ca-e10a5bd03874)


seq 10 | sed '2,9c hello'
## OUTPUT
![316713441-2172476a-9496-4731-8a00-4aa66e508025](https://github.com/NAVEEN23013059/OS-Linux-commands-Shell-script/assets/150319555/2da6790f-e826-4fd7-84bc-f527a05b249e)


sed -n '2,4{s/^/$/;p}' file23
## OUTPUT
![316713416-ffbab54b-04a3-46cf-a14d-6e660027986c](https://github.com/NAVEEN23013059/OS-Linux-commands-Shell-script/assets/150319555/891fe098-a5d5-4d02-9238-36cff6ed8d31)



sed -n '2,4{s/$/*/;p}' file23


#Sorting File content
cat > file21
```
1001 | Ram | 10000 | HR
1002 | tom |  5000 | Admin
1003 | Joe |  7000 | Developer
1005 | Sam |  5000 | HR
1004 | Sit |  7000 | Dev
``` 
sort file21
## OUTPUT
![316713307-645048fc-c5a0-40e6-9c36-f8515f3deae8](https://github.com/NAVEEN23013059/OS-Linux-commands-Shell-script/assets/150319555/cdebcc36-f662-4e55-bc82-a84055e6abeb)


cat > file22
```
1001 | Ram | 10000 | HR
1001 | Ram | 10000 | HR
1002 | tom |  5000 | Admin
1003 | Joe |  7000 | Developer
1005 | Sam |  5000 | HR
1004 | Sit |  7000 | Dev
``` 
uniq file22
## OUTPUT

![316713349-45ffde7f-6740-4d97-88ea-b2e83e08e8b5](https://github.com/NAVEEN23013059/OS-Linux-commands-Shell-script/assets/150319555/61e7bab6-31c8-442c-9f8e-fde64a8f8ce8)


#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT
![316714355-19427389-b301-4520-8239-c0efeb8796bb](https://github.com/NAVEEN23013059/OS-Linux-commands-Shell-script/assets/150319555/ad7290a5-b7ba-4c17-b2d0-0f5f8ac01c93)

cat < urllist.txt
```
www. yahoo. com
www. google. com
www. mrcet.... com
^d
 ```
cat > urllist.txt
```
www. yahoo. com
www. google. com
www. mrcet.... com
 ```
cat urllist.txt | tr -d ' '
 ## OUTPUT


 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT


![316714423-caf922b2-acc6-4bb8-ab40-b1cc091bd36c](https://github.com/NAVEEN23013059/OS-Linux-commands-Shell-script/assets/150319555/c9b4566e-9594-4c25-b1b4-c87095cdd9f4)

#Backup commands
tar -cvf backup.tar *
## OUTPUT
![316714442-de9360d7-95a0-4c23-8cf6-020aaf6880c9](https://github.com/NAVEEN23013059/OS-Linux-commands-Shell-script/assets/150319555/a037be68-3d7f-42ef-a976-c43f7a189a1b)


mkdir backupdir
 
mv backup.tar backupdir
 
tar -tvf backup.tar
## OUTPUT

![316714479-4e0dfc45-bf13-459d-a185-06a5b7a0da98](https://github.com/NAVEEN23013059/OS-Linux-commands-Shell-script/assets/150319555/7d8a73c5-125f-4656-b118-02f538e681d1)

tar -xvf backup.tar
## OUTPUT
![316714512-1dffd79f-9c88-4f95-a9e3-b57fa18cb586](https://github.com/NAVEEN23013059/OS-Linux-commands-Shell-script/assets/150319555/5127fe73-3dd1-44b1-9f68-8b5c12fbe513)

gzip backup.tar

ls .gz
## OUTPUT
 ![316717934-96813167-e0d6-46b2-90db-29f21b5a176a](https://github.com/NAVEEN23013059/OS-Linux-commands-Shell-script/assets/150319555/dbe5aecb-1d20-4d59-ae6a-0cf164652a49)

gunzip backup.tar.gz
## OUTPUT

 ![316717812-99679687-a045-4561-b634-362f69a5dc94](https://github.com/NAVEEN23013059/OS-Linux-commands-Shell-script/assets/150319555/75f6f8bc-009b-4d06-b69a-2e3c1c02a45d)

# Shell Script
```
echo '#!/bin/sh' > my-script.sh
echo 'echo Hello World‘; exit 0 >> my-script.sh
```
chmod 755 my-script.sh
./my-script.sh
## OUTPUT
![316718085-b46aa069-3262-43d7-bd01-651d123778c9](https://github.com/NAVEEN23013059/OS-Linux-commands-Shell-script/assets/150319555/d223fc8c-cda6-4c8b-a1ca-634a9a5158eb)

 
cat << stop > herecheck.txt
```
hello in this world
i cant stop
for this non stop movement
stop
```

cat herecheck.txt
## OUTPUT

![316718208-cab070f9-34aa-43c1-a38b-f5f9ee3abdf3](https://github.com/NAVEEN23013059/OS-Linux-commands-Shell-script/assets/150319555/ac977470-a226-48a7-86c0-1e8a40ce90c6)

cat < scriptest.sh 
```bash
\#!/bin/sh
echo “File name is $0 ”
echo "File name is " `basename $0`
echo “First arg. is ” $1
echo “Second arg. is ” $2
echo “Third arg. is ” $3
echo “Fourth arg. is ” $4
echo 'The $@ is ' $@
echo 'The $\# is ' $1#
echo 'The $$ is ' $$
ps
^d
 ```

cat scriptest.sh 
```bash
\#!/bin/sh
echo “File name is $0 ”
echo "File name is " `basename $0`
echo “First arg. is ” $1
echo “Second arg. is ” $2
echo “Third arg. is ” $3
echo “Fourth arg. is ” $4
echo 'The $@ is ' $@
echo 'The $\# is ' $\#
echo 'The $$ is ' $$
ps
```
 
chmod 777 scriptest.sh
 
./scriptest.sh 1 2 3

## OUTPUT

 
ls file1![316718328-65ae614d-035b-4c79-a761-b99c26c90c6c](https://github.com/NAVEEN23013059/OS-Linux-commands-Shell-script/assets/150319555/baee8084-29a6-484d-90c1-2f90b2e021f2)

## OUTPUT
![316718654-1f5e2aa4-0f43-44b7-a109-cfc900fb0846](https://github.com/NAVEEN23013059/OS-Linux-commands-Shell-script/assets/150319555/a17f8330-9733-4693-a4b5-245118e2f8b5)

echo $?
## OUTPUT 
./one
bash: ./one: Permission denied
 
echo $?
## OUTPUT 
 
abcd
 
echo $?
 ## OUTPUT


 
# mis-using string comparisons

cat < strcomp.sh 
```bash
\#!/bin/bash
val1=baseball
val2=hockey
if [ $val1 \> $val2 ]
then
echo "$val1 is greater than $val2"
else
echo "$val1 is less than $val2"
fi
^d
```

cat strcomp.sh 
```bash
\#!/bin/bash
val1=baseball
val2=hockey
if [ $val1 \> $val2 ]
then
echo "$val1 is greater than $val2"
else
echo "$val1 is less than $val2"
fi
```
##OUTPUT



chmod 755 strcomp.sh
 
./strcomp.sh 
## OUTPUT

![316718736-ff2cbc1f-6ee5-4f32-aee8-0e2de3dbfd00](https://github.com/NAVEEN23013059/OS-Linux-commands-Shell-script/assets/150319555/b05513e1-4ecd-4a30-8dc0-0e3ea5c2a82f)

# check file ownership
cat < psswdperm.sh 
```bash
\#!/bin/bash
if [ -O /etc/passwd ]
then
echo “You are the owner of the /etc/passwd file”
else
echo “Sorry, you are not the owner of the /etc/passwd file”
fi
^d
```

cat psswdperm.sh 
```bash
/#!/bin/bash
if [ -O /etc/passwd ]
then
echo “You are the owner of the /etc/passwd file”
else
echo “Sorry, you are not the owner of the /etc/passwd file”
fi
 ```
./psswdperm.sh
## OUTPUT
![316718799-debdb3bb-8a1c-43fc-a31a-f2868563b850](https://github.com/NAVEEN23013059/OS-Linux-commands-Shell-script/assets/150319555/22045156-c01c-4d52-8ea1-954b0cd9afd2)

# check if with file location
cat>ifnested.sh 
```bash
\#!/bin/bash
if [ -e $HOME ]
then
echo “$HOME The object exists, is it a file?”
if [ -f $HOME ]
then
echo “Yes,$HOME it is a file!”
else
echo “No,$HOME it is not a file!”
if [ -f $HOME/.bash_history ]
then
echo “But $HOME/.bash_history is a file!”
fi
fi
else
echo “Sorry, the object does not exist”
fi
^d
```
cat ifnested.sh 
```
\#!/bin/bash
if [ -e $HOME ]
then
echo “$HOME The object exists, is it a file?”
if [ -f $HOME ]
then
echo “Yes,$HOME it is a file!”
else
echo “No,$HOME it is not a file!”
if [ -f $HOME/.bash_history ]
then
echo “But $HOME/.bash_history is a file!”
fi
fi
else
echo “Sorry, the object does not exist”
fi
```

./ifnested.sh 
## OUTPUT
![316718924-81168090-3d8c-491f-98de-fcbf0c1b453c](https://github.com/NAVEEN23013059/OS-Linux-commands-Shell-script/assets/150319555/eec4d445-337c-4937-bdf3-d44393c78d1b)



# using numeric test comparisons
cat > iftest.sh 
```bash
\#!/bin/bash
val1=10
val2=11
if [ $val1 -gt 5 ]
then
echo “The test value $val1 is greater than 5”
fi
if [ $val1 -eq $val2 ]
then
echo “The values are equal”
else
echo “The values are different”
fi
^d
```


cat iftest.sh 
```bash
\#!/bin/bash
val1=10
val2=11
if [ $val1 -gt 5 ]
then
echo “The test value $val1 is greater than 5”
fi
if [ $val1 -eq $val2 ]
then
echo “The values are equal”
else
echo “The values are different”
fi
```

$ chmod 755 iftest.sh
 
$ ./iftest.sh 
##OUTPUT

# check if a file
cat > ifnested.sh 
```bash
\#!/bin/bash
if [ -e $HOME ]
then
echo “$HOME The object exists, is it a file?”
if [ -f $HOME ]
then
echo “Yes,$HOME it is a file!”
else
echo “No,$HOME it is not a file!”
if [ -f $HOME/.bash_history ]
then
echo “But $HOME/.bash_history is a file!”
fi
fi
else
echo “Sorry, the object does not exist”
fi
^d
```

cat ifnested.sh 
```bash
\#!/bin/bash
if [ -e $HOME ]
then
echo “$HOME The object exists, is it a file?”
if [ -f $HOME ]
then
echo “Yes,$HOME it is a file!”
else
echo “No,$HOME it is not a file!”
if [ -f $HOME/.bash_history ]
then
echo “But $HOME/.bash_history is a file!”
fi
fi
else
echo “Sorry, the object does not exist”
fi
```

$ chmod 755 ifnested.sh
 
$ ./ifnested.sh 
##OUTPUT

# looking for a possible value using elif
cat elifcheck.sh 
```bash
\#!/bin/bash
if [ $USER = Ram ]
then
echo "Welcome $USER"
echo "Please enjoy your visit"
elif [ $USER = Rahim ]
then
echo "Welcome $USER"
echo "Please enjoy your visit"
elif [ $USER = Robert ]
then
echo "Special testing account"
elif [ $USER = gganesh ]
then
echo "$USER, Do not forget to logout when you're done"
else
echo "Sorry, you are not allowed here"
fi
```

$ chmod 755 elifcheck.sh
 
$ ./elifcheck.sh 
## OUTPUT
![316719082-80023581-a998-40c4-8f65-926441c27f41](https://github.com/NAVEEN23013059/OS-Linux-commands-Shell-script/assets/150319555/57f7aaaf-7dcf-4e81-8b01-ef7c8ed7a810)


# testing compound comparisons
cat> ifcompound.sh 
```bash
\#!/bin/bash
if [ -d $HOME ] && [ -w $HOME ]
then
echo "The file exists and you can write to it"
else
echo "I cannot write to the file"
fi
```
$ chmod 755 ifcompound.sh
$ ./ifcompound.sh 
## OUTPUT

![316717241-56693acd-71aa-4947-b4e3-bb584fa8f5d3](https://github.com/NAVEEN23013059/OS-Linux-commands-Shell-script/assets/150319555/c49960b9-87b2-49ac-aba5-b704cc1fab84)



# using the case command
cat >casecheck.sh 
```bash
case $USER in
Ram | Robert)
echo "Welcome, $USER"
echo "Please enjoy your visit";;
Rahim)
echo "Special testing account";;
gganesh)
echo "$USER, Do not forget to log off when you're done";;
*)
echo "Sorry, you are not allowed here";;
esac
```
$ chmod 755 casecheck.sh 
 
$ ./casecheck.sh 
 
cat > whiletest
```bash
#!/bin/bash
#while command test
var1=10
while [ $var1 -gt 0 ]
do
echo $var1
var1=$[ $var1 - 1 ]
done
```
$ chmod 755 whiletest.sh
 
$ ./whiletest.sh
 
 
cat untiltest.sh 
```bash
\#using the until command
var1=100
until [ $var1 -eq 0 ]
do
echo $var1
var1=$[ $var1 - 25 ]
done
``` 
$ chmod 755 untiltest.sh
 
 
 
cat forin1.sh 
```bash
\#!/bin/bash
\#basic for command
for test in Alabama Alaska Arizona Arkansas California Colorado
do
echo The next state is $test
done
 ```
 
$ chmod 755 forin1.sh
 
 
cat forin2.sh 
```bash
\#!/bin/bash
\# another example of how not to use the for command
for test in I don't know if this'll work
do
echo “word:$test”
done
 ```
 
$ chmod 755 forin2.sh
 
cat forin2.sh 
```bash
\#!/bin/bash
\# another example of how not to use the for command
for test in I don't know if this'll work
do
echo “word:$test”
done
```
$ chmod 755 forin2.sh
 
$ ./forin2.sh 
 
cat forin3.sh 
```bash
\#!/bin/bash
\# another example of how not to use the for command
for test in I don\'t know if "this'll" work
do
echo "word:$test"
done
```
$ ./forin3.sh 
 
cat forin1.sh 
```bash
#!/bin/bash
# basic for command
for test in Alabama Alaska Arizona Arkansas California Colorado
do
echo The next state is $test
done
```
$ chmod 755 forin1.sh

## OUTPUT

![316717079-8899c703-62dd-4c51-aa84-ea21297d24a1](https://github.com/NAVEEN23013059/OS-Linux-commands-Shell-script/assets/150319555/b1270270-2ae8-44fa-904c-4480b2f016b0)

cat forinfile.sh 
```bash
#!/bin/bash
# reading values from a file
file="cities"
for state in `cat $file`
do
echo "Visit beautiful $file“
done
```
$ chmod 777 forinfile.sh
$ cat cities
Hyderabad
Alampur
Basara
Warangal
Adilabad
Bhadrachalam
Khammam

## OUTPUT

![316716908-34d755eb-cd75-4ef2-8f7c-1cc2d6171e75](https://github.com/NAVEEN23013059/OS-Linux-commands-Shell-script/assets/150319555/16d2f00c-df1b-4160-9400-f77340597814)


cat forctype.sh 
```bash
#!/bin/bash
# testing the C-style for loop
for (( i=1; i <= 5; i++ ))
do
echo "The value of i is $i"
done
````
$ chmod 755 forctype.sh
$ ./forctype.sh 
## OUTPUT

![316716763-56576de7-bb31-482f-8367-6695f4492afd](https://github.com/NAVEEN23013059/OS-Linux-commands-Shell-script/assets/150319555/315323a6-4337-4865-8f60-e1b52258e6c9)


cat forctype1.sh 
```bash
#!/bin/bash
# multiple variables
for (( a=1, b=5; a <= 5; a++, b-- ))
do
echo "$a - $b"
done
```
$ chmod 755 forctype.sh
$ ./forctype1.sh 
## OUTPUT


cat fornested1.sh 
```bash
#!/bin/bash
# nesting for loops
for (( a = 1; a <= 3; a++ ))
do
echo "Starting loop $a:"
for (( b = 1; b <= 3; b++ ))
do
echo " Inside loop: $b"
done
done
```
$ chmod 755 fornested1.sh
 
$ ./fornested1.sh 
 ## OUTPUT
 
![316716596-6af845d8-7abd-4511-86a7-7e3d502a29eb](https://github.com/NAVEEN23013059/OS-Linux-commands-Shell-script/assets/150319555/009e765b-4c8a-4463-9cf2-df4a45f44efa)

 
cat forbreak.sh 
```bash
#!/bin/bash
# breaking out of a for loop
for var1 in 1 2 3 4 5
do
if [ $var1 -eq 3 ]
then
break
fi
echo "Iteration number: $var1"
done
echo "The for loop is completed“
```
## OUTPUT
![316716596-6af845d8-7abd-4511-86a7-7e3d502a29eb](https://github.com/NAVEEN23013059/OS-Linux-commands-Shell-script/assets/150319555/eccd64bf-a0cb-4102-9995-e8dc0dc0552f)



$ chmod 755 forbreak.sh
 
$ ./forbreak.sh 
 
cat forbreak.sh 
```bash
#!/bin/bash
# breaking out of a for loop
for var1 in 1 2 3 4 5
do
if [ $var1 -eq 3 ]
then
continue
fi
echo "Iteration number: $var1"
done
echo "The for loop is completed“
```

 
$ chmod 755 forcontinue.sh
 
$ ./forcontinue.sh 
## OUTPUT
 ![316716483-5f68dc6e-d782-4755-ae4d-2779817a8a49](https://github.com/NAVEEN23013059/OS-Linux-commands-Shell-script/assets/150319555/18c07a6c-ab4f-488d-97e2-c095cbf53a40)

cat exread.sh 
```bash
#!/bin/bash
# testing the read command
echo -n "Enter your name: "
read name
echo "Hello $name, welcome to my program. "
 ```
 
$ chmod 755 exread.sh 
 
$ ./exread.sh 
## OUTPUT


![316716342-595ee82c-49fd-46fe-8357-26901ec8e2ea](https://github.com/NAVEEN23013059/OS-Linux-commands-Shell-script/assets/150319555/a1dfd249-100e-4f5f-9aa4-016c3a502bdc)


 cat exread1.sh
```bash
#!/bin/bash
# testing the read command
read -p "Enter your name: " name
echo "Hello $name, welcome to my program. “
``` 
$ chmod 755 exread1.sh 

## OUTPUT

![316715995-de17793b-6c93-4235-87aa-a09b2ff46662](https://github.com/NAVEEN23013059/OS-Linux-commands-Shell-script/assets/150319555/cac39737-2911-4db8-9689-c18b51042839)




$ ./exread1.sh 
 
cat funcex.sh
```bash
#!/bin/bash
# trying to access script parameters inside a function
function func {
echo $[ $1 * $2 ]
}
if [ $# -eq 2 ]
then
value=`func $1 $2`
echo "The result is $value"
else
echo "Usage: badtest1 a b"
fi
```
## OUTPUT

![316715995-de17793b-6c93-4235-87aa-a09b2ff46662](https://github.com/NAVEEN23013059/OS-Linux-commands-Shell-script/assets/150319555/bf8f3b3a-eb94-434b-90a6-2c38306a5d6f)


 ./funcex.sh 

 
 ./funcex.sh 1 2

 
cat argshift.sh
```bash
#!/bin/bash 
 while (( "$#" )); do 
  echo $1 
  shift 
done
```
$ chmod 777 argshift.sh

## OUTPUT
![316715835-e74fbcc7-e92e-4774-bced-7b2fae5e3617](https://github.com/NAVEEN23013059/OS-Linux-commands-Shell-script/assets/150319555/58942500-92b0-4cb7-a06a-6397ccbd583c)


$ ./argshift.sh 1 2 3
 
 cat argshift1.sh
```bash
 #/bin/bash 
 # store arguments in a special array 
args=("$@") 
# get number of elements 
ELEMENTS=${#args[@]} 
 # echo each element in array  
# for loop 
for (( i=0;i<$ELEMENTS;i++)); do 
    echo ${args[${i}]} 
done
```
$ chmod 777 argshift.sh
## OUTPUT
$ ./argshift.sh 1 2 3
 
cat argshift.sh
```bash
#!/bin/bash 
set -x 
while (( "$#" )); do 
  echo $1 
  shift 
done
set +x
```
## OUTPUT

![316715730-07bf82e6-0425-444a-a0ae-61d9c92d9a4e](https://github.com/NAVEEN23013059/OS-Linux-commands-Shell-script/assets/150319555/acc6b674-d173-4ca3-812f-84c14d2291a3)

 ./argshift.sh 1 2 3
 
 
cat > nc.awk
```bash
BEGIN{}
{
print len=length($0),"\t",$0 
wordcount+=NF
chrcnt+=len
}
END {
print "total characters",chrcnt 
print "Number of Lines are",NR
print "No of Words count:",wordcount
}
 ```
cat>data.dat
```bash
bcdfghj
abcdfghj
bcdfghj
ebcdfghj
bcdfghj
ibcdfghj
bcdfghj
obcdfghj
bcdfghj
ubcdfghj
```
awk -f nc.awk data.dat
## OUTPUT 
![316715628-ca198f8b-6ece-47ac-b236-bf8b4db1f2bb](https://github.com/NAVEEN23013059/OS-Linux-commands-Shell-script/assets/150319555/8461af2d-2d3e-42cc-9ee2-6b9721b85037)

 
cat > palindrome.

```bash
#num=545
echo "Enter the number"
read num
s=0
rev=""
temp=$num
while [ $num -gt 0 ]
do
	# Get Remainder
	s=$(( $num % 10 ))
	# Get next digit
	num=$(( $num / 10 ))
	# Store previous number and
	# current digit in reverse
	rev=$( echo ${rev}${s} )
done
if [ $temp -eq $rev ];
then
	echo "Number is palindrome"
else
	echo "Number is NOT palindrome"
fi
```
## OUTPUT 
![316715496-ad48f573-4392-4d47-8cb8-927e77bd8199](https://github.com/NAVEEN23013059/OS-Linux-commands-Shell-script/assets/150319555/e56aa375-fa49-4390-ac94-85eecf5f7cbb)


# RESULT:
The Commands are executed successfully.

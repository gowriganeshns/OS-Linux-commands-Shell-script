# GOWTHAM N CSE(CS)
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
![image](https://github.com/HareeshrajaR/OS-Linux-commands-Shell-script/assets/144870459/7528a087-9824-44ac-aa77-6128901d8fc0)



cat < file2
## OUTPUT

![image](https://github.com/HareeshrajaR/OS-Linux-commands-Shell-script/assets/144870459/5efa87e6-0d63-4d21-9c17-8ea4c9f869ac)

# Comparing Files
cmp file1 file2
## OUTPUT
 ![image](https://github.com/HareeshrajaR/OS-Linux-commands-Shell-script/assets/144870459/2369bf72-0c7e-4a4a-8d9c-f2817448649e)

comm file1 file2
 ## OUTPUT
![image](https://github.com/HareeshrajaR/OS-Linux-commands-Shell-script/assets/144870459/34b7d485-8cd4-4686-ba34-2c670fcaafb5)


 
diff file1 file2
## OUTPUT

![image](https://github.com/HareeshrajaR/OS-Linux-commands-Shell-script/assets/144870459/af7bc968-5664-4eea-aecb-510f6fd2806c)

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

![image](https://github.com/HareeshrajaR/OS-Linux-commands-Shell-script/assets/144870459/c924d3c5-77d0-4d43-ab9a-9df9b570c884)



cut -d "|" -f 1 file22
## OUTPUT

![image](https://github.com/HareeshrajaR/OS-Linux-commands-Shell-script/assets/144870459/a1ade342-d6f7-40e0-bc3d-a2114ba4393b)


cut -d "|" -f 2 file22
## OUTPUT
![image](https://github.com/HareeshrajaR/OS-Linux-commands-Shell-script/assets/144870459/a785b063-a475-49fe-86ab-87934f42de4f)


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

![image](https://github.com/HareeshrajaR/OS-Linux-commands-Shell-script/assets/144870459/918fd2d1-a5c2-44b3-8857-af3a62a3dd90)


grep hello newfile 
## OUTPUT

![image](https://github.com/HareeshrajaR/OS-Linux-commands-Shell-script/assets/144870459/98b182a7-0843-4e15-9c9b-64bc6c808b4d)



grep -v hello newfile 
## OUTPUT


![image](https://github.com/HareeshrajaR/OS-Linux-commands-Shell-script/assets/144870459/73054690-36c2-4d1a-b158-b68a7b6b3507)

cat newfile | grep -i "hello"
## OUTPUT

![image](https://github.com/HareeshrajaR/OS-Linux-commands-Shell-script/assets/144870459/969653d1-89f7-4706-82dc-1f4780c78fdd)



cat newfile | grep -i -c "hello"
## OUTPUT

![image](https://github.com/HareeshrajaR/OS-Linux-commands-Shell-script/assets/144870459/844132bd-b8b5-4215-ba32-ba489c0d6014)



grep -R ubuntu /etc
## OUTPUT

![image](https://github.com/HareeshrajaR/OS-Linux-commands-Shell-script/assets/144870459/c7ce112d-af5e-4d92-a968-c92781ded17e)


grep -w -n world newfile   
## OUTPUT

![image](https://github.com/HareeshrajaR/OS-Linux-commands-Shell-script/assets/144870459/efc11869-fbbb-4274-a95e-b9fc5d38d7b8)

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

![image](https://github.com/HareeshrajaR/OS-Linux-commands-Shell-script/assets/144870459/f340880e-10a0-4153-a6e8-24f5803eb3d0)


egrep -w '(H|h)ello' newfile 
## OUTPUT

![image](https://github.com/HareeshrajaR/OS-Linux-commands-Shell-script/assets/144870459/bc13760c-523b-4bc9-a248-86612f8457aa)


egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT

![image](https://github.com/HareeshrajaR/OS-Linux-commands-Shell-script/assets/144870459/d52fc186-1711-4f61-b721-46c43149f75b)



egrep '(^hello)' newfile 
## OUTPUT

![image](https://github.com/HareeshrajaR/OS-Linux-commands-Shell-script/assets/144870459/dafcaa24-98f8-461c-834a-90a0f9f22042)


egrep '(world$)' newfile 
## OUTPUT


![image](https://github.com/HareeshrajaR/OS-Linux-commands-Shell-script/assets/144870459/e5b7a566-53ac-4c40-81d8-e92251d84705)


egrep '(World$)' newfile 
## OUTPUT
![image](https://github.com/HareeshrajaR/OS-Linux-commands-Shell-script/assets/144870459/db9b134b-2f67-4831-88f1-dd376546a9b1)


egrep '((W|w)orld$)' newfile 
## OUTPUT

![image](https://github.com/HareeshrajaR/OS-Linux-commands-Shell-script/assets/144870459/07b2b361-19d2-4325-a80f-90ee10da31a1)


egrep '[1-9]' newfile 
## OUTPUT

![image](https://github.com/HareeshrajaR/OS-Linux-commands-Shell-script/assets/144870459/e65b1028-bdfc-4c9d-80a5-690869d58baa)


egrep 'Linux.*world' newfile 
## OUTPUT

![image](https://github.com/HareeshrajaR/OS-Linux-commands-Shell-script/assets/144870459/717e504e-9ee0-45dd-8a43-20c54ce25e1a)

egrep 'Linux.*World' newfile 
## OUTPUT

![image](https://github.com/HareeshrajaR/OS-Linux-commands-Shell-script/assets/144870459/dba5e101-51b6-43cc-8fd4-24fda134e0e5)

egrep l{2} newfile
## OUTPUT

![image](https://github.com/HareeshrajaR/OS-Linux-commands-Shell-script/assets/144870459/77c4514f-f813-4c19-9398-e84c99e4ecf9)


egrep 's{1,2}' newfile
## OUTPUT 
![image](https://github.com/HareeshrajaR/OS-Linux-commands-Shell-script/assets/144870459/061d3ce2-4e67-4c87-88a4-18bf33137c2f)


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

![image](https://github.com/HareeshrajaR/OS-Linux-commands-Shell-script/assets/144870459/935675a0-9795-429f-b332-dac1a0df4585)


sed -n -e '$p' file23
## OUTPUT

![image](https://github.com/HareeshrajaR/OS-Linux-commands-Shell-script/assets/144870459/2c858b0e-ab68-440a-8444-7d752e2bb87f)


sed  -e 's/Ram/Sita/' file23
## OUTPUT

![image](https://github.com/HareeshrajaR/OS-Linux-commands-Shell-script/assets/144870459/171431fb-405a-46a2-a389-9bff3f7d5fd9)


sed  -e '2s/Ram/Sita/' file23
## OUTPUT

![image](https://github.com/HareeshrajaR/OS-Linux-commands-Shell-script/assets/144870459/3f7eb83f-3849-4559-8f9b-fd44dde88d9c)


sed  '/tom/s/5000/6000/' file23
## OUTPUT

![image](https://github.com/HareeshrajaR/OS-Linux-commands-Shell-script/assets/144870459/3d05d047-9edd-414c-bd64-180a50cb67bd)


sed -n -e '1,5p' file23
## OUTPUT

![image](https://github.com/HareeshrajaR/OS-Linux-commands-Shell-script/assets/144870459/3c3c8c82-64bf-4a61-b74d-0e4894fd0cce)


sed -n -e '2,/Joe/p' file23
## OUTPUT

![image](https://github.com/HareeshrajaR/OS-Linux-commands-Shell-script/assets/144870459/4a9ec8d2-4043-430b-bd3c-37e9ba77753b)



sed -n -e '/tom/,/Joe/p' file23
## OUTPUT

![image](https://github.com/HareeshrajaR/OS-Linux-commands-Shell-script/assets/144870459/f10b3ec1-8b19-481e-8dc0-c5aecdc79256)


seq 10 
## OUTPUT

![image](https://github.com/HareeshrajaR/OS-Linux-commands-Shell-script/assets/144870459/4d45e5ad-1b87-4e1b-ae3d-80a3c2499b88)


seq 10 | sed -n '4,6p'
## OUTPUT
![image](https://github.com/HareeshrajaR/OS-Linux-commands-Shell-script/assets/144870459/c599a819-c954-40cc-97b4-e0ba9840f76a)



seq 10 | sed -n '2,~4p'
## OUTPUT
![image](https://github.com/HareeshrajaR/OS-Linux-commands-Shell-script/assets/144870459/31847249-709d-4f4c-8a36-933006e8c918)



seq 3 | sed '2a hello'
## OUTPUT

![image](https://github.com/HareeshrajaR/OS-Linux-commands-Shell-script/assets/144870459/4e1e44e1-0275-4115-9eeb-17dca6edb024)


seq 2 | sed '2i hello'
## OUTPUT

![image](https://github.com/HareeshrajaR/OS-Linux-commands-Shell-script/assets/144870459/d4f040d9-b131-4c9f-b4bc-a232b3925822)

seq 10 | sed '2,9c hello'
## OUTPUT

![image](https://github.com/HareeshrajaR/OS-Linux-commands-Shell-script/assets/144870459/66d090d9-1141-4440-90d6-b6904930420e)

sed -n '2,4{s/^/$/;p}' file23



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

![image](https://github.com/HareeshrajaR/OS-Linux-commands-Shell-script/assets/144870459/f22c53a2-d867-44ff-b973-51aabcfea661)

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

![image](https://github.com/HareeshrajaR/OS-Linux-commands-Shell-script/assets/144870459/54b9d1b8-9935-40d1-8d31-24579af43011)


#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT
![image](https://github.com/HareeshrajaR/OS-Linux-commands-Shell-script/assets/144870459/ec3da3c1-d6e9-4626-8e83-f5ebac077abd)

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
![image](https://github.com/HareeshrajaR/OS-Linux-commands-Shell-script/assets/144870459/f0764e0d-496d-4b50-bed3-12af4f1247ee)


 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT

![image](https://github.com/HareeshrajaR/OS-Linux-commands-Shell-script/assets/144870459/510df307-db0f-45da-aa4e-53b487854204)


#Backup commands
tar -cvf backup.tar *
## OUTPUT

![image](https://github.com/HareeshrajaR/OS-Linux-commands-Shell-script/assets/144870459/eeb22489-13ad-4c16-8b3c-80b265c56342)

mkdir backupdir
 
mv backup.tar backupdir
 
tar -tvf backup.tar
## OUTPUT
![image](https://github.com/HareeshrajaR/OS-Linux-commands-Shell-script/assets/144870459/03050655-c052-4079-bdd0-0c1c456396e5)


tar -xvf backup.tar
## OUTPUT
![image](https://github.com/HareeshrajaR/OS-Linux-commands-Shell-script/assets/144870459/a8ba39c2-8596-4d5f-a90d-591c27ecd8f9)

gzip backup.tar


ls .gz
## OUTPUT
 ![image](https://github.com/HareeshrajaR/OS-Linux-commands-Shell-script/assets/144870459/0fcbfd6d-d13c-48bc-a517-f6ff9f64cdb6)

gunzip backup.tar.gz
## OUTPUT

 ![image](https://github.com/HareeshrajaR/OS-Linux-commands-Shell-script/assets/144870459/9a516b72-0dbb-426b-80cd-a0c35dbe56b9)

# Shell Script
```
echo '#!/bin/sh' > my-script.sh
echo 'echo Hello World‘; exit 0 >> my-script.sh
```
chmod 755 my-script.sh
./my-script.sh
## OUTPUT

 ![image](https://github.com/HareeshrajaR/OS-Linux-commands-Shell-script/assets/144870459/944a6318-0993-41f0-83a3-4e0d31c7747b)

cat << stop > herecheck.txt
```
hello in this world
i cant stop
for this non stop movement
stop
```

cat herecheck.txt
## OUTPUT
![image](https://github.com/HareeshrajaR/OS-Linux-commands-Shell-script/assets/144870459/a67ef2a8-efa1-4d30-b46f-c4d8d9aff6f6)


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
![image](https://github.com/HareeshrajaR/OS-Linux-commands-Shell-script/assets/144870459/3bf7acf6-ced2-49b4-8c26-3aee860d283d)

 
ls file1
## OUTPUT
![image](https://github.com/HareeshrajaR/OS-Linux-commands-Shell-script/assets/144870459/062e9d43-b487-4175-9d66-638f4eae8124)

echo $?
## OUTPUT 
![image](https://github.com/HareeshrajaR/OS-Linux-commands-Shell-script/assets/144870459/b3dc11e7-1fb9-42eb-9fc0-5dee991a740a)

./onebash: ./one: Permission denied
 
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
## OUTPUT

![image](https://github.com/HareeshrajaR/OS-Linux-commands-Shell-script/assets/144870459/d3c586d5-7711-4037-bef5-a5471159e95d)


chmod 755 strcomp.sh
 
./strcomp.sh 
## OUTPUT
![image](https://github.com/HareeshrajaR/OS-Linux-commands-Shell-script/assets/144870459/802c33b4-9293-4c1e-a42e-03b3001bd464)


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
![image](https://github.com/HareeshrajaR/OS-Linux-commands-Shell-script/assets/144870459/0767a906-2530-4dc9-b718-f9df8f324d56)

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
![image](https://github.com/HareeshrajaR/OS-Linux-commands-Shell-script/assets/144870459/2af720ff-fe3f-4448-b7de-6bbc53f400e0)



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
## OUTPUT
![image](https://github.com/HareeshrajaR/OS-Linux-commands-Shell-script/assets/144870459/dd76eefb-8f02-47ed-b214-bcedadd6fac3)

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
## OUTPUT
![image](https://github.com/HareeshrajaR/OS-Linux-commands-Shell-script/assets/144870459/0d818d8b-f359-4a2d-bcc9-33c4d8eb2e2a)

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

![image](https://github.com/HareeshrajaR/OS-Linux-commands-Shell-script/assets/144870459/60f3ced8-cf0f-4712-a8b1-799d7e7597b5)

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
![image](https://github.com/HareeshrajaR/OS-Linux-commands-Shell-script/assets/144870459/8ec298bf-4359-4da2-9872-c2c13b620661)

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
## OUTPUT
![image](https://github.com/HareeshrajaR/OS-Linux-commands-Shell-script/assets/144870459/2e1927ad-e4fb-429e-8220-dcb542af2b1b)

 
cat > whiletest.sh
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
## OUTPUT
![image](https://github.com/HareeshrajaR/OS-Linux-commands-Shell-script/assets/144870459/b43d560e-1485-41e9-a36c-c529930a5bd2)

 
 
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
 
 ## OUTPUT
 ![image](https://github.com/HareeshrajaR/OS-Linux-commands-Shell-script/assets/144870459/690a4c5c-abde-49ba-845e-9d3aed194677)

 
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
 ## OUTPUT
 ![image](https://github.com/HareeshrajaR/OS-Linux-commands-Shell-script/assets/144870459/a4c8db23-b308-4106-93b7-20c4c0e30fbf)

 
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
 ## OUTPUT
 ![image](https://github.com/HareeshrajaR/OS-Linux-commands-Shell-script/assets/144870459/0541fbbd-8226-43ed-a89e-746691689be3)

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
## OUTPUT

![image](https://github.com/HareeshrajaR/OS-Linux-commands-Shell-script/assets/144870459/d91349d5-3f02-4fe8-8c30-56eae0bd5908)

$ cat > cities
Hyderabad
Alampur
Basara
Warangal
Adilabad
Bhadrachalam
Khammam

## OUTPUT
![image](https://github.com/HareeshrajaR/OS-Linux-commands-Shell-script/assets/144870459/5a2a72e8-7829-4a2a-aa50-d45b84acae28)


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
![image](https://github.com/HareeshrajaR/OS-Linux-commands-Shell-script/assets/144870459/ee0760bc-1152-48ec-8c28-bfb9699bf539)

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
![image](https://github.com/HareeshrajaR/OS-Linux-commands-Shell-script/assets/144870459/d2b9b477-6a26-4eff-8ad9-1ef84070fd13)

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

 ![image](https://github.com/HareeshrajaR/OS-Linux-commands-Shell-script/assets/144870459/7a6b46e9-a024-46d4-9770-51057f95ae6c)

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
 ![image](https://github.com/HareeshrajaR/OS-Linux-commands-Shell-script/assets/144870459/86ddc8e8-f42d-4e7d-bb4b-e1cc69bb8625)

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
![image](https://github.com/HareeshrajaR/OS-Linux-commands-Shell-script/assets/144870459/32c1adce-cb5d-44c2-8050-b35d2fa6c778)


 cat exread1.sh
```bash
#!/bin/bash
# testing the read command
read -p "Enter your name: " name
echo "Hello $name, welcome to my program. “
``` 
$ chmod 755 exread1.sh 

## OUTPUT



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
![image](https://github.com/HareeshrajaR/OS-Linux-commands-Shell-script/assets/144870459/bc56e21d-c2ed-44c4-a627-a651370559fd)

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
![image](https://github.com/HareeshrajaR/OS-Linux-commands-Shell-script/assets/144870459/12baf701-1c70-4fb0-a366-381d01418dce)

 
 cat >argshift1.sh
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
$ ./argshift.sh 1 2 3
## OUTPUT
![image](https://github.com/HareeshrajaR/OS-Linux-commands-Shell-script/assets/144870459/5724f3a3-fc08-4383-b0f1-1314f98e019e)


 
cat >argshift.sh
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
 ./argshift.sh 1 2 3
 
 ![image](https://github.com/HareeshrajaR/OS-Linux-commands-Shell-script/assets/144870459/e954b54f-ca35-4f34-bf46-9d87602e221e)

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
 ![image](https://github.com/HareeshrajaR/OS-Linux-commands-Shell-script/assets/144870459/654bba20-181a-4810-8919-6f5d5e990f32)

cat > palindrome.sh
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
![image](https://github.com/HareeshrajaR/OS-Linux-commands-Shell-script/assets/144870459/4c86ecae-a50d-4a9d-8146-78ad4d1d4a20)



# RESULT:
The Commands are executed successfully.

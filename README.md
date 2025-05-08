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
![image](https://github.com/EzhilsreeJ/OS-Linux-commands-Shell-script/assets/144870412/a2098cdc-e082-4aa0-8a5a-37757d65dc4e)



cat < file2
## OUTPUT

![image](https://github.com/EzhilsreeJ/OS-Linux-commands-Shell-script/assets/144870412/e1d80f93-4510-4009-aaf7-6919d3839d69)


# Comparing Files
cmp file1 file2
## OUTPUT
 ![image](https://github.com/EzhilsreeJ/OS-Linux-commands-Shell-script/assets/144870412/330e66a1-395d-4718-b691-de8530159f3c)

comm file1 file2
 ## OUTPUT

 ![image](https://github.com/EzhilsreeJ/OS-Linux-commands-Shell-script/assets/144870412/ab4aa939-f9cb-43f1-9d75-1259cd8d8fed)

diff file1 file2
## OUTPUT
![image](https://github.com/EzhilsreeJ/OS-Linux-commands-Shell-script/assets/144870412/123f2d7e-ce13-4484-a2f6-e0a79601a4ea)


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

![image](https://github.com/EzhilsreeJ/OS-Linux-commands-Shell-script/assets/144870412/ffe6152f-bc01-4e38-a82d-6dd208ce1967)



cut -d "|" -f 1 file22
## OUTPUT

![image](https://github.com/EzhilsreeJ/OS-Linux-commands-Shell-script/assets/144870412/9a3a0b77-5360-4cbe-90f2-6400b1c723a9)


cut -d "|" -f 2 file22
## OUTPUT
![image](https://github.com/EzhilsreeJ/OS-Linux-commands-Shell-script/assets/144870412/7c4c4392-5801-4e33-90f7-158f8b91b9f6)


cat > newfile 
```
Hello world
hello world
^d
````
cat < newfile 
Hello world
hello world
 
grep Hello newfile 
## OUTPUT

![image](https://github.com/EzhilsreeJ/OS-Linux-commands-Shell-script/assets/144870412/e3967bd6-4fca-4920-92c8-53fac552a111)


grep hello newfile 
## OUTPUT

![image](https://github.com/EzhilsreeJ/OS-Linux-commands-Shell-script/assets/144870412/0e322eb8-5e63-4abe-b1f2-48ec54e535f4)




grep -v hello newfile 
## OUTPUT

![image](https://github.com/EzhilsreeJ/OS-Linux-commands-Shell-script/assets/144870412/f6ac291a-7642-4337-837a-10fe3ab034e7)


cat newfile | grep -i "hello"
## OUTPUT

![image](https://github.com/EzhilsreeJ/OS-Linux-commands-Shell-script/assets/144870412/c25d5ce9-0ba2-4400-9693-bd966a244a2b)



cat newfile | grep -i -c "hello"
## OUTPUT

![image](https://github.com/EzhilsreeJ/OS-Linux-commands-Shell-script/assets/144870412/3e067559-1413-4573-a45d-5c6896bd8f32)



grep -R ubuntu /etc
## OUTPUT

![image](https://github.com/EzhilsreeJ/OS-Linux-commands-Shell-script/assets/144870412/7e50f0bb-a7df-4712-9a1f-e433e573c4d8)



grep -w -n world newfile   
## OUTPUT
![image](https://github.com/EzhilsreeJ/OS-Linux-commands-Shell-script/assets/144870412/aea89003-bcf5-4e01-99ba-c757c58dafab)


cat > newfile 
```
Hello world
hello world
Linux is world number 1
Unix is predecessor
Linux is best in this World
^d
```

cat < newfile
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
![image](https://github.com/EzhilsreeJ/OS-Linux-commands-Shell-script/assets/144870412/3ed6244f-aeac-49ca-b722-28c4f471aa68)



egrep -w '(H|h)ello' newfile 
## OUTPUT
![image](https://github.com/EzhilsreeJ/OS-Linux-commands-Shell-script/assets/144870412/6914ac05-5482-4dde-bdba-5039eb3db230)



egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT




egrep '(^hello)' newfile 
## OUTPUT
![image](https://github.com/EzhilsreeJ/OS-Linux-commands-Shell-script/assets/144870412/c061646f-612a-4210-97da-720257b08fd8)



egrep '(world$)' newfile 
## OUTPUT

![image](https://github.com/EzhilsreeJ/OS-Linux-commands-Shell-script/assets/144870412/bbd8cdd0-8d3e-4991-91f9-0d2dfdf649ce)


egrep '(World$)' newfile 
## OUTPUT


egrep '((W|w)orld$)' newfile 
## OUTPUT

![image](https://github.com/EzhilsreeJ/OS-Linux-commands-Shell-script/assets/144870412/2b05273a-8abf-474a-8779-fc5793e893ca)


egrep '[1-9]' newfile 
## OUTPUT

![image](https://github.com/EzhilsreeJ/OS-Linux-commands-Shell-script/assets/144870412/48f6b45d-988f-488b-bf8d-0d3299da405b)


egrep 'Linux.*world' newfile 
## OUTPUT
![image](https://github.com/EzhilsreeJ/OS-Linux-commands-Shell-script/assets/144870412/9acaa140-4631-4e08-b966-7dc9174ddb2d)


egrep 'Linux.*World' newfile 
## OUTPUT


egrep l{2} newfile
## OUTPUT



egrep 's{1,2}' newfile
## OUTPUT 
![image](https://github.com/EzhilsreeJ/OS-Linux-commands-Shell-script/assets/144870412/9725c4b3-33ab-4353-bf3c-d44a4fc5ce35)


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

![image](https://github.com/EzhilsreeJ/OS-Linux-commands-Shell-script/assets/144870412/37bc66c4-c69d-4eed-b390-c9d7c8d6ebf8)


sed -n -e '$p' file23
## OUTPUT
![image](https://github.com/EzhilsreeJ/OS-Linux-commands-Shell-script/assets/144870412/89720c0e-e06c-4095-9098-0199d94b0ea6)



sed  -e 's/Ram/Sita/' file23
## OUTPUT

![image](https://github.com/EzhilsreeJ/OS-Linux-commands-Shell-script/assets/144870412/8ad0adb8-85cd-4f26-8285-284d93012ab4)


sed  -e '2s/Ram/Sita/' file23
## OUTPUT

![image](https://github.com/EzhilsreeJ/OS-Linux-commands-Shell-script/assets/144870412/5fcbf7de-d343-4430-81b4-cb939f614ab3)


sed  '/tom/s/5000/6000/' file23
## OUTPUT

![image](https://github.com/EzhilsreeJ/OS-Linux-commands-Shell-script/assets/144870412/77ae23cb-b5a4-42a5-804d-b8609f5db589)


sed -n -e '1,5p' file23
## OUTPUT
![image](https://github.com/EzhilsreeJ/OS-Linux-commands-Shell-script/assets/144870412/108d406e-1463-42c5-887b-e853fec41d99)



sed -n -e '2,/Joe/p' file23
## OUTPUT

![image](https://github.com/EzhilsreeJ/OS-Linux-commands-Shell-script/assets/144870412/7cb9e47e-72e0-47a5-ad1b-14b123952276)



sed -n -e '/tom/,/Joe/p' file23
## OUTPUT

![image](https://github.com/EzhilsreeJ/OS-Linux-commands-Shell-script/assets/144870412/f542b2db-825f-4ca6-856e-4b798ca7462b)


seq 10 
## OUTPUT

![image](https://github.com/EzhilsreeJ/OS-Linux-commands-Shell-script/assets/144870412/079dd40e-13bf-493a-9e98-db96b30f71ef)


seq 10 | sed -n '4,6p'
## OUTPUT

![image](https://github.com/EzhilsreeJ/OS-Linux-commands-Shell-script/assets/144870412/5c540b63-9778-464c-8371-e94ec4e28540)


seq 10 | sed -n '2,~4p'
## OUTPUT
![image](https://github.com/EzhilsreeJ/OS-Linux-commands-Shell-script/assets/144870412/294b1247-5f49-426f-9c6c-ac0cb60b86a0)



seq 3 | sed '2a hello'
## OUTPUT

![image](https://github.com/EzhilsreeJ/OS-Linux-commands-Shell-script/assets/144870412/454e33b1-e8b9-43e5-90c7-52c75cc99864)


seq 2 | sed '2i hello'
## OUTPUT
![image](https://github.com/EzhilsreeJ/OS-Linux-commands-Shell-script/assets/144870412/9e5bb04c-7dc6-4b05-9a3c-b9e722126f95)


seq 10 | sed '2,9c hello'
## OUTPUT
![image](https://github.com/EzhilsreeJ/OS-Linux-commands-Shell-script/assets/144870412/e2bd0512-86ce-461c-b48e-7bdbe7721b04)


sed -n '2,4{s/^/$/;p}' file23
## OUTPUT

![image](https://github.com/EzhilsreeJ/OS-Linux-commands-Shell-script/assets/144870412/fcd129d5-ed73-494f-b1b1-0ef8cd86d7a6)


sed -n '2,4{s/$/*/;p}' file23
## OUTPUT
![image](https://github.com/EzhilsreeJ/OS-Linux-commands-Shell-script/assets/144870412/7d786d5b-1adb-432d-ade1-d179750dd697)


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
![image](https://github.com/EzhilsreeJ/OS-Linux-commands-Shell-script/assets/144870412/6a9fde1e-980c-4f57-873f-6c314f9b47b0)


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

![image](https://github.com/EzhilsreeJ/OS-Linux-commands-Shell-script/assets/144870412/e1c8f14b-a8b7-411c-b1af-074232536292)


#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT
![image](https://github.com/EzhilsreeJ/OS-Linux-commands-Shell-script/assets/144870412/fc856008-1d83-4536-a357-4b488060b1c4)

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



#Backup commands
tar -cvf backup.tar *
## OUTPUT


mkdir backupdir
 
mv backup.tar backupdir

cd backupdir
 
tar -tvf backup.tar
## OUTPUT


tar -xvf backup.tar
## OUTPUT

gzip backup.tar

ls .gz
## OUTPUT
 
gunzip backup.tar.gz
## OUTPUT

 
# Shell Script
```
echo '#!/bin/sh' > my-script.sh
echo 'echo Hello World‘; exit 0 >> my-script.sh
```
chmod 755 my-script.sh
./my-script.sh
## OUTPUT

 
cat << stop > herecheck.txt
```
hello in this world
i cant stop
for this non stop movement
stop
```

cat herecheck.txt
## OUTPUT


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

 
ls file1
## OUTPUT

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


# RESULT:
The Commands are executed successfully.


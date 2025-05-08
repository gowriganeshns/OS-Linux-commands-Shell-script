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
```
chanchal singhvi
c.k. shukla
s.n. dasgupta
sumit chakrobarty
^d
```
cat < file2
## OUTPUT
cat > file2
```
anil aggarwal
barun sengupta
c.k. shukla
lalit chowdury
s.n. dasgupta
^d
```
# Comparing Files
cmp file1 file2

 
 ## OUTPUT
![303979828-3d17b2b3-39c8-43a8-abdc-519c900acba8](https://github.com/23004513/OS-Linux-commands-Shell-script/assets/138973069/75a5512e-1a3b-45f7-ad9a-369f872d4e8a)



comm file1 file2

## OUTPUT

![303980017-9f15abc6-fa53-4ce6-9690-41d0c5527c64](https://github.com/23004513/OS-Linux-commands-Shell-script/assets/138973069/06aaf5ba-ea64-4e0c-8499-115f566e830f)



diff file1 file2


##OUTPUT
![303980022-6f0df5d6-6dc0-473f-8764-8f8788dc1423](https://github.com/23004513/OS-Linux-commands-Shell-script/assets/138973069/dd5d576c-fdad-4142-8a42-957143d516bb)



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

![303980526-e74cc399-e869-4514-9294-e4d66bdbb553](https://github.com/23004513/OS-Linux-commands-Shell-script/assets/138973069/057abf47-bdbc-4ed1-b8c0-df0302401aad)



cut -d "|" -f 1 file22
## OUTPUT

![303980625-45a81470-3b96-4c0b-9c34-21ef65d280c1](https://github.com/23004513/OS-Linux-commands-Shell-script/assets/138973069/64f3b346-85d6-40e6-a5ca-0795b38c67c2)

cut -d "|" -f 2 file22
## OUTPUT
![303980718-81235175-e464-4178-a1da-d78a36605b9b](https://github.com/23004513/OS-Linux-commands-Shell-script/assets/138973069/26e24d41-1567-4bb7-a427-463ae5f32f95)


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

![304111559-7d5dc360-1c3a-4ec4-9367-a9d3ebf3da9d](https://github.com/23004513/OS-Linux-commands-Shell-script/assets/138973069/a75c35a9-3407-45bb-a60c-51ac39e93dd0)


grep hello newfile 
## OUTPUT
![304111717-3b622860-62e3-4eba-88ad-9644765927df](https://github.com/23004513/OS-Linux-commands-Shell-script/assets/138973069/1fed07d9-9937-4958-934c-dae3f0c403d3)




grep -v hello newfile 
## OUTPUT

![304112410-0a4e551a-c35b-4f53-a343-e0c41baeefdf](https://github.com/23004513/OS-Linux-commands-Shell-script/assets/138973069/675e0427-572c-4aca-953c-cc45455944ae)


cat newfile | grep -i "hello"
## OUTPUT
![304112674-10be401c-081e-4138-af1f-88aa41158c77](https://github.com/23004513/OS-Linux-commands-Shell-script/assets/138973069/8dea6fe3-2ada-4ab9-ae14-db1f7eaa36f7)




cat newfile | grep -i -c "hello"
## OUTPUT

![304113192-a2eb2603-767e-486a-bb38-c9e1f53f51a3](https://github.com/23004513/OS-Linux-commands-Shell-script/assets/138973069/fd4ce646-de28-4957-83b6-e305c1f4439a)


grep -R ubuntu /etc
## OUTPUT
grep -w -n world newfile   
## OUTPUT

![304114184-cb370c18-be74-432d-9314-51f331acf7df](https://github.com/23004513/OS-Linux-commands-Shell-script/assets/138973069/dfaf1853-3e52-470b-9bc5-38d3057ce4b2)

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

![304114445-2d621e3e-9f9a-44ac-a6db-043fdba5cc21](https://github.com/23004513/OS-Linux-commands-Shell-script/assets/138973069/63f44836-f6b6-4d66-bdf4-9a53fb6fe0d4)


egrep -w '(H|h)ello' newfile 
## OUTPUT


![304114664-f2413676-3063-4310-9007-e31987305c59](https://github.com/23004513/OS-Linux-commands-Shell-script/assets/138973069/8cc574fc-24a7-4e1d-bfd0-56ca0ff8dd45)

egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT

![304116131-7a74a2cf-5316-47fc-8448-8cae00930409](https://github.com/23004513/OS-Linux-commands-Shell-script/assets/138973069/50e2bb9b-2c9b-4df4-9d46-903adbd0e6da)



egrep '(^hello)' newfile 
## OUTPUT
![304751858-2097ab41-753f-4c27-bf30-f3c2b3edd826](https://github.com/23004513/OS-Linux-commands-Shell-script/assets/138973069/67ad9538-9b91-423e-8266-1fb2edbc9d40)



egrep '(world$)' newfile 
## OUTPUT

![304752068-d6105214-5e17-4bcf-82c9-256ac369f797](https://github.com/23004513/OS-Linux-commands-Shell-script/assets/138973069/6339ba41-1e5e-443d-825d-b2809e856a19)


egrep '(World$)' newfile 
## OUTPUT

![304752280-d3019e06-e463-45ab-bf66-985f54a7edb9](https://github.com/23004513/OS-Linux-commands-Shell-script/assets/138973069/fb6711f3-9556-4718-a749-555f06debab1)

egrep '((W|w)orld$)' newfile 
## OUTPUT
![304752550-c0c28d29-8373-4c75-b10a-e3a1ee97271a](https://github.com/23004513/OS-Linux-commands-Shell-script/assets/138973069/cc9d61d6-82b4-42a2-a3eb-593038c19fc7)



egrep '[1-9]' newfile 
## OUTPUT
![304752743-d525b4d0-ceaf-456e-b23e-98fc98180629](https://github.com/23004513/OS-Linux-commands-Shell-script/assets/138973069/6d099778-2b88-4e6f-8b06-c40b2f09a638)



egrep 'Linux.*world' newfile 
## OUTPUT
![304753008-b3b81c41-51b4-406b-b712-21a2a4c9d97c](https://github.com/23004513/OS-Linux-commands-Shell-script/assets/138973069/d1c365df-03a4-4e54-928e-4a381e058096)


egrep 'Linux.*World' newfile 
## OUTPUT

![304753573-6bb38c3a-f787-4522-9190-8a797f9ec430](https://github.com/23004513/OS-Linux-commands-Shell-script/assets/138973069/591ab9e6-e543-40a3-a4ec-f9012f8ceadf)

egrep l{2} newfile
## OUTPUT

![304754057-82fd9878-0b30-4a54-8ab5-18dd15381f65](https://github.com/23004513/OS-Linux-commands-Shell-script/assets/138973069/98619322-54a4-4a4c-ad34-fa84af7dfff4)


egrep 's{1,2}' newfile
## OUTPUT 
![304754458-c92a0337-816f-4d2f-a34d-6748b3cb1bee](https://github.com/23004513/OS-Linux-commands-Shell-script/assets/138973069/91245c5a-f669-4b1c-8641-44667f0689f7)


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
![304757591-a648b63d-4908-491b-83e2-15d2a6549860](https://github.com/23004513/OS-Linux-commands-Shell-script/assets/138973069/6067006c-52ab-4263-bb7c-8675a5cba9d7)



sed -n -e '$p' file23
## OUTPUT
sed  -e 's/Ram/Sita/' file23
## OUTPUT

![304758431-084144ca-9506-4676-8b2a-4ce86686c9e6](https://github.com/23004513/OS-Linux-commands-Shell-script/assets/138973069/ea154aa6-2031-4bc9-a5fa-d246da2078ce)


sed  -e '2s/Ram/Sita/' file23
## OUTPUT


![304758637-033e8dc7-f710-400f-9fa0-78d15ed14fce](https://github.com/23004513/OS-Linux-commands-Shell-script/assets/138973069/b35d81b6-ed9b-4d25-b8cb-d3ca5c25fdf0)

sed  '/tom/s/5000/6000/' file23
## OUTPUT

![304759583-b67f110e-2c70-4583-a1be-a37ad91ad49d](https://github.com/23004513/OS-Linux-commands-Shell-script/assets/138973069/e6e1ba26-5291-43fd-8f40-d6fe00a20498)


sed -n -e '1,5p' file23

## OUTPUT

![304759738-4539c59e-1967-4511-aa85-02e0193a1e13](https://github.com/23004513/OS-Linux-commands-Shell-script/assets/138973069/d727de65-8c1f-474b-a1a7-2d87bbc4b354)



sed -n -e '2,/Joe/p' file23
## OUTPUT

![304759889-30234a9f-dd11-4ae5-b7a5-9045148072a0](https://github.com/23004513/OS-Linux-commands-Shell-script/assets/138973069/ca6da655-591e-498b-9afb-e9bcd8e09c64)



sed -n -e '/tom/,/Joe/p' file23
## OUTPUT

![304766794-9a68ec8b-c637-4d4f-b099-279531805f0b](https://github.com/23004513/OS-Linux-commands-Shell-script/assets/138973069/7a82bd4e-4d0e-4340-89d1-882aa938ae94)



seq 10 
## OUTPUT

![304767015-a6426c76-366f-4acd-9a74-05d4c22cd1ef](https://github.com/23004513/OS-Linux-commands-Shell-script/assets/138973069/fa19b57d-1c9d-4bef-81a8-159ef1e802be)


seq 10 | sed -n '4,6p'
## OUTPUT

![304767368-be70bf5e-1699-41fc-aa85-bdcde8e946ca](https://github.com/23004513/OS-Linux-commands-Shell-script/assets/138973069/a4650fd0-7816-4e90-88fe-036a692d2e76)


seq 10 | sed -n '2,~4p'
## OUTPUT

![304767623-4dae8842-394b-4660-98d8-f1ff6de58121](https://github.com/23004513/OS-Linux-commands-Shell-script/assets/138973069/e76d46db-4e87-4616-adf3-209f22705a28)


seq 3 | sed '2a hello'
## OUTPUT


![304768147-98a1731b-3015-45f1-ba23-6cb031f09c8d](https://github.com/23004513/OS-Linux-commands-Shell-script/assets/138973069/b251a39b-a769-44e6-aca2-a4a33e8afc48)

seq 2 | sed '2i hello'
##OUTPUT

![304768296-37f79adc-6b21-4499-bbfa-d74aeae1461a](https://github.com/23004513/OS-Linux-commands-Shell-script/assets/138973069/50840e06-7531-454b-893b-82157fa696d9)


seq 10 | sed '2,9c hello'
## OUTPUT

![304768441-9c4330d4-0447-451d-a81a-cf358636d16d](https://github.com/23004513/OS-Linux-commands-Shell-script/assets/138973069/02460176-5dbc-4cd3-86e2-676ef79130bc)


sed -n '2,4{s/^/$/;p}' file23
## OUTPUT

![304768689-da40ce9b-3d87-4252-90db-988a1f344a81](https://github.com/23004513/OS-Linux-commands-Shell-script/assets/138973069/757e595f-068c-4a2d-9a74-a0c5c280d674)

sed -n '2,4{s/$/*/;p}' file23
##OUTPUT

![304769027-3459be51-4d3f-4d3b-a8ad-e63a1fcadd62](https://github.com/23004513/OS-Linux-commands-Shell-script/assets/138973069/3a948998-5ccc-471c-8301-871e4f040ac5)


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

![304769719-6ddff4be-6d23-46ab-9e48-2d436930fea3](https://github.com/23004513/OS-Linux-commands-Shell-script/assets/138973069/9dcd56c0-8260-4a34-a658-4a9bedfc00a6)

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


![304771138-0b50c2dc-0ef6-4965-92c6-5b0ff5735bd1](https://github.com/23004513/OS-Linux-commands-Shell-script/assets/138973069/10564297-a8ca-42e7-9e7b-11d2f5823b34)


#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT
 
![304771761-734761d9-86e9-4b02-9948-1a8de5e92c36](https://github.com/23004513/OS-Linux-commands-Shell-script/assets/138973069/9ddada14-d8d3-4b5a-a383-4e756bac6c9c)

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


 ![304797034-9a10a40c-28d3-4c0d-929f-609b1615fb79](https://github.com/23004513/OS-Linux-commands-Shell-script/assets/138973069/a3958730-a84b-4be3-934c-75127fd45e20)

cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT

![304797372-2499ab97-1897-440e-b6b7-2d2f3a95a31a](https://github.com/23004513/OS-Linux-commands-Shell-script/assets/138973069/36ba05c2-828f-4cf0-b89c-7704eb2a9ca0)


#Backup commands
tar -cvf backup.tar *
## OUTPUT

![304797792-7f1581bd-5f95-4e4e-866f-1699b6f40de5](https://github.com/23004513/OS-Linux-commands-Shell-script/assets/138973069/59aebb74-5bab-4b16-856c-0702c0987aa0)

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

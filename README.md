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
![1](https://github.com/VPOOJAASREE/OS-Linux-commands-Shell-script/assets/155145525/7d68dce0-534a-4e2c-8b89-d822f595251d)


cat < file2
## OUTPUT
![2](https://github.com/VPOOJAASREE/OS-Linux-commands-Shell-script/assets/155145525/4dc8ba1f-c6a0-4142-9c59-e153627bbe0b)


# Comparing Files
cmp file1 file2
## OUTPUT
![3](https://github.com/VPOOJAASREE/OS-Linux-commands-Shell-script/assets/155145525/82bbb511-bebc-4949-913c-2004b6132263)

 
comm file1 file2
 ## OUTPUT
 ![4](https://github.com/VPOOJAASREE/OS-Linux-commands-Shell-script/assets/155145525/80cce471-2ba7-477a-83aa-6ecf0db66e90)


diff file1 file2
## OUTPUT
![5](https://github.com/VPOOJAASREE/OS-Linux-commands-Shell-script/assets/155145525/fe734926-2f5b-485f-9956-f8ea7da9c0ab)



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
![6](https://github.com/VPOOJAASREE/OS-Linux-commands-Shell-script/assets/155145525/d174de7f-5a57-448c-920d-4db2819ba777)


cut -d "|" -f 1 file22
## OUTPUT
![7](https://github.com/VPOOJAASREE/OS-Linux-commands-Shell-script/assets/155145525/d71a633f-3ae3-48e0-bcfd-ea3f75b2983a)


cut -d "|" -f 2 file22
## OUTPUT
![8](https://github.com/VPOOJAASREE/OS-Linux-commands-Shell-script/assets/155145525/6b0d3852-a8d7-4f36-8990-f73df0564d61)



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
![9](https://github.com/VPOOJAASREE/OS-Linux-commands-Shell-script/assets/155145525/cfeb20d5-8c20-4a07-ae94-77cddd26bafe)


grep hello newfile 
## OUTPUT
![10](https://github.com/VPOOJAASREE/OS-Linux-commands-Shell-script/assets/155145525/69af16c5-80e9-4c71-abf9-fa5647db389b)


grep -v hello newfile 
## OUTPUT
![11](https://github.com/VPOOJAASREE/OS-Linux-commands-Shell-script/assets/155145525/60c40c09-606d-4901-a7f2-10754416ab03)


cat newfile | grep -i "hello"
## OUTPUT
![12](https://github.com/VPOOJAASREE/OS-Linux-commands-Shell-script/assets/155145525/55a8b75d-b507-4539-a960-0b1e3f99adec)



cat newfile | grep -i -c "hello"
## OUTPUT
![13](https://github.com/VPOOJAASREE/OS-Linux-commands-Shell-script/assets/155145525/51276fc6-65cc-4c29-83e1-fd631c6d83b4)




grep -R ubuntu /etc
## OUTPUT
![14](https://github.com/VPOOJAASREE/OS-Linux-commands-Shell-script/assets/155145525/35961fed-0a61-4357-a85a-cc227da6d754)



grep -w -n world newfile   
## OUTPUT
![15](https://github.com/VPOOJAASREE/OS-Linux-commands-Shell-script/assets/155145525/92b93a08-db9e-401b-8750-3418d7ab1266)



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
![16](https://github.com/VPOOJAASREE/OS-Linux-commands-Shell-script/assets/155145525/c54659ae-8415-4d86-82f6-b975ba714d70)


egrep -w '(H|h)ello' newfile 
## OUTPUT
![17](https://github.com/VPOOJAASREE/OS-Linux-commands-Shell-script/assets/155145525/9cd9b749-3efe-467b-a292-6225f7eea3d8)


egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT
![18](https://github.com/VPOOJAASREE/OS-Linux-commands-Shell-script/assets/155145525/87018045-f97e-4c31-943b-341c17423e90)


egrep '(^hello)' newfile 
## OUTPUT
![19](https://github.com/VPOOJAASREE/OS-Linux-commands-Shell-script/assets/155145525/d08322f6-aceb-40a6-821f-008f20d85dd3)


egrep '(world$)' newfile 
## OUTPUT
![20](https://github.com/VPOOJAASREE/OS-Linux-commands-Shell-script/assets/155145525/ceab53e7-f82f-4bcc-af10-91c0e0f5f141)


egrep '(World$)' newfile 
## OUTPUT
![21](https://github.com/VPOOJAASREE/OS-Linux-commands-Shell-script/assets/155145525/38f28771-ae56-4891-b325-0d6a9e93f41f)


egrep '((W|w)orld$)' newfile 
## OUTPUT
![22](https://github.com/VPOOJAASREE/OS-Linux-commands-Shell-script/assets/155145525/6c604f63-2369-4d1a-8ab3-4d7b65c32537)


egrep '[1-9]' newfile 
## OUTPUT
![23](https://github.com/VPOOJAASREE/OS-Linux-commands-Shell-script/assets/155145525/9cca5fed-6632-4149-8a78-c809c92d7c33)


egrep 'Linux.*world' newfile 
## OUTPUT
![24](https://github.com/VPOOJAASREE/OS-Linux-commands-Shell-script/assets/155145525/15e70b4b-7a7b-4602-9635-77a44921967b)


egrep 'Linux.*World' newfile 
## OUTPUT
![25](https://github.com/VPOOJAASREE/OS-Linux-commands-Shell-script/assets/155145525/b05ea97a-c37c-40da-bd42-63a0fa9fb48f)


egrep l{2} newfile
## OUTPUT
![26](https://github.com/VPOOJAASREE/OS-Linux-commands-Shell-script/assets/155145525/595f5970-7414-4faa-a26f-ff8926f83a0a)


egrep 's{1,2}' newfile
## OUTPUT 
![27](https://github.com/VPOOJAASREE/OS-Linux-commands-Shell-script/assets/155145525/009a0afa-0adc-4615-a466-b6231f23d2c6)



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
![28](https://github.com/VPOOJAASREE/OS-Linux-commands-Shell-script/assets/155145525/79762d67-4f65-468d-afa8-c577467383e3)


sed -n -e '$p' file23
## OUTPUT
![29](https://github.com/VPOOJAASREE/OS-Linux-commands-Shell-script/assets/155145525/a6d2e835-e398-4823-a7fa-5445ccb5a901)


sed  -e 's/Ram/Sita/' file23
## OUTPUT
![30](https://github.com/VPOOJAASREE/OS-Linux-commands-Shell-script/assets/155145525/6d6183f8-f583-483c-ae86-b6d82286019a)


sed  -e '2s/Ram/Sita/' file23
## OUTPUT
![31](https://github.com/VPOOJAASREE/OS-Linux-commands-Shell-script/assets/155145525/163c2c42-13de-4228-809a-033d0928e10f)


sed  '/tom/s/5000/6000/' file23
## OUTPUT
![32](https://github.com/VPOOJAASREE/OS-Linux-commands-Shell-script/assets/155145525/b6a56c0b-bf64-417d-9e1c-4f5a93f358da)


sed -n -e '1,5p' file23
## OUTPUT
![33](https://github.com/VPOOJAASREE/OS-Linux-commands-Shell-script/assets/155145525/7ce4349c-40af-4e70-99cc-fb9377fc9810)


sed -n -e '2,/Joe/p' file23
## OUTPUT
![34](https://github.com/VPOOJAASREE/OS-Linux-commands-Shell-script/assets/155145525/d0b928de-6ef6-4c87-b211-767699188e94)


sed -n -e '/tom/,/Joe/p' file23
## OUTPUT
![35](https://github.com/VPOOJAASREE/OS-Linux-commands-Shell-script/assets/155145525/f9a1cc98-3868-4abf-9e83-00afb06ee3f5)


seq 10 
## OUTPUT
![36](https://github.com/VPOOJAASREE/OS-Linux-commands-Shell-script/assets/155145525/c21392f5-80dd-43c0-be44-d9a918c05b7a)


seq 10 | sed -n '4,6p'
## OUTPUT
![37](https://github.com/VPOOJAASREE/OS-Linux-commands-Shell-script/assets/155145525/1caa1a54-e28f-4631-9d4e-718f6c06b617)


seq 10 | sed -n '2,~4p'
## OUTPUT
![38](https://github.com/VPOOJAASREE/OS-Linux-commands-Shell-script/assets/155145525/c621dd52-1e88-4a48-a82a-9a94ac209bb8)


seq 3 | sed '2a hello'
## OUTPUT
![39](https://github.com/VPOOJAASREE/OS-Linux-commands-Shell-script/assets/155145525/9b419ee3-a53b-4fa6-849e-7eaf4100891a)


seq 2 | sed '2i hello'
## OUTPUT
![40](https://github.com/VPOOJAASREE/OS-Linux-commands-Shell-script/assets/155145525/6f59e417-bee1-4849-a4e6-90800f95590a)


seq 10 | sed '2,9c hello'
## OUTPUT
![41](https://github.com/VPOOJAASREE/OS-Linux-commands-Shell-script/assets/155145525/07615a7f-e479-4842-99f9-449cd86a7d5a)


sed -n '2,4{s/^/$/;p}' file23
## OUTPUT
![42](https://github.com/VPOOJAASREE/OS-Linux-commands-Shell-script/assets/155145525/b8dc42e1-b0a7-4dd3-92ee-8bf36276ca13)


sed -n '2,4{s/$/*/;p}' file23
## OUTPUT
![43](https://github.com/VPOOJAASREE/OS-Linux-commands-Shell-script/assets/155145525/7ddba572-36fe-4051-90b2-94fbec1b00c0)


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
![44](https://github.com/VPOOJAASREE/OS-Linux-commands-Shell-script/assets/155145525/85e9d712-ed60-4499-a832-924a5af54927)


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
![45](https://github.com/VPOOJAASREE/OS-Linux-commands-Shell-script/assets/155145525/ec089e79-b3d0-450b-a8c3-8ea0bd949e32)


#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT
 ![46](https://github.com/VPOOJAASREE/OS-Linux-commands-Shell-script/assets/155145525/01751d74-7e92-4c93-8ef4-1ed9e5b22a48)


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
 ![47](https://github.com/VPOOJAASREE/OS-Linux-commands-Shell-script/assets/155145525/8c901d20-9fc2-4e8e-997a-4820710757af)


cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT
![48](https://github.com/VPOOJAASREE/OS-Linux-commands-Shell-script/assets/155145525/57adfa5f-0ddd-4974-9232-fafef1cabf70)



#Backup commands
tar -cvf backup.tar *
## OUTPUT
![Screenshot 2024-03-29 122717](https://github.com/VPOOJAASREE/OS-Linux-commands-Shell-script/assets/155145525/320c7704-7e43-464b-b8ca-ed3f1add62c4)


mkdir backupdir
 
mv backup.tar backupdir
 
tar -tvf backup.tar
## OUTPUT
![Screenshot 2024-03-29 122733](https://github.com/VPOOJAASREE/OS-Linux-commands-Shell-script/assets/155145525/5fdfcefa-20c8-4cba-957c-81f2f167da9f)


tar -xvf backup.tar
## OUTPUT
![Screenshot 2024-03-29 122751](https://github.com/VPOOJAASREE/OS-Linux-commands-Shell-script/assets/155145525/1395c7e0-5da7-4e28-98a5-01fc08709a80)


gzip backup.tar

ls .gz
## OUTPUT
![Screenshot 2024-03-29 122805](https://github.com/VPOOJAASREE/OS-Linux-commands-Shell-script/assets/155145525/badbe015-26e9-41cd-8540-9af4cfd5d763)

 
gunzip backup.tar.gz
## OUTPUT
```
backup.tar
```

 
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

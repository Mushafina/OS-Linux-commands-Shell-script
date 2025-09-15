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
<img width="290" height="153" alt="image" src="https://github.com/user-attachments/assets/3b8e387e-d006-4899-b064-623ea4c9442b" />


cat < file2
## OUTPUT
<img width="333" height="179" alt="image" src="https://github.com/user-attachments/assets/30fba26f-95f9-4806-b8d7-efe7357f4e69" />


# Comparing Files
cmp file1 file2
## OUTPUT
<img width="377" height="79" alt="image" src="https://github.com/user-attachments/assets/abe8bfcb-1f9c-41d2-bb6a-a6f3542df901" />

comm file1 file2
 ## OUTPUT
<img width="441" height="328" alt="image" src="https://github.com/user-attachments/assets/4e45fe32-f1a7-4427-b4c1-e2e984c5f092" />

 
diff file1 file2
## OUTPUT
<img width="458" height="302" alt="image" src="https://github.com/user-attachments/assets/d00f52bb-9c3c-4362-b62f-2c5425b699f0" />


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

<img width="316" height="103" alt="image" src="https://github.com/user-attachments/assets/40636cbc-203f-4037-8477-355172ab82f1" />



cut -d "|" -f 1 file22
## OUTPUT
<img width="320" height="130" alt="image" src="https://github.com/user-attachments/assets/b08857cf-f8ca-4839-81d5-4a0295eba233" />



cut -d "|" -f 2 file22
## OUTPUT
<img width="363" height="131" alt="image" src="https://github.com/user-attachments/assets/09f71301-0582-4cbd-95c2-22002ff1534d" />


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
<img width="290" height="76" alt="image" src="https://github.com/user-attachments/assets/792789e1-6162-4639-aee4-252bda2c2f8b" />



grep hello newfile 
## OUTPUT
<img width="396" height="77" alt="image" src="https://github.com/user-attachments/assets/4674134e-952e-475e-81a5-3bce6a1a0861" />




grep -v hello newfile 
## OUTPUT
<img width="349" height="81" alt="image" src="https://github.com/user-attachments/assets/d8c54b30-88c8-4368-9c87-f40f6d2772b5" />



cat newfile | grep -i "hello"
## OUTPUT
<img width="386" height="101" alt="image" src="https://github.com/user-attachments/assets/c3441c30-30ab-47c5-8876-9a560114f85c" />




cat newfile | grep -i -c "hello"
## OUTPUT
<img width="499" height="73" alt="image" src="https://github.com/user-attachments/assets/5bb878d0-e16c-4872-9426-9845335a60bb" />




grep -R ubuntu /etc
## OUTPUT
<img width="596" height="484" alt="image" src="https://github.com/user-attachments/assets/1588f62a-bca4-46ff-a754-db883305549b" />



grep -w -n world newfile   
## OUTPUT
<img width="373" height="98" alt="image" src="https://github.com/user-attachments/assets/3755001a-8ea8-436c-b29a-578299aae463" />


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
<img width="403" height="103" alt="image" src="https://github.com/user-attachments/assets/4d740e46-bac9-4ca0-a678-cd7ad8cd42f9" />



egrep -w '(H|h)ello' newfile 
## OUTPUT
<img width="382" height="107" alt="image" src="https://github.com/user-attachments/assets/34dc4869-3944-4f8d-a7aa-4bfbd387076e" />



egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT
<img width="415" height="101" alt="image" src="https://github.com/user-attachments/assets/a92a0dc3-bea1-4c84-a434-7074ada182c9" />




egrep '(^hello)' newfile 
## OUTPUT
<img width="382" height="76" alt="image" src="https://github.com/user-attachments/assets/f5e1352a-0447-411a-8749-cb70be5ce225" />



egrep '(world$)' newfile 
## OUTPUT
<img width="446" height="229" alt="image" src="https://github.com/user-attachments/assets/1dde8c76-53d0-405b-80e8-e8d94a11b287" />



egrep '(World$)' newfile 
## OUTPUT
<img width="446" height="229" alt="image" src="https://github.com/user-attachments/assets/ad9b179b-1ca6-4011-9271-cc78b722278c" />


egrep '((W|w)orld$)' newfile 
## OUTPUT
<img width="446" height="229" alt="image" src="https://github.com/user-attachments/assets/0a424871-5795-478b-9bf0-03129c32351f" />



egrep '[1-9]' newfile 
## OUTPUT
<img width="388" height="81" alt="image" src="https://github.com/user-attachments/assets/112a3122-8262-4b26-ba7c-0b6d433aaba4" />



egrep 'Linux.*world' newfile 
## OUTPUT
<img width="453" height="81" alt="image" src="https://github.com/user-attachments/assets/9843ed17-65be-4160-a59c-5460923d0020" />


egrep 'Linux.*World' newfile 
## OUTPUT
<img width="453" height="81" alt="image" src="https://github.com/user-attachments/assets/05980bc6-9850-4a67-8587-9c3a29cf3401" />


egrep l{2} newfile
## OUTPUT
<img width="321" height="106" alt="image" src="https://github.com/user-attachments/assets/4dbabd06-4b44-4d51-9e48-562c64391616" />



egrep 's{1,2}' newfile
## OUTPUT 
<img width="365" height="132" alt="image" src="https://github.com/user-attachments/assets/38528c4f-17dd-413a-8d6e-6441a90c4d4a" />


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
<img width="333" height="79" alt="image" src="https://github.com/user-attachments/assets/d068ddd5-3309-401e-9483-a21954d7d38d" />



sed -n -e '$p' file23
## OUTPUT
<img width="360" height="76" alt="image" src="https://github.com/user-attachments/assets/fc5fa8e6-5de2-41f8-ad67-a5e15ed01ff5" />



sed  -e 's/Ram/Sita/' file23
## OUTPUT
<img width="425" height="254" alt="image" src="https://github.com/user-attachments/assets/1e5ada66-3240-412f-ba29-c24cebf157a8" />



sed  -e '2s/Ram/Sita/' file23
## OUTPUT
<img width="458" height="249" alt="image" src="https://github.com/user-attachments/assets/b5748f4e-6b57-4881-8965-48505e71def1" />



sed  '/tom/s/5000/6000/' file23
## OUTPUT
<img width="514" height="253" alt="image" src="https://github.com/user-attachments/assets/c28c83e7-8972-41e3-b813-794ac4e3c6bf" />



sed -n -e '1,5p' file23
## OUTPUT
<img width="391" height="177" alt="image" src="https://github.com/user-attachments/assets/c2e619f2-128d-409d-816a-7911a4256266" />



sed -n -e '2,/Joe/p' file23
## OUTPUT
<img width="463" height="130" alt="image" src="https://github.com/user-attachments/assets/229ef4d0-354c-41e5-bd87-aaf0cbc141cb" />




sed -n -e '/tom/,/Joe/p' file23
## OUTPUT
<img width="434" height="105" alt="image" src="https://github.com/user-attachments/assets/5730b524-7efa-4a26-898e-efcae89799e8" />



seq 10 
## OUTPUT
<img width="318" height="306" alt="image" src="https://github.com/user-attachments/assets/9e3e6657-0dc2-45c2-8cf6-9896a1bf7c06" />



seq 10 | sed -n '4,6p'
## OUTPUT
<img width="349" height="131" alt="image" src="https://github.com/user-attachments/assets/46cf3504-d3e3-42e1-94fe-46937510389b" />



seq 10 | sed -n '2,~4p'
## OUTPUT
<img width="328" height="128" alt="image" src="https://github.com/user-attachments/assets/07916011-f8eb-4292-81f2-fb62626ae4b1" />



seq 3 | sed '2a hello'
## OUTPUT
<img width="332" height="157" alt="image" src="https://github.com/user-attachments/assets/fe1a231e-ebc0-4acb-9c5d-c022867b9152" />



seq 2 | sed '2i hello'
## OUTPUT
<img width="328" height="126" alt="image" src="https://github.com/user-attachments/assets/2bcb170a-9203-49e9-bbd1-03c506cdcb3d" />


seq 10 | sed '2,9c hello'
## OUTPUT
<img width="388" height="127" alt="image" src="https://github.com/user-attachments/assets/f6ce6e27-377a-40d2-97c4-09263a6a4ed1" />


sed -n '2,4{s/^/$/;p}' file23
## OUTPUT
<img width="434" height="127" alt="image" src="https://github.com/user-attachments/assets/0b654062-3357-48f1-b3cc-58ee2efb11ce" />



sed -n '2,4{s/$/*/;p}' file23
<img width="405" height="134" alt="image" src="https://github.com/user-attachments/assets/7e1814eb-244a-491d-a70c-7614e79e159a" />


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



#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT

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

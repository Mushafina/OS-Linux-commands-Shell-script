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
## OUTPUT
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
<img width="407" height="178" alt="image" src="https://github.com/user-attachments/assets/2b29c83b-80c6-40a9-8e89-f4e36797a013" />


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
<img width="359" height="180" alt="image" src="https://github.com/user-attachments/assets/82e1d7dc-5250-46b8-bcca-14a343bfebb4" />



#Using tr command

cat file23 | tr [:lower:] [:upper:]
## OUTPUT
<img width="456" height="256" alt="image" src="https://github.com/user-attachments/assets/8d732a09-6de8-4c55-ac4b-eaf1771d6a08" />

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
<img width="385" height="123" alt="image" src="https://github.com/user-attachments/assets/3b290cfa-9212-4640-9091-8870a6bdcd35" />


 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT
<img width="523" height="133" alt="image" src="https://github.com/user-attachments/assets/f813f7af-e102-4f89-8e75-bbb88f84df96" />



#Backup commands
tar -cvf backup.tar *
## OUTPUT
<img width="332" height="434" alt="image" src="https://github.com/user-attachments/assets/93730744-d713-4142-b37d-127e95ab969c" />


mkdir backupdir
 
mv backup.tar backupdir

cd backupdir
 
tar -tvf backup.tar
## OUTPUT
<img width="691" height="608" alt="image" src="https://github.com/user-attachments/assets/df0a951b-2f55-43fb-8b41-24258f1131e6" />


tar -xvf backup.tar
## OUTPUT
<img width="432" height="426" alt="image" src="https://github.com/user-attachments/assets/39743891-955c-427f-a49a-0d7e1862f22a" />

gzip backup.tar

ls .gz
## OUTPUT
<img width="322" height="83" alt="image" src="https://github.com/user-attachments/assets/e61fc360-d21b-4557-9dea-99c1903b5ca2" />


gunzip backup.tar.gz
## OUTPUT

<img width="840" height="153" alt="image" src="https://github.com/user-attachments/assets/e3d3273d-728e-4235-8348-5eb93624fa29" />

 
# Shell Script
```
echo '#!/bin/sh' > my-script.sh
echo 'echo Hello World‘; exit 0 >> my-script.sh
```
chmod 755 my-script.sh
./my-script.sh
## OUTPUT
<img width="625" height="308" alt="image" src="https://github.com/user-attachments/assets/a9abd609-0e2b-43cb-8a67-7d687b8bf91b" />

 
cat << stop > herecheck.txt
```
hello in this world
i cant stop
for this non stop movement
stop
```

cat herecheck.txt
## OUTPUT
<img width="420" height="281" alt="image" src="https://github.com/user-attachments/assets/4d9b07d8-f90e-466e-a3ce-7ecb8969c4a5" />


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
<img width="641" height="454" alt="image" src="https://github.com/user-attachments/assets/022bb770-54be-423f-a03d-37f134268182" />

 
ls file1
## OUTPUT
<img width="304" height="80" alt="image" src="https://github.com/user-attachments/assets/bc22393b-8bd0-4c68-826d-7b70715091a5" />

echo $?
## OUTPUT 
<img width="306" height="77" alt="image" src="https://github.com/user-attachments/assets/947bf1ce-bbf8-426b-b31b-1f5f98adbd21" />

./one
bash: ./one: Permission denied
 
echo $?
## OUTPUT 
<img width="306" height="77" alt="image" src="https://github.com/user-attachments/assets/1eeb734d-56d7-41bc-b4b2-8c08ab974f17" />

abcd
 
echo $?
 ## OUTPUT
<img width="306" height="77" alt="image" src="https://github.com/user-attachments/assets/5734d5ff-8b66-4ab8-a3b7-985158871801" />


 
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
<img width="439" height="276" alt="image" src="https://github.com/user-attachments/assets/a7c9376c-ed44-45dd-83e8-99d658c646c8" />



chmod 755 strcomp.sh
 
./strcomp.sh 
## OUTPUT
<img width="652" height="151" alt="image" src="https://github.com/user-attachments/assets/2ed2f85e-0996-4adb-b6db-2bceb18ceb23" />


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
<img width="634" height="220" alt="image" src="https://github.com/user-attachments/assets/e0a52bc2-6c9c-4f2b-8d53-c246d3f384ac" />

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
<img width="558" height="476" alt="image" src="https://github.com/user-attachments/assets/5bd49a1b-75db-4af6-a178-c80289ce3bb9" />



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
<img width="664" height="182" alt="image" src="https://github.com/user-attachments/assets/690d4175-a79e-4929-8ab6-855704ca0b00" />


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
<img width="702" height="207" alt="image" src="https://github.com/user-attachments/assets/3bf40078-612e-4e25-91ea-0a6b234d25c8" />

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
<img width="725" height="151" alt="image" src="https://github.com/user-attachments/assets/abcecf7a-acc2-40e2-956d-cccf2726cc6d" />


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
<img width="696" height="161" alt="image" src="https://github.com/user-attachments/assets/8b796204-476e-401d-b581-cf55943bb505" />

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
<img width="416" height="128" alt="image" src="https://github.com/user-attachments/assets/3321cd90-6d65-44f7-9255-7d7ce43671ec" />

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

## OUTPUT
<img width="376" height="353" alt="image" src="https://github.com/user-attachments/assets/9cbf7035-ccd0-40e9-aea4-6d31aa6f4a9f" />

 
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
<img width="589" height="227" alt="image" src="https://github.com/user-attachments/assets/81c84333-595f-497d-9a40-b9cda70bb053" />

 
 
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
<img width="662" height="308" alt="image" src="https://github.com/user-attachments/assets/373671b8-68a3-4012-8151-6821cfcba03c" />


 
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
<img width="679" height="233" alt="image" src="https://github.com/user-attachments/assets/4073bb13-1f66-4cdc-b920-e85415fe4517" />

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

## OUTPUT 
<img width="682" height="306" alt="image" src="https://github.com/user-attachments/assets/032e514f-43df-4b40-83d6-516d855c8e32" />


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
<img width="680" height="85" alt="image" src="https://github.com/user-attachments/assets/c553002c-db1d-43ad-965d-c5e5cfd6fa9d" />


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
<img width="503" height="279" alt="image" src="https://github.com/user-attachments/assets/387de63b-855c-4b41-9ae9-e1fbfa7b3198" />


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
<img width="550" height="304" alt="image" src="https://github.com/user-attachments/assets/3111a2e9-f774-4a75-af6b-cc02200c9e03" />


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
<img width="465" height="407" alt="image" src="https://github.com/user-attachments/assets/c97e9dab-13d2-4f7e-be08-0385532c42f0" />

 
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
$ chmod 755 forbreak.sh
 
$ ./forbreak.sh 

## OUTPUT 
<img width="726" height="185" alt="image" src="https://github.com/user-attachments/assets/261818db-6327-426f-a8a7-1c957f245232" />

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
<img width="742" height="232" alt="image" src="https://github.com/user-attachments/assets/a26f8089-f76e-4081-b289-769022ab5221" />

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
<img width="488" height="156" alt="image" src="https://github.com/user-attachments/assets/342c4b67-83e1-4eae-9516-a68d1ee07892" />


 cat exread1.sh
```bash
#!/bin/bash
# testing the read command
read -p "Enter your name: " name
echo "Hello $name, welcome to my program. “
``` 
$ chmod 755 exread1.sh 

$ ./exread1.sh 

 ## OUTPUT
<img width="454" height="155" alt="image" src="https://github.com/user-attachments/assets/f6fe98ad-4dbe-4b3b-b7de-910a575fa254" />

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
 
<img width="385" height="198" alt="image" src="https://github.com/user-attachments/assets/3a84e6db-2184-4e64-ac4c-7f75d6aa64db" />

 
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

<img width="360" height="181" alt="image" src="https://github.com/user-attachments/assets/9b897422-0898-4ea7-ad67-2dd71ecbc7d4" />

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

<img width="383" height="184" alt="image" src="https://github.com/user-attachments/assets/26ba670a-294a-4e5b-ac17-bb95f3dfece6" />

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
 
 <img width="490" height="407" alt="image" src="https://github.com/user-attachments/assets/18b1c496-d496-42b2-9bb6-b47d63559c72" />

 
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
<img width="570" height="377" alt="image" src="https://github.com/user-attachments/assets/26190180-5ae6-4bae-b520-98b0ded6123e" />

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
<img width="393" height="132" alt="image" src="https://github.com/user-attachments/assets/c792542f-f58f-47b7-9766-d2be9ee0739e" />

# RESULT:
The Commands are executed successfully.

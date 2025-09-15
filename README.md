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
<img width="574" height="266" alt="Screenshot at 2025-08-12 12-24-00" src="https://github.com/user-attachments/assets/7ceb73f5-b919-4632-a3c1-e735151f18de" />

cat < file2
## Output
<img width="489" height="345" alt="Screenshot at 2025-08-12 12-26-56" src="https://github.com/user-attachments/assets/32949c37-fcb0-43ee-a84a-4f774d1ec911" />

# Comparing Files
cmp file1 file2
## OUTPUT
<img width="619" height="125" alt="OUTPUT 1" src="https://github.com/user-attachments/assets/90fd1b0c-9315-481f-a106-41c380dd8652" />

 
comm file1 file2
 ## OUTPUT
<img width="649" height="433" alt="4" src="https://github.com/user-attachments/assets/7b2424ec-874e-48a5-90d6-9b66bf610ff5" />


 
diff file1 file2
## OUTPUT
<img width="582" height="541" alt="5" src="https://github.com/user-attachments/assets/4b29962f-98ba-4947-8e59-53afbf9231ab" />


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
<img width="540" height="169" alt="6" src="https://github.com/user-attachments/assets/a23217d5-dfcb-4db6-ae56-ed5f8537e633" />

cut -d "|" -f 1 file22
## OUTPUT
<img width="365" height="179" alt="123" src="https://github.com/user-attachments/assets/c5a25eaa-3a1a-4d9b-b382-c9c2ceaba6b7" />



cut -d "|" -f 2 file22
## OUTPUT
<img width="536" height="150" alt="7" src="https://github.com/user-attachments/assets/97112110-77dd-49f7-9484-1b2ea78567ba" />


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
<img width="480" height="139" alt="8" src="https://github.com/user-attachments/assets/d6a09c82-2254-4ec2-a76b-9a901e2b887c" />



grep hello newfile 
## OUTPUT

<img width="313" height="140" alt="1113" src="https://github.com/user-attachments/assets/bd634123-ef2b-4b6e-bec7-26ed3b96b247" />




grep -v hello newfile 
## OUTPUT
<img width="295" height="75" alt="10" src="https://github.com/user-attachments/assets/66ed2563-2b1d-4a80-9834-14a8f675518c" />



cat newfile | grep -i "hello"
## OUTPUT
<img width="374" height="150" alt="11" src="https://github.com/user-attachments/assets/145f27ff-ca6f-42b9-af99-7ce6de1668f4" />




cat newfile | grep -i -c "hello"
## OUTPUT
<img width="401" height="139" alt="12" src="https://github.com/user-attachments/assets/75b546db-e0bf-472c-afa8-c21443919d2c" />




grep -R ubuntu /etc
## OUTPUT
<img width="793" height="555" alt="1" src="https://github.com/user-attachments/assets/a231d252-6e6f-4e16-afbb-68876dd5a96f" />




grep -w -n world newfile   
## OUTPUT

<img width="393" height="152" alt="2" src="https://github.com/user-attachments/assets/3206ed3a-162d-4052-ab41-129eee3cac76" />


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
<img width="402" height="185" alt="4" src="https://github.com/user-attachments/assets/c39a8d92-3120-4336-ae26-22392ed8594b" />



egrep -w '(H|h)ello' newfile 
## OUTPUT

<img width="427" height="150" alt="5" src="https://github.com/user-attachments/assets/7d1128fb-3198-412b-8e41-3e9cee5e2e60" />


egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT

![6](https://github.com/user-attachments/assets/237fcc99-5ed7-45ac-9a7c-753eda716926)



egrep '(^hello)' newfile 
## OUTPUT
![1](https://github.com/user-attachments/assets/578a98d9-11e6-4159-9a19-f81eeb68994b)



egrep '(world$)' newfile 
## OUTPUT
<img width="430" height="140" alt="2" src="https://github.com/user-attachments/assets/416182c6-cc7f-4b0e-9f94-6807499284bb" />



egrep '(World$)' newfile 
## OUTPUT
<img width="507" height="126" alt="3" src="https://github.com/user-attachments/assets/4388bf65-c5a7-4e4b-a385-635a130f0e7e" />


egrep '((W|w)orld$)' newfile 
## OUTPUT
<img width="589" height="174" alt="5" src="https://github.com/user-attachments/assets/8ffb2827-62f1-46c0-8d7e-d366d6f76cc8" />



egrep '[1-9]' newfile 
## OUTPUT
<img width="472" height="125" alt="7" src="https://github.com/user-attachments/assets/b5ed7aaf-06f0-4ecd-9c8d-c1659083bf9c" />



egrep 'Linux.*world' newfile 
## OUTPUT
<img width="456" height="127" alt="1" src="https://github.com/user-attachments/assets/5ca406be-09af-458d-817d-df6cd3ed96d1" />


egrep 'Linux.*World' newfile 
## OUTPUT

<img width="447" height="114" alt="2" src="https://github.com/user-attachments/assets/5c9b4b52-233d-4832-823b-9e0c7d37b766" />

egrep l{2} newfile
## OUTPUT
<img width="398" height="116" alt="3" src="https://github.com/user-attachments/assets/2d365a63-fa45-4bfd-ba9d-d05a966eb3b4" />



egrep 's{1,2}' newfile
## OUTPUT 
<img width="422" height="175" alt="5" src="https://github.com/user-attachments/assets/0fc486c4-25b3-4afa-b126-d73d29292ffb" />


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
<img width="418" height="121" alt="1" src="https://github.com/user-attachments/assets/aa1ea824-21ef-4d62-8335-44a832aa7f51" />



sed -n -e '$p' file23
## OUTPUT

<img width="430" height="124" alt="33" src="https://github.com/user-attachments/assets/558e2f45-cdc6-4c3a-aff6-31696fadee8a" />


sed  -e 's/Ram/Sita/' file23
## OUTPUT

<img width="555" height="121" alt="2" src="https://github.com/user-attachments/assets/07a18839-44c1-4bfd-9aea-5e8ff6e54a77" />


sed  -e '2s/Ram/Sita/' file23
## OUTPUT
<img width="557" height="250" alt="33333" src="https://github.com/user-attachments/assets/40304491-a122-42f2-b5c1-1f95507cb2de" />



sed  '/tom/s/5000/6000/' file23
## OUTPUT
<img width="423" height="260" alt="32" src="https://github.com/user-attachments/assets/6ef31d47-4d9c-4a9d-b1cf-788b9a6d6003" />



sed -n -e '1,5p' file23
## OUTPUT
<img width="434" height="187" alt="355" src="https://github.com/user-attachments/assets/d0776a56-9ebb-4ae8-a080-d8ddee795c49" />



sed -n -e '2,/Joe/p' file23
## OUTPUT
<img width="507" height="125" alt="2" src="https://github.com/user-attachments/assets/9f6893e8-01cc-434a-80bf-0922e7d7cf21" />


sed -n -e '/tom/,/Joe/p' file23
## OUTPUT
<img width="440" height="281" alt="111" src="https://github.com/user-attachments/assets/a5e3ada6-3d93-4007-8af7-a7bba528910d" />



seq 10 
## OUTPUT
<img width="630" height="359" alt="10" src="https://github.com/user-attachments/assets/fdee7110-b7cd-4ef4-a481-4fa856184806" />



seq 10 | sed -n '4,6p'
## OUTPUT
<img width="407" height="183" alt="11" src="https://github.com/user-attachments/assets/3a2adfde-6902-4d3f-8922-367b6046e5e8" />



seq 10 | sed -n '2,~4p'
## OUTPUT

<img width="478" height="180" alt="174" src="https://github.com/user-attachments/assets/2bd5c886-488e-458b-ae78-2a6a98ffc73e" />


seq 3 | sed '2a hello'
## OUTPUT
<img width="510" height="201" alt="369" src="https://github.com/user-attachments/assets/4e8d51a1-4ee2-47c2-808a-816bdd59884c" />



seq 2 | sed '2i hello'
## OUTPUT
<img width="421" height="194" alt="4" src="https://github.com/user-attachments/assets/c4ae87ae-f81a-4d47-9c8d-00f3415cbe1b" />


seq 10 | sed '2,9c hello'
## OUTPUT
<img width="468" height="170" alt="06" src="https://github.com/user-attachments/assets/7c63f60d-99b7-402d-a4bb-09ea9453358c" />


sed -n '2,4{s/^/$/;p}' file23
## OUTPUT
<img width="439" height="154" alt="png" src="https://github.com/user-attachments/assets/dcef4d6d-32db-4287-bad8-aa4675ccd42c" />



sed -n '2,4{s/$/*/;p}' file23

<img width="466" height="155" alt="693" src="https://github.com/user-attachments/assets/d8c23f75-8b26-4749-96da-ceff00f375d5" />

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
<img width="512" height="238" alt="12" src="https://github.com/user-attachments/assets/7bbc0366-64b0-4410-b8f2-e0f84347a29a" />


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
<img width="461" height="219" alt="456" src="https://github.com/user-attachments/assets/c202d8f0-8f7b-43cc-a146-3cc7d4f59339" />



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

<img width="345" height="135" alt="1" src="https://github.com/user-attachments/assets/461262b9-87a1-4002-b4c4-7579d8dbb811" />

 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT
<img width="629" height="71" alt="2" src="https://github.com/user-attachments/assets/83f8fd55-b363-4ba2-87e9-8a479739e306" />



#Backup commands
tar -cvf backup.tar *
## OUTPUT
<img width="419" height="234" alt="4" src="https://github.com/user-attachments/assets/d7301bb0-5e2d-4591-982d-4a7ff2ffb84c" />


mkdir backupdir
 
mv backup.tar backupdir

cd backupdir
 
tar -tvf backup.tar
## OUTPUT
<img width="405" height="61" alt="5" src="https://github.com/user-attachments/assets/1c4fbcf9-8e41-4aed-9004-470a021f71dd" />


tar -xvf backup.tar
## OUTPUT
<img width="419" height="234" alt="4" src="https://github.com/user-attachments/assets/6f61639a-05e1-40df-ab25-4b103a9bd9ca" />

gzip backup.tar

ls .gz
 
gunzip backup.tar.gz

 
# Shell Script
```
echo '#!/bin/sh' > my-script.sh
echo 'echo Hello World‘; exit 0 >> my-script.sh
```
chmod 755 my-script.sh
./my-script.sh
## OUTPUT
<img width="406" height="208" alt="7" src="https://github.com/user-attachments/assets/ce2f7766-d027-45c5-979e-dd3393afcd9f" />

 
cat << stop > herecheck.txt
```
hello in this world
i cant stop
for this non stop movement
stop
```

cat herecheck.txt
## OUTPUT
<img width="346" height="170" alt="rew" src="https://github.com/user-attachments/assets/f03298a1-0724-4817-8ef3-19b1934d7aef" />


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
<img width="360" height="93" alt="1" src="https://github.com/user-attachments/assets/3c2abeb4-e1b7-4612-9c6c-340b7bd9de77" />

echo $?

## OUTPUT 
<img width="357" height="75" alt="2" src="https://github.com/user-attachments/assets/f274f2c9-ef10-4233-8cc3-365312bd8e47" />
./one
bash: ./one: Permission denied
 
echo $?
## OUTPUT 
 <img width="357" height="75" alt="2" src="https://github.com/user-attachments/assets/d2275edc-a779-4840-b187-face7dd63a5d" />

abcd
 
echo $?
 ## OUTPUT
<img width="365" height="96" alt="3" src="https://github.com/user-attachments/assets/9082f9be-6bd2-4852-bf59-bec5ca82b2c6" />


 
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
<img width="451" height="300" alt="4" src="https://github.com/user-attachments/assets/f1b5d17b-58ad-4155-8ea2-6c705ad3ff3d" />



chmod 755 strcomp.sh
 
./strcomp.sh 
## OUTPUT
<img width="647" height="167" alt="5" src="https://github.com/user-attachments/assets/83ed608d-57cd-4330-8d9b-3c1799189c4f" />


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
<img width="624" height="224" alt="7" src="https://github.com/user-attachments/assets/af9837c2-a0e7-4bc6-ae4e-4e29b472e985" />



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
<img width="180" height="242" alt="258" src="https://github.com/user-attachments/assets/5dea7af8-a1f1-4d09-a9d1-970f7a8ba79c" />


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
<img width="547" height="192" alt="image" src="https://github.com/user-attachments/assets/90ed3e7b-eb75-4ab7-9e42-b0dc1864be0e" />


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

<img width="333" height="273" alt="image" src="https://github.com/user-attachments/assets/14477c4b-8637-497b-a127-5972401623f7" />

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
<img width="887" height="178" alt="image" src="https://github.com/user-attachments/assets/4176ba96-6f21-48dd-acb3-ca9716521c74" />

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
 <img width="812" height="284" alt="image" src="https://github.com/user-attachments/assets/054d5bbc-d06e-4fae-91b0-093a7bb4b8ff" />

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
<img width="1219" height="124" alt="image" src="https://github.com/user-attachments/assets/55724fc3-59b7-4f0d-ac8d-63301ecd210b" />


 cat exread1.sh
```bash
#!/bin/bash
# testing the read command
read -p "Enter your name: " name
echo "Hello $name, welcome to my program. “
``` 
$ chmod 755 exread1.sh 

## OUTPUT


<img width="1219" height="124" alt="image" src="https://github.com/user-attachments/assets/3ecad28d-549a-4b36-991f-de1f46d58e61" />

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
<img width="762" height="57" alt="image" src="https://github.com/user-attachments/assets/7120475a-60b4-4d7a-a57b-f8ca199cc2af" />

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
<img width="656" height="160" alt="image" src="https://github.com/user-attachments/assets/26eaf9c5-38d2-49a3-b478-898acfd7cec2" />

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
<img width="656" height="160" alt="image" src="https://github.com/user-attachments/assets/104c0f63-e996-49c1-9249-5ab0811cf301" />

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
<img width="656" height="160" alt="image" src="https://github.com/user-attachments/assets/14989410-ebba-4c74-b081-c36a070e7bd1" />

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
<img width="724" height="694" alt="image" src="https://github.com/user-attachments/assets/46a836b0-8635-4896-a04d-5fe8541efae3" />

```
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
Enter the number 121 Number is palindrome Enter the number 69 Number is NOT palindrome
# RESULT:
The Commands are executed successfully.


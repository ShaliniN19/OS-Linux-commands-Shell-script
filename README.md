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
![Screenshot from 2025-04-23 20-59-28](https://github.com/user-attachments/assets/9cab95d0-1739-488c-9bf8-dc80059c30cf)



cat < file2
## OUTPUT
![Screenshot from 2025-04-23 20-59-53](https://github.com/user-attachments/assets/1d3687a8-dd77-48b8-a3a0-2430060f142e)


# Comparing Files
cmp file1 file2
## OUTPUT
 ![Screenshot from 2025-04-23 21-00-22](https://github.com/user-attachments/assets/1321b2aa-55d5-4232-a0f0-2ba6e3257a43)

comm file1 file2
 ## OUTPUT
![Screenshot from 2025-04-23 21-01-22](https://github.com/user-attachments/assets/4dc53faf-3a25-4b39-8167-008aee17fb71)

 
diff file1 file2
## OUTPUT
![Screenshot from 2025-04-23 21-02-07](https://github.com/user-attachments/assets/96cd2603-036c-4ef6-bee6-29fbcbb81b4f)


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

![Screenshot from 2025-04-23 21-04-03](https://github.com/user-attachments/assets/622b60d7-b68e-4534-b248-5addeac1b99c)



cut -d "|" -f 1 file22
## OUTPUT
![Screenshot from 2025-04-23 21-04-54](https://github.com/user-attachments/assets/617ba348-7516-437a-911b-76954d81367d)



cut -d "|" -f 2 file22
## OUTPUT
![Screenshot from 2025-04-23 21-05-26](https://github.com/user-attachments/assets/e58a1df5-32b2-4106-8d0b-41b2367a5094)


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

![Screenshot from 2025-04-23 21-07-35](https://github.com/user-attachments/assets/8307256f-4520-4e3a-ad31-1533e1d128e4)


grep hello newfile 
## OUTPUT

![Screenshot from 2025-04-23 21-07-53](https://github.com/user-attachments/assets/d8f91b38-19b7-4deb-bc9c-50eef5a6e6f4)



grep -v hello newfile 
## OUTPUT
![Screenshot from 2025-04-23 21-08-17](https://github.com/user-attachments/assets/baed0d88-7164-45de-828b-56d9ba3d8acf)



cat newfile | grep -i "hello"
## OUTPUT
![Screenshot from 2025-04-23 21-09-04](https://github.com/user-attachments/assets/5c5ffe1b-fc7f-46b0-abb4-84d96045d1fc)




cat newfile | grep -i -c "hello"
## OUTPUT

![Screenshot from 2025-04-23 21-09-57](https://github.com/user-attachments/assets/1840e229-ecd5-4d80-94b8-531521bdf41f)



grep -R ubuntu /etc
## OUTPUT
![Screenshot from 2025-04-23 21-14-22](https://github.com/user-attachments/assets/57944980-7c27-4fd0-9dbc-1aa46064f40a)



grep -w -n world newfile   
## OUTPUT
![Screenshot from 2025-04-23 21-15-35](https://github.com/user-attachments/assets/a0628088-ea24-4cb5-9409-220cc69fe44a)



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
![Screenshot from 2025-04-23 21-17-28](https://github.com/user-attachments/assets/ebc7bbf0-4474-49e1-88a9-cb4f9f81a7ab)




egrep -w '(H|h)ello' newfile 
## OUTPUT
![Screenshot from 2025-04-23 21-18-27](https://github.com/user-attachments/assets/22e26b36-087e-4054-8311-693baf1d7ce6)




egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT
![Screenshot from 2025-04-23 21-19-11](https://github.com/user-attachments/assets/1bf33801-b68d-4d4a-ade4-d23868eda936)




egrep '(^hello)' newfile 
## OUTPUT
![Screenshot from 2025-04-23 21-19-52](https://github.com/user-attachments/assets/1dc6b2ac-eb6d-42c5-821a-440c76aeda23)



egrep '(world$)' newfile 
## OUTPUT
![Screenshot from 2025-04-23 21-20-25](https://github.com/user-attachments/assets/399ae42c-48d1-4222-addf-723f7cb6c91e)



egrep '(World$)' newfile 
## OUTPUT
![Screenshot from 2025-04-23 21-20-53](https://github.com/user-attachments/assets/08e801a3-00de-46e1-8708-1a2f6639f708)


egrep '((W|w)orld$)' newfile 
## OUTPUT
![Screenshot from 2025-04-23 21-23-11](https://github.com/user-attachments/assets/15833c6a-0fa9-4112-bd80-7da9a84c7869)



egrep '[1-9]' newfile 
## OUTPUT
![Screenshot from 2025-04-23 21-24-00](https://github.com/user-attachments/assets/f9e52d25-c6ac-4711-98f5-204d67adacd9)



egrep 'Linux.*world' newfile 
## OUTPUT
![Screenshot from 2025-04-23 21-24-37](https://github.com/user-attachments/assets/a62730fa-d20c-4e92-9849-a77a12c9ec69)


egrep 'Linux.*World' newfile 
## OUTPUT
![Screenshot from 2025-04-23 21-24-53](https://github.com/user-attachments/assets/2832db5c-ff8c-4275-a2ae-fcf4da09bc0a)


egrep l{2} newfile
## OUTPUT
![Screenshot from 2025-04-23 21-25-34](https://github.com/user-attachments/assets/e9e42117-f7c7-4a30-859b-24cf965321fd)



egrep 's{1,2}' newfile
## OUTPUT 
![Screenshot from 2025-04-23 21-26-23](https://github.com/user-attachments/assets/036e3eef-2ed6-465c-bc8f-8eb8ace94fef)


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
![Screenshot from 2025-04-23 21-40-21](https://github.com/user-attachments/assets/9d7d829d-543b-4ff9-aeb8-f1ad8d1574d7)



sed -n -e '$p' file23
## OUTPUT
![Screenshot from 2025-04-23 21-40-43](https://github.com/user-attachments/assets/535225ed-fff6-4304-bbe1-f6bac9aa5926)



sed  -e 's/Ram/Sita/' file23
## OUTPUT
![Screenshot from 2025-04-23 21-41-30](https://github.com/user-attachments/assets/56aa6d55-20e4-46bc-8a26-732391a5461c)



sed  -e '2s/Ram/Sita/' file23
## OUTPUT
![Screenshot from 2025-04-23 21-42-03](https://github.com/user-attachments/assets/e42d64ad-6f05-4a37-9f46-ca8d7b3f9f0f)



sed  '/tom/s/5000/6000/' file23
## OUTPUT
![Screenshot from 2025-04-23 21-42-51](https://github.com/user-attachments/assets/7e3e147c-f1d5-458f-8d22-8de1e50bfbe2)



sed -n -e '1,5p' file23
## OUTPUT
![Screenshot from 2025-04-23 21-43-31](https://github.com/user-attachments/assets/8db4dcc6-faa2-4c4f-9cb1-f1ccccc478ae)



sed -n -e '2,/Joe/p' file23
## OUTPUT
![Screenshot from 2025-04-23 21-44-03](https://github.com/user-attachments/assets/2308b229-aaae-40cd-8526-5d4ea589bde6)




sed -n -e '/tom/,/Joe/p' file23
## OUTPUT

![Screenshot from 2025-04-23 21-44-43](https://github.com/user-attachments/assets/8d7021dc-d408-4fd4-86a0-9308817ff000)


seq 10 
## OUTPUT

![Screenshot from 2025-04-23 21-45-00](https://github.com/user-attachments/assets/5772f993-1515-4b9b-a3c8-dab193f546e1)


seq 10 | sed -n '4,6p'
## OUTPUT
![Screenshot from 2025-04-23 21-46-01](https://github.com/user-attachments/assets/b30e67ac-d1fb-42ef-9819-7452941f36cb)



seq 10 | sed -n '2,~4p'
## OUTPUT
![Screenshot from 2025-04-23 21-47-30](https://github.com/user-attachments/assets/a95efd32-bf61-46ed-8f37-e6446e95d723)



seq 3 | sed '2a hello'
## OUTPUT
![Screenshot from 2025-04-23 21-48-03](https://github.com/user-attachments/assets/59f19e83-7d00-402c-8adc-22bc53eeb892)



seq 2 | sed '2i hello'
## OUTPUT
![Screenshot from 2025-04-23 21-48-27](https://github.com/user-attachments/assets/0e8acacc-5f4f-4516-8490-42536fa5283b)


seq 10 | sed '2,9c hello'
## OUTPUT
![Screenshot from 2025-04-23 21-49-13](https://github.com/user-attachments/assets/29895c09-13db-45d6-9f6f-0affbdc3b9ad)


sed -n '2,4{s/^/$/;p}' file23
## OUTPUT
![Screenshot from 2025-04-23 21-50-29](https://github.com/user-attachments/assets/ca551685-ca08-4b9e-bfe8-5d51305ed5ed)

![Screenshot from 2025-04-23 21-51-08](https://github.com/user-attachments/assets/f5b70aa9-e723-45d5-adb7-8880a62eaf78)


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
![Screenshot from 2025-04-23 21-52-21](https://github.com/user-attachments/assets/32ba4d3f-7d2e-4397-8e8b-68246be55534)



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

![Screenshot from 2025-04-23 21-53-31](https://github.com/user-attachments/assets/876d724c-9a1e-4250-a0da-f304551f32f5)


#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT
![Screenshot from 2025-04-23 21-54-19](https://github.com/user-attachments/assets/3d64cc1e-8686-4fd7-90cb-88f6e5a51155)


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


![Screenshot from 2025-04-23 21-56-22](https://github.com/user-attachments/assets/54c9eb0d-a87a-41d4-b077-ac7e66de7439)

 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT
![Screenshot from 2025-04-23 21-57-18](https://github.com/user-attachments/assets/e0c36084-5e1d-44c9-bff1-5089f68a012a)



#Backup commands
tar -cvf backup.tar *
## OUTPUT

![Screenshot from 2025-04-23 21-58-00](https://github.com/user-attachments/assets/12a015ce-08fb-4954-99d6-bfbbfa36e6b4)

mkdir backupdir
 
mv backup.tar backupdir
 
tar -tvf backup.tar
## OUTPUT
![Screenshot 2025-04-27 191153](https://github.com/user-attachments/assets/37bf87b1-4aad-407f-8b89-e2dad7f25cd5)


tar -xvf backup.tar
## OUTPUT
![Screenshot 2025-04-27 191206](https://github.com/user-attachments/assets/dbc07317-71f8-4afb-880f-eb4c016041b0)

gzip backup.tar

ls .gz
## OUTPUT
 ![Screenshot 2025-04-27 191213](https://github.com/user-attachments/assets/5ba09313-3ff5-46cb-8913-2f635bbcbcf3)

gunzip backup.tar.gz
## OUTPUT
![Screenshot 2025-04-27 191223](https://github.com/user-attachments/assets/8e0ce6fd-6272-49df-9951-8c76d0f5ab91)

 
# Shell Script
```
echo '#!/bin/sh' > my-script.sh
echo 'echo Hello World‘; exit 0 >> my-script.sh
```
chmod 755 my-script.sh
./my-script.sh
## OUTPUT
![Screenshot from 2025-04-23 22-17-46](https://github.com/user-attachments/assets/d3dab852-ce43-434a-9123-a079f4aed2bb)

 
cat << stop > herecheck.txt
```
hello in this world
i cant stop
for this non stop movement
stop
```

cat herecheck.txt
## OUTPUT
![Screenshot from 2025-04-23 22-19-17](https://github.com/user-attachments/assets/d09e7235-d6ab-4a3d-b99c-2360f86ea22e)


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
![Screenshot from 2025-04-23 22-21-50](https://github.com/user-attachments/assets/67c07529-645f-4aa2-9088-a650349b3418)

 
ls file1
## OUTPUT

![Screenshot from 2025-04-23 22-22-12](https://github.com/user-attachments/assets/dadba493-3307-4a54-9ddf-2e44e851a566)



echo $?
## OUTPUT 


![Screenshot from 2025-04-23 22-22-32](https://github.com/user-attachments/assets/d27c21c1-7a69-4afb-b455-ab2486a83780)

./one
bash: ./one: Permission denied
 
echo $?
## OUTPUT 

 ![Screenshot from 2025-04-23 22-24-04](https://github.com/user-attachments/assets/6e0f4ef3-aa98-44c7-b5af-dd424d1a89ab)

abcd
 
echo $?
 ## OUTPUT


![Screenshot from 2025-04-23 22-31-02](https://github.com/user-attachments/assets/6b4618a9-9bbd-42b8-8145-a9a31644ed61)


 
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

![Screenshot from 2025-04-23 22-40-22](https://github.com/user-attachments/assets/30ea678a-2f51-44a3-bfbf-9d8d02b4f697)



chmod 755 strcomp.sh
 
./strcomp.sh 
## OUTPUT

![Screenshot from 2025-04-23 22-31-02](https://github.com/user-attachments/assets/10470b83-36ea-4e48-b716-1830f30c800f)



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

![Screenshot from 2025-04-23 22-40-22](https://github.com/user-attachments/assets/906d7b39-a86d-4c2c-bbca-b59b372eb5e2)



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


![Screenshot from 2025-04-23 22-41-31](https://github.com/user-attachments/assets/0ad19303-f3d5-42d8-a980-38b6100507d1)




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

![Screenshot from 2025-04-23 22-43-10](https://github.com/user-attachments/assets/c2813bc1-ccdc-4cda-abfb-a16caf79908c)

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

![Screenshot from 2025-04-23 22-47-27](https://github.com/user-attachments/assets/9b6f8105-45d6-4fb4-ad67-86dd1fd03394)

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
![Screenshot from 2025-04-23 22-49-12](https://github.com/user-attachments/assets/2c2533b5-2f4d-44cf-9a8e-bc93f554e95a)



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

![Screenshot from 2025-04-23 22-50-21](https://github.com/user-attachments/assets/82d02eb8-ba32-479b-8532-4968c47f2da9)

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
## OUTPUT

 ![Screenshot from 2025-04-23 22-54-25](https://github.com/user-attachments/assets/e455d8c7-f797-45ae-a6dc-6dcded8c60cb)

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
./untiltest.sh
## OUTPUT 

![Screenshot from 2025-04-23 22-55-51](https://github.com/user-attachments/assets/e1693148-2a40-40e0-bb71-9c2f9a3e1e15)

 
 
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
./forin1.sh
## OUTPUT

![Screenshot from 2025-04-23 22-57-35](https://github.com/user-attachments/assets/895cb439-fe36-4c33-b550-3afccbf1bd75)

 
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

![Screenshot from 2025-04-23 22-58-44](https://github.com/user-attachments/assets/59a4a03e-a4e4-4e06-b97f-2b683f08b602)

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

![Screenshot from 2025-04-23 23-01-13](https://github.com/user-attachments/assets/2ac19508-ca83-4634-b954-7e57428f356a)

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
./forin1.sh

## OUTPUT
![Screenshot from 2025-04-23 23-02-02](https://github.com/user-attachments/assets/2bcf3e77-6470-40a2-bc18-2d750e9f35ce)


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
![Screenshot from 2025-04-23 23-06-35](https://github.com/user-attachments/assets/5c9e74e1-4810-41c5-945a-9ddf18db993b)


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

![Screenshot from 2025-04-23 23-07-29](https://github.com/user-attachments/assets/d0ab7984-0787-4d58-9971-3bffc40e6af9)

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

![Screenshot from 2025-04-23 23-08-44](https://github.com/user-attachments/assets/25e01ccf-f7ac-422a-954f-e3da98fbad7f)

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

![Screenshot from 2025-04-23 23-09-38](https://github.com/user-attachments/assets/67cd7366-ab5b-415d-a3cc-65e1e5414c83)

 
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
![Screenshot from 2025-04-23 23-11-09](https://github.com/user-attachments/assets/11137e07-6660-4e0c-b268-b3f9a2d0472a)

 
cat continue.sh 
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
 ![Screenshot from 2025-04-23 23-12-49](https://github.com/user-attachments/assets/86ad4ea8-3c89-4253-82cd-e6ef96172f42)

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

![Screenshot from 2025-04-23 23-15-01](https://github.com/user-attachments/assets/1190652e-3e72-4bed-a601-8abd464d5395)

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
![Screenshot from 2025-04-23 23-17-31](https://github.com/user-attachments/assets/988a0f43-5cdd-49a1-996a-f93bfa8f2a09)




 
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
![Screenshot from 2025-04-23 23-18-49](https://github.com/user-attachments/assets/d3afdbe4-0b5f-4a0e-82f0-3f157be90856)

 
 ./funcex.sh 1 2
![Screenshot from 2025-04-23 23-19-24](https://github.com/user-attachments/assets/fe0f7697-50b3-40b3-9e89-2ef0de13bc88)

 
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
 ![Screenshot from 2025-04-23 23-21-02](https://github.com/user-attachments/assets/a0399329-fed0-4c28-903d-c06fa5e0ffc5)

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
 ![Screenshot from 2025-04-23 23-23-15](https://github.com/user-attachments/assets/09ce6440-2762-4021-8fe9-325ac80bd545)

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
 
 ![Screenshot from 2025-04-23 23-24-36](https://github.com/user-attachments/assets/9acc38d8-e34f-4581-9db4-fb663e400dfd)

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
 ![Screenshot from 2025-04-23 23-26-05](https://github.com/user-attachments/assets/a3f8ec38-453e-455d-9588-2f2dd84095d0)

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
	# current digit in reverseift.sh 1 2 3
 
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
![Screenshot from 2025-04-23 23-27-49](https://github.com/user-attachments/assets/24dd43f4-cc5f-498a-9f58-a11ce91883e9)


# RESULT:
The Commands are executed successfully.

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
![Screenshot from 2025-03-17 09-40-18](https://github.com/user-attachments/assets/4494c84c-3c0e-445f-bbb0-714b6cfa0c8d)



cat < file2
## OUTPUT
![Screenshot from 2025-03-17 09-40-31](https://github.com/user-attachments/assets/a03aff58-5589-4164-a6b3-b714fcb91d72)


# Comparing Files
cmp file1 file2
## OUTPUT
 ![Screenshot from 2025-05-05 11-20-55](https://github.com/user-attachments/assets/274316a7-a071-4926-8139-1efcb5c53d58)

comm file1 file2
 ## OUTPUT
![Screenshot from 2025-05-22 09-17-45](https://github.com/user-attachments/assets/b4c4b650-23fb-472a-a533-afc726eeaf3f)

 
diff file1 file2
## OUTPUT
![Screenshot from 2025-05-05 11-24-16](https://github.com/user-attachments/assets/a5509d8a-1d10-444f-af61-c3bc28d8c560)


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
![Screenshot from 2025-05-05 11-25-55](https://github.com/user-attachments/assets/0bc7726c-1253-4d22-804c-36a25630e692)




cut -d "|" -f 1 file22
## OUTPUT
![Screenshot from 2025-05-05 11-26-19](https://github.com/user-attachments/assets/525198d7-dc44-4c8d-945d-be7e50d2424e)



cut -d "|" -f 2 file22
## OUTPUT
![Screenshot from 2025-05-05 11-26-39](https://github.com/user-attachments/assets/4c4d515f-2044-4598-ab7a-4cf85825a55e)


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
![Screenshot from 2025-05-20 20-03-47](https://github.com/user-attachments/assets/f7170d34-9f00-4558-832b-1cc09a033de3)



grep hello newfile 
## OUTPUT
![Screenshot from 2025-05-20 20-13-18](https://github.com/user-attachments/assets/3d6b73aa-6281-4cb3-a794-5893a86ec54b)



grep -v hello newfile 
## OUTPUT
![Screenshot from 2025-05-20 20-03-47](https://github.com/user-attachments/assets/7571d9bb-fd34-4081-9e58-3a559d9447d0)



cat newfile | grep -i "hello"
## OUTPUT
![Screenshot from 2025-05-20 20-36-10](https://github.com/user-attachments/assets/bab5bb3d-5fe1-4373-9c9e-d261429c59a4)




cat newfile | grep -i -c "hello"
## OUTPUT
![Screenshot from 2025-05-20 20-36-54](https://github.com/user-attachments/assets/51ebe578-c55c-4768-a066-e6cb4028e5f2)




grep -R ubuntu /etc
## OUTPUT
![Screenshot from 2025-05-20 20-16-21](https://github.com/user-attachments/assets/ea120d7d-875c-4f62-85e5-09ff1fc159ae)



grep -w -n world newfile   
## OUTPUT
![Screenshot from 2025-05-20 20-40-32](https://github.com/user-attachments/assets/8383b87b-84f1-4581-89fc-d417164409f6)
![Screenshot from 2025-05-20 20-40-48](https://github.com/user-attachments/assets/45a5ea4d-b0dd-4424-9f8c-b8baa2feab05)


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
![Screenshot from 2025-05-20 20-47-07](https://github.com/user-attachments/assets/a3e45d86-fe17-4325-9a47-8f6c6d2de34e)



egrep -w '(H|h)ello' newfile 
## OUTPUT
![Screenshot from 2025-05-20 20-47-17](https://github.com/user-attachments/assets/c2f66c1c-fe3a-41b5-a4a6-615e261d5c1b)



egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT
![Screenshot from 2025-05-20 20-47-25](https://github.com/user-attachments/assets/aab729a4-81f7-4189-8f5e-a186fb961eef)




egrep '(^hello)' newfile 
## OUTPUT
![Screenshot from 2025-05-20 20-48-01](https://github.com/user-attachments/assets/55986000-2a27-4ce4-a5dd-2834acceaffa)



egrep '(world$)' newfile 
## OUTPUT
![Screenshot from 2025-05-20 20-48-16](https://github.com/user-attachments/assets/9ff46f7b-2a97-45a5-aa4c-8362196b589f)



egrep '(World$)' newfile 
## OUTPUT
![Screenshot from 2025-05-20 20-48-33](https://github.com/user-attachments/assets/72bf3019-c942-445a-a185-3e1caf8f19f5)


egrep '((W|w)orld$)' newfile 
## OUTPUT
![Screenshot from 2025-05-20 20-49-43](https://github.com/user-attachments/assets/00971ff5-4da7-4abf-9a95-12ecb5207d97)



egrep '[1-9]' newfile 
## OUTPUT
![Screenshot from 2025-05-20 20-50-26](https://github.com/user-attachments/assets/d2e0bf2c-7dee-41d6-8edb-98d8547e4ff9)



egrep 'Linux.*world' newfile 
## OUTPUT
![Screenshot from 2025-05-20 20-50-55](https://github.com/user-attachments/assets/0478c72b-df19-45ef-a68e-71dfad7d32ed)


egrep 'Linux.*World' newfile 
## OUTPUT
![Screenshot from 2025-05-20 20-51-14](https://github.com/user-attachments/assets/2a83e147-7f7d-4520-835d-9d24de489aa1)


egrep l{2} newfile
## OUTPUT
![Screenshot from 2025-05-20 20-51-59](https://github.com/user-attachments/assets/addbed7e-93c0-4af4-a667-36c9259d6d6e)



egrep 's{1,2}' newfile
## OUTPUT 


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
![Screenshot from 2025-05-20 20-53-12](https://github.com/user-attachments/assets/3b73ad14-ae20-4d38-b781-d032a0fd3380)



sed -n -e '$p' file23
## OUTPUT
![Screenshot from 2025-05-20 20-53-30](https://github.com/user-attachments/assets/b31145ec-288b-4cca-a0f9-bb251cac90b3)



sed  -e 's/Ram/Sita/' file23
## OUTPUT
![Screenshot from 2025-05-20 20-54-20](https://github.com/user-attachments/assets/110869af-6349-44fe-ada7-1c7e0e61ce31)



sed  -e '2s/Ram/Sita/' file23
## OUTPUT
![Screenshot from 2025-05-20 20-54-43](https://github.com/user-attachments/assets/9d9bd1f9-a14f-4745-bf37-d8b10b925cca)



sed  '/tom/s/5000/6000/' file23
## OUTPUT
![Screenshot from 2025-05-20 20-55-16](https://github.com/user-attachments/assets/2b0d8545-d3a1-4a75-8829-5a8f8c0bdc6e)



sed -n -e '1,5p' file23
## OUTPUT
![Screenshot from 2025-05-20 20-55-54](https://github.com/user-attachments/assets/1d21e9f4-4d96-4bfd-87d6-a93e77e4b7cf)



sed -n -e '2,/Joe/p' file23
## OUTPUT
![Screenshot from 2025-05-20 21-01-13](https://github.com/user-attachments/assets/f8f3c318-2428-4bc4-90b9-84fd947fc3fb)




sed -n -e '/tom/,/Joe/p' file23
## OUTPUT
![Screenshot from 2025-05-20 21-04-39](https://github.com/user-attachments/assets/3d1fc8dc-4401-40fd-bd0b-23cdc167c5c5)



seq 10 
## OUTPUT
![Screenshot from 2025-05-20 21-05-06](https://github.com/user-attachments/assets/08bad095-02de-4217-9ff1-4ce22e933d91)



seq 10 | sed -n '4,6p'
## OUTPUT
![Screenshot from 2025-05-20 21-05-29](https://github.com/user-attachments/assets/112da445-f2ed-470a-a170-3c714c5ad464)



seq 10 | sed -n '2,~4p'
## OUTPUT
![Screenshot from 2025-05-20 21-05-44](https://github.com/user-attachments/assets/d4489f72-bbb8-4b7d-9f61-5e116ccb6f48)



seq 3 | sed '2a hello'
## OUTPUT
![Screenshot from 2025-05-20 21-06-11](https://github.com/user-attachments/assets/84763f0c-b788-4043-ae7a-8e280af1a6aa)



seq 2 | sed '2i hello'
## OUTPUT
![Screenshot from 2025-05-20 21-06-28](https://github.com/user-attachments/assets/11a5ea25-7e89-4704-88a8-863cc2000ffa)


seq 10 | sed '2,9c hello'
## OUTPUT
![Screenshot from 2025-05-20 21-06-43](https://github.com/user-attachments/assets/5694699b-a82d-476e-ad9d-18192fadbfc8)


sed -n '2,4{s/^/$/;p}' file23
## OUTPUT
![Screenshot from 2025-05-20 21-06-59](https://github.com/user-attachments/assets/943192d9-c8db-4f59-b690-ece725305098)


sed -n '2,4{s/$/*/;p}' file23
## OUTPUT
![Screenshot from 2025-05-20 21-08-09](https://github.com/user-attachments/assets/4772848a-70c7-4a5f-be14-d23f3606c986)


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
![Screenshot from 2025-05-20 21-15-02](https://github.com/user-attachments/assets/8a52bbcb-6436-41f5-942b-2b9ecf33585e)


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

![Screenshot from 2025-05-20 21-16-12](https://github.com/user-attachments/assets/51455790-432a-44b2-9eb9-e53817c88f0e)

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

![Screenshot from 2025-05-20 21-17-59](https://github.com/user-attachments/assets/174970da-c06b-4129-b683-b35ed2d372b8)


 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT

![Screenshot from 2025-05-20 21-17-59](https://github.com/user-attachments/assets/b7eb8cc0-ab85-462f-a1f0-6ff4335201a4)



#Backup commands
tar -cvf backup.tar *
## OUTPUT

![Screenshot from 2025-05-20 21-20-23](https://github.com/user-attachments/assets/28251136-658e-4801-8b0b-bf455d1cf068)


mkdir backupdir
 
mv backup.tar backupdir
 
tar -tvf backup.tar
## OUTPUT

![Screenshot from 2025-05-20 21-28-02](https://github.com/user-attachments/assets/1d3dadf4-311f-4099-8986-5d4d80d7e167)


tar -xvf backup.tar
## OUTPUT

![Screenshot from 2025-05-20 21-36-28](https://github.com/user-attachments/assets/31c98356-59c7-4d92-ae9c-1627f0837a95)

gzip backup.tar

ls .gz
## OUTPUT

 ![Screenshot from 2025-05-20 21-43-19](https://github.com/user-attachments/assets/9330e639-6cd2-46f3-b9f6-bf0e8e99d93f)

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

![Screenshot from 2025-05-22 09-12-00](https://github.com/user-attachments/assets/008c78ae-7c90-4c1c-8877-f8ce81effeb5)

 
cat << stop > herecheck.txt
```
hello in this world
i cant stop
for this non stop movement
stop
```

cat herecheck.txt
## OUTPUT

![Screenshot from 2025-05-22 09-13-17](https://github.com/user-attachments/assets/acaa7c16-ed7f-4659-97f1-ecb74c9c7b41)


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

![Screenshot from 2025-05-22 09-16-09](https://github.com/user-attachments/assets/42b76341-04cc-471d-a6d0-263a9e2bea9e)

 
ls file1
## OUTPUT

![Screenshot from 2025-05-22 09-16-33](https://github.com/user-attachments/assets/33b4e4f6-698c-47c1-b1d2-b8d2910ce4ab)

echo $?
## OUTPUT 

![Screenshot from 2025-05-22 09-16-45](https://github.com/user-attachments/assets/970cedd9-b8a3-46a2-b089-6d964211acc3)

./one
bash: ./one: Permission denied
 
echo $?
## OUTPUT 

 ![Screenshot from 2025-05-22 09-17-45](https://github.com/user-attachments/assets/ff7b4b85-2c98-4646-8e37-637ed5addcc4)

abcd
 
echo $?
 ## OUTPUT

![Screenshot from 2025-05-22 09-17-45](https://github.com/user-attachments/assets/eb7f4979-3b9d-45e9-99ed-5f7d3970abbb)



 
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

![Screenshot from 2025-05-22 09-20-22](https://github.com/user-attachments/assets/31e5cb72-b2cc-433a-8726-a505744e1303)


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

![Screenshot from 2025-05-22 09-23-18](https://github.com/user-attachments/assets/34e5157a-c22d-4a12-9721-fd50127e6b7d)

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

![Screenshot from 2025-05-22 09-24-55](https://github.com/user-attachments/assets/4da8c50f-d3d5-4047-8a51-cfcd344cfeb8)



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

![Screenshot from 2025-05-22 09-26-38](https://github.com/user-attachments/assets/849cabf0-9cda-4898-841c-42a8afbc6973)

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

![Screenshot from 2025-05-22 09-27-42](https://github.com/user-attachments/assets/72357fef-1c49-434d-8cb8-17ff1b5cc6c0)

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

![Screenshot from 2025-05-22 09-28-51](https://github.com/user-attachments/assets/e1011eae-84ed-4822-b91a-f0b0a49d5a99)


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

![Screenshot from 2025-05-22 09-30-02](https://github.com/user-attachments/assets/7b77dfa7-8361-4797-934c-c47db2d2d8fe)

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

![Screenshot from 2025-05-22 09-30-59](https://github.com/user-attachments/assets/ffbbaba3-31c2-46c6-aa28-7952a74bfc36)

 
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

 ![Screenshot from 2025-05-22 09-35-26](https://github.com/user-attachments/assets/1cb7d4b5-ce4a-4ca4-9873-0356923264e0)

 
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
$ ./untilest.sh
# OUTPUT

 ![Screenshot from 2025-05-22 09-36-36](https://github.com/user-attachments/assets/73119f6d-ae78-4254-824a-819641c26045)

 
 
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
$ ./forin1.sh
# OUTPUT

 ![Screenshot from 2025-05-22 09-37-33](https://github.com/user-attachments/assets/34192698-e012-4730-9ddc-338756bad5df)

 
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
# OUTPUT

![Screenshot from 2025-05-22 09-38-36](https://github.com/user-attachments/assets/572dbcb2-5fe5-4a04-8a64-86515a443fcb)

 
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
# OUTPUT
 
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

![Screenshot from 2025-05-22 09-40-29](https://github.com/user-attachments/assets/fde532cc-b773-4f94-9f1b-3fdc0af84142)

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

![Screenshot from 2025-05-22 09-47-28](https://github.com/user-attachments/assets/1d429ae3-5725-4d02-bcf5-6ba93a140972)


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

![Screenshot from 2025-05-22 19-50-24](https://github.com/user-attachments/assets/f15aa7ea-fcdd-4018-9d67-e30e42e24251)

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

![Screenshot from 2025-05-22 19-53-18](https://github.com/user-attachments/assets/a85f1d8b-c589-4112-94ad-f25da5e3770d)

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

![Screenshot from 2025-05-22 19-54-15](https://github.com/user-attachments/assets/8d98c452-ce36-4208-b1eb-94b6546b7fcb)

 
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

![Screenshot from 2025-05-22 19-55-21](https://github.com/user-attachments/assets/99f17f20-e819-45ba-a2c8-2c8bd5fb3880)

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

![Screenshot from 2025-05-22 19-58-09](https://github.com/user-attachments/assets/41d7e690-eb69-460e-8270-d7d51b4737eb)



 cat exread1.sh
```bash
#!/bin/bash
# testing the read command
read -p "Enter your name: " name
echo "Hello $name, welcome to my program. “
``` 
$ chmod 755 exread1.sh 

## OUTPUT


![Screenshot from 2025-05-22 19-59-23](https://github.com/user-attachments/assets/ca68ada4-9a8c-4f0b-a9d7-00ccbd7eebf9)



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

![Screenshot from 2025-05-22 20-02-53](https://github.com/user-attachments/assets/00f6b89a-ff10-49e1-a576-9bff35b2e645)

 
 ./funcex.sh 1 2

![Screenshot from 2025-05-22 20-03-32](https://github.com/user-attachments/assets/74f5ae1a-acf6-46d5-bb11-2a48a28e7969)

 
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

 ![Screenshot from 2025-05-22 20-06-24](https://github.com/user-attachments/assets/258ceda7-d5b2-4b02-9231-6f6bdd3a0355)

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

 ![Screenshot from 2025-05-22 20-08-28](https://github.com/user-attachments/assets/40b53863-5ffb-439a-80f6-af214135a23d)

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

![Screenshot from 2025-05-22 20-09-23](https://github.com/user-attachments/assets/5db8ae0a-4ead-48cb-bc2a-3bc9125f4cd7)

 
 
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

![Screenshot from 2025-05-22 20-10-34](https://github.com/user-attachments/assets/bee74bbb-3e21-44b4-af32-8b519ab00369)

 
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

![Screenshot from 2025-05-22 20-11-48](https://github.com/user-attachments/assets/5867bd59-2198-4c1a-9030-c2b0406906d6)


# RESULT:
The Commands are executed successfully.

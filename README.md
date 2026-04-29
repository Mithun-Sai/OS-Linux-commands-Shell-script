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
<img width="559" height="133" alt="image" src="https://github.com/user-attachments/assets/488f1578-5692-4186-80e6-3194a9e361c5" />


cat < file2
## OUTPUT
<img width="609" height="146" alt="image" src="https://github.com/user-attachments/assets/a9de771e-9f4d-4fab-bc88-cbbcea8cb349" />


# Comparing Files
cmp file1 file2
## OUTPUT
 <img width="575" height="54" alt="image" src="https://github.com/user-attachments/assets/65d3b9e4-d6ed-41f6-8d99-7150b291d26f" />


comm file1 file2
 ## OUTPUT
<img width="594" height="259" alt="image" src="https://github.com/user-attachments/assets/fa140367-8606-4fbb-bcd9-7d81cbd773df" />

 
diff file1 file2
## OUTPUT
<img width="614" height="202" alt="image" src="https://github.com/user-attachments/assets/2b4e82ba-b0f5-42c3-8893-331c4a381591" />


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
<img width="606" height="96" alt="image" src="https://github.com/user-attachments/assets/34a636d9-0d15-46d4-b5d7-7b88d14ebc54" />



cut -d "|" -f 1 file22
## OUTPUT
<img width="580" height="112" alt="image" src="https://github.com/user-attachments/assets/bb66c140-3d84-47fd-8c63-1e3c3a6f676a" />



cut -d "|" -f 2 file22
## OUTPUT
<img width="629" height="110" alt="image" src="https://github.com/user-attachments/assets/81207329-2d1c-4a51-b274-c37ebd3c50ae" />


cat > newfile 
```
Hello world
hello world
^d
````
cat < newfile 
## output
 <img width="582" height="110" alt="image" src="https://github.com/user-attachments/assets/1371b011-b9e2-480a-b4cf-bce772b745c4" />

grep Hello newfile 
## OUTPUT
<img width="606" height="57" alt="image" src="https://github.com/user-attachments/assets/b5240765-ffcb-42d3-9d18-ce41ae7dd567" />



grep hello newfile 
## OUTPUT
<img width="633" height="52" alt="image" src="https://github.com/user-attachments/assets/8db37a1a-de62-4c75-8871-7cd39981f31b" />


grep -v hello newfile 
## OUTPUT
<img width="590" height="76" alt="image" src="https://github.com/user-attachments/assets/0d46baa5-e5a7-4735-ae1c-8d8786b21da6" />


cat newfile | grep -i "hello"
## OUTPUT
<img width="607" height="75" alt="image" src="https://github.com/user-attachments/assets/0b216727-158d-4148-8925-545d7617ba66" />



cat newfile | grep -i -c "hello"
## OUTPUT
<img width="572" height="59" alt="image" src="https://github.com/user-attachments/assets/e1144233-70b3-4710-803e-b1a7b6060551" />



grep -R ubuntu /etc
## OUTPUT



grep -w -n world newfile   
## OUTPUT
<img width="624" height="75" alt="image" src="https://github.com/user-attachments/assets/5635bb24-e4e8-4b82-bbfc-ea5e98b66fe2" />


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
<img width="618" height="79" alt="image" src="https://github.com/user-attachments/assets/ff6607e5-fee5-4383-840e-2b92af1d8b35" />



egrep -w '(H|h)ello' newfile 
## OUTPUT
<img width="574" height="77" alt="image" src="https://github.com/user-attachments/assets/b3cc5129-6364-45d0-800e-8e3d72334afb" />



egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT
<img width="587" height="74" alt="image" src="https://github.com/user-attachments/assets/b08b7e82-422c-4c7d-b4d0-fbaa62976f40" />




egrep '(^hello)' newfile 
## OUTPUT
<img width="586" height="58" alt="image" src="https://github.com/user-attachments/assets/45fd8a8d-b87d-4ef3-827b-d49a408ba487" />



egrep '(world$)' newfile 
## OUTPUT
<img width="544" height="75" alt="image" src="https://github.com/user-attachments/assets/e5bcd77f-fc0c-4e6f-ba9a-3852dc864a02" />



egrep '(World$)' newfile 
## OUTPUT
<img width="582" height="60" alt="image" src="https://github.com/user-attachments/assets/7ec20320-827c-45b9-aa7f-3d5f7ca8ecd7" />


egrep '((W|w)orld$)' newfile 
## OUTPUT
<img width="590" height="94" alt="image" src="https://github.com/user-attachments/assets/381b25a6-a1af-40fa-a167-7f92cd316613" />



egrep '[1-9]' newfile 
## OUTPUT
<img width="564" height="59" alt="image" src="https://github.com/user-attachments/assets/ad6a9b3e-81df-4d57-be1f-631b8f8b69b7" />



egrep 'Linux.*world' newfile 
## OUTPUT
<img width="586" height="57" alt="image" src="https://github.com/user-attachments/assets/aeb9f463-82a6-4149-b196-5985636fabde" />


egrep 'Linux.*World' newfile 
## OUTPUT
<img width="547" height="61" alt="image" src="https://github.com/user-attachments/assets/a98db281-c337-4c4b-9aff-0f1f43944516" />


egrep l{2} newfile
## OUTPUT
<img width="576" height="76" alt="image" src="https://github.com/user-attachments/assets/61f25822-4ccc-4317-89a0-1a567db1c300" />



egrep 's{1,2}' newfile
## OUTPUT 
<img width="577" height="98" alt="image" src="https://github.com/user-attachments/assets/9f6a0a54-f616-400d-8d57-e615719795f2" />


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
<img width="620" height="58" alt="image" src="https://github.com/user-attachments/assets/2e768682-510a-4eca-bd50-fb545f541590" />



sed -n -e '$p' file23
## OUTPUT
<img width="598" height="59" alt="image" src="https://github.com/user-attachments/assets/19dca5df-fc65-496a-891b-f66cc0c6141b" />



sed  -e 's/Ram/Sita/' file23
## OUTPUT
<img width="574" height="202" alt="image" src="https://github.com/user-attachments/assets/2fcf3691-be8f-4760-897c-4b0e146068be" />



sed  -e '2s/Ram/Sita/' file23
## OUTPUT
<img width="582" height="202" alt="image" src="https://github.com/user-attachments/assets/bb7530c8-c8b8-4226-80c7-920806e57fcc" />



sed  '/tom/s/5000/6000/' file23
## OUTPUT
<img width="580" height="201" alt="image" src="https://github.com/user-attachments/assets/9194fbb9-6e25-4663-ba44-3fc6017fee06" />



sed -n -e '1,5p' file23
## OUTPUT
<img width="596" height="131" alt="image" src="https://github.com/user-attachments/assets/64c56a1e-3b55-4385-90ba-dac36c6eefab" />



sed -n -e '2,/Joe/p' file23
## OUTPUT
<img width="640" height="94" alt="image" src="https://github.com/user-attachments/assets/91baae5c-a88e-4b69-a11d-173d3110acbd" />




sed -n -e '/tom/,/Joe/p' file23
## OUTPUT
<img width="629" height="75" alt="image" src="https://github.com/user-attachments/assets/a2f3c4bf-93b8-40f2-ae19-c34d8d7893dd" />



seq 10 
## OUTPUT
<img width="597" height="217" alt="image" src="https://github.com/user-attachments/assets/36da543c-a108-42e9-9a61-146debd84369" />



seq 10 | sed -n '4,6p'
## OUTPUT
<img width="602" height="93" alt="image" src="https://github.com/user-attachments/assets/c263781a-081e-42de-88e1-21fcf653a011" />



seq 10 | sed -n '2,~4p'
## OUTPUT
<img width="612" height="90" alt="image" src="https://github.com/user-attachments/assets/061d13be-8156-4d0b-bc3b-2f2add30b039" />



seq 3 | sed '2a hello'
## OUTPUT
<img width="593" height="113" alt="image" src="https://github.com/user-attachments/assets/9023d8ed-87a2-4868-aeb1-028ec73b86a1" />



seq 2 | sed '2i hello'
## OUTPUT
<img width="597" height="95" alt="image" src="https://github.com/user-attachments/assets/894383bd-3bed-438f-a378-d2cdb156e610" />


seq 10 | sed '2,9c hello'
## OUTPUT
<img width="586" height="95" alt="image" src="https://github.com/user-attachments/assets/7432b324-649c-4490-a408-13df738a88e3" />


sed -n '2,4{s/^/$/;p}' file23
## OUTPUT
<img width="585" height="88" alt="image" src="https://github.com/user-attachments/assets/e364ac54-749b-486c-a049-fff652bd22d5" />



sed -n '2,4{s/$/*/;p}' file23
<img width="642" height="92" alt="image" src="https://github.com/user-attachments/assets/34760927-5bc3-4a0b-8148-4d84a49b1397" />


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
<img width="639" height="135" alt="image" src="https://github.com/user-attachments/assets/4c413957-0dbf-4337-b8cc-ce7eea626296" />


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
<img width="608" height="129" alt="image" src="https://github.com/user-attachments/assets/cbe4fafd-7fd0-4a39-8441-6e42587d4e0b" />



#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT
<img width="603" height="199" alt="image" src="https://github.com/user-attachments/assets/61e72d20-85fb-4366-bff2-f77b7b365acc" />


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
<img width="630" height="95" alt="image" src="https://github.com/user-attachments/assets/339d4950-7fe9-48ca-a5a2-3ef267ac39c3" />


 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT
<img width="596" height="86" alt="image" src="https://github.com/user-attachments/assets/c5a15b10-ea6c-499c-94ee-be9268b92ed2" />



#Backup commands
tar -cvf backup.tar *
## OUTPUT
<img width="642" height="220" alt="image" src="https://github.com/user-attachments/assets/d383fd9c-a9ba-4c1c-b4b8-8f307444f2a0" />


mkdir backupdir
 
mv backup.tar backupdir

cd backupdir
 
tar -tvf backup.tar
## OUTPUT
<img width="661" height="331" alt="image" src="https://github.com/user-attachments/assets/3f97841a-f8c0-46a1-9de8-0c58db1e7312" />



tar -xvf backup.tar
## OUTPUT
<img width="652" height="217" alt="image" src="https://github.com/user-attachments/assets/d28bc50a-1556-4723-9ee5-ca1d2ec930e5" />


gzip backup.tar

ls .gz
## OUTPUT
 <img width="651" height="198" alt="image" src="https://github.com/user-attachments/assets/c732aa9a-e29f-4193-b7ad-7a595133bda8" />


gunzip backup.tar.gz
## OUTPUT
<img width="651" height="198" alt="image" src="https://github.com/user-attachments/assets/a9f1d6db-cc53-4988-a0b5-e8b3f05e5d77" />

 ls
# Shell Script
```
echo '#!/bin/sh' > my-script.sh
echo 'echo Hello World'; exit 0 >> my-script.sh
```
chmod 755 my-script.sh
./my-script.sh
## OUTPUT
<img width="610" height="171" alt="image" src="https://github.com/user-attachments/assets/567fdb61-fe69-4641-9a25-962a82b11f81" />

 
cat << stop > herecheck.txt
```
hello in this world
i cant stop
for this non stop movement
stop
```

cat herecheck.txt
## OUTPUT
<img width="525" height="95" alt="image" src="https://github.com/user-attachments/assets/8e78c1a5-c014-4c6c-8591-e73e100f662a" />


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
<img width="591" height="245" alt="image" src="https://github.com/user-attachments/assets/1544fd02-0b6b-4c85-a727-adf9365f5c8b" />

 
ls file1
## OUTPUT
<img width="511" height="47" alt="image" src="https://github.com/user-attachments/assets/75755b49-40d2-4800-8791-85e19e34c332" />


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
<img width="599" height="170" alt="image" src="https://github.com/user-attachments/assets/43c777f9-ac14-434e-a487-18a310e223b4" />



chmod 755 strcomp.sh
 
./strcomp.sh 
## OUTPUT
<img width="514" height="69" alt="image" src="https://github.com/user-attachments/assets/6b8be655-f7fb-46a6-96e9-cb173ea4c09d" />


# check file ownership
cat > psswdperm.sh 
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
<img width="570" height="65" alt="image" src="https://github.com/user-attachments/assets/d90d2b7d-fefd-400c-9ad6-43a31ed9d0f7" />

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
<img width="623" height="76" alt="image" src="https://github.com/user-attachments/assets/b4565e5b-164c-49ea-afc2-2d33a16bfb6e" />



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
<img width="568" height="69" alt="image" src="https://github.com/user-attachments/assets/61718417-e519-4ec1-9039-7c0780698c35" />


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
<img width="528" height="82" alt="image" src="https://github.com/user-attachments/assets/696d2ea8-d5dc-41bc-994a-23848f3e80c5" />


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
<img width="516" height="48" alt="image" src="https://github.com/user-attachments/assets/95110ad9-bb2a-40ea-b300-344b8ce1bbc2" />


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
<img width="499" height="45" alt="image" src="https://github.com/user-attachments/assets/9c816921-aaba-499f-b10a-fecba468fc44" />


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
 <img width="513" height="53" alt="image" src="https://github.com/user-attachments/assets/d606ced2-0489-4ec2-a7f1-c527a2bbdb0c" />


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
 <img width="560" height="185" alt="image" src="https://github.com/user-attachments/assets/089e600d-9c0d-4ed6-afc8-bfad293ff7c3" />

 
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
./untiltesh.sh
 ##output
<img width="557" height="106" alt="image" src="https://github.com/user-attachments/assets/396628ed-f606-413f-96fc-c3cab3e31671" />

 
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

 .forin1.sh
 ##output
 <img width="538" height="142" alt="image" src="https://github.com/user-attachments/assets/1a5910ec-36f9-41f7-bdbc-f33bc71ecb8a" />

cat > forin2.sh 
```bash
\#!/bin/bash
\# another example of how not to use the for command
for test in I don't know if this'll work
do
echo “word:$test”
done
 ```
 
$ chmod 755 forin2.sh
 ./forin2.sh
 ##output
 <img width="580" height="92" alt="image" src="https://github.com/user-attachments/assets/489b92ca-9899-45f7-8f6b-f5267a1ec57d" />


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
 ##output
 <img width="522" height="120" alt="image" src="https://github.com/user-attachments/assets/88b161f3-0499-4401-8a8e-b31cecd9cd53" />

cat forin3.sh 
```bash
\#!/bin/bash
\# another example of how not to use the for command
for test in I don\'t know if "this'll" work
do
echo "word:$test"
done
```
$ chmod 755 forin3.sh

$ ./forin3.sh 
 ##output
 <img width="564" height="139" alt="image" src="https://github.com/user-attachments/assets/37d991ed-47b8-4cbb-91a9-093d52a84e10" />

cat > forin1.sh 
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

##output
<img width="520" height="119" alt="image" src="https://github.com/user-attachments/assets/81e312ea-e466-43ea-bd9d-1d9491e66c14" />

## OUTPUT
cat forinfile.sh 
```bash
#!/bin/bash
# reading values from a file
file="cities"
for state in `cat $file`
do
echo "Visit beautiful $file"
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
<img width="556" height="137" alt="image" src="https://github.com/user-attachments/assets/86c42693-2ef7-4cb7-90a0-c6f51659f191" />


cat forctype.sh 
```bash
#!/bin/bash
# testing the C-style for loop
for (( i=1; i <= 5; i++ ))
do
echo "The value of i is $i"
done
````
chmod 755 forctype.sh
./forctype.sh 
## OUTPUT
<img width="549" height="111" alt="image" src="https://github.com/user-attachments/assets/e354c21d-ff43-407a-88be-cbafd3f2b335" />

cat forctype1.sh 
```bash
#!/bin/bash
# multiple variables
for (( a=1, b=5; a <= 5; a++, b-- ))
do
echo "$a - $b"
done
```
chmod 755 forctype.sh
./forctype1.sh 
## OUTPUT
<img width="583" height="112" alt="image" src="https://github.com/user-attachments/assets/18e2b529-1b8c-432c-9585-13300fa2b9d7" />

cat > fornested1.sh 
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
chmod 755 fornested1.sh
 
./fornested1.sh 
## OUTPUT
<img width="559" height="214" alt="image" src="https://github.com/user-attachments/assets/3bb63c55-e19f-45b6-8994-11575d07cb3f" />

 
cat > forbreak.sh 
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
echo "The for loop is completed"
```

chmod 755 forbreak.sh
./forbreak.sh

 ## OUTPUT
<img width="569" height="71" alt="image" src="https://github.com/user-attachments/assets/a61ae0c3-de25-4e97-80b3-98b8a8f954ee" />


cat > forcontiune.sh
```
```
chmod 755 forcontinue.sh
./forcontinue.sh 
## OUTPUT
 
cat > exread.sh 
```bash
#!/bin/bash
# testing the read command
echo -n "Enter your name: "
read name
echo "Hello $name, welcome to my program. "
 ```
 
chmod 755 exread.sh 
./exread.sh 
## OUTPUT
<img width="548" height="73" alt="image" src="https://github.com/user-attachments/assets/aa676abc-73fe-484b-aef2-6083ea2b3ed6" />


 cat > exread1.sh
```bash
#!/bin/bash
# testing the read command
read -p "Enter your name: " name
echo "Hello $name, welcome to my program. "
``` 
chmod 755 exread1.sh 
./exread.sh
## OUTPUT
<img width="594" height="87" alt="image" src="https://github.com/user-attachments/assets/42d7a79c-c109-4bcf-93a7-2f020e3837b6" />

 
cat > funcex.sh
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
```
## OUTPUT
./funcex.sh 
<img width="542" height="51" alt="image" src="https://github.com/user-attachments/assets/16d48951-d1e3-49b0-bbeb-0228ee89cd9c" />

./funcex.sh 1 2
 
cat > argshift.sh
```bash
#!/bin/bash 
 while (( "$#" )); do 
  echo $1 
  shift 
done
```
chmod 777 argshift.sh

## OUTPUT
./argshift.sh 1 2 3
 <img width="567" height="87" alt="image" src="https://github.com/user-attachments/assets/e6d849e6-8009-484d-ba21-23b3d996ef87" />

 cat > argshift1.sh
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
chmod 777 argshift.sh
## OUTPUT
./argshift.sh 1 2 3
 <img width="533" height="80" alt="image" src="https://github.com/user-attachments/assets/f3f88c70-baf1-483f-991d-f6bf014114c8" />

cat > argshift.sh
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
 <img width="536" height="248" alt="image" src="https://github.com/user-attachments/assets/7d198e9d-552d-4950-a52c-7b0485fc8988" />

 
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
cat > data.dat
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
 <img width="561" height="244" alt="image" src="https://github.com/user-attachments/assets/631f09cb-f7ac-4373-97df-5599dd905f77" />

cat > palindrome.sh
```bash
num=545
echo "Enter the number"
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
<img width="585" height="70" alt="image" src="https://github.com/user-attachments/assets/d41ef7fe-cc4b-4706-8e19-8b299285fb3b" />


# RESULT:
The Commands are executed successfully.

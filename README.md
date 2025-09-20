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
<img width="578" height="100" alt="Screenshot from 2025-08-15 12-43-00 (copy)" src="https://github.com/user-attachments/assets/8a7a2fb1-f5c6-46da-acf3-21c1659e16df" />



cat < file2
## OUTPUT
<img width="578" height="118" alt="Screenshot from 2025-08-15 12-43-20" src="https://github.com/user-attachments/assets/efc65212-71aa-474f-874a-08f6ac46ea61" />


# Comparing Files
cmp file1 file2
## OUTPUT
 <img width="578" height="42" alt="Screenshot from 2025-08-15 12-43-35" src="https://github.com/user-attachments/assets/60523d16-7541-4fa4-a3fd-afbf3b0ba7b6" />

comm file1 file2
 ## OUTPUT
<img width="527" height="167" alt="Screenshot from 2025-08-15 12-47-07" src="https://github.com/user-attachments/assets/87c24323-dc4f-43cd-a780-74be974b0fba" />

 
diff file1 file2
## OUTPUT
<img width="527" height="181" alt="Screenshot from 2025-08-15 12-47-49" src="https://github.com/user-attachments/assets/7fa236fa-8599-4ea7-9a37-62942e1b1d89" />


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
<img width="527" height="58" alt="Screenshot from 2025-08-15 13-02-15" src="https://github.com/user-attachments/assets/0243d978-4908-4ffe-a6ea-e0f61ad59f99" />




cut -d "|" -f 1 file22
## OUTPUT
<img width="553" height="78" alt="Screenshot from 2025-08-15 13-02-45" src="https://github.com/user-attachments/assets/276040d4-d13b-473f-8de0-da5aa037e2cc" />



cut -d "|" -f 2 file22
## OUTPUT
<img width="553" height="78" alt="Screenshot from 2025-08-15 13-02-53" src="https://github.com/user-attachments/assets/a2053b5f-48a6-4896-979a-8163ce7a0b8f" />


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
<img width="553" height="42" alt="Screenshot from 2025-08-15 13-06-55" src="https://github.com/user-attachments/assets/ebeef68c-91d4-43bb-8972-faed24e7e7f3" />



grep hello newfile 
## OUTPUT
<img width="553" height="42" alt="Screenshot from 2025-08-15 13-07-02" src="https://github.com/user-attachments/assets/16de91f2-accd-4ca4-9af2-45d1bdfb3b3b" />




grep -v hello newfile 
## OUTPUT
<img width="553" height="42" alt="Screenshot from 2025-08-15 13-07-11" src="https://github.com/user-attachments/assets/eb26e811-d972-48aa-82b8-ab5e2a51deb9" />



cat newfile | grep -i "hello"
## OUTPUT
<img width="613" height="63" alt="Screenshot from 2025-08-15 13-07-44" src="https://github.com/user-attachments/assets/73b4be1b-c243-44ed-81b2-6afbab5d529e" />




cat newfile | grep -i -c "hello"
## OUTPUT
<img width="643" height="39" alt="Screenshot from 2025-08-15 13-07-59" src="https://github.com/user-attachments/assets/572132eb-ee36-4871-b903-921ee7421bce" />




grep -R ubuntu /etc
## OUTPUT
<img width="920" height="326" alt="Screenshot from 2025-08-15 13-10-17" src="https://github.com/user-attachments/assets/e3f0af62-52d6-4f66-8622-07258a7cb030" />



grep -w -n world newfile   
## OUTPUT

<img width="610" height="57" alt="Screenshot from 2025-08-15 13-10-58" src="https://github.com/user-attachments/assets/058236e2-123c-41c1-9831-84de10304828" />

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
<img width="627" height="63" alt="Screenshot from 2025-08-18 11-31-41" src="https://github.com/user-attachments/assets/007cc3c1-a67a-43a8-ae7c-fd299971bdbb" />



egrep -w '(H|h)ello' newfile 
## OUTPUT



egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT
<img width="643" height="60" alt="Screenshot from 2025-08-18 11-31-57" src="https://github.com/user-attachments/assets/82b993d0-ad58-4599-88c6-a0fc4644bd54" />




egrep '(^hello)' newfile 
## OUTPUT
<img width="643" height="47" alt="Screenshot from 2025-08-18 11-32-05" src="https://github.com/user-attachments/assets/d474fd2f-fa23-4641-b5b5-e54159162283" />



egrep '(world$)' newfile 
## OUTPUT
<img width="643" height="59" alt="Screenshot from 2025-08-18 11-32-16" src="https://github.com/user-attachments/assets/d65098e3-ee09-46c4-bda8-2d0b50ccce06" />



egrep '(World$)' newfile 
## OUTPUT
<img width="643" height="42" alt="Screenshot from 2025-08-18 11-32-24" src="https://github.com/user-attachments/assets/3478b3fa-90b5-4daa-a935-399536b92fa1" />


egrep '((W|w)orld$)' newfile 
## OUTPUT

<img width="643" height="76" alt="Screenshot from 2025-08-18 11-32-32" src="https://github.com/user-attachments/assets/61e9cdcb-0607-45c3-83c7-8bcecf71b3cc" />


egrep '[1-9]' newfile 
## OUTPUT
<img width="643" height="47" alt="Screenshot from 2025-08-18 11-32-45" src="https://github.com/user-attachments/assets/e65b737e-5c1b-49b9-b4c6-22902a2f8f87" />



egrep 'Linux.*world' newfile 
## OUTPUT
<img width="643" height="45" alt="Screenshot from 2025-08-18 11-32-55" src="https://github.com/user-attachments/assets/a5078bbc-7190-404c-a428-16c4a9c033d5" />


egrep 'Linux.*World' newfile 
## OUTPUT
<img width="643" height="45" alt="Screenshot from 2025-08-18 11-33-01" src="https://github.com/user-attachments/assets/e8fb7c37-186e-414c-a091-8459e128a5f4" />


egrep l{2} newfile
## OUTPUT
<img width="643" height="57" alt="Screenshot from 2025-08-18 11-33-09" src="https://github.com/user-attachments/assets/a22dbf91-0676-41a9-9d66-d489b855f789" />



egrep 's{1,2}' newfile
## OUTPUT 
<img width="643" height="75" alt="Screenshot from 2025-08-18 11-33-16" src="https://github.com/user-attachments/assets/f0a3538e-24a8-4914-b42d-1d62ad9cfed1" />


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
<img width="643" height="46" alt="Screenshot from 2025-08-18 11-45-45" src="https://github.com/user-attachments/assets/01eea23e-2b38-4e42-a3d4-0250fab300b0" />



sed -n -e '$p' file23
## OUTPUT
<img width="643" height="39" alt="Screenshot from 2025-08-18 11-45-54" src="https://github.com/user-attachments/assets/64359668-d6fd-457b-9f17-a49ce6bdbe32" />



sed  -e 's/Ram/Sita/' file23
## OUTPUT
<img width="643" height="169" alt="Screenshot from 2025-08-18 11-46-01" src="https://github.com/user-attachments/assets/2865290b-ab37-434e-8738-6d4cfd81c03c" />



sed  -e '2s/Ram/Sita/' file23
## OUTPUT
<img width="643" height="169" alt="Screenshot from 2025-08-18 11-46-10" src="https://github.com/user-attachments/assets/18748a9c-ac3d-4279-adb1-447a5733cdcd" />



sed  '/tom/s/5000/6000/' file23
## OUTPUT
<img width="643" height="169" alt="Screenshot from 2025-08-18 11-46-16" src="https://github.com/user-attachments/assets/bc4984d3-3ff6-49a6-ac68-f4d0238dd056" />



sed -n -e '1,5p' file23
## OUTPUT

<img width="643" height="113" alt="Screenshot from 2025-08-18 11-46-26" src="https://github.com/user-attachments/assets/3b210678-1494-4519-9c69-b7986d2e7778" />


sed -n -e '2,/Joe/p' file23
## OUTPUT
<img width="643" height="77" alt="Screenshot from 2025-08-18 11-47-09" src="https://github.com/user-attachments/assets/de770e0d-90c9-4d36-8749-b7ee850cd12a" />




sed -n -e '/tom/,/Joe/p' file23
## OUTPUT
<img width="643" height="60" alt="Screenshot from 2025-08-18 11-47-20" src="https://github.com/user-attachments/assets/f430b640-1c02-4d6e-9b71-499855710b79" />



seq 10 
## OUTPUT
<img width="643" height="203" alt="Screenshot from 2025-08-18 11-47-28" src="https://github.com/user-attachments/assets/0b32dbc5-0848-4c19-b5b7-dc97b838f1bc" />



seq 10 | sed -n '4,6p'
## OUTPUT
<img width="643" height="75" alt="Screenshot from 2025-08-18 11-47-40" src="https://github.com/user-attachments/assets/a7d31636-da34-4669-ae29-95e235fa563d" />



seq 10 | sed -n '2,~4p'
## OUTPUT
<img width="643" height="75" alt="Screenshot from 2025-08-18 11-48-02" src="https://github.com/user-attachments/assets/1f7c1b0f-5e9b-4053-8deb-0b0ceb6d590f" />



seq 3 | sed '2a hello'
## OUTPUT
<img width="643" height="94" alt="Screenshot from 2025-08-18 11-48-13" src="https://github.com/user-attachments/assets/85a491b8-562e-4705-96f8-948e5791fd17" />



seq 2 | sed '2i hello'
## OUTPUT
<img width="643" height="83" alt="Screenshot from 2025-08-18 11-48-20" src="https://github.com/user-attachments/assets/b76d42a0-0165-4495-be8b-16b3532682b5" />


seq 10 | sed '2,9c hello'
## OUTPUT
<img width="643" height="80" alt="Screenshot from 2025-08-18 11-48-26" src="https://github.com/user-attachments/assets/30a0beec-40af-4b6b-8abd-28f9e351294e" />


sed -n '2,4{s/^/$/;p}' file23
## OUTPUT
<img width="643" height="90" alt="Screenshot from 2025-08-18 11-48-38" src="https://github.com/user-attachments/assets/73d81c60-ce43-4d41-834e-cd79e0ec47f2" />
<img width="643" height="77" alt="Screenshot from 2025-08-18 11-48-49" src="https://github.com/user-attachments/assets/4cf2e168-d2e3-4e1b-b13e-45fd569cbb2e" />



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
<img width="643" height="93" alt="Screenshot from 2025-08-18 11-51-45" src="https://github.com/user-attachments/assets/6bf49e9b-04fc-45bd-8c87-935e9ae0e114" />


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
<img width="643" height="115" alt="Screenshot from 2025-08-18 11-51-56" src="https://github.com/user-attachments/assets/4894679b-dca0-4d18-94ee-f6dc1ad9ef41" />



#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT
<img width="677" height="166" alt="Screenshot from 2025-08-18 11-52-07" src="https://github.com/user-attachments/assets/ca93b037-563a-49b9-b859-3734039cec13" />

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
<img width="677" height="85" alt="Screenshot from 2025-08-18 11-53-43" src="https://github.com/user-attachments/assets/760d8a4c-857b-4617-bc7a-6c32d30a3101" />


 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT
<img width="728" height="79" alt="Screenshot from 2025-08-18 11-55-31" src="https://github.com/user-attachments/assets/7f4c9c96-96d6-4755-ac8b-9cc33a6b98a1" />



#Backup commands
tar -cvf backup.tar *
## OUTPUT
<img width="863" height="157" alt="Screenshot from 2025-08-19 20-54-56" src="https://github.com/user-attachments/assets/4c790a64-b0e0-4d90-9cf6-7dfe28d90f20" />


mkdir backupdir
 
mv backup.tar backupdir

cd backupdir
 
tar -tvf backup.tar
## OUTPUT
<img width="844" height="204" alt="Screenshot from 2025-08-19 21-03-08" src="https://github.com/user-attachments/assets/0629ac7d-80b0-457d-b634-81de0876589b" />



tar -xvf backup.tar
## OUTPUT
<img width="518" height="200" alt="Screenshot from 2025-08-19 21-07-33" src="https://github.com/user-attachments/assets/3c51ef5b-41fb-469a-bfa6-c26f94c0a26e" />


gzip backup.tar

ls .gz
## OUTPUT
 <img width="518" height="44" alt="Screenshot from 2025-08-19 21-08-54" src="https://github.com/user-attachments/assets/1a95b29f-da69-46b2-af7f-daf352c61d5a" />

gunzip backup.tar.gz
## OUTPUT
<img width="704" height="308" alt="Screenshot from 2025-08-19 21-10-00" src="https://github.com/user-attachments/assets/77e9942f-f9d8-4db9-8696-e247fed38020" />

 
# Shell Script
```
echo '#!/bin/sh' > my-script.sh
echo 'echo Hello World‘; exit 0 >> my-script.sh
```
chmod 755 my-script.sh
./my-script.sh
## OUTPUT
<img width="529" height="48" alt="Screenshot from 2025-08-19 21-16-59" src="https://github.com/user-attachments/assets/8911a329-2edb-4e1b-bee9-ad1fe11ff5a4" />

 
cat << stop > herecheck.txt
```
hello in this world
i cant stop
for this non stop movement
stop
```

cat herecheck.txt
## OUTPUT
<img width="532" height="63" alt="Screenshot from 2025-08-19 21-20-55" src="https://github.com/user-attachments/assets/f95efbc1-c4d3-414e-a3e1-bd531cf272c3" />


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
<img width="571" height="345" alt="Screenshot from 2025-08-19 21-24-36" src="https://github.com/user-attachments/assets/679e99d5-1492-4664-a40a-0dc3826ed024" />

 
ls file1
## OUTPUT
<img width="571" height="49" alt="Screenshot from 2025-08-19 21-26-06" src="https://github.com/user-attachments/assets/cd5b0b3a-164a-4c8f-92be-233b9e00219b" />

echo $?
## OUTPUT 
<img width="571" height="43" alt="Screenshot from 2025-08-19 21-26-20" src="https://github.com/user-attachments/assets/67c17e8d-d98d-49fa-80ea-3da34e4f1bad" />

./one
bash: ./one: Permission denied
 
echo $?
## OUTPUT 
 <img width="571" height="43" alt="Screenshot from 2025-08-19 21-27-19" src="https://github.com/user-attachments/assets/d3cab4fe-cacc-4427-a952-8ff5cb26430c" />

abcd
 
echo $?
 ## OUTPUT
<img width="571" height="43" alt="Screenshot from 2025-08-19 21-27-19" src="https://github.com/user-attachments/assets/6278962e-5be4-42d4-98d9-dc734596dc38" />


 
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

chmod 755 strcomp.sh
 
./strcomp.sh 
## OUTPUT
<img width="571" height="62" alt="Screenshot from 2025-08-19 21-31-19" src="https://github.com/user-attachments/assets/3595c50c-6eb8-48e7-9b3f-12555868f693" />



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
<img width="593" height="61" alt="Screenshot from 2025-08-20 14-06-54" src="https://github.com/user-attachments/assets/036df755-6149-4319-9766-8b6b826a6c1d" />

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
<img width="812" height="114" alt="Screenshot from 2025-08-21 15-56-08" src="https://github.com/user-attachments/assets/36d73493-16ff-413e-a01f-328ceb536307" />



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
<img width="812" height="114" alt="Screenshot from 2025-08-21 15-54-55" src="https://github.com/user-attachments/assets/910f4c78-e5e3-4570-9926-04ebf56fd1cd" />

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
<img width="812" height="114" alt="Screenshot from 2025-08-21 15-56-08" src="https://github.com/user-attachments/assets/464253fc-5b3a-4b71-ae05-5b6f232bcdf8" />

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
<img width="812" height="79" alt="Screenshot from 2025-08-21 15-57-28" src="https://github.com/user-attachments/assets/7f84f6a5-704f-45a4-9f95-778adaab800f" />


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
<img width="812" height="79" alt="Screenshot from 2025-08-21 15-58-26" src="https://github.com/user-attachments/assets/c9d4ac81-3395-4ca6-a53a-d88af6b32553" />

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
 ## output
 <img width="728" height="79" alt="Screenshot from 2025-08-21 16-00-11" src="https://github.com/user-attachments/assets/13d32690-9b12-49de-adbf-bd42598efbf3" />

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
 ## output
 <img width="595" height="133" alt="Screenshot from 2025-08-21 16-02-54" src="https://github.com/user-attachments/assets/5e6e97fe-ab88-4dbe-9a26-79a792792ab8" />

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
 
 ## output
 <img width="595" height="133" alt="Screenshot from 2025-08-21 16-04-01" src="https://github.com/user-attachments/assets/c4575de0-dd99-450a-b717-6fdb3fb8d8f0" />

 
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
<img width="595" height="167" alt="Screenshot from 2025-08-21 16-05-17" src="https://github.com/user-attachments/assets/895156a0-5321-4a64-a2ed-d7336a57fff5" />

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
<img width="595" height="133" alt="Screenshot from 2025-08-21 16-10-31" src="https://github.com/user-attachments/assets/f71dec9c-46e5-4dfa-8bd0-08670fdc9512" />

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
<img width="595" height="133" alt="Screenshot from 2025-08-21 16-12-08" src="https://github.com/user-attachments/assets/05629741-c140-40e5-a762-6bfc4b94e86e" />

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

 <img width="595" height="255" alt="Screenshot from 2025-08-21 16-12-57" src="https://github.com/user-attachments/assets/4cd33f06-9595-47ba-be7c-920f858afa9f" />

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
<img width="595" height="96" alt="Screenshot from 2025-08-21 16-14-47" src="https://github.com/user-attachments/assets/5a1d16e6-70c1-4fed-b710-0291dfd1001a" />


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
<img width="595" height="78" alt="Screenshot from 2025-08-21 16-16-30" src="https://github.com/user-attachments/assets/07d92465-486f-468a-b84c-3831436aeb0e" />


 cat exread1.sh
```bash
#!/bin/bash
# testing the read command
read -p "Enter your name: " name
echo "Hello $name, welcome to my program. “
``` 
$ chmod 755 exread1.sh 

## OUTPUT
<img width="595" height="59" alt="Screenshot from 2025-08-21 16-18-14" src="https://github.com/user-attachments/assets/b95dab42-1bc8-48d0-8559-534f0e222760" />



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

<img width="595" height="59" alt="Screenshot from 2025-08-21 16-19-05" src="https://github.com/user-attachments/assets/bb61588b-f125-47a0-8c4a-0db0f414bd87" />


 ./funcex.sh 

 
 ./funcex.sh 1 2
## output

<img width="595" height="41" alt="Screenshot from 2025-08-21 16-19-26" src="https://github.com/user-attachments/assets/7f063252-0b93-48ec-8a23-7f389727d83e" />
 
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

<img width="595" height="76" alt="Screenshot from 2025-08-21 16-20-23" src="https://github.com/user-attachments/assets/4b97c9bc-d208-4d22-9a0d-ef99203276c9" />

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

<img width="595" height="76" alt="Screenshot from 2025-08-21 16-21-05" src="https://github.com/user-attachments/assets/bc6a99f9-e028-429f-b176-d59e7b0e36b2" />

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

<img width="595" height="291" alt="Screenshot from 2025-08-21 16-21-47" src="https://github.com/user-attachments/assets/737e4070-c183-4100-97fe-0e6748c08b1d" />

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

 <img width="559" height="281" alt="Screenshot from 2025-08-21 22-42-43" src="https://github.com/user-attachments/assets/32a45908-1a41-45e7-9962-1c23c2ff0579" />

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

<img width="599" height="112" alt="Screenshot from 2025-08-21 22-44-13" src="https://github.com/user-attachments/assets/4d6da4f2-3757-44fe-bb60-fb298fe3bf9a" />


# RESULT:
The Commands are executed successfully.

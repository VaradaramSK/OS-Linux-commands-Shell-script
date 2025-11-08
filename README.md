# OS-Linux-commands-Shell-scripting
Operating systems Lab exercise
# Linux commands-Shell scripting
Linux commands-Shell scripting
## Developed By: Varadaram SK
## Reg.NO: 212223040232
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
<img width="257" height="127" alt="image" src="https://github.com/user-attachments/assets/f5ad22c2-0744-48c8-86d6-dcfe845232f1" />



cat < file2

## OUTPUT
cat > file2

<img width="224" height="144" alt="image" src="https://github.com/user-attachments/assets/2002d054-715f-4418-bda1-bcb268939837" />


# Comparing Files
cmp file1 file2
## OUTPUT
 <img width="316" height="139" alt="image" src="https://github.com/user-attachments/assets/34a86adb-68bd-408b-a478-5f4570ba70ef" />


comm file1 file2
 ## OUTPUT
<img width="428" height="245" alt="image" src="https://github.com/user-attachments/assets/97d4034d-af70-47a8-a14b-e6a5ffe596e4" />


 
diff file1 file2
## OUTPUT

<img width="409" height="252" alt="image" src="https://github.com/user-attachments/assets/07cbcaf4-76cd-4513-8743-196ea6933987" />


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
<img width="235" height="103" alt="image" src="https://github.com/user-attachments/assets/23059c75-9996-45cb-b9b9-93e066ebe948" />




cut -d "|" -f 1 file22
## OUTPUT
<img width="326" height="116" alt="image" src="https://github.com/user-attachments/assets/29cc4769-665b-4656-98c3-e46ee2ea92aa" />


cut -d "|" -f 2 file22
## OUTPUT
<img width="325" height="109" alt="image" src="https://github.com/user-attachments/assets/16c5e3b7-3b66-4fcd-84db-c7614d4976ce" />

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
<img width="257" height="71" alt="image" src="https://github.com/user-attachments/assets/2d5c35e4-7b6f-433d-8cb7-8715841df1fd" />



grep hello newfile 
## OUTPUT
<img width="318" height="56" alt="image" src="https://github.com/user-attachments/assets/90fb65c2-55e1-4b58-aac2-150bed42b972" />


grep -v hello newfile 
## OUTPUT
<img width="315" height="70" alt="image" src="https://github.com/user-attachments/assets/ebf14b2b-536c-4a7f-b694-5ca656d85fbf" />


cat newfile | grep -i "hello"
## OUTPUT

<img width="370" height="81" alt="image" src="https://github.com/user-attachments/assets/47767e65-2487-4c4a-a73f-b8c0457d6778" />



cat newfile | grep -i -c "hello"
## OUTPUT
<img width="428" height="70" alt="image" src="https://github.com/user-attachments/assets/54b3a5f0-29a4-4a2d-baf3-4e4ffa20598c" />


grep -R ubuntu /etc


<img width="932" height="603" alt="image" src="https://github.com/user-attachments/assets/35065331-2937-4b9d-8a4b-c9ccb76d9384" />


grep -w -n world newfile   
## OUTPUT
<img width="390" height="81" alt="image" src="https://github.com/user-attachments/assets/09a3bbda-3187-496f-8be9-fce6a0fcfcfe" />


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
<img width="379" height="91" alt="image" src="https://github.com/user-attachments/assets/85407260-c470-4af3-a2f2-51329829cd6a" />



egrep -w '(H|h)ello' newfile 
## OUTPUT
<img width="471" height="81" alt="image" src="https://github.com/user-attachments/assets/2a465a8e-b714-4205-a372-303d4f0795ff" />



egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT
<img width="448" height="81" alt="image" src="https://github.com/user-attachments/assets/98f5aabc-f048-447f-bd7c-f455c2af93c7" />




egrep '(^hello)' newfile 
## OUTPUT
<img width="412" height="56" alt="image" src="https://github.com/user-attachments/assets/065c3133-e2c9-4d50-bc83-57d86bf3b1a3" />


egrep '(world$)' newfile 
## OUTPUT
<img width="401" height="80" alt="image" src="https://github.com/user-attachments/assets/65ed6e74-9790-4539-a67e-a81416f5341b" />



egrep '(World$)' newfile 
## OUTPUT

<img width="414" height="72" alt="image" src="https://github.com/user-attachments/assets/7bc509df-869b-49d2-8f23-8bb6535e7447" />

egrep '((W|w)orld$)' newfile 
## OUTPUT

<img width="391" height="102" alt="image" src="https://github.com/user-attachments/assets/2cfc5fdc-3d40-412c-8c09-8f693e768c54" />


egrep '[1-9]' newfile 
## OUTPUT
<img width="304" height="60" alt="image" src="https://github.com/user-attachments/assets/b06c5a9a-62fe-4b30-a9c2-5a7bb6ba35a7" />


egrep 'Linux.*world' newfile 
## OUTPUT
<img width="324" height="56" alt="image" src="https://github.com/user-attachments/assets/54d3c935-dba5-4399-b2c7-56e6be920697" />


egrep 'Linux.*World' newfile 
## OUTPUT
<img width="345" height="76" alt="image" src="https://github.com/user-attachments/assets/439c2649-63d7-42d2-bf38-759ec62a048a" />



egrep l{2} newfile
## OUTPUT

<img width="269" height="81" alt="image" src="https://github.com/user-attachments/assets/d974b41f-6030-4526-97da-83c9745e1e96" />


egrep 's{1,2}' newfile
## OUTPUT 
<img width="319" height="100" alt="image" src="https://github.com/user-attachments/assets/efa40ff0-4278-4a85-a54b-f56b961dca06" />


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
<img width="305" height="63" alt="image" src="https://github.com/user-attachments/assets/c29e0957-1aa1-4d30-ac94-54aebf8475ae" />



sed -n -e '$p' file23
## OUTPUT
<img width="364" height="71" alt="image" src="https://github.com/user-attachments/assets/58979690-7655-4365-8acb-42e372ce8056" />



sed  -e 's/Ram/Sita/' file23
## OUTPUT
<img width="331" height="193" alt="image" src="https://github.com/user-attachments/assets/14c17d9c-fa17-4528-a81e-a551f86f982a" />



sed  -e '2s/Ram/Sita/' file23
## OUTPUT
<img width="347" height="193" alt="image" src="https://github.com/user-attachments/assets/649b2753-9246-4003-90cc-77e0d45f275a" />


sed  '/tom/s/5000/6000/' file23
## OUTPUT
<img width="346" height="196" alt="image" src="https://github.com/user-attachments/assets/4d6d28ce-8e77-41ef-91d8-aa1b41b2c282" />




sed -n -e '1,5p' file23
## OUTPUT
<img width="342" height="131" alt="image" src="https://github.com/user-attachments/assets/3dc4cc1f-7f89-4d43-a4d2-3c3176383243" />


sed -n -e '2,/Joe/p' file23
## OUTPUT
<img width="383" height="106" alt="image" src="https://github.com/user-attachments/assets/44d1a35a-0361-4800-a12b-516059598fc5" />




sed -n -e '/tom/,/Joe/p' file23
## OUTPUT
<img width="336" height="81" alt="image" src="https://github.com/user-attachments/assets/ff344088-9477-48d8-99ad-1fb2cfa29bfc" />

seq 10 
## OUTPUT

<img width="274" height="220" alt="image" src="https://github.com/user-attachments/assets/dbf44be7-f8c0-4c7c-b0f2-f8eed17a31bc" />


seq 10 | sed -n '4,6p'
## OUTPUT
<img width="294" height="95" alt="image" src="https://github.com/user-attachments/assets/194b01c2-d93c-4424-99e6-02fb1b883ebe" />



seq 10 | sed -n '2,~4p'
## OUTPUT

<img width="295" height="92" alt="image" src="https://github.com/user-attachments/assets/d1c0cd16-e88d-4841-98c8-3ff59979e459" />


seq 3 | sed '2a hello'
## OUTPUT
<img width="258" height="118" alt="image" src="https://github.com/user-attachments/assets/4ee56ba2-156e-42ba-a7dd-7443406df104" />


seq 2 | sed '2i hello'
## OUTPUT
<img width="264" height="90" alt="image" src="https://github.com/user-attachments/assets/a8c69cd9-25e8-4a13-b30b-dbe6d9790b8e" />



seq 10 | sed '2,9c hello'
## OUTPUT

<img width="326" height="89" alt="image" src="https://github.com/user-attachments/assets/89c9bcef-9236-4c34-86d9-fb34a31c72bb" />


sed -n '2,4{s/^/$/;p}' file23
## OUTPUT
<img width="361" height="96" alt="image" src="https://github.com/user-attachments/assets/2ae3e5d6-27a6-45ba-a5f2-1795c09016dd" />

sed -n '2,4{s/$/*/;p}' file23
## OUTPUT
<img width="402" height="104" alt="image" src="https://github.com/user-attachments/assets/0bfb9364-6ec6-4c25-b6c9-e21f32a250a0" />


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
<img width="301" height="133" alt="image" src="https://github.com/user-attachments/assets/ed87e3f7-ca64-484a-8c21-76279c0199a3" />

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
<img width="266" height="129" alt="image" src="https://github.com/user-attachments/assets/12e30a76-cec4-4c94-9a9c-4164347d7f7d" />


#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT
<img width="377" height="191" alt="image" src="https://github.com/user-attachments/assets/77081f45-38de-4a5d-a20a-cb634a46e204" />


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

<img width="298" height="118" alt="image" src="https://github.com/user-attachments/assets/e5a5c71c-d3d8-4718-97d2-d5ad600e2b50" />


 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT
<img width="419" height="108" alt="image" src="https://github.com/user-attachments/assets/9feaa6f2-4a77-4507-b3dc-21557e8b69ac" />



#Backup commands
tar -cvf backup.tar *
## OUTPUT
<img width="570" height="733" alt="image" src="https://github.com/user-attachments/assets/9346e8a9-2116-46a3-bf9b-0a9fb4af4ba0" />




mkdir backupdir
 
mv backup.tar backupdir
 
tar -tvf backup.tar
## OUTPUT
<img width="754" height="444" alt="image" src="https://github.com/user-attachments/assets/b1f3b1cb-e02f-4bed-ad99-5a6940047124" />

tar -xvf backup.tar
## OUTPUT
<img width="412" height="454" alt="image" src="https://github.com/user-attachments/assets/6f383123-8394-4510-8e2e-2132887afd55" />


gzip backup.tar

ls .gz
## OUTPUT
 <img width="274" height="71" alt="image" src="https://github.com/user-attachments/assets/25e15d2e-f4bd-4e6c-8b29-92c6608acbcc" />

gunzip backup.tar.gz
## OUTPUT
<img width="301" height="52" alt="image" src="https://github.com/user-attachments/assets/1941d9bc-d303-40db-841d-cc40dabeb736" />

 
# Shell Script
```
echo '#!/bin/sh' > my-script.sh
echo 'echo Hello World‘; exit 0 >> my-script.sh
```
chmod 755 my-script.sh
./my-script.sh
## OUTPUT
<img width="479" height="118" alt="image" src="https://github.com/user-attachments/assets/deecf525-3538-4dd0-9971-8ebf35f63796" />

 
cat << stop > herecheck.txt



cat herecheck.txt
## OUTPUT
<img width="282" height="90" alt="image" src="https://github.com/user-attachments/assets/62f1a6a0-cac2-4004-8a08-796a18ecdba6" />



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

```
./scriptest.sh: line 1: #!/bin/sh: No such file or directory
“File name is ./scriptest.sh ”
File name is  scriptest.sh
“First arg. is ” 1
“Second arg. is ” 2
“Third arg. is ” 3
“Fourth arg. is ”
The $@ is  1 2 3
The $\# is  1#
The $$ is  14337
    PID TTY          TIME CMD
  13614 pts/1    00:00:00 bash
  14337 pts/1    00:00:00 bash
  14340 pts/1    00:00:00 ps
```

 ls file1
 ## Output
 ```
file1
```
echo $?
## OUTPUT
```
0
```

echo $?
## OUTPUT 
```
1
```
./one bash: ./one: Permission denied
 
echo $?
## OUTPUT 
```
0
```
 
abcd
 
echo $?
 ## OUTPUT
 ```
127
```
 
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

```
baseball is less than hockey
```

chmod 755 strcomp.sh
 
./strcomp.sh 
## OUTPUT
```
You are the owner of the /etc/passwd file

```

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
```
"/root The object exists, is it a file?"
"No,/root it is not a file!"
```


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

```


“/home/sec The object exists, is it a file?”
“No,/home/sec it is not a file!”
“But /home/sec/.bash_history is a file!”

```

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
```
“The test value 10 is greater than 5”
“The values are different”

```



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
```
“/home/sec The object exists, is it a file?”
“No,/home/sec it is not a file!”
“But /home/sec/.bash_history is a file!”

```


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
```
./elifcheck.sh: line 1: #!/bin/bash: No such file or directory
Sorry, you are not allowed here

```

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
```
./ifcompound.sh: line 1: #!/bin/bash: No such file or directory
The file exists and you can write to it
```

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

 ## Output
 ```
Sorry, you are not allowed here
```
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
 ## Output
 ```
10
9
8
7
6
5
4
3
2
1

```
 
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
 $./untiltest.sh 
 ## Output 
 ```
./untiltest.sh: line 1: #using: command not found
100
75
50
25

```
 
 
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

 ## Output
 ```
./forin1.sh: line 1: #!/bin/bash: No such file or directory
./forin1.sh: line 2: #basic: command not found
The next state is Alabama
The next state is Alaska
The next state is Arizona
The next state is Arkansas
The next state is California
The next state is Colorado

```

 
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
 ## Output 
 ```
“word:I”
“word:dont know if thisll”
“word:work”
```
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

## Output 
```
word:I
word:don't
word:know
word:if
word:this'll
word:work

```
 
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
```
The next state is Alabama
The next state is Alaska
The next state is Arizona
The next state is Arkansas
The next state is California
The next state is Colorado
```
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
```
Visit beautiful cities
Visit beautiful cities
Visit beautiful cities
Visit beautiful cities
Visit beautiful cities
Visit beautiful cities
Visit beautiful cities

```
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
```
The value is i is 1
The value is i is 2
The value is i is 3
The value is i is 4
The value is i is 5
```

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
```
1 - 5
2 - 4
3 - 3
4 - 2
5 - 1
```
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
```
Starting loop 1:
 Inside loop: 1
 Inside loop: 2
 Inside loop: 3
Starting Loop 2:
 Inside loop: 1
 Inside loop: 2
 Inside loop: 3
Starting Loop 3:
 Inside loop: 1
 Inside loop: 2
 Inside loop: 3




```
 
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
```
Iteration number: 1
Iteration number: 2
The for loop is completed

```

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
```
Enter your name: Karthikeyan
Hello Karthikeyan, welcome to my program. 

```

 cat exread1.sh
```bash
#!/bin/bash
# testing the read command
read -p "Enter your name: " name
echo "Hello $name, welcome to my program. “
``` 
$ chmod 755 exread1.sh 

## OUTPUT
```
Enter your name: Karthikeyan
Hello Karthikeyan, welcome to my program. 
```


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
```
Usage: badtest1 a b
```
 
 ./funcex.sh 1 2

```
The result is 2
```
 
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
 ```
1
2
3

```
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
```
1
2
3

```
 
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

 ./argshift.sh 1 2 3
 ## OUTPUT
 ```
+ ((  3  ))
+ echo 1 
1
+ shift
+ ((  2  ))
+ echo 2
2
+ shift
+ ((  1  ))
+ echo 3
+ shift
+ ((  0  ))
+ set +x

```
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

```
7         bcdfghj
8	  abcdfghj
7	  bcdfghj
8  	  ebcdfghj
7	  bcdfghhj
8	  ibcdfghj
7	  bcdfghj
8	  obcdfghj
7	  bcdfghj
8 	  ubcdfghj
total characters 75
Number of Lines are 10
No of Words count: 10

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
```
locathost:~# chmod 755 palindrome.sh
locathost:~# ./palindrome.sh
Enter the number
21
Number is NOT palindrome
```
```
locathost:~# chmod 755 palindrome.sh
locathost:~# ./palindrome.sh
Enter the number
33
Number is palindrome
locathost:~#


```
# RESULT:
The Commands are executed successfully.

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
haashika
sinou
haash
sinz
^d
```
cat > file2
```
haashi
sin
haash
sinz
^d
```
### Display the content of the files
cat < file1
## OUTPUT
<img width="541" height="362" alt="image" src="https://github.com/user-attachments/assets/63931cb3-9c16-4b44-9a2d-728e6e43efaa" />




cat < file2
## OUTPUT
<img width="541" height="362" alt="Screenshot from 2025-09-03 20-53-21" src="https://github.com/user-attachments/assets/212166b9-cb1a-47e5-b7fc-6575c26bd3a4" />



# Comparing Files
cmp file1 file2
## OUTPUT
<img width="615" height="58" alt="Screenshot from 2025-09-03 20-57-57" src="https://github.com/user-attachments/assets/1507f041-f041-47e0-ae01-16f62a337a69" />

 
comm file1 file2
 ## OUTPUT
 <img width="653" height="249" alt="Screenshot from 2025-09-03 20-58-28" src="https://github.com/user-attachments/assets/f3a8b5e3-f94d-4812-b9b5-ca91a270b676" />


 
diff file1 file2
## OUTPUT

<img width="647" height="161" alt="Screenshot from 2025-09-03 20-59-02" src="https://github.com/user-attachments/assets/1c7ba2df-4808-4829-a90a-b4abf4358259" />


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
<img width="707" height="438" alt="Screenshot from 2025-09-03 21-02-50" src="https://github.com/user-attachments/assets/2d2114fd-8a97-4d94-9087-24339792b719" />




cut -d "|" -f 1 file22
## OUTPUT

<img width="707" height="438" alt="Screenshot from 2025-09-03 21-02-50" src="https://github.com/user-attachments/assets/0acf0bd5-a7ec-4616-a22e-955b713452a8" />


cut -d "|" -f 2 file22
## OUTPUT

<img width="707" height="438" alt="Screenshot from 2025-09-03 21-02-50" src="https://github.com/user-attachments/assets/4266ffab-227b-46a6-9211-d5e1e7fd1b5e" />

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
<img width="796" height="77" alt="Screenshot from 2025-09-03 21-10-13" src="https://github.com/user-attachments/assets/9af1edc5-5522-45c0-9387-be2244de44a3" />



grep hello newfile 
## OUTPUT
<img width="796" height="77" alt="Screenshot from 2025-09-03 21-10-48" src="https://github.com/user-attachments/assets/d5ccd63b-3734-4259-97d7-e882717f63ea" />




grep -v hello newfile 
## OUTPUT

<img width="796" height="77" alt="Screenshot from 2025-09-03 21-11-24" src="https://github.com/user-attachments/assets/1fa9dcb0-4d4f-4060-9bad-e12737baf6a8" />



cat newfile | grep -i "hello"
## OUTPUT


<img width="796" height="77" alt="image" src="https://github.com/user-attachments/assets/e61b2e7e-4678-431b-9dff-d9fb51b310ad" />


cat newfile | grep -i -c "hello"
## OUTPUT
<img width="785" height="55" alt="image" src="https://github.com/user-attachments/assets/94b62645-c75a-4ccd-8898-a5b6042286fc" />




grep -R ubuntu /etc
## OUTPUT
<img width="976" height="358" alt="image" src="https://github.com/user-attachments/assets/5d755c2a-c63f-4582-a08d-86e33c6e7837" />

<img width="964" height="253" alt="image" src="https://github.com/user-attachments/assets/725cdf49-27b1-4973-b9e3-9b19f9d097e2" />


grep -w -n world newfile   
## OUTPUT
<img width="964" height="84" alt="image" src="https://github.com/user-attachments/assets/a9adb362-4d1e-47de-88e7-9a997de75c1d" />



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
<img width="964" height="84" alt="image" src="https://github.com/user-attachments/assets/85d9f37e-88c0-4fba-9928-56b6899aebb9" />



egrep -w '(H|h)ello' newfile 
## OUTPUT

<img width="964" height="84" alt="image" src="https://github.com/user-attachments/assets/c43afeba-cf13-463f-b30d-1df204adfd5f" />


egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT


<img width="964" height="84" alt="image" src="https://github.com/user-attachments/assets/0a7c6fa0-c704-4c4a-becc-62cc715c2fea" />


egrep '(^hello)' newfile 
## OUTPUT
<img width="846" height="54" alt="image" src="https://github.com/user-attachments/assets/1065f89b-6b74-4376-bc27-40017c041fe5" />



egrep '(world$)' newfile 
## OUTPUT

<img width="846" height="73" alt="image" src="https://github.com/user-attachments/assets/375a1472-0bcb-44d7-8b6a-907cbe4f1cfd" />


egrep '(World$)' newfile 
## OUTPUT

<img width="846" height="73" alt="image" src="https://github.com/user-attachments/assets/cad2a69a-7a68-449c-8746-14e4ee406486" />

egrep '((W|w)orld$)' newfile 
## OUTPUT
<img width="846" height="73" alt="image" src="https://github.com/user-attachments/assets/e49ecd82-0efd-4d02-afb5-9e1e076cbe8f" />



egrep '[1-9]' newfile 
## OUTPUT
<img width="846" height="73" alt="image" src="https://github.com/user-attachments/assets/165b95a4-242a-4547-b3cb-44738ba14741" />



egrep 'Linux.*world' newfile 
## OUTPUT
<img width="846" height="73" alt="image" src="https://github.com/user-attachments/assets/6c1d418e-b02e-492c-9357-2ee82773b390" />


egrep 'Linux.*World' newfile 
## OUTPUT

<img width="846" height="73" alt="image" src="https://github.com/user-attachments/assets/f703926c-4c09-4ad7-8715-d7c7589cd634" />

egrep l{2} newfile
## OUTPUT
<img width="846" height="73" alt="image" src="https://github.com/user-attachments/assets/45ba11ae-fc42-48dd-a030-7c9197441797" />



egrep 's{1,2}' newfile
## OUTPUT 
<img width="846" height="93" alt="image" src="https://github.com/user-attachments/assets/5c6abecb-c273-457f-9524-9ac1f244c5de" />


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

<img width="831" height="53" alt="image" src="https://github.com/user-attachments/assets/6424f964-e661-43b9-b6b0-8300395a9e4e" />


sed -n -e '$p' file23
## OUTPUT

<img width="831" height="53" alt="image" src="https://github.com/user-attachments/assets/7994a48c-0fcc-40eb-93d3-2dc6125a9938" />


sed  -e 's/Ram/Sita/' file23
## OUTPUT
<img width="866" height="209" alt="image" src="https://github.com/user-attachments/assets/5d31ff16-84a9-48a8-ae85-3bb3af39d879" />



sed  -e '2s/Ram/Sita/' file23
## OUTPUT

<img width="866" height="209" alt="image" src="https://github.com/user-attachments/assets/c922c420-8b9a-4d28-8269-a6c603a2394e" />


sed  '/tom/s/5000/6000/' file23
## OUTPUT

<img width="866" height="209" alt="image" src="https://github.com/user-attachments/assets/b4292489-4242-46a9-9b46-c14b1ea4a12c" />


sed -n -e '1,5p' file23
## OUTPUT

<img width="866" height="136" alt="image" src="https://github.com/user-attachments/assets/12dd88b7-bd08-473c-be3a-d2ef79a782d4" />


sed -n -e '2,/Joe/p' file23
## OUTPUT

<img width="866" height="136" alt="image" src="https://github.com/user-attachments/assets/804d61e4-99f7-4264-86d1-e5224ee18824" />



sed -n -e '/tom/,/Joe/p' file23
## OUTPUT


<img width="866" height="73" alt="image" src="https://github.com/user-attachments/assets/adcdd4f6-171b-48fd-97e2-724564b1f8d8" />

seq 10 
## OUTPUT
<img width="706" height="251" alt="image" src="https://github.com/user-attachments/assets/4ba6fa6f-9e8c-4548-a796-075b88c9dfdf" />



seq 10 | sed -n '4,6p'
## OUTPUT

<img width="706" height="110" alt="image" src="https://github.com/user-attachments/assets/f2d85569-15fd-4d44-8cb0-23a87a57ee2a" />


seq 10 | sed -n '2,~4p'
## OUTPUT

<img width="706" height="110" alt="image" src="https://github.com/user-attachments/assets/26f33cb8-82c5-41d1-86ee-c49145da3f9e" />


seq 3 | sed '2a hello'
## OUTPUT

<img width="706" height="110" alt="image" src="https://github.com/user-attachments/assets/3ac76523-5be6-4322-8175-8eea9d1807aa" />


seq 2 | sed '2i hello'
## OUTPUT
<img width="706" height="110" alt="image" src="https://github.com/user-attachments/assets/940c5f69-6212-49d5-aac7-7b111035f0a5" />


seq 10 | sed '2,9c hello'
## OUTPUT
<img width="706" height="110" alt="image" src="https://github.com/user-attachments/assets/0d19d1a6-2a8a-491a-9b7a-be7984db4c2e" />


sed -n '2,4{s/^/$/;p}' file23
## OUTPUT

<img width="745" height="110" alt="image" src="https://github.com/user-attachments/assets/c8b2b055-c8d2-42f9-a81e-8a9dd0569355" />




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
<img width="745" height="295" alt="image" src="https://github.com/user-attachments/assets/8d2a3b34-710c-497e-880c-f7111d234b64" />


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
<img width="745" height="322" alt="image" src="https://github.com/user-attachments/assets/c3f9d61a-268b-4dd7-8c76-c6c3ce727eb6" />



#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT
<img width="819" height="248" alt="image" src="https://github.com/user-attachments/assets/1d339b41-c9fb-476a-beba-1e97e61bc812" />

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
<img width="864" height="106" alt="image" src="https://github.com/user-attachments/assets/ec270eea-fcb1-435e-9111-e7e11fc1b8f2" />


 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT

<img width="864" height="106" alt="image" src="https://github.com/user-attachments/assets/006a4000-9459-4b96-b90d-46c918e5b02d" />


#Backup commands
tar -cvf backup.tar *
## OUTPUT
<img width="953" height="106" alt="image" src="https://github.com/user-attachments/assets/9a069b65-1eee-481f-b756-37ae73a72d18" />


mkdir backupdir
 
mv backup.tar backupdir

cd backupdir
 
tar -tvf backup.tar
## OUTPUT

<img width="867" height="152" alt="image" src="https://github.com/user-attachments/assets/c45a5985-3a6f-491f-b365-6516dc4ec196" />

tar -xvf backup.tar
## OUTPUT
<img width="867" height="152" alt="image" src="https://github.com/user-attachments/assets/6b63571c-99a4-4512-93af-1c9aa944436b" />

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

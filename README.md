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
![1](https://github.com/user-attachments/assets/2d945e19-3d40-40d4-b83b-8e33f67bd443)



cat < file2
## OUTPUT
![2](https://github.com/user-attachments/assets/4448ecf1-5853-49a2-9c10-29b707815fdf)


# Comparing Files
cmp file1 file2
## OUTPUT
![3](https://github.com/user-attachments/assets/4ca83c6f-b70b-4185-9959-87bfa1120442)

comm file1 file2
 ## OUTPUT
![4](https://github.com/user-attachments/assets/416ad956-1b4a-4071-a4fb-64cec969f9e7)

 
diff file1 file2
## OUTPUT
![5](https://github.com/user-attachments/assets/7fb9d078-a66a-4c6b-aefb-522668ffe274)



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

![6](https://github.com/user-attachments/assets/bd43497e-8141-44e0-862a-7476218a981f)



cut -d "|" -f 1 file22
## OUTPUT

![7](https://github.com/user-attachments/assets/4f2a5ba2-0a65-41bf-aba6-4c9c66ca27a6)


cut -d "|" -f 2 file22
## OUTPUT

![8](https://github.com/user-attachments/assets/b45162e1-fcf0-4b35-a841-59fb0606e939)

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

![9](https://github.com/user-attachments/assets/14d83f82-93d4-4ba5-9b5d-8b888381091b)


grep hello newfile 
## OUTPUT

![10](https://github.com/user-attachments/assets/668b18a3-6425-4403-8477-f2deddad6e92)



grep -v hello newfile 
## OUTPUT

![11](https://github.com/user-attachments/assets/3610e76a-25a7-41ef-a256-315de8286f69)


cat newfile | grep -i "hello"
## OUTPUT

![12](https://github.com/user-attachments/assets/227c0a9c-0ead-4427-944c-aa13325f1e70)



cat newfile | grep -i -c "hello"
## OUTPUT

![13](https://github.com/user-attachments/assets/7679c51c-dab9-4042-b561-88752df23824)



grep -R ubuntu /etc
## OUTPUT

![14](https://github.com/user-attachments/assets/e6c5e1e3-c80c-4837-83b1-1c55cba41b62)


grep -w -n world newfile   
## OUTPUT
![15](https://github.com/user-attachments/assets/de7b3444-5dc7-4499-8b05-33b6674e4e5c)


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

![16](https://github.com/user-attachments/assets/0c12c023-fa7a-4c6d-8158-0de96c385aa4)


egrep -w '(H|h)ello' newfile 
## OUTPUT

![17](https://github.com/user-attachments/assets/c47a7d06-e123-47c9-8270-a9bc6db25b72)


egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT

![18](https://github.com/user-attachments/assets/546dd8d7-d4c8-48d0-872c-7e0cc1287291)



egrep '(^hello)' newfile 
## OUTPUT

![19](https://github.com/user-attachments/assets/e61f89c3-2dbe-4af3-abf9-510547560232)


egrep '(world$)' newfile 
## OUTPUT

![20](https://github.com/user-attachments/assets/8d82b919-ddbf-4eeb-aa4e-984b6bd0eef7)


egrep '(World$)' newfile 
## OUTPUT
![21](https://github.com/user-attachments/assets/d1c4e4f2-5c6f-474a-a627-5a496a162ef2)


egrep '((W|w)orld$)' newfile 
## OUTPUT

![22](https://github.com/user-attachments/assets/f4182131-70f2-462a-b832-eeec706185db)


egrep '[1-9]' newfile 
## OUTPUT

![23](https://github.com/user-attachments/assets/73822756-610d-4161-86c2-3aaa6ef3a4f9)


egrep 'Linux.*world' newfile 
## OUTPUT

![24](https://github.com/user-attachments/assets/b6bced43-056d-4f0a-924c-f88340a954ee)

egrep 'Linux.*World' newfile 
## OUTPUT
![Screenshot 2025-05-11 133647](https://github.com/user-attachments/assets/1b07074c-34bb-42c3-be3e-775291b9e1f6)


egrep l{2} newfile
## OUTPUT

![Screenshot 2025-05-11 133658](https://github.com/user-attachments/assets/153d0f01-965e-404f-ae86-13c80a8a125c)


egrep 's{1,2}' newfile
## OUTPUT 
![Screenshot 2025-05-11 133706](https://github.com/user-attachments/assets/f88e84b3-33a9-45c5-98f6-d44d310a81c0)


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

![Screenshot 2025-05-11 133727](https://github.com/user-attachments/assets/16da5512-bbbe-4f30-862f-f993785f170e)


sed -n -e '$p' file23
## OUTPUT

![Screenshot 2025-05-11 133739](https://github.com/user-attachments/assets/fa137cbf-5a05-4699-a778-76f725459617)


sed  -e 's/Ram/Sita/' file23
## OUTPUT
![Screenshot 2025-05-11 133753](https://github.com/user-attachments/assets/5562f8f4-f06b-45d5-b451-51a17f44c4f3)



sed  -e '2s/Ram/Sita/' file23
## OUTPUT

![Screenshot 2025-05-11 133803](https://github.com/user-attachments/assets/188aa00d-35ce-4d34-9d55-4fabd4ba1ae0)


sed  '/tom/s/5000/6000/' file23
## OUTPUT

![Screenshot 2025-05-11 133816](https://github.com/user-attachments/assets/64f56a6b-5344-405c-af4d-494d1de951d2)


sed -n -e '1,5p' file23
## OUTPUT

![Screenshot 2025-05-11 133826](https://github.com/user-attachments/assets/d73c4e09-2a51-492a-a386-f14f12de1297)


sed -n -e '2,/Joe/p' file23
## OUTPUT

![Screenshot 2025-05-11 133837](https://github.com/user-attachments/assets/55fed57a-b100-4f8e-aa4a-1364f03a9ae3)



sed -n -e '/tom/,/Joe/p' file23
## OUTPUT

![Screenshot 2025-05-11 133848](https://github.com/user-attachments/assets/d5e3fcf2-98c3-4a95-8b6d-00899d1985dd)


seq 10 
## OUTPUT

![Screenshot 2025-05-11 133859](https://github.com/user-attachments/assets/964561ad-34ab-4d37-b894-f560ab3941b7)


seq 10 | sed -n '4,6p'
## OUTPUT

![Screenshot 2025-05-11 133909](https://github.com/user-attachments/assets/c3cb1752-15e9-4146-b059-16f60f8ae186)


seq 10 | sed -n '2,~4p'
## OUTPUT
![Screenshot 2025-05-11 133931](https://github.com/user-attachments/assets/a72526af-4bf6-4be8-bc08-a6e34b83284d)



seq 3 | sed '2a hello'
## OUTPUT
![Screenshot 2025-05-11 133943](https://github.com/user-attachments/assets/877a39ca-14b4-4674-a68f-068a6389d9b0)



seq 2 | sed '2i hello'
## OUTPUT
![Screenshot 2025-05-11 134008](https://github.com/user-attachments/assets/25184c08-413b-446c-a2a1-522f3b01b466)


seq 10 | sed '2,9c hello'
## OUTPUT
![Screenshot 2025-05-11 134027](https://github.com/user-attachments/assets/153bd5e8-d43a-4968-9551-aec8dd0fb5f0)


sed -n '2,4{s/^/$/;p}' file23
## OUTPUT

![Screenshot 2025-05-11 134047](https://github.com/user-attachments/assets/3aa51b8d-5a0e-49c4-a490-90fd841c5516)


sed -n '2,4{s/$/*/;p}' file23

![Screenshot 2025-05-11 134057](https://github.com/user-attachments/assets/27ba38e3-69e4-4c6e-9a84-4e8ebe80aa42)

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
![Screenshot 2025-05-11 134109](https://github.com/user-attachments/assets/51fe3072-b9f4-4fd3-95ce-920849c63df3)


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

![Screenshot 2025-05-11 134154](https://github.com/user-attachments/assets/a3f93af6-8bce-490b-8491-26937051ba40)


#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT
![Screenshot 2025-05-11 134236](https://github.com/user-attachments/assets/a818aa25-6c2b-4dfb-9031-1050b03e0ae1)

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

![Screenshot 2025-05-11 134250](https://github.com/user-attachments/assets/2b7285ea-32e9-48ac-9b7b-536b1368fc57)

 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT

![Screenshot 2025-05-11 134258](https://github.com/user-attachments/assets/039101ed-1eff-47f1-8bab-6d477d9ddbf4)


#Backup commands
tar -cvf backup.tar *
## OUTPUT

![Screenshot 2025-05-11 134307](https://github.com/user-attachments/assets/aab34f7b-8681-4dc3-9b72-a2fdbdc46799)

mkdir backupdir
 
mv backup.tar backupdir

cd backupdir
 
tar -tvf backup.tar
## OUTPUT
![Screenshot 2025-05-11 134327](https://github.com/user-attachments/assets/96f4d308-dd33-4e45-9249-8497174e7d55)


tar -xvf backup.tar
## OUTPUT
![Screenshot 2025-05-11 134339](https://github.com/user-attachments/assets/a0561dd2-60c5-4cc5-873d-aa6a856acd4e)

gzip backup.tar

ls .gz
## OUTPUT
![Screenshot 2025-05-11 134350](https://github.com/user-attachments/assets/e71c32cd-c7e5-4d27-bf6f-9ef36a6e6e13)

gunzip backup.tar.gz
## OUTPUT
![Screenshot 2025-05-11 134359](https://github.com/user-attachments/assets/8ba3d08b-b184-48b9-919c-e1181f2c5372)

 
# Shell Script
```
echo '#!/bin/sh' > my-script.sh
echo 'echo Hello World‘; exit 0 >> my-script.sh
```
chmod 755 my-script.sh
./my-script.sh
## OUTPUT
![Screenshot 2025-05-11 134505](https://github.com/user-attachments/assets/3b9d8ab1-b3d5-4962-97c4-e4488394b1b1)

cat << stop > herecheck.txt
```
hello in this world
i cant stop
for this non stop movement
stop
```

cat herecheck.txt
## OUTPUT
![Screenshot 2025-05-11 134531](https://github.com/user-attachments/assets/a46207e4-6b28-40a3-99e3-370be55548f1)


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
![Screenshot 2025-05-11 134540](https://github.com/user-attachments/assets/66df0993-3215-420b-981b-d864a158b4ef)

 
ls file1
## OUTPUT

![Screenshot 2025-05-11 134548](https://github.com/user-attachments/assets/121e891e-be00-4b52-a543-506d2eda7b2e)

echo $?
## OUTPUT 
./one
bash: ./one: Permission denied

![Screenshot 2025-05-11 134618](https://github.com/user-attachments/assets/ab412cd9-7af6-48be-b36d-151dd8111f9d)

echo $?
## OUTPUT 
 abcd

![Screenshot 2025-05-11 134647](https://github.com/user-attachments/assets/1b1659b0-e784-4dea-a9d3-ab01095335f0)



 
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

![Screenshot 2025-05-11 134709](https://github.com/user-attachments/assets/3f24b938-f4e6-494b-8664-5218a6f6ac67)


chmod 755 strcomp.sh
 
./strcomp.sh 
## OUTPUT
![Screenshot 2025-05-11 134719](https://github.com/user-attachments/assets/16bc9691-8177-4770-be46-2bac220707ec)

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
![Screenshot 2025-05-11 134746](https://github.com/user-attachments/assets/a90472da-ad8d-4e82-a0e5-11d4f224172a)




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


![Screenshot 2025-05-11 134907](https://github.com/user-attachments/assets/708c2785-d422-44a1-8604-81c1fff7cbde)


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


![Screenshot 2025-05-11 134927](https://github.com/user-attachments/assets/ee275588-bb34-4d9b-b128-1b635da8ef90)

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

![Screenshot 2025-05-11 134939](https://github.com/user-attachments/assets/f8328ca3-f228-4368-8e37-ab928bfc2c0e)




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


![Screenshot 2025-05-11 134953](https://github.com/user-attachments/assets/6790c073-5faf-42df-b4d5-d3f2f28c9648)


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


![Screenshot 2025-05-11 135023](https://github.com/user-attachments/assets/81d42c4c-09b2-4715-b1c5-806d7e6698a7)



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


![Screenshot 2025-05-11 135040](https://github.com/user-attachments/assets/6bfa903c-509a-4843-a5ca-2ca374ae9c57)

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



![Screenshot 2025-05-11 135058](https://github.com/user-attachments/assets/471e421a-4574-45ab-801c-f85d40ca88d0)

 
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



![Screenshot 2025-05-11 135135](https://github.com/user-attachments/assets/90d55d19-01f7-4573-b42d-c7d009af67cd)

 
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



![Screenshot 2025-05-11 135213](https://github.com/user-attachments/assets/3d803e25-8928-49f7-badb-744af9d78164)

 
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


![Screenshot 2025-05-11 135224](https://github.com/user-attachments/assets/56fec994-5797-411f-a55c-4fff5668780c)

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



![Screenshot 2025-05-11 135233](https://github.com/user-attachments/assets/da7f8a6b-2eeb-464a-93f2-9df082535973)

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



![Screenshot 2025-05-11 140810](https://github.com/user-attachments/assets/e186a905-4ae2-49e3-a840-01a8b2ac52dc)

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



![Screenshot 2025-05-11 140826](https://github.com/user-attachments/assets/78f1afd4-7fcd-4c76-8055-2e3874dfbafe)

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



![Screenshot 2025-05-11 140900](https://github.com/user-attachments/assets/0312ad7f-ecc8-449d-8298-796b5e4bf732)

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



![Screenshot 2025-05-11 145614](https://github.com/user-attachments/assets/29df7f04-d1b7-4db1-acec-e821afdd28e9)

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

![Screenshot 2025-05-11 140931](https://github.com/user-attachments/assets/431b33c5-6b0e-4658-b779-b568da1f47da)




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

![Screenshot 2025-05-11 140942](https://github.com/user-attachments/assets/5e66e787-691f-4d4d-ae9a-ffd5788a71c3)

 cat exread1.sh
```bash
#!/bin/bash
# testing the read command
read -p "Enter your name: " name
echo "Hello $name, welcome to my program. “
``` 
$ chmod 755 exread1.sh 

## OUTPUT

![Screenshot 2025-05-11 140953](https://github.com/user-attachments/assets/4440e9c7-213e-4e95-a5d9-7673b2d16e0e)


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


![Screenshot 2025-05-11 141047](https://github.com/user-attachments/assets/eb4e9d93-e51e-4a7a-beac-ca5fed8ed1cb)



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



![Screenshot 2025-05-11 141101](https://github.com/user-attachments/assets/86a96528-0b31-41b8-97de-8bb9f51545b6)

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


![Screenshot 2025-05-11 141113](https://github.com/user-attachments/assets/86a50bdb-210d-4329-b2c0-c5bf575d5499)


# RESULT:
The Commands are executed successfully.

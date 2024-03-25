**OS-Linux-commands-Shell-scripting
Operating systems Lab exercise
Linux commands-Shell scripting
Linux commands-Shell scripting
AIM:**
To practice Linux Commands and Shell Scripting

**DESIGN STEPS:
Step 1:**
Navigate to any Linux environment installed on the system or installed inside a virtual environment like virtual box/vmware or online linux JSLinux (https://bellard.org/jslinux/vm.html?url=alpine-x86.cfg&mem=192) or docker.

**Step 2:**
Execute the following commands

**Step 3:**
Testing the commands for the desired output.

**COMMANDS:
Create the following files file1, file2 as follows:**
cat > file1

chanchal singhvi c.k. shukla s.n. dasgupta sumit chakrobarty ^d

cat > file2

anil aggarwal barun sengupta c.k. shukla lalit chowdury s.n. dasgupta ^d

**Display the content of the files**
cat < file1

OUTPUT chanchal singhvi c.k. shukla s.n. dasgupta sumit chakrobarty ^d

cat < file2

OUTPUT cat > file2

anil aggarwal barun sengupta c.k. shukla lalit chowdury s.n. dasgupta ^d

**Comparing Files**
cmp file1 file2

**OUTPUT**

![image](https://github.com/greffinaprem/OS-Linux-commands-Shell-script/assets/119475603/d73284a9-3d35-4285-a3eb-8f7f66d8dc51)


comm file1 file2
**OUTPUT**

![image](https://github.com/greffinaprem/OS-Linux-commands-Shell-script/assets/119475603/166c2dd4-ec88-4cf5-bdbc-d28c13c87fed)


diff file1 file2

![image](https://github.com/greffinaprem/OS-Linux-commands-Shell-script/assets/119475603/8a6c1e55-7ce2-4454-aa41-f8a5abba4b72)


#Filters

**Create the following files file11, file22 as follows:**
cat > file11

Hello world This is my world ^d

cat > file22

1001 | Ram | 10000 | HR 1002 | tom | 5000 | Admin 1003 | Joe | 7000 | Developer ^d

cut -c1-3 file11

**OUTPUT**

![image](https://github.com/greffinaprem/OS-Linux-commands-Shell-script/assets/119475603/27c5fad3-70c1-4b5e-8ef7-f5e99f330f0e)


cut -d "|" -f 1 file22

**OUTPUT**

![image](https://github.com/greffinaprem/OS-Linux-commands-Shell-script/assets/119475603/da933c29-a136-4eb0-b86c-57a69fb53ad0)


cut -d "|" -f 2 file22

**OUTPUT**

![image](https://github.com/greffinaprem/OS-Linux-commands-Shell-script/assets/119475603/e017ee8d-87bc-47b7-849a-cad76cede1f3)


cat < newfile

Hello world hello world ^d ` cat > newfile Hello world hello world

grep Hello newfile

OUTPUT

![image](https://github.com/greffinaprem/OS-Linux-commands-Shell-script/assets/119475603/1c361e71-d5f0-46a2-b4fe-2db6542f3708)


grep hello newfile

![image](https://github.com/greffinaprem/OS-Linux-commands-Shell-script/assets/119475603/0e57b9d0-f7ad-47ab-a05f-e8f0c168f6cf)


grep -v hello newfile

OUTPUT

![image](https://github.com/greffinaprem/OS-Linux-commands-Shell-script/assets/119475603/918c77da-840b-426a-b3c0-5f4845a9fd71)


cat newfile | grep -i "hello"

OUTPUT

![image](https://github.com/greffinaprem/OS-Linux-commands-Shell-script/assets/119475603/b47f3a56-f45f-4e88-b434-717824a8dff8)


cat newfile | grep -i -c "hello"

OUTPUT

![image](https://github.com/greffinaprem/OS-Linux-commands-Shell-script/assets/119475603/0277c6f3-8934-409b-8119-1ccf0438ef99)


grep -R ubuntu /etc

OUTPUT
grep -w -n world newfile

OUTPUT

![image](https://github.com/greffinaprem/OS-Linux-commands-Shell-script/assets/119475603/9be17fdf-f54d-48aa-9284-a7d2bef78a17)


cat < newfile

Hello world hello world Linux is world number 1 Unix is predecessor Linux is best in this World ^d

cat > newfile

Hello world hello world Linux is world number 1 Unix is predecessor Linux is best in this World ^d

egrep -w 'Hello|hello' newfile

OUTPUT

![image](https://github.com/greffinaprem/OS-Linux-commands-Shell-script/assets/119475603/95412f1f-d4aa-4fb6-a951-8a399de6f8de)


egrep -w '(H|h)ello' newfile

OUTPUT

![image](https://github.com/greffinaprem/OS-Linux-commands-Shell-script/assets/119475603/6993939a-083d-4e39-b4c1-8476fb13fefd)


egrep -w '(H|h)ell[a-z]' newfile

OUTPUT

![image](https://github.com/greffinaprem/OS-Linux-commands-Shell-script/assets/119475603/51ef3445-6188-4813-ab05-71f744b143f7)


egrep '(^hello)' newfile

OUTPUT

![image](https://github.com/greffinaprem/OS-Linux-commands-Shell-script/assets/119475603/25c8e983-ab19-4598-8355-ef49e453c62f)


egrep '(world$)' newfile

OUTPUT

![image](https://github.com/greffinaprem/OS-Linux-commands-Shell-script/assets/119475603/222387be-7270-4f96-b305-d610f444c61f)


egrep '(World$)' newfile

OUTPUT

![image](https://github.com/greffinaprem/OS-Linux-commands-Shell-script/assets/119475603/3dcbbdb7-312c-4d01-a246-4b5eede1f781)


egrep '((W|w)orld$)' newfile

OUTPUT

![image](https://github.com/greffinaprem/OS-Linux-commands-Shell-script/assets/119475603/4d34c81f-9bd9-44ef-aa0f-a1a0475f54aa)


egrep '[1-9]' newfile

OUTPUT

![image](https://github.com/greffinaprem/OS-Linux-commands-Shell-script/assets/119475603/7b038a43-22d1-4bc6-80f0-08d528cfd888)


egrep 'Linux.*world' newfile

OUTPUT

![image](https://github.com/greffinaprem/OS-Linux-commands-Shell-script/assets/119475603/5c0a7d22-d318-4be0-a13f-c73b0ef967f0)


egrep 'Linux.*World' newfile

OUTPUT

![image](https://github.com/greffinaprem/OS-Linux-commands-Shell-script/assets/119475603/d7ec8611-ed0a-4585-841a-709199cbcad2)


egrep l{2} newfile

OUTPUT

![image](https://github.com/greffinaprem/OS-Linux-commands-Shell-script/assets/119475603/20846880-51ab-4654-9c9d-97b2d30bd868)


egrep 's{1,2}' newfile

OUTPUT

![image](https://github.com/greffinaprem/OS-Linux-commands-Shell-script/assets/119475603/4be46925-f31d-404a-b6ab-307108844d46)


cat > file23

1001 | Ram | 10000 | HR 1001 | Ram | 10000 | HR 1002 | tom | 5000 | Admin 1003 | Joe | 7000 | Developer 1005 | Sam | 5000 | HR 1004 | Sit | 7000 | Dev 1003 | Joe | 7000 | Developer 1001 | Ram | 10000 | HR ^d

sed -n -e '3p' file23

OUTPUT

![image](https://github.com/greffinaprem/OS-Linux-commands-Shell-script/assets/119475603/5986b6b1-da27-47bf-a9fa-fa8d39c63e09)


sed -n -e '$p' file23

OUTPUT sed -e 's/Ram/Sita/' file23

OUTPUT

![image](https://github.com/greffinaprem/OS-Linux-commands-Shell-script/assets/119475603/8aafea15-5913-4207-8ab5-25bdc57fe487)


sed -e '2s/Ram/Sita/' file23

OUTPUT

![image](https://github.com/greffinaprem/OS-Linux-commands-Shell-script/assets/119475603/9d5b0bbe-a46b-4aba-b5a3-eea915a8768f)


sed '/tom/s/5000/6000/' file23

OUTPUT

![image](https://github.com/greffinaprem/OS-Linux-commands-Shell-script/assets/119475603/3fc5da3a-8892-48b0-b582-8baafca0d809)


sed -n -e '1,5p' file23

OUTPUT

![image](https://github.com/greffinaprem/OS-Linux-commands-Shell-script/assets/119475603/8d30ef76-c09d-40d3-b7c1-2249fa6561f9)


sed -n -e '2,/Joe/p' file23

OUTPUT

![image](https://github.com/greffinaprem/OS-Linux-commands-Shell-script/assets/119475603/03965757-40a3-462d-80a0-de0488e295d5)


sed -n -e '/tom/,/Joe/p' file23

OUTPUT

![image](https://github.com/greffinaprem/OS-Linux-commands-Shell-script/assets/119475603/8c275d43-1a53-4b87-984a-0a1292397854)


seq 10

OUTPUT

![image](https://github.com/greffinaprem/OS-Linux-commands-Shell-script/assets/119475603/ca7ee09d-c845-4ae5-ab5e-dfc58bdee233)


seq 10 | sed -n '4,6p'

OUTPUT

![image](https://github.com/greffinaprem/OS-Linux-commands-Shell-script/assets/119475603/4c28ed41-28c0-4201-a5a2-d0170a662c9a)


seq 10 | sed -n '2,~4p'

OUTPUT

![image](https://github.com/greffinaprem/OS-Linux-commands-Shell-script/assets/119475603/b224d5c1-d851-4078-8227-bc40957d07e1)


seq 3 | sed '2a hello'

OUTPUT

![image](https://github.com/greffinaprem/OS-Linux-commands-Shell-script/assets/119475603/3a9feb08-8f68-40f4-a302-5c8c8c8050d7)


seq 2 | sed '2i hello' ##OUTPUT 304768296-37f79adc-6b21-4499-bbfa-d74aeae1461a

seq 10 | sed '2,9c hello'

OUTPUT

![image](https://github.com/greffinaprem/OS-Linux-commands-Shell-script/assets/119475603/d0214cd9-6970-4dbc-b020-becc8cb571ab)


sed -n '2,4{s/^/$/;p}' file23

OUTPUT

![image](https://github.com/greffinaprem/OS-Linux-commands-Shell-script/assets/119475603/39a8edd2-dfd8-4fa2-989b-3eaa64a36fe5)


sed -n '2,4{s/$/*/;p}' file23 ##OUTPUT

304769027-3459be51-4d3f-4d3b-a8ad-e63a1fcadd62

Sorting File content cat > file21
1001 | Ram | 10000 | HR 1002 | tom | 5000 | Admin 1003 | Joe | 7000 | Developer 1005 | Sam | 5000 | HR 1004 | Sit | 7000 | Dev

sort file21

OUTPUT

![image](https://github.com/greffinaprem/OS-Linux-commands-Shell-script/assets/119475603/c1c888a7-3dd7-48ae-8c1c-2d0ccc3cf307)


cat > file22

1001 | Ram | 10000 | HR 1001 | Ram | 10000 | HR 1002 | tom | 5000 | Admin 1003 | Joe | 7000 | Developer 1005 | Sam | 5000 | HR 1004 | Sit | 7000 | Dev

uniq file22

OUTPUT

![image](https://github.com/greffinaprem/OS-Linux-commands-Shell-script/assets/119475603/5aa82f7a-8e05-4226-82f0-8d70aaa8b71b)


Using tr command
cat file23 | tr [:lower:] [:upper:]


OUTPUT

![image](https://github.com/greffinaprem/OS-Linux-commands-Shell-script/assets/119475603/59333fe5-8296-4899-90e2-22528d92805b)


cat < urllist.txt

www. yahoo. com www. google. com www. mrcet.... com ^d

cat > urllist.txt

www. yahoo. com www. google. com www. mrcet.... com

cat urllist.txt | tr -d ' '

OUTPUT

![image](https://github.com/greffinaprem/OS-Linux-commands-Shell-script/assets/119475603/2ca97979-4ecf-471f-bd45-35e7f60d93e4)


cat urllist.txt | tr -d ' ' | tr -s '.'

OUTPUT

![image](https://github.com/greffinaprem/OS-Linux-commands-Shell-script/assets/119475603/f64ac272-3fb8-43a9-b713-f3c8c3e323be)


#Backup commands tar -cvf backup.tar *

OUTPUT

![image](https://github.com/greffinaprem/OS-Linux-commands-Shell-script/assets/119475603/03f66574-3f22-411d-8447-9ebc1bd30e08)


mkdir backupdir

mv backup.tar backupdir

tar -tvf backup.tar

OUTPUT
tar -xvf backup.tar

OUTPUT
gzip backup.tar ls .gz

OUTPUT
gunzip backup.tar.gz

OUTPUT
Shell Script
echo '#!/bin/sh' > my-script.sh echo 'echo Hello World‘; exit 0 >> my-script.sh

chmod 755 my-script.sh ./my-script.sh

OUTPUT
cat << stop > herecheck.txt

hello in this world i cant stop for this non stop movement stop

cat herecheck.txt

OUTPUT
cat < scriptest.sh bash #!/bin/sh echo “File name is $0 ” echo "File name is " basename $0 echo “First arg. is ” $1 echo “Second arg. is ” $2 echo “Third arg. is ” $3 echo “Fourth arg. is ” @ is '

is '
You can't use 'macro parameter character #' in math mode
You can't use 'macro parameter character #' in math mode
$1#
echo 'The $$ is ' $$ ps ^d

cat scriptest.sh bash #!/bin/sh echo “File name is $0 ” echo "File name is " basename $0 echo “First arg. is ” $1 echo “Second arg. is ” $2 echo “Third arg. is ” $3 echo “Fourth arg. is ” @ is '

is '
You can't use 'macro parameter character #' in math mode
You can't use 'macro parameter character #' in math mode
$#
echo 'The $$ is ' $$ ps

chmod 777 scriptest.sh

./scriptest.sh 1 2 3

OUTPUT
ls file1

OUTPUT
echo $?

OUTPUT
./one bash: ./one: Permission denied echo $?

OUTPUT
abcd echo $?

OUTPUT
mis-using string comparisons
cat < strcomp.sh bash #!/bin/bash val1=baseball val2=hockey if [ $val1 > $val2 ] then echo "$val1 is greater than $val2" else echo "$val1 is less than $val2" fi ^d

cat strcomp.sh bash #!/bin/bash val1=baseball val2=hockey if [ $val1 > $val2 ] then echo "$val1 is greater than $val2" else echo "$val1 is less than $val2" fi

OUTPUT
chmod 755 strcomp.sh

./strcomp.sh

OUTPUT
check file ownership
cat < psswdperm.sh bash #!/bin/bash if [ -O /etc/passwd ] then echo “You are the owner of the /etc/passwd file” else echo “Sorry, you are not the owner of the /etc/passwd file” fi ^d

cat psswdperm.sh bash /#!/bin/bash if [ -O /etc/passwd ] then echo “You are the owner of the /etc/passwd file” else echo “Sorry, you are not the owner of the /etc/passwd file” fi

./psswdperm.sh

OUTPUT
check if with file location
cat>ifnested.sh bash #!/bin/bash if [ -e $HOME ] then echo “$HOME The object exists, is it a file?” if [ -f $HOME ] then echo “Yes,$HOME it is a file!” else echo “No,$HOME it is not a file!” if [ -f $HOME/.bash_history ] then echo “But $HOME/.bash_history is a file!” fi fi else echo “Sorry, the object does not exist” fi ^d

cat ifnested.sh

#!/bin/bash if [ -e $HOME ] then echo “$HOME The object exists, is it a file?” if [ -f $HOME ] then echo “Yes,$HOME it is a file!” else echo “No,$HOME it is not a file!” if [ -f $HOME/.bash_history ] then echo “But $HOME/.bash_history is a file!” fi fi else echo “Sorry, the object does not exist” fi

./ifnested.sh

OUTPUT
using numeric test comparisons
cat > iftest.sh bash #!/bin/bash val1=10 val2=11 if [ $val1 -gt 5 ] then echo “The test value $val1 is greater than 5” fi if [ $val1 -eq $val2 ] then echo “The values are equal” else echo “The values are different” fi ^d

cat iftest.sh bash #!/bin/bash val1=10 val2=11 if [ $val1 -gt 5 ] then echo “The test value $val1 is greater than 5” fi if [ $val1 -eq $val2 ] then echo “The values are equal” else echo “The values are different” fi

$ chmod 755 iftest.sh

$ ./iftest.sh ##OUTPUT

check if a file
cat > ifnested.sh bash #!/bin/bash if [ -e $HOME ] then echo “$HOME The object exists, is it a file?” if [ -f $HOME ] then echo “Yes,$HOME it is a file!” else echo “No,$HOME it is not a file!” if [ -f $HOME/.bash_history ] then echo “But $HOME/.bash_history is a file!” fi fi else echo “Sorry, the object does not exist” fi ^d

cat ifnested.sh bash #!/bin/bash if [ -e $HOME ] then echo “$HOME The object exists, is it a file?” if [ -f $HOME ] then echo “Yes,$HOME it is a file!” else echo “No,$HOME it is not a file!” if [ -f $HOME/.bash_history ] then echo “But $HOME/.bash_history is a file!” fi fi else echo “Sorry, the object does not exist” fi

$ chmod 755 ifnested.sh $ ./ifnested.sh ##OUTPUT

looking for a possible value using elif
cat elifcheck.sh bash #!/bin/bash if [ $USER = Ram ] then echo "Welcome $USER" echo "Please enjoy your visit" elif [ $USER = Rahim ] then echo "Welcome $USER" echo "Please enjoy your visit" elif [ $USER = Robert ] then echo "Special testing account" elif [ $USER = gganesh ] then echo "$USER, Do not forget to logout when you're done" else echo "Sorry, you are not allowed here" fi

$ chmod 755 elifcheck.sh $ ./elifcheck.sh

OUTPUT
testing compound comparisons
cat> ifcompound.sh bash #!/bin/bash if [ -d $HOME ] && [ -w $HOME ] then echo "The file exists and you can write to it" else echo "I cannot write to the file" fi

$ chmod 755 ifcompound.sh $ ./ifcompound.sh

OUTPUT
using the case command
cat >casecheck.sh bash case $USER in Ram | Robert) echo "Welcome, $USER" echo "Please enjoy your visit";; Rahim) echo "Special testing account";; gganesh) echo "$USER, Do not forget to log off when you're done";; *) echo "Sorry, you are not allowed here";; esac

$ chmod 755 casecheck.sh $ ./casecheck.sh cat > whiletest bash #!/bin/bash #while command test var1=10 while [ $var1 -gt 0 ] do echo [ $var1 - 1 ] done

$ chmod 755 whiletest.sh

$ ./whiletest.sh

cat untiltest.sh bash #using the until command var1=100 until [ $var1 -eq 0 ] do echo [ $var1 - 25 ] done

$ chmod 755 untiltest.sh

cat forin1.sh bash #!/bin/bash #basic for command for test in Alabama Alaska Arizona Arkansas California Colorado do echo The next state is $test done

$ chmod 755 forin1.sh

cat forin2.sh bash #!/bin/bash # another example of how not to use the for command for test in I don't know if this'll work do echo “word:$test” done

$ chmod 755 forin2.sh

cat forin2.sh bash #!/bin/bash # another example of how not to use the for command for test in I don't know if this'll work do echo “word:$test” done

$ chmod 755 forin2.sh

$ ./forin2.sh

cat forin3.sh bash #!/bin/bash # another example of how not to use the for command for test in I don't know if "this'll" work do echo "word:$test" done

$ ./forin3.sh

cat forin1.sh bash #!/bin/bash

basic for command
for test in Alabama Alaska Arizona Arkansas California Colorado do echo The next state is $test done

$ chmod 755 forin1.sh

OUTPUT
cat forinfile.sh bash #!/bin/bash

reading values from a file
file="cities" for state in cat $file do echo "Visit beautiful $file“ done

$ chmod 777 forinfile.sh $ cat cities Hyderabad Alampur Basara Warangal Adilabad Bhadrachalam Khammam

OUTPUT
cat forctype.sh bash #!/bin/bash

testing the C-style
for loop
for (( i=1; i <= 5; i++ )) do echo "The value of i is chmod 755 forctype.sh $ ./forctype.sh

OUTPUT
cat forctype1.sh bash #!/bin/bash

multiple variables
for (( a=1, b=5; a <= 5; a++, b-- )) do echo "$a - $b" done

$ chmod 755 forctype.sh $ ./forctype1.sh

OUTPUT
cat fornested1.sh bash #!/bin/bash

nesting for loops
for (( a = 1; a <= 3; a++ )) do echo "Starting loop $a:" for (( b = 1; b <= 3; b++ )) do echo " Inside loop: $b" done done

$ chmod 755 fornested1.sh

$ ./fornested1.sh

OUTPUT
cat forbreak.sh bash #!/bin/bash

breaking out of a for loop
for var1 in 1 2 3 4 5 do if [ $var1 -eq 3 ] then break fi echo "Iteration number: $var1" done echo "The for loop is completed“

OUTPUT
$ chmod 755 forbreak.sh

$ ./forbreak.sh

cat forbreak.sh bash #!/bin/bash

breaking out of a for loop
for var1 in 1 2 3 4 5 do if [ $var1 -eq 3 ] then continue fi echo "Iteration number: $var1" done echo "The for loop is completed“

$ chmod 755 forcontinue.sh

$ ./forcontinue.sh

OUTPUT
cat exread.sh bash #!/bin/bash

testing the read command
echo -n "Enter your name: " read name echo "Hello $name, welcome to my program. "

$ chmod 755 exread.sh

$ ./exread.sh

OUTPUT
cat exread1.sh bash #!/bin/bash

testing the read command
read -p "Enter your name: " name echo "Hello $name, welcome to my program. “

$ chmod 755 exread1.sh

OUTPUT
$ ./exread1.sh

cat funcex.sh bash #!/bin/bash

trying to access script parameters inside a function function func { echo $[ $1 * Extra close brace or missing open brace
Extra close brace or missing open brace
$2 ]
}
if [ $# -eq 2 ] then value=func $1 $2 echo "The result is $value" else echo "Usage: badtest1 a b" fi

OUTPUT
./funcex.sh ./funcex.sh 1 2 cat argshift.sh bash #!/bin/bash while (( "$#" )); do echo $1 shift done

$ chmod 777 argshift.sh

OUTPUT
$ ./argshift.sh 1 2 3

cat argshift1.sh bash #/bin/bash

store arguments in a special array args=("$@")

get number of elements
ELEMENTS=${#args[@]}

echo each element in array
for loop for (( i=0;i<$ELEMENTS;i++)); do echo ${args[${i}]} done

$ chmod 777 argshift.sh

OUTPUT
$ ./argshift.sh 1 2 3

cat argshift.sh bash #!/bin/bash set -x while (( "$#" )); do echo $1 shift done set +x

OUTPUT
./argshift.sh 1 2 3 cat > nc.awk bash BEGIN{} { print len=length($0),"\t",$0 wordcount+=NF chrcnt+=len } END { print "total characters",chrcnt print "Number of Lines are",NR print "No of Words count:",wordcount }

cat>data.dat bash bcdfghj abcdfghj bcdfghj ebcdfghj bcdfghj ibcdfghj bcdfghj obcdfghj bcdfghj ubcdfghj

awk -f nc.awk data.dat

OUTPUT
cat > palindrome.sh bash #num=545 echo "Enter the number" read num s=0 rev="" temp=$num while [ You can't use 'macro parameter character #' in math mode $num -gt 0 ] do

Get Remainder
s=$(( You can't use 'macro parameter character #' in math mode $num % 10 ))

Get next digit
num=$(( You can't use 'macro parameter character #' in math mode $num / 10 ))

Store previous number and
current digit in reverse
rev=$( echo ${rev}${s} ) done if [ $temp -eq $rev ]; then echo "Number is palindrome" else echo "Number is NOT palindrome" fi

**RESULT:**
The Commands are executed successfully.

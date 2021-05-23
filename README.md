logname - displays current user who is logged in -ex logname --> ec2-user
pwd- displays current working directory - pwd --> /home/ec2-user
date - displays current date
who am i - displays current user and his login time 
who - similar to above cmd
cal - displays calendar - cal 2021 --> displays calendar of year 2021
touch - creates new empty file -->  touch demo --> creates empty demo file | touch demo1 demo2 demo3 --> creates empty files
cat - creates new file with some content or append some content to file and also displays content of file --> cat > demo --> creates new file demo and prompts for content
cat >> demo --> appends content into demo file | cat demo --> displays content of file demo
rm - removes file --> rm demo --> removes demo file | rm -i demo --> prompts for confirmation
mkdir - creates new directory
rmdir - removes empty directory
rmdir -r - removes dir and all files in that dir --> rm -r somedir
cp demo1 demo2 - copies files from demo1 to demo2 --> cp demo /home/ec2-user/subdir -->copies files into subdir --> cp -i demo1 /home/ec2-user/demo -->asks for confirmation
cd -change dir
cmp file1 file2 - compares contents of file1 and file2 and displays difference in linenumber and no of bytes
wc filename- word count --> first number indicates no of lines second indicates no of words third indicates no of letters 
ls -a --> lists all files | ls -t --> lists files based on time | ls a* --> lists files that starts with a | ls [ased]*  --> lists all files that starts with ased
chmod - changes permissions for r root users, groups , other users | + means add permissions and - means remove permissions and = means assign permissions
chmod u-r demo --> removes read operations on demofile for current user
chmod u=w,o-x demo --> assigns write permission to root user and removes execute permission to other users '
*** u stands for root user , w means write , r means read , x means execute , g means groups , o means all other users in your linux machine , +means add permissions, - means remove permissions and = means assign permissions
permission weight
Read        4
write       2
execute     1
R and W     6
W and E     3 
R and E     5 
R,W and E   7
note- 0 means no permissions
chmod 700 demo --> indicates 7 for root user , 0 for groups and 0 for other users
umask 077 demo - similar to chmod 700 obtained by 777-700 and is used to change permissions during file creation and also for all files
chown newuser demo --> change the owner of file demo to newuser
*****vimp******
ssh allows you to control a remote machine all using commandline 
to ssh any remote host machine

ssh -i EC2pemkey.pem ec2-user@35.41.158.141(publicip)
grep searchword filename --> displays all lines containing that searchable word --> grep "Hello Hi" demo.txt --> grep unix * -->searches for unix in all files
grep -v techno demo.txt --> displays all lines except that do not conatain techno | file * | grep -v text --> displays all files in current dir except text files
fgrep --> similar to grep but we can provide multiple targets(searchable words) and it do not accept wildcards
fgrep "UNIX
>c++
>java" students
egrep--> similar to fgrep but with reg exp feature --> egrep "c|c++|unix" students 
sort -o result file1 file2 file3 --> sort the contents of file1,2,3 and stores them in result file
cut--> selects only partcular no of colunms and displays result --> cut -f 1,3 students --> displays 1st and 3rd columns
cut --f 2-5 students --> displays columns from 2 to 5
cat techno1 > techno2 --> sends contents of techno1 to techno2  | cat techno1 >> techno2 --> sends contents of techno1 to techno2 and allows user to data into techno2 file
ls | wc -l --> connects op of ls to wc
write --> writes something on someones terminal | write techno
sending mail -->
mail user@gmail.com user2@gmail.com
subject : from linux terminal
hello,how r u
ctrl d
mail techno2 techno3 teechno4 < myprog.c --> contents of myprog.c mailed to users
find dirname -name file(files) -print --> find . -name file1 -print --> finds path of file1 in current dir --> find / -name file1 -print -->searches from root dir
find -name "*data" -print --> finds all files end with data
file * --> displays all files in current dir
program to count no of users logged in to system --> who | wc -l
program to read and display name --> read name      echo $name
program to add two nos
echo 'enter 2 numbers'
read a b
$c = $a+ $b
echo $c
if-then-else-fi statement syntax
if condition
then
----------------
---------------
else
----------
----------
fi










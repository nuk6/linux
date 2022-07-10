# linux
All about Linux / Shell scripts
1) Reading an input from command line
```shell
#! /bin/dash
echo Hi
read -p "Enter your name" NAME
echo "The name entered is ${NAME}"
```
2) Test if a number is even or odd
```shell
#! /bin/rbash
read -p "Enter a number to check whether even : " N
# echo "Number entered is ${N}"
if [ $((N%2)) == 0 ]
    then
        echo "The Number is Even"
    else 
        echo "The Number is Odd"
fi
```
3) For and While loops
```shell
#! /bin/bash
for i in {1,2,3,4,5}
    do
        echo $i
    done

i=10
while [ $i -gt 0 ]
    do
        echo $i
        ((i = i-1))
    done
```
4) For loop for N times
```shell
#! /bin/rbash
read -p "Enter a number : " N
for ((i = 0; i < N; ++i));
    do 
        echo $i
    done

```
5) Printing fibonacci numbers
```shell
#! /bin/bash
read -p "Enter a number : " N
a=1
b=2
i=$N
echo $i
while [ $i -gt 2 ]
    do
        ((t = a+b))
        ((a = b))
        ((b = t))
        ((i = i-1))
    done
echo $t
```
6) Testing if  file or a directory eists
```shell
#! /bin/dash

read dirOrFileName
if [ -d ${dirOrFileName} ]
    then
        echo "Directory ${dirOrFileName} exists"
    else 
        echo "Directory ${dirOrFileName} does not exist"
fi
if [ -f ${dirOrFileName} ]
    then
        echo "File ${dirOrFileName} exists"
    else 
        echo "File ${dirOrFileName} does not exist"
fi
```

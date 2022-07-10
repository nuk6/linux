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
if [ `expr $N % 2` == 0 ]
    then
        echo "The Number is Even"
    else 
        echo "The Number is Odd"
fi
```

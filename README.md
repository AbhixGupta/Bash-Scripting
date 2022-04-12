
# Bash Scripting

A command line interpreter which stands for the "Bourne Shell Again", the need for bash scripting arise to automate the tasks.

First to open and create any directory and make one file with ".sh" extension.
```bash
  #!/bin/bash
  echo "Hello welcome to Bash Scripting"
  echo "Hey"
```
Save this and give permission using chmod commad:
```bash
  chmod a+x filename.sh
```
Now execute your first bash scipt by running: There are different ways to execute the Bash scripts.
```bash
  ./filename.sh
  /root/scripts/filename.sh
  /bin/bash filename.sh
  bash filename.sh
```
* (.) --> Means current working directory
* (/) --> For execution

### Working with variables
Generally we use variables to store some and it help in long run, as we will not have to change the values explicitly all over, we have to just change the values. There are some rules while dealing with the variables:
* "$" helps to print the value of the variables
* " " are to print the string values
* ' ' are also used to print the values but ignores the "$" symbol and treat that variable as regular character.
* \ used to ignore the special meaning of "$" symbol
```bash
  # Var="abc"
  # echo "$Var"
  # echo " THis is $VAR"
  # echo ' THis is $VAR'
  # echo " THis is \$VAR"
```
Run the following commands in the terminal to deeply understand the basic difference.

### Taking Input from the User
```bash
  !#/bin/bash
  echo "Enter the Any Number"
  read NUM

  echo "You have entered $NUM this number"
```
To take the input we generally use the "read" method which takes the input from the terminal. To use other features of the read we can use the following commands.
```bash
  read -p 'Username: ' USER
  read -sp 'Password: ' PASSWD
  echo
  echo "Login Successfully: Hello $USER"
```
### Storing Values of Linux Commands into the variable
To store the values of the linux commands into the varible we can use the backtics "``" or "()". 
```bash
  VAR=`ls`
  VAR1=$(ls)
  echo $VAR
  echo $VAR1
  MEMVAR=`free -m | grep Mem | awk '{print $4}'`
  MEMVAR=$(free -m | grep Mem | awk '{print $4})`
  echo $MEMVAR
````

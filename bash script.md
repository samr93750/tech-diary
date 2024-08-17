-  shebang = #!/bin/bash
- to display = echo "some thing to display"
- to declare variable 
- fname="samrawit"
- lname="amare"
- to display variable 
- echo "your name is $fname  your father name is $lname"
- to create array 
- var=("list1" "list2"...)
- to display 
- echo ${var[0]}
- to display all lists 
- echo ${var[0]}
- to get the index number
- echo ${!var[0]}
- to get the length of the lists
-  echo ${#var[0]}
- to add additional element
- var[4]="list5"
- to remove
- unset var[2]
bash input handling
1. read function 
2. Argument
1.bash read
- read -p "enter your number" var
- read -sp "enter your password"var => used to accept hidden texts like password
- read -a var => for accepting array(lists)
2.Argument
- helps to get input before the script starts 
- syntax
- just use $0-$9 while you want to work with the out put

comment 
- using hashtag # for one line
- for multiple line comment 
- <<COMMENTS  ......the comments ..... COMMENTS
bash sleep
  sleep used to make delay
   - sleep second e.g sleep 8, sleep 120 

### operations
- arithmetic operation
let  "z=$(5+8)"
echo $z
comparison operator >> 
using alphabet and sign comparison 
> ....  -gt
< ,,,,, -lt
	if {condition}
	then
	 body 
	 else
	 body
	 fi... this is the ending
	for the condition 
	- use square bracket [] for alphabetic comparison 
	- but for strings we can also use sign too
	- if we use numeric comparison we have to use double bracket and it should be sign operator>>

	   ### Day 11
	### further on bash scripting
### - Regular Expression
-most filter validation on any platform done by regular expression/regex/
- are patterns that helps to filter so texts spaces tabs and symobls.
- regex are used on linux tools called grep, awk and sed.
- reg ex code 
- the pattern is same but the implementation may differ on programming languages.
- on python 
- `import re
- a=re.search("pattern",searching file").group(0)
- print(a)`

metacharacters
- those are regex pattern symbols for filter.
- they are:
- .  = used to filter all lines exept new lines those lines must contain texts it jumps new lines that doesn't contain text
- [] = used to create your own patterns. to customize patterns e.g [a-z] used to filter characters that is found between a to z.
- ^  = used to get that starts with the pattern e.g ^hi binil hi bemil yemijemr linin select yaregal
- ()
- $   = used to get a that ends with that pattern e.g hi$ then hi bemil yemiyalku textochn filter yaregilinal.                 
- * = used to get line that have pattern that occur 0 or more times baydegemim bidegemim chigir yelewm                      
- + = used to get if the inserted pattern is found one or more times in the file e.g hellos+
- ?  = used to get lines that have pattern that is repeated 0 or one times
- {}  = to get line that have pattern that occurs min and max times. it is custom. hellos{1,3} .a text hello that have s at least 0 times and more.
\w = used to get alphanumeric key = used to filter only texts and numbers 
\W =if it is capital w it filters other than texts and numbers.
\s = used to filter spaces between words
\S = the opposite of \s it filters other than spaces/ all characters/
\d = used to get number digits
\D = used to get characters other than digits.
pipe | =or is  used to search 2 different things 
escape \= to use meta characters as a normal pattern.


^http|\.com$

Bash regex

you can use it on awk , sed ,grep

REGEX in bash script
- we use =~ operator for regex check with if condition statement
- we use here double brackets for our conditional statements.


else if condition
- to do more than one comparing
- it is samr with python is "elif"
- if condition
- then 
- body
- elif condition
- then
- body
- fi

LOOPS

- on bash there are 3 types of loops
- 1. for loop
- 2.while loop
- 3. until loop

for condition
do
 body
 done
 
for i in ${array[0]}
do 
echo $i
done

or

for ((i=1; i<=10; i++))
do
	echo $i
	done


-with slicing
for num in {1..10..1}
		start..stop..step
comment>>

while loop 

while [expression]
do
body 
done

infinite while loop

while :
do
echo "something here"
done

until loop 
it is same but one exits the loop when the expression is true. 

until [expression]
do
body
done

Function

function name (){
body
}
functionname

print-it () {
sum=$(($1+$2))
return 
}

when we have a function and the arguments will be $1, $2...
if we use $? will call the return value.

we can use linux commands in bash file

#! /bin/bash

echo "i can run apt commands in bash"
apt run update

- we can access files in current directory using * sign 

#! /bin/bash
echo **

we can interact with linux using bash
using command /bin/bash
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
	- if we use numeric comparison we have to use double bracket and it should be sign operator

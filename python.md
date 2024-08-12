= 
Logical Error
 - are errors that occur at run time (after passing the syntax test) are called exceptions or logical errors 
 - e.g try to call an index that is greater than the list have causes(Index Error) 
 - try to divide a number by zero (zero divistion error)
 - error on syntax (Name Error) and so on.
 Error Handling
 - we can use try ... except block
 - try: #CODE that cause the exception
 - exception

### python loop
- loops are used to repeat a block of code
- there are 2 types of loops in python 
- 1. for loop
- 2. while loop
For loop
- for loop is used to run a block of code for a certain number of times. it is used to iterate over any sequences such as list, tuple , string etc.
- `for val in sequence:
- `statement`
- sequence is a list , tuple , string, or range
- val is a variable which will hold the iteration from the sequence.
- e.g language=["swift","python","go", "javascript"]
- for language in languages:
- print (language)
Range
is a series of values between two numeric intervals.
range(size)
len 
to know the length of list 

while loop
- used to run a specific code until a certain condition is met
- syntax
- `while condition:
- `body of while loop

INFINITE LOOP

- `while true `: #CODE 

- for loop ends when the iteration is finished
- while loop ends when the condition is false
`break`
	- used to exit from an infinite loop

CORE OF PYTHON PROGRAMMING
----------------------------------------------------------
-INDEXING AND SLICING{START,STOP,STEP}
-INPUT HANLING
-OPERATIONS
-INDENTATION
-IF ELSE
-ERRORS(EXCEPTIONS)
-ERROR HANDLING
-LOOPS

1. INDEXING
- there are positive indexing and negative indexing
- positive indexing is from left to right
- negative indexing is from right to left
- in negative index the indexing is started from -1 not 0
- calling texts by indexes also works for strings and tuples
- e.g name("hello",30,40)
- print(name[2])//output 30
- e.g name ='nathan"
- print(name[-2])//output a

- Slicing
- syntax mylist[start:stop:step]
- is used to extract a portion from a list, then a[m:n] returns the portion of a 
- starting with position m
- upto but not including n
- negative indexing can be used
- it is more applicable for strings
- python uses default step as 1 , sometimes no need to tell/put it 
- also default stopping index is the final , still no need to tell for this kinda purpose.

USER INPUT HANDLING
- there are 2 types of inputs
- 1. by input functions
- 2.by argument
- 1.by input functions
- syntax var = input("text you like to display")
- it stores the value you put in the variable
- we can change the input type to int() float() eval() str()
- e.g number =int(input(enter your number))
- number=eval(input("enternumber:"))
- 2. by argument
- this help to get the input from command line 
- e.g import sys 
- name=sys.argv[1]
- print(f"hello {name})


### Arithmetic operators
- are simple math operation
- ** = power 2**4=16
### Assignment operator
= is used to assign 
+= addition assignment
-=subtraction assignment
*=multiplication assignment
/=division assignment
%=remainder assignment
**=exponent assignment

### comparison operators
- used to compare to variables and return boolean result
- boolean means true or false
- ==
- !=
- >
- <
- >=
- <=
### logical operator
- and
- or
- not
### Bitwise operators
- computers work with binarys
- on pythn there is a key word called bin(your decimal)
- this helps to show the binary value of your decimal
- they used to do math (logical operators) on binary.
- ~=not
- it will add 1 to the number and makes it negative.
- &=compliment
- XOR - is like and or but the ifference is the logic here = if they are the same 0 if they are different 1
- left shift(<<) is shifting 2 bits to the left
- 10 -> 1010.0000=101000.00
- 10<<2
 ### indentation
 are just white space which python uses for some of its function. if there is no proper indentation error then you are doomed
### if else conditions
if .... else

elif= else if

nested if = means using if statement inside an if statement
if a=0:
 if b>4:
  print "hi"


 
Day 1
=

 - go is much faster
 - in terms of compilation speed first rust,c,c++,go
 - in terms of excution speed js , python, ruby, php.
 - go run time ...it uses much less memory 
 - interms of memory efficiency 1st rust then go then java

# compilation
- from human readable form to machine readable form (binary)
- it can be run every where
variables
-bools
string 

Go 
- built in multi concurrency mechanism

Go language characterstic 
- used on server side or backend language
- microservices 
- web applications 
- database services 
- work with docker , vault 
- has a very simple syntax
- can be built very fast 
- requires fewer resources 
- faster than interpreted languages like python 
- consistent across different platforms os
go module 
- describes the name of the project and 
- the go version
go packages
- go programs are organized in to packages 
- go's standard library , provides different core packages for us to use
- "fmt " is one of these , which you can use by importing it
- a package is a collection of source files 

variables 
- are used to store values 
- like containers for values
- give the fariable  a name and reference every were in the code 
- constants are like variables except that their values cannot be changed.
### printing formatted data(printf)

- fmt.printf("some text with a variable %s",myVariable)
- it takes a template string that contains the text that needs to be formatted 
- plus some annotation verbs (or place holder) that tells the fmt functions how to format the variable passed in . 
### Data types in go 

- string
- integers
- boolean
- maps 
- Arrays
-go is statically typed language
-we need to tell Go compiler , the data type when declaring the variable.
-but go can infere a type when u assign a value 
- var userTicket int
- var username string
- %T = means type of the variable
- %v = means the value of the variable
-uin98= unsigned 8 bit integers(0-255)
-uint16=unsigned 16-bit integers (0-65535)
-uint32=unsigned 32-bit integers (0-4294967295)
-uint 64 =unsigned 64 bit integers (0-)
-int8=signed 8bit integers(-128 to 127)
-int16=signed 16bit integers (-32768 to 32768)

Floating point Types

-are numbers that contain a decimal component.


- to easily assign variables with value
- conferencetikcets := 50 this is equivalen to var conferencetickets = 50
### User input
- fmt.Scan()
- what is a pointer 
- a pointer is a variable that points to the memory address of another variable.
- fmt.Scan(username) - is wrong
- fmt.Scan(&username)- is correct
- scan function can now assign the user's value to the userName variable
- because it has a pointer to its memory address

Arrays and Slices 

- are data structures to store collection of elements in a single variable.
- var variable_name [size] variable type
  - only the same data type can be stored 

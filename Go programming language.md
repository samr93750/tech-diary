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


- Arrays are data structures to store collection of elements in a single variable.
- var variable_name [size] variable type
  - only the same data type can be stored 
  - array type is the size of array and the data type of the array

Slices

- what if we don't know the size when creating it?
- slice is an abstraction of an array
- are more flexible and powerful :
- variable-length or get an sub-array of its own.
- are also index based and have a size, but is resized when needed
Loops 

- provides various control structures to control the application flow
- a loop statement allows us to execute code multiple times in a loop
- loops are simplified in Go
- you only have for loop
for loop with different types
 - 1. infinite for loop
for{----}
- 2. for each loop 
- range iterates over elements for different data structures (so not only arrays and slices)
- for arrays and slices , range provides the index and values for each element.
### IF Else statement
if something=something{
do this...
}

Break statement
   - terminates for loop
   - and continues with the code right after the for loop ( inout case we don't have any code)
#### continue

skip the current process and skip to the next iteration

#### elseif statement

we can have unlimited else if statement.

End of a loop 
 -- a loop continues as long as  a condition is true
 --- we can handle that using for loop condition
infinite Loop
-- infinite loop = a loop that repeats endlessly, as the condition is always true.

### user input validation
 - handling bad user inputs. 
len  returns the length of a variables according to its type. 

### switch statement
- is best case for if else statement.
e.g
city:= "london"

    switch city{

    case "newyork":

        //something

    case "singapore":

        //something

    case "berlin":

        //something

    case "london":

        //something

    }
### Functions
- Encapsulate code into own container (=function). Which logically belong together!
- like a variable name we should give a function a descriptive name
- function greetUser{
- fmt.println("welcome...")
- }
- call a function by its name , when ever you want to execute this block of code
- greetUser()
- every program in go has at least one function , which is the main() function.
- function is only executedd , when called!
- you can call a functions as many times you want 
- so a function is also used to reduce code duplication 
- informations can be passed in to functions as parameters.
- parameteres are also called arguments.

Return values

- A function can return data as a result
- so a function can take an input and return an output
- go can return multiple values in a function.

Package level variables
 - Defined at the top outside all functions 
 - it can be accessed inside any functions 
- best practice : define variable as "local" as possible

	 local variables 
- define inside a function or a block.
- they can be accessed only inside that function or block of code.
#### Go packages
- go programs are organized in to packages.
- a package is a collection of Go files.
- variables and functions defined outside any function can be accessed in all other files within the same package.
### Exporting a variable 
- make it available for all packages in the app.
- to export just capitalize the first letter of the function

### scope of variables

1. Local
- declaration within function 
- can be used only within that function
- delclaration within block (for,if else)
- can only be used in side that block
2. package scope
- declaration outside all functions
- can be used every where in the same package
3. global
- declaration outside all functions and uppercase first letter 
- can be used everywhere across all packages 


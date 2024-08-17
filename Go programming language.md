## What is Go?

- Go is a cross-platform, open source programming language
- Go can be used to create high-performance applications
- Go is a fast, statically typed, compiled language known for its simplicity and efficiency
- Go was developed at Google by Robert Griesemer, Rob Pike, and Ken Thompson in 2007
- Go's syntax is similar to C++

---

## What is Go Used For?

- Web development (server-side)
- Developing network-based programs
- Developing cross-platform enterprise applications
- Cloud-native development

---

## Why Use Go?

- Go is fun and easy to learn
- Go has fast run time and compilation time
- Go supports concurrency
- Go has memory management
- Go works on different platforms (Windows, Mac, Linux, Raspberry Pi, etc.)

---

## Go Compared to Python and C++

|Go|[Python](https://www.w3schools.com/python/default.asp)|[C++](https://www.w3schools.com/cpp/default.asp)|
|---|---|---|
|Statically typed|Dynamically typed|Statically typed|
|Fast run time|Slow run time|Fast run time|
|Compiled|Interpreted|Compiled|
|Fast compile time|Interpreted|Slow compile time|
|Supports concurrency through goroutines and channel|No built-in concurrency mechanism|Supports concurrency through threads|
|Has automatic garbage collection|Has automatic garbage collection|Does not have automatic garbage collection|
|Does not support classes and objects|Has classes and objects|Has classes and objects|
|Does not support inheritance|Supports inheritance|Supports inheritance|

**Notes:**

- Compilation time refers to translating the code into an executable program
- Concurrency is performing multiple things out-of-order, or at the same time, without affecting the final outcome
- Statically typed means that the variable types are known at compile time
## Go Get Started

To start using Go, you need two things:

- A text editor, like VS Code, to write Go code
- A compiler, like GCC, to translate the Go code into a language that the computer will understand

There are many text editors and compilers to choose from. In this tutorial, we will use an IDE (see below).

---

## Go Install

You can find the relevant installation files at [https://golang.org/dl/](https://golang.org/dl/).

Follow the instructions related to your operating system. To check if Go was installed successfully, you can run the following command in a terminal window:

go version

Which should show the version of your Go installation.

---

## Go Install IDE

An IDE (Integrated Development Environment) is used to edit AND compile the code.

Popular IDE's include Visual Studio Code (VS Code), Vim, Eclipse, and Notepad. These are all free, and they can be used to both edit and debug Go code.

**Note:** Web-based IDE's can work as well, but functionality is limited.

We will use **VS Code** in our tutorial, which we believe is a good place to start.

You can find the latest version of VS Code at [https://code.visualstudio.com/](https://code.visualstudio.com/).

---

## Go Quickstart

Let's create our first Go program.

- Launch the VS Code editor
- Open the extension manager or alternatively, press `Ctrl + Shift + x`
- In the search box, type "go" and hit enter
- Find the Go extension by the GO team at Google and install the extension
- After the installation is complete, open the command palette by pressing `Ctrl + Shift + p`
- Run the `Go: Install/Update Tools` command
- Select all the provided tools and click OK

VS Code is now configured to use Go.

Open up a terminal window and type:

go mod init example.com/hello

Do not worry if you do not understand why we type the above command. Just think of it as something that you always do, and that you will learn more about in a later chapter.

Create a new file (`File > New File`). Copy and paste the following code and save the file as `helloworld.go` (`File > Save As`):

#### helloworld.go

package main  
import ("fmt")  
  
func main() {  
  fmt.Println("Hello World!")  
}  

Now, run the code: Open a terminal in VS Code and type:

go run .\helloworld.go

`Hello World!`

**Congratulations**! You have now written and executed your first Go program.

## Go Syntax

A Go file consists of the following parts:

- Package declaration
- Import packages
- Functions
- Statements and expressions

Look at the following code, to understand it better:

### Example

package main  
import ("fmt")  
  
func main() {  
  fmt.Println("Hello World!")  
}  

[Try it Yourself »](https://www.w3schools.com/go/trygo.php?filename=demo_helloworld)

### Example explained

**Line 1:** In Go, every program is part of a package. We define this using the `package` keyword. In this example, the program belongs to the `main` package.

**Line 2:** `import ("fmt")` lets us import files included in the `fmt` package.

**Line 3:** A blank line. Go ignores white space. Having white spaces in code makes it more readable.

**Line 4:** `func main() {}` is a function. Any code inside its curly brackets `{}` will be executed.

**Line 5:** `fmt.Println()` is a function made available from the `fmt` package. It is used to output/print text. In our example it will output "Hello World!".

**Note:** In Go, any executable code belongs to the `main` package.

---

## Go Statements

`fmt.Println("Hello World!")` is a statement.

In Go, statements are separated by ending a line (hitting the Enter key) or by a semicolon "`;`".

Hitting the Enter key adds "`;`" to the end of the line implicitly (does not show up in the source code).

The left curly bracket `{` cannot come at the start of a line.

Run the following code and see what happens:

### Example

package main  
import ("fmt")  
  
func main()  
{  
  fmt.Println("Hello World!")  
}  

[Try it Yourself »](https://www.w3schools.com/go/trygo.php?filename=demo_helloworld2)

---

## Go Compact Code

You can write more compact code, like shown below (this is not recommended because it makes the code more difficult to read):

### Example

package main; import ("fmt"); func main() { fmt.Println("Hello World!");}

\
### go comment
for single line comment use //
for multiple line comment use /* */

## Go Variable Types

In Go, there are different **types** of variables, for example:

- `int`- stores integers (whole numbers), such as 123 or -123
- `float32`- stores floating point numbers, with decimals, such as 19.99 or -19.99
- `string` - stores text, such as "Hello World". String values are surrounded by double quotes
- `bool`- stores values with two states: true or false

More about different variable types, will be explained in the [Go Data Types](https://www.w3schools.com/go/go_data_types.php) chapter.

---

## Declaring (Creating) Variables

In Go, there are two ways to declare a variable:

#### 1. With the `var` keyword:

Use the `var` keyword, followed by variable name and type:

### Syntax

var _variablename type_ = _value_

**Note:** You always have to specify either `type` or `value` (or both).

#### 2. With the `:=` sign:

Use the `:=` sign, followed by the variable value:

### Syntax

_variablename_ := _value_

**Note:** In this case, the type of the variable is **inferred** from the value (means that the compiler decides the type of the variable, based on the value).

**Note:** It is not possible to declare a variable using `:=`, without assigning a value to it.

---

## Variable Declaration With Initial Value

If the value of a variable is known from the start, you can declare the variable and assign a value to it on one line:

### Example

package main  
import ("fmt")  
  
func main() {  
  var student1 string = "John" _//type is string_  
  var student2 = "Jane" _//type is inferred_  
  x := 2 _//type is inferred_  
  
  fmt.Println(student1)  
  fmt.Println(student2)  
  fmt.Println(x)  
}

[Try it Yourself »](https://www.w3schools.com/go/trygo.php?filename=demo_variable_declaration1)

**Note:** The variable types of `student2` and `x` is **inferred** from their values.

---

---

## Variable Declaration Without Initial Value

In Go, all variables are initialized. So, if you declare a variable without an initial value, its value will be set to the default value of its type:

### Example

package main  
import ("fmt")  
  
func main() {  
  var a string  
  var b int  
  var c bool  
  
  fmt.Println(a)  
  fmt.Println(b)  
  fmt.Println(c)  
}

[Try it Yourself »](https://www.w3schools.com/go/trygo.php?filename=demo_variable_declaration2)

#### Example explained

In this example there are 3 variables:

- `a`
- `b`
- `c`

These variables are declared but they have not been assigned initial values.

By running the code, we can see that they already have the default values of their respective types:

- `a` is `""`
- `b` is `0`
- `c` is `false`

---

## Value Assignment After Declaration

It is possible to assign a value to a variable after it is declared. This is helpful for cases the value is not initially known.

### Example

package main  
import ("fmt")  
  
func main() {  
  var student1 string  
  student1 = "John"  
  fmt.Println(student1)  
}

[Try it Yourself »](https://www.w3schools.com/go/trygo.php?filename=demo_variable_declaration3)

**Note:** It is not possible to declare a variable using "`:=`" without assigning a value to it.

---

## Difference Between var and :=

There are some small differences between the `var` var `:=`:

|var|:=|
|---|---|
|Can be used **inside** and **outside** of functions|Can only be used **inside** functions|
|Variable declaration and value assignment **can be done separately**|Variable declaration and value assignment **cannot be done separately** (must be done in the same line)|

### Example

This example shows declaring variables outside of a function, with the `var` keyword:

package main  
import ("fmt")  
  
var a int  
var b int = 2  
var c = 3  
  
func main() {  
  a = 1  
  fmt.Println(a)  
  fmt.Println(b)  
  fmt.Println(c)  
}

[Try it Yourself »](https://www.w3schools.com/go/trygo.php?filename=demo_variable_declaration4)

### Example

Since `:=` is used outside of a function, running the program results in an error.

package main  
import ("fmt")  
  
a := 1  
  
func main() {  
  fmt.Println(a)  
}

Result:

`./prog.go:5:1: syntax error: non-declaration statement outside function body`

[Try it Yourself »](https://www.w3schools.com/go/trygo.php?filename=demo_variable_declaration5)

## Go Multiple Variable Declaration

In Go, it is possible to declare multiple variables in the same line.

### Example

This example shows how to declare multiple variables in the same line:

package main  
import ("fmt")  
  
func main() {  
  var a, b, c, d int = 1, 3, 5, 7  
  
  fmt.Println(a)  
  fmt.Println(b)  
  fmt.Println(c)  
  fmt.Println(d)  
}

[Try it Yourself »](https://www.w3schools.com/go/trygo.php?filename=demo_variable_declaration6)

**Note:** If you use the `type` keyword, it is only possible to declare **one type** of variable per line.

If the `type` keyword is not specified, you can declare different types of variables in the same line:

### Example

package main  
import ("fmt")  
  
func main() {  
  var a, b = 6, "Hello"  
  c, d := 7, "World!"  
  
  fmt.Println(a)  
  fmt.Println(b)  
  fmt.Println(c)  
  fmt.Println(d)  
}

[Try it Yourself »](https://www.w3schools.com/go/trygo.php?filename=demo_variable_declaration7)

---

## Go Variable Declaration in a Block

Multiple variable declarations can also be grouped together into a block for greater readability:

### Example

package main  
import ("fmt")  
  
func main() {  
   var (  
     a int  
     b int = 1  
     c string = "hello"  
   )  
  
  fmt.Println(a)  
  fmt.Println(b)  
  fmt.Println(c)  
}
## Go Variable Naming Rules

A variable can have a short name (like x and y) or a more descriptive name (age, price, carname, etc.).

Go variable naming rules:

- A variable name must start with a letter or an underscore character (_)
- A variable name cannot start with a digit
- A variable name can only contain alpha-numeric characters and underscores (`a-z, A-Z`, `0-9`, and `_` )
- Variable names are case-sensitive (age, Age and AGE are three different variables)
- There is no limit on the length of the variable name
- A variable name cannot contain spaces
- The variable name cannot be any Go keywords

---

## Multi-Word Variable Names

Variable names with more than one word can be difficult to read.

There are several techniques you can use to make them more readable:

## Camel Case

Each word, except the first, starts with a capital letter:

myVariableName = "John"

---

## Pascal Case

Each word starts with a capital letter:

MyVariableName = "John"

---

## Snake Case

Each word is separated by an underscore character:

my_variable_name = "John"
## Go Constants

If a variable should have a fixed value that cannot be changed, you can use the `const` keyword.

The `const` keyword declares the variable as "constant", which means that it is **unchangeable and read-only**.

### Syntax

const _CONSTNAME type_ = _value_

**Note:** The value of a constant must be assigned when you declare it.

---

## Declaring a Constant

Here is an example of declaring a constant in Go:

### Example

package main  
import ("fmt")  
  
const PI = 3.14  
  
func main() {  
  fmt.Println(PI)  
}

[Try it Yourself »](https://www.w3schools.com/go/trygo.php?filename=demo_variable_constants)

---

## Constant Rules

- Constant names follow the same naming rules as [variables](https://www.w3schools.com/go/go_variable_naming_rules.php)
- Constant names are usually written in uppercase letters (for easy identification and differentiation from variables)
- Constants can be declared both inside and outside of a function

---

## Constant Types

There are two types of constants:

- Typed constants
- Untyped constants

---

## Typed Constants

Typed constants are declared with a defined type:

### Example

package main  
import ("fmt")  
  
const A int = 1  
  
func main() {  
  fmt.Println(A)  
}

[Try it Yourself »](https://www.w3schools.com/go/trygo.php?filename=demo_variable_constants1)

---

---

## Untyped Constants

Untyped constants are declared without a type:

### Example

package main  
import ("fmt")  
  
const A = 1  
  
func main() {  
  fmt.Println(A)  
}

[Try it Yourself »](https://www.w3schools.com/go/trygo.php?filename=demo_variable_constants2)

**Note:** In this case, the type of the constant is inferred from the value (means the compiler decides the type of the constant, based on the value).

---

## Constants: Unchangeable and Read-only

When a constant is declared, it is not possible to change the value later:

### Example

package main  
import ("fmt")  
  
func main() {  
  const A = 1  
  A = 2  
  fmt.Println(A)  
}

Result:

`./prog.go:8:7: cannot assign to A`

[Try it Yourself »](https://www.w3schools.com/go/trygo.php?filename=demo_variable_constants3)

---

## Multiple Constants Declaration

Multiple constants can be grouped together into a block for readability:

### Example

package main  
import ("fmt")  
  
const (  
  A int = 1  
  B = 3.14  
  C = "Hi!"  
)  
  
func main() {  
  fmt.Println(A)  
  fmt.Println(B)  
  fmt.Println(C)  
}
### Go out put
Go has three functions to output text:

- `Print()`
- `Println()`
- `Printf()`

---

## The Print() Function

The `Print()` function prints its arguments with their default format.

### Example

Print the values of `i` and `j`:

package main  
import ("fmt")  
  
func main() {  
  var i,j string = "Hello","World"  
  
  fmt.Print(i)  
  fmt.Print(j)  
}

Result:

`HelloWorld   `

[Try it Yourself »](https://www.w3schools.com/go/trygo.php?filename=demo_output1)

### Example

If we want to print the arguments in new lines, we need to use `\n`.

package main  
import ("fmt")  
  
func main() {  
  var i,j string = "Hello","World"  
  
  fmt.Print(i, "\n")  
  fmt.Print(j, "\n")  
}

Result:

`Hello   World   `

[Try it Yourself »](https://www.w3schools.com/go/trygo.php?filename=demo_output2)

**Tip:** `\n` creates new lines.

### Example

It is also possible to only use one `Print()` for printing multiple variables.

package main  
import ("fmt")  
  
func main() {  
  var i,j string = "Hello","World"  
  
  fmt.Print(i, "\n",j)  
}

Result:

`Hello   World   `

[Try it Yourself »](https://www.w3schools.com/go/trygo.php?filename=demo_output3)

### Example

If we want to add a space between string arguments, we need to use " ":

package main  
import ("fmt")  
  
func main() {  
  var i,j string = "Hello","World"  
  
  fmt.Print(i, " ", j)  
}

Result:

`Hello World   `

[Try it Yourself »](https://www.w3schools.com/go/trygo.php?filename=demo_output4)

### Example

`Print()` inserts a space between the arguments if **neither** are strings:

package main  
import ("fmt")  
  
func main() {  
  var i,j = 10,20  
  
  fmt.Print(i,j)  
}

Result:

`10 20   `

[Try it Yourself »](https://www.w3schools.com/go/trygo.php?filename=demo_output7)

---

---

## The Println() Function

The `Println()` function is similar to `Print()` with the difference that a whitespace is added between the arguments, and a newline is added at the end:

### Example

package main  
import ("fmt")  
  
func main() {  
  var i,j string = "Hello","World"  
  
  fmt.Println(i,j)  
}

Result:

`Hello World`

[Try it Yourself »](https://www.w3schools.com/go/trygo.php?filename=demo_output5)

---

## The Printf() Function

The `Printf()` function first formats its argument based on the given formatting verb and then prints them.

Here we will use two formatting verbs:

- `%v` is used to print the **value** of the arguments
- `%T` is used to print the **type** of the arguments

### Example

package main  
import ("fmt")  
  
func main() {  
  var i string = "Hello"  
  var j int = 15  
  
  fmt.Printf("i has value: %v and type: %T\n", i, i)  
  fmt.Printf("j has value: %v and type: %T", j, j)  
}

Result:

`i has value: Hello and type: string   j has value: 15 and type: int`
# Go Formatting Verbs

---

## Formatting Verbs for Printf()

Go offers several formatting verbs that can be used with the `Printf()` function.

---

## General Formatting Verbs

The following verbs can be used with all data types:

|Verb|Description|
|---|---|
|%v|Prints the value in the default format|
|%#v|Prints the value in Go-syntax format|
|%T|Prints the type of the value|
|%%|Prints the % sign|

### Example

package main  
import ("fmt")  
  
func main() {  
  var i = 15.5  
  var txt = "Hello World!"  
  
  fmt.Printf("%v\n", i)  
  fmt.Printf("%#v\n", i)  
  fmt.Printf("%v%%\n", i)  
  fmt.Printf("%T\n", i)  
  
  fmt.Printf("%v\n", txt)  
  fmt.Printf("%#v\n", txt)  
  fmt.Printf("%T\n", txt)  
}

Result:

`15.5   15.5   15.5%   float64   Hello World!   "Hello World!"   string`

[Try it Yourself »](https://www.w3schools.com/go/trygo.php?filename=demo_formatting1)

---

## Integer Formatting Verbs

The following verbs can be used with the integer data type:

|Verb|Description|
|---|---|
|%b|Base 2|
|%d|Base 10|
|%+d|Base 10 and always show sign|
|%o|Base 8|
|%O|Base 8, with leading 0o|
|%x|Base 16, lowercase|
|%X|Base 16, uppercase|
|%#x|Base 16, with leading 0x|
|%4d|Pad with spaces (width 4, right justified)|
|%-4d|Pad with spaces (width 4, left justified)|
|%04d|Pad with zeroes (width 4|

### Example

package main  
import ("fmt")  
  
func main() {  
  var i = 15  
   
  fmt.Printf("%b\n", i)  
  fmt.Printf("%d\n", i)  
  fmt.Printf("%+d\n", i)  
  fmt.Printf("%o\n", i)  
  fmt.Printf("%O\n", i)  
  fmt.Printf("%x\n", i)  
  fmt.Printf("%X\n", i)  
  fmt.Printf("%#x\n", i)  
  fmt.Printf("%4d\n", i)  
  fmt.Printf("%-4d\n", i)  
  fmt.Printf("%04d\n", i)  
}

Result:

`1111   15   +15   17   0o17   f   F   0xf     15   15   0015`

## Go Integer Data Types

Integer data types are used to store a whole number without decimals, like 35, -50, or 1345000.

The integer data type has two categories:

- **Signed integers** - can store both positive and negative values
- **Unsigned integers** - can only store non-negative values

**Tip:** The default type for integer is `int`. If you do not specify a type, the type will be `int`.

---

## Signed Integers

Signed integers, declared with one of the `int` keywords, can store both positive and negative values:

### Example

package main  
import ("fmt")  
  
func main() {  
  var x int = 500  
  var y int = -4500  
  fmt.Printf("Type: %T, value: %v", x, x)  
  fmt.Printf("Type: %T, value: %v", y, y)  
}

[Try it Yourself »](https://www.w3schools.com/go/trygo.php?filename=demo_data_types_integer2)

Go has five keywords/types of signed integers:

|Type|Size|Range|
|---|---|---|
|`int`|Depends on platform:  <br>32 bits in 32 bit systems and  <br>64 bit in 64 bit systems|-2147483648 to 2147483647 in 32 bit systems and  <br>-9223372036854775808 to 9223372036854775807 in 64 bit systems|
|`int8`|8 bits/1 byte|-128 to 127|
|`int16`|16 bits/2 byte|-32768 to 32767|
|`int32`|32 bits/4 byte|-2147483648 to 2147483647|
|`int64`|64 bits/8 byte|-9223372036854775808 to 9223372036854775807|

---

---

## Unsigned Integers

Unsigned integers, declared with one of the `uint` keywords, can only store non-negative values:

### Example

package main  
import ("fmt")  
  
func main() {  
  var x uint = 500  
  var y uint = 4500  
  fmt.Printf("Type: %T, value: %v", x, x)  
  fmt.Printf("Type: %T, value: %v", y, y)  
}  

[Try it Yourself »](https://www.w3schools.com/go/trygo.php?filename=demo_data_types_integer1)

Go has five keywords/types of unsigned integers:

|Type|Size|Range|
|---|---|---|
|`uint`|Depends on platform:  <br>32 bits in 32 bit systems and  <br>64 bit in 64 bit systems|0 to 4294967295 in 32 bit systems and  <br>0 to 18446744073709551615 in 64 bit systems|
|`uint8`|8 bits/1 byte|0 to 255|
|`uint16`|16 bits/2 byte|0 to 65535|
|`uint32`|32 bits/4 byte|0 to 4294967295|
|`uint64`|64 bits/8 byte|0 to 18446744073709551615|

---

## Which Integer Type to Use?

The type of integer to choose, depends on the value the variable has to store.

### Example

This example will result in an error because 1000 is out of range for int8 (which is from -128 to 127):

package main  
import ("fmt")  
  
func main() {  
  var x int8 = 1000  
  fmt.Printf("Type: %T, value: %v", x, x)  
}

Result:

`./prog.go:5:7: constant 1000 overflows int8`
## Go Arrays

Arrays are used to store multiple values of the same type in a single variable, instead of declaring separate variables for each value.

---

## Declare an Array

In Go, there are two ways to declare an array:

#### 1. With the `var` keyword:

### Syntax

var _array_name =_ [_length_]_datatype_{_values_} // here length is defined  
  
or  
  
var _array_name =_ [...]_datatype_{_values_} // here length is inferred

#### 2. With the `:=` sign:

### Syntax

_array_name_ := [_length_]_datatype_{_values_} // here length is defined  
  
or  
  
_array_name_ := [...]_datatype_{_values_} // here length is inferred

**Note:** The _length_ specifies the number of elements to store in the array. In Go, arrays have a fixed length. The length of the array is either defined by a number or is inferred (means that the compiler decides the length of the array, based on the number of _values_).

---

## Array Examples

### Example

This example declares two arrays (arr1 and arr2) with defined lengths:

package main  
import ("fmt")  
  
func main() {  
  var arr1 = [3]int{1,2,3}  
  arr2 := [5]int{4,5,6,7,8}  
  
  fmt.Println(arr1)  
  fmt.Println(arr2)  
}

Result:

`[1 2 3]   [4 5 6 7 8]   `

[Try it Yourself »](https://www.w3schools.com/go/trygo.php?filename=demo_arrays1)

### Example

This example declares two arrays (arr1 and arr2) with inferred lengths:

package main  
import ("fmt")  
  
func main() {  
  var arr1 = [...]int{1,2,3}  
  arr2 := [...]int{4,5,6,7,8}  
  
  fmt.Println(arr1)  
  fmt.Println(arr2)  
}

Result:

`[1 2 3]   [4 5 6 7 8]   `

[Try it Yourself »](https://www.w3schools.com/go/trygo.php?filename=demo_arrays2)

### Example

This example declares an array of strings:

package main  
import ("fmt")  
  
func main() {  
  var cars = [4]string{"Volvo", "BMW", "Ford", "Mazda"}  
  fmt.Print(cars)  
}

Result:

`[Volvo BMW Ford Mazda]`

[Try it Yourself »](https://www.w3schools.com/go/trygo.php?filename=demo_arrays_string)

---

---

## Access Elements of an Array

You can access a specific array element by referring to the index number.

In Go, array indexes start at 0. That means that [0] is the first element, [1] is the second element, etc.

### Example

This example shows how to access the first and third elements in the prices array:

package main  
import ("fmt")  
  
func main() {  
  prices := [3]int{10,20,30}  
  
  fmt.Println(prices[0])  
  fmt.Println(prices[2])  
}

Result:

`10   30   `

[Try it Yourself »](https://www.w3schools.com/go/trygo.php?filename=demo_arrays3)

---

## Change Elements of an Array

You can also change the value of a specific array element by referring to the index number.

### Example

This example shows how to change the value of the third element in the prices array: 

package main  
import ("fmt")  
  
func main() {  
  prices := [3]int{10,20,30}  
  
  prices[2] = 50  
  fmt.Println(prices)  
}

Result:

`[10 20 50]   `

[Try it Yourself »](https://www.w3schools.com/go/trygo.php?filename=demo_arrays4)

---

## Array Initialization

If an array or one of its elements has not been initialized in the code, it is assigned the default value of its type.

**Tip:** The default value for int is 0, and the default value for string is "".

### Example

package main  
import ("fmt")  
  
func main() {  
  arr1 := [5]int{} //not initialized  
  arr2 := [5]int{1,2} //partially initialized  
  arr3 := [5]int{1,2,3,4,5} //fully initialized  
  
  fmt.Println(arr1)  
  fmt.Println(arr2)  
  fmt.Println(arr3)  
}

Result:

`[0 0 0 0 0]   [1 2 0 0 0]   [1 2 3 4 5]   `

[Try it Yourself »](https://www.w3schools.com/go/trygo.php?filename=demo_arrays5)

---

## Initialize Only Specific Elements

It is possible to initialize only specific elements in an array.

### Example

This example initializes only the second and third elements of the array: 

package main  
import ("fmt")  
  
func main() {  
  arr1 := [5]int{1:10,2:40}  
  
  fmt.Println(arr1)  
}

Result:

`[0 10 40 0 0]   `

[Try it Yourself »](https://www.w3schools.com/go/trygo.php?filename=demo_arrays6)

#### Example Explained

 The array above has 5 elements.

- `1:10` means: assign `10` to array index `1` (second element).
- `2:40` means: assign `40` to array index `2` (third element).

---

## Find the Length of an Array

The `len()` function is used to find the length of an array:

### Example

package main  
import ("fmt")  
  
func main() {  
  arr1 := [4]string{"Volvo", "BMW", "Ford", "Mazda"}  
  arr2 := [...]int{1,2,3,4,5,6}  
  
  fmt.Println(len(arr1))  
  fmt.Println(len(arr2))  
}

Result:

`4   6   `

## Go Slices

Slices are similar to arrays, but are more powerful and flexible.

Like arrays, slices are also used to store multiple values of the same type in a single variable.

However, unlike arrays, the length of a slice can grow and shrink as you see fit.

In Go, there are several ways to create a slice:

- Using the []_datatype_{_values_} format
- Create a slice from an array
- Using the make() function

---

### Create a Slice With []_datatype_{_values_}

### Syntax

_slice_name_ := []_datatype_{_values_}

A common way of declaring a slice is like this:

myslice := []int{}

The code above declares an empty slice of 0 length and 0 capacity.

To initialize the slice during declaration, use this:

myslice := []int{1,2,3}

The code above declares a slice of integers of length 3 and also the capacity of 3.

In Go, there are two functions that can be used to return the length and capacity of a slice:

- `len()` function - returns the length of the slice (the number of elements in the slice)
- `cap()` function - returns the capacity of the slice (the number of elements the slice can grow or shrink to)

### Example

This example shows how to create slices using the []_datatype_{_values_} format:

package main  
import ("fmt")  
  
func main() {  
  myslice1 := []int{}  
  fmt.Println(len(myslice1))  
  fmt.Println(cap(myslice1))  
  fmt.Println(myslice1)  
  
  myslice2 := []string{"Go", "Slices", "Are", "Powerful"}  
  fmt.Println(len(myslice2))  
  fmt.Println(cap(myslice2))  
  fmt.Println(myslice2)  
}

Result:

`0   0   []   4   4   [Go Slices Are Powerful]`

[Try it Yourself »](https://www.w3schools.com/go/trygo.php?filename=demo_slices1)

In the example above, we see that in the first slice (myslice1), the actual elements are not specified, so both the length and capacity of the slice will be zero. In the second slice (myslice2), the elements are specified, and both length and capacity is equal to the number of actual elements specified.

---

---

## Create a Slice From an Array

You can create a slice by slicing an array:

### Syntax

var myarray = [length]datatype{values} // An array  
myslice := myarray[start:end] // A slice made from the array  

### Example

This example shows how to create a slice from an array:

package main  
import ("fmt")  
  
func main() {  
  arr1 := [6]int{10, 11, 12, 13, 14,15}  
  myslice := arr1[2:4]  
  
  fmt.Printf("myslice = %v\n", myslice)  
  fmt.Printf("length = %d\n", len(myslice))  
  fmt.Printf("capacity = %d\n", cap(myslice))  
}

Result:

`myslice = [12 13]   length = 2   capacity = 4`

[Try it Yourself »](https://www.w3schools.com/go/trygo.php?filename=demo_slices2)

In the example above `myslice` is a slice with length 2. It is made from `arr1` which is an array with length 6.

The slice starts from the third element of the array which has value 12 (remember that array indexes start at 0. That means that [0] is the first element, [1] is the second element, etc.). The slice can grow to the end of the array. This means that the capacity of the slice is 4.

If `myslice` started from element 0, the slice capacity would be 6.

---

## Create a Slice With The make() Function

The `make()` function can also be used to create a slice.

### Syntax

_slice_name_ := make([]_type_, _length_, _capacity_)  

**Note:** If the _capacity_ parameter is not defined, it will be equal to _length_.

### Example

This example shows how to create slices using the `make()` function:

package main  
import ("fmt")  
  
func main() {  
  myslice1 := make([]int, 5, 10)  
  fmt.Printf("myslice1 = %v\n", myslice1)  
  fmt.Printf("length = %d\n", len(myslice1))  
  fmt.Printf("capacity = %d\n", cap(myslice1))  
  
  // with omitted capacity  
  myslice2 := make([]int, 5)  
  fmt.Printf("myslice2 = %v\n", myslice2)  
  fmt.Printf("length = %d\n", len(myslice2))  
  fmt.Printf("capacity = %d\n", cap(myslice2))  
}

Result:

`myslice1 = [0 0 0 0 0]   length = 5   capacity = 10   myslice2 = [0 0 0 0 0]   length = 5   capacity = 5`
# Go Access, Change, Append and Copy Slices

[❮ Previous](https://www.w3schools.com/go/go_slices.php)[Next ❯](https://www.w3schools.com/go/go_operators.php)

---

## Access Elements of a Slice

You can access a specific slice element by referring to the index number.

In Go, indexes start at 0. That means that [0] is the first element, [1] is the second element, etc.

### Example

This example shows how to access the first and third elements in the prices slice:

package main  
import ("fmt")  
  
func main() {  
  prices := []int{10,20,30}  
  
  fmt.Println(prices[0])  
  fmt.Println(prices[2])  
}

Result:

`10   30`

[Try it Yourself »](https://www.w3schools.com/go/trygo.php?filename=demo_slices4)

---

## Change Elements of a Slice

You can also change a specific slice element by referring to the index number.

### Example

This example shows how to change the third element in the prices slice:

package main  
import ("fmt")  
  
func main() {  
  prices := []int{10,20,30}  
  prices[2] = 50  
  fmt.Println(prices[0])  
  fmt.Println(prices[2])  
}

Result:

`10   50`

[Try it Yourself »](https://www.w3schools.com/go/trygo.php?filename=demo_slices4_2)

---

## Append Elements To a Slice

You can append elements to the end of a slice using the `append()`function:

### Syntax

_slice_name_ = append(_slice_name_, _element1_, _element2_, ...)  

### Example

This example shows how to append elements to the end of a slice:

package main  
import ("fmt")  
  
func main() {  
  myslice1 := []int{1, 2, 3, 4, 5, 6}  
  fmt.Printf("myslice1 = %v\n", myslice1)  
  fmt.Printf("length = %d\n", len(myslice1))  
  fmt.Printf("capacity = %d\n", cap(myslice1))  
  
  myslice1 = append(myslice1, 20, 21)  
  fmt.Printf("myslice1 = %v\n", myslice1)  
  fmt.Printf("length = %d\n", len(myslice1))  
  fmt.Printf("capacity = %d\n", cap(myslice1))  
}

Result:

`myslice1 = [1 2 3 4 5 6]   length = 6   capacity = 6   myslice1 = [1 2 3 4 5 6 20 21]   length = 8   capacity = 12`

[Try it Yourself »](https://www.w3schools.com/go/trygo.php?filename=demo_slices5)

---

---

## Append One Slice To Another Slice

To append all the elements of one slice to another slice, use the `append()`function:

### Syntax

_slice3_ = append(_slice1_, _slice2_...)  

**Note:** The **'...'** after _slice2_ is **necessary** when appending the elements of one slice to another.

### Example

This example shows how to append one slice to another slice:

package main  
import ("fmt")  
  
func main() {  
  myslice1 := []int{1,2,3}  
  myslice2 := []int{4,5,6}  
  myslice3 := append(myslice1, myslice2...)  
  
  fmt.Printf("myslice3=%v\n", myslice3)  
  fmt.Printf("length=%d\n", len(myslice3))  
  fmt.Printf("capacity=%d\n", cap(myslice3))  
}

Result:

`myslice3=[1 2 3 4 5 6]   length=6   capacity=6`

[Try it Yourself »](https://www.w3schools.com/go/trygo.php?filename=demo_slices6)

---

## Change The Length of a Slice

Unlike arrays, it is possible to change the length of a slice.

### Example

This example shows how to change the length of a slice:

package main  
import ("fmt")  
  
func main() {  
  arr1 := [6]int{9, 10, 11, 12, 13, 14} // An array  
  myslice1 := arr1[1:5] // Slice array  
  fmt.Printf("myslice1 = %v\n", myslice1)  
  fmt.Printf("length = %d\n", len(myslice1))  
  fmt.Printf("capacity = %d\n", cap(myslice1))  
  
  myslice1 = arr1[1:3] // Change length by re-slicing the array  
  fmt.Printf("myslice1 = %v\n", myslice1)  
  fmt.Printf("length = %d\n", len(myslice1))  
  fmt.Printf("capacity = %d\n", cap(myslice1))  
  
  myslice1 = append(myslice1, 20, 21, 22, 23) // Change length by appending items  
  fmt.Printf("myslice1 = %v\n", myslice1)  
  fmt.Printf("length = %d\n", len(myslice1))  
  fmt.Printf("capacity = %d\n", cap(myslice1))  
}

Result:

`myslice1 = [10 11 12 13]   length = 4   capacity = 5   myslice1 = [10 11]   length = 2   capacity = 5   myslice1 = [10 11 20 21 22 23]   length = 6   capacity = 10`

[Try it Yourself »](https://www.w3schools.com/go/trygo.php?filename=demo_slices7)

---

## Memory Efficiency

 When using slices, Go loads all the underlying elements into the memory.

If the array is large and you need only a few elements, it is better to copy those elements using the `copy()` function.

The `copy()` function creates a new underlying array with only the required elements for the slice. This will reduce the memory used for the program. 

### Syntax

copy(_dest_, _src_)

The `copy()` function takes in two slices _dest_ and _src_, and copies data from _src_ to _dest_. It returns the number of elements copied.

### Example

This example shows how to use the `copy()` function:

package main  
import ("fmt")  
  
func main() {  
  numbers := []int{1,2,3,4,5,6,7,8,9,10,11,12,13,14,15}  
  // Original slice  
  fmt.Printf("numbers = %v\n", numbers)  
  fmt.Printf("length = %d\n", len(numbers))  
  fmt.Printf("capacity = %d\n", cap(numbers))  
  
  // Create copy with only needed numbers  
  neededNumbers := numbers[:len(numbers)-10]  
  numbersCopy := make([]int, len(neededNumbers))  
  copy(numbersCopy, neededNumbers)  
  
  fmt.Printf("numbersCopy = %v\n", numbersCopy)  
  fmt.Printf("length = %d\n", len(numbersCopy))  
  fmt.Printf("capacity = %d\n", cap(numbersCopy))  
}

Result:

`// Original slice   numbers = [1 2 3 4 5 6 7 8 9 10 11 12 13 14 15]   length = 15   capacity = 15   // New slice   numbersCopy = [1 2 3 4 5]   length = 5   capacity = 5`

[Try it Yourself »](https://www.w3schools.com/go/trygo.php?filename=demo_slices8)

The capacity of the new slice is now less than the capacity of the original slice because the new underlying array is smaller.

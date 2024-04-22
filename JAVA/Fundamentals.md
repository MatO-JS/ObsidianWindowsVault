Source : Mosh Ultimate Java Fundamentals Part 1

### Declaring and initializing variables  
[2- Variables.mp4](file:///D:%5CDevelopment%5CMosh%20Courses%5CUltimate%20Java%20Part%201%20Fundamentals%5C2.%20Types%5C2-%20Variables.mp4)


`int age = 30;`


> 	We are storing the number 30 somewhere in computers memory and we are assigning the label `age`  to that memory location.

- `int` is the type of  the variable `age`  
	`int` means integer numbers that don't have a decimal point.
- `age` is the name of the variable or label or  identifier 
- `=` is the assignment operator
- `30` is the initial value of the variable

### Various data types in java
[3- Primitive Types.mp4](file:///D:%5CDevelopment%5CMosh%20Courses%5CUltimate%20Java%20Part%201%20Fundamentals%5C2.%20Types%5C3-%20Primitive%20Types.mp4)

- Primitive data types - for storing simple values
- Reference data types - for storing complex objects

## Primitive types


#### Storing Integers

| Type                                   | Bytes | Range                   |
| -------------------------------------- | ----- | ----------------------- |
| **<font color="#ffc000">byte</font>**  | 1     | **-128 to 127**         |
| **<font color="#ffc000">short</font>** | 2     | **-32k to 32k**         |
| **<font color="#ffc000">int</font>**   | 4     | **-2B to 2 Billion**    |
| **<font color="#ffc000">long</font>**  | 8     | **2 Billion and above** |
|                                        |       |                         |
#### Storing Decimal numbers

| Type                                    | Bytes |
| --------------------------------------- | ----- |
| **<font color="#ffc000">float</font>**  | 4     |
| **<font color="#ffc000">double</font>** | 8     |


### Character storing

| Type     | Bytes | Range          |
| -------- | ----- | -------------- |
| **char** | **2** | **A,B,C, ...** |

#### Boolean

| Type    | Bytes | Range        |
| ------- | ----- | ------------ |
| **boolean** | **1**     | **true / false** |

#### Notes To Remember

- Use meaningful and descriptive name for your variables

- When writing very large numbers in java every three digits can be separated by an underscore from the right to make the numbers more readable
	`int count = 123_456_789;`


- By default<font color="#00b0f0"> java sees all numbers as integers</font> even numbers</font> greater     than 2    billion( long should be the data type of numbers  above 2  billion).Even after assigning `long` data type to the variable that contains a number above 2 billion , the compiler still shows error. This is because the compiler still sees the number above 2 Billion as an integer. So we need to assign `L` after the number to make the number of data type long;
	 `long count = 3_123_456_789L;`
	

- By default<font color="#00b0f0"> java sees all decimal numbers as double</font>. So for a  number with float data type we need to assign a suffix `F` to the number just as above 
		`float price = 10.9F;`

- In java single characters should be represented in single quotes and strings or multiple characters should be in double quotes


- We cannot use the reserved keywords in java to name variables , classes , and methods.
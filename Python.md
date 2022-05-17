#python 
# #IO
## #print_statements
print()
## #input 
var = input("prompt")
## #files
var =  file, mode)
| mode  | effect          |
| ----- | --------------- |
| "r"   | read            |
| "w"   | write           |
| "a"   | append          |
| "r+"" | reand and write |
### useful functions
readline() returns a line
readlines() returns all lines in a file in a list
close() closes file
write(string)
# #importing 
from x import * imports all of x package
import file
# #variables
variables are loosely typed meaning they van hold any primitive value
## deceleration
var_name = x
## #string
concatenated with "+"
cannot concatenate strings with numbers
"\" serves as an #escape_character
| Escape Sequence | meaning                                   |
| --------------- | ----------------------------------------- |
| \’              | Single quote                              |
| \\’             | Double quote                              |
| \\              | Backslash                                 |
| \n              | new line                                  |
| \t              | tab                                       |
| \b              | backspace                                 |
| \uxxxxxxxx      | Unicode character with a 16-bit hex value |
| \Uxxxxxxxx      | Unicode character with a 32-bit hex value |
| \000            | Character with octal value ooo            |
| \xhh            | Character with hex value hh               |
### useful functions
len(var) is used to get the length of a string
str(num) returns the string value of a number
## numbers
### useful functions
abs(num) returns |num|
pow(num,pow) returns num ^ pow
max(num1, num2) returns max of num1 and num2
min(num1, rum 2) returns min ...
round(num, digit) retruns num rounded to digit places
## #boolean
var = True
var = False
"or" or's two booleans
"and" and's two booleans
"not" flips a boolean

## list
var = [x,y,z]
lists can contain multiple variable types
var[x] returns element x
var[x:] returns elements x tothe end of the list
var[x:y] returns elements x to y-1
var[:y] returns elements 0 to y-1

## tuple
var = (x,y,z)
tuples are immutable

## #dictionary
dict = {
	key: value,
	key2: value
}
dict[key] returns value
dict.get(val,default) returns value or default if key does not exist
# function
def name(params):
code within functions must be indented
functions that do not have a return statement in them return "None"


# #control_statements
## #if statements
if boolean_condition:
 	code
elif boolean_condition:
	code
else:
	code
if x in collection:
	code
code to be run in if or else must be indented
## #while loop
while condition:
	code
## #for loop
iterate through a collection
for var in string:
	code

# #comments
"#" are used for single line comment
" ''' " are used for block comments
# #exception_handling
try:
	code
except exception as err:
 	code
except:
 	code
# #class
class name:
	def __init__ (self,parameters): # initialize class
## #inheritance
import parant
class child(parent)
# js-cheat-sheet

```js
JavaScript:
statements: programming instructions
semicolons: end of each executable statement
code blocks: grouped statements
keywords: to identify the JavaScript action to be performed
syntax: set of rules,how JavaScript programs are constructed
values: fixed/literals, variables
operators: arithmetic/assignment (== equal to (comparison operator always converts (to matching types) before comparison), === equal value (operator forces comparison of values and type))
expressions: combination of values, variables, and operators, which computes to a value
comments: used to explain code, prevent execution
variables: automatically/var/let/const (scope, redeclare, reassign, hoisted, bind this) (const: the variable identifier cannot be reassigned)
Difference Between var, let and const
var   scope: no   redeclare: yes  reassign: yes   hoisted: yes  bind this: yes
let   scope: yes  redeclare: no   reassign: yes   hoisted: no   bind this: no
const scope: yes  redeclare: no   reassign: no    hoisted: no   bind this: no
logical operators: &&,||,!
type operators: typeof(to find the data type), instanceof(to see if the prototype property of a constructor appears anywhere in the prototype chain of an object)
function: parameter, argument, invoke
return: to stop executing, return value is "returned" back to the "caller"(invoker)
objects: variable,literals,properties,key:value pair, new Object()
this: refers to an object
new: the variable is created as an object
events: are "things" that happen to HTML elements
strings: zero or more characters written inside quotes, string templates, string interpolation ${...}, substitutions, escape characters, string length, string methods
numbers: can be written with or without decimals(always 64-bit Floating Point), only accurate up to 15 digits, number methods
BigInt: variables are used to store big integer values that are too big, append n to the end of an integer or call BigInt()
arrays: is a special variable, which can hold more than one value(element), new Array('a', 'b')
array methods:
at(): method returns an indexed element from an array, method returns the same as [], return existing array, return string
join(): method also joins all array elements into a string, return string
pop(): method removes the last element from an array, original array length decrease, return removed type element
push(): method adds a new element to an array (at the end), returns the new array length when declared in a variable, return array
shift(): removes the first array element and "shifts" all other elements to a lower index, original array length decrease, return removed element as string when declared in a variable, return removed type element
unshift(): adds a new element to an array (at the beginning), and "unshifts" older elements, returns the new array length when declared in a variable, return array
.length: return count of an array elements, property provides an easy way to append a new element to an array like array[array.length] that returns array, return number
changing elements: array elements are accessed using their index number, array[0] = 'new value', returns string new value when declared in a variable, return array
delete: leaves undefined<empty item> holes in the array, use pop() or shift() instead, return array
concat(): method creates a new array by merging (concatenating) existing arrays, does not change the existing arrays, can also take strings as arguments, can take any number of array argument, return array
copyWithin(): method copies array elements to another position in an array, fruits.copyWithin(2, 0, 2) copy to index 2, the elements from index 0 to 2, return array
flat(): method creates a new array with sub-array elements concatenated to a specified depth, existing array is as is, return array
splice(): method can be used to add new items to an array(also can removed by second parameter), return array with second parameter how many elements removed (any value > 0) when method declared in a variable else empty array, remove elements without leaving "holes" in the array <empty>, return array
toSpliced(): method as a safe way to splice an array without altering the original array, your ECMAScript version has to be ES2023, return array
slice(): method slices out a piece of an array into a new array, retain existing array, when 2 arguments selects elements from the start argument, and up to (but not including) the end argument and return selected elements from arguments, return array
toString(): converts an array to a comma separated string when a primitive value is expected, retain existing array, return string
array search:
indexOf(): method searches an array for an element value and returns its position, return -1 when not found, return number
lastIndexOf(): returns the position of the last occurrence of the specified element, return number
includes(): check if an element is present in an array (including NaN, unlike indexOf), retain existing array, return boolean
find(): method returns the value of the first array element that passes a test function which is the actual element, should receive callback as parameter, return type of value
findIndex(): method returns the index of the first array element that passes a test function, should receive callback as parameter, returns index of element, return number
findLast(): is an ES2023 feature, same as find() but finds from last element, returns actual element value, return number
findLastIndex(): is an ES2023 feature, same as find() but finds from last element, returns index of element, return number
sort(): method sorts an array alphabetically, modify existing array, can have callback to do ascending or descending, return array
reverse(): method reverses the elements in an array, it didn't sort array, modify existing array, return array
toSorted(): ES2023, method as a safe way to sort an array without altering the original array, return array
toReversed(): ES2023, method as a safe way to reverse an array without altering the original array, return array
array iteration methods: methods operate on every array item
forEach(): method calls a function (a callback function) once for each array element to the provided callback function, does not returns a new array based on the given array, returns “undefined“ or type of element
map(): method does not change the original array, method returns the newly created array according to the provided callback function, retain original array, return array
flatMap(): method first maps all elements of an array and then creates a new array by flattening the array to the provided callback function, retain original existing array, return array
filter(): method creates a new array with array elements that pass a test on the provided callback function, retain original array, return array
reduce(): method runs a function on each array element to produce (reduce it to) a single value depends on the second argument or parameter, retain original array, return the dependency(accumulator) type
reduceRight(): reduce from right-to-left in the array, retain original array, return the dependency(accumulator) type
every(): method checks if all array values pass a test, works with callback, return boolean
some(): method checks if some array values pass a test, works with callback, return boolean
Array.from(): method returns an Array object from any object with a length property or any iterable object like string, return array
keys(): method of Array instances returns a new array iterator object that contains the keys for each index in the array, retain existing array
entries(): method returns an Array Iterator object with key/value pairs, retain existing array
with(): ES2023 added the Array with() method as a safe way to update elements in an array without altering the original array
...: spread operator expands an iterable (like an array) into more elements
loops: often this is the case when working with arrays
for in: statement loops through the properties of an Object
for of: statement loops through the values of an iterable object
while loop: loops through a block of code as long as a specified condition is true
break: statement "jumps out" of a loop, stop iteration
continue: statement "jumps over" one iteration in the loop, statement breaks one iteration (in the loop), if a specified condition occurs, and continues with the next iteration in the loop, socket_import_stream
Sets: works like objects/arrays
new Set(): is a collection of unique values, each value can only occur once in a Set, the values can be of any type, primitive values or objects
add(): you add equal elements, only the first will be saved
new Map(): to pass an array
set(): can add elements to a Map
get(): method gets the value of a key in a Map
size: property returns the number of elements in a map
delete(): method removes a map element
clear(): method removes all the elements from a map
has(): method returns true if a key exists in a map
values(): method returns an iterator object with the values in a map
"use strict": helps you to write cleaner code, like preventing you from using undeclared variables.
Classes: a template for creating objects, class ClassName {constructor(name, year) {this.name = name;this.year = year; }method_1() { ... }method_2() { ... }}
Class create object: const myCar = new Car("Ford", 2014) // using a Class
Class use method: myCar.age()
Modules: import, export default, export
JSON: JavaScript Object Notation, a format for storing and transporting data, often used when data is sent from a server to a web page
Debugger: console.log, debugger(stops the execution of JavaScript)
event loop: responsible for executing the code, collecting and processing events, and executing queued sub-tasks. allows programs to remain responsive while handling potentially long-running tasks asynchronously (Memory heap/callstack -> web api -> memory/callback queue -> repeat)

```

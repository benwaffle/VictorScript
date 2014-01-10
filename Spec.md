Language Specification for VictorScript

Types
* style - a type for storing boolean values
  * hard - false or 0
  * soft - true or 1
  * this may seem odd, but when we return successfully from a function, we write `go hard;` since going hard is what we do
  * the exclamation point (!) is used to denote the opposite of a boolean (`soft! == hard` and `hard! == soft`)
* dub - used to define a function
* num - an IEEE 754 64-bit floating point value (double-precision)
* string - a string of characters

Other Keywords
* we - an interface to the system, with functions such as out (printing output) and in (reading input)
* go - return a value from a function
* if, else, else if - conditional keywords
* valx() - the first function called when running a VictorScript program; executables need to have this, libraries do not
* yikes - a type for storing traps (thrown when errors occur)
* try - attempt to do something
* trap - jump to this block if we catch a trap
* yeah - always executed regardless of whether a trap was trapped

Single line comments always start with an octothorpe (#)

To access a method of a class, just use a space 

for example:
`we out "swag";`

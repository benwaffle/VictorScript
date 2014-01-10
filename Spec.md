Language Specification for VictorScript

Types
* style - a type for storing boolean values
  * soft - false or 0
  * hard - true or 1
  * the exclamation point (!) is used to denote the opposite of a boolean (`soft! == hard` and `hard! == soft`)
* dub - used to define a function
* num - an IEEE 754 64-bit floating point value (double-precision)
* string - a string of characters

Other Keywords
* we - an interface to the system, with functions such as out (printing output) and in (reading input)
* go - return a value from a function
  * to signify success, convention dictates you write `go hard!;`, even though `go soft;` will compile fine 
* if, else, else if - conditional keywords
* spin - loop with init, check, and update. syntax: `spin (num i=0/i<10/i++) { # will run 10 times # }`  
* valx() - the first function called when running a VictorScript program; executables need to have this, libraries do not
* yikes - a type for storing traps (thrown when errors occur)
* try - attempt to do something
* trap - jump to this block if we catch a trap
* yeah - always executed regardless of whether a trap was trapped

Comments start and end with an octothorpe (#)

Access methods or passing arguments use a space:

for example:
```
we out "swag";
func arg;
```

`we` methods:
* `we out` - print out to the console
* `we in` - take in from the console
* `we drop` - halt the program 

you can use the `hmu` library for networking

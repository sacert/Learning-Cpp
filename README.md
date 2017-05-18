# Learning Cpp

Documenting myself learning C++ for an interview.

# Fundamental types

**Booleans:**
  - Declare as `bool`
  - Return either `0` or `1`
  
**Characters:**
  - String may be created with an array of chars + null character to indicate end of string
    - Example: `char word[] = "Hello"`;
  - Returns `char` value
  - Cast to `int` to get ASCII value
  - Belong to integral type so arithmetic and logical operations can be performed on them
  
**Integers:**
  - Default `signed` - first bit represents signed value (1/0)
  - May be:
    - `short` - not used often
    - `int` - could be either 16/32 bits depending on the system
    - `long`
    - `long long`
    
**Floating-points:**
  - Is compossed of sign bit (positive/negative), significand (significant digits), exponent (decimal place)
  - `float` - 1 sign bit, 23 bits of significand, and 8 bits of exponent
  - `double` - 1 sign bit, 52 bits of significand, and 11 bits of exponenet
  
**Voids:**
  - `void` means nothing / no type
  - when constructing a function, `int foo()` is the same as `int foo(void)`
  
#Other Types

**Strings**
  - May be constructed by including the `std` namespace 
  - Example: `string word = "hello";`
  
#Data Types

**Enumerations**
  - Compiled as integers where the default starts at 0 and increments + 1 to each of the remaining values
  - Possible to initialize each value with a distinct integer
  - Values within enum are declared within the scope
  - Example: enum colors { RED = 3, GREEN = 2, BLUE = 1 };
 
#Pointers
  - `(*)` Dereferencing operator - points to the variable whose address they store
    - *Must* point to an address
    - When using a pointer variable, it will access it's stored address and give you the value of that memory location
    - Example: `*foo = &bar` sets the address of `bar` to `foo`, when using `foo`, it will look up the address and output the value
    - Can have a double pointer which points to an address and then gets that address to point to another address
  - `(&)` Address-of operator - gets the address of the variable 
    - Example: `foo = 26` and `&foo = 1776`
    - Since arrays are pointers, a pointer can point to an array like `int *copy = array`
  
#Arrays
  - Array variables are pointers to the first address and increment the address value depending on which value you want
  - Example: With `int test[25]`, `test` points to `&test[0]`
  - Example declaration: `int foo[25];` or `int foo[] = {24,25,26,27};`
  - Multidimensional arrays = `int foo[y][x];`

#Constants
  - May not be altered
  - either with `#define indentifier value` or `const`

#Structures
  - Declare with `struct`
  - Example: `struct test { int foo = 5; } foo, bar;`
  - Mainly for backwards compatibility
  - Default functions and variables are public
  

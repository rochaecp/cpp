# C++ - Strings

- To use strings, you must include an additional header file in the source code, the <string> library.
- A string in C++ is actually an object, which contain functions that can perform certain operations on strings.
- If you try to add a number to a string, an error occurs.

~~~c++
string greeting = "Hello";
greeting = "Hello " + name;                                     // concatenate
string fullName = firstName.append(lastName); // append function - concatenate - its faster than '+'
int size = txt.length();                                            // lib string
int size = txt.size();                                                // size is an alias of length
char c = txt[0];                                                            // first character of the string
txt[0] = 'B';                                                                 // change string characters
~~~
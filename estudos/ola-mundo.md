# C++ - Olá Mundo

~~~cpp
/* Ex.: 1 */
#include <iostream>     // header file library - lets us work with input and output objects, ex: cout.
using namespace std;    // use names for objects and variables from the standard library.

int main() {
    cout << "Ola\n";        // cout is an object. << is the insert operator.
    return 0;
} 

/* Ex.: 2 */
#include <iostream>

int main() {
    std::cout << "Ola"; // The using namespace std line can be omitted and replaced with the std keyword, followed by the :: operator for some objects
    return 0;
}

/* Ex.: 3 */
/* The using namespace std line can be omitted and replaced with the std keyword, 
followed by the :: operator for string (and cout) objects */
#include <iostream>
#include <string>

int main() {
    std::string greeting = "Hello";
    std::cout << greeting;
    return 0;
} 
~~~

## Comments

~~~cpp
// This is a comment
/* This is a multi-line comment */
~~~
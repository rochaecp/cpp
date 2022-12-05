# C++ - Funções

## Functions

- A function is a block of code which only runs when it is called.
- To call a function, write the function's name followed by two parentheses () and a semicolon ;
- A C++ function consist of two parts:
    - Declaration: the function's name, return type, and parameters (if any)
    - Definition: the body of the function (code to be executed)
- It is possible to separate the declaration and the definition of the function - for code optimization - Ex2.
- The void keyword indicates that the function should not return a value.
- The return keyword indicates that the function should return a value. Use a data type instead of void.

#### Ex.: functions - void function

~~~cpp
#include <iostream>

using namespace std;

void myFunction() { // declaration
    cout << "I just got executed!"; // definition
}

int main() {
    myFunction(); // call the function
    return 0;
}
~~~

#### Ex.: functions - int function

~~~cpp
#include <iostream>

using namespace std;

int mySum(int x, int y) {
    return x + y;
}

int main() {
    cout << mySum(2, 3) << endl;
    return 0;
}
~~~

#### Ex.: functions - separate the declaration and the definition of the function 

~~~cpp
#include <iostream>

using namespace std;

void myFunction();

int main() {
    myFunction();    // call the function
    return 0;
}

void myFunction() {
    cout << "I just got executed!";
}
~~~

### Function Parameters

- Parameters act as variables inside the function.
- When a parameter is passed to the function, it is called an argument.


#### Ex: function parameters

- fname is a parameter, while Liam and Jenny are arguments.

~~~cpp
#include <iostream>

using namespace std;

void myFunction(string fname) {
    cout << "Hi " << fname << "\n";
}

int main() {
    myFunction("Liam");
    myFunction("Jenny");
    return 0;
}
~~~

#### Ex.: parameters - default parameter value

- A parameter with a default value, is often known as an "optional parameter". 

~~~c++
#include <iostream>

using namespace std;

void myFunction(string country = "empty") {
    cout << country << "\n";
}

int main() {
    myFunction();
    myFunction("Brasil");
    return 0;
}
~~~

#### Ex.: pass by reference

~~~cpp
#include <iostream>

using namespace std;

void swapNums(int &x, int &y) {
    int z = x;
    x = y;
    y = z;
}

int main() {
    int x = 2, y = 3;
    swapNums(x, y);
    cout << "x, y = " << x << ", " << y << endl;
    return 0;
}
~~~

### Function Overloading

- Instead of defining two functions that should do the same thing, it is better to overload one. 
- Multiple functions can have the same name as long as the number and/or type of parameters are different.

~~~cpp
#include <iostream>
using namespace std;

int plusFunc(int x, int y) {
    return x + y;
}

double plusFunc(double x, double y) {
    return x + y;
}

int main() {
    int numI = plusFunc(2, 3);
    double numF = plusFunc(2.1, 3.4); 
    
    cout << numI << endl;
    cout << numF << endl;
    
    return 0;
}
~~~
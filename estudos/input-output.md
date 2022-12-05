# C++ - Input e Output

## Output

~~~cpp
cout << "Hello \n";                                    // new line - preferred way
cout << "Hello" << endl;                         // new line
cout << "Hello " << myName << endl;    // print var string
cout << "Hello " << myName << "\n";    // print var string
cout << myInt << "\n";                             // print var int
~~~

#### Ex.: input - formatting double

~~~cpp
#include <iostream>
#include <iomanip>
using namespace std;

int main() {
    const double pi = 3.14159;
    double r;
    double area;

    cin >> r;
    area = pi * r * r;
    cout << fixed << setprecision(4); // #include <iomanip>
    cout << "A = " << area << endl;

    return 0;
}
~~~

## Input

~~~cpp
cin >> myName;     // Get user input from the keyboard - only 1 word
~~~
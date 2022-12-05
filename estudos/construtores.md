# C++ - Construtores

### Class Methods

- Methods are functions that belongs to the class.
- There are two ways to define functions that belongs to a class:
    - Inside class definition
    - Outside class definition

#### Ex.: class methods - inside class definition

~~~cpp
#include <iostream>
using namespace std;

class MyClass {                 // The class
    public:                             // Access specifier
        void myMethod() {     // Method/function
            cout << "Hello World!\n";
        }
};

int main() {
    MyClass myObj;         // Create an object of MyClass
    myObj.myMethod();    // Call the method
    return 0;
}
~~~

#### Ex.: class methods - outside class definition

~~~cpp
#include <iostream>
using namespace std;

class MyClass {                 // The class
    public:                             // Access specifier
        void myMethod();        // Method/function declaration
};

// Method/function definition outside the class
void MyClass::myMethod() {
    cout << "Hello World!\n";
}

int main() {
    MyClass myObj;         // Create an object of MyClass
    myObj.myMethod();    // Call the method
    return 0;
}
~~~

#### Ex.: class methods - outside class definition - parameters

~~~cpp
#include <iostream>
using namespace std;

class Car {
    public:
        int speed(int maxSpeed);
};

int Car::speed(int maxSpeed) {
    return maxSpeed;
}

int main() {
    Car myObj;
    cout << myObj.speed(200) << endl;
    return 0;
}
~~~


### Constructors

- A constructor in C++ is a special method that is automatically called when an object of a class is created.
- The constructor has the same name as the class, it is always public, and it does not have any return value.
- Constructors can also take parameters (just like regular functions), which can be useful for setting initial values for attributes.

#### Ex.: constructors

~~~cpp
#include <iostream>
using namespace std;

class Car {                // The class
    public:                    // Access specifier
        string brand;    // Attribute
        string model;    // Attribute
        int year;            // Attribute
        Car(string x, string y, int z) {    // Constructor with parameters
            brand = x;
            model = y;
            year = z;
        }
};

int main() {
    // Create Car objects and call the constructor with different values
    Car carObj1("BMW", "X5", 1999);
    Car carObj2("Ford", "Mustang", 1969);

    // Print values
    cout << carObj1.brand << " " << carObj1.model << " " << carObj1.year << "\n";
    cout << carObj2.brand << " " << carObj2.model << " " << carObj2.year << "\n";
    return 0;
}
~~~

#### Ex.: constructors - defined outside the class

~~~cpp
#include <iostream>
using namespace std;

class Car {                // The class
    public:                    // Access specifier
        string brand;    // Attribute
        string model;    // Attribute
        int year;            // Attribute
        Car(string x, string y, int z); // Constructor declaration
};

// Constructor definition outside the class
Car::Car(string x, string y, int z) {
    brand = x;
    model = y;
    year = z;
}

int main() {
    // Create Car objects and call the constructor with different values
    Car carObj1("BMW", "X5", 1999);
    Car carObj2("Ford", "Mustang", 1969);

    // Print values
    cout << carObj1.brand << " " << carObj1.model << " " << carObj1.year << "\n";
    cout << carObj2.brand << " " << carObj2.model << " " << carObj2.year << "\n";
    return 0;
}
~~~
# C++ - Classes

## OOP - Object-Oriented Programming

- Object-oriented programming is about creating objects that contain both data and functions.
- OOP makes it possible to create full reusable applications with less code and shorter development time.
- So, a class is a template for objects, and an object is an instance of a class.
- When the individual objects are created, they inherit all the variables and functions from the class.

> The "Don't Repeat Yourself" (DRY) principle is about reducing the repetition of code. You should extract out the codes that are common for the application, and place them at a single place and reuse them instead of repeating it.

### Classes/Objects

- Classes and objects are the two main aspects of object-oriented programming.
- Class: Fruit -> Objects: Apple, Banana, Orange
- Class: Car -> Objects: Volvo, Audi, Toyota

### Class Attributes

- Attributes and methods are basically variables and functions that belongs to the class.
- These are often referred to as "class members".
- A class is a user-defined data type that we can use in our program, and it works as an object constructor, or a "blueprint" for creating objects.

#### Ex.: create a class and a object with atributes

~~~cpp
#include <iostream>
#include <string>
using namespace std;

class MyClass {             // The class
    public:                         // Access specifier
        int myNum;                // Attribute (int variable)
        string myString;    // Attribute (string variable)
};

int main() {
    MyClass myObj;    // Create an object of MyClass

    // Access attributes and set values
    myObj.myNum = 15;
    myObj.myString = "Some text";

    // Print values
    cout << myObj.myNum << "\n"; 
    cout << myObj.myString << "\n"; 
    return 0;
}
~~~
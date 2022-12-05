# C++ - Herança

- We group the "inheritance concept" into two categories:
    - derived class (child) - the class that inherits from another class
    - base class (parent) - the class being inherited from
- To inherit from a class, use the : symbol.
- It is useful for code reusability: reuse attributes and methods of an existing class when you create a new class.

~~~cpp
#include <iostream>
#include <string>
using namespace std;

// Base class
class Vehicle {
    public: 
        string brand = "Ford";
        void honk() {
            cout << "Tuut, tuut! \n" ;
        }
};

// Derived class
class Car: public Vehicle {
    public: 
        string model = "Mustang";
};

int main() {
    Car myCar;
    myCar.honk();
    cout << myCar.brand + " " + myCar.model << endl;
    return 0;
}
~~~

#### Ex.: C++ Multilevel Inheritance

- A class can also be derived from one class, which is already derived from another class.

~~~cpp
#include <iostream>
using namespace std;

// Parent class
class MyClass {
    public: 
        void myFunction() {
            cout << "Some content in parent class.\n" ;
        }
};

// Child class
class MyChild: public MyClass {
};

// Grandchild class 
class MyGrandChild: public MyChild {
};

int main() {
    MyGrandChild myObj;
    myObj.myFunction();
    return 0;
}
~~~

#### Ex.: C++ Multiple Inheritance

- A class can also be derived from more than one base class, using a comma-separated list.

~~~cpp
#include <iostream>
using namespace std;

// Base class
class MyClass {
    public:
        void myFunction() {
            cout << "Some content in parent class.\n" ;
        }
};

// Another base class
class MyOtherClass {
    public:
        void myOtherFunction() {
            cout << "Some content in another class.\n" ;
        }
};

// Derived class
class MyChildClass: public MyClass, public MyOtherClass {
};

int main() {
    MyChildClass myObj;
    myObj.myFunction();
    myObj.myOtherFunction();
    return 0;
}
~~~

#### Ex.: C++ Inheritance Access

-    The third specifier, protected, is similar to private, but it can also be accessed in the inherited class.

~~~cpp
#include <iostream>
using namespace std;

// Base class
class Employee    {
    protected:    // Protected access specifier
        int salary;
};

// Derived class
class Programmer: public Employee {
    public:
        int bonus;
        void setSalary(int s) {
            salary = s;
        }
        int getSalary() {
            return salary;
        }
};

int main() {
    Programmer myObj;
    myObj.setSalary(50000);
    myObj.bonus = 15000;
    cout << "Salary: " << myObj.getSalary() << "\n";
    cout << "Bonus: " << myObj.bonus << "\n";
    return 0;
}
~~~
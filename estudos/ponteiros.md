# C++ - Ponteiros

- A pointer is a variable that stores the memory address as its value. 
- The type of the pointer has to match the type of the variable you're working with.
- & reference operator: get the memory address of a variable.
- * dereference operator: get the value of the variable.

#### Ex.: pointers

~~~cpp
cout << ptr << endl;    // mem address
cout << *ptr << endl; // 10
*ptr = 20; //change the value of the pointer
cout << *ptr << endl; // 20
~~~
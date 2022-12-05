# C++ - Arrays

~~~cpp
int myNum[3] = {10, 20, 30};

cout << myNum << endl; 
cout << myNum[0] << endl;
myNum[2] = 40;
~~~

#### Ex.: arrays - loop in array

~~~cpp
string cars[4] = {"Volvo", "BMW", "Ford", "Mazda"};
for(int i = 0; i < 4; i++) {
    cout << i << ": " << cars[i] << "\n";
~~~
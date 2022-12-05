# C++ - Arquivos

- The fstream library allows us to work with files.
- To use the fstream library, include both the standard <iostream> AND the <fstream> header file.
- There are three classes included in the fstream library, which are used to create, write or read files:
    - ofstream 	Creates and writes to files
    - ifstream 	Reads from files
    - fstream 	A combination of ofstream and ifstream: creates, reads, and writes to files

> Why do we close the file? It is considered good practice, and it can clean up unnecessary memory space.

#### Ex.: read a file

~~~cpp
#include <iostream>
#include <fstream>
#include <string>
using namespace std;

int main () {
    // Create a text file
    ofstream MyWriteFile("filename.txt");

    // Write to the file
    MyWriteFile << "Files can be tricky, but it is fun enough!";
 
    // Close the file
    MyWriteFile.close();

    // Create a text string, which is used to output the text file
    string myText;

    // Read from the text file
    ifstream MyReadFile("filename.txt");

    // Use a while loop together with the getline() function to read the file line by line
    while (getline (MyReadFile, myText)) {
        // Output the text from the file
        cout << myText;
    }

    // Close the file
    MyReadFile.close();
}

~~~
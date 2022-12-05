# C++ - Break e Continue

## Break

- When C++ reaches a break keyword, it breaks out of the block.
- The break statement can also be used to jump out of a loop.

~~~cpp
for (int i = 0; i < 10; i++) {
    if (i == 4) {
        break;
    }
    cout << i << "\n";
}
~~~

## Continue

- The continue statement breaks one iteration (in the loop), if a specified condition occurs, and continues with the next iteration in the loop.

~~~cpp
for (int i = 0; i < 10; i++) {
    if (i == 4) {
        continue;
    }
    cout << i << "\n";
} 
~~~
# Hello world!

To start off let's make hello world:
```cpp
#include <iostream> // makes std::cout accessible

int main() {
    std::cout << "Hello, new world!\n";
}
```
`#include <iostream>` is quite simple: "imports" the input/output library. After we have this `int main()` thing... it's the entry point of your app i.e. it is where it starts and ends. The code executed is contained between the two curly braces of it. The last thing to understand is `std::cout << "Hello, new world!\n";`. It abasically "pushes/inserts" (`<<`) in the **C**haracter **OUT**put the string `Hello, new world!\n` which will print on your console. (`\n` being a new line.) And that's all. Just be sure that this code compiles for you and we can continue to:
## Hello... you...

Let's write a program that asks you your name and says hello to you.
```cpp
#include <iostream>

int main() {
    std::cout << "Hello you, what is your name?\n";
    // WHAT DO I WRITE AFTER???
}
```
well what do we need to do? Se need to 
1. do input to a string
2. print the string with a nice message

So let's resolve part one: because `std::cout` exists there is also `std::cin` (**C**haracter **IN**put). It uses `>>` to "extract" characters.
```cpp
std::cin >> name;
std::cout << "Your name is: " << name << "\n";
```
But we have a new problem now: what should be name? Well it should be a string, specifically a `std::string`. You will need to `#include <string>` to use it. In the end the program should look like:
```cpp
#include <iostream>
#include <string>

int main() {
    std::cout << "Hello you, what is your name?\n";
    std::string name;
    std::cin >> name;
    std::cout << "Your name is: " << name << "\n";
}
```

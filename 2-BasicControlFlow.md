Last time we made a program that asks the user their name and prints it out afterwrds. Let's make it so that is you enter a specific name it prints an other thing. How would we do it? Using an `if` statement.
```cpp
#include <iostream>
#include <string>

int main() {
    std::cout << "Hello you, what is your name?\n";
    std::string name;
    std::cin >> name;
    std::cout << "Your name is: " << name << "\n";
    if (name == "MyName") {
        std::cout << "And I know you!\n";
    }
}
```

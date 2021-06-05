# Basic control flow
### `if` statements
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
Note: if you find it too painful to write all those `std::` you can write `using namespace std;` in the `main()` body although keep in mind that it might break stuff later...
### Thruth machine
From the [Esolang wiki](https://esolangs.org/wiki/Truth-machine):
> Essentially, a truth-machine works like this:
> - Ask for input.
> - If the input is 0:
> 	- Output 0.
> 	- Terminate program.
> - Whereas if the input is 1:
> 	- Repeat infinitely:
> 		- Output 1.
That means that we need to input an integer:
```cpp
#include <iostream>

int main() {
    int number = 0; // INTeger
    std::cin >> number;
    if (number == 0) {
        std::cout << 0;
    }
    else if (number == 1) {
        while (true == true) {
            std::cout << 1;
        }
    }
    else {
        // do nothing (this else "statement" isn't needed)
    }
}
```
Seeing all of of that you might wonder what is this blue `true` thing; it's a `bool` (boolean) value. All thing like `if`/`else`, `while` or others that takes a condition expects a boolean value i.e. something either `true` or `false`.

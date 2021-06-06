# Intro to `std::vector`
`std::vector` is a standard C++ container that represents a collection of elements, or as programmers like to call it, an array; i.e. you could have a `std::vector` which contains `int`s like `[0, 2, 4, 5, 8]`.
### The C++ type system
One thing that you might have not caught is that C++ has a strong type system. I.e. you cannot not give a type to a variable (a type being something like `int`, `std::string` or `double` for [floating point arithmetic](https://en.wikipedia.org/wiki/Floating-point_arithmetic) [decimal numbers]). For example this is valid C++:
```cpp
int i = 384;
std::string str = "Some text";
double d = 0.69;
```
but _declaring_ them without types would be illegal. i.e. doing a program like
```cpp
int main() {
    a = 50; // lacking a type (probably int)
}
```
would be wrong.
### Computing the average of notes

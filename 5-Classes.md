# Classes
A class is a thing that represents a single idea.
### Defining a class
To declare a class we use the `class` keyword:
```cpp
class MyClass {
    // ??? fill it with useful stuff
};
```
It's important to not forget the semi-column after the closing curly brace of the class.
### Defining a more useful class
In the lasts chapters we created a program to output the average of notes. But who has theses notes?
The answer is a student. So let's create one:
```cpp
class Student {
    std::string name;
    std::vector<double> notes;
    double average() {
        return std::accumulate(notes.begin(), notes.end(), 0.0) / notes.size(); 
    }
};
```
We can now create a new student:
```cpp
// in main...
Student you;
you.name = "Your cool name";
you.notes.push_back(100.0);
double yourAverageNote = you.average(); // 100% because you are wonderful
```
But there is a problem because if you try to compile this program it will fail. Why? Because of:
### [Access specifiers](https://en.wikipedia.org/wiki/Access_modifiers)
In C++ by default we can't access from outside of the class things declared inside because the default access specifier is `private`. i.e.
```cpp
class Thing {
    int something = 284;
};
```
is equivalent to
```cpp
class Thing {
private:
    int something = 284;
}
```
So to fix our problem we can just write `public:` before declaring any members (the things inside the class).

But what is the purpose of `private:` then?

If you want your stuff to not be used by bad pepoles.

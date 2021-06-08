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
public: // without this line, we would not be able to access stuff inside here from outside.
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

# Basic inheritance
C++ provides a way to expand a "thing", inheritance:
```cpp
struct Human { // struct is like class,
               // but everything in it is public
               // and we normally use it only for
               // storing (public) data; i.e. no functions in it.
    std::string name;
};

class Student : public Human { // we steal all the public functionality of a Human
public:
    std::vector<double> notes;
};
```

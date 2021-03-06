# Basic inheritance
C++ provides a way to expand a "thing", inheritance:
```cpp
struct Human { // struct is like class,
               // but everything in it is public
               // and we normally use it only for
               // storing (public) data; i.e. no functions in it.
    std::string name;
};

class Student : public Human { // we steal all public functionality of Human
public:
    std::vector<double> notes;
    double average(); // we already implemented it earlier...
};
```
Now in a function you can use it like so:
```cpp
Sutdent maybeYou;
maybeYou.name = "???"; // we got name from Human
```

### Fun starts with references (polymorphism)
```cpp
void seeHuman(const Human& human) { // Take any human, of any type...
    // (put a breakpoint here)
}

int main() {
    Human yourMom;
    Student you;
    seeHuman(yourMom); // If you debug inside this function
                       // you should not see a notes member
    seeHuman(you); // But here you will.
}
```
In a way we sort of got rid of the type because a `Student` is also a `Human` (ok I get it, in real life this might not always be true but whatever; in our C++ example it is.)
Seeing that you may ask is there a more "general" way to "stop caring about the type"?
Yes, there is and it's in the next chapter.

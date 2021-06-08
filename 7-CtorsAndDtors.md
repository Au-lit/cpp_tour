# Constructors and destructors
Last lime when we did the `Student` class we had to, after creating it, fill it manually by accessing each member. That meant that we had an uninitialised object that (could have) contained undefined values. Wouldn't it be practical if we could call a function each time we construct an object to initialise all member variables? Well yes it would be; this is where constructors become useful:
```cpp
class Position {
public:
     double x;
     double y;
     // constructor:
     Position(double otherX, double otherY)
          : x(otherX), y(otherY) {
          // you can execute code here to do stuff on creation
     }
};
// we can now create a new Position object like so:
Position pos(20.0, 3.65);
// as we can write:
double d(35.0);
```
And now we have initialized values... and a new problem: we no longer can create a "default" instance; i.e.:
```cpp
Position pos; // error :(
```
But we can fix that by well adding a default one:
```cpp
// in the class...
Position() : x(0.0), y(0.0) {}
```
This is why we didn't have undefined values when writing stuff like `std::string str;`; because std classes normally have a default constructor. And yes, `std::string` and `std::vector` are classes.
#### Notes:
- Destructors are the inverse of constructors. But you won't really need to write one yet because all that we use is automatically freed on destruction of the class.
- We will see later that the compiler can write constructirs for you _sometimes_...

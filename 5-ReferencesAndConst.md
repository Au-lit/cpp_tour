# References (`&`) and `const`
The best way to explain references that I can think of is just showing code with comments:
```cpp
int main() {
    int number = 2;
    int& reference = number;
    reference = 7; // number is now 7. That means that reference is number.
                   // Try using a debugger to really see what happens.
}
```
You should care about references because they avoid useless copies; when you take arguments without references they will be copied and the copy will be passed to your function.
That means that you potentially are copying a lot of data (depending on the thing you asked for) for basically no good reasons.
### And... what about `const`?
`const` allows you to declare an immutable object (for true constants there is an other keyword that we will see later.)
It gets interesting when mixed with references.
For example, a `const std::vector<int>&` would be a constant reference to a `std::vector` of ints.
That means that it will be a reference but we can't modify the object referenced.
Essentially somebody reading code with a const reference will know that there is no copy but we won't modify it through the reference.

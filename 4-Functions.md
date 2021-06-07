# Functions
When we wrote `int main() {}` we defined the main function. Let's define other ones.
### Structuing code in a more useful way...
Instead of putting all our code in the main function we can move it to an other function (outside of main):
```cpp
double average(std::vector<double> vec) {
    double sum = 0.0;
    for (double d : vec) {
        sum = sum + d;
    }
    return sum / vec.size();
}
```
We can now rewrite our program like so:
```cpp
// in main...
std::vector<double> vec;
double tmp = 0.0;
while (std::cin >> tmp) {
    vec.push_back(tmp);
}
std::cout << "The average is: " << average(vec);
```
### Note on expessing intent
It is appreciated when reading other pepoles code (it will happend someday) to make it clear what you want to acheive. i.e. instead of using a raw loop we could use an algorithm from `<algorithm>` (`std::find`, `std::count`...) or `<numeric>` (`std::accumulate`...). Keeping that in mind we can rewrite an other time tthis `average` function to be more expressive:
```cpp
#include <numeric>

double average(std::vector<double> vec) { 
     return std::accumulate(vec.begin(), vec.end(), 0.0) / vec.size();
}
```
We pass to `std::accumulate` the beginning of the vector, the end and the initial value of the sum.

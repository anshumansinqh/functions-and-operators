# Function and Operator Overloading

## Aim 
To study Function and Operator Overloading

## Theory
### Definition
#### Function Overloading
- Function overloading is a feature in C++ that allows you to define multiple functions with the same name but with different parameters.
- The compiler differentiates these functions based on the number and/or type of their parameters.
> For example:
```cpp
#include <iostream>
using namespace std;

void print(int num) {
    cout << "Integer: " << num << endl;
}

void print(double num) {
    cout << "Double: " << num << endl;
}

void print(const string& str) {
    cout << "String: " << str << endl;
}

int main() {
    print(5); 
    print(3.14);
    print("Hello, World!");

    return 0;
}

```
#### Operator Overloading
- Operator overloading is a feature in C++ that allows developers to redefine the way operators work for user-defined types (such as classes).
- This enables you to use operators like `+`, `-`, `*`, and others with objects of your classes in a way that is intuitive and similar to built-in types.
> For example:
```cpp
#include <iostream>
using namespace std;

class Point {
private:
    int x, y;

public:
    Point(int xCoord, int yCoord) : x(xCoord), y(yCoord) {}

    Point operator+(const Point& other) {
        return Point(x + other.x, y + other.y);
    }

    void display() const {
        cout << "(" << x << ", " << y << ")" << endl;
    }
};

int main() {
    Point p1(1, 2);
    Point p2(3, 4);
    Point p3 = p1 + p2;

    cout << "Point 1: ";
    p1.display();
    cout << "Point 2: ";
    p2.display();
    cout << "Point 3 (Point 1 + Point 2): ";
    p3.display();

    return 0;
}

```
## Conclusion 
In this experiment we learned how to do Function Overloading in cpp.

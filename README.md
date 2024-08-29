#include <iostream>
using namespace std;

class Circle {
private:
    double radius;

public:
    // Constructor to initialize radius
    Circle() : radius(0.0) {}

    // Setter function for radius
    void setRadius(double r) {
        radius = r;
    }

    // Getter function for radius
    double getRadius() const {
        return radius;
    }

    // Overload the + operator for Circle objects
    Circle operator+(const Circle& c) {
        Circle temp;
        temp.radius = this->radius + c.radius;
        return temp;
    }
};

int main() {
    // Create three objects c1, c2, and c3
    Circle c1, c2, c3;

    // Call setter function for objects c1 and c2
    c1.setRadius(5.5);
    c2.setRadius(4.5);

    // The program should be able to execute the following statement
    c3 = c1 + c2;

    // Call the getter function for c3
    cout << "The radius of c3 is: " << c3.getRadius() << endl;

    return 0;
}

#include <iostream>
using namespace std;

double calcAreaHexagon(double s) {
    return 1.5 * 1.732 * s;
}

double calcPerimeterHexagon(double s) {
    return 6 * s;
}

double calcAngleSum() {
    double angle = 120;
    return 6 * angle;
}

double calcAreaSquare(double s) {
    double length = s + 1;
    return length * 2;
}

double calcPerimeterSquare(double s) {
    double length = s + 1;
    return 4 * length;
}

void displayHexagon(double area, double perimeter, double angleSum) {
    cout << "Area of Hexagon is: " << area << endl;
    cout << "Perimeter of Hexagon is: " << perimeter << endl;
    cout << "Sum of Angles of Hexagon is: " << angleSum << endl;
}

void displaySquare(double area, double perimeter) {
    cout << "Area of Square is: " << area << endl;
    cout << "Perimeter of Square is: " << perimeter << endl;
}

int main() {
    double s = 3;
    cout << "Enter 1 to calculate area, perimeter, sum of all angles of hexagon:" << endl;
    cout << "Enter 2 to calculate area and perimeter of square:" << endl;
    cout << "Enter any other key to exit:" << endl;
    
    char x;
    cin >> x;

    if (x == '1') {
        double areaOfHexagon = calcAreaHexagon(s);
        double perimeterOfHexagon = calcPerimeterHexagon(s);
        double angleSum = calcAngleSum();
        displayHexagon(areaOfHexagon, perimeterOfHexagon, angleSum);
    } else if (x == '2') {
        double areaOfSquare = calcAreaSquare(s);
        double perimeterOfSquare = calcPerimeterSquare(s);
        displaySquare(areaOfSquare, perimeterOfSquare);
    } else {
        
    }
}

#include <iostream>
using namespace std;

void add(double a, double b) {
    cout << "Result: " << a + b << endl;
}

void subtract(double a, double b) {
    cout << "Result: " << a - b << endl;
}

void multiply(double a, double b) {
    cout << "Result: " << a * b << endl;
}

void divide(double a, double b) {
    if (b != 0) {
        cout << "Result: " << a / b << endl;
    } else {
        cout << "Error: Division by zero is not allowed." << endl;
    }
}

int main() {
    double num1, num2;
    char operation;

    cout << "Welcome to the Simple Calculator!" << endl;
    cout << "Enter two numbers: ";
    cin >> num1 >> num2;
    cout << "Enter the operation (+, -, *, /): ";
    cin >> operation;

    switch (operation) {
        case '+':
            add(num1, num2);
            break;
        case '-':
            subtract(num1, num2);
            break;
        case '*':
            multiply(num1, num2);
            break;
        case '/':
            divide(num1, num2);
            break;
        default:
            cout << "Error: Invalid operation." << endl;
    }

    return 0;
}

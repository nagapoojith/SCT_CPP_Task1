# SCT_CPP_Task1
#include <iostream>
using namespace std;

void convertFromCelsius(double celsius) {
    double fahrenheit = (celsius * 9.0 / 5.0) + 32;
    double kelvin = celsius + 273.15;

    cout << "\nTemperature in Fahrenheit: " << fahrenheit << " °F" << endl;
    cout << "Temperature in Kelvin: " << kelvin << " K" << endl;
}

void convertFromFahrenheit(double fahrenheit) {
    double celsius = (fahrenheit - 32) * 5.0 / 9.0;
    double kelvin = celsius + 273.15;

    cout << "\nTemperature in Celsius: " << celsius << " °C" << endl;
    cout << "Temperature in Kelvin: " << kelvin << " K" << endl;
}

void convertFromKelvin(double kelvin) {
    double celsius = kelvin - 273.15;
    double fahrenheit = (celsius * 9.0 / 5.0) + 32;

    cout << "\nTemperature in Celsius: " << celsius << " °C" << endl;
    cout << "Temperature in Fahrenheit: " << fahrenheit << " °F" << endl;
}

int main() {
    int choice;
    double temp;

    cout << "==== Temperature Converter ====" << endl;
    cout << "1. Convert from Celsius" << endl;
    cout << "2. Convert from Fahrenheit" << endl;
    cout << "3. Convert from Kelvin" << endl;
    cout << "Enter your choice (1-3): ";
    cin >> choice;

    switch (choice) {
        case 1:
            cout << "Enter temperature in Celsius: ";
            cin >> temp;
            convertFromCelsius(temp);
            break;
        case 2:
            cout << "Enter temperature in Fahrenheit: ";
            cin >> temp;
            convertFromFahrenheit(temp);
            break;
        case 3:
            cout << "Enter temperature in Kelvin: ";
            cin >> temp;
            convertFromKelvin(temp);
            break;
        default:
            cout << "Invalid choice. Please run the program again." << endl;
    }

    return 0;
}

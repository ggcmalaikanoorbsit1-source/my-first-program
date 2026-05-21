#include <iostream>
#include <cmath>     // For sqrt() and pow()
using namespace std;

int main()
{
    int choice;
    double num1, num2, result;

    do
    {
        cout << "\n====== SIMPLE CALCULATOR ======\n";
        cout << "1. Addition\n";
        cout << "2. Subtraction\n";
        cout << "3. Multiplication\n";
        cout << "4. Division\n";
        cout << "5. Modulus\n";
        cout << "6. Power\n";
        cout << "7. Square Root\n";
        cout << "8. Exit\n";
        cout << "Enter your choice: ";
        cin >> choice;

        switch(choice)
        {
            case 1:
                cout << "Enter two numbers: ";
                cin >> num1 >> num2;
                result = num1 + num2;
                cout << "Result = " << result;
                break;

            case 2:
                cout << "Enter two numbers: ";
                cin >> num1 >> num2;
                result = num1 - num2;
                cout << "Result = " << result;
                break;

            case 3:
                cout << "Enter two numbers: ";
                cin >> num1 >> num2;
                result = num1 * num2;
                cout << "Result = " << result;
                break;

            case 4:
                cout << "Enter two numbers: ";
                cin >> num1 >> num2;

                if(num2 != 0)
                {
                    result = num1 / num2;
                    cout << "Result = " << result;
                }
                else
                {
                    cout << "Division by zero is not possible!";
                }
                break;

            case 5:
            {
                int a, b;
                cout << "Enter two integers: ";
                cin >> a >> b;

                if(b != 0)
                {
                    cout << "Result = " << a % b;
                }
                else
                {
                    cout << "Modulus by zero is not possible!";
                }
                break;
            }

            case 6:
                cout << "Enter base and power: ";
                cin >> num1 >> num2;
                result = pow(num1, num2);
                cout << "Result = " << result;
                break;

            case 7:
                cout << "Enter a number: ";
                cin >> num1;

                if(num1 >= 0)
                {
                    result = sqrt(num1);
                    cout << "Square Root = " << result;
                }
                else
                {
                    cout << "Square root of negative number is not possible!";
                }
                break;

            case 8:
                cout << "Exiting Calculator...";
                break;

            default:
                cout << "Invalid Choice! Please try again.";
        }

    } while(choice != 8);

    return 0;
}

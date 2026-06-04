# new
calculator in c

#include <stdio.h>

int main() {
    char operator;
    double num1, num2, result;

    // 1. Get the desired operator from the user
    printf("Enter an operator (+, -, *, /): ");
    scanf("%c", &operator);

    // 2. Get two numbers from the user
    printf("Enter two operands: ");
    scanf("%lf %lf", &num1, &num2);

    // 3. Perform calculation based on the operator
    switch (operator) {
        case '+':
            result = num1 + num2;
            printf("%.2lf + %.2lf = %.2lf\n", num1, num2, result);
            break;
            
        case '-':
            result = num1 - num2;
            printf("%.2lf - %.2lf = %.2lf\n", num1, num2, result);
            break;
            
        case '*':
            result = num1 * num2;
            printf("%.2lf * %.2lf = %.2lf\n", num1, num2, result);
            break;
            
        case '/':
            // Prevent crash from division by zero
            if (num2 != 0.0) {
                result = num1 / num2;
                printf("%.2lf / %.2lf = %.2lf\n", num1, num2, result);
            } else {
                printf("Error: Division by zero is not allowed.\n");
            }
            break;

        // Handle invalid operators
        default:
            printf("Error: Invalid operator input.\n");
    }

    return 0;
}

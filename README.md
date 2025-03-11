Create a simple Python program that asks the user to input two numbers and a mathematical operation (addition, subtraction, multiplication, or division). Perform the operation based on the user's input and print the result. Example: If a user inputs 10, 5, and +, your program should display 10 + 5 = 15.



def perform_operation(num1, num2, operation):
    if operation == '+':
        result = num1 + num2
    elif operation == '-':
        result = num1 - num2
    elif operation == '*':
        result = num1 * num2
    elif operation == '/':
        # Check for division by zero
        if num2 == 0:
            return "Error: Division by zero is not allowed."
        result = num1 / num2
    else:
        return "Error: Invalid operation."
    
    return f"{num1} {operation} {num2} = {result}"

def main():
    try:
        num1 = float(input("Enter the first number: "))
        num2 = float(input("Enter the second number: "))
        operation = input("Enter the operation (+, -, *, /): ")

        result = perform_operation(num1, num2, operation)
        print(result)
    except ValueError:
        print("Error: Invalid input. Please enter numbers for the calculations.")

if __name__ == "__main__":
    main()

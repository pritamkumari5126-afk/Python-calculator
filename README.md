# Python-calculator
A simple python program
def add(a, b):
    return a + b


def subtract(a, b):
    return a - b


def multiply(a, b):
    return a * b


def divide(a, b):
    if b == 0:
        return "Error: Cannot divide by zero"
    return a / b


def floor_divide(a, b):
    if b == 0:
        return "Error: Cannot divide by zero"
    return a // b


def remainder(a, b):
    if b == 0:
        return "Error: Cannot divide by zero"
    return a % b


def power(a, b):
    return a ** b


def calculator():
    while True:
        print("\n========== PYTHON CALCULATOR ==========")
        print("1. Addition")
        print("2. Subtraction")
        print("3. Multiplication")
        print("4. Division")
        print("5. Floor Division")
        print("6. Remainder")
        print("7. Power")
        print("8. Exit")
        print("=======================================")

        choice = input("Enter your choice (1-8): ")

        if choice == "8":
            print("Thank you for using the calculator!")
            break

        if choice not in ["1", "2", "3", "4", "5", "6", "7"]:
            print("Invalid choice. Please try again.")
            continue

        try:
            a = float(input("Enter first number: "))
            b = float(input("Enter second number: "))
        except ValueError:
            print("Invalid input! Please enter numbers only.")
            continue

        if choice == "1":
            result = add(a, b)

        elif choice == "2":
            result = subtract(a, b)

        elif choice == "3":
            result = multiply(a, b)

        elif choice == "4":
            result = divide(a, b)

        elif choice == "5":
            result = floor_divide(a, b)

        elif choice == "6":
            result = remainder(a, b)

        elif choice == "7":
            result = power(a, b)

        print("Result =", result)


calculator()

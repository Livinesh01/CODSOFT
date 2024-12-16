def calculator():
    print("Welcome to the Calculator!")
    print("Options:")
    print("1: Addition (+)")
    print("2: Subtraction (-)")
    print("3: Multiplication (*)")
    print("4: Division (/)")
    print("5: Exit")
    
    while True:
         try:
            choice = int(input("Choose an operation (1/2/3/4/5): "))
            if choice == 5:
                print("Exiting the calculator. Goodbye!")
                break
            
            if choice in [1, 2, 3, 4]:
                num1 = float(input("Enter the first number: "))
                num2 = float(input("Enter the second number: "))
                
                if choice == 1:
                    print(f"The result of {num1} + {num2} is: {num1 + num2}")
                elif choice == 2:
                    print(f"The result of {num1} - {num2} is: {num1 - num2}")
                elif choice == 3:
                    print(f"The result of {num1} * {num2} is: {num1 * num2}")
                elif choice == 4:
                    if num2 != 0:
                        print(f"The result of {num1} / {num2} is: {num1 / num2}")
                    else:
                        print("Error: Division by zero is not allowed!")
            else:
                print("Invalid choice. Please select a valid operation.")
        except ValueError:
            print("Invalid input! Please enter numeric values.")

# Run the calculator
calculator()

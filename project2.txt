#FUNCTION : MENU

def menu():
    print("\n MENU")
    print("1. Generate a Pattern")
    print("2. Number Analyzer")
    print("3. Exit")

#FUNCTION : PATTERN

def generate_a_pattern():
    rows= int(input("Enter number of rows: "))
    if rows <= 0:
        print("Please enter positive number.")
        return
    print("Generated Pattern:")
    
    # Nested Loop
    for i in range(1, rows + 1):
        for j in range(i):
            print("*", end=" ")

        print()

# FUNCTION : NUMBER ANALYZER

def number_analyzer():
    start = int(input("Enter starting number: "))
    end = int(input("Enter ending number: "))

    if start > end:
        print("Invalidate range!")
        return
    total = 0
    
    print("Number Analysis:")

    for num in range(start, end + 1):
        if num %2 == 0:
            print(num,"is Even")
        else:
            print(num,"is Odd")
#MAIN PROGRAM
print(" Pattern & Number Analyzer ")

while True:
    menu()
    
    choice = input("Enter your choice: ")

    if choice == "1":
        generate_a_pattern()

    elif choice == "2":
        number_analyzer()
        
    elif choice == "3":4
    print("\nProgram Closed.")
    break
else:
    print("Invalid choice!")

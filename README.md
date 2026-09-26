def calculate_average(a1, a2, a3):
    return (a1 + a2 + a3) / 3

while True:
    num_students = int(input("Enter number of students to process (minimum 3): "))
    if num_students >= 3:
        break
    print("Please enter 3 or more students.\n")


for i in range(num_students):
    print(f"\n----- Student {i+1} -----")
    name = input("Enter student's name: ")
    act1 = float(input("Enter Activity 1 score: "))
    act2 = float(input("Enter Activity 2 score: "))
    act3 = float(input("Enter Activity 3 score: "))
    
    average = calculate_average(act1, act2, act3)
    
    # Determine status
    if average >= 90:
        status = "Excellent"
    elif average >= 80:
        status = "Very Good"
    elif average >= 75:
        status = "Passed"
    else:
        status = "Failed"
    
   
    print("\n----- Result -----")
    print(f"Name: {name}")
    print(f"Activity 1: {act1}")
    print(f"Activity 2: {act2}")
    print(f"Activity 3: {act3}")
    print(f"Average: {average:.2f}")
    print(f"Status: {status}")

print("\nAll students processed! ")

# ---------------------------------------------
# Name: Krishyangi Dixit
# Date: 15-Oct-2025
# Project Title: Daily Calorie Tracker
# ---------------------------------------------
# This program helps you record your daily meals,
# calculate total and average calories,
# and check if you stayed within your daily limit.
# ---------------------------------------------

# Task 1: Welcome message
print("🍎 Welcome to the Daily Calorie Tracker 🍎")
print("Track your meals, count your calories, and stay on goal!\n")

# Task 2: Input & Data Collection
meals = []      # to store meal names
calories = []   # to store calorie amounts

# Ask user how many meals they want to enter
num_meals = int(input("How many meals did you have today? "))

# Use a loop to take input for each meal
for i in range(num_meals):
    meal = input(f"\nEnter the name of meal #{i+1}: ")
    cal = float(input(f"Enter calories for {meal}: "))
    meals.append(meal)
    calories.append(cal)

# Task 3: Calorie Calculations
total_calories = sum(calories)
average_calories = total_calories / num_meals

# Ask user for their daily calorie limit
limit = float(input("\nEnter your daily calorie limit: "))

# Task 4: Exceed Limit Warning System
if total_calories > limit:
    print("\n⚠️ You have exceeded your daily calorie limit!")
else:
    print("\n✅ Great job! You are within your calorie goal.")

# Task 5: Summary table using f-string 
print("\n----- DAILY CALORIE SUMMARY -----")
print("Meal Name\tCalories")
print("---------------------------------")
for i in range(num_meals):
    print(meals[i] + "\t" + str(calories[i]))

print("---------------------------------")
print("Total:\t\t" + str(total_calories))
print("Average:\t" + str(round(average_calories, 2)))

print("\n\nTHANK YOU!")

    

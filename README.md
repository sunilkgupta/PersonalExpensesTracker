# Personal Expenses Tracker
It is Personal Expenses Tracker console application developed in Python. It stores data in CSV file and read it from file itself.

Code
    
def add_expense(expenses):
    from datetime import datetime
    date = input("Enter date (YYYY-MM-DD): ")
    category = input('Enter category as "Food" or "Travel"')
    try:
        amount = float(input("Enter amount: "))
    except ValueError:
        print("Invalid amount. Please try again!")
        return
    description = input("Enter short description: ")
    
    try:
        datetime.strptime(date, "%Y-%m-%d")
    except ValueError:
        print("Invalid date format. Use YYYY-MM-DD.")
        return
    
    expense = {
        "date": date, 
        "category": category, 
        "amount" : amount, 
        "description": description
    }
    expenses.append(expense)
    print("Successfully, expense added.")

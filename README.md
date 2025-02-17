CODE:-

from datetime import datetime

def calculate_days_survived(birthdate):
    
    today = datetime.today()
    
    birthdate = datetime.strptime(birthdate, "%d/%m/%Y")
    
    days_survived = (today - birthdate).days
    
    return days_survived

def main():
    print("Welcome to the Days Survived Calculator!")
    
    birthdate = input("Enter your birthdate (DD/MM/YYYY): ")
    
    try:
        days = calculate_days_survived(birthdate)
        print(f"You have survived {days} days in this world!")
    
    except ValueError:
        print("Invalid date format. Please enter the date in DD/MM/YYYY format.")

if __name__ == "__main__":
    main()


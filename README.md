num_of_friends = int(input("How many people are splitting the bill? "))

running_total = 0.0

while True:
    category = input("Enter expense category (or 'done' to finish): ")

    if category.lower() == "done":
        break

    amount = float(input(f"Amount for {category}: "))
    running_total += amount
    print("Current total:", running_total)

    if num_of_friends > 0:
    per_person = running_total / num_of_friends
    per_person = round(per_person, 2)
    print("Total bill:", running_total)
    print("Bill per person:", per_person)
else:
    print("Number of friends must be greater than 0.")

    # main.py
# Simple, open-ended bill splitter

def main():
    print("Welcome to the Bill Splitter!")

    # Get number of friends
    while True:
        try:
            num_of_friends = int(input("How many people are splitting the bill? "))
            if num_of_friends <= 0:
                print("Please enter a number greater than 0.")
            else:
                break
        except ValueError:
            print("Please enter a valid whole number.")

    running_total = 0.0
    expense_count = 0

    # Collect expenses
    while True:
        category = input("Enter expense category (or 'done' to finish): ")

        if category.lower() == "done":
            break

        try:
            amount = float(input(f"Amount for {category}: "))
            if amount < 0:
                print("Amount cannot be negative. Try again.")
                continue
        except ValueError:
            print("Please enter a valid number for the amount.")
            continue

        running_total += amount
        expense_count += 1
        print(f"Added {category}: {amount}")
        print(f"Current total: {running_total}\n")

    if expense_count == 0:
        print("No expenses were added. Nothing to split.")
        return

    # Split and round
    per_person = running_total / num_of_friends
    per_person = round(per_person, 2)

    print("\n--- Summary ---")
    print(f"Number of people: {num_of_friends}")
    print(f"Number of expenses: {expense_count}")
    print(f"Total bill: {running_total}")
    print(f"Bill per person: {per_person}")

if __name__ == "__main__":
    main()

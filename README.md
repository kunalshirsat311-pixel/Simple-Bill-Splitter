# Simple Bill Splitter (CLI)

A beginner-friendly Python command-line app to split any kind of shared expenses between friends.

Instead of hard-coded categories like "food" or "drinks", this tool lets you enter any expense name (travel, fuel, tickets, shopping, etc.), adds everything up, and then divides the total equally among the group.

## Features

- Ask how many people are splitting the bill.
- Add any number of expenses with custom category names.
- See the running total after each expense.
- Handle simple invalid input (non-numeric amounts, zero or negative people).
- Show a short summary: total bill and amount per person (rounded to 2 decimal places).

## How to Run

1. Make sure you have Python 3 installed.
2. Clone this repository:
   ```bash
   git clone https://github.com/your-username/your-repo-name.git
   ```
3. Change into the project folder:
   ```bash
   cd your-repo-name
   ```
4. Run the script:
   ```bash
   python main.py
   ```
   or on some systems:
   ```bash
   python3 main.py
   ```

## How It Works

- The program asks for the number of people.
- Then it repeatedly:
  - asks for an expense category (for example: `travel`, `fuel`, `food`),
  - asks for the amount,
  - adds the amount to a running total.
- When you type `done` as the category, the app stops asking for new expenses.
- Finally, it divides the total by the number of people and prints how much each person should pay, rounded to 2 decimal places.

## Example Flow

- Number of people: 3  
- Expenses:
  - travel: 1500
  - food: 600
  - fuel: 300  

Total = 2400 → each person pays 800.00.

## Possible Future Improvements

- Let each person have a name and track who paid what.
- Allow different split types (for example: one person pays a fixed amount, others split the rest).
- Export the result to a text file or JSON.

This project is mainly for learning purposes and to show basic understanding of Python input, loops, and simple calculations.
   

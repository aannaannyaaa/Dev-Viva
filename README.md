# Dev-Viva

### Objective: Create an expense tracker that allows users to input their expenses and income, and displays a summary. Tasks:

Function addTransaction: Adds an expense or income transaction.
Function calculateTotal: Calculates the total balance based on transactions.
Function displaySummary: Displays a summary of expenses, income, and balance.
Attach addTransaction to the submit button for transactions.
Attach calculateTotal to update the balance after every transaction.

### Approach 

- I’ll start with an empty transactions array to keep track of all my income and expenses. 
- Each time I add a transaction, addTransaction will pop it into this array, and it’ll automatically update my balance and summary. 
- To keep my balance accurate, calculateTotal will add up all income, subtract the expenses, and give me the current balance. 
- Then, displaySummary will pull everything together—showing the total income, expenses, and balance. 
- I’ll hook up addTransaction to the submit button, so every time I enter something new, the balance and summary update instantly.

### Pseudo Code :
- Initialize transactions array

- Function addTransaction(description, amount, type):
    - Create transaction with {description, amount, type}
    - Add transaction to transactions array (Totals will auto-update based on state changes)

- Function getTotals():
    - Initialize income and expenses to 0
    - For each transaction in transactions array:
        - If type is "income", add to income
        - If type is "expense", add to expenses
  - Return {income, expenses, balance: income - expenses}

- Function displaySummary():
    - Display total income, total expenses, and balance from getTotals()

- Event: On form submit:
    - Retrieve input values and call addTransaction()
    - UI automatically reflects updated totals

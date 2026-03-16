# Mini__Project
class BankAccount:
    def __init__(self, owner, balance=0):
        self.owner = owner
        self.balance = balance

    def deposit(self, amount):
        self.balance += amount
        return f"Deposited {amount}, New Balance: {self.balance}"

    def withdraw(self, amount):
        if amount <= self.balance:
            self.balance -= amount
            return f"Withdrew {amount}, New Balance: {self.balance}"
        else:
            return "Insufficient funds"


owner_name = input("Enter account owner's name: ")
initial_balance = float(input("Enter initial balance: "))

acc = BankAccount(owner_name, initial_balance)
deposit_amount = float(input("Enter amount to deposit: "))
print(acc.deposit(deposit_amount))

withdraw_amount = float(input("Enter amount to withdraw: "))
print(acc.withdraw(withdraw_amount))

withdraw_amount2 = float(input("Enter another amount to withdraw: "))
print(acc.withdraw(withdraw_amount2))

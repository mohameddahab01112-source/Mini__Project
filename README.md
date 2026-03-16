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
            return f"Not enough money"

acc = BankAccount("Ali", 1000)
print(acc.deposit(500))
print(acc.withdraw(300))
print(acc.withdraw(1500))

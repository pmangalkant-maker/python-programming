# python-programming
class BankAccount:
    def _init_(self):
        self.balance = 0

    def deposit(self, amount):
        self.balance += amount
        print("Amount Deposited:", amount)

    def withdraw(self, amount):
        if amount > self.balance:
            print("Insufficient balance!")
        else:
            self.balance -= amount
            print("Amount Withdrawn:", amount)

    def show_balance(self):
        print("Current Balance:", self.balance)


# Main Program Loop
account = BankAccount()

while True:
    print("\n===== Simple Bank System =====")
    print("1. Deposit")
    print("2. Withdraw")
    print("3. Check Balance")
    print("4. Exit")

    choice = input("Enter your choice (1-4): ")

    if choice == "1":
        amt = int(input("Enter amount to deposit: "))
        account.deposit(amt)

elif choice == "2":
        amt = int(input("Enter amount to withdraw: "))
        account.withdraw(amt)

    elif choice == "3":
        account.show_balance()

    elif choice == "4":
        print("Thank you for using the Bank System!")
        break

    else:
        print("Invalid choice! Please try again.")

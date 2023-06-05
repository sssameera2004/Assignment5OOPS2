CHALLENGE 3:-

class Student:

    def getName(self):
        return self.__name

    def getRollNumber(self):
        return self.__RollNumber

    def setName(self, name):
        self.__name = name

    def setRollNumber(self, RollNumber):
        self.__RollNumber = RollNumber

demo1 = Student()
demo1.setName("Samchandu")
print("Name:", demo1.getName())
demo1.setRollNumber(1432)
print("Roll Number:", demo1.getRollNumber())

CHALLENGE 4:-
Implement a Banking Account
class Account:
    def __init__(self, title=None, balance=0):
        self.title = title
        self.balance = balance


class SavingsAccount(Account):
    def __init__(self, title=None, balance=0, interestRate=0):
        super().__init__(title, balance)
        self.interestRate = interestRate
CHALLENGE 5:- Handling a Bank Account
METHOD 1:-
class Account:  # parent class
    def __init__(self, title=None, balance=0):
        self.title = title
        self.balance = balance

    def withdrawal(self, amount):
        self.balance = self.balance - amount

    def deposit(self, amount):
        self.balance = self.balance + amount

    def getBalance(self):
        return self.balance
class SavingsAccount(Account):
    def __init__(self, title=None, balance=0, interestRate=0):
        super().__init__(title, balance)
        self.interestRate = interestRate

    def interestAmount(self):
        return (self.balance * self.interestRate / 100)
demo1 = SavingsAccount("Mark", 2000, 5)  # initializing a SavingsAccount
METHOD 2:-
class BankAccount:
    # create the constuctor with parameters: accountNumber, name and balance 
    def __init__(self,accountNumber, name, balance):
        self.accountNumber = accountNumber
        self.name = name
        self.balance = balance
        
    # create Deposit() method
    def Deposit(self , d ):
        self.balance = self.balance + d
    
    # create Withdrawal method
    def Withdrawal(self , w):
        if(self.balance < w):
            print("impossible operation! Insufficient balance !")
        else:
            self.balance = self.balance - w
    # create bankFees() method
    def bankFees(self):
        self.balance = (95/100)*self.balance
        
    # create display() method
    def display(self):
        print("Account Number : " , self.accountNumber)
        print("Account Name : " , self.name)
        print("Account Balance : " , self.balance , "Rs")
# Testing the code :
newAccount = BankAccount(181909121511, "Samchandu" , 2700)
# Creating Withdrawal Test
newAccount.Withdrawal(300)
# Create deposit test
newAccount.Deposit(200)
# Display account informations
newAccount.display()


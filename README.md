# class

class Car: 
    def __init__(self, brand, year):
         self.brand = brand
         self.year = year
    
    def drive(self): 
        print(f"Mašīna {self.brand} brauc!")

car1 = Car("Toyota" , 2010)
car2 = Car("Ferrari" , 2006)
car3 = Car("Alfa Romeo" , 2001)


cars = [
    Car("Toyota" , 2010),
    Car("Ferrari" , 2006),
    Car("Alfa Romeo" , 2001)
]

for car in cars:
    print(car.brand)

print(f"{car1.brand}, {car1.year}" )
print(f"{car2.brand}, {car2.year}" )
print(f"{car3.brand}, {car3.year}" )

class Person:
    def __init__(self,name,age):
        self.name = name 
        self.age = age
        print(f"Sveiks, {self.name}, tev ir {self.age} gadi!")

person1 = Person("Lija", 52)
person2 = Person("Sonja", 67)


class Animal:
    def make_sound(self):
        print("Dzīvnieks izdod skaņu.")


class Dog(Animal):
    def make_sound(self):
        print("Vau vau!")

animal = Animal()
dog = Dog()


animal.make_sound()
dog.make_sound()


class BankAccount:
    def __init__(self, owner, balance=0):
        self.owner = owner
        self.balance = balance

    def deposit(self, amount):
        self.balance += amount
        print(f"{self.owner} iemaksāja {amount} €. Jaunais atlikums: {self.balance} €")

    def withdraw(self, amount):
        if amount <= self.balance:
            self.balance -= amount
            print(f"{self.owner} izņēma {amount} €. Jaunais atlikums: {self.balance} €")
        else:
            print("Nepietiek līdzekļu!")

    def info(self):
        print(f"Konta īpašnieks: {self.owner}, atlikums: {self.balance} €")


acc1 = BankAccount("Anna")
acc1.deposit(100)
acc1.withdraw(30)
acc1.info()

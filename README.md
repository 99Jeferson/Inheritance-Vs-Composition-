# Inheritance-Vs-Composition-
# 1. Inheritance
# Definition 
Inheritance is  a mechanism where one class acquires the properties and behaviors of another class.
It represents an "IS-A" relationship.

Example: A dog is an Animal.
# Code Example 
# Parent Class
class Animal:
    def __init__(self, name):
        self.name = name

    def speak(self):
        print("Animal makes a sound")

# Child Class
class Dog(Animal):
    def speak(self):
        print(f"{self.name} says Woof!")

# Code Flow
dog1 = Dog("Buddy")
dog1.speak()
# Code Flow Explanation 
1. Dog class inherits from Animal.
2. Dog ("Budy") calls the constructor from Animal
3. Dog1. speak () executes the overidden method in Dog
# Key Characteristics of Inheritance.
- Creates tight coupling
- Allows nethod overriding
- Forms a class hierarchy
- Represents IS-A relationship
# 2. Composition
# Definition
Composition is when a class contains another class as a member.
It represents a "HAS-A" relationship.
Example: A car has an Engine.
# Code Example 
# Component Class
class Engine:
    def start(self):
        print("Engine starts")

# Main Class
class Car:
    def __init__(self):
        self.engine = Engine()  # Car HAS-A Engine

    def start_car(self):
        print("Starting car...")
        self.engine.start()

# Code Flow
my_car = Car()
my_car.start_car()
# Code flow Explanation
1. Car creates an instance of Engine
2. Cae.start_cacr() calls Engine.start()
# Key Characteristics of Composition
- Loose coupling
- More flexible
- Encourages module design
- Represents HAS-A relationship
- Preferred in modern software design (e.g, microservices)

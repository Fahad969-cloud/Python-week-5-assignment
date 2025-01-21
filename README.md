Assignment 1: Design Your Own Class! 🏗️
Create a class representing anything you like (a Smartphone, Book, or even a Superhero!).
Add attributes and methods to bring the class to life!
Use constructors to initialize each object with unique values.
Add an inheritance layer to explore polymorphism or encapsulation.


class Smartphone:

    def __init__(self, brand, model, battery_life, storage):
        self.brand = brand  # Brand of the smartphone (e.g., Apple, Samsung)
        self.model = model  # Model of the smartphone (e.g., iPhone 13, Galaxy S21)
        self.__battery_life = battery_life  # Battery life in hours (private attribute)
        self.storage = storage  # Storage in GB (e.g., 128GB, 256GB)


    def get_battery_life(self):
        return self.__battery_life


    def set_battery_life(self, new_battery_life):
        if new_battery_life > 0:
            self.__battery_life = new_battery_life
        else:
            print("Battery life must be a positive number.")

    def display_info(self):
        print(f"Brand: {self.brand}, Model: {self.model}, Battery Life: {self.__battery_life} hours, Storage: {self.storage}GB")

class GamingSmartphone(Smartphone):
    def __init__(self, brand, model, battery_life, storage, gpu_type):
        super().__init__(brand, model, battery_life, storage)  # Calling the parent class constructor
        self.gpu_type = gpu_type  # Specific attribute for gaming smartphones

    def display_info(self):
        super().display_info()  # Calling the parent class display_info method
        print(f"GPU Type: {self.gpu_type}")



smartphone1 = Smartphone("Apple", "iPhone 13", 20, 128)
gaming_phone = GamingSmartphone("Asus", "ROG Phone 5", 18, 512, "Adreno 660")

smartphone1.display_info()
print()
gaming_phone.display_info()


smartphone1.set_battery_life(25)
print(f"Updated Battery Life: {smartphone1.get_battery_life()} hours")



Create a program that includes animals or vehicles with the same action (like move()). However, make each class define move() differently (for example, Car.move() prints "Driving" 🚗, while Plane.move() prints "Flying" ✈️).

class Animal:
    def __init__(self, name):
        self.name = name

    def move(self):
        raise NotImplementedError("Subclasses must implement the move() method")


class Dog(Animal):
    def move(self):
        print(f"{self.name} is running 🐶")


class Bird(Animal):
    def move(self):
        print(f"{self.name} is flying 🐦")


class Car:
    def __init__(self, brand):
        self.brand = brand

    def move(self):
        print(f"{self.brand} is driving 🚗")


class Plane:
    def move(self):
        print("The plane is flying ✈️")


my_dog = Dog("Buddy")
my_bird = Bird("Tweety")
my_car = Car("Tesla")
my_plane = Plane()

my_dog.move()
my_bird.move()
my_car.move()
my_plane.move()



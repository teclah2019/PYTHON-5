# PYTHON-5

# Assignment 1: Smartphone Class

class Smartphone:
    def __init__(self, brand, model, price, battery_life):
        self.brand = brand  # public attribute
        self.model = model  # public attribute
        self._price = price  # private attribute (encapsulation)
        self._battery_life = battery_life  # private attribute (encapsulation)

    def turn_on(self):
        print(f"The {self.brand} {self.model} is now ON.")

    def make_call(self, number):
        print(f"Calling {number} from {self.brand} {self.model}...")

    def battery_status(self):
        print(f"Battery status of {self.brand} {self.model}: {self._battery_life}%")

    def set_price(self, price):
        if price > 0:
            self._price = price
        else:
            print("Invalid price.")

    def get_price(self):
        return self._price

# Create an instance of Smartphone
phone = Smartphone("Apple", "iPhone 13", 999, 85)
phone.turn_on()
phone.make_call("123-456-7890")
phone.battery_status()

# Set a new price
phone.set_price(1050)
print(f"Updated price: ${phone.get_price()}")



# Assignment 2: Polymorphism with Car and Plane

class Car:
    def __init__(self, make, model):
        self.make = make
        self.model = model

    def move(self):
        print(f"The {self.make} {self.model} is driving 🚗.")

class Plane:
    def __init__(self, make, model):
        self.make = make
        self.model = model

    def move(self):
        print(f"The {self.make} {self.model} is flying ✈️.")

# Create instances of Car and Plane
car = Car("Toyota", "Camry")
plane = Plane("Boeing", "747")

# Call move() on both objects
car.move()  # Output: The Toyota Camry is driving 🚗.
plane.move()  # Output: The Boeing 747 is flying ✈️.

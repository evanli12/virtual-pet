# Virtual Pet Program - FBLA 2025–2026
# Author: [Evan Li, Jihoo Byun]
# Description: A simple text-based virtual pet game that teaches users about
# pet care and budgeting.

class Pet:
    def __init__(self, name, pet_type):
        self.name = name
        self.pet_type = pet_type
        self.hunger = 50
        self.energy = 50
        self.happiness = 50
        self.health = 100
        self.money = 100
        self.expenses = 0

    # ----------------------------
    # Pet Actions
    # ----------------------------

    def feed(self):
        cost = 10
        if self.money >= cost:
            self.hunger = max(0, self.hunger - 20)
            self.money -= cost
            self.expenses += cost
            print(f"You fed {self.name}. Hunger decreased!")
        else:
            print("Not enough money to buy food!")

# AliMustafa_261942231_lab9
class Person:
    def __init__(self, name, age):
        self.name = name
        self.age = age

class House:
    def __init__(self, address, num_rooms):
        self.address = address
        self.num_rooms = num_rooms
        self.residents = []

    def addresident(self, person):
        self.residents.append(person)

    def removeresident(self, person):
        if person in self.residents:
            self.residents.remove(person)

    def printresidents(self):
        print("Residents of", self.address)
        for resident in self.residents:
            print(resident.name, "-", resident.age)

person1 = Person("Ali", 23)
person2 = Person("Baber", 25)

house = House("fcc 216", 3)
house.addresident(person1)
house.addresident(person2)

house.printresidents()

print( "removing baber person from the fcc")
house.removeresident(person2)

house.printresidents()

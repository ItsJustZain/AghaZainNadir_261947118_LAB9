class Person:
    def __init__(self, name, age):
        self.name = name
        self.age = age

class House:
    def __init__(self, address, num_of_rooms):
        self.address = address
        self.num_of_rooms = num_of_rooms
        self.people = []

    def add_person(self, person):
        self.people.append(person)

    def remove_person(self, person):
        self.people.remove(person)

    def display_people(self):
        print(f"People living at: {self.address}, rooms: {self.num_of_rooms}")
        for person in self.people:
            print(f"    {person.name}, {person.age} years old")

steve = Person("Steve Jobs", 23)
elon = Person("Elon Musk", 50)
joma = Person("Joma Tech", 32)

house = House("90 Bedford Street", 3)
house.add_person(steve)
house.add_person(elon)

house.display_people()

house.remove_person(steve)

house.display_people()

house.add_person(joma)

house.display_people()

house.add_person(steve)

house.display_people()

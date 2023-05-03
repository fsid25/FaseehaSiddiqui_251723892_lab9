# FaseehaSiddiqui_251723892_lab9

#Faseehasiddiqui 251723892 lab 9

#Question 1
class person:
    def __init__(self,name,age):
        self.name=name
        self.age=age

class house:
    def __init__(self,address, room_num):
        self.address=address
        self.room_num=room_num
        self.people=[]

    def add_person(self,name,age):
        for n in range(len(name)):
            res=person(name[n],age[n])
            self.people.append(res)

    def remove_person(self):
        indiv=input("which name do you want to remove? ").lower()
        for p in self.people:
            if p.name.lower() ==indiv:
                self.people.remove(p)
                return

    def display(self):
        print("People living at ", self.address,"are: ")
        for i in self.people:
            print(i.name,"lives at this adrress and their age is ", i.age)

#creating objects
obj_h=house("23 Baker st main Boulvard",5)

obj_h.add_person(["Alma","Katie","Matt"],[24,12,65])

print("After adding the new name: ")

obj_h.add_person(["Ariel"],[34])

obj_h.display()
print()
obj_h.remove_person()
print()
print("After removing the name: ")
obj_h.display()

### OOP
#membuat sebuah kelas
class Cat:
    def __init__(self,name,breed, age):
        self.name = name
        self.breed = breed
        self.age = age
    def speak(self):
        print("meow, my name is : ", self.name)

cat1 = Cat("aril","anggora", 1)
cat1.speak()
cat2 = Cat("dea","persia",2)
cat2.speak()
print(cat1.name,cat1.breed,cat1.age)
print(cat2.name,cat2.breed,cat2.age)

#inheritance
# parent class
class Person:
    def __init__(self,name, npm):
        self.name = name
        self.npm = npm
    def display(self):
        print(self.name,self.npm,self.salary)
        #print(self.npm)
#child class
class Employe(Person):
    def __init__(self,name,npm,salary):
        self.salary = salary
        Person.__init__(self,name,npm)
#object employe
a = Employe('Dea',2317051027, 500000000)
a.display()

#polymorphism
class Bird:
    def intro(self):
        print("Ada banyak tipe burung")
    def flight(self):
        print("Kebanyakan burung bisa terbang, tetapi ada beberapa yang tidak bisa terbang")
class Eagle(Bird):
    def flight(self):
        print("Elang bisa terbang")
class Penguin(Bird):
    def flight(self):
        print("Penguin tidak bisa terbang")
obj_bird =Bird()
obj_eagle =Eagle()
obj_penguin = Penguin()
obj_bird.intro()
obj_bird.flight()
#obj_eagle.intro()
obj_eagle.flight()
#obj_penguin.intro()
obj_penguin.flight()

#encapsulation
class Mobil:
    def __init__(self, merk, type):
        self.merk = merk
        self.type = type
    def tampilkan_merk(self):
        print ("Merk : ",self.merk)
        print ("type : ", self.type)
jip = Mobil('Inova','Matic')
jip.tampilkan_merk()
print(jip.merk,jip.type)

class Car:
    def __init__(self, brand, color):
        self.brand = brand
        self.color = color
    def display_info(self):
        print ("Merk :",self.brand) 
        print ("Warna :",self.color)
mobil = Car("Toyota","Merah")
mobil.display_info()

class ElectricCar:
    def display_battery_info(self, brand, color, batery):
        self.batery = batery
        print ("Merk : ",self.brand)
        print ("Warna : ",self.color)
        print ("Baterai: ",self.batery)
batery = ElectricCar("Honda","Biru","100kWh")
batery.display_batery_info()

    


###DASAR
# a = int (input()) #input di terminal
# a = 5
# if a % 2 == 0 :
#     print("Bilangan Genap")
# else: 
#     print("Bilangan Ganjil")

# A = "8"
# print(A)
# print(type(A))
# a = 3
# print(a)
# print(type(a))

# x = 0
# if x > 0:
#     print("Positif")
# elif x ==0:
#     print("nol")
# else:
#     print("Negatif")

# for i in range(10):
#     print(i*2) # mencetak bilangan genap sebanyak 10 bilangan

# angka = 1
# while angka < 8:
#     print(angka)
#     angka +=2

#my_list = [] #input angka diterminal
# fruits = ["anggur","pisang","pir"]
# numbers = [1,2,3,4,5]
#my_list = [1,"apel",True,3.6]

#mytup = (2,3,4)
myset = {1,2,3}
print(myset)






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






###REKRUSIF
#membuat fungsi faktorial
def factorial(n):
    if (n==0):
        return 1
    else:
        return n*factorial(n-1)
x = factorial(5)
print("hasil : ",x)

#mencari nilai maksimum
# def cari_maksimal(list_angka):
#     if len(list_angka) == 1:#menghitung panjang list
#         return list_angka[0]
#     else:
#         max_sebelumnya = cari_maksimal(list_angka[1:])
#         if list_angka[0] > max_sebelumnya:
#             return list_angka[0]
#         else:
#             return max_sebelumnya
# angka = [9,12,3,7,22,5,14]
# print(angka)
# print("Nilai Terbesar: ", cari_maksimal(angka))

#binary search
# def binary_search(arr, low, high, x):#low index awal
#     if high >= low:#apakah high lebih besar dri low
#         mid = (high+low)//2#menghitung indeks array
#         if arr[mid]== x:#jika nilai tengah = x maka akan dikembalikan
#             return mid
#         elif arr[mid] >x:
#             return binary_search(arr,low, mid-1,x)
#         else:
#             return binary_search(arr,mid+1, high, x)
#     else:
#         return -1
    
# arr = [2,3,4,10,40]
# x = 50
# result = binary_search(arr, 0, len(arr)-1,x)

# if result != -1:
#     print("Angka ditemukan dalam index ",str(result))#str type data
# else:
#     print("Angka tidak ditemukan dalam array")

def luas_segitiga(alas, tinggi):
    if alas == 0 or tinggi == 0 :
        return 0
    else: 
        return (alas * tinggi)/2

x = luas_segitiga(2,3)
print("luas : ",x )


###ARRAYBASEDSEQUENCES
#list
# hewan = ['kucing','hiu','burung','cicak']
# print(hewan)
# print(len(hewan))#menghitung panjang
# print(hewan[0])
# print(hewan[1])
# hewan[1]= 'ulet'#mengganti hewan
# print(hewan)
# hewan.append('kanguru')#menambahkan list
# print(hewan)


#tuple
#mahasiswailkom = ('dea','alia','febri','lekok','dea')
# mahasiswa = 'dea','alia'
# mahasiswa2 = 'febri',
# mahasiswa3 = ("Lekok",)
# print(type(mahasiswailkom))
# print(type(mahasiswa))
# print(type(mahasiswa2))
# print(type(mahasiswa3))
# print(mahasiswailkom[3])#menulis dari awal keakhir
# print(mahasiswailkom[-2])
# print(mahasiswailkom[-3])
# print(mahasiswailkom[0])
# convert_tuple = list(mahasiswailkom)#mengganti tuple
# convert_tuple[1]= 'anin'
# mahasiswailkom = tuple(convert_tuple)
# print(mahasiswailkom)
# jml = mahasiswailkom.count('dea')#menghitung brp banyak dea
# print(f"Nama dea sebanyak {jml} kali") 
# firstname = 'dea'#menghitung jml karakter
# lastname = 'delvinata'
# fullname = firstname + " " + lastname
# print(fullname)
# print(firstname)
# print(lastname)
# print(len(fullname))
# upper = fullname.upper()
# lower = fullname.lower()
# print('method upper : ', upper)
# print('method lower : ', lower)

A = 'aku suka makan ayam betina'
print(A)
B = A.replace('makan','cium')
print(B)





###STACKANDQUEUE
class Stack:
    def __init__(self):
        self.items=[]
    def is_empty(self):
        return self.items==[]
    def push(self,item):
        self.items.append(item)
    def pop(self):
        if not self.is_empty():
            return self.items.pop()
        else:
            print("stack kosong")
    def peek(self):
        if not self.is_empty():
            return self.items[-1]
        else:
            print("stack kosong")
    def size(self):
        return len(self.items)

s= Stack()
# s.push(1)#kalau append itu nambahin datanya satu satu
# s.push(2)#push masukin data
# s.push(3)
# print("stuck",s.items)
# print("stuck akhir :",s.peek())
# print("buang : ",s.pop())
# print("stack setelah dibuang : ",s.items)
while True:
    print("Pilih Kategori")
    print("1. Push")
    print("2. Pop")
    print("3. Peek")
    print("4. Menampilkan Seluruh Data")
    print("5. Exit")
    pilihan = input("Silahkan Pilih Nomor :")
    if pilihan == '1':
        item = input("push :")
        s.push(item)
        print(item,"berhasil diinput")
    elif pilihan == '2':
        item = s.pop()
        if item is not None:
            print(" Data ",item,"dihapus")
    elif pilihan == '3':
        item = s.peek()
        if item is not None:
            print("Data paling akhir:", item)
    elif pilihan == '4':
        if not s.is_empty():
            print("Isi Data:", s.items)
        else:
            print("Stack kosong.")
    elif pilihan == '5':
        print("Program selesai.")
        break        


    

    


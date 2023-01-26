# -16.7.1
Откройте сайт «‎Дом питомца» и на основе имеющихся в нем данных создайте конструктор класса Cat со следующими параметрами: имя, пол, возраст.  В отдельный файл импортируйте и создайте объект Cat, который выводит имеющихся на сайте котов, с одинаковыми параметрами, но с разными значениями. 

class Cat:

    def __init__(self, name, gender, age):
        self.name = name
        self.gender = gender
        self.age = age

    def getName(self):
        return self.name

    def getGender(self):
        return self.gender

    def getAge(self):
        return self.age


cat1 = Cat ("Сэм", "male", 2)
cat2 = Cat ("Барон", "male", 2)
cat3 = Cat ("Пуся", "female", 5)

cats = [cat1, cat2, cat3]

for item in cats:
    if isinstance(item, Cat):
        if item.gender == "male":
            gender_label = "кот"
        else:
            gender_label = "кошка"
        print(f"{gender_label}, имя  {item.name}, возраст {item.age}")

    else:
        print("-Дом питомца-")
        

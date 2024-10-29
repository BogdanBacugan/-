# Тема 8
Отчет по Теме #8 выполнила:
- Дробышева Екатерина
- ИВТ-22-1

| Задание | Лаб_раб | Сам_раб |
| - | - | - |
| Задание 1 | + | + |
| Задание 2 | + | + |
| Задание 3 | + | + |
| Задание 4 | + | + |
| Задание 5 | + | + |


# Лабараторные работы 
   ## Лабараторная работа 1

  ```python
class Car:
    def __init__(self, make, model):
        self.make = make
        self.model= model

my_car=Car("Save", "Me")
```
  ### Результат
  ![image](https://github.com/user-attachments/assets/0a41d25a-b165-47f5-be2a-b101e345c2f8)
## Лабараторная работа 2
  
 ```python
class Car:
    def __init__(self, make, model):
        self.make = make
        self.model= model

    def drive(self):
        print(f"Driving the {self.make} {self.model}")
my_car=Car("Save", "Me")
my_car.drive()
```

### Результат

![image](https://github.com/user-attachments/assets/0a41d25a-b165-47f5-be2a-b101e345c2f8)


## Лабараторная работа 3
  
 ```python
class Car:
    def __init__(self, make, model):
        self.make = make
        self.model= model

    def drive(self):
        print(f"Driving the {self.make} {self.model}")

class ECar(Car):
    def __init__(self, make, model, bc):
        super().__init__(make, model)
        self.bc = bc

    def charge(self):
        print(f"Charging the {self.make} {self.model} with {self.bc} kWh")

my_Ecar=ECar("Tesla", "S", 75)
my_Ecar.drive()
my_Ecar.charge()
```
### Результат

![image](https://github.com/user-attachments/assets/dfd5ac3d-d32f-422e-88f1-d2647ff50cc3)


## Лабараторная работа 4

 ```python
class Car:
    def __init__(self, make, model):
        self.make = make
        self.model= model

    def drive(self):
        print(f"Driving the {self.make} {self.model}")


my_car=Car("Tesla", "S")
print(my_car.make)
my_car.drive()
```
### Результат

![image](https://github.com/user-attachments/assets/0b83b167-9aa2-4649-839f-d9eef4aeed76)


## Лабараторная работа 5

 ```python
class Shape:
    def area(self):
        pass

class Rectangle(Shape):
    def __init__(self, width, height):
        self.width = width
        self.height = height
    
    def area(self):
        return self.width * self.height
    
class Circle(Shape):
    def __init__(self, radius):
        self.radius = radius

    def area(self):
        return 3,14*self.radius*self.radius
```
### Результат

![image](https://github.com/user-attachments/assets/c9f9a762-e32e-4011-b177-da9c7cdeb9e9)




# Самостоятельные работы

## Самостоятельная работа №1

 ```python
class Mood:
    def __init__(self, food, sleep):
        self.food = food
        self.sleep= sleep

    def awail(self):
        print(f"I have {self.food} {self.sleep}")

my_mood=Mood("No food", "No sleep")
my_mood.awail()
```

### Результат

![image](https://github.com/user-attachments/assets/29a2b36b-11ce-4d17-a9a2-80c9feb62fba)


## Краткий вывод:
Класс — это шаблон для создания объектов. Он определяет свойства (атрибуты) и поведение (методы) объектов
 
## Самостоятельная работа №2

 ```python
class Mood:
    def __init__(self, food, sleep):
        self.food = food
        self.sleep= sleep

    def awail(self):
        print(f"I have {self.food} {self.sleep}")

my_mood=Mood("No food", "No sleep")
my_mood.awail()
```

### Результат

![image](https://github.com/user-attachments/assets/56c6e896-17fe-47e9-b47e-78efae4c9b17)


## Краткий вывод:

Атрибуты в объектно-ориентированном программировании представляют собой переменные, которые хранят состояние объекта и определяют его характеристики

## Самостоятельная работа №3

 ```python
class Mood:
    def __init__(self, food, sleep):
        self.food = food
        self.sleep= sleep

class EMood(Mood):
    def __init__(self, food, sleep, emoites):
        super().__init__(food, sleep)
        self.e = emoites

    def feel(self):
        print(f"I have {self.food} {self.sleep} and {self.e}")
my_mood=EMood("no food", "no sleep", "depression")
my_mood.feel()
```

### Результат

![image](https://github.com/user-attachments/assets/33c6c182-70c2-4492-9304-672220d0b1db)


## Краткий вывод:

Наследование позволяет создавать новые классы на основе существующих. Новый класс (подкласс) наследует атрибуты и методы родительского класса (суперкласса), что способствует повторному использованию кода и улучшает его структуру.

## Самостоятельная работа №4

 ```python
class Mood:
    def __init__(self, food, sleep):
        self.food = food
        self.sleep= sleep

class EMood(Mood):
    def __init__(self, food, sleep, emoites):
        super().__init__(food, sleep)
        self.e = emoites

    def feel(self):
        print(f"I have {self.food} {self.sleep} and {self.e}")
my_mood=EMood("no food", "no sleep", "depression")
my_mood.feel()
```

### Результаты

![image](https://github.com/user-attachments/assets/34a3e14e-47bb-4cb9-9fa2-f24f2e5b6bdd)


## Краткий вывод:

Инкапсуляция позволяет скрывать внутренние детали реализации и защищать состояние объекта от несанкционированного доступа. Это достигается с помощью модификаторов доступа (например, использование одного или двух подчеркиваний перед именем атрибута).

## Самостоятельная работа №5

 ```python
class Mood:
    def __init__(self, food, sleep):
        self.food = food
        self.sleep= sleep

class EMood(Mood):
    def __init__(self, food, sleep, emoites):
        super().__init__(food, sleep)
        self.e = emoites

    def feel(self):
        print(f"I have {self.food} {self.sleep} and {self.e}")
my_mood=EMood("no food", "no sleep", "depression")
my_mood.feel()
```

### Результат

![image](https://github.com/user-attachments/assets/1344fe78-3470-4edf-bef3-cb12b466e285)


## Краткий вывод:

Полиморфизм позволяет использовать объекты разных классов через единый интерфейс. Это означает, что один и тот же метод может вести себя по-разному в зависимости от объекта, который его вызывает

# Общий вывод 

Объектно-ориентированное программирование — это парадигма программирования, которая основывается на концепции "объектов", представляющих собой экземпляры классов. ООП позволяет организовывать код таким образом, чтобы он был более структурированным, переиспользуемым и удобным для сопровождения

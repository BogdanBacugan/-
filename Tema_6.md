# Тема 6. Функции и модули
Отчет по Теме #6 выполнил:
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

  В школе, где вы учились, узнали, что вы крутой программист и попросили написать программу для учителей, которая будет при вводе кабинета писать для него ключ доступа и статус, занят кабинет или нет. При написании программы необходимо использовать словарь (dict), который на вход получает номер кабинета, а выводит необходимую информацию. Если кабинета, который вы ввели нет в словаре, то в консоль в виде значения ключа нужно вывести “None” и виде статуса вывести “False”.
По большому счету написав данную программу мы с вами научились заменять иногда громоздкую конструкцию if/elif/else. Поскольку здесь функционал словаря полностью повторяет функционал условия, но при этом у использования словарей в более сложных программах есть намного больше возможностей реализации.

  ```python
request = int(input("№ Кабинета: "))

dictionary = {
    101: {"key": 1234, "access": True},
    102: {"key": 1337, "access": True},
    103: {"key": 8943, "access": True},
    104: {"key": 5555, "access": False},
    None: {"key": None, "access": False},

}

response = dictionary.get(request)
if not response:
    response = dictionary[None]
key = response.get("key")
access = response.get("access")
print(key, access)

```
  ### Результат
  
![image](https://github.com/user-attachments/assets/40967ca1-79ff-4ff2-a5b8-e3988e0f5bc3)


## Лабараторная работа 2

  Алексей решил создать самый большой словарь в мире. Для этого он придумал функцию dict_maker (**kwargs), которая принимает неограниченное количество параметров «ключ: значение» и обновляет
созданный им словарь my_dict, состоящий всего из одного элемента
«first» со значением «so easy». Помогите Алексею создать данную функцию.

 ```python
from pprint import pprint

my_dict = {"first": "so easy"}


def dict_maker(**kwargs):
    my_dict.update(**kwargs)


dict_maker(a1=1, a2=2, a3=3, a4=13)
dict_maker(name="Alex", age=20, weight=70)
pprint(my_dict)

```

### Результат

![image](https://github.com/user-attachments/assets/8b2bffe7-1fe1-49cc-8a55-f8c8a91a0d35)

## Лабараторная работа 3

  Для решения некоторых задач бывает необходимо разложить строку на отдельные символы. Мы знаем что это можно сделать при помощи split(), у которого более гибкая настройка для разделения для этого, но если нам нужно посимвольно разделить строку без всяких условий, то для этого мы можем использовать кортежи (tuple). Для этого напишем любую строку, которую будем делить и “обвернем” ее в tuple и дальше мы можем как нам угодно с ней работать, например, сделать ее списком (тогда получится полный аналог split()) или же работать с ним дальше, как с кортежем.
  
 ```python
sstring = "Hello world"
res = tuple(sstring)
print(res)
print(list(res))

```
### Результат

![image](https://github.com/user-attachments/assets/2fcbd966-c538-48f2-a1d9-070acc8826c5)


## Лабараторная работа 4

  Вовочка решил написать крутую функцию, которая будет писать имя, возраст и место работы, но при этом на вход этой функции будет поступать кортеж. Помогите Вовочке написать эту программу.

 ```python
def pers_info(name, age, company="unnamed"):
    print(f"Name: {name} Age: {age} Company: {company}")


tom = ("Tom", 22)
bob = ("Bob", 30, "Google",)

pers_info(*tom)
pers_info(*bob)

```
### Результат
![image](https://github.com/user-attachments/assets/51be192e-db49-4f85-b83f-53c4536132d4)


## Лабараторная работа 5

  Для сопровождения первых лиц государства X нужен кортеж, но никто не может определиться с порядком машин, поэтому вам нужно написать функцию, которая будет сортировать кортеж, состоящий из целых чисел по возрастанию, и возвращает его. Если хотя бы один элемент не является целым числом, то функция возвращает исходный кортеж.

 ```python
def tuple_sort(tpl):
    for elm in tpl:
        if not isinstance(elm, int):
            return tpl
    return tuple(sorted(tpl))


if __name__ == '__main__':
    print(tuple_sort((5, 5, 6, 6, 1, 2, 3, 9)))
    print(tuple_sort)

```
### Результат

![image](https://github.com/user-attachments/assets/3d042e04-86f4-4839-911a-64796da0611c)




# Самостоятельные работы

## Самостоятельная работа №1

 При создании сайта у вас возникла потребность обрабатывать данные пользователя в странной форме, а потом переводить их в нужные вам форматы. Вы хотите принимать от пользователя последовательность чисел, разделенных пробелом, а после переформатировать эти данные в список и кортеж. Реализуйте вашу задумку. Для получения начальных данных используйте input(). Результатом программы будет выведенный список и кортеж из начальных данных.

 ```python
mass = input("Here: ")

my_list = list(mass.split())
my_tuple = tuple(mass.split())

print(my_list)
print(my_tuple)

```
### Результат

![image](https://github.com/user-attachments/assets/830b9d21-7865-4bb4-9ffd-49243d9517d6)


## Краткий вывод:
   В программе создаётся переменная mass, в которую записывается введённая пользователем строка. Затем при помощи встроенной функции split строка разбивается на элементы и записывается сперва в список, затем в кортеж. В конце список и кортеж выводятся в консоль.
 
## Самостоятельная работа №2
  Николай знает, что кортежи являются неизменяемыми, но он очень упрямый и всегда хочет доказать, что он прав. Студент решил создать функцию, которая будет удалять первое появление определенного элемента из кортежа по значению и возвращать кортеж без него. Попробуйте повторить шедевр не признающего авторитеты начинающего программиста. Но учтите, что Николай не всегда уверен в наличии элемента в кортеже (в этом случае кортеж вернется функцией в исходном виде).
Входные данные:
(1, 2, 3), 1)
(1, 2, 3, 1, 2, 3, 4, 5, 2, 3, 4, 2, 4, 2), 3)
(2, 4, 6, 6, 4, 2), 9)
Ожидаемый результат:
(2, 3)
(1, 2, 1, 2, 3, 4, 5, 2, 3, 4, 2, 4, 2)
(2, 4, 6, 6, 4, 2)

 ```python
def remove(kort, removeNum):
    my_list = list(kort)
    for i in range(len(my_list)):
        if my_list[i] == removeNum:
            my_list.pop(i)
            return my_list
    return kort


print(remove((1, 2, 3), 1))
print(remove((1, 2, 3, 1, 2, 3, 4, 5, 2, 3, 4, 2, 4, 2), 3))
print(remove((1, 2, 3, 4, 5), 6))

```

### Результат

![image](https://github.com/user-attachments/assets/5d850545-40d9-4eb5-ae77-201f73bf15a2)


## Краткий вывод:
Для обхода неизменности кортежа в функции, которая принимает на вход необходимый кортеж и элемент, который надо удлить, создаётся список из предоставленного кортежа. Затем с помощью for идёт поэлементная проверка значений списка и, если такой элемент находится, то он удаляется из списка и список возвращается, если необходимо вернуть кортеж, а не список, то необходимо изменить "return my_list" на "return tuple(my_list)". В случае, если цикл for завершил свою работу и искомый элемент не был найден, то функция вернёт переданный кортеж без изменений.

## Самостоятельная работа №3
  Ребята поспорили кто из них одним нажатием на numpad наберет больше повторяющихся цифр, но не понимают, как узнать победителя. Вам им нужно в этом помочь. Дана строка в виде случайной последовательности чисел от 0 до 9 (длина строки минимум 15 символов). Требуется создать словарь, который в качестве ключей будет принимать данные числа (т. е. ключи будут типом int), а в качестве значений – количество этих чисел в имеющейся последовательности. Для построения словаря создайте функцию, принимающую строку из цифр. Функция должна возвратить словарь из 3-х самых часто встречаемых чисел, также эти значения нужно вывести в порядке возрастания ключа.

 ```python
def count_most_common_numbers(inputString):
    numberCounts = {}

    for digit in inputString:
        digit = int(digit)
        numberCounts[digit] = numberCounts.get(digit, 0) + 1

    most_common_numbers = sorted(numberCounts.items(), key=lambda x: x[1], reverse=True)[:3]

    result_dict = {key: value for key, value in sorted(most_common_numbers)}

    return result_dict


# Пример использования функции
input_string = "112223333456789"
result = count_most_common_numbers(input_string)
print("Словарь из трех самых частых чисел в порядке возрастания ключа:")
print(result)

```

### Результат

![image](https://github.com/user-attachments/assets/2bc5de5d-781f-4e43-9cf8-97cb03f1d766)


## Краткий вывод:

В программе создаются функция, которая на вход получает строку из цифр. Затем при помощи цикла for программа проходит по каждому элементу в заданной строке, преобразовывает этот элемент в число и проверяет, содержится ли такой ключ в словаре. Если да, то программа добавит к значению этого ключа 1, если нет, то программа создат этот ключ со значением равным 1. После в переменную most_common_numbers записываются кортежи с 3 самыми популярными цифрами и их количеством. После чего из этих кортежей создаётся новый словарь, который затем выводится в консоль.

## Самостоятельная работа №4

  Ваш хороший друг владеет офисом со входом по электронным картам, ему нужно чтобы вы написали программу, которая показывала в каком порядке сотрудники входили и выходили из офиса. Определение сотрудника происходит по id. Напишите функцию, которая на вход принимает кортеж и случайный элемент (id), его можно придумать самостоятельно. Требуется вернуть новый кортеж, начинающийся с первого появления элемента в нем и заканчивающийся вторым его появлением включительно.
Если элемента нет вовсе – вернуть пустой кортеж.
Если элемент встречается только один раз, то вернуть кортеж, который начинается с него и идет до конца исходного.
Входные данные:
(1, 2, 3), 8)
(1, 8, 3, 4, 8, 8, 9, 2), 8)
(1, 2, 8, 5, 1, 2, 9), 8)
Ожидаемый результат:
()
(8, 3, 4, 8)
(8, 5, 1, 2, 9)


 ```python
def find(inp_tuple: tuple, find_id: int) -> tuple:
    """
    Функция принимает кортеж и ID искомого сотрудника.
    """
    start_index = -1
    finish_index = len(inp_tuple)
    k = 0

    for i in range(len(inp_tuple)):
        if find_id == inp_tuple[i]:
            start_index = i
            k += 1
            break
    if k != 0:
        for i in range(start_index + 1, len(inp_tuple)):
            if find_id == inp_tuple[i]:
                finish_index = i + 1
                break

    if start_index != -1:
        return inp_tuple[start_index:finish_index]
    else:
        return ()


if __name__ == '__main__':
    print(find((1, 8, 3, 4, 8, 8, 9, 2), 8))

```

### Результаты

![image](https://github.com/user-attachments/assets/40ea3a89-cd0c-4734-8b4e-2f509cd2f44b)


## Краткий вывод:

В программе создаётся функция, которая принимает на вход кортеж и искомое ID. Затем создаются 3 переменные для выяснения стартового и конечного индекса для вывода и вспомогательная переменная k, которая позволяет не проверять дважды кортеж на поиск элемента, если такой элемент не был найден в первый раз. В переменную start_index при создании записывается значение -1, чтобы в случае не обнаружения искомого ID в списке вернуть пустой список, в переменную finish_index записывается индекс последнего элемента в переданном кортеже. Затем запускаются 2 цикла for, в первом находится индекс первого появления искомого id в кортеже и, если такой найден, то этот индекс записывается в соответствующую переменную, к переменной k прибавляется 1, а выполнение цикла прекращается, после чего запускается новый цикл, начиная со следующего элемента за тем, что был найден в прошлом цикле. Если в этом списке удаётся найти искомый элемент ещё раз, то его индекс записывается в переменную finish_idex, выполнение цикла прекращается и на экран выводится срез из переданного кортежа. Таким образом программа выведен срез, если элемент был найден хотя бы 1 раз и выведет пустой кортеж, если элемента не нашлось.

## Самостоятельная работа №5

Напишите функцию, которая сортирует кортеж, состоит из целых чисел по возрастанию и возвращает его. Если хотя бы один элемент не является целым числом, то функция возвращает исходный кортеж.

 ```python

def tpl_sort(tpl):
    for element in tpl:
        if not isinstance(element, int):
            return tpl
    return tuple(sorted(tpl))

print(tpl_sort((5, 5, 3, 1, 9)))
print(tpl_sort((5, 5, 2.1, '1', 9)))

```
### Результат

![image](https://github.com/user-attachments/assets/5c5750cb-918f-44cc-a513-bd3a8923daf2)


## Краткий вывод:

В программе создаётся словарь, в котором ключами являются имена, а значениями строки с оценками. Так же создаётся функция, которая принимает на вход имя студента. Сперва в программе выполняется проверка на наличае ключа в словаре и, если такого ключа не находится, то программа об этом сообщает и просит ввести имчя ещё раз. Если такой ключ находится, то программа в переменную grades записывает строку с оценками из словаря. Затем в цикле for считается сумма оценок и происходит из запись в список. После чего выводится сперва список оценок студента, затем количество двоек, троек, четвёрок и пятёрок, а после выводится средний балл студента. В конце программа просит ввести имя следующего студента для продолжения, либо слово "Нет" для выхода.


# Общий вывод 

Функции - это блоки кода, которые могут быть многократно вызваны для выполнения определенных задач. Они создаются с использованием ключевого слова def и могут принимать параметры.
Функции могут возвращать значения с помощью ключевого слова return, что позволяет функции передавать результат своей работы обратно в вызывающую программу.
Функции могут принимать параметры, которые могут быть обязательными или необязательными. Это позволяет функциям принимать входные данные и делать их более универсальными.
Переменные, определенные внутри функции, являются локальными и видны только внутри этой функции. Переменные, определенные вне функций, являются глобальными и могут быть доступны в любом месте программы.

Модули - это файлы, содержащие функции и переменные, предназначенные для многократного использования. Их можно импортировать в другие программы с помощью ключевого слова import.
Python поставляется с богатой библиотекой стандартных модулей, которые предоставляют готовые решения для различных задач, таких как работа с файлами, математические вычисления и многое другое.
Пользовательские модули позволяют программистам организовывать свой код в логические блоки, улучшая его читаемость и обслуживаемость.

Понимание функций и модулей в Python не только повышает эффективность и чистоту кода, но и способствует повторному использованию кода, что делает программирование более удобным и эффективным.

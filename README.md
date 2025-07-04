# python_for_beginners
Конспект курса [Поколение Python: курс для начинающих](https://stepik.org/course/58852/promo)

## Ввод-вывод данных
### Вывод данных, команда print
Для вывода данных на экран используется команда ``` print() ```  
То, что мы пишем в круглых скобках у команды print(), называется аргументами команды.  
**Аргументы – это конкретные значения, которые вы передаете функции при ее вызове.**  

### Ввод данных, команда input()
Для считывания данных в языке Python используется команда ```input()```  

```python
variable_name = input()
print('Вы ввели текст:', variable_name)
```

### sep, end
По умолчанию команда ```print()``` принимает несколько аргументов, выводит их через один пробел, после чего ставит перевод строки. Это поведение можно изменить, используя необязательные именованные параметры sep и end.  
______
sep (separator – разделитель) - параметр, который отвечает за разделение аргументов при выводе. По умолчанию этот параметр равен символу пробела  .
Мы можем изменить параметр sep на любую другую строку, например, на символ звёздочки *.
```python
print('aa', 'bb', 'cc', sep='*')
>>>aa*bb*cc
```
**Параметр end**  
параметр end определяет строку, которая будет добавлена после вывода всех аргументов команды print().
```python
print('a', '\n', 'b', '\n', 'c', sep='*', end='#')
>>>
a*
*b*
*c#
```
Для разных команд print() можно задавать разные параметры sep и end.
```python
arg1 = 'Hello'
sep1 = '_-_'
end2 = '+++'
print(arg1, 'everyone', sep=sep1, end='! ')
print('How', 'are', 'you', 'in', '2024?', sep=' ', end=end2)
>>>
Hello_-_everyone! How are you in 2024?+++
```
**Множественное присваивание**  
за одну инструкцию присваивания можно задавать значения сразу нескольким переменным. 
```python
name, surname = 'Timur', 'Guev'
print('Имя:', name, 'Фамилия:', surname)
```

```python
name, surname = input(), input()
print('Имя:', name, 'Фамилия:', surname)
```
Множественное присваивание удобно использовать, когда нужно обменять значения двух переменных.   
```python
name1 = 'Timur'
name2 = 'Gvido'

name1, name2 = name2, name1
>>>
Gvido
```

### Арифметика
**Основные операции с числами**
```python
+  сложение
-  вычитание
*  умножение
/  деление
**  возведение в степень
%  остаток от деления
//  целочисленное деление
```
**Приоритет выполнения операций**
```python
1.	() Скобки
2.	** Возведение в степень
3.	- (унарный минус)
4.	*, /, //, % Умножение, деление, целочисленное деление, остаток от деления
5.	+, - Сложение, вычитание
```
## Логические операторы
### Условный оператор if-else   
Проверка условий и принятие решений по результатам этой проверки называется ветвлением (branching). Программа таким способом выбирает, по какой из возможных ветвей ей двигаться дальше.
```python
answer = input('Какой язык программирования мы изучаем?')

if answer == 'Python':
    print('Верно! Мы ботаем Python =)')
    print('Python - отличный язык!')
else:
    print('Не совсем так!')
```
**Операторы сравнения**
```python
Выражение                          Описание
if x > 7                           если x больше 7         
if x < 7                           если x меньше 7
if x >= 7                          если x больше либо равен 7
if x <= 7                          если x меньше либо равен 7
if x == 7                          если x равен 7
if x != 7                          если x не равен 7
```

**or, and, not**
```python
and — логическое умножение;
or — логическое сложение;
not — логическое отрицание.
```
Приоритеты логических операторов  
```python
в первую очередь выполняется логическое отрицание not;
далее выполняется логическое умножение and;
далее выполняется логическое сложение or.
```
## Типы данных
### Числовые типы данных
```python
int(n)  # целочисленный тип данных (1)  
float(n)  # число с плавающей точкой (0.1)  
max(a, b ... n)  # максимальное число  
min(a, b ... n)  # минимальное число  
abs(n)  # абсолютная величина числа (модуль)
```
### Строковый тип данных
```python
str(12345)  # преобразование в строку  
len('abc')  # длина строки
>>> 3 

print("ab"+"bc")  # конкатенация (сложение строк)  
>>> abbc  

print("abc" * 3)  # умножение строки  
>>> abcabcabc  

text = """  
многострочный текст выделяется  
тройными кавычками  
"""  
```

IN позволяет проверить, что одна строка находится внутри другой
```python
s = 'https://pygen.ru/'
if 'a' in s:
    print('Введенная строка содержит символ а')
else:
    print('Введенная строка не содержит символ а')
>>>
Введенная строка не содержит символ а
```
Мы можем использовать оператор in вместе с логическим оператором not, например:
```python
s = input()
if '.' not in s:
    print('Введенная строка не содержит символа точки')
```
### Модуль math
Модуль ```math``` – один из наиважнейших в Python. Этот модуль предоставляет обширный функционал для проведения вычислений с действительными числами.     
Для использования этих функций в начале программы необходимо подключить модуль, что делается командой ```import```:
```python
import math
# программный код
```
После подключения модуля мы можем использовать его функции. Пусть мы хотим:
вычислить корень квадратный из двух;
округлить число 3.8 до ближайшего целого числа вверх и вниз
```python
import math
num1 = math.sqrt(2)     # вычисление квадратного корня из двух
num2 = math.ceil(3.8)   # округление числа вверх
num3 = math.floor(3.8)  # округление числа вниз

print(num1)
print(num2)
print(num3)
>>>
1.4142135623730951
4
3
```
Для того чтобы не указывать название модуля и символ точки при вызове функций:
```python
from math import *
num1 = sqrt(2)     # вычисление корня квадратного из двух
num2 = ceil(3.8)   # округление числа вверх
num3 = floor(3.8)  # округление числа вниз

print(num1)
print(num2)
print(num3)
```
Если нужно использовать только некоторые функции модуля, то мы можем импортировать их следующим образом:  
```python
from math import sqrt, ceil
```
Теперь мы можем вызывать функции sqrt() и ceil() без префикса math., однако мы не можем вызвать функцию floor(), так как она не подключена:
```python
from math import sqrt, ceil

print(sqrt(25))
print(ceil(34.7))

print(floor(12.8))  # приведет к ошибке, так как функция floor не подключена
```

Список функций модуля math    
  
| Функция   | Описание   |  
|---|---|  
| Округления   |    |  
| int()   | Округляет число в сторону нуля   |  
| round(x)   | Округляет число x до ближайшего целого. Если дробная часть числа равна 0.50.5, то число округляется до ближайшего четного числа (банковское округление)   |  
| round(x, n)   | Округляет число x до n знаков после точки   |  
| floor(x)   | Округляет число x вниз («пол»)   |  
| ceil(x)   | Округляет число x вверх («потолок»)   |  
| abs(x)   | Модуль числа x (абсолютная величина)   |  
| Корни, логарифмы, степени и факториал   |    |  
| sqrt(x)   | Квадратный корень числа x   |  
| pow(x, n)   | Возведение числа x в степень n   |  
| log(x)   | Натуральный логарифм числа x. Основание натурального логарифма равно числу e   |  
| log10(x)   | Десятичный логарифм числа x. Основание десятичного логарифма равно числу 10   |  
| log(x, b)   | Логарифм числа x по основанию b   |  
| factorial(n)   | Факториал натурального числа n   |  
| Тригонометрия   |    |  
| degrees(x)   | Преобразует угол x, заданный в радианах, в градусы   |  
| radians(x)   | Преобразует угол x, заданный в градусах, в радианы   |  
| cos(x)   | Косинус угла x, задаваемого в радианах   |  
| sin(x)   | Синус угла x, задаваемого в радианах   |  
| tan(x)   | Тангенс угла x, задаваемого в радианах   |  
| acos(x)   | Возвращает угол в радианах от 0 до π, cos которого равен x   |  
| asin(x)   | Возвращает угол в радианах от −π2−2π​ до π22π​, sin которого равен x   |  
| atan(x)   | Возвращает угол в радианах от −π2−2π​ до π22π​, tan которого равен x   |  
| atan2(y, x)   | Полярный угол (в радианах) точки с координатами (x, y)   |  

## Циклы
### for
**for** - цикл, повторяющийся определенное количество раз  
Структура цикла for в Python выглядит так:
```python
for название_переменной_цикла in range(количество_повторений):
    блок кода
```
Двоеточие (:) в конце строки с инструкцией for сообщает интерпретатору Python, что дальше находится блок команд. В блок команд входят все строки, расположенные с отступом от строки с инструкцией for, вплоть до следующей строки без отступа.  
Когда цикл впервые начинает работу, Python устанавливает значение переменной цикла i = 0. Каждый раз, когда мы повторяем тело цикла, Python увеличивает значение переменной на 1.   
**Для переменных цикла обычно используют буквы i, j, k.**      
**Бывают ситуации, когда переменная цикла не используется в теле цикла. В таком случае, вместо того, чтобы давать ей имя, мы можем указать символ нижнего подчеркивания _:**  

range() с двумя параметрами  
Если мы хотим начинать последовательность не с 0, а с какого-то другого числа, то мы можем использовать перегрузку функции range() принимающую два параметра. Например, вызов функции range(1, 5) сгенерирует последовательность чисел 1, 2, 3, 4  (правая граница не включительна).    
Если нам нужны числа от 1 до 5 включительно, то мы используем range(1, 6).  
Таким образом:
```python
range(stop): создает последовательность чисел 0, 1, 2, 3, ..., stop - 1;
range(start, stop): создает последовательность чисел start, start + 1, start + 2, ..., stop - 2, stop - 1.
```
```python
for i in range(1, 10):  
    print(i)  
>>> 1  
>>> 2  
>>> 3  
>>> 4  
>>> 5  
>>> 6  
>>> 7  
>>> 8  
>>> 9
```
**range() с 3 параметрами**  
Первый параметр задает старт последовательности, второй параметр задает стоп последовательности и третий – шаг генерации чисел.  
```python
for i in range(1, 10, 2):  
    print(i)  
>>> 1  
>>> 3  
>>> 5  
>>> 7  
>>> 9
```
### Частые сценарии
**Подсчет количества**    
Нередко нужно, чтобы наши программы подсчитывали, сколько раз что-либо произошло. К примеру, видеоигра может подсчитывать количество поворотов персонажа, или математическая программа может считать, как много чисел обладают некоторым свойством. Ключ к подсчету – использование переменной счетчика.   
Напишем программу, которая считывает 10 чисел и определяет, сколько из них больше 10   
```python
counter = 0
for _ in range(10):
    num = int(input())
    if num > 10:
        counter = counter + 1

print('Было введено', counter, 'чисел, больших 10.')
```
Подсчет количества – это очень частый сценарий. Он состоит из двух шагов:   
 - Создание переменной счетчика, и придание ей первоначального значения: counter = 0;
 - Увеличение переменной счетчика на 1: counter = counter + 1.
**Вычисление суммы и произведения**
```python
total = 0
for _ in range(10):
    num = int(input())
    if num > 10:
        total = total + num

print('Сумма чисел больших 10 равна',  total)
```

**Обмен значений переменных**   
```python
x, y = y, x
```
**Сигнальные метки**
Сигнальная метка (флажок) может использоваться, когда надо, чтобы одна часть программы узнала о происходящем в другой части программы.
Напишем программу, определяющую, что натуральное число является простым: 
```python
num = int(input())
flag = True

for i in range(2, num):
    if num % i == 0:  #  если исходное число делится на какое-либо отличное от 1 и самого себя
        flag = False

if num == 1:
    print('Это единица, она не простая и не составная') 
elif flag == True:
    print('Число простое')
else:
    print('Число составное')
```
**Максимум и минимум**   
```python 
largest = 0
for _ in range(10):
    num = int(input())    
    if num > largest:
        largest = num

print('Наибольшее число равно', largest)
```
**Расширенные операторы присваивания**       
| Оператор   | Пример использования   | Эквивалент   |
|---|---|---|
| +=   | x += 5   | x = x + 5   | 
| -=   | x -= 2   | x = x - 2   |
| *=   | x *= 10   | x = x * 10   |
| /=   | x /= 4   | x = x / 4   |
| //=   | x //= 4   | x = x // 4   |
| %=   | x %= 4   | x = x % 4   |   

### while
while выполняет некую задачу до тех пор, пока условие является истинным (и количество итераций в этом случае заранее оценить просто невозможно).   
Напишем программу, выводящую все числа, кратные 3, используя цикл for и while:
```python
# используем for
for i in range(0, 100, 3):
    print(i)

# используем while
i = 0
while i < 100:
    print(i)
    i += 3 
```
Не всегда, однако, удается заменить цикл while с помощью цикла for. Если заранее не известно количество итераций, то необходимо использовать цикл while и только его.       

### while: break, continue, else
Иногда бывает нужно прервать выполнение цикла преждевременно. Оператор ```break``` прерывает ближайший цикл for или while.  
Проверка числа на простоту:  
```python
num = int(input())
flag = True

for i in range(2, num):
    if num % i == 0:        #  если исходное число делится на какое-либо отличное от 1 и самого себя
        flag = False
        break               # останавливаем цикл если встретили делитель числа        

if flag:  # эквивалентно if flag == True:
    print('Число простое')
else:
    print('Число составное')
```
Оператор прерывания цикла ```break``` позволяет ускорять программы, так как мы избавляемся от лишних итераций.  

Оператор **continue** позволяет перейти к следующей итерации цикла for или while до завершения всех команд в теле цикла.  
Программа, которая выводит все числа от 1 до 100, кроме чисел 7, 17, 29 и 78.
```python
for i in range(1, 101):
    if i == 7 or i == 17 or i == 29 or i == 78:
        continue  # переходим на следующую итерацию
    print(i)
```
![image](https://github.com/user-attachments/assets/bb5aa196-a874-418e-8430-1fc5a375551d)

**else**
Python допускает необязательный блок else в конце циклов while и for. Это уникальная особенность Python, не встречающаяся в большинстве других языков программирования. Синтаксис такой конструкции следующий:
```python
while условие:
    блок кода1
else:
    блок кода2

# или

for i in range(10):
    блок кода1
else:
    блок кода2
```
Блок кода2, указанный в else, будет выполнен, когда штатным образом завершается цикл while или for.    
Если слово else отсутствует в описании цикла, то блок кода2 будет выполняться после завершения цикла, несмотря ни на что. Если же слово else присутствует, то блок кода2 будет выполняться только в том случае, если цикл завершается штатным образом. Под штатным завершением цикла подразумевается его завершение без использования оператора прерывания break.    
```python
n = 5
while n > 0:
    n -= 1
    print(n)
else:
    print('Цикл завершен.')
>>>>>>>>>
4
3
2
1
0
Цикл завершен.
```
### Вложенные циклы    
Оператор break выполняет прерывание ближайшего цикла в котором он расположен. Аналогично, оператор continue осуществляет переход на следующую итерацию ближайшего цикла.   
```python
for i in range(3):
    for j in range(3):
        if i == j:
            break
        print(i, j)
>>>>>>>>>
1 0
2 0
2 1
```
## Строки
### Индексация строк
Очень часто бывает необходимо обратиться к конкретному символу в строке. Для этого в Python используются квадратные скобки [], в которых указывается индекс (номер) нужного символа в строке.   
Пусть s = 'Python'.     Таблица ниже показывает, как работает индексация:  
| Выражение   | Результат   | Пояснение   |
|---|---|---|
| s[0]   | P   | первый символ строки   |
| s[1]   | y   | второй символ строки   |
| s[2]   | t   | третий символ строки   |
| s[3]   | h   | четвертый символ строки   |
| s[4]   |	o   | пятый символ строки   |
| s[5]   |	n   |	шестой символ строки   |


![image](https://github.com/user-attachments/assets/b08c04e2-bf1e-49d7-9fb9-b45482ed4de1)
Таким образом получается:     
![image](https://github.com/user-attachments/assets/1238df95-40fd-49c6-9534-bda5619aecd3)

### Итерирование строк
![image](https://github.com/user-attachments/assets/553fde32-4f08-4ed4-b829-b4844c1d79af)
![image](https://github.com/user-attachments/assets/1bc179ee-3abc-4d74-ae25-3273ac2f5d08)

### Срезы строк   
С помощью среза мы можем получить несколько символов исходной строки, создав диапазон индексов разделенных двоеточием s[x:y].      
```python
s = 'abcdefghij'
print(s[2:5])
print(s[0:6])
print(s[2:7])
>>>>>>>>>
cde
abcdef
cdefg
```
![image](https://github.com/user-attachments/assets/4c760ee8-9436-4319-baa0-c000e56dd47c)

При построении среза s[x:y] первое число – это то место, где начинается срез (включительно), а второе – это место, где заканчивается срез (невключительно). Разрезая строки, мы создаем подстроку, которая по сути является строкой внутри другой строки.       
Срез s[:] возвращает исходную строку.    
**При использовании отрицательных индексов первый параметр среза должен быть меньше второго, либо должен быть пропущен.**    
**Удалить из строки последний символ можно при помощи среза s[:-1].**    
![image](https://github.com/user-attachments/assets/c7dd14d0-ac30-4b94-aa2f-61615e93bd57)
![image](https://github.com/user-attachments/assets/404fa15c-1ddf-4704-a278-2d18d23a134e)
![image](https://github.com/user-attachments/assets/1be94d79-eacc-4780-9d16-76406c152c3a)

### Методы строк
Метод — функция, применяемая к объекту. В данном случае к строке. Метод вызывается в виде **имя_объекта.имя_метода(параметры).**   
Например, s.find('e') — это применение к строке s метода find с одним параметром 'e'.   
**Конвертация регистра**      
Метод capitalize() возвращает копию строки s, в которой первый символ имеет верхний регистр, а все остальные символы имеют нижний регистр.  
```python
s = 'foO BaR BAZ quX'
print(s.capitalize())
>>>>>>>>>
Foo bar baz qux
```
Метод swapcase() возвращает копию строки s, в которой все символы, имеющие верхний регистр, преобразуются в символы нижнего регистра и наоборот.
```python
s = 'FOO Bar 123 baz qUX'
print(s.swapcase())
>>>>>>>>>
foo bAR 123 BAZ Qux
```
Метод title() возвращает копию строки s, в которой первый символ каждого слова переводится в верхний регистр.
```python
s = 'the sun also rises'
print(s.title())
>>>>>>>>>
The Sun Also Rises
```
Метод lower() возвращает копию строки s, в которой все символы имеют нижний регистр.
```python
s = 'FOO Bar 123 baz qUX'
print(s.lower())
>>>>>>>>>
foo bar 123 baz qux
```
Метод upper() возвращает копию строки s, в которой все символы имеют верхний регистр.
```python
s = 'FOO Bar 123 baz qUX'
print(s.upper())
>>>>>>>>>
FOO BAR 123 BAZ QUX
```
![image](https://github.com/user-attachments/assets/e9ec9e84-b70d-4d86-88c7-1aca3a533992)

**Поиск и замена**    
Каждый метод в этой группе поддерживает необязательные аргументы start и end. Как и в строковых срезах, действие метода ограничено частью исходной строки, начинающейся с позиции символа start и продолжающейся вплоть до позиции символа end, но не включающей её. Если параметр start указан, а параметр end нет, то метод применяется к части исходной строки от start до конца строки. Если параметры не заданы, то подразумевается, что start = 0, end = len(s).     

Метод count(sub, start, end) считает количество непересекающихся вхождений подстроки sub в исходную строку s.   
```python
s = 'foo goo moo'
print(s.count('oo'))
print(s.count('oo', 0, 8))  # подсчет с 0 по 7 символ
>>>>>>>>>
3
2
```
Метод startswith(prefix, start, end) определяет, начинается ли исходная строка s подстрокой prefix. Метод возвращает значение True, если исходная строка начинается с подстроки prefix, или False в противном случае.   
```python
s = 'foobar'
print(s.startswith('foo'))
print(s.startswith('baz'))
>>>>>>>>>
True
False
```
Метод endswith(suffix, start, end) определяет, оканчивается ли исходная строка s подстрокой suffix. Метод возвращает значение True, если исходная строка оканчивается на подстроку suffix, или False в противном случае.  

```python
s = 'foobar'
print(s.endswith('bar'))
print(s.endswith('baz'))
>>>>>>>>>
True
False
```
Метод find(sub, start, end) находит индекс первого вхождения подстроки sub в исходной строке s. Если строка s не содержит подстроки sub, то метод возвращает значение -1. Мы можем использовать данный метод наравне с оператором in для проверки: содержит ли заданная строка некоторую подстроку или нет.

```python
s = 'foo bar foo baz foo qux'
print(s.find('foo'))
print(s.find('bar'))
print(s.find('qu'))
print(s.find('python'))
>>>>>>>>>
0
4
20
-1
```
Метод index(sub, start, end) идентичен методу find(sub, start, end), за тем исключением, что он вызывает ошибку ValueError: substring not found во время выполнения программы, если подстрока sub не найдена.     
Метод rindex(sub, start, end) идентичен методу index(sub, start, end), за тем исключением, что он ищет первое вхождение подстроки sub, начиная с конца строки s.   
![image](https://github.com/user-attachments/assets/908fae41-4224-4bef-a71c-27f25b9f420c)

Метод strip() возвращает копию строки s, у которой удалены все пробелы, стоящие в начале и конце строки.
```python
s = '     foo bar foo baz foo qux      '
print(s.strip())
>>>>>>>>>
foo bar foo baz foo qux
```
Метод lstrip() возвращает копию строки s, у которой удалены все пробелы, стоящие в начале строки.
```python
s = '     foo bar foo baz foo qux      '
print(s.lstrip())
>>>>>>>>>
foo bar foo baz foo qux⎵⎵⎵⎵⎵⎵
```
Метод rstrip() возвращает копию строки s, у которой удалены все пробелы, стоящие в конце строки.
```python
s = '      foo bar foo baz foo qux      '
print(s.rstrip())
>>>>>>>>>
⎵⎵⎵⎵⎵⎵foo bar foo baz foo qux
```
Метод replace(old, new) возвращает копию s со всеми вхождениями подстроки old, заменёнными на <new>.
```python
s = 'foo bar foo baz foo qux'
print(s.replace('foo', 'grault'))
>>>>>>>>>
grault bar grault baz grault qux
```
Метод replace() может принимать необязательный третий аргумент count, который определяет количество замен.  
```python
s = 'foo bar foo baz foo qux'
print(s.replace('foo', 'grault', 2))
>>>>>>>>>
grault bar grault baz foo qux
```
![image](https://github.com/user-attachments/assets/7dc954ee-6fc7-4fd7-891e-56ca3886aaaa)

**Классификация символов**       
Метод isalnum() определяет, состоит ли исходная строка из буквенно-цифровых символов. Метод возвращает значение True, если исходная строка является непустой и состоит только из буквенно-цифровых символов (либо только буквенных или только цифровых), или False в противном случае.    
```python
s1 = 'abc123'
s2 = 'abc$*123'
s3 = ''

print(s1.isalnum())
print(s2.isalnum())
print(s3.isalnum())
>>>>>>>>>
True
False
False
```
Метод isalpha() определяет, состоит ли исходная строка из буквенных символов. Метод возвращает значение True, если исходная строка является непустой и состоит только из буквенных символов, или False в противном случае.   
```python
s1 = 'ABCabc'
s2 = 'abc123'
s3 = ''

print(s1.isalpha())
print(s2.isalpha())
print(s3.isalpha())
>>>>>>>>>
True
False
False
```
Метод isdigit() определяет, состоит ли исходная строка только из цифровых символов. Метод возвращает значение True, если исходная строка является непустой и состоит только из цифровых символов, или False в противном случае.
```python
s1 = '1234567'
s2 = 'abc123'
s3 = ''

print(s1.isdigit())
print(s2.isdigit())
print(s3.isdigit())
>>>>>>>>>
True
False
False
```
Метод islower() определяет, являются ли все буквенные символы исходной строки строчными (имеют нижний регистр). Метод возвращает значение True, если все буквенные символы исходной строки являются строчными, или False в противном случае.
```python
s1 = 'abc'
s2 = 'abc1$d'
s3 = 'Abc1$D'

print(s1.islower())
print(s2.islower())
print(s3.islower())
>>>>>>>>>
True
True
False
```
Метод isupper() определяет, являются ли все буквенные символы исходной строки заглавными (имеют верхний регистр). Метод возвращает значение True, если все буквенные символы исходной строки являются заглавными, или False в противном случае.
```python
s1 = 'ABC'
s2 = 'ABC1$D'
s3 = 'Abc1$D'

print(s1.isupper())
print(s2.isupper())
print(s3.isupper())
>>>>>>>>>
True
True
False
```
Метод isspace() определяет, состоит ли исходная строка только из пробельных символов. Метод возвращает значение True, если строка состоит только из пробельных символов, или False в противном случае.
```python
s1 = '       '
s2 = 'abc1$d'

print(s1.isspace())
print(s2.isspace())
>>>>>>>>>
True
False
```
Для пустой строки метод isspace() также возвращает False, так как в этом случае строка не состоит из пробельных символов.    

**Форматирование строк**    
Хранить строки в переменных удобно, но часто бывает необходимо собирать строки из других объектов (строк, чисел и т.д.) и выполнять с ними нужные манипуляции. Для этой цели можно воспользоваться механизмом форматирования строк(строковый метод format())    
```python
birth_year = 1992
name = 'Timur'
profession = 'math teacher'
text = 'My name is {}, I was born in {}, I work as a {}.'.format(name, birth_year, profession)

print(text)
>>>>>>>>>
My name is Timur, I was born in 1992, I work as a math teacher.
```
Мы можем использовать одно и то же число в нескольких заполнителях или не использовать совсем, а также мы можем использовать числа в разном порядке.   
```python
name = 'Timur'
city = 'Moscow'
text1 = 'My name is {0}-{0}-{0}!'.format(name, city)
text2 = '{1} is my city and {0} is my name!'.format(name, city)

print(text1)
print(text2)
>>>>>>>>>
My name is Timur-Timur-Timur!
Moscow is my city and Timur is my name!
```

**f-строки**    
Если поставить перед строкой префикс f, в заполнители можно будет включить код, например, имя переменной или любые другие выражения. f-строки обеспечивают чистый и интуитивно понятный способ форматирования строк.     
```python
first_name = 'Taylor'
last_name = 'Swift'
country = 'USA'
birth_date = '1989/12/13'
birth_place = 'West Reading, Pennsylvania'
text = f'{first_name} {last_name} is a very famous singer from the {country}. She was born on {birth_date} in {birth_place}.'

print(text)
```
На место заполнителя {first_name} встает значение переменной first_name, на место заполнителя {last_name} встает значение переменной last_name и т.д.       
Помимо переменных в заполнителях f-строк мы можем использовать выражения.
```python
print(f'5 + 2 = {5 + 2}')
print(f'5 - 2 = {5 - 2}')
print(f'5 * 2 = {5 * 2}')
print(f'5 / 2 = {5 / 2}')
>>>>>>>>>
5 + 2 = 7
5 - 2 = 3
5 * 2 = 10
5 / 2 = 2.5
```
**Строки в памяти компьютера**               
Любой набор данных в оперативной памяти компьютера должен храниться в виде двоичного числа. Это относится и к строкам, которые состоят из символов (буквы, знаки препинания и так далее). Когда символ сохраняется в памяти, он сначала преобразуется в цифровой код. И затем этот цифровой код сохраняется в памяти как двоичное число.     
Таблица символов ASCII представляет собой набор из 128 цифровых кодов, которые обозначают английские буквы, различные знаки препинания и другие символы. Например, код ASCII для прописной английской буквы «А» (латинской) равняется 65. Когда на компьютерной клавиатуре вы набираете букву «А» в верхнем регистре, в памяти сохраняется число 65 (как двоичное число). 
![image](https://github.com/user-attachments/assets/afcbc128-5696-4eda-9f65-581de0d77539)

![image](https://github.com/user-attachments/assets/350f9a19-981b-47a8-82a1-e5aa14a8e796)

### Сравнение строк
В Python мы можем сравнивать с помощью операторов ==, !=, <, <=, > и >= не только числа, но и строки. В отличие от чисел, сравнение строк происходит на основе лексикографического порядка – в соответствии с кодами составляющих их символов в таблице Unicode.     
Начнем с примера сравнения строк, состоящих из одного символа. В Python это сравнение происходит путём сравнения кодов этих символов в таблице Unicode.  
```python
print('a' > 'b')
print('a' < 'z')
>>>>>>>>>
False
True
```
Действительно, код символа a в таблице Unicode равен числу 97, а символа b – числу 98. Число 97 меньше числа 98, поэтому и символ a меньше символа b. Аналогично символ z больше символа a, потому что код символа z (число 122) больше кода символа a (число 97).     
Буквы в нижнем регистре всегда больше своих аналогов в верхнем регистре(потому что буквы в нижнем регистре идут после букв в верхнем регистре в таблице Unicode). Для букв русского алфавита это правило также работает.  
__________________________________________________
**Сравнение строк не единичной длины**    
Алгоритм сравнения строк:   

Начинаем с первых символов каждой строки. Если символы равны, переходим к следующей паре символов     
Когда находим первый отличающийся символ, строка с меньшим символом считается "меньше"       
Если одна из строк заканчивается раньше, то более короткая считается "меньше"             
Чтобы лучше разобраться с алгоритмом сравнения строк, рассмотрим несколько примеров.              

Пример 1. Сравним строки 'hello' и 'hell'.                                       
Сравнение первых символов: h и h – оба символа равны, переходим к следующей паре символов                      
Сравнение вторых символов: e и e – оба символа равны, переходим к следующей паре символов                  
Сравнение третьих символов: l и l – оба символа равны, переходим к следующей паре символов                        
Сравнение четвертых символов: l и l – оба символа равны, переходим к следующей паре символов                    
Сравнение пятых символов: o (у первой строки) и отсутствующий символ (у второй строки) – вторая строка закончилась                        
Поскольку у второй строки закончились символы, а у первой строки они еще есть, считается, что первая строка больше второй. Поэтому 'hello' > 'hell'.                   
![image](https://github.com/user-attachments/assets/f6da4e9d-294f-46d2-b366-c9e2b87d3637)

-------------------------------------------
## Списки
Список представляет собой последовательность элементов, пронумерованных от 0, как символы в строке.    
### Создание списка    
Чтобы создать список, нужно перечислить его элементы через запятую в квадратных скобках:   
```python
numbers = [2, 4, 6, 8, 10]
languages = ['Python', 'C#', 'C++', 'Java']
```
Список numbers состоит из 5 элементов, и каждый из них — целое число.    
```python
numbers[0] == 2;
numbers[1] == 4;
numbers[2] == 6;
numbers[3] == 8;
numbers[4] == 10.
```
![image](https://github.com/user-attachments/assets/8da8e2d2-6863-443f-a37f-89c8d241b3dc)
![image](https://github.com/user-attachments/assets/75a6d011-8a05-40a5-a354-5be11301242a)

### Встроенная функция list
![image](https://github.com/user-attachments/assets/13baa988-eba7-439b-a85b-7d07a35955c1)

### Основы работы со списками
Функция len() - длина списка      
```python
numbers = [2, 4, 6, 8, 10]
languages = ['Python', 'C#', 'C++', 'Java']

print(len(numbers))      # выводим длину списка numbers
print(len(languages))    # выводим длину списка languages

print(len(['apple', 'banana', 'cherry']))   # выводим длину списка, состоящего из 3 элементов
>>>>>>>>>
5
4
3
```
**Оператор in позволяет проверить, содержит ли список некоторый элемент.**
```python
numbers = [2, 4, 6, 8, 10]

if 2 in numbers:
    print('Список numbers содержит число 2')
else:
    print('Список numbers не содержит число 2')
>>>>>>>>>
Список numbers содержит число 2
```
В списках индексация, срезы, конкатенация и умножение аналогично строкам, только тут вместо символов строки элементы списка.     
Для изменения целого диапазона элементов списка можно использовать срезы. Например, если мы хотим перевести на русский язык названия фруктов 'banana', 'cherry', 'kiwi', то это можно сделать с помощью среза.
```python
fruits = ['apple', 'apricot', 'banana', 'cherry', 'kiwi', 'lemon', 'mango']
fruits[2:5] = ['банан', 'вишня', 'киви']

print(fruits)
>>>>>>>>>
['apple', 'apricot', 'банан', 'вишня', 'киви', 'lemon', 'mango']
```
![image](https://github.com/user-attachments/assets/91ed5cbe-44d9-4bb6-9e12-e29a9921a070)

### Добавление и удаление элементов в список
**Для добавления нового элемента в конец списка используется метод append()**
```python
numbers = [1, 1, 2, 3, 5, 8, 13]  # создаем список

numbers.append(21)  # добавляем число 21 в конец списка
numbers.append(34)  # добавляем число 34 в конец списка

print(numbers)
>>>>>>>>>
[1, 1, 2, 3, 5, 8, 13, 21, 34]
```
для того чтобы использовать метод append(), нужно, чтобы список был создан (при этом он может быть пустым).     
```python
numbers = []  # создаем пустой список

numbers.append(1)
numbers.append(2)
numbers.append(3)

print(numbers)
>>>>>>>>>
[1, 2, 3]
```
**Можно также расширить список другим списком путём вызова метода extend().**
```python
numbers = [0, 2, 4, 6, 8, 10]
odds = [1, 3, 5, 7]

numbers.extend(odds)
print(numbers)
>>>>>>>>>
[0, 2, 4, 6, 8, 10, 1, 3, 5, 7]
```
Метод extend() как бы расширяет один список, добавляя к нему элементы другого списка.      

Отличие между методами append() и extend() проявляется при добавлении строки к списку.         
**Метод append() добавляет строку целиком к списку, а метод extend() разбивает строку на символы и их добавляет в качестве элементов списка.     
________________________________________
**С помощью оператора del можно удалять элементы списка по определенному индексу.**

```python
numbers = [1, 2, 3, 4, 5, 6, 7, 8, 9]
del numbers[5]    # удаляем элемент, имеющий индекс 5

print(numbers)
>>>>>>>>>
[1, 2, 3, 4, 5, 7, 8, 9]
```
Оператор del работает и со срезами: мы можем удалить целый диапазон элементов списка.
```python
numbers = [1, 2, 3, 4, 5, 6, 7, 8, 9]
del numbers[2:7]    # удаляем элементы с 2 по 6 включительно

print(numbers)
>>>>>>>>>
[1, 2, 8, 9]
```
Мы можем удалить все элементы на чётных позициях (0, 2, 4, ...) исходного списка.
```python
numbers = [1, 2, 3, 4, 5, 6, 7, 8, 9]
del numbers[::2]

print(numbers)
>>>>>>>>>
[2, 4, 6, 8]
```
### Вывод элементов списка
Для вывода элементов списка каждого на отдельной строке можно использовать следующий код:
```python
numbers = [0, 1, 2, 3, 4, 5, 6, 7, 8, 9, 10]

for i in range(len(numbers)):
    print(numbers[i])
>>>>>>>>>
```
Если индексы не нужны:
```python
numbers = [0, 1, 2, 3, 4, 5, 6, 7, 8, 9, 10]

for num in numbers:
    print(num)
>>>>>>>>>
```
**Вывод с помощью распаковки списка**      
Вывод элементов списка через один символ пробела:
```python
numbers = [0, 1, 2, 3, 4, 5, 6, 7, 8, 9, 10]

print(*numbers)
>>>>>>>>>
0 1 2 3 4 5 6 7 8 9 10
```
Вывод элементов списка, каждого на отдельной строке:
```python
numbers = [0, 1, 2, 3, 4, 5, 6, 7, 8, 9, 10]

print(*numbers, sep='\n')
>>>>>>>>>
0
1
2
3
4
5
6
7
8
9
10
```
### split() и join()
Метод split() разбивает строку на слова, используя в качестве разделителя последовательность пробельных символов, и возвращает список из этих слов.     
```python
s = 'Python is the most powerful language'
words = s.split()
print(words)
>>>>>>>>>
['Python', 'is', 'the', 'most', 'powerful', 'language']
```
У метода split() есть необязательный параметр, который определяет, какой набор символов будет использоваться в качестве разделителя между элементами списка. Например, вызов метода split('.') вернёт список, полученный разделением исходной строки по символу '.'.    
```python
ip = '192.168.1.24'
numbers = ip.split('.')    # указываем явно разделитель
print(numbers)
>>>>>>>>>
['192', '168', '1', '24']
```
Метод join() собирает строку из элементов списка, используя в качестве разделителя строку, к которой применяется метод.   
```python
words = ['Python', 'is', 'the', 'most', 'powerful', 'language']
s = ' '.join(words)
print(s)
>>>>>>>>>
Python is the most powerful language
```
![image](https://github.com/user-attachments/assets/afa74ab8-51bc-41d8-9303-2bb52a25cfb4)

### методы списков
Метод insert() позволяет вставлять значение в список в заданной позиции. В него передается два аргумента:

index: индекс, задающий место вставки значения;
value: значение, которое требуется вставить.
Когда значение вставляется в список, список расширяется в размере, чтобы разместить новое значение. Значение, которое ранее находилось в заданной индексной позиции, и все элементы после него сдвигаются на одну позицию к концу списка.
```python
names = ['Gvido', 'Roman', 'Timur']
print(names)
names.insert(0, 'Anders')
print(names)
names.insert(3, 'Josef')
print(names)
>>>>>>>>>
['Gvido', 'Roman', 'Timur']
['Anders', 'Gvido', 'Roman', 'Timur']
['Anders', 'Gvido', 'Roman', 'Josef', 'Timur']
```
Метод index() возвращает индекс первого элемента, значение которого равняется переданному в метод значению. Таким образом, в метод передается один параметр:

value: значение, индекс которого требуется найти.
```python
names = ['Gvido', 'Roman', 'Timur']
position = names.index('Timur')
print(position)
>>>>>>>>>
2
```
Метод remove() удаляет первый элемент, значение которого равняется переданному в метод значению. В метод передается один параметр:

value: значение, которое требуется удалить.
```python
food = ['Рис', 'Курица', 'Рыба', 'Брокколи', 'Рис']
print(food)
food.remove('Рис')
print(food)
>>>>>>>>>
['Рис', 'Курица', 'Рыба', 'Брокколи', 'Рис']
['Курица', 'Рыба', 'Брокколи', 'Рис']
```
Метод pop() удаляет элемент по указанному индексу и возвращает его. В метод pop() передается один необязательный аргумент:

index: индекс элемента, который требуется удалить.
Если индекс не указан, то метод удаляет и возвращает последний элемент списка. Если список пуст или указан индекс за пределами диапазона, то во время выполнения происходит ошибка.
```python
names = ['Gvido', 'Roman', 'Timur']
item = names.pop(1)
print(item)
print(names)
>>>>>>>>>
Roman
['Gvido', 'Timur']
```
Метод count() возвращает количество элементов в списке, значения которых равны переданному в метод значению. 

Таким образом, в метод передается один параметр:

value: значение, количество элементов, равных которому, нужно посчитать.
Если значение в списке не найдено, то метод возвращает 0.
```python
names = ['Timur', 'Gvido', 'Roman', 'Timur', 'Anders', 'Timur']
cnt1 = names.count('Timur')
cnt2 = names.count('Gvido')
cnt3 = names.count('Josef')

print(cnt1)
print(cnt2)
print(cnt3)
>>>>>>>>>
3
1
0
```
Метод reverse() инвертирует порядок следования значений в списке, то есть меняет его на противоположный.
```python
names = ['Gvido', 'Roman', 'Timur']
names.reverse()
print(names)
>>>>>>>>>
['Timur', 'Roman', 'Gvido']
```
Метод clear() удаляет все элементы из списка.
```python
names = ['Gvido', 'Roman', 'Timur']
names.clear()
print(names)
>>>>>>>>>
[]
```
Метод copy() создаёт поверхностную копию списка.
```python
names = ['Gvido', 'Roman', 'Timur']
names_copy = names.copy()              # создаем поверхностную копию списка names

print(names)
print(names_copy)
>>>>>>>>>
['Gvido', 'Roman', 'Timur']
['Gvido', 'Roman', 'Timur']
```
```python
>>>>>>>>>
```
```python
>>>>>>>>>
```

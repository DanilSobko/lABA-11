Лабораторна робота №12: Робота з Матрицями в Python
Мета роботи:
Мета:
Ознайомитися з різними методами роботи з матрицями в Python.

Очікуваний результат:
Отримати практичні навички виконання задач, пов'язаних з обробкою матриць.

Опис завдання:
У цій лабораторній роботі необхідно було реалізувати кілька методів для роботи з матрицями, включаючи додавання елементів, обчислення суми рядків, транспонування, множення, перевірку симетричності, поворот, вирівнювання та отримання діагоналі.
Виконання роботи:
Структура проекту:
Код містить клас Matrix, який включає всі необхідні методи для роботи з матрицями.
Опис файлів:
student_main.py:
Містить Python-код із реалізацією класу Matrix та його методів.

README.md:
Описує структуру проекту, призначення кожного файлу, основні методи класу Matrix з поясненням їх роботи.

Опис основних методів класу Matrix з поясненням їх роботи:
__init__(self, rows, cols, data=None):
Ініціалізує матрицю розміром rows на cols. Якщо дані не задані, створює матрицю, заповнену нулями.

add_element(self, row, col, value):
Додає значення value в позицію (row, col). Викликає помилку, якщо позиція некоректна.

sum_of_rows(self):
Повертає список, що містить суми елементів кожного рядка.

transpose(self):
Повертає нову матрицю, яка є транспонованою версією поточної матриці.

multiply_by(self, other):
Множить поточну матрицю на іншу матрицю other. Викликає помилку, якщо розміри матриць несумісні для множення.

is_symmetric(self):
Перевіряє, чи є матриця симетричною.

rotate_right(self):
Повертає матрицю на 90 градусів за годинниковою стрілкою.

flatten(self):
Повертає матрицю як плоский список.

from_list(list_of_lists):
Створює матрицю з заданого списку списків.

diagonal(self):
Повертає діагональні елементи матриці. Викликає помилку, якщо матриця не квадратна.

Приклади використання:
Ініціалізація матриці:
python
Копіювати код
m = Matrix(3, 3)
Додавання елементу:
python
Копіювати код
m.add_element(0, 0, 5)
Сума рядків:
python
Копіювати код
print(m.sum_of_rows())  # Виведе: [5, 0, 0] (якщо додано лише один елемент)
Транспонування:
python
Копіювати код
t = m.transpose()
print(t.data)
Множення матриць:
python
Копіювати код
m1 = Matrix.from_list([[1, 2], [3, 4]])
m2 = Matrix.from_list([[2, 0], [1, 2]])
m3 = m1.multiply_by(m2)
print(m3.data)  # Виведе: [[4, 4], [10, 8]]
Перевірка симетричності:
python
Копіювати код
print(m.is_symmetric())  # Виведе: False
Поворот матриці:
python
Копіювати код
m.rotate_right()
print(m.data)
Вирівнювання матриці:
python
Копіювати код
print(m.flatten())  # Виведе плоский список елементів
Створення матриці з списку списків:
python
Копіювати код
m = Matrix.from_list([[1, 2, 3], [4, 5, 6], [7, 8, 9]])
print(m.data)
Діагональні елементи:
python
Копіювати код
print(m.diagonal())  # Виведе: [1, 5, 9]
Висновки:
Мета роботи досягнута: були розглянуті та реалізовані різні методи обробки матриць у Python, а також набуті навички роботи з ними.
Інструкції з запуску:
Відкрийте файл будь-яким зручним для вас способом, де є встановлений компілятор Python. Додайте необхідні виведення, наведені у файлі README.md. Після цього запустіть файл для отримання необхідних результатів.
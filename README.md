# Python: основы и применение

*Курс на платформе `stepik.org`. Ссылка на курс: [https://stepik.org/course/512/](https://stepik.org/course/512/).*

---

# Неделя 1. «Функции и стек вызовов»

## Задача 1
Напишите реализацию функции `closest_mod_5`, принимающую в качестве единственного аргумента целое число x и возвращающую самое маленькое целое число y, такое что:

- y больше или равно x
- y делится нацело на 5

Формат того, что ожидается от вас в качестве ответа:
```python
def closest_mod_5(x):
    if x % 5 == 0:
        return x
    return "I don't know :("
```

### ***Моё решение***
```python
def closest_mod_5(x):
    if x % 5 == 0:
        return x
    return x + (5 - x % 5)
```

### ***Рекурсивное решение***
```python
def closest_mod_5(x):
    return x if x % 5 == 0 else closest_mod_5(x + 1)
```

### ***Хитрое решение***
```python
def closest_mod_5(x):
    return (x + 4) // 5 * 5
```
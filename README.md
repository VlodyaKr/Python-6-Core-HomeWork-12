# Програма-бот для ведення телефонної книги

### *Python 6 Core HomeWork 12*

[![Language](https://img.shields.io/badge/language-python-blue)](https://www.python.org)
![GitHub release (latest by date)](https://img.shields.io/github/v/release/VlodyaKr/Python-6-Core-HomeWork-12?color=orange&style=plastic)
![GitHub Release Date](https://img.shields.io/github/release-date/VlodyaKr/Python-6-Core-HomeWork-12?color=blue&style=plastic)
![GitHub repo size](https://img.shields.io/github/repo-size/VlodyaKr/Python-6-Core-HomeWork-12?style=plastic)
![GitHub all releases](https://img.shields.io/github/downloads/VlodyaKr/Python-6-Core-HomeWork-12/total?color=blue&style=plastic)
[![GitHub issues](https://img.shields.io/github/issues/VlodyaKr/Python-6-Core-HomeWork-12?style=plastic)](https://github.com/VlodyaKr/Python-6-Core-HomeWork-12/issues)
[![GitHub forks](https://img.shields.io/github/forks/VlodyaKr/Python-6-Core-HomeWork-12?style=plastic)](https://github.com/VlodyaKr/Python-6-Core-HomeWork-12/network)
[![GitHub stars](https://img.shields.io/github/stars/VlodyaKr/Python-6-Core-HomeWork-12?style=plastic)](https://github.com/VlodyaKr/Python-6-Core-HomeWork-12/stargazers)
___
#### Робота програми

##### Формат запуску з консолі:
##### ***`py assistant.py`***

##### Підтримувані команди:

`help` або `?` - виведення допомоги;

`hello` - привітання;

`add name phone [date]` - додаємо контакт з телефоном в довідник, при першому виклику для контакта можливе додавання дня народження, при наступних викликах додається лише телефон до існуючого контакта;

`change name old_phone new_phone` - змінюємо номер телефону контакту;

`del name phone` - видаляємо номер телефону контакту;

`birthday name date` - додаємо чи змінюємо день народження контакта;

`show name` - виводимо дані одного контакту;

`show all` - виводимо дані всіх контактів;

`days to birthday name` - виводимо кількість днів до дня народження контакту;

`show birthday days N` - виводимо дані контактів, до дня народження яких залишилося не більше N днів;

`good bye` або `close` або `exit` або `.` - вихід з програми

##### Формати введення:

`phone` - для номерів України - 10-ти чи 12-цифровий формат з перевіркою кодів операторів `[+38]0XXXXXXXXX`; для номерів інших країн - формат з 10-14 цифр; допускаються символи `(`, `)`, `-`;

`date' - найпопулярніші формати `DD.MM.YYYY` або `YYYY-MM-DD`.

___
#### Завдання
Потрібно написати консольного бота помічника, який розпізнаватиме команди введені з клавіатури і відповідатиме відповідно введеній команді.

Бот помічник має стати для нас прототипом додатка-асистента. Додаток асистент у першому наближенні повинен уміти працювати з книгою контактів та календарем. У цій роботі зосередимося на інтерфейсі самого робота. Найбільш простий і зручний на початковому етапі розробки інтерфейс - це консольна програма CLI (Command Line Interface). CLI досить просто продати. Будь-який CLI складається з трьох основних елементів:
- Парсер команд. Частина яка відповідає за розбір введених користувачем рядків, виділення з рядка ключових слів та модифікаторів команд.
- Функції обробники команд - набір функцій, які ще називають `handler`, вони відповідають за безпосереднє виконання команд.
- Цикл запит-відповідь. Ця частина програми відповідає за отримання від користувача даних та повернення користувачеві відповіді від функції-`handler`а.

На першому етапі наш бот-асистент повинен вміти зберігати ім'я та номер телефону, знаходити номер телефону на ім'я, змінювати записаний номер телефону, виводити в консоль усі записи, які зберіг. Щоб реалізувати таку нескладну логіку, скористаємося словником. У словнику зберігатимемо ім'я користувача як ключ і номер телефону як значення.

На другому етапі ми повинні реалізувати такі класи:

Клас `AddressBook`, який успадковується від `UserDict`, і ми потім додамо логіку пошуку за записами цього класу.

Клас `Record`, який відповідає за логіку додавання/видалення/редагування необов'язкових полів та зберігання обов'язкового поля `Name`.

Клас `Field`, який буде батьківським для всіх полів, потім потім реалізуємо логіку загальну для всіх полів.

Клас `Name` - обов'язкове поле з ім'ям.

Клас `Phone`, необов'язкове поле з телефоном і один запис (`Record`) може містити кілька.

На третьому етапі:

Додаємо поле для дня народження `Birthday`. Це поле не обов'язкове, але може бути лише одне.

Додаємо функціонал роботи з `Birthday` до класу `Record`, а саме функцію `days_to_birthday`, яка повертає кількість днів до наступного дня народження.

Додаємо функціонал перевірки правильність наведених значень для полів `Phone`, `Birthday`.

Додаємо пагінацію (посторінкове виведення) `AddressBook` для ситуацій, коли книга дуже велика і треба показати вміст частинами, а не все відразу. Реалізуємо це через створення ітератора за записами.

___
#### Автор
[![GitHub Contributors Image](https://contrib.rocks/image?repo=VlodyaKr/Python-6-Core-HomeWork-12)](https://github.com/VlodyaKr)

#### Володимир Кравченко
[Написати автору листа](mailto:vlodya@gmail.com?subject=Python-6-Core-HomeWork-12)
___
#### Ліцензія
[![GitHub license](https://img.shields.io/github/license/VlodyaKr/Python-6-Core-HomeWork-12?style=plastic)](https://github.com/VlodyaKr/Python-6-Core-HomeWork-12/blob/main/LICENSE)

Цей проєкт ліцензується відповідно до ліцензії MIT — подробиці див. у файлі [LICENSE](https://github.com/VlodyaKr/Python-6-Core-HomeWork-12/blob/main/LICENSE)

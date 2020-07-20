## iCovid - засіб візуалізації поширення вірусу SARS-nCov-2
#### v2.0.0

Інструмент призначений для отримання зведених даних щодо поширення вірусу SARS-nCov-2 в Україні та інших країнах світу.
Також надається функціонал для генерування й автоматичного оновлення мережевої сторінки.

_Вигляд інтерфейсу у командному рядку._

![Зображення командного рядка](v2_0_0_cli.png?raw=true "Вигляд даних з консолі")

_Вигляд інтерфейсу на мережевому ресурсі._

![Зображення мережового ресурсу](v2_0_0_web.png?raw=true "Вигляд даних у мережі")


##### Принцип роботи

* Скрипт підвантажує локальну базу даних і створює її резервну копію.
* Скрипт аналізує набір мережевих сторінок, що містять інформацію про поширення вірусу в тій чи іншій державі,
або певному регіоні.
* Отримані дані зберігаються в форматі JSON в якості БД скрипта.
* Наприкінці виконання, скрипт виведе дані для користувача у термінал.
* За наявності додаткового параметру, скрипт згенерує мережеву сторінку для відображення ортиманих даних у
зручнішому вигляді. Додатково скрипт може вивантажити згенеровану сторінку на мережевий сервер.
* Скрипт зберігає оновлені дані у базу даних.


##### Командний інтерфейс
Запуск скрипта виконується командою терміналу:
```sh
./icovid.py
```

Генерування веб-сторінки та її вивантаження ініціюється вказанням прапорця:
```sh
./icovid.py [--web_update | -w]
```

Для отримання додаткової інформації слід увімкнути режим зневадження:
```sh
./icovid.py [--debug | -d]
```

Для отримання допомоги слід викликати меню допомоги:
```sh
./icovid.py [--help | -h]
```

##### Можливі помилки

Наразі існує перелік випадків, коли скрипт може працювати неправильно чи не працювати взагалі.
Серед таких ситуацій є зокрема наступні випадки:
* Зміна формату даних на мережевому ресурсі, звідки скрипт отримує інформацію.
* Зміна моделі взаємодії користувача з клієнтом на мережевому ресурсі.
* Видалення чи зміна мережевої адреси ресурсу.
* тощо.
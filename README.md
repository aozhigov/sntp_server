# Обманывающий SNTP сервер
### Формулировка
Написать "обманывающий" сервер времени. 
На вход передается количество секунд (+ или -) смещения 
относительно точного времени.

### Параметры:
| key | description |
| --- | -----------|
| -h/--help | справка |
-p/--port <port> | порт, который будет слушать сервер
-d/--delay <delay> | (обязательный аргумент) вряме задержки времени относительно точного

### Пример запуска
* sudo python3 -m ./sntp_server -d 60
* ! обязательно запускать с правами админа

### Проверка работы сервера
* Linux: rdate -u -n -v -p localhost
* Windows: ntpdate -d -q localhost
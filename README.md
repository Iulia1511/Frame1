 # Лабораторная работа №1 

## Цель
* Целью данной лабораторной работы является изучение основных принципов протокола HTTP.

## Условие
* Задание №1. Анализ HTTP-запросов

* Зайдите на сайт http://sandbox.usm.md/login.
* Откройте вкладку Network в инструментах разработчика браузера.
* Введите неверные данные для входа (например, username: student, password: studentpass).
* Проанализируйте запросы, которые были отправлены на сервер.
![1](https://github.com/user-attachments/assets/d032dd03-1fb8-436f-81c5-c90f9b888774)
* Ответьте на следующие вопросы:
### Какой метод HTTP был использован для отправки запроса?
* Метод POST
### Какие заголовки были отправлены в запросе?
* Name, status, type , initiator, Size, Time
### Какие параметры были отправлены в запросе?
* Параметры содержат введённые данные для авторизации:
username: student.
password: studentpass.
### Какой код состояния был возвращен сервером?
* Сервер вернул код состояния 401 (Unauthorized), что означает, что попытка авторизации не удалась из-за неверных данных.
### Какие заголовки были отправлены в ответе?
* process.php,401, xhr, jquery-3.6.0.min.js:, 648 B, 29ms

* Повторите шаги 3-5, введя верные данные для входа (username: admin, password: password).
![2](https://github.com/user-attachments/assets/1be3f895-60be-419b-83a6-9b9c5ef978a9)
### Какой метод HTTP был использован для отправки запроса?
* Метод POST
### Какие заголовки были отправлены в запросе?
* Name, status, type , initiator, Size, Time
### Какие параметры были отправлены в запросе?
* Параметры содержат введённые данные для авторизации:
username: admin.
password: password.
### Какой код состояния был возвращен сервером?
* Сервер вернул код состояния 200 (OK), что означает успешную авторизацию.
### Какие заголовки были отправлены в ответе?
* process.php,200, xhr, jquery-3.6.0.min.js:, 638 B, 27ms

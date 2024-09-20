 # Лабораторная работа №1 

## Цель
* Целью данной лабораторной работы является изучение основных принципов протокола HTTP.

## Условие
### Задание №1. Анализ HTTP-запросов

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

### Задание №2. Составление HTTP-запросов
* Составьте GET-запрос к серверу по адресу http://sandbox.com, указав в заголовке User-Agent ваше имя и фамилию.
  ![4](https://github.com/user-attachments/assets/5c67ede4-3668-4772-8169-549c3d292ad2)

* Составьте POST-запрос к серверу по адресу http://sandbox.com/cars, указав в теле запроса следующие параметры:
make: Toyota
model: Corolla
year: 2020
![image](https://github.com/user-attachments/assets/5182c541-e233-4712-9518-5312a99f2855)
* Напишите один из возможных вариантов ответа сервера следующий запрос. http POST /cars HTTP/1.1 Host: sandbox.com Content-Type: application/json User-Agent: John Doe model=Corolla&make=Toyota&year=2020 Предположите ситуации, когда сервер может вернуть HTTP-коды состояния 200, 201, 400, 401, 403, 404, 500.
* 200 OK: Запрос успешно выполнен и данные обновлены или возвращены.

* 201 Created: Новый ресурс успешно создан.

* 400 Bad Request: Неверный формат данных или отсутствуют необходимые параметры.

* 401 Unauthorized: Требуется аутентификация, но она отсутствует или некорректна.

* 403 Forbidden: Аутентификация успешна, но доступ к ресурсу запрещен.

* 404 Not Found: Ресурс не найден по указанному пути.

* 500 Internal Server Error: Внутренняя ошибка сервера при обработке запроса.

## Вывод
В этой лабораторной работе я научилась составлять и отправлять различные HTTP-запросы (GET, POST, PUT), добавлять заголовки и передавать параметры в теле запроса. Я также разобралась с обработкой кодов ответа сервера, таких как 200, 301, 404, 405 и 500.



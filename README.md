Use commands in terminal:


```shell
git clone https://github.com/DmitriiButk/Docker-compose-hw.git
```
```shell
cd Docker-compose-hw\3.2-crud
```
```shell
docker-compose up -d --build
```


Click on one of the links:

http://localhost:7070/api/v1/
or
http://localhost:7070/admin/login/?next=/admin/

**Make sure static files are in place.**
**Done. :)**

#
Домашнее задание к лекции «Docker Compose»
Инструкцию по сдаче домашнего задания вы найдете на главной странице репозитория.

Задание* (необязательное)
Cделать конфигурацию docker-compose любого Вашего проекта из курса по Django, который использует БД (например, CRUD: Склады и запасы).

Результатом является docker-compose.yml файл с описанием конфигурации для развертывания приложения (и не забудьте про Dockerfile).

P.S. для создания конфигурации необходим образ своего проекта, а значит предварительно необходимо описать Dockerfile, сделать образ и потом уже писать docker-compose.yml (это типичный сценарий при работе с Docker и Docker Compose).

Созданные файлы отправьте в личном кабинете на сайте netology.ru

Подсказка:
Конфигурация должна состоять из 3-х контейнеров: backend, postgres, nginx.

Контейнеры объединяются в сеть, которые работают в связке:

Nginx работает в качестве proxy-http для пересылки динамических запросов к Django или возвращая статические html файлы.
PostgreSQL запускается до Django.
Django запускается через Gunicorn.

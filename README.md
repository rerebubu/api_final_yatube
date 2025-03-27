#  <img src="https://github.com/StasKrut/hw05_final/blob/master/yatube/static/img/logo.png" width="100"> atube project API


### Описание
Проект представляет собой API для небольшой социальной сети Yatube, в рамках которого возможно создание и аутентификация пользователей, создание записей, комментариев к ним и подписка на полюбившихся авторов. Записи могут разделяться по группам.

### Стек технологий, использованный в проекте:

- Python 3.7

- Django 2.2.28

- DRF

- JWT

### Запуск проекта в dev-режиме:

- Клонировать репозиторий и перейти в него в командной строке.
- Установить и активировать виртуальное окружение c учетом версии Python 3.7 (выбираем python не ниже 3.7):

```py -3.7 -m venv venv```

```source venv/Scripts/activate```
- Затем нужно установить все зависимости из файла requirements.txt

```python -m pip install --upgrade pip```

```pip install -r requirements.txt```
- Выполняем миграции:

```python manage.py migrate```
- Создаем суперпользователя:

```python manage.py createsuperuser```

Документация  REDOC будет доступна по [ссылке](http://127.0.0.1:8000/redoc/).

### Примеры запросов

```
GET  http://127.0.0.1:8000/api/v1/posts/
```
Результат:
```json
[
    {
        "id": 1,
        "author": "newbor",
        "text": "Hey",
        "pub_date": "2022-08-08T18:41:19.125087Z",
        "image": null,
        "group": null
    },
    {
        "id": 2,
        "author": "newbor",
        "text": "Тестовый пост",
        "pub_date": "2022-08-09T13:23:43.516385Z",
        "image": null,
        "group": null
    }
]
```
```
POST  http://127.0.0.1:8000/api/v1/follow/
```
Данные запроса: 
```json
{
  "following": "leo"
}
```
Результат: 
```json
{
    "id": 1,
    "following": "leo",
    "user": "newbor"
}
```
Проект сделан в рамках учебного процесса по специализации Python-разработчик (backend) Яндекс.Практикум.

Автор в рамках учебного курса ЯП Python - разработчик:
- :white_check_mark: [Stanislav Krutskikh](https://github.com/StasKrut)

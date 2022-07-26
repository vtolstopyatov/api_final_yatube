### Что за проект:

API для [YaTube](https://github.com/vtolstopyatov/hw05_final), с помощью которого можно управлять подписками, постами сервиса и комментариями к ним.

Целью работы над этим проектом стала практика с Django REST framework. Для аутентификации пользователей с помощью токенов, использовался плагин Simple JWT для DRF. Запросы к API во время работы над проектом выполнялись с помощью программы Postman.

### Как запустить проект:

Клонировать репозиторий и перейти в него в командной строке:

```
git clone https://github.com/vtolstopyatov/api_final_yatube.git
```

```
cd api_final_yatube
```

Cоздать и активировать виртуальное окружение:

```
python -m venv venv
```

```
source venv/Scripts/activate
```

Установить зависимости из файла requirements.txt:

```
python -m pip install --upgrade pip
```

```
pip install -r requirements.txt
```

Выполнить миграции:

```
python manage.py migrate
```

Запустить проект:

```
python3 manage.py runserver
```
### Примеры запросов:

Запрос постов:

```
/api/v1/posts/
```

Ответ:

```
[
    {
        "id": 1,
        "author": "admin",
        "text": "First post",
        "pub_date": "2022-07-19T21:53:46.019190Z",
        "image": null,
        "group": null
    }
]
```

Запрос групп:

```
/api/v1/groups/
```

Ответ:

```
[
    {
        "id": 1,
        "title": "First group",
        "slug": "fg",
        "description": "Just first group"
    }
]
```

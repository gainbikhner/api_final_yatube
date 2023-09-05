# REST API для проекта Yatube

## Описание

Реализована аутентификация по JWT-токену.

### Автор

https://github.com/gainbikhner

### Стек технологий

- Django
- DRF
- JWT

### Документация API

http://127.0.0.1:8000/redoc/

## Инструкция

### Как запустить проект

Клонировать репозиторий и перейти в него в командной строке:

```
git clone https://github.com/gainbikhner/api_final_yatube.git
```

```
cd api_final_yatube
```

Cоздать и активировать виртуальное окружение:

```
python3 -m venv env
```

```
source env/bin/activate
```

Установить зависимости из файла requirements.txt:

```
python3 -m pip install --upgrade pip
```

```
pip install -r requirements.txt
```

Выполнить миграции:

```
python3 manage.py migrate
```

Запустить проект:

```
python3 manage.py runserver
```

Создать юзера для админки:

```
python3 manage.py createsuperuser
```

## Примеры

### Запросы к API

Получить все посты / опубликовать новый пост:

```
http://127.0.0.1:8000/api/v1/posts/
```

```
{
    "text": "string",
    "image": "string",
    "group": 0
}
```

Получить все комментарии к посту / опубликовать новый комментарий:

```
http://127.0.0.1:8000/api/v1/posts/{post_id}/comments/
```

```
{
    "text": "string"
}
```

Получить токен:

```
http://127.0.0.1:8000/api/v1/jwt/create/
```

```
{
    "username": "string",
    "password": "string"
}
```

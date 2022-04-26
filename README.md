**Описание проекта:**
<br>
<br>В API для Yatube реализованы следующие задачи:
- создавать пользователей;
- любой пользователь может просматривать список постов и отдельный существующий пост, список сообществ и отдельное сообщество, создавать комментари к существующим постам;
- авторизованые пользователи могут создавать посты и при желании присваивать им существующие сообщества, комментировать существующие посты, подписываться на других авторов, просматривать свои подписки и осуществлять поиск по определенному автору;
- авторы постов и комментариев могут их удалять, исправлять полностью и частично.

Документация для API **Yatube**: (http://127.0.0.1:8000/redoc/)


______________________________________________
**Как запустить проект:**

Клонировать репозиторий и перейти в него в командной строке:

```
git clone https://github.com/yandex-praktikum/kittygram2plus.git
```

```
cd kittygram2plus
```

Cоздать и активировать виртуальное окружение:

```
python3 -m venv env
```

```
source env/bin/activate
```

```
python3 -m pip install --upgrade pip
```

Установить зависимости из файла requirements.txt:

```
pip install -r requirements.txt
```

Выполнить миграции:

```
python3 manage.py migrate
```

Запустить проект:

```
python3 manage.py runserver
```

_________________________________________________________________________
**Примеры запросов к API:**

<br> Создание поста и просмотр списка постов:
```
http://127.0.0.1:8000/api/v1/posts/
```

Удаление, редактирование и просмотр отдельного поста:
```
http://127.0.0.1:8000/api/v1/posts/{id}/
```
Добавление комментария, получение списка комментариев:
```
http://127.0.0.1:8000/api/v1/posts/{post_id}/comments/
```

Получение отдельного комментария и редактирование его:
```
http://127.0.0.1:8000/api/v1/posts/{post_id}/comments/{id}/
```

Получение списка сообществ:
```
http://127.0.0.1:8000/api/v1/groups/
```

Получение информации о сообществе:
```
http://127.0.0.1:8000/api/v1/groups/{id}/
```

Подписки:
```
http://127.0.0.1:8000/api/v1/follow/
```

Получить JWT-токен:
```
http://127.0.0.1:8000/api/v1/jwt/create/
```

Обновить JWT-токен:
```
http://127.0.0.1:8000/api/v1/jwt/refresh/
```


Проверить JWT-токен:
```
http://127.0.0.1:8000/api/v1/jwt/verify/
```

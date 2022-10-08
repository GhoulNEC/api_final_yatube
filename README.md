# API final Yatube
***
<details>
    <summary style="font-size: 16pt; font-weight: bold">Описание</summary>

#### В проекте API Yatube реализована возможность пользоваться функционалом сайта Yatube без посещения самого сайта.

### Через этот API Вы сможете:
* Просматривать посты авторов.
* Создавать, изменять и удалять собственные посты.
* Просматривать существующие группы.
* Просматривать комментарии к постам.
* Создавать, удалять и редактировать собственные комментарии.
* Подписываться на авторов постов.

</details>

***
<details>
    <summary style="font-size: 16pt; font-weight: bold">Технологии</summary>

* Python 3.9.6
* Django 2.2.16
* djangorestframework 3.12.4

С полным списком технологий можно ознакомиться в файле ```requirements.txt```

</details>

***
<details>
    <summary style="font-size: 16pt; font-weight: bold">Документация</summary>

С документацией проекта можно ознакомиться по [ссылке](http://127.0.0.1:8000/redoc/) после запуска проекта.

</details>

***
<details>
    <summary style="font-size: 16pt; font-weight: bold">Запуск проекта</summary>

### Как запустить проект:

Клонировать репозиторий и перейти в него в командной строке:

```
git clone https://github.com/GhoulNEC/api_final_yatube.git
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

```
python3 -m pip install --upgrade pip
```

Установить зависимости из файла requirements.txt:

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

</details>

***
<details>
    <summary style="font-size: 16pt; font-weight: bold">Примеры получения API</summary>

___
### Регистрация
Для получения токена отправляем POST-запрос с эндпоинтом ```api/v1/jwt/create/```, передав в него ```username``` и ```password```.

В ответ на запрос Вы получите два токена:
* ```refresh``` - нужен для обновления текущего токена.
* ```access``` - используется для аутентификации пользователя.

### Создание поста
Для создания поста нужно отправить POST-запрос с эндпоинтом ```api/v1/posts/```, передав в него обязательное поле ```text```.
Так же в заголовок запроса нужно передать ```Authorization```:```Bearer <token>```

</details>

***
<details>
    <summary style="font-size: 16pt; font-weight: bold">Автор</summary>

[Роман Евстафьев](https://github.com/GhoulNEC)

</details>

***
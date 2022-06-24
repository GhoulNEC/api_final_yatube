# API final
___

## Описание
___
#### В проекте API Yatube реализована возможность пользоваться функционалом сайта Yatube без посещения самого сайта.

### Через этот API Вы сможете:
* Просматривать посты авторов.
* Создавать, изменять и удалять собственные посты.
* Просматривать существующие группы.
* Просматривать комментарии к постам.
* Создавать, удалять и редактировать собственные комментарии.
* Подписываться на авторов постов.

#### Можно обратиться к документации по [ссылке](http://127.0.0.1:8000/redoc/).

## Установка
___
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

## Примеры
___
### Регистрация
Для получения токена отправляем POST-запрос с эндпоинтом ```auth/jwt/create/```, передав в него ```username``` и ```password```.

В ответ на запрос Вы получите два токена:
* ```refresh``` - нужен для обновления текущего токена.
* ```access``` - используется для аутентификации пользователя.

### Создание поста
Для создания поста нужно отправить POST-запрос с эндпоинтом ```api/v1/posts/```, передав в него обязательное поле ```text```.
Так же в заголовок запроса нужно передать ```Authorization```:```Bearer <token>```

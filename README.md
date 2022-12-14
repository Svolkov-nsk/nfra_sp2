# Проект YaMDb

Сервис YaMDb — база отзывов о фильмах, книгах и музыке.

Это совместный проект и настоящая командная работа трёх студентов на Яндекс.Практикум


## Описание проекта

API для сервиса YaMDb.

**Отзывы**: получить список всех отзывов, создать новый отзыв, получить отзыв по id, частично обновить отзыв по id, удалить отзыв по id.

**Комментарии к отзывам**: получить список всех комментариев к отзыву по id, создать новый комментарий для отзыва, получить комментарий для отзыва по id, частично обновить комментарий к отзыву по id, удалить комментарий к отзыву по id.

**JWT-токен**: отправить confirmation_code на переданный email, получение JWT-токена в обмен на email и confirmation_code.

**Пользователи**: получить список всех пользователей, создание пользователя, получить пользователя по username, изменить данные пользователя по username, удалить пользователя по username, получить данные своей учетной записи, изменить данные своей учетной записи.

**Категории (типы) произведений**: получить список всех категорий, создать категорию, удалить категорию.

**Категории жанров**: получить список всех жанров, создать жанр, удалить жанр.

**Произведения, к которым пишут отзывы**: получить список всех объектов, создать произведение для отзывов, информация об объекте, обновить информацию об объекте, удалить произведение.


### Полная документация API 

по адресу `http://127.0.0.1:8000/redoc/`


## Как запустить проект
Как запустить проект:
Клонируйте репозиторий и перейдите в него в командной строке:

git clone https://github.com/Svolkov-nsk/infra_sp2
cd infra_sp2
Перейдите в папку с проектом:

cd api_yamdb
Cоздайте и активируйте виртуальное окружение:

python3 -m venv venv
. venv/bin/activate
python3 -m pip install --upgrade pip
Установите зависимости из файла requirements.txt:

pip install -r requirements.txt
Перейдите в папку с файлом docker-compose.yaml:

cd infra
Разверните контейнеры:

docker-compose up -d --build
Выполните миграции:

docker-compose exec web python manage.py migrate
Создайте суперпользователя:

docker-compose exec web python manage.py createsuperuser
Соберите статику:

docker-compose exec web python manage.py collectstatic --no-input
## Запуск тестов


Из корня проекта:


```
pytest
```


## Авторы

[Сергей Волков](https://github.com/Svolkov-nsk)
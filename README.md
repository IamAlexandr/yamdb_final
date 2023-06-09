![yamdb_workflow](https://github.com/IamAlexandr/yamdb_final/actions/workflows/yamdb_workflow.yml/badge.svg?event=push)
# Групповой учебный проект "REST API YaMDb"
## Яндекс.Практикум
### Описание
Проект YaMDb собирает отзывы (Review) пользователей на произведения (Titles). Произведения делятся на категории: «Книги», «Фильмы», «Музыка». Список категорий (Category) может быть расширен администратором (например, можно добавить категорию «Изобразительное искусство» или «Ювелирка»). В каждой категории есть произведения: книги, фильмы или музыка. Произведению может быть присвоен жанр (Genre) из списка предустановленных. Новые жанры может создавать только администратор. Пользователи оставляют к произведениям текстовые отзывы (Review) и ставят произведению оценку в диапазоне от одного до десяти (целое число); из пользовательских оценок формируется усреднённая оценка произведения — рейтинг (целое число). На одно произведение пользователь может оставить только один отзыв.


### Технологии проекта
- Python 3.9
- Django
- Django REST Framework
- SQLite3
- Simple-JWT
- Git

### Запуск
- Клонировать репозиторий и перейти в него в командной строке:
```
git clone git@github.com:theramblingrover/api_yamdb.git
```
```
cd api_yamdb
```
- Cоздать и активировать виртуальное окружение: python -m venv venv
```
python3 -m venv venv
```
```
source venv/bin/activate
```
```
python3 -m pip install --upgrade pip
```

- Установить зависимости из файла requirements.txt:
```
pip install -r requirements.txt
```

- При необходимости подготовить миграции:
```
python3 manage.py makemigrations
```

- Выполнить миграции:
```
python3 manage.py migrate
```
- Запустить проект:
```
python3 manage.py runserver
```
Подробная документация по API доступна по адресу http://localhost:8000/redoc/.


### Как запустить проект на боевом сервере:
- Установить на сервере docker и docker-compose. Скопировать на сервер файлы docker-compose.yaml и default.conf:
```
-scp docker-compose.yaml <логин_на_сервере>@<IP_сервера>:/home/<логин_на_сервере>/docker-compose.yaml
-scp default.conf <логин_на_сервере>@<IP_сервера>:/home/<логин_на_сервере>/nginx/default.conf
```
- Выполнить команды:
```
git add .

git commit -m ""

git push
```
- После успешного завершения процессов workflow на боевом сервере необходимо выполнить следующие команды:
```
sudo docker-compose exec web python manage.py migrate

sudo docker-compose exec web python manage.py createsuperuser

sudo docker-compose exec web python manage.py collectstatic --no-input 
```

### Участники проекта:
- Dmitriy839
- IamAlexandr
- theramblingrover

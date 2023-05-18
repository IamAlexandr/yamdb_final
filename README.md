  [![GitHub Workflow Status](https://img.shields.io/github/workflow/status/IamAlexandr/yamdb_final/.github/workflows/yamdb_workflow.yml?label=YamDB_workflow)](https://github.com/IamAlexandr/yamdb_final/actions/workflows/yamdb_workflow.yml)
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

### Участники проекта:
- Dmitriy839
- IamAlexandr
- theramblingrover

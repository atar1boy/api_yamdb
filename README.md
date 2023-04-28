### Сервис позволяющий пользователям оценивать и писать свои рецензии на любые категории творчества
api_yamdb

## Команда разработчиков:
Самсонов Дмитрий
Никита Ковалев
Алексей Наумов

## Используемые технолологии:

Django v.3.2
djangorestframework v.3.12.4
PyJWT v.2.1.0

## Как запустить проект:

Клонировать репозиторий и перейти в него в командной строке:

```
git clone git@github.com:Samsooon/api_yamdb.git
```

Cоздать и активировать виртуальное окружение:

```
python3 -m venv env
```

* Если у вас Linux/macOS

    ```
    source env/bin/activate
    ```

* Если у вас windows

    ```
    source env/scripts/activate
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

* !!!Если некоторые таблицы не создадутся, после предыдущей команды     используйте...!!!:

    ```
    python manage.py migrate --run-syncdb
    ```

Далее можно загрузить в базу данных тестовые данные с помощью следующей команды:

```
python manage.py import_data
```

А теперь запускаем!:

```
python manage.py runserver
```

## Аунтификация токена:

Самостоятельная регистрация и подтверждение адреса электронной почты:

```
http://127.0.0.1:8000/api/v1/auth/signup/
```

Получить/обновить токен:

```
http://127.0.0.1:8000/api/v1/auth/token/
```

## Примеры запросов к Api:

Получение ревью по id тайтла.

```
http://127.0.0.1:8000/api/v1/titles/1/reviews/
```
Получение списка комментариев на ревью
```
http://127.0.0.1:8000/api/v1/titles/1/reviews/1/comments/
```
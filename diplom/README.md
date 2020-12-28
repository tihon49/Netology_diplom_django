# Инструкция по запуску проекта

* Создать виртуальное окружение
* Установить все зависимости командой: 
```
pip install -r requirements.txt

(файл requirements.txt находится в корневой папке проекта)
```
* Настройка базы данных (settings.py):
```buildoutcfg
DATABASES = {
    'default': {
        'ENGINE': 'django.db.backends.postgresql',
        'NAME': 'django_diplom',
        'USER': 'postgres',
        'PASSWORD': '1234',
        'HOST': 'localhost',
        'PORT': '5432',
    }
}
```
* Для тестового заполнения сайта выполнить следующие команды:
```buildoutcfg
python manage.py migrate
python manage.py loaddata fixture.json
```
после чего будет доступен аккаунт admin с паролем admin
* Запустить проект комадой:
```
python manage.py runserver
```
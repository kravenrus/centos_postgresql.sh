# Инструкция по использованию скрипта

**В скрипте реализована установка сервера PostgreSQL при его отсутствии или же удаление, если он установлен. Так же если сервер установлен, по желанию, есть возможность создать базу данных и пользователя с правами на нее.**

Для начала необходимо переключиться на суперпользователя (root), введя команду ниже и пароль по требованию

    su
Перед началом работы необходимо установить **git**

    sudo dnf install -y git
Скачивание данного репозитория

    git clone https://github.com/kravenrus/centos_postgresql.sh.git
Переход в каталог со скаченным репозиторием

    cd centos_postgresql.sh
Делаем скрипт исполняемым

    chmod +x ./postgresql.sh
Запуск скрипта

    ./postgresql.sh
Вывод созданных пользователей **(на месте PORT - порт на котором запущен сервер)**

    sudo -i -u postgres psql -p PORT -c 'select * from pg_shadow;'
Вывод созданных баз данных **(на месте PORT - порт на котором запущен сервер)**

    sudo -i -u postgres psql -p PORT -c 'select * from pg_database;'

## Демонстрация

![Farmers Market Finder Demo](demo.gif)

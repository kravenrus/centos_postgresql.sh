# Инструкция по использованию скрипта

    su
Перед началом работы необходимо установить **git**

    sudo dnf install -y git
Для скачивания данного репозитория введите

    git clone https://github.com/kravenrus/centos_postgresql.sh.git
Делаем скрипт исполняемым

    chmod +x ./postgresql.sh
    
    cd centos_postgresql.sh
Запуск скрипта

    ./postgresql.sh

sudo -i -u postgres psql -p $port -c 'select * from pg_shadow;'

sudo -i -u postgres psql -p $port -c 'select * from pg_database;'

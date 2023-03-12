# 08-ansible-04-role

Playbook устанавливает Clickhouse, Vector и Lighthouse на три хоста, доступные по по ssh, запускает службы `clickhouse-server`, `vector`, создает базу `logs` в `clickhouse`,устанавливает и запускает веб-север nginx, разворачивает web-интерфейс `lighthouse`

### Variables

| Имя           | Значение по умолчанию | Описание                        |
| -------------- | ------------- | -----------------------------------|
| `clickhouse_version` |  "22.3.3.44" | Версия Clickhouse |
| `clickhouse_packages` | clickhouse-client, clickhouse-server, clickhouse-common-static | Пакеты Clickhouse для установки |
| vector_version | "0.27.0" | Версия Vector |
|lighthouse_src| https://github.com/VKCOM/lighthouse/archive/refs/heads/master.zip|ссылка на zip-архив ветки master в  git lighthouse|
|nginx_user_name|root|пользователь для запуска  nginx|
    
### Install Clickhouse
 Скачиваются rpm пакеты, устанавливается Сlickhouse, создается база logs. 
 
### Install Vector
Скачиваются пакеты, устанавливается Vector. Запуск службы.

### Install Lighthouse
Устанавливается веб-сервер nginx. Настраивается конфиги веб-сервера. Добавляется сервис nginx в автозагрузку. Создается директория /var/www/
Распаковываются файлы lighthouse.


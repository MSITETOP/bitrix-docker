# Подключение к MySql

Для подключения к базе данных необходимо использовать в качестве адреса сервера
название сервиса MySql, по-умолчанию название `mysql`

Пароль `root` пользователя указывается в `.env` файле в переменной 
`MYSQL_ROOT_PASSWORD`

# Настройка SSL

SSL настраивается автоматически при запуске `docker-compose.yml`

Для избежания ошибки небезопасного соединения необходимо добавить 
корневой сертификат `rootCA.pem` в доверенные сертификаты системы, это требуется сделать
только один раз, все сертификаты выдаваемые контейнером `Nginx` создают их на основе
корневого сертефиката

# Запуск

`docker compose up -d`


# Объединение частей бекапа для распаковки

`cat *$(ls -v  bs.view.ipg4you.com_20231001_075454_full.tar.*) > backup.tar.gz`

# для windows
копировать проект обяхательно в linux и оттуда же запускать docker

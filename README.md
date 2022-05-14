# 08-ansible-03-yandex

## Что делает playbook

Плейбук развернёт три приложения на разных хостах используя роли:

- Clickhouse
- Lighthouse/Nginx	
- Vector/Nginx

## Для веб доступа к БД clickhouse

- После установки необходимо в строке браузера указать IP адрес сервера clickhouse-02
- После перехода на сайт, необходимо указать IP адрес сервера clickhouse-01 (таким образом мы получим доступ к БД clickhouse через web)
- Для проверки записи логов необходимо в строке браузера указать IP адрес сервера clickhouse-03 там мы увидим стандартную страницу Nginx логи о посещении которой передаются через vector
- Теперь на веб странице clickhouse-02, в базе данных logs, в таблице access_logs, после обновления мы увидим данные лога /var/log/nginx/access.log с сервера clickhouse-03

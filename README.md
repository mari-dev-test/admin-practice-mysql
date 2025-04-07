# Инструкция по запуску MySQL-стенда

## Требования
- Docker
- Docker Compose

## Запуск
1. Клонируйте репозиторий

2. Выполните: 
   """
   docker-compose up -d
   """

3. Проверка подключения:
   - MySQL: `localhost:3306`
   - phpMyAdmin: [http://localhost:8080](http://localhost:8080)

## Подключение
- *MySQL*:
   - username: root | password: superpass
   - username: user | password: user123
   - База данных: admin_practice
- *phpMyAdmin*:
   - username: root | password: rootpass

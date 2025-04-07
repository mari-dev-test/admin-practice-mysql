# Инструкция по запуску MySQL-стенда

## Требования
- Docker
- Docker Compose

## Установка Docker и Docker Compose
1. **Обновите репозитории пакетов:**
- ```sudo apt update```
2. **Установите Docker:**
- ```sudo apt install -y docker.io```
3. **Установите Docker Compose:**
- ```sudo apt install -y docker-compose```
4. **Добавьте текущего пользователя в группу Docker, чтобы использовать Docker без sudo:**
- ```sudo usermod -aG docker $USER```
5. **Обновите группу пользователя, чтобы изменения вступили в силу:**
- ```newgrp docker```
6. **Проверьте, что Docker и Docker Compose успешно установлены:**
- ```docker --version```
- ```docker-compose --version```

## Запуск
1. **Клонируйте репозиторий**
Откройте терминал и выполните команду для клонироваия репозитория
- ```git clone https://github.com/mari```
2. **Перейдите в папку с проектом**: 
- ```cd admin-practice-mysql```
3. **Запустите контейнеры с помощью Docker Compose:**
- ```docker-compose up -d```
3. Проверка подключения:
   - MySQL: `localhost:3306`
   - phpMyAdmin: [http://localhost:8080](http://localhost:8080)

## Данные для подключения к БД
**MySQL**:
   - username: root | password: superpass
   - username: user | password: user123
   - База данных: admin_practice
   
**phpMyAdmin:**
   - username: root | password: rootpass

## Подключение к БД
Чтобы подключить к БД через терминал, выполните следующую команду:
**root:**
- ```docker exec -it admin-practice-mysql mysql -u root -p superpass admin_practice```

**user:**
- ```docker exec -it admin-practice-mysql mysql -u user -p user123 admin_practice```

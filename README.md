# Инструкция по запуску MySQL-стенда

## Требования
- Docker
- Docker Compose

## Установка Docker и Docker Compose
1. **Обновите репозитории пакетов:**

```sudo apt update```

2. **Установите Docker:**

```sudo apt install -y docker.io```

3. **Установите Docker Compose:**

```sudo apt install -y docker-compose```

4. **Добавьте текущего пользователя в группу Docker, чтобы использовать Docker без sudo:**

```sudo usermod -aG docker $USER```

5. **Обновите группу пользователя, чтобы изменения вступили в силу:**

```newgrp docker```

6. **Проверьте, что Docker и Docker Compose успешно установлены:**

```docker --version```

```docker-compose --version```

## Запуск
1. **Остановите локальную службу MySQL (если установлена):**

Если у вас установлен MySQL вне Docker, он может занимать порт 3306, и контейнер не сможет стартовать. Чтобы избежать конфликта, остановите службу:

```sudo systemctl stop mysql```

2. **Клонируйте репозиторий**

Откройте терминал и выполните команду для клонироваия репозитория

```git clone https://github.com/mari-dev-test/admin-practice-mysql.git```

3. **Перейдите в папку с проектом**: 

```cd admin-practice-mysql```

4. **Запустите контейнеры с помощью Docker Compose:**

```docker-compose up -d```

5. Проверьте, что всё работает:

```docker ps```

## Данные для подключения к БД
**MySQL**:
   - username: ```root``` | password: ```superpass```
   - username: ```user``` | password: ```user123```
   - База данных: ```admin_practice```

**phpMyAdmin:**
   - username: ```root``` | password: ```superpass```

## Подключение к БД
Чтобы подключить к БД через терминал, выполните следующую команду:

**root:**
- ```docker exec -it mysql_admin mysql -u root -psuperpass admin_practice```

**user:**
- ```docker exec -it mysql_admin mysql -u user -puser123 admin_practice```

## Задания
Файл с практическими заданиями для работы с MySQL находится в каталоге tasks/ и называется tasks.md. В нем содержится список практических задач по администрированию MySQL, включая создание пользователей, управление привилегиями, бэкапами и другие задачи для закрепления навыков работы с MySQL.

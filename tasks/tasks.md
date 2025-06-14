# Практические задания по администрированию MySQL

## Раздел 1: Управление пользователями
1. Создайте пользователя readonly_user с доступом только к SELECT.
2. Создайте пользователя editor_user с доступом на SELECT и INSERT.
3. Ограничьте доступ пользователя readonly_user только к базе practice_db.
4. Ограничьте подключение пользователя editor_user только с локального хоста.
5. Измените пароль пользователя readonly_user на newpassword123.
6. Дайте пользователю editor_user возможность удалять записи в таблице posts.
7. Удалите пользователя readonly_user из базы данных.
8. Дайте привилегии пользователю editor_user на все таблицы в базе данных admin_practice.
9. Отмените все привилегии для пользователя editor_user на базе данных admin_practice.
10. Создайте временного пользователя temp_user с ограничением действия на 1 день (используйте EVENT для удаления).
11. Заблокируйте пользователя editor_user, временно отключив ему доступ.
12. Создайте роль admin_role и назначьте ей все привилегии на базу admin_practice.

## Раздел 2: Бэкапы и восстановление
13. Создайте резервную копию базы данных admin_practice в файл admin_practice_backup.sql.
14. Восстановите базу данных из файла admin_practice_backup.sql.
15. Настройте автоматическое создание резервных копий базы данных каждые 24 часа.
16. Настройте скрипт для резервного копирования только выбранных таблиц из базы данных.
17. Создайте резервную копию в сжатом формате (например, gzip).

## Раздел 3: Производительность и мониторинг
18. Найдите запросы, которые выполняются более 10 секунд.
19. Изучите использование индексов в таблице posts и создайте индекс на поле user_id.
20. Оптимизируйте таблицу posts, используя команду OPTIMIZE TABLE.
21. Используйте команду SHOW STATUS для мониторинга производительности MySQL.
22. Создайте EXPLAIN для запроса, чтобы увидеть, как MySQL планирует его выполнение.
23. Установите и подключите утилиту mysqltuner для анализа производительности.
24. Настройте лог медленных запросов с порогом 2 секунды выполнения.

## Раздел 4: Безопасность
25. Включите шифрование для соединений с MySQL.
26. Настройте ограничение на количество неудачных попыток входа для пользователей.
27. Настройте аудит (логирование) всех операций с базой данных.
28. Включите SSL для MySQL для более безопасных подключений.
29. Ограничьте доступ к базе данных admin_practice только с конкретных IP-адресов.
30. Создайте и примените политику паролей для пользователей.
31. Настройте двухфакторную авторизацию для доступа к phpMyAdmin (через базовую HTTP-аутентификацию).
32. Настройте firewall (например, ufw или iptables) для ограничения внешнего доступа к порту 3306.

## Раздел 5: Работа с таблицами и данными
33. Измените таблицу users, добавив новое поле phone_number типа VARCHAR(15).
34. Удалите все записи в таблице likes, где столбец created_at старше 1 года.
35. Переносите все данные из таблицы posts в новую таблицу с именем archived_posts (сохраните структуру).
36. Обновите все email-адреса в таблице users, заменив домен gmail.com на example.com.
37. Удалите все записи из таблицы comments, которые не имеют лайков в таблице likes.
38. Создайте новый индекс на столбце content таблицы posts.
39. Создайте представление (VIEW), объединяющее таблицы posts и users с именами автора и содержимым поста.
40. Создайте триггер, который будет автоматически добавлять запись в лог при вставке новой строки в таблицу comments.

## Раздел 6: Журналирование и отладка
41. Включите журнал запросов в MySQL.
42. Создайте таблицу для хранения журналов ошибок и вставьте в неё последние ошибки из MySQL.
43. Изучите журнал ошибок MySQL с помощью команды SHOW ERROR LOG.
44. Установите уровень логирования запросов для отслеживания медленных запросов.
45. Просмотрите и проанализируйте лог медленных запросов MySQL.

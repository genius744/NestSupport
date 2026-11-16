# Установка и запуск NeftSupport

## 1. Требования к среде

Для работы проекта использовалась следующая конфигурация:

- Windows 11
- WSL2
- Ubuntu 22.04
- Docker Desktop
- Visual Studio Code
- Расширение Dev Containers

## 2. Используемые компоненты

- Frappe Framework 15
- ERPNext 15
- Frappe Wiki версии 3
- MariaDB 11.8
- Redis

## 3. Структура среды разработки

Основная рабочая директория:

`/workspace/development/frappe-bench`

Каталог приложений:

`/workspace/development/frappe-bench/apps`

В каталоге приложений находятся:

- frappe
- erpnext
- wiki

## 4. Запуск среды

1. Запустить Docker Desktop.
2. Открыть проект в Visual Studio Code.
3. Подключиться к Dev Container Frappe Bench.
4. Открыть терминал внутри контейнера.

## 5. Запуск ERPNext

Перейти в каталог Bench:

`cd /workspace/development/frappe-bench`

Выполнить команду:

`bench --site neftsupport.localhost serve --port 8000`

После запуска открыть в браузере:

`http://localhost:8000/app`

## 6. Запуск базы знаний Wiki

После запуска ERPNext база знаний доступна по адресу:

`http://localhost:8000/wiki-app`

## 7. Остановка

Для остановки локального сервера нажать `Ctrl + C` в терминале, где выполняется команда запуска.

## 8. Резервное копирование

Для создания резервной копии сайта с файлами используется команда:

`bench --site neftsupport.localhost backup --with-files`

Резервные копии сохраняются в каталоге:

`sites/neftsupport.localhost/private/backups/`

## 9. Примечание

Данная инструкция описывает запуск уже установленной среды разработки. Для развёртывания проекта на другом компьютере дополнительно потребуется установить Docker, подготовить Dev Container, получить исходный код приложений и восстановить резервную копию сайта.

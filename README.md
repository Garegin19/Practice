# Это подробная инструкция по пользованию git

## Что такое GIT?    
Git - _это система контроля версий_, удобный инструмент для __командной разработки.__

## Первоначальная настройка    
Настройка информации о пользователе для всех локальных репозиториев  
$ git config --global user.name "[имя]"  

## Создание репозитория
$ git init [название проекта]  
Создаёт новый локальный репозиторий с заданным именем

$ git clone [url-адрес]  
Скачивает репозиторий вместе со всей его историей изменений

## Основные команды и операции
$ git rm [файл]  
Удаляет конкретный файл из рабочей директории и индексирует его удаление

$ git mv [оригинальный файл] [новое имя]  
Перемещает и переименовывает указанный файл, сразу индексируя его для последующего коммита

$ git status  
Перечисляет все новые или изменённые файлы, которые нуждаются в фиксации

$ git add [файл]  
Индексирует указанный файл для последующего коммита

$ git commit -m "[сообщение с описанием]"  
Фиксирует проиндексированные изменения и сохраняет их в историю версий

$ git log  
История коммитов для текущей ветки

$ git push [удалённый репозиторий] [ветка]  
Загружает все изменения локальной ветки в удалённый репозиторий




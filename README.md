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

$ git log --oneline  
Краткая история коммитов для текущей ветки

$ git push [удалённый репозиторий] [ветка]  
Загружает все изменения локальной ветки в удалённый репозиторий

## Статусы untracked/tracked, staged и modified  
Одна из ключевых задач Git — отслеживать изменения файлов в репозитории. Для этого каждый файл помечается каким-либо статусом. Рассмотрим основные.

__untracked__ - неотслеживаемый тип файлов, гит видит, что такой файл существует, но не отслеживает его изменения. У __untracked-файла__ нет предыдущих версий, зафиксированных в коммитах или через команду __git add__.  

__staged__ - подготовленный тип файлов. После выполнения команды __git add__ файл попадает в _staging area_ (от англ. stage — «сцена», «этап [процесса]» и area — «область»), то есть в список файлов, которые войдут в коммит. В этот момент файл находится в состоянии _staged._  

__tracked__ - отслеживаемый тип файлов. Состояние __tracked__ — это противоположность untracked. Оно довольно широкое по смыслу: в него попадают файлы, которые уже были зафиксированы с помощью _git commit_, а также файлы, которые были добавлены в staging area командой _git add_. То есть все файлы, в которых Git так или иначе отслеживает изменения.

__modified__ - отслеживаемый тип файлов. Состояние __modified__ означает, что Git сравнил содержимое файла с последней сохранённой версией и нашёл отличия. Например, файл был закоммичен и после этого изменён.  

__Большинство файлов в проектах «шагает» по следующему циклу: «изменён» → «добавлен в список на коммит» → «закоммичен» → «изменён» → и так далее.__





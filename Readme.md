# Инструкция по работе с Git и удалёнными репозиториями

## Что такое git?
**Git** - это наиболее популярная реализация распределённой системы контроля версий. Самая популярная реализация **Git** - это [GitHub](https://github.com/)

## Подготовка репозитория
Для сооздания репозитория используется команда *git init*. Для этого необходимо в терминале перейти в пустую папку, где в будущем будет репозиторий. Затем в терминале с папкой написать команду *git init*.

## Создание коммитов

### Добавление файла к коммиту
Для добавления файла к будущему коммиту используется команда *git add*. Для этого в терминале с папкой-репозиторием необходимо написать *git add <название файла>*.

### Создание коммита
Для создания коммита используется команда *git commit*. Для этого в терминале с папкой репозиторием необходимо написать *git commit -m <сообщение к коммиту>*. Сообщение к коммиту писать ***ОБЯЗАТЕЛЬНО!!!***.

## Журнал изменений
Для просмотра журнала изменений используется команда *git log*. Для этого в терминале с папкой-репозиторием необходимо написать *git log*.

## Перемещение между коммитами
Для перемещения на предущие коммиты используется команда *git checkout*. Для этого необходимо в журнале изменений, как показано в предыдущей части, найти необходимый коммит и его номер. После чего в терминале с папкой-репозиторием написать команду *git checkout <номер коммита>*. После примененения этой команды Вы попадёте в состояние **Detached head**, в котором никакие изменения фиксироваться не будут. Для возврата в обычное состояние необходимо написать команду *git checkout master*.

## Ветки в Git
### Создание веток в Git
Для создания новой ветки используется команда *git branch*. Для этого в терминале с папкой-репозиторием необходимо написать *git branch <название ветки>*
### Просмотр списка веток
Для просмотра списка веток используется комнада *git branch*. Для этого в терминале с папкой-репозиторием необходимо написать команду *git branch*. Зелёным цветом с символом **звёздочка** будет выделена текущая ветка

### Переключение между вектами
Для перехода на другую ветку используется команда *git checkout*. Для этого в терминале с папкой-репозиторием пишем команду *git checkout <название ветки*. Для перехода на ветку ветка должна быть ***создана***!!!

## Слияние веток и разрешение конфликтов
### Слияние веток
Для слияния веток используется команда git merge. Для этого сначала необходимо перейти в ветку master с помощью команды git checkout master. После этого в терминале с папкой-репозиторием написать команду git merge <название ветки, которую сливаем с master>.

### Разрешение конфликтов
При возникновении конфликтов появится сообщение о конфликте в терминале, а в поле с текстом будут выделены версии из ветки master и сливаемой ветки разными цветами. Объединение возможно путем принятия ожного из варинтов, предлагаемого системой автоматически, так и вручную, удалив служебные выделения и обозначения. После разрешения конфликтов и создания финальной версии в master необходимо сохранить изменения и далее применить команды git add <Название файла> и git commit -m <Сообщение к коммиту>.

## Удаление веток
Для удаление веток используется команда git branch -d <Название удаляемой ветки>. Для этого в терминале папки-репозитория необходимо ввести вышеуказанную команду.
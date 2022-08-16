# Инструкция по работе с  Git

## Что такое Git?
Git - одна из реализаций распределённых систем контроля версий, позволяющая организовать версионность, как локально, так и на удалённом сервере. Самая популярная плотформа, реализующая Git, - [GitHub](https://github.com)
## Подготовка репозитория 
Для создания в папке репозитория необхлдимо открыть эту папку в терменале и написать команду * git init*, после чего в этой папке создаётся скрытая папка *.git*, и таким образом папка станет репозиторием
## Создание коммитов

### Просмотр состояний репозитория
Для просмотра состояния репозитория  используется команда *git status*. В терминале с открытой папкой-репозиторием необходимо написать команду *git  status*. В результате можно увидить следующие выводы:
1. On branch *** nothing to commit - это  означает нет октивных изменений
2. Untracked file - это означает, что имеются файлы, не отслеживаемые системой контроля версий
...

### создание фиксации
Для создания фиксации используется команда *git commit*. Для этого в терминале с папкой-репозиториев необходимо написать команду *git commit -m<сообщение к коммиту>*. Сообщение к коммиту писать ОБЯЗАТЕЛЬНО.

## Журнал изменений
Для проосмотра истории изменений используется команда git log.Для этого в терменале с папкой-репозиторием необходимо написать git log, и Вы увидете список всех коммитов в этой ветке с описанием: имени, электронной почты, сообщением к коммиту и номер коммита.
## Перемещение между коммитами
Для перемещения между коммитами используется команда *git Checkout*. Для этого в терминале с папкой-репозиторием необбходимо написать *git checkout <номер коммита>*. Номер коммита бертся из журнала изменений ветки.
## Ветки в Git
### Создание ветки
Для того, чтобы создать ветку используется команда git Branch. Для этого в терминале с папкой-репозиторием необходимо написать git branch <название ветки> и таким образом создаётся новая ветка, но вы останетесь в исходной.

### Переключение между ветками
Для того, чтобы переключиться на другую ветку, используется команда git checkout. Для этого в терминале с папкой-репозиторием необходимо написать git checkout < название ветки>, и тогда Вы перейдёте в указанную ветку. Для переключения между ветками, ветка должна СУЩЕСТВОВАТЬ, и в текущий ветке НЕ ДОЛЖНО быть активных изменений.
## Слияние веток и решение конфликтов

### Слияние веток
Процедура объединения веток называется слияние (merge). Для слияния текущей ветки с какой-либо другой используется команда git merge имя_ветки. В результате выполнения этой команды в текущей ветке появится новый коммит. Этот коммит будет иметь два предка – последние коммиты обоих веток, участвующих в слиянии. Содержимое этого коммита будет включать содержимое коммитов обоих веток

## Удаление веток
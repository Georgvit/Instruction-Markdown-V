# Что такое GIT

**Git** (произносится «гит»[7]) — распределённая система управления версиями. Проект был создан Линусом Торвальдсом для управления разработкой ядра Linux, первая версия выпущена 7 апреля 2005 года. На сегодняшний день его поддерживает Джунио Хамано.

## Подготовка репозитория

Обычно вы получаете репозиторий Git одним из двух способов:

Вы можете взять локальный каталог, который в настоящее время не находится под версионным контролем, и превратить его в репозиторий Git, либо

Вы можете клонировать существующий репозиторий Git из любого места.

В обоих случаях вы получите готовый к работе Git репозиторий на вашем компьютере.

## Создание сохранений

Команда *git add* добавляет изменение из рабочего каталога в раздел проиндексированных файлов. Она сообщает Git, что вы хотите включить изменения в конкретном файле в следующий коммит. Однако на самом деле команда git add не оказывает существенного влияния на репозиторий: изменения регистрируются в нем только после выполнения команды *git commit*.

## Переключение между сохранениями

сли у вас уже есть ветка feature, то после коммита в нее сделайте *git checkout master* – это переключит текущую ветку на master.

Пока вы не вкоммитили изменения, вы не можете переключиться на другую ветку. 

Выхода два: вкоммитить изменения или отложить их. Второе можно сделать с помощью 

*git stash* – это добавит текущие незакоммиченные изменения в стек изменений и сбросит текущую рабочую копию до HEAD'а репозитория. 

Далее вы сможете:

*git stash list*: показать все изменения в стеке

*git stash show*: показать последнее изменение в стеке (патч)

*git stash apply*: применить последнее изменение из стека к текущей рабочей копии

*git stash drop*: удалить последнее изменение в стеке

*git stash pop*: применить последнее изменение из стека к текущей рабочей копии и удалить его из стека

*git stash clear*: очистить стек изменений

## Журнал изменений

Журнал изменений — это файл, который содержит общий, хронологически упорядоченный список изменений, внесенных в проект. Он часто организован по версии с указанием даты, после чего следует список добавленных, переработанных и удаленных функций.

В общем смысле, существует два способа делать записи в журнал изменений.

* Обычный способ: создайте текстовый файл и начните перечислять все внесенные вами изменения с указанием определенной даты.
* Выбор разработчика (он же вариант для ленивых): автоматическое создание списка изменений из ваших сообщений к коммитам. У меня для вас хорошие новости — именно об этом вы узнаете из этой статьи!


«Журнал изменений представляет собой программное протоколирование изменений, вносимых в большой проект. Таким проектом может быть веб-сайт или проект программного обеспечения. Обычно записи журнала изменений содержат информацию об исправлении ошибок, о новых возможностях и т.д»

## Ветки в GIT

Почти каждая система контроля версий (СКВ) в какой-то форме поддерживает ветвление. Используя ветвление, Вы отклоняетесь от основной линии разработки и продолжаете работу независимо от неё, не вмешиваясь в основную линию. Во многих СКВ создание веток — это очень затратный процесс, часто требующий создания новой копии каталога с исходным кодом, что может занять много времени для большого проекта.
 
## Слияние веток 

Это перенос кода из одной ветки в другую с помощью команды *git merge*. Например, когда мы заканчиваем работу над веткой, например, сделали новый функционал или поправили багу, мы сливаем ее в мастер. В мастере код проверяется еще раз и выкладывается на боевой сервер.

Сливать друг в друга можно любые ветки. Технически, с точки зрения git нет никакой разницы, сливается ветка с новым функционалом в мастер или наоборот. Для нас мастер - это основная ветка разработки, а для git это просто ветка.

## Удаление веток

Чтобы удалить ветку из локального Git-репозитория, выполните: git branch -d <имя_ветки> Удалить Удаленную Ветку. Чтобы удалить ветку из удаленного Git-репозитория, выполните: git push origin --delete <имя_ветки>. Для просмотра изменений одного файла, можно воспользоваться следующей командой: Изменения по коммитам git log -p FILE_NAME. Изменения до коммита git diff FILE_NAME Hard Reset. Самый жесткий вариант.

## Удаление веток 2

Чтобы удалить ветку из локального Git-репозитория, выполните: git branch -d <имя_ветки> Удалить Удаленную Ветку. Чтобы удалить ветку из удаленного Git-репозиториb, выполните: git push origin --delete <имя_ветки>. Для просмотра изменений одного файла, можно воспользоваться следующей командой: Изменения по коммитам git log -p FILE_NAME. Изменения до коммита git diff FILE_NAME Hard Reset. *Самый жесткий вариант*.



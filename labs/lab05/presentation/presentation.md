---
## Front matter
lang: ru-RU
title: Лабораторная работа №5
subtitle: "Анализ файловой системы Linux.
Команды для работы с файлами и каталогами"
author:
  - Барабанова Кристина, НКАбд-01-22

## i18n babel
babel-lang: russian
babel-otherlangs: english

## Formatting pdf
toc: false
toc-title: Содержание
slide_level: 2
aspectratio: 169
section-titles: true
theme: metropolis
header-includes:
 - \metroset{progressbar=frametitle,sectionpage=progressbar,numbering=fraction}
 - '\makeatletter'
 - '\beamer@ignorenonframefalse'
 - '\makeatother'
---

## Докладчик

:::::::::::::: {.columns align=center}
::: {.column width="70%"}

  * Барабанова Кристина, НКАбд-01-22

:::
::: {.column width="30%"}


:::
::::::::::::::
# Цель работы

Ознакомление с файловой системой Linux, её структурой, именами и содержанием
каталогов. Приобретение практических навыков по применению команд для работы
с файлами и каталогами, по управлению процессами (и работами), по проверке исполь-
зования диска и обслуживанию файловой системы.


# Задание

1. Выполните все примеры, приведённые в первой части описания лабораторной работы.
2. Выполните следующие действия, зафиксировав в отчёте по лабораторной работе
используемые при этом команды и результаты их выполнения:
2.1. Скопируйте файл /usr/include/sys/io.h в домашний каталог и назовите его
equipment. Если файла io.h нет, то используйте любой другой файл в каталоге
/usr/include/sys/ вместо него.
2.2. В домашнем каталоге создайте директорию ~/ski.plases.
2.3. Переместите файл equipment в каталог ~/ski.plases.
2.4. Переименуйте файл ~/ski.plases/equipment в ~/ski.plases/equiplist.
2.5. Создайте в домашнем каталоге файл abc1 и скопируйте его в каталог
~/ski.plases, назовите его equiplist2.
2.6. Создайте каталог с именем equipment в каталоге ~/ski.plases.
2.7. Переместите файлы ~/ski.plases/equiplist и equiplist2 в каталог
~/ski.plases/equipment.
2.8. Создайте и переместите каталог ~/newdir в каталог ~/ski.plases и назовите
его plans.


# Задания

3. Определите опции команды chmod, необходимые для того, чтобы присвоить перечис-
ленным ниже файлам выделенные права доступа, считая, что в начале таких прав
нет:
3.1. drwxr--r-- ... australia
3.2. drwx--x--x ... play
3.3. -r-xr--r-- ... my_os
3.4. -rw-rw-r-- ... feathers
При необходимости создайте нужные файлы.
4. Проделайте приведённые ниже упражнения, записывая в отчёт по лабораторной
работе используемые при этом команды:
4.1. Просмотрите содержимое файла /etc/password.
4.2. Скопируйте файл ~/feathers в файл ~/file.old.
4.3. Переместите файл ~/file.old в каталог ~/play.
4.4. Скопируйте каталог ~/play в каталог ~/fun.
4.5. Переместите каталог ~/fun в каталог ~/play и назовите его games.
4.6. Лишите владельца файла ~/feathers права на чтение.
4.7. Что произойдёт, если вы попытаетесь просмотреть файл ~/feathers командой
cat?
4.8. Что произойдёт, если вы попытаетесь скопировать файл ~/feathers?
4.9. Дайте владельцу файла ~/feathers право на чтение.
4.10. Лишите владельца каталога ~/play права на выполнение.
4.11. Перейдите в каталог ~/play. Что произошло?
4.12. Дайте владельцу каталога ~/play право на выполнение.
5. Прочитайте man по командам mount, fsck, mkfs, kill и кратко их охарактеризуйте,
приведя примеры


# Выполнение лабораторной работы

## Задание 1

Выполнила все примеры, приведённые в первой части описания лабораторной работы. (рис. @fig:001-005).

![ВЫполнение примеров](1.jpg){#fig:001 width=70%}

![ВЫполнение примеров](2.jpg){#fig:002 width=70%}

## Задание 2

Выполнила следующие действия:

Скопировала файл /usr/include/sys/io.h в домашний каталог и назовите его
equipment. (рис. @fig:006)

![Копирование файла и изменение его имени](6.jpg){#fig:006 width=70%}

В домашнем каталоге создала директорию ~/ski.plases. (рис. @fig:007)

![Создание директории](7.jpg){#fig:007 width=70%}

## Задание 2

Переместила файл equipment в каталог ~/ski.plases. (рис. @fig:008)

![Перемещение файла](8.jpg){#fig:008 width=70%}

Переименовала файл ~/ski.plases/equipment в ~/ski.plases/equiplist. (рис. @fig:009)

![Переименование файла](9.jpg){#fig:009 width=70%}

## Задание 2

Создала в домашнем каталоге файл abc1 и скопировала его в каталог
~/ski.plases, назовите его equiplist2. (рис. @fig:010)

![Создание, копирование и переименование файла](10.jpg){#fig:010 width=70%}

Создала каталог с именем equipment в каталоге ~/ski.plases. (рис. @fig:011)

![Создание каталога](11.jpg){#fig:011 width=70%}

## Задание 2

Переместила файлы ~/ski.plases/equiplist и equiplist2 в каталог
~/ski.plases/equipment. (рис. @fig:012)

![Перемещение файлов в каталог](12.jpg){#fig:012 width=70%}

Создала и переместила каталог ~/newdir в каталог ~/ski.plases и назвала
его plans. (рис. @fig:013)

![создание и премещение одного каталога в другой](13.jpg){#fig:013 width=70%}


## Задание 3

Определила опции команды chmod, необходимые для того, чтобы присвоить перечис-
ленным ниже файлам выделенные права доступа, считая, что в начале таких прав
нет:
3.1. drwxr--r-- ... australia
3.2. drwx--x--x ... play
3.3. -r-xr--r-- ... my_os
3.4. -rw-rw-r-- ... feathers (рис. @fig:014-019)

![Создание необходимых файлов и каталогов](14.jpg){#fig:014 width=70%}

![Определение опций команды chmod](15.jpg){#fig:015 width=70%}

![Определение опций команды chmod](16.jpg){#fig:016 width=70%}
 
## Задание 4

Проделайте приведённые ниже упражнения. 

Просмотрела содержимое файла /etc/password. (рис. @fig:020)

![просмотр содержимого файла](20.jpg){#fig:020 width=70%}

Скопировала файл ~/feathers в файл ~/file.old (рис. @fig:021)

![копирование одного файла в другой](21.jpg){#fig:021 width=70%}

## Задание 4

Переместила файл ~/file.old в каталог ~/play. (рис. @fig:022)

![перемещение файла в каталог](22.jpg){#fig:022 width=70%}

Скопировала каталог ~/play в каталог ~/fun. (рис. @fig:022)

![копирование одного каталога в другой](22.jpg){#fig:022 width=70%}

Переместила каталог ~/fun в каталог ~/play и назвала его games. (рис. @fig:023)

![перемещение и переименование каталога](23.jpg){#fig:023 width=70%}


## Задание 4

Лишила владельца файла ~/feathers права на чтение. (рис. @fig:024)

![лишение владельца файла права на чтение](24.jpg){#fig:024 width=70%}

Посмотрела, что произойдёт, если я попытаюсь просмотреть файл ~/feathers командой
cat. (рис. @fig:025)

![что произойдет при попытке посмотреть файл](25.jpg){#fig:025 width=70%}

Посмотрела, что произойдёт, если я попытаюсь скопировать файл ~/feathers. (рис. @fig:026)

![что произойдет при попытке скопировать файл](26.jpg){#fig:026 width=70%}


## Задание 5

Прочитала man по командам mount, fsck, mkfs, kill. (рис. @fig:031)

![команда man](31.jpg){#fig:031 width=70%}




# Выводы

Ознакомилась с файловой системой Linux, её структурой, именами и содержанием
каталогов. Приобрела практические навыки по применению команд для работы
с файлами и каталогами, по управлению процессами (и работами), по проверке исполь-
зования диска и обслуживанию файловой системы.



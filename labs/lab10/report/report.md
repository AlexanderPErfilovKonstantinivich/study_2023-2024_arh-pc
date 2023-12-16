---
## Front matter
title: "Лабораторная работа №10"
subtitle: "Работа с файлами средствами Nasm"
author: "Перфилов Александр Константинович | группа: НПИбд 02-23"

## Generic otions
lang: ru-RU
toc-title: "Содержание"

## Bibliography
bibliography: bib/cite.bib
csl: pandoc/csl/gost-r-7-0-5-2008-numeric.csl

## Pdf output format
toc: true # Table of contents
toc-depth: 2
lof: true # List of figures
lot: true # List of tables
fontsize: 12pt
linestretch: 1.5
papersize: a4
documentclass: scrreprt
## I18n polyglossia
polyglossia-lang:
  name: russian
  options:
	- spelling=modern
	- babelshorthands=true
polyglossia-otherlangs:
  name: english
## I18n babel
babel-lang: russian
babel-otherlangs: english
## Fonts
mainfont: PT Serif
romanfont: PT Serif
sansfont: PT Sans
monofont: PT Mono
mainfontoptions: Ligatures=TeX
romanfontoptions: Ligatures=TeX
sansfontoptions: Ligatures=TeX,Scale=MatchLowercase
monofontoptions: Scale=MatchLowercase,Scale=0.9
## Biblatex
biblatex: true
biblio-style: "gost-numeric"
biblatexoptions:
  - parentracker=true
  - backend=biber
  - hyperref=auto
  - language=auto
  - autolang=other*
  - citestyle=gost-numeric
## Pandoc-crossref LaTeX customization
figureTitle: "Рис."
tableTitle: "Таблица"
listingTitle: "Листинг"
lofTitle: "Список иллюстраций"
lotTitle: "Список таблиц"
lolTitle: "Листинги"
## Misc options
indent: true
header-includes:
  - \usepackage{indentfirst}
  - \usepackage{float} # keep figures where there are in the text
  - \floatplacement{figure}{H} # keep figures where there are in the text
---

# Цель работы

Приобретение навыков написания программ для работы с файлами.

# Выполнение лабораторной работы


Создадим каталог для программ лабораторной работы № 10, перейдем в него и создадим файл lab10-1.asm, readme-1.txt и readme-2.txt:

![Рис 2.1.1: Создание каталога, файла .asm и файлов .txt](image/Рис 2.1.1.png)

Введем в файл lab10-1.asm текст программы из листинга 10.1 (Программа записи в файл сообщения)

![Рис 2.1.2: Программа](image/Рис 2.1.2.png)

Создадим исполняемый файл и проверим его.

![Рис 2.1.3: Создание файла и проверка](image/Рис 2.1.3.png)

С помощью команды chmod изменим права доступа к исполняемому файлу lab10-1, запретив его выполнение. Попытаемся выполнить файл.

![Рис 2.1.4: Изменение прав доступа к исп. файлу и проверка](image/Рис 2.1.4.png)

Командой chomod u-x lab10-1 мы запрещаем его выполнение для владельца. Поэтому мы не можем выполнить файл

С помощью команды chmod изменим права доступа к файлу lab10-1.asm с исходным текстом программы, добавив права на исполнение. Попытайтаемся выполнить его.

![Рис 2.1.5: Изменение прав доступа и проверка](image/Рис 2.1.5.png)

Когда мы пытаемся исполнить этот файл исполнение начинается, но не исполняется, так как не содержит в себе команд для терминала

В соответствии с вариантом 19 в таблице 10.4 предоставим права доступа к файлу readme-1.txt представленные в символьном виде, а для файла readme-2.txt – в двочном виде. Проверим правильность выполнения с помощью команды ls -l

![Рис 2.1.6: Предоставление прав доступа для .txt и проверка](image/Рис 2.1.5.png)

Права доступа были предоставлены правильно.


# Самостоятельная работа

Задание 1 Напишите программу работающую по следующему алгоритму:
• Вывод приглашения “Как Вас зовут?”
• ввести с клавиатуры свои фамилию и имя
• создать файл с именем name.txt
• записать в файл сообщение “Меня зовут”
• дописать в файл строку введенную с клавиатуры
• закрыть файлм
Создать исполняемый файл и проверить его работу. Проверить наличие файла и его
содержимое с помощью команд ls и cat.


Для того чтобы не начинать с нуля, мы возьмем файл lab10-1.asm, скопируем его, переименуем в "task" и напишем программу под условие задания, а также создадим файл name.txt для программы

![Рис 3.1.1: Создание нужных файлов](image/Рис 3.1.1.png)

![Рис 3.1.2: Программа для задания](image/Рис 3.1.2.png)

Создадим испол. файл, запустим, проверим наличией файла и его содержиое

![Рис 3.1.3: Проверка программы](image/Рис 3.1.3.png)

Программа работает правильно.


# Выводы

Я приобрел навыки написания программ для работы с файлами


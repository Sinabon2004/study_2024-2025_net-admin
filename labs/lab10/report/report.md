---
## Front matter
title: "Отчёт по лабораторной работе №10"
subtitle: "НПИбд-02-22"
author: "Чесноков Артемий Павлович"

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
mainfont: IBM Plex Serif
romanfont: IBM Plex Serif
sansfont: IBM Plex Sans
monofont: IBM Plex Mono
mathfont: STIX Two Math
mainfontoptions: Ligatures=Common,Ligatures=TeX,Scale=0.94
romanfontoptions: Ligatures=Common,Ligatures=TeX,Scale=0.94
sansfontoptions: Ligatures=Common,Ligatures=TeX,Scale=MatchLowercase,Scale=0.94
monofontoptions: Scale=MatchLowercase,Scale=0.94,FakeStretch=0.9
mathfontoptions:
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

Освоить настройку прав доступа пользователей к ресурсам сети.


# Выполнение лабораторной работы

Подключаем laptop (рис. [-@fig:001]).

![прямым| 24 порт](image/1.png){#fig:001 width=70%}

Выдаем статический адрес (рис. [-@fig:002]).

![10.128.6.200](image/2.png){#fig:002 width=70%}

Даем gateaway и dns адреса (рис. [-@fig:003]).

![выдали](image/3.png){#fig:003 width=70%}

Разрешаем обращаться к web (рис. [-@fig:004]).

![пока что только по ip](image/4.png){#fig:004 width=70%}

Пример захода на адрес по ip через устройство(рис. [-@fig:005]).

![по домену пока что не можем](image/5.png){#fig:005 width=70%}

Разрешаем админу ftp и telnet (рис. [-@fig:006]).

![только админу](image/6.png){#fig:006 width=70%}

Пробуем от админа (рис. [-@fig:007]).

![успешно](image/7.png){#fig:007 width=70%}

Пробуем от любого другого пользователя (рис. [-@fig:008]).

![ловим таймаут](image/8.png){#fig:008 width=70%}

Делаем доступ на файловый сервер (рис. [-@fig:009]).

![выдали](image/9.png){#fig:009 width=70%}

Настраиваем доступы для mail и dns (рис. [-@fig:010]).

![сделали](image/10.png){#fig:010 width=70%}

Заходим по домену с любого устройства (рис. [-@fig:011]) (рис. [-@fig:012]).

![ура](image/11.png){#fig:011 width=70%}

Всегда пропускаем icmp через маршрутизатор, всегда разрешаем, откуда угодно и куда угодно

![Ставим в первый порядок](image/12.png){#fig:012 width=70%}

Даем админу доступ к сетевому оборудованию (рис. [-@fig:013]).

![выдали](image/13.png){#fig:013 width=70%}



# Выводы

Освоили настройку прав доступа пользователей к ресурсам сети.

# Список литературы{.unnumbered}

::: {#refs}
:::

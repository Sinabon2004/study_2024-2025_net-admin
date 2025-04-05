---
## Front matter
title: "Отчёт по лабораторной работе №2"
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

Получить основные навыки по начальному конфигурированию оборудования
Cisco.


# Выполнение лабораторной работы

Строим схему с маршрутизатором (рис. [-@fig:001]).

![витая пара + консоль](image/1.png){#fig:001 width=70%}

Конфигурируем маршрутизатор (рис. [-@fig:002]).

![базовая конфигурация](image/2.png){#fig:002 width=70%}

Продолжение (рис. [-@fig:003]).

![](image/3.png){#fig:003 width=70%}

Строим схему с коммутатором (рис. [-@fig:004]).

![прамой кабель + консоль](image/4.png){#fig:004 width=70%}

конфигурируем коммутатор (рис. [-@fig:005]).

![по лабе](image/5.png){#fig:005 width=70%}

Не забываем задать статические адреса (рис. [-@fig:006]).

![1 комп](image/6.png){#fig:006 width=70%}

Второе устройство (рис. [-@fig:007]).

![2 комп](image/7.png){#fig:007 width=70%}

В PC-1 открываем командную консоль  (рис. [-@fig:008]).

![открыли](image/8.png){#fig:008 width=70%}

Пингуем (рис. [-@fig:009]).

![успешно](image/9.png){#fig:009 width=70%}

Подключаемся по ssh  (рис. [-@fig:010]).

![подключились](image/10.png){#fig:010 width=70%}

Аналогично стучимся к коммутатору (рис. [-@fig:011]).

![успешно](image/11.png){#fig:011 width=70%}




# Выводы

Получили основные навыки по начальному конфигурированию оборудования
Cisco

# Список литературы{.unnumbered}

::: {#refs}
:::

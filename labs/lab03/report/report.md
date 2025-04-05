---
## Front matter
title: "Отчёт по лабораторной работе №3"
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

Познакомится с принципами планирования локальной сети организации.


# Выполнение лабораторной работы

Повторяем схему первого слоя в нашей системе (рис. [-@fig:001]).

![Физические устройства сети с номерами портов Layer 1](image/1.png){#fig:001 width=70%}

Повторяем схему распределения VLAN (рис. [-@fig:002]).

![Схема VLAN сети Layer 2 ](image/2.png){#fig:002 width=70%}

Повторяем схему маршрутизации (рис. [-@fig:003]).

![Схема маршрутизации сети Layer 3](image/3.png){#fig:003 width=70%}

Повторяем таблицу VLAN'ов, ознакамливаемся (рис. [-@fig:004]).

![перенесли к себе](image/4.png){#fig:004 width=70%}

Повторяем таблицу IP адресов, ознакамливаемся (рис. [-@fig:005]).

![перенесли к себе](image/5.png){#fig:005 width=70%}

Повторяем таблицу портов, ознакамливаемся (рис. [-@fig:006]).

![перенесли к себе](image/6.png){#fig:006 width=70%}

Делаем схему маршрутизации для 176.16.0.0/12 (рис. [-@fig:007]).

![остальные схемы сходятся](image/7.png){#fig:007 width=70%}

Делаем схему маршрутизации для 192.168.0.0/16 (рис. [-@fig:008]).

![остальные схемы сходятся](image/8.png){#fig:008 width=70%}

Таблицы для IP адресов для 176.16.0.0/12  (рис. [-@fig:009]).

![остальные таблицы сходятся](image/9.png){#fig:009 width=70%}

Таблицы для IP адресов для 192.168.0.0/16  (рис. [-@fig:010]).

![остальные таблицы сходятся](image/10.png){#fig:010 width=70%}





# Выводы

Получили основные навыки по начальному конфигурированию оборудования
Cisco

# Список литературы{.unnumbered}

::: {#refs}
:::

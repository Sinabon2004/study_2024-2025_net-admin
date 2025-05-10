---
## Front matter
title: "Отчёт по лабораторной работе №13"
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

Провести подготовительные мероприятия по организации взаимодействия
через сеть провайдера посредством статической маршрутизации локальной
сети с сетью основного здания, расположенного в 42-м квартале в Москве,
и сетью филиала, расположенного в г. Сочи.


# Выполнение лабораторной работы

Выделяем области для новых частей сети (рис. [-@fig:001]).

![ квартал 42, сочи-филиал ](image/1.png){#fig:001 width=70%}

Размещаем все необходимые устройства (рис. [-@fig:002]).

![на территории новых областей ](image/2.png){#fig:002 width=70%}

Называем наши устройства в соответствии с соглашением об именовании (рис. [-@fig:003]).

![назвали](image/3.png){#fig:003 width=70%}

Добавляем дополнительный интерфейс
NM-2FE2W (рис. [-@fig:004]) .

![на msk-q42-gw-1](image/4.png){#fig:004 width=70%}

Заменим модули на повторителях (рис. [-@fig:005]).

![пример для msk-q42-mc-1](image/5.png){#fig:005 width=70%}

 Добавляем в физическую область здание 42 квартала (рис. [-@fig:006]) 

![называем его q42](image/6.png){#fig:006 width=70%}

Создаем город Sochi(рис. [-@fig:007]) 

![называем его sochi](image/7.png){#fig:007 width=70%}

Создаем здание филиала(рис. [-@fig:008]).

![называем его sch](image/8.png){#fig:008 width=70%}

Пример того как должна выглядеть физическая область для простраснства q42(рис. [-@fig:009]).

![заблаговременно перетаскиваем нужные устройства с Донской](image/9.png){#fig:009 width=70%}

Пример того как должна выглядеть физическая область для простраснства sochi(рис. [-@fig:010]).

![заблаговременно перетаскиваем нужные устройства с Донской](image/10.png){#fig:010 width=70%}

Соединяем все устройства(рис. [-@fig:011]).

![пример того как этого может выглядеть](image/11.png){#fig:011 width=70%}

Первоначальная настройка для маршрутизатора q42(рис. [-@fig:012]) (рис. [-@fig:013]).

![Добавление доступов](image/12.png){#fig:012 width=70%}

![Продолжение cli команд](image/13.png){#fig:013 width=70%}

Первоначальная настройка для коммутатора q42(рис. [-@fig:014]) (рис. [-@fig:015]).

![Добавление доступов](image/14.png){#fig:014 width=70%}

![Продолжение cli команд](image/15.png){#fig:015 width=70%}

Первоначальная настройка для маршутизатора hostel(рис. [-@fig:016]) (рис. [-@fig:017]).

![Добавление доступов](image/16.png){#fig:016 width=70%}

![Продолжение cli команд](image/17.png){#fig:017 width=70%}

Первоначальная настройка для коммутатора hostel(рис. [-@fig:018]) (рис. [-@fig:019]).

![Добавление доступов](image/18.png){#fig:018 width=70%}

![Продолжение cli команд](image/19.png){#fig:019 width=70%}

Первоначальная настройка для коммутатора sochi(рис. [-@fig:020]) (рис. [-@fig:021]).

![Добавление доступов](image/20.png){#fig:020 width=70%}

![Продолжение cli команд](image/21.png){#fig:021 width=70%}

Первоначальная настройка для маршрутизатора sochi(рис. [-@fig:022]) (рис. [-@fig:023]).

![Добавление доступов](image/22.png){#fig:022 width=70%}

![Продолжение cli команд](image/23.png){#fig:023 width=70%}

# Выводы

Провели подготовительные мероприятия по организации взаимодействия
через сеть провайдера посредством статической маршрутизации локальной
сети с сетью основного здания, расположенного в 42-м квартале в Москве,
и сетью филиала, расположенного в г. Сочи.


# Список литературы{.unnumbered}

::: {#refs}

:::

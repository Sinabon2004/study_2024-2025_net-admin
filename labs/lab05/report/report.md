---
## Front matter
title: "Отчёт по лабораторной работе №5"
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

Получить основные навыки по настройке VLAN на коммутаторах сети.


# Выполнение лабораторной работы

Настраиваем trunk порты (рис. [-@fig:001]).

![пример для первого маршрутизатора](image/1.png){#fig:001 width=70%}

Настраиваем маршрутизатор-сервер (рис. [-@fig:002]).

![первый донской](image/2.png){#fig:002 width=70%}

Показываем результат списком (рис. [-@fig:003]).

![Show vlan](image/3.png){#fig:003 width=70%}

Закрепляем остальные маршрутизаторы как клиенты (рис. [-@fig:004]).

![пример для второго маршрутизатора](image/4.png){#fig:004 width=70%}

Список для четвертого маршрутизатора (рис. [-@fig:005]).

![show vlan](image/5.png){#fig:005 width=70%}

Прописываем диапазоны (рис. [-@fig:006]).

![пример для четвертого маршрутизатора](image/6.png){#fig:006 width=70%}

Проставляем статические IP адреса на конечные устройства (рис. [-@fig:007]).

![пример для web сервера](image/7.png){#fig:007 width=70%}

Открываем командную строку на донском и пингуем павловскую (рис. [-@fig:008]).

![ipconfig;ping](image/8.png){#fig:008 width=70%}

Включаем симуляцию и отслеживаем ICMP протокол (рис. [-@fig:009]).

![ICMP](image/9.png){#fig:009 width=70%}

Отправляем  (рис. [-@fig:010]).

![от dk-donskaya-1](image/10.png){#fig:010 width=70%}

Получаем  (рис. [-@fig:011]).

![dk-pavlovskaya-1](image/11.png){#fig:011 width=70%}

Наблюдаем передоваемую информацию  (рис. [-@fig:012]).

![ура](image/12.png){#fig:012 width=70%}

# Выводы

Получили основные навыки по настройке VLAN на коммутаторах сети.

# Список литературы{.unnumbered}

::: {#refs}
:::

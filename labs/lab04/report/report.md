---
## Front matter
title: "Отчёт по лабораторной работе №4"
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

Провести подготовительную работу по первоначальной настройке коммутаторов сети.


# Выполнение лабораторной работы

Строим сеть (рис. [-@fig:001]).

![согласно схеме сети L1](image/1.png){#fig:001 width=70%}

Настраиваем все коммутаторы, изменяя название устройства в соответствии с соглашением об именовании (рис. [-@fig:002]).

![1 часть ](image/2.png){#fig:002 width=70%}

Продолжение конфигурации (рис. [-@fig:003]).

![2 часть](image/3.png){#fig:003 width=70%}

Продолжение конфигурации (рис. [-@fig:004]).

![3 часть](image/4.png){#fig:004 width=70%}

В целях экономии времени переписываем все команды на блокнот и для каждого коммутатора просто вставляем нужное имя и адрес (рис. [-@fig:005]).

![для каждого коммутатора в сети](image/5.png){#fig:005 width=70%}

Для третьего (рис. [-@fig:006]).

![вставляем содержимое блокнота](image/6.png){#fig:006 width=70%}

Для четвертого (рис. [-@fig:007]).

![вставляем содержимое блокнота](image/7.png){#fig:007 width=70%}

Для второго (рис. [-@fig:008]).

![вставляем содержимое блокнота](image/8.png){#fig:008 width=70%}



# Выводы

Провели подготовительную работу по первоначальной настройке коммутаторов сети.

# Список литературы{.unnumbered}

::: {#refs}
:::

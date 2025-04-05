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

Настроить статическую маршрутизацию VLAN в сети.


# Выполнение лабораторной работы

Добаляем в локальную сеть маршрутизатор(рис. [-@fig:001]).

![msk-donskaya-gw-1](image/1.png){#fig:001 width=70%}

Первоначальная конфигурация поставленного маршрутизатора (рис. [-@fig:002]).

![даем удаленный доступ](image/2.png){#fig:002 width=70%}

Настраиваем порт 24 коммутатора msk-donskaya-sw-1 как trunk-порт (рис. [-@fig:003]).

![trunk mode](image/3.png){#fig:003 width=70%}

Добавляем порты (рис. [-@fig:004]).

![в GUI](image/4.png){#fig:004 width=70%}

Настраиваем все виртуальные интерфейсы (рис. [-@fig:005]).

![настроили](image/5.png){#fig:005 width=70%}

Пингуем (рис. [-@fig:006]).

![видно что нужно время чтобы подняться](image/6.png){#fig:006 width=70%}

Симулируем запрос (рис. [-@fig:007]).

![видно что мы не заходим в маршрутизатор](image/7.png){#fig:007 width=70%}

# Выводы
Настроили статическую маршрутизацию VLAN в сети.
# Список литературы{.unnumbered}

::: {#refs}
:::

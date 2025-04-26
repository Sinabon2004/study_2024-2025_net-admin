---
## Front matter
title: "Отчёт по лабораторной работе №11"
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

Провести подготовительные мероприятия по подключению локальной сети
организации к Интернету.


# Выполнение лабораторной работы

Обновляем нашу L1 схему, которую мы создаем в 3ей лабораторной работе (рис. [-@fig:001]).

![добавили области провайдера и сети Интернет ](image/1.png){#fig:001 width=70%}

Непосредственно в packetTracer'е размещаем все устройства (рис. [-@fig:002]).

![так же, как и в L1 разделяем на две области](image/2.png){#fig:002 width=70%}

В physical view размещаем новые здания: Provider и Internet (рис. [-@fig:003]).

![разместили](image/3.png){#fig:003 width=70%}

Переносим в physical view все устройства на их здания(рис. [-@fig:004]) (рис. [-@fig:005]).

![пример для переноса маршрутизатора провайдера](image/4.png){#fig:004 width=70%}

![как должно выглядеть содержимое здания Internet](image/5.png){#fig:005 width=70%}

Заменяем модули на повторителях (рис. [-@fig:006]).

![пример для нового повторителя на донской](image/6.png){#fig:006 width=70%}

Итоговая схема сети (рис. [-@fig:007]).

![всё подключили](image/7.png){#fig:007 width=70%}

Настраиваем статические адреса на сервера (рис. [-@fig:008]).

![пример для esystem.rudn.ru](image/8.png){#fig:008 width=70%}

Добавляем адреса серверов в dns list (рис. [-@fig:009]).

![итоговый list](image/9.png){#fig:009 width=70%}


# Выводы

Провели подготовительные мероприятия по подключению локальной сети
организации к Интернету.


# Список литературы{.unnumbered}

::: {#refs}

:::

---
## Front matter
title: "Отчёт по лабораторной работе №8"
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

Приобретение практических навыков по настройке динамического распределения IP-адресов посредством протокола DHCP (Dynamic Host Configuration
Protocol) [5] в локальной сети.


# Выполнение лабораторной работы

Разместим и подключим сервер (рис. [-@fig:001]).

![прямым кабелем](image/1.png){#fig:001 width=70%}

Подключаем коммутатор и активируем порт (рис. [-@fig:002]).

![замечательно](image/2.png){#fig:002 width=70%}

 Присваиваем статический адрес (рис. [-@fig:003]).

![10.128.0.5](image/3.png){#fig:003 width=70%}

Настроим сервис DNS по нашим нуждам (рис. [-@fig:004]).

![добавляем домены](image/4.png){#fig:004 width=70%}

В целях экономии времени переписываем все команды на блокнот и вставляем в наш маршрутизатор(рис. [-@fig:005]).

![это полная конфигурация](image/5.png){#fig:005 width=70%}

Информация о пулах DHCP (рис. [-@fig:006]).

![ ](image/6.png){#fig:006 width=70%}

Информация об привязках выданных адресов: (рис. [-@fig:007]).

![ ](image/7.png){#fig:007 width=70%}

Меняем всем устройствам статическую адресацию на динамическую (рис. [-@fig:008]).

![вставляем содержимое блокнота](image/8.png){#fig:008 width=70%}

Наблюдаем за присвоением адреса ДК на донской (рис. [-@fig:009]).

![успешно присвоено](image/9.png){#fig:009 width=70%}

Наблюдаем за присвоением адреса ДК на павловской (рис. [-@fig:010]).

![успешно присвоено](image/10.png){#fig:010 width=70%}

Отправляем тестовые пакеты (рис. [-@fig:011]).

![успешно отправляется](image/11.png){#fig:011 width=70%}

В содержимом пакета наблюдаем конкретные значения адресов (рис. [-@fig:012]).

![ура](image/12.png){#fig:012 width=70%}



# Выводы

Провели подготовительную работу по первоначальной настройке коммутаторов сети.

# Список литературы{.unnumbered}

::: {#refs}
:::

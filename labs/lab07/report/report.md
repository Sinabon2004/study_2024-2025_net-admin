---
## Front matter
title: "Отчёт по лабораторной работе №7"
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

Получить навыки работы с физической рабочей областью Packet Tracer,
а также учесть физические параметры сети.


# Выполнение лабораторной работы

Даем название городу(рис. [-@fig:001]).

![Moscow](image/1.png){#fig:001 width=70%}

Добавляем здания (рис. [-@fig:002]).

![Donskaya + pavlovskaya](image/2.png){#fig:002 width=70%}

Перемещаем в физ.отображении коммутаторы и др. устройства (рис. [-@fig:003]).

![pavlovskaya](image/3.png){#fig:003 width=70%}

Проверяем работоспособность соединения(рис. [-@fig:004]).

![ping](image/4.png){#fig:004 width=70%}

Включаем влияение длины кабеля на нашу сеть(рис. [-@fig:005]).

![Enable Cable Length Effects](image/5.png){#fig:005 width=70%}

Физически размещаем здания на расстояние > 1000м  (рис. [-@fig:006]).

![physic view](image/6.png){#fig:006 width=70%}

Убираем витой кабель, ставим повторители (рис. [-@fig:007]).

![Repeater-PT](image/7.png){#fig:007 width=70%}

Заменяем модули (рис. [-@fig:008]).

![на PT-REPEATERNM-1FFE и PT-REPEATER-NM-1CFE](image/8.png){#fig:008 width=70%}

Переносим на павловскую её повторитель (рис. [-@fig:009]).

![msk-pavlovskaya-mc-1](image/9.png){#fig:009 width=70%}

Соединяем (рис. [-@fig:010]).

![повторители соединяем через fiber](image/10.png){#fig:010 width=70%}

Проверяем работоспособность соединения(рис. [-@fig:011]).

![видно что запрос проходит!!!](image/11.png){#fig:011 width=70%}

# Выводы
Получили навыки работы с физической рабочей областью Packet Tracer,
а также научились учитывать физические параметры сети.
# Список литературы{.unnumbered}

::: {#refs}
:::

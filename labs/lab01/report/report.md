--
## Front matter
title: "Лабораторная работа №5"
subtitle: "Конфигурирование VLAN"
author: "Хрусталев Влад Николаевич"

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
--

# Цель работы

Получить основные навыки по настройке VLAN на комуникаторах сети.

# Задание

1. На коммутаторах сети настроить Trunk-порты на соответствующих интерфейсах, связывающих коммутаторы между собой.

2. Коммутатор msk-donskaya-sw-1 настроить как VTP-сервер и прописать на
нём номера и названия VLAN.

3. Коммутаторы msk-donskaya-sw-2 — msk-donskaya-sw-4, msk-pavlovskaya-sw-1 настроить как VTP-клиенты, на интерфейсах указать
принадлежность к соответствующему VLAN.

4. На серверах прописать IP-адреса.

5. На оконечных устройствах указать соответствующий адрес шлюза и прописать статические IP-адреса из диапазона соответствующей сети, следуя регламенту выделения ip-адресов.

6. Проверить доступность устройств, принадлежащих одному VLAN, и недоступность устройств, принадлежащих разным VLAN.

7. При выполнении работы необходимо учитывать соглашение об именовании.[@netadmin]

# Выполнение лабораторной работы

Откроем проект созданный и прокофнигурированный на LAB04. Используя приведённую в файле лабораторной работы последовательность команд из примера по конфигурации Trunk-порта на интерфейсе g0/1 коммутатора msk-donskaya-sw-1 (msk-donskaya-vnkhrustalev-sw-1), настроем Trunk-порты на соответствующих интерфейсах всех коммутаторов (рис. [-@fig:001]). 

![Настройка Trunk-порта на msk-donskaya-vnkhrustalev-sw-1](image/1.png){#fig:001 width=70%}

![Настройка Trunk-порта на msk-donskaya-vnkhrustalev-sw-2](image/2.png){#fig:002 width=70%}

![Настройка Trunk-порта на msk-donskaya-vnkhrustalev-sw-3](image/3.png){#fig:003 width=70%}

![Настройка Trunk-порта на msk-donskaya-vnkhrustalev-sw-4](image/4.png){#fig:004 width=70%}

![Настройка Trunk-порта на msk-donskaya-vnkhrustalev-sw-1](image/5.png){#fig:005 width=70%}

![Настройка Trunk-порта на msk-pavlovskaya-vnkhrustalev-sw-1](image/6.png){#fig:006 width=70%}

Используя приведённую в лабораторной работе последовательность команд по конфигурации VTP, настроем коммутатор msk-donskaya-vnkhrustalev-sw-1(рис. [-@fig:007]) как VTP-сервер и пропишем на нём номера и названия VLAN. Настроем коммутаторы msk-donskaya-vnkhrustalev-sw-2(рис. [-@fig:008]) — msk-donskaya-vnkhrustalev-sw-4(рис. [-@fig:010]), msk-pavlovskaya-vnkhrustalev-sw-1(рис. [-@fig:011]) как VTP-клиенты.

Используя приведённую в лабораторной работе последовательность команд по конфигурации диапазонов портов и на интерфейсах
укажем принадлежность к VLAN.

Выполним эту конфигурацию в соответствии с таблицей:

:Таблица портов

| Устройство                       | Порт        | Примечание           | Access VLAN | Trunk VLAN               |
|----------------------------------|-------------|----------------------|-------------|--------------------------|
| msk-donskaya-vnkhrustalev-gw-1    | f0/1        | UpLink               |             |                          |
|                                  | f0/0        | msk-donskaya-sw-1    |             | 2, 3, 101, 102, 103, 104 |
| msk-donskaya-vnkhrustalev-sw-1    | f0/24       | msk-donskaya-gw-1    |             | 2, 3, 101, 102, 103, 104 |
|                                  | g0/1        | msk-donskaya-sw-2    |             | 2, 3                     |
|                                  | g0/2        | msk-donskaya-sw-4    |             | 2, 101, 102, 103, 104    |
|                                  | g0/1        | msk-pavlovskaya-sw-1 |             | 2, 101, 104              |
| msk-donskaya-vnkhrustalev-sw-2    | g0/1        | msk-donskaya-sw-1    |             | 2, 3                     |
|                                  | g0/2        | msk-donskaya-sw-3    |             | 2, 3                     |
|                                  | f0/1        | Web-server           | 3           |                          |
|                                  | f0/2        | File-server          | 3           |                          |
| msk-donskaya-vnkhrustalev-sw-3    | g0/1        | msk-donskaya-sw-2    |             | 2, 3                     |
|                                  | f0/1        | Mail-server          | 3           |                          |
|                                  | f0/2        | Dns-server           | 3           |                          |
| msk-donskaya-vnkhrustalev-sw-4    | g0/1        | msk-donskaya-sw-1    |             | 2, 101, 102, 103, 104    |
|                                  | f0/1–f0/5   | dk                   | 101         |                          |
|                                  | f0/6–f0/10  | departments          | 102         |                          |
|                                  | f0/11–f0/15 | adm                  | 103         |                          |
|                                  | f0/16–f0/24 | other                | 104         |                          |
| msk-pavlovskaya-vnkhrustalev-sw-1 | f0/24       | msk-donskaya-sw-1    |             | 2, 101, 104              |
|                                  | f0/1–f0/15  | dk                   | 101         |                          |
|                                  | f0/20       | other                | 104         |                          | 


![Настройка коммутатора msk-donskaya-vnkhrustalev-sw-1 как VTP-сервер, добавление номеров и названий VLAN](image/7.png){#fig:007 width=70%}

![Настройка коммутатора msk-donskaya-vnkhrustalev-sw-2 как VTP-клиент и указание принадлежности к VLAN](image/8.png){#fig:008 width=70%}

![Настройка коммутатора msk-donskaya-vnkhrustalev-sw-3 как VTP-клиент и указание принадлежности к VLAN](image/9.png){#fig:009 width=70%}

![Настройка коммутатора msk-donskaya-vnkhrustalev-sw-4 как VTP-клиент и указание принадлежности к VLAN](image/10.png){#fig:010 width=70%}

![Настройка коммутатора msk-pavlovskaya-vnkhrustalev-sw-1 как VTP-клиент и указание принадлежности к VLAN](image/11.png){#fig:011 width=70%}

Затем требуется указать статические IP-адреса на оконечных устройствах

Задавать IP-адреса будем в соответствии с таблицей:

:Таблица IP. Сеть 10.128.0.0/16

| IP-адреса               | Примечание                 | VLAN |
|-------------------------|----------------------------|------|
| 10.128.0.0/16           | Вся сеть                   |      |
| 10.128.0.0/24           | Серверная ферма            | 3    |
| 10.128.0.1              | Шлюз                       |      |
| 10.128.0.2              | Web                        |      |
| 10.128.0.3              | File                       |      |
| 10.128.0.4              | Mail                       |      |
| 10.128.0.5              | Dns                        |      |
| 10.128.0.6-10.128.0.254 | Зарезервировано            |      |
| 10.128.1.0/24           | Управление                 | 2    |
| 10.128.1.1              | Шлюз                       |      |
| 10.128.1.2              | msk-donskaya-sw-1          |      |
| 10.128.1.3              | msk-donskaya-sw-2          |      |
| 10.128.1.4              | msk-donskaya-sw-3          |      |
| 10.128.1.5              | Msk-donskaya-sw-4          |      |
| 10.128.1.6              | msk-pavlovskaya-sw-1       |      |
| 10.128.1.7-10.128.1.254 | Зарезервировано            |      |
| 10.128.2.0/24           | Сеть Point-to-Point        |      |
| 10.128.2.1              | Шлюз                       |      |
| 10.128.2.2-10.128.2.254 | Зарезервировано            |      |
| 10.128.3.0/24           | Дисплейные классы(DK)      | 101  |
| 10.128.3.1              | Шлюз                       |      |
| 10.128.3.2-10.128.3.254 | Пул для пользователей      |      |
| 10.128.4.0/24           | Кафедра (DEP)              | 102  |
| 10.128.4.1              | Шлюз                       |      |
| 10.128.4.2-10.128.4.254 | Пул для пользователей      |      |
| 10.128.5.0/24           | Администрация (ADM)        | 103  |
| 10.128.5.1              | Шлюз                       |      |
| 10.128.5.2-10.128.5.254 | Пул для пользователей      |      |
| 10.128.6.0/24           | Другие пользователи(OTHER) | 104  |
| 10.128.6.1              | Шлюз                       |      |
| 10.128.6.2-10.128.6.254 | Пул для пользователей      |      |

Задаем IP-адрес шлюза(рис. [-@fig:012]) и самого сервера web(рис. [-@fig:013]):

![Задание IP-адреса шлюза](image/12.png){#fig:012 width=70%}

![Задание IP-адреса](image/13.png){#fig:013 width=70%}

По аналогии и с помощью таблицы IP-адресов задаем IP-адреса всем оконечным устройствам.

Далее выполним проверку нашей настройке устройств и пропингуем msk-pavlovskaya-vnkhrustalev-sw-1 c msk-donskaya-vnkhrustalev-sw-1 (рис. [-@fig:014])

![Проверка доступности устройств, принадлежащих одному VLAN, и недоступность устройств, принадлежащих разным VLAN.](image/14.png){#fig:014 width=70%}

Используя режим симуляции в Packet Tracer, изучим процесс передвижения пакета ICMP по сети. Изучим содержимое передаваемого пакета и заголовки задействованных протоколов.

Передача пакета между устройствами из одной сети проходит успешно. (рис. [-@fig:015])

![Режим симуляции(успешно)](image/15.png){#fig:015 width=70%}

Можем посмотреть информацию о пакете, его заголовки. Кадр физического уровня Ethernet, где указаны mac-адреса, кадр сетевого уровня IP, где указаны IP-адреса и ICMP кадр.(рис. [-@fig:016])

![Информация о PDU](image/16.png){#fig:016 width=70%}

При передачи пакетов между устройствами из разных сетей происходит сбой:(рис. [-@fig:017])

![Режим симуляции(неудачно)](image/17.png){#fig:017 width=70%}


## Ответы на котрольные вопросы

1. Какая команда используется для просмотра списка VLAN на сетевом устройстве?**  
```
show vlan brief
```
- Эта команда выводит список VLAN на коммутаторе, включая их идентификаторы (ID), названия и назначенные порты.  

```
show vlan
```
- Выводит более детальную информацию о VLAN, включая состояние и дополнительные параметры.  

```
show vtp status
```
- Отображает информацию о VLAN Trunking Protocol (VTP), включая режим работы и количество VLAN в базе.  

2. Охарактеризуйте VLAN Trunking Protocol (VTP). Приведите перечень команд с пояснениями для настройки и просмотра информации о VLAN.**  
**VTP (VLAN Trunking Protocol)** – это протокол Cisco, используемый для управления VLAN в сети. Он позволяет централизованно создавать, изменять и удалять VLAN на всех коммутаторах, которые работают в режиме клиента.  

**Режимы работы VTP**:  
- **Server (сервер)** – главный коммутатор, управляющий VLAN и распространяющий информацию.  
- **Client (клиент)** – получает информацию о VLAN от сервера, но не может сам изменять конфигурацию.  
- **Transparent (прозрачный)** – не участвует в управлении VLAN, но передает VTP-объявления дальше.  

**Команды настройки VTP:**  

```
configure terminal
vtp mode server          ! Установка режима сервера
vtp domain mydomain      ! Установка VTP-домена
vtp password mypass      ! Установка пароля VTP
vtp version 2           ! Установка версии VTP (рекомендуется 2)
```
  
**Добавление VLAN:**  

```
vlan 10
name Sales
exit
```

**Проверка информации о VLAN:**  

```
show vlan brief          ! Краткий список VLAN
show vtp status         ! Информация о VTP
show vtp counters       ! Количество переданных VTP-сообщений
```

3. Охарактеризуйте Internet Control Message Protocol (ICMP). Опишите формат пакета ICMP.**  
**ICMP (Internet Control Message Protocol)** – это сетевой протокол, используемый для диагностики соединений в IP-сетях. Он передает сообщения об ошибках и другую служебную информацию.  

**Основные функции ICMP:**  

- Проверка доступности узлов (`ping`)  
- Уведомление об ошибках маршрутизации (`Destination Unreachable`)  
- Контроль перегрузки сети (`Source Quench`)  
- Изменение маршрутизации (`Redirect`)  

**Формат ICMP-пакета:**  

| Поле          | Размер (бит) | Описание |
|--------------|-------------|------------|
| Тип          | 8           | Определяет тип сообщения (например, 0 – эхо-ответ, 8 – эхо-запрос) |
| Код          | 8           | Дополнительная информация (например, 0 – стандартное поведение) |
| Контрольная сумма | 16      | Проверка целостности пакета |
| Данные       | Переменный  | Оригинальные данные пакета |

Пример команды для проверки связи через ICMP:  

```
ping 192.168.1.1
```

4. **Охарактеризуйте Address Resolution Protocol (ARP). Опишите формат пакета ARP.**  

**ARP (Address Resolution Protocol)** – протокол, используемый для преобразования IP-адресов в MAC-адреса в локальных сетях.  

**Принцип работы ARP:**  

1. Узел отправляет ARP-запрос (`Who has 192.168.1.1? Tell 192.168.1.2`).  
2. Узел с IP-адресом `192.168.1.1` отвечает, указывая свой MAC-адрес.  
3. MAC-адрес сохраняется в ARP-кэше отправителя.  

**Формат ARP-пакета:**  

| Поле           | Размер (бит) | Описание |
|---------------|-------------|------------|
| Тип аппаратного адреса | 16 | Определяет тип сети (Ethernet = 1) |
| Тип протокола | 16 | IPv4 = 0x0800 |
| Длина MAC-адреса | 8 | Обычно 6 байт |
| Длина IP-адреса | 8 | Обычно 4 байта |
| Код операции | 16 | 1 = ARP-запрос, 2 = ARP-ответ |
| MAC-адрес отправителя | 48 | MAC-адрес узла, отправляющего запрос |
| IP-адрес отправителя | 32 | IP-адрес отправителя |
| MAC-адрес получателя | 48 | Оставляется пустым в запросе |
| IP-адрес получателя | 32 | IP-адрес целевого узла |

Пример команды для просмотра ARP-кэша:  

```
show arp
```

5. **Что такое MAC-адрес? Какова его структура?**  

**MAC-адрес (Media Access Control address)** – это уникальный физический адрес сетевого устройства, записанный в его сетевую карту.  

**Структура MAC-адреса (48 бит / 6 байт):**  

Формат: `XX:XX:XX:YY:YY:YY`, где:  
- `XX:XX:XX` – первые 3 байта (OUI) определяют производителя устройства.  
- `YY:YY:YY` – последние 3 байта уникальны для конкретного устройства.  

Пример MAC-адреса:  

```
00:1A:2B:3C:4D:5E
```

Команда для просмотра MAC-адресов, привязанных к портам коммутатора: 

```
show mac address-table
```

# Выводы

В ходе выполнения лабораторной работы мы получили основные навыки по настройке VLAN на коммутаторах сети.

# Список литературы{.unnumbered}

::: {#refs}
:::

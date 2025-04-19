---
## Front matter
lang: ru-RU
title: Защита по лабораторной работе №10
subtitle: pf
author:
  - Чесноков Артемий Павлович
institute:
  - Российский университет дружбы народов, Москва, Россия
date: 15 марта 2025

## i18n babel
babel-lang: russian
babel-otherlangs: english

## Formatting pdf
toc: false
toc-title: Содержание
slide_level: 2
aspectratio: 169
section-titles: true
theme: metropolis
header-includes:
 - \metroset{progressbar=frametitle,sectionpage=progressbar,numbering=fraction}
---

# Информация


## Цель

Освоить настройку прав доступа пользователей к ресурсам сети.

## Подключаем laptop .

![прямым| 24 порт](image/1.png)

## Выдаем статический адрес  .

![10.128.6.200](image/2.png)

## Даем gateaway и dns адреса  .

![выдали](image/3.png)

## Разрешаем обращаться к web .

![пока что только по ip](image/4.png)

## Пример захода на адрес по ip через устройство .

![по домену пока что не можем](image/5.png)

## Разрешаем админу ftp и telnet .

![только админу](image/6.png)

## Пробуем от админа  .

![успешно](image/7.png)

## Пробуем от любого другого пользователя .

![ловим таймаут](image/8.png)

## Делаем доступ на файловый сервер .

![выдали](image/9.png)

## Настраиваем доступы для mail и dns  .

![сделали](image/10.png)

## Заходим по домену с любого устройства  .

![ура](image/11.png)

##  Всегда пропускаем icmp через маршрутизатор, всегда разрешаем, откуда угодно и куда угодно  .

![Ставим в первый порядок](image/12.png)

## Даем админу доступ к сетевому оборудованию  .

![выдали](image/13.png)

## Спасибо за внимание.

---
## Front matter
lang: ru-RU
title: Защита по лабораторной работе №11
subtitle: student
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

![докладчик](image/me.jpeg)

## Цель

Провести подготовительные мероприятия по подключению локальной сети
организации к Интернету.

## Обновляем нашу L1 схему, которую мы создаем в 3ей лабораторной работе .

![добавили области провайдера и сети Интернет](image/1.png)

## Непосредственно в packetTracer'е размещаем все устройства  .

![так же, как и в L1 разделяем на две области](image/2.png)

## В physical view размещаем новые здания: Provider и Internet  .

![разместили](image/3.png)

## Переносим в physical view все устройства на их здания .

![пример для переноса маршрутизатора провайдера](image/4.png)

![как должно выглядеть содержимое здания Internet](image/5.png)

## Заменяем модули на повторителях .

![пример для нового повторителя на донской](image/6.png)

## Итоговая схема сети  .

![всё подключили](image/7.png)

## Настраиваем статические адреса на сервера .

![пример для esystem.rudn.ru](image/8.png)

## Добавляем адреса серверов в dns list .

![итоговый list](image/9.png)



## Спасибо за внимание.

---
layout: post
date: 2016-08-06 0:24:00 +0300
title: "Поиск SQL Injection"
description: Как быстро просканировать сайт на SQL Injection. Используем Nmap для быстрого поиска уязвимостей движка.
keywords: nmap, взлом, sql injection
mood: happy
comments: false
category:
- security
tags:

---

<figure>
    <img src="http://dubkov.xyz/assets/img/sql-injection.png" alt="SQL Injection" />
</figure>

Планирую собрать интересную подборочку статей о поиске SQL инъекций и методах внедрения SQL-кода в различные веб-интерфейсы. 
И начинается моя подборка с поста о быстром поиске SQL Injection на сайте с помощью Nmap. Скрипт достаточно популярный и
с его помощью, можно осуществлять поиск дырок на веб-страницах.
<!--more-->
<h2>Быстрый поиск SQL Injection</h2>

Как осуществить быстрый поиск SQL-уязвимостей на сайте с помощью Nmap?
Очень просто. Потребуется одна команда и потенциально уязвимый веб-ресурс. 
Так как, я не трогаю чужие веб-сайты и сервера, поиск уязвимости я буду осуществлять на своем сайте.

Обращаемся с помощью Nmap к веб-серверу с помощью простой команды:

`nmap -sV --script=http-sql-injection www.website.com -Pn -p 80`

<blockquote>О значении указанных флагов, можно прочитать в справке Nmap, например</blockquote>

<h3>Результаты поиска SQL Injection</h3>

Проходит чуть меньше минуты, смотрим на результаты

![SQL Injection Nmap](/assets/img/sql-injection-nmap.png)

![SQL Injection Nmap](/assets/img/sql-injection-nmap-2.png)

Открываем любую из найденных уязвимостей через браузер

![SQL Injection Iceweasel](/assets/img/iceweasel-sql-injection.png)

Необязательно пользоваться различными сканерами уязвимостей, искать руками, ведь Nmap неплохо справляется с этой задачей, не правда ли? 

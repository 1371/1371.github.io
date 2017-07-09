---
layout: post
date: 2017-06-26 20:15
title: "Установка WPScan в Windows 10"
description: Как установить скрипт для проверки на уязвимости плагинов и расширений в CMS WordPress (WPScan) на Windows 10? Пошаговая инструкция. 
mood: happy
category:
- security
comments: true
---

<figure>
    <img src="http://dubkov.xyz/assets/img/wordpress.jpg" alt="WordPress" />
</figure>

WPScan — утилита, которая служит помощником в поиске уязвимостей на движке Wordpress. Она входит в состав инструментария операционной системы Kali Linux. Некоторые инструменты для пентестинга
различных CMS, теперь можно устанавливать и в Windows.

<!--more-->

Внимание! Инструкция содержит множество изображений и заголовков. Будьте внимательны.

#### Включаем режим разработчика в Windows 10

<figure>
    <img src="http://dubkov.xyz/assets/img/install-wpscan-1.png" alt="Включение режима разработчика Windows 10" />
</figure>

<figure>
    <img src="http://dubkov.xyz/assets/img/install-wpscan-2.png" alt="Включение режима разработчика Windows 10" />
</figure>

<figure>
    <img src="http://dubkov.xyz/assets/img/install-wpscan-3.png" alt="Включение режима разработчика Windows 10" />
</figure>

#### Активируем подсистему Windows для Linux

<figure>
    <img src="http://dubkov.xyz/assets/img/install-wpscan-4.png" alt="Включение подсистемы" />
</figure>

<figure>
    <img src="http://dubkov.xyz/assets/img/install-wpscan-5.png" alt="Включение подсистемы" />
</figure>

##### Перезагружаем операционную систему

### Нам нужен Bash

#### Ищем bash в поисковой строке

<figure>
    <img src="http://dubkov.xyz/assets/img/install-wpscan-6.png" alt="Поиск bash в Windows 10" />
</figure>

### Устанавливаем среду Ubuntu в Windows

<figure>
    <img src="http://dubkov.xyz/assets/img/install-wpscan-7.png" alt="Установка среды" />
    <figcaption>Соглашаемся с консолью</figcaption>
</figure>

#### Создаем учетную запись пользователя

<figure>
    <img src="http://dubkov.xyz/assets/img/install-wpscan-8.png" alt="Установка среды" />
    <figcaption>Вводим желаемый логин и пароль суперпользователя</figcaption>
</figure>


##### Система готова к установке WPScan

<figure>
    <img src="http://dubkov.xyz/assets/img/install-wpscan-9.png" alt="Установка среды" />
</figure>


## Установка WPScan на Windows
##### Убунту, Гитхаб, Бандлер, Джем

Идем на сайт разработчика (wpscan.org). Листаем до заголовка про установку в ручную.

<figure>
    <img src="http://dubkov.xyz/assets/img/install-wpscan-10.png" alt="Установка WPScan" />
</figure>


Копируем в bash команду для установки WPScan на Ubuntu

<figure>
    <img src="http://dubkov.xyz/assets/img/install-wpscan-11.png" alt="Установка WPScan" />
</figure>

Устанавливаем Ruby Version Manager. Для этого копируем в консоль все необходимые строки для полноценной установки. 

<figure>
    <img src="http://dubkov.xyz/assets/img/install-wpscan-12.png" alt="Установка RVM" />
</figure>

Не забываем установить менеджер для управления gem'ами командой:

{% highlight bash linenos %}bundle install{% endhighlight %}

<figure>
    <img src="http://dubkov.xyz/assets/img/install-wpscan-13.png" alt="Bundle Install" />
</figure>

Обновляем базу данных WPScan с помощью команды:

{% highlight bash linenos %}./wpscan.rb --update{% endhighlight %}

<figure>
    <img src="http://dubkov.xyz/assets/img/install-wpscan-13.png" alt="Обновление WPScan" />
</figure>

Можно пользоваться. Утилита WPScan является универсальным инструментом для поиска уязвимостей в WordPress. С помощью нее можно найти уязвимые плагины, узнать логины администраторов, название и версию установленной темы.

Данная инструкция подойдет и для установки других подобных скриптов в Windows 10. То, что мы видели раньше только на Linux постепенно приходит и в Windows.
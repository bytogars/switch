---
permalink: /lanplay.html
title: Мультиплеер на прошитой консоли (LAN Play)
author_profile: true
---
{% include toc title="Разделы" %}

Думаю, ни для кого не секрет, что на прошитой приставке за игру онлайн бан прилетает со сверхзвуковой скоростью. Это связано с тем, что игра онлайн происходит через сервера Nintendo, которые прекрасна знают куплена ли ваша игра или нет. Что касается картриджа, то в каждый картридж вшит уникальный идентификатор, который сервер так же может отслеживать. Если с картриджа снят дамп, то все, кто выйдет с такого образа онлайн будут иметь одинаковый идентификатор, что, естественно, так же приведёт к бану картриджа и его пользователей.

В данный момент можно играть в официальный онлайн только на свой страх и риск, используя, например, легальную копию игры для онлайна или бесплатные игры. Некоторое время вас даже не забанят. 

Выход нашли в локальной сетевой игре. Некоторые игры поддерживают LAN-play, что позволяет нам перенаправить данные, которые посылает консоль на ПК и через специальный сервер направить их другим приставкам. Все подключенные к одному серверу консоли будут считать, что они соединены напрямую. И да, этот метод даст возможность поиграть даже тем, кого забанили.

Самый существенный минус этого способа - это необходимость договариваться заранее со всеми участниками игры. В русскоязычном сегменте это делается в Discord на канале [Switch Пиратский онлайн](https://discordapp.com/invite/By4JA4C){:target="_blank"}. С игроками со всего мира можно пообщаться [здесь](https://discordapp.com/invite/KAFHaWj){:target="_blank"}. Договоритесь с другими игроками во что будете играть, и на каком сервере.

## Что понадобится

* Свежая версия [SDFiles](https://github.com/rashevskyv/switch/releases/latest){:target="_blank"}
* Свежая версия программы [Lan-Play-Server-Manager](https://github.com/Urferu/Lan-Play-Server-Manager/releases/latest){:target="_blank"}
	* Пользователи MacOS и Linux могут воспользоваться программой [lan-play-GUI](https://gbatemp.net/threads/lan-play-gui-a-graphical-interface-for-lan-play-updated-v1-0-0.525900/){:target="_blank"}
* Драйвера [WinPCap](https://www.winpcap.org/install/bin/WinPcap_4_1_3.exe){:target="_blank"}

## Предварительные настройки

### Часть I - Настраиваем клиент

Инструкция будет дана для приложения [Lan-Play-Server-Manager](https://github.com/Urferu/Lan-Play-Server-Manager/releases/latest){:target="_blank"}, которое работает только на Windows. Пользователи MacOS и Linux могут воспользоваться программой [lan-play-GUI](https://gbatemp.net/threads/lan-play-gui-a-graphical-interface-for-lan-play-updated-v1-0-0.525900/){:target="_blank"}. Как её настраивать можно посмотреть в видео, которое есть по ссылке.

1. Скачайте и установите драйвера [WinPCap](https://www.winpcap.org/install/bin/WinPcap_4_1_3.exe){:target="_blank"}
1. Скачайте свежую версию [Lan-Play-Server-Manager](https://github.com/Urferu/Lan-Play-Server-Manager/releases/latest){:target="_blank"} и распакуйте её на ПК
1. Распакуйте архив `Lan-Play-Server-Manager.zip` в удобную папку 
1. Запустите `Lan-Play-Server-Manager.exe` от имени Администратора 
1. Снимите галочку с пункта "**Fake Internet**" 
1. Выберите нужный сервер из представленных в списке и нажмите "**Подключиться**"
	* Договоритесь с другими игроками в [Discord](https://discordapp.com/invite/By4JA4C){:target="_blank"} на каком сервере вы будете играть
	* Если подключение установлено, кнопка станет зелёной и сменит название

### Часть II - Настраиваем Switch

1. Обновите [SDFiles](https://github.com/rashevskyv/switch/releases/latest){:target="_blank"} по инструкции из репозитория, если не делали этого ранее
1. Включите приставку и перейдите в "**Системные настройки**" -> "**Интернет**" -> "**Интернет-настройки**"
1. Подключитесь к вашей WiFi-сети 
1. После успешного подключения снова перейдите в "**Интернет-настройки**" и выберите вашу WiFi-сеть 
1. Выберите "**Изменить настройки**"
1. Измените "**Настройки IP-адреса**" на "**Ручной ввод**"
	1. В поле "**IP-адрес**" введите любой IP адрес в диапазоне от `10.13.0.1` до `10.13.255.254` (кроме `10.13.37.1`, его мы используем в качестве шлюза)
	1. В поле "**Маска подсети**" введите `255.255.0.0`
	1. В поле "**Шлюз**" `10.13.37.1`
1. Выберите "**Настройки DNS**" -> "**Ручной ввод**"
	1. В поле "**Первичный DNS**" введите `163.172.141.219`
	1. В поле "**Вторичный DNS**" введите `45.248.48.62` и нажмите "**Сохранить**", а затем OK
1. Выберите "**Подключиться к этой сети**", после проверки нажмите ОК
	* Вы не пройдёте проверку, если не запустили клиент и не подключились к серверу
1. Если вы используете [SX OS](){:target="_blank"}, откройте меню SXOS (альбомы) и во вкладке "**Options**" активируйте "**Internet Local Wireless Play**"
	* Необходимо активировать заново после каждой перезагрузки приставки
	
## Подключение к LAN-play

Не в каждой игре есть возможность LAN-play. Актуальный список игр, которые поддерживают этот режим можно посмотреть [здесь](https://docs.google.com/spreadsheets/d/1fCPkCXSy_RJCcMvde3OxCeJeFRCfnnSZPcF3A6sBOPM/edit?usp=sharing){:target="_blank"}. В некоторых играх эта функция активируется [специальной комбинацией клавиш](http://www.lan-play.com/games){:target="_blank"}. Более подробно об этом вы можете узнать в [Discord](https://discordapp.com/invite/By4JA4C){:target="_blank"}

Так же не забывайте, что для успешного подключения все игроки должны иметь одинаковую версию игры и не всегда лучшей будет последняя. Уточняйте в чате на какой версии следует играть и где брать апдейт.

Настроим игру на примере Mario Kart 8

1. Запустите игру
1. Нажмите одновременно (L)+(R)+(Left_Analog)
	* Вы увидите, как название последнего пункта изменилось на "**Игра по LAN**"
1. Зайдите в "**Игра по LAN**" и выберите "**1и**", если собираетесь играть самостоятельно на своей приставке и "**2и**", если на одной консоли будут играть два игрока
1. Создайте комнату, или подключите к уже имеющейся 
1. Играйте 

## Возможные проблемы и их решения

### Ошибка 2110-3127 при подключении к WiFi

1. Lan-play запущен без прав администратора
1. Слетел Winpcap driver - переустановите его
1. Проблема на стороне роутера (случается с дешёвыми моделями) - перегрузите роутер
1. WiFi неправильно настроен. Убедитесь, что в точности повторили все пункты

### Ошибка 2160-8007

1. WiFi неправильно настроен. Убедитесь, что в точности повторили все пункты

### Ошибка 2155-8007 при подключении к серверам Nintendo

Вам и не нужно к ним подключаться
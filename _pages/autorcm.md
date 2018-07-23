---
permalink: /autorcm.html
title: AutoRCM
author_profile: true
---
{% include toc title="Разделы" %}

AutoRCM - на консоли специальным образом портится BOOT0, вследствие чего консоль не может загрузиться прямо в систему и загружается автоматически в режим [RCM](fusee-gelee#что-такое-rcm){:target="_blank"}. Достаточно просто включить консоли и она автоматически попадёт в режим восстановления. Не нужно зажимать комбинацию кнопок и использовать [замыкатель](fusee-gelee#замыкатель){:target="_blank"}!
{: .notice--info}

# Что понадобится

* Умение [запускать пейлоады через Fusée Gelée](fusee-gelee){:target="_blank"}
* Свежая версия [briccmii](https://switchtools.sshnuke.net/){:target="_blank"}

# Рекомендуемый способ 

## Установка AutoRCM

1. Запустите пейлоад [brickmii](https://switchtools.sshnuke.net/){:target="_blank"} с помощью [Fusée Gelée](fusee-gelee){:target="_blank"}
1. На Switch откроется окно программы "brickmii" - эта программа создана для контроля режима AutoRCM 
1. Нажмите (VOL-) для включения AutoRCM
1. Нажмите (POWER) для перезагрузки консоли в режим RCM

## Удаление AutoRCM 

Категорически не рекомендуется удалять AutoRCM, если вы делали [безопасное обновление системы](update-to-latest){:target="_blank"} - [сожжёте предохранители](update-to-latest#%D1%82%D0%B5%D0%BE%D1%80%D0%B5%D1%82%D0%B8%D1%87%D0%B5%D1%81%D0%BA%D0%B0%D1%8F-%D1%87%D0%B0%D1%81%D1%82%D1%8C){:target="_blank"}

1. Запустите пейлоад [brickmii](https://switchtools.sshnuke.net/){:target="_blank"} с помощью [Fusée Gelée](fusee-gelee){:target="_blank"}
1. На Switch откроется окно программы "brickmii" - эта программа создана для контроля режима AutoRCM 
1. Нажмите (VOL+) для отключения AutoRCM
1. Нажмите (POWER) для перезагрузки консоли в режим RCM 

# SX OS

В SX OS есть встроенный механизм активации AutoRCM через меню загрузчика, однако я все же рекомендую использовать для этого bricmii
	
## Установка AutoRCM

1. Запустите SX OS
1. При появлении заставки зажмите и удерживайте (VOL+)
1. Перейдите в "Options" -> "Install AutoRCM" -> "Continue"
1. Нажмите "Back" дважды, чтобы вернуться в главное меню и выберите "Boot custom FW" для запуска SX OS

После активации AutoRCM при наличии донгла система сразу будет грузиться в SX OS, если донгла нет, то нужно будет посылать [загрузчик SX OS](https://sx.xecuter.com/download/payload.bin){:target="_blank"} с помощью [Fusée Gelée](fusee-gelee){:target="_blank"}

## Удаление AutoRCM 

Категорически не рекомендуется удалять AutoRCM, если вы делали [безопасное обновление системы](update-to-latest){:target="_blank"} - [сожжёте предохранители](update-to-latest#%D1%82%D0%B5%D0%BE%D1%80%D0%B5%D1%82%D0%B8%D1%87%D0%B5%D1%81%D0%BA%D0%B0%D1%8F-%D1%87%D0%B0%D1%81%D1%82%D1%8C){:target="_blank"}

1. Запустите SX OS
1. При появлении заставки зажмите и удерживайте (VOL+)
1. Перейдите в "Options" -> "Uninstall AutoRCM" -> "Continue"
1. Нажмите "Back" дважды, чтобы вернуться в главное меню и выберите "Boot custom FW" для запуска SX OS
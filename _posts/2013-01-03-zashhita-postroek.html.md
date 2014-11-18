---
layout: post
title: Защита построек
description: ""
modified: 2013-01-03
tags: [сервер]
comments: false
image:
  feature: abstract-3.jpg
  #credit: dargadgetz
  #creditlink: http://www.dargadgetz.com/ios-7-abstract-wallpaper-pack-for-iphone-5-and-ipod-touch-retina/
---

![privat]({{ site.url }}/images/posts/privat.jpg)
{: .pull-center}

Для защиты построек пользователь, со статусом **Admin**, должен посредством команды "/region" создать регион.
<!-- more -->
Для начала необходимо поставить точки протекта "/region set (1/2)", затем дать региону имя "/region define (имя региона)" и , если необходимо, то подогнать размер региона командой "/region resize (имя региона) (l,r,u,d) (на сколько блоков)", потом дать разрешение на изменение региона игроку, построившему данную постройку, командой "/region allow (ник) (имя региона)".

Для удаления региона используется команда "/region delete (имя региона)", а для удаления игрока из региона "/region remove (ник) (имя региона)".

Если необходимо проверить существование региона в определённой точке, то исполняется команда "/region name", затем ударяется блок.

Включить или отключить защиту в регионе можно командой "/region protect (имя региона) (true/false)".

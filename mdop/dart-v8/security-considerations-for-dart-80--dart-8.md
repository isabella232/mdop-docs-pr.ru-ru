---
title: Рекомендации по обеспечению безопасности для DaRT 8.0
description: Рекомендации по обеспечению безопасности для DaRT 8.0
author: dansimp
ms.assetid: 45ef8164-fee7-41a1-9a36-de4e3264e7a8
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 02d32d926c0def7d33bebd399cd380eed4e8385e
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10812696"
---
# Рекомендации по обеспечению безопасности для DaRT 8.0


В этой статье содержится краткий обзор учетных записей и групп, файлов журналов и других вопросов, связанных с безопасностью, для средств диагностики и восстановления Microsoft (DaRT) 8,0. Чтобы получить дополнительные сведения, воспользуйтесь ссылками, приведенными в этой статье.

## Общие рекомендации по безопасности


**Общие сведения о рисках для системы безопасности**. DaRT 8,0 включает в себя функции, позволяющие администратору или сотрудникам службы поддержки выполнять удаленное выполнение инструментов DaRT для устранения неполадок на компьютере конечного пользователя. Кроме того, вы можете сохранить образ международной организации по стандартизации (ISO) на USB-накопителе или разместить его содержимое как раздел восстановления на жестком диске компьютера, чтобы добавить на него образ ISO в сети. Эти возможности обеспечивают гибкость, но также создают потенциальные риски безопасности, которые следует принимать во время настройки DaRT.

**Физическая защита компьютеров**. Если администраторы и сотрудники службы поддержки не находятся на своем компьютере, они должны блокировать свои компьютеры и использовать защищенную экранную заставку.

**Установка последних обновлений для системы безопасности на всех компьютерах**. Будьте в курсе новых обновлений для операционных систем, подписавшись на службу уведомлений системы безопасности ( <https://go.microsoft.com/fwlink/?LinkId=28819> ).

## Ограничение доступа к средствам DaRT для конечных пользователей


При создании изображения для восстановления DaRT вы можете выбрать инструменты, которые вы хотите включить. По соображениям безопасности вы можете ограничить доступ конечных пользователей к более мощным средствам DaRT, таким как очистка диска и Locksmith. В DaRT 8,0 вы можете отключить определенные инструменты в ходе настройки и по-прежнему сделать их доступными для сотрудников службы поддержки, когда конечный пользователь запускает функцию удаленного подключения.

Вы даже можете настроить изображение DaRT таким образом, чтобы параметр начала сеанса удаленного подключения был единственным средством, доступным для конечного пользователя.

**Важно!**  После установки удаленного подключения все инструменты, которые вы включили в образ восстановления, в том числе те, которые недоступны для конечного пользователя, станут доступны любому сотруднику службы поддержки, работающему на компьютере конечного пользователя.

 

Дополнительные сведения о том, как включить инструменты в образ восстановления DaRT, приведены в статье [Обзор средств на dart 8,0](overview-of-the-tools-in-dart-80-dart-8.md).

## Защита изображения для восстановления DaRT


Если вы развертываете изображение для восстановления DaRT, сохранив его на USB-накопителе или создави удаленную секцию или раздел восстановления, вы можете добавить предпочтительный способ шифрования диска в ISO. Шифрование ISO помогает гарантировать, что конечные пользователи не смогут использовать функцию DaRT, если они должны получить доступ к образу восстановления, и это гарантирует, что неавторизованные пользователи не смогут загрузить DaRT на компьютерах, входящих в состав другого пользователя. Если вы используете метод шифрования, не забудьте развернуть и включить его на всех компьютерах.

**Примечание**  DaRT 8,0 поддерживает BitLocker Native.

 

Чтобы включить шифрование диска, добавьте файлы решения для шифрования при создании образа восстановления. Ваше решение для шифрования должно быть способно работать в среде WinPE. Конечные пользователи, которые загружают из ISO, смогут получить доступ к этому решению шифрования и разблокировать диск.

## Обеспечение безопасности двух компьютеров при использовании удаленного подключения


По умолчанию связь между двумя компьютерами, на которых установлен **Удаленный сеанс подключения** , может быть не зашифрована. Таким образом, чтобы обеспечить безопасность двух компьютеров, рекомендуется, чтобы оба компьютера были частью одной сети.

## Статьи по теме


[Безопасность и конфиденциальность в DaRT 8.0](security-and-privacy-for-dart-80-dart-8.md)

 

 





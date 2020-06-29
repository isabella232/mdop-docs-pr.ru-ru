---
title: Использование разностного SFT-файла
description: Использование разностного SFT-файла
author: dansimp
ms.assetid: 607e30fd-2f0e-4e2f-b669-0b3f010aebb0
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 85cc45f9665569d77fcf275db6dbc080eb919229
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10816389"
---
# Использование разностного SFT-файла


При виртуализации приложения секвенсор Microsoft Application Virtualization (App-V) создает файлы SFT (SFT), в которых хранятся все содержимое файлов виртуального приложения и сведения о конфигурации. В версии 4.5 App-V появился Разностный SFT-файл (dsft). После использования программы Sequencer для создания обновления существующего пакета вы можете создать этот файл, чтобы сохранить только различия между исходным пакетом приложения и новой версией. Таким образом, этот файл значительно меньше полного SFT-файла для новой версии приложения и уменьшает влияние отправки обновлений пакетов по сетевым подключениям с низкой пропускной способностью. Тем не менее, его использование поддерживается только в определенных ситуациях, использующих определенные ограничения. Эта функция предназначена специально для тех случаев, когда вы используете систему электронной рассылки программного обеспечения (ESD) для управления группой пользователей с помощью локального файлового сервера в соединении с низким пропускной способностью и не используете потоковые серверы App-V.

Если вы используете конфигурацию Manager2007 для управления пользователями, вам не нужно использовать Разностный SFT-файл, так как Configuration Manager поддерживает развертывания с низким пропускной способностью, которые уже встроены. Это также не требуется, если вы используете сервер Application Virtualization (App-V) или Streaming Servers с активной модернизацией, так как клиент извлекает только различия между старыми и новыми версиями пакетов.

В приведенной ниже процедуре показано, как использовать mkdiffpkg.exe, включенный в установку Sequencer, для создания разностного SFT, после завершения обновления виртуального пакета приложения, а также для развертывания разностного SFT файла. Выполнение этой процедуры гарантирует, что если пакет будет выгружен с клиентского компьютера, то при следующем запуске приложения клиент вернется к URL-адресу переопределения, который задается потоком для полного пакета v2. SFT из локального общего файлового файла. Это позволит избежать сбоев для пользователя при запуске приложения. Если весь клиент поврежден или удален, рекомендуется настроить систему ESD на развертывание полной версии обновленного пакета (для версии v2. SFT) для клиента.

Дополнительные сведения об обновлении пакета можно найти в разделе "как обновить существующее виртуальное приложение" в руководстве по эксплуатации App-V 4.5 на странице <https://go.microsoft.com/fwlink/?LinkId=133129>

**Примечание**  В качестве предварительной версии для всех компьютеров пользователей, для которых требуется использовать ESD, должен быть полностью загружен файл v1. SFT в локальном кэше, а на всех компьютерах должна быть включена потоковая передача файлов.

 

**Использование разностного SFT — файла**

1.  Войдите на компьютер секвенсор, используя учетную запись с правами администратора. Откройте исходный пакет (v1) для обновления в секвенсоре, а затем обновите пакет до новой версии (v2) и сохраните его как новый v2. SFT.

2.  Откройте окно команд в установочной папке App-V 4.5 и выполните следующую команду:

    `“mkdiffpkg.exe V2.sft V2.dsft”`

3.  С помощью системы ESD или другого процесса копирования файлов скопируйте полный файл содержимого пакета версии 2 (SFT) в локальную общую файловую систему, доступную для компьютеров пользователей по надежному подключенному сетевому подключению.

4.  Используя систему ESD, разместите на каждом компьютере пользователя копию SFT-файла версии 2. dsft.

5.  Чтобы импортировать файл V2. dsft, выполните следующую команду SFTMIME на каждом компьютере пользователя:

    `“SFTMIME load package:<package name> /SFTPATH <path to V2.dsft>”`

6.  Выполните следующую команду SFTMIME для каждого компьютера пользователя, чтобы настроить URL-адрес для переопределения файла v2. SFT:

    `“SFTMIME configure package:<package name> /OverrideURL FILE://<network path to V2.sft>”`

**Примечание.**  
-   Разностные SFT файлы должны применяться к клиентам в правильном порядке. Например, параметр v2. dsft необходимо применить к приложению v1 перед применением v3. dsft.

-   Возможность **создания пакета установщика Microsoft Windows (MSI)** в секвенсоре не может использоваться с РАЗНОСТным SFT-файлом.

 

## Статьи по теме


[Создание и обновление виртуальных приложений с помощью секвенсора App-V](how-to-create-or-upgrade-virtual-applications-using--the-app-v-sequencer.md)

 

 





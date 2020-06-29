---
title: Развертывание рабочей области MED-V в образе Windows 7
description: Развертывание рабочей области MED-V в образе Windows 7
author: dansimp
ms.assetid: a83aba4e-8681-4906-9872-f431c0bb15f9
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 49dd796d6f6af425b9000b595a0d828c3cb0035a
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10827282"
---
# Развертывание рабочей области MED-V в образе Windows 7


Все компоненты MED-V можно установить в образ Windows 7, распространяемый в рамках всего предприятия, так же, как и в любой новой версии Windows 7. Конечный пользователь затем завершает установку рабочей области MED-V, щелкнув ярлык меню " **Пуск** ", который вы настроили на запуск med-v. При первом запуске программы установки для завершения настройки выполняются инструкции конечного пользователя.

В следующем разделе содержатся сведения и инструкции, которые помогут вам развернуть рабочую область MED-V в рамках всего предприятия с помощью образа Windows 7.

**Развертывание рабочей области MED-V в образе Windows 7**

1.  Создание стандартного изображения Windows 7. Дополнительные сведения можно найти в [статье Создание стандартного образа Windows 7: пошаговое руководство](https://go.microsoft.com/fwlink/?LinkId=204843) ( https://go.microsoft.com/fwlink/?LinkId=204843) .

2.  В образе Windows 7 Установите Windows Virtual PC и обновления виртуальных компьютеров с Windows. Дополнительные сведения можно найти в разделе [Настройка предварительных требований для установки](configure-installation-prerequisites.md).

3.  Установите агент узла MED-V с помощью установочного файла MED-V \ _HostAgent \ _Setup. Дополнительные сведения [можно найти в разделе Установка агента узла MED-V вручную](how-to-manually-install-the-med-v-host-agent.md).

    **Предупреждение**  Internet Explorer необходимо закрыть перед установкой агента узла MED-V, в противном случае конфликты могут возникать позже с перенаправлением URL-адреса. Вы также можете сделать это, указав компьютер во время распространения.

     

4.  Скопируйте файлы пакета рабочей области для MED-V в образ Windows 7. Файлы пакета рабочей области для MED-V — это файл установщика рабочей области MED-V, MEDV и файл setup.exe, созданный с помощью **диспетчера рабочих областей med-v**.

    **Важно!**  Файл. MEDV и setup.exe должен находиться в той же папке, что и программа установки рабочей области MED-V. Затем установите рабочую область MED-V, запустив setup.exe.

     

5.  Настройте ярлык в меню " **Пуск** ", чтобы открыть пакет рабочей области для MED-V.

    Создание ярлыка меню " **Пуск** " для файла setup.exe, позволяющего конечному пользователю ЗАПУСКАТЬ установку MED-V по мере необходимости.

6.  Используя стандартный процесс развертывания образа компании, вы можете распространять его на компьютеры в вашей организации, требующие MED-V.

Когда конечный пользователь должен получить доступ к приложению, опубликованному в рабочей области MED-V, он может щелкнуть ярлык меню " **Пуск** ", чтобы установить рабочую область "med-v". Это автоматически запускается при первом запуске программы установки и завершает настройку MED-V. После того как вы закончите настройку, конечный пользователь сможет получить доступ к приложениям для MED-V в меню " **Пуск** ".

## Статьи по теме


[Обзор развертывания MED-V 2.0](med-v-20-deployment-overview.md)

[Развертывание рабочей области MED-V с помощью системы электронного распространения программного обеспечения](how-to-deploy-a-med-v-workspace-through-an-electronic-software-distribution-system.md)

 

 





---
title: Ручное развертывание рабочей области MED-V
description: Ручное развертывание рабочей области MED-V
author: dansimp
ms.assetid: 94bfb209-2230-49b6-bb40-9c6ab088dbf4
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 3f13d06e2232681f87df7a71b9a3ef3269b4f9ce
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10827279"
---
# Ручное развертывание рабочей области MED-V


В некоторых случаях вам может потребоваться развернуть рабочую область MED-V вручную, например, если ваша компания не использует электронную систему распространения программного обеспечения для развертывания приложений.

В этом разделе приведены инструкции по развертыванию рабочей области MED-V вручную.

**Развертывание рабочей области для MED-V вручную**

1.  Скопируйте все необходимые приложения и файлы пакета рабочей области для MED-V на общий диск или DVD-диск. Ниже приведен список необходимых приложений и файлов.

    -   **Windows Virtual PC**. Дополнительные сведения можно найти в разделе [Настройка предварительных требований для установки](configure-installation-prerequisites.md).

    -   **Дополнения и обновления для ВИРТУАЛЬНЫХ ПК Windows**. Дополнительные сведения можно найти в разделе [Настройка предварительных требований для установки](configure-installation-prerequisites.md).

    -   **Установочный файл агента узла MED-v** — Установка агента узла (MED-V \ _HostAgent \ _setup установочный файл).

        **Warning**  
        Перед установкой агента узла MED-V закройте Internet Explorer, в противном случае конфликты могут возникать позже с перенаправлением URL-адреса. Вы также можете сделать это, указав компьютер во время распространения.



~~~
-   **MED-V Workspace Installer, VHD, and Setup Executable** – created with the **MED-V Workspace Packager**. For more information, see [Create a MED-V Workspace Package](create-a-med-v-workspace-package.md).

    **Important**  
    The compressed VHD file (.medv) and the Setup executable program (setup.exe) must be in the same folder as the MED-V workspace installer.
~~~



2. Установите указанные ниже действия в указанном порядке. Конечный пользователь может выполнить эту задачу вручную или создать сценарий, чтобы установить следующие возможности:

   -   Windows Virtual PC и Windows Virtual PC, дополненные и обновления. Требуется перезагрузка компьютера.

   -   Агент узла MED-V.

       **Примечание.**  
       Если он запущен, необходимо перезапустить Internet Explorer, прежде чем можно будет завершить установку агента узла MED-V.



~~~
-   The MED-V workspace package.

    Install the MED-V workspace by running the setup.exe program that is included in the MED-V workspace package files.
~~~

3. Закончите настройку первого раза.

   После установки рабочей области для MED-V вы сможете запустить MED-V. Запустится агент хоста MED-V. В это время вы можете либо запустить MED-V, либо запустить агент хоста MED-V позже, чтобы завершить настройку первой последующей настройки.

   Чтобы запустить агент узла MED-V, нажмите кнопку **Пуск**, выберите **все программы**, нажмите кнопку **Microsoft Enterprise Virtualization**и выберите пункт **Агент хоста MED-V**.

## Статьи по теме


[Развертывание рабочей области MED-V с помощью системы электронного распространения программного обеспечения](how-to-deploy-a-med-v-workspace-through-an-electronic-software-distribution-system.md)

[Развертывание рабочей области MED-V в образе Windows 7](how-to-deploy-a-med-v-workspace-in-a-windows-7-image.md)

[Развертывание пакета рабочих областей MED-V](deploying-the-med-v-workspace-package.md)










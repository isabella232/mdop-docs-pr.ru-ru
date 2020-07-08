---
title: Настройка образа Windows Virtual PC для MED-V
description: Настройка образа Windows Virtual PC для MED-V
author: dansimp
ms.assetid: d87a0df8-9e08-4d1e-bfb0-9dc3cebf0d28
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 11/01/2016
ms.openlocfilehash: 340754b33576651c8ba89c85f369c48c0a0ab957
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10826819"
---
# Настройка образа Windows Virtual PC для MED-V


После установки всех элементов, которые вы хотите включить в образ MED-V, вы можете настроить его для использования в Microsoft Enterprise Virtualization (MED-V) 2,0. В этом разделе приведены рекомендации по настройке образа MED-V для запуска программы установки в первый раз перед созданием пакета рабочей области для MED-V.

При первом запуске программы установки будет выполнена подготовка рабочей области MED-V для конечного пользователя. Процесс создает виртуальную машину из образа, упакованного в рабочую область MED-V, и затем запускает мини-настройку Windows на виртуальной машине. Это включает в себя выполнение как настраиваемых сценариев настройки, так и первого приложения завершения настройки FtsCompletion.exe.

Выполните указанные ниже действия, чтобы настроить изображение MED-V для первого запуска программы установки.

1. В качестве варианта вы можете сжать виртуальный жесткий диск (VHD), чтобы освободить пустое место на диске, а затем уменьшить размер виртуального жесткого диска, прежде чем продолжить настройку образа Virtual PC для Windows. Дополнительные сведения можно найти [в разделе Сжатие виртуального жесткого диска MED-V](compacting-the-med-v-virtual-hard-disk.md).

2. Настройте процесс настройки виртуальной машины.

3. Запечатайте образ MED-V с помощью Sysprep.

   **Настройка процесса настройки виртуальной машины**

4. В процессе подготовки образа для использования с MED-V вы можете настраивать различные параметры на виртуальной машине, например задавать параметры для запуска центра обновления Windows. Укажите все необходимые параметры виртуальной машины перед созданием пакета рабочей области для MED-V.

5. Перед созданием пакета рабочей области для MED-V мы рекомендуем отключить точки восстановления на виртуальной машине, чтобы не допустить неограниченного увеличения разностного диска. Дополнительные сведения можно найти в разделе Отключение [и включение восстановления системы в Windows XP](https://go.microsoft.com/fwlink/?LinkId=195927) ( https://go.microsoft.com/fwlink/?LinkId=195927) .

   **Примечание.**  
   Вы можете настроить файл Sysprep. INF, чтобы отключить точки восстановления при первом запуске программы установки. Пример настройки этого ключа GuiRunOnce можно найти в разделе Пример файла Sysprep. inf ниже.



6. Настройте процесс настройки так, чтобы вместо экрана приветствия Windows по умолчанию выполнялась мини-установка. Вы должны запустить средство Sysprep с помощью переключателя **-Mini** или установить флажок **MiniSetup** в графическом интерфейсе пользователя. Дополнительные сведения [можно найти в разделе как запечатать изображение с помощью Sysprep](#bkmk-seal).

   **Вызов файла завершения настройки в первый раз**

   1.  Исполняемый файл, именуемый FtsCompletion.exe, входит в состав установки гостевого агента MED-V. По умолчанию он находится на системном диске вашего образа MED-V в разделе **файлы программ — виртуализация классической версии Microsoft Enterprise**.

       **Важно.**  
       На последнем этапе при первом запуске программы установки необходимо запустить эту программу. Пользователь, для которого вызывается исполняемая программа, должен быть членом локальной группы администраторов гостя.



   2.  Вы можете выбрать способ вызова этой исполняемой программы, например, с помощью сценария, развернутого вместе с рабочей областью MED-V. Вы можете вызвать этот исполняемый файл в последней строке файла Sysprep. INF. Пример вызова этой исполняемой программы в файле Sysprep. inf можно найти в файле примера ниже в этом разделе.

После завершения настройки изображения MED-V вы можете запечатать его с помощью Sysprep.

<a href="" id="bkmk-seal"></a>**Запечатывание образа MED-V с помощью программы Sysprep**

1.  Программа подготовки системы (Sysprep) — это технология, которую можно использовать для выполнения установок на основе изображений во всей сети с минимальным вмешательством администратора или специалистами по ИТ-профессионалам.

2.  В среде MED-V вы можете использовать Sysprep для присвоения уникальных идентификаторов безопасности (SID) и других параметров для каждой рабочей области MED-V при первом запуске.

    **Примечание.**  
    Дополнительные сведения об использовании Sysprep можно найти в [техническом справочнике по Sysprep](https://go.microsoft.com/fwlink/?LinkId=195930) ( https://go.microsoft.com/fwlink/?LinkId=195930) .



~~~
**Caution**  
When you use non-ASCII characters in the Sysprep.inf file, you must save the file by using the encoding appropriate for the characters entered. Windows XP expects the Sysprep.inf file to be encoded by using the code page for the language that you are targeting.

You must also make sure that the System Locale of the computers to which the MED-V workspace is deployed is set to handle the language specific characters that might be present in the Sysprep.inf file. To change the settings for the System Locale, follow these steps:

1.  To open Region and Language, click **Start**, click **Control Panel**, and then click **Region and Language**.

2.  Click the **Administrative** tab, and then click **Change System Locale** under **Language for non-Unicode programs**.

    If you are prompted for an administrator password or confirmation, type the administrator password or provide confirmation.

3.  Select your preferred language and then click **OK**.



**To configure Sysprep on the MED-V Guest Computer**

1.  Create a folder named *Sysprep* in the root of the MED-V image system drive.

2.  Download the deploy.cab file. For more information, see [Windows XP Service Pack 3 Deployment Tools](https://go.microsoft.com/fwlink/?LinkId=195928) From the Microsoft Download Center (https://go.microsoft.com/fwlink/?LinkId=195928).

3.  From the deploy.cab file, copy or extract the Setupmgr.exe, Sysprep.exe, and Setupcl.exe files to the Sysprep folder.

4.  In the Sysprep folder, run **Setup Manager** (Setupmgr.exe) to create a Sysprep.inf answer file.

    Or, you can create this file manually or use your company’s existing file. For more information, see [How to use the Sysprep tool to automate successful deployment of Windows XP](https://go.microsoft.com/fwlink/?LinkId=195929) (https://go.microsoft.com/fwlink/?LinkId=195929).

5.  Follow the **Setup Manager** wizard.

    **Important**  
    You must configure the MED-V guest to join a domain that lets users log on by using the credentials that they use to log on to the MED-V host.



    **Caution**  
    When you configure a proxy account for joining virtual machines to the domain, know that it is possible for an end user to obtain the proxy account credentials. Take all the necessary security precautions to minimize risk, such as limiting account user rights. For more information about security concerns when you configure a Windows Virtual PC image for MED-V, see [Security Best Practices for MED-V Operations](security-best-practices-for-med-v-operations.md).



    If end users must provide information during the first time setup process based on the parameters specified in the Sysprep.inf file, you must also specify that first time setup is run in **Attended** mode when you are creating your MED-V workspace package. If no information will be required from the end user, you can specify that first time setup is run in **Unattended** mode when you are creating your MED-V workspace package. For more information, see [Create a MED-V Workspace Package](create-a-med-v-workspace-package.md).

    Although you can specify any settings that you prefer, a MED-V best practice is that you create the Sysprep.inf file so that first time setup can be run in **Unattended** mode. This requires that you provide all of the required settings information as you continue through the **Setup Manager** wizard.

    **Caution**  
    If you have set a local policy or registry entry to include a service level agreement (SLA) in your image (VHD), you must specify that first time setup is run in **Attended** mode or first time setup will fail. Or, a MED-V best practice is to enforce the SLA through Group Policy later so that the SLA is displayed to the end user after first time setup is finished.



    **Note**  
    You can configure the MED-V workspace to set certain Sysprep.inf settings based on the configuration of the host and the identity of the end user. For more information, see [Create a MED-V Workspace Package](create-a-med-v-workspace-package.md).



6.  Seal the MED-V image.

    **Important**  
    We recommend that you make a backup copy of the MED-V image before sealing it.



    After you have completed all the steps in the **Setup Manager** wizard, you are ready to run Sysprep to seal the MED-V image.

**To run Sysprep**

1.  Run the System Preparation Tool (Sysprep.exe) from the *Sysprep* folder that you created when you configured Sysprep in the MED-V virtual machine.

2.  In the warning message box that appears, click **OK**.

3.  In the **Options** dialog box, select the **Don't reset grace period for activation** and **Use Mini-Setup** check boxes. Also, make sure that the **Shutdown mode** box is set to **Shut down**.

4.  Click **Reseal**. This removes identity information and clears event logs to prepare for first time setup.

5.  If you are not satisfied with the information listed in the confirmation message box that appears, click **Cancel** and then change the selections.

6.  Click **OK** to complete the system preparation process.

After you have run Sysprep on your MED-V image, the virtual machine shuts down and is ready for use in creating a MED-V workspace.
~~~

## Пример.


Ниже приведен пример файла Sysprep. INF.

``` syntax
;SetupMgrTag
[GuiUnattended]
    EncryptedAdminPassword=NO
    TimeZone=10
    OEMDuplicatorstring="MED_V v2 Host"
    AdminPassword="administrator"
    AutoLogon=Yes
    AutoLogonCount=1
    OEMSkipRegional=1
    OemSkipWelcome=1

[UserData]
    ProductKey=
    FullName="MED-V User"
    OrgName="Contoso"
    ComputerName=*

[Identification]
    JoinDomain=domain.corp.contoso.com
    DomainAdmin=UserName
    DomainAdminPassword=Password

[Networking]
    InstallDefaultComponents=Yes

[Branding]
    BrandIEUsingUnattended=Yes

[Proxy]
    Proxy_Enable=0
    Use_Same_Proxy=0

[Unattended]
    InstallFilesPath=C:\sysprep\i386
    TargetPath=\WINDOWS
    UpdateServerProfileDirectory=1
    OemSkipEula=Yes

[RegionalSettings]
    LanguageGroup=1
    Language=00000409

[GuiRunOnce]
    Command0="wmic /namespace:\\root\default path SystemRestore call Disable %SystemDrive%\"
    Command1="c:\Program Files\Microsoft Enterprise Desktop Virtualization\FtsCompletion.exe"

[sysprepcleanup]
```

## Статьи по теме


[Создание пакета рабочих областей MED-V](create-a-med-v-workspace-package.md)

[Подготовка образа MED-V](prepare-a-med-v-image.md)










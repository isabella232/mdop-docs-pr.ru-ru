---
title: Создание пакета рабочих областей MED-V
description: Создание пакета рабочих областей MED-V
author: dansimp
ms.assetid: 3f75fe73-41ac-4389-ae21-5efb2d437f4d
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: e20cf4cc9394c4a5e90178fff4fc36ed83c12d60
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10823262"
---
# Создание пакета рабочих областей MED-V


Рабочая область MED-V — это настольная среда Windows XP, в которой пользователи взаимодействуют с виртуальной машиной, предоставляемой MED-V. Администратор создает и настроит рабочую область MED-V. Рабочая область состоит из изображения и групповой политики, определяющей правила и функциональные возможности рабочей области MED-V.

Вы можете создать несколько рабочих областей для MED-V, каждый из которых настроен с помощью собственной конфигурации, параметров и правил. Пользователи, группы или несколько пользователей или групп могут быть связаны с каждой рабочей областью MED-V. Настройка делает рабочую область MED-V доступной только для этого пользователя или группы.

Использование **диспетчера рабочих областей med-v** для создания рабочих областей med-v. **Диспетчер рабочих областей MED-V** делится на два основных раздела:

-   Главная панель, содержащая три кнопки, которые используются для создания рабочих областей MED-V и управления ими. Кнопка " **создать пакет рабочей области для MED-v** " открывает **Мастер создания пакета рабочей области** для MED-v, который используется для создания рабочих областей med-v.

-   **Центр справки** в правой части окна, в котором содержатся сведения и рекомендации по созданию, тестированию и управлению рабочими областями MED-V.

**Важно.**  
Прежде чем вы сможете использовать **Диспетчер рабочих областей MED-V**, сначала убедитесь, что для политики выполнения Windows PowerShell задано значение "неограниченный".

`Set-ExecutionPolicy Unrestricted`

Кроме того, политика SAN для компьютера, на котором запускается **Диспетчер рабочих областей MED-V** , должна иметь значение "в сети". Чтобы проверить настройку политики SAN, выполните следующие команды в командной строке с учетными данными администратора.

`diskpart.exe`

`DISKPART> san`

`DISKPART> exit`

При необходимости измените политику SAN на "в сети", введя указанные ниже команды в командной строке с учетными данными администратора.

`diskpart.exe`

`DISKPART> san policy=onlineall`

`DISKPART> exit`



**Важно.**  
Если на компьютере, с которого вы подключаетесь к виртуальному жесткому диску и собрано приложение MED-V, необходимо отключить автоматическое шифрование дисков, прежде чем приступить к работе. В противном случае вы не сможете использовать рабочую область MED-V на любом другом компьютере.



Предоставленные здесь сведения помогут вам создать пакет развертывания рабочей области для MED-V.

## <a href="" id="bkmk-prereq"></a>Предварительные условия


Прежде чем приступить к созданию пакета развертывания рабочей области для MED-V, убедитесь в том, что у вас есть доступ к следующим элементам:

-   **Подготовленный образ Windows XP**

    Дополнительные сведения о том, как создать образ Windows XP для использования в MED-V, можно найти в статье [Подготовка образа MED-v](prepare-a-med-v-image.md).

-   **Текстовый файл или список, содержащий сведения о перенаправлении URL-адреса**

    В текстовом файле или списке перенаправления URL-адресов находятся URL-адреса, которые нужно перенаправлять с главного компьютера в Internet Explorer в рабочей области MED-V. Если вы используете мастер упаковки для создания рабочей области для MED-V, импортируйте, введите (или скопируйте и вставьте) эти сведения о перенаправлении как один из шагов процесса создания пакета.

    **Примечание.**  
    Перенаправление URL-адресов в MED-V поддерживает только протоколы HTTP и HTTPS. MED-V не обеспечивает поддержку FTP или других протоколов.



~~~
Enter each web address on a single line, for example:

http://www.contoso.com/webapps/webapp1

http://www.contoso.com/webapps/webapp2

http://\*.contoso.com

http://www.contoso.com/webapps/\*

**Important**  
If you import a text file that includes a URL that uses special characters (such as ~ ! @ \# and so on), make sure that you specify UTF-8 encoding when you save the text file. Special characters do not import correctly into the MED-V Workspace Packager if the text file was saved using the default ANSI encoding.
~~~



## Упаковка рабочей области для MED-V на язык, отличный от языка компьютера с диспетчером рабочих областей MED-V


По умолчанию в рабочей области MED-V поддерживаются символы как на языке компьютера, так и на английском. Чтобы создать рабочую область для MED-V на языке, отличном от установленного на компьютере, в сценарии PowerShell (PS1) после имени рабочей области для MED-V введите **-Loc \ [locale \]** .

Чтобы создать пакет рабочей области для MED-V на языке, отличном от языка по умолчанию на компьютере с диспетчером рабочих областей MED-V, создайте сценарий на языке по умолчанию, запустив диспетчер рабочих областей MED-V и изменив сценарий вывода нужным образом для вашего языкового стандарта. Сценарий находится в каталоге выходных данных рабочей области MED-V, который был указан во время упаковки. Названия региональных параметров находятся в. WXL файлы в следующем каталоге:

C:\\program Files Files\\Microsoft Enterprise для настольных компьютеров Virtualization\\WindowsPowerShell\\Modules\\Microsoft.Medv.Administration.Commands.WorkspacePackager\\locale

## Создание пакета рабочей области для MED-V


Чтобы создать пакет рабочей области для MED-V, выполните указанные ниже действия.

****

1.  Чтобы открыть **Диспетчер рабочих областей MED-V**, нажмите **кнопку Пуск**, выберите **все программы**, а затем — **Microsoft Enterprise Virtualization**, а затем — **Диспетчер рабочих областей med-v**.

2.  На главной панели **диспетчера рабочих областей med-v** щелкните **создать пакет рабочей области для MED-v**.

    Откроется **Мастер создания пакета рабочей области для MED** -v (MED). Мастер состоит из следующих страниц:

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <tbody>
    <tr class="odd">
    <td align="left"><p><strong>Сведения о пакете</strong></p></td>
    <td align="left"><p>Укажите имя рабочей области MED-V и выберите папку, в которой хранятся файлы пакета рабочей области для MED-V.</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><strong>Выбор образа Windows XP</strong></p></td>
    <td align="left"><p>Укажите свой подготовленный образ Virtual PC для Windows XP.</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><strong>Установка первого раза</strong></p></td>
    <td align="left"><p>Укажите процесс настройки, заданный для MED-V, при первом запуске программы установки.</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><strong>Сообщения MED-V</strong></p></td>
    <td align="left"><p>Укажите сообщения и Необязательный URL-адрес для справочной информации, которую конечный пользователь видит при первом запуске программы установки.</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><strong>Именование компьютеров</strong></p></td>
    <td align="left"><p>Укажите, как называется виртуальная машина MED-V.</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><strong>Копирование параметров с узла</strong></p></td>
    <td align="left"><p>Укажите, как определяются параметры рабочей области для MED-V.</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><strong>Запуск и работа в сети</strong></p></td>
    <td align="left"><p>Укажите параметры для запуска рабочей области MED-V, сети и учетных данных пользователя.</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><strong>Перенаправление веб-сайта</strong></p></td>
    <td align="left"><p>Укажите текстовый файл или список URL-адресов, которые нужно перенаправлять в Internet Explorer в рабочей области MED-V.</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><strong>Краткий обзор</strong></p></td>
    <td align="left"><p>Проверьте параметры рабочей области для MED-V и начните создавать пакет развертывания для рабочей области MED-V.</p></td>
    </tr>
    </tbody>
    </table>



3.  На странице **сведения о пакете** введите имя рабочей области MED-v и выберите папку, в которой хранятся файлы пакета рабочей области для MED-v.

    **Warning**  
    Необходимо присвоить имя рабочей области MED-V и указать папку для продолжения.



~~~
After you have finished, click **Next**.
~~~

4. На странице " **Выбор образа Windows XP** " укажите расположение готового образа виртуального компьютера для Windows XP (VHD-файла).

   **Warning**  
   Чтобы продолжить, необходимо задать VHD-образ Windows XP.



~~~
After you have finished, click **Next**.
~~~

5. На странице "Настройка" в **первый раз** выберите, нужно ли запускать программу установки при входе в систему, а также в том случае, если вы хотите использовать рабочую область MED-V отдельно или для всех конечных пользователей на компьютере с общим доступом.

   Если вы выберете параметр **Автоматическая установка без уведомления**, конечные пользователи не уведомляются, пока не будет запущена программа установки, и виртуальная машина не отображается для конечных пользователей при первом запуске программы установки. Кроме того, страница " **Сообщения MED-V** " мастера скрыта, так как при первом запуске программы установки в автоматическом режиме не требуется никаких сообщений.

   Если вы выберете параметр **Автоматическая установка, но уведомлять конечных пользователей перед первой попыткой настройки**, конечные пользователи будут уведомлены до начала настройки. Однако виртуальная машина не отображается для конечного пользователя при первом запуске программы установки.

   Выберите пункт **Ручная настройка** , если пользователь должен ввести данные при первом запуске программы.

   По умолчанию используется **Автоматическая установка, но уведомление конечных пользователей перед первой повременной настройкой**.

   **Осторожны**  
   Если файл Sysprep. INF создан таким образом, что для завершения работы мини-установки требуется ввод данных пользователем, необходимо выбрать параметр невозможная **Настройка** или проблемы при первом запуске программы установки.



~~~
You can also specify how a MED-V workspace is used on computers that are shared by multiple end users. You can decide that you want to create a unique MED-V workspace for each end user or that you want the MED-V workspace made available to all end users who share the computer. The default is that the MED-V workspace is unique for each end user.

**Important**  
We recommend that you disable the fast user switching feature in Windows if you configure the MED-V workspace to be accessed by all users on a shared computer. Problems can occur if an end user logs on by using the fast user switching feature in Windows when another user is still logged on.



**Tip**  
When you create a name mask for the MED-V workspace on the **Naming Computers** page, make sure that each virtual machine on a shared computer has a unique computer name.



You can also specify whether the MED-V workspace is added to the Administrators group or administrator credentials are managed outside MED-V. By default, the MED-V workspace is not automatically added to the Administrators group.

After you have finished, click **Next**.
~~~

6. На странице **Сообщения MED-V** укажите следующие сообщения, которые будет видеть конечный пользователь при первом запуске программы установки:

   -   Сообщение, которое пользователь видит при первом запуске программы установки.

   -   Сообщение, которое пользователь видит при возникновении ошибки при первом запуске программы установки.

   **Примечание.**  
   Страница **сообщений MED-V** в мастере скрыта, если вы выбрали параметр **Автоматическая установка без уведомления** на странице **настройки в первый раз** .



~~~
You can also specify an optional URL location for help information that is provided to the end user when first time setup is running.

For example, the URL can point to an internal IT webpage with answers to questions such as "How long will this take and how will I know when it has completed?" or "What do you do if you get an error message?"

**Note**  
If you specify a URL, a link is shown during first time setup that points the end user to this help information. If you do not specify a URL, no link is provided.



After you have finished, click **Next**.
~~~

7. На странице **именование компьютеров** вы можете указать, следует ли управлять именованием компьютеров с помощью MED-V или с помощью средства управления системой (например, Sysprep). По умолчанию имя компьютера управляется средством управления системой.

   Если вы указали, что именование компьютеров управляется MED-V, выберите в раскрывающемся списке предопределенное соглашение об именовании компьютеров (маска). На экране появится образец имени компьютера, основанный на компьютере, который вы используете для создания пакета рабочей области для MED-V.

   Если вы выбрали один из настраиваемых соглашений об именовании, поля, которые можно указать, ограничиваются следующими символами:

   -   Поля "префикс" и "суффикс" ограничены символами A-Z, a-z, 0-9 и специальными знаками! @ \ # $% ^ & ()-\ _ ' {}. и ~.

   -   Поля hostname и username ограничены цифрами от 0 до 9.

   **Важно.**  
   Имена компьютеров должны быть уникальными и содержать не более 15 символов. Если вы решите наименование компьютеров, разрешите конечные пользователи, у которых есть несколько компьютеров или общий доступ к компьютеру, и не используйте маски имен компьютеров, которые могут привести к конфликтам в сети.



~~~
**Caution**  
The computer name settings that you specify on this page override those specified in the Sysprep.inf answer file.



After you have finished, click **Next**.
~~~

8. На странице " **копирование параметров с узла** " можно выбрать следующие параметры, чтобы указать, как настроена Рабочая область MED-V.

   **Осторожны**  
   Параметры, которые вы задаете на этой странице, копируются из главного компьютера в рабочую область MED-V, переопределяя те из них, которые указаны в файле ответов Sysprep. INF.



~~~
<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><strong>Copy regional settings</strong></p></td>
<td align="left"><p>Select this check box to copy the regional settings from the host computer to the MED-V workspace.</p></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p>If you select this check box, the following settings are set in the Sysprep.inf file:</p>
<pre class="syntax" space="preserve"><code>[RegionalSettings]
Language
SystemLocale
UserLocale
UserLocale_DefaultUser
InputLocale
InputLocale_DefaultUser
</code></pre></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>Copy user settings</strong></p></td>
<td align="left"><p>Select this check box to copy certain user settings, such as user name and company name, from the host to the MED-V workspace.</p></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p>If you select this check box, the following settings are set in the Sysprep.inf file:</p>
<pre class="syntax" space="preserve"><code>[UserData]
OrgName
FullName</code></pre>
<div class="alert">
<strong>Note</strong>  
<p>Personal settings, such as Internet browsing history, are not copied over to the MED-V workspace.</p>
</div>
<div>

</div></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>Copy domain name</strong></p></td>
<td align="left"><p>Select this check box to let the guest join the same domain as the host.</p></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><div class="alert">
<strong>Important</strong>  
<p>The MED-V guest must be configured to join a domain that lets users log on by using the credentials that they use to log on to the MED-V host.</p>
</div>
<div>

</div></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>Copy domain organizational unit</strong></p></td>
<td align="left"><p>Select this check box to copy the domain organizational unit from the host computer to the MED-V workspace. This check box is only enabled if you select to copy the domain name from the host computer.</p></td>
</tr>
</tbody>
</table>



After you have finished, click **Next**.
~~~

9. На странице **Загрузка и** работа с сетью вы можете изменить поведение по умолчанию для указанных ниже параметров.

   <table>
   <colgroup>
   <col width="50%" />
   <col width="50%" />
   </colgroup>
   <tbody>
   <tr class="odd">
   <td align="left"><p><strong>Запуск рабочей области для MED-V</strong></p></td>
   <td align="left"><p>Укажите, следует ли запускать рабочую область MED-V при входе пользователя в систему, при первом использовании или разрешить конечному пользователю при запуске рабочей области MED-V.</p></td>
   </tr>
   <tr class="even">
   <td align="left"><p></p></td>
   <td align="left"><p>Рабочая область MED-V запускается одним из двух способов: при входе пользователя в систему или при первом запуске действия, требующего MED-V (например, при открытии опубликованного приложения или вводе URL-адреса, требующего перенаправления).</p>
   <p>Вы можете задать этот параметр для конечного пользователя или позволить конечному пользователю управлять тем, как запустится MED-V.</p>
   <div class="alert">
   <strong>Примечание.</strong><br/><p>Если вы указали, что конечный пользователь решает проблему, поведение по умолчанию — Рабочая область MED-V запускается при входе в систему. Они могут изменить значение по умолчанию, щелкнув правой кнопкой мыши значок MED-V в области уведомлений и выбрав пункт <strong> Параметры пользователя MED-v </strong> . Если вы определили этот параметр для конечного пользователя, он не сможет изменить способ запуска MED-V.</p>
   </div>
   <div>

   </div></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><strong>Сеть</strong></p></td>
   <td align="left"><p>Выберите <strong> параметр Общий доступ </strong> или <strong> мост </strong> для сети. Значение по умолчанию — <strong> Shared </strong> .</p></td>
   </tr>
   <tr class="even">
   <td align="left"><p></p></td>
   <td align="left"><p><strong>Общая </strong> - Рабочая область для MED-V использует преобразование сетевых адресов (NAT) для предоставления общего доступа к узлу&#39;s IP для исходящего трафика.</p>
   <p><strong>В мост </strong> - для рабочей области MED-V есть собственный сетевой адрес, обычно получаемый с помощью DHCP.</p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><strong>Хранение учетных данных</strong></p></td>
   <td align="left"><p>Укажите, нужно ли хранить учетные данные конечного пользователя.</p></td>
   </tr>
   <tr class="even">
   <td align="left"><p></p></td>
   <td align="left"><p>По умолчанию хранение учетных данных отключено, так что конечный пользователь должен пройти проверку подлинности при каждом входе.</p>
   <div class="alert">
   <strong>Важно.</strong><br/><p>Несмотря на то, что кэширование учетных данных конечного пользователя обеспечивает наилучшее взаимодействие с пользователем, следует учитывать риски, связанные с этим.</p>
   <p>Учетные данные домена конечного пользователя хранятся в диспетчере учетных данных Windows в обратимом формате. В результате злоумышленник может написать программу, которая извлекает пароль и может получить доступ к учетным данным пользователя. Вы можете уменьшить этот риск, отключив хранение учетных данных конечного пользователя.</p>
   </div>
   <div>

   </div></td>
   </tr>
   </tbody>
   </table>



~~~
After you have finished, click **Next**.
~~~

10. На странице **Переадресация веб-сайта** можно ввести, вставить или импортировать список URL-адресов, перенаправленных в Internet Explorer в рабочей области MED-V. Дополнительные сведения о том, как настроить перенаправление URL-адресов, можно найти в разделе [Предварительные требования](#bkmk-prereq).

   Вы также можете указать, как Internet Explorer в рабочей области MED-V настроен для конечных пользователей. По умолчанию для зоны Интернета установлен высокий уровень безопасности. Кроме того, некоторые возможности просмотра по умолчанию, такие как адресная строка, удаляются. Эта конфигурация Internet Explorer по умолчанию в рабочей области MED-V обеспечивает более безопасную среду просмотра для конечных пользователей.

   **Осторожны**  
   Изменяя параметры по умолчанию, вы можете настроить Internet Explorer в рабочей области для MED-V. Тем не менее, если вы измените параметры по умолчанию так, чтобы они были менее надежными, вы можете предоставить своей организации угрозу безопасности, которые присутствуют в более ранних версиях Internet Explorer. Дополнительные сведения можно найти в разделе Советы и [рекомендации по обеспечению безопасности при работе с MED-V](security-best-practices-for-med-v-operations.md).



~~~
After you have finished, click **Next**.
~~~

11. На странице **сводки** вы можете просмотреть параметры упаковки для этой рабочей области MED-V. Если вы хотите изменить параметры, нажмите кнопку " **назад** ", чтобы вернуться к нужной странице. После того как вы закончите просмотр параметров, нажмите кнопку **создать**.

   Откроется страница **завершения** **мастера создания пакета рабочей области для MED-V** , чтобы показать ход выполнения создания пакета.

   **Примечание.**  
   Процесс создания пакета рабочей области MED-V может занять несколько минут в зависимости от размера указанного виртуального жесткого диска.



~~~
If the MED-V workspace package is created successfully, the **Completion** page displays a list of the files that you created and their respective locations. The following is a list of the files that are created and their descriptions:

-   **setup.exe**—an installation program that you deploy and run on end-user computers to install the MED-V workspaces.

-   **&lt;*workspace\_name*&gt;.msi**—an installer file that you deploy to the end-user computers. The setup.exe file will run this file to install the MED-V workspaces.

-   **&lt;*vhd\_name*&gt;.medv**—a compressed VHD file that you deploy to the end-user computers. The setup.exe file uses it when it installs the MED-V workspaces.

-   **&lt;*workspace\_name*&gt;.reg**—the configuration settings that are installed when the setup.exe, &lt;*workspace\_name*&gt;.msi, and &lt;*vhd\_name*&gt;.medv files are deployed and setup.exe is run.

-   **&lt;*workspace\_name*&gt;.ps1**—a Windows PowerShell script that you can use to rebuild the registry file and re-build the MED-V workspace package.

    **Important**  
    Before deployment, you can edit configuration settings by updating the .ps1 file that has your preferred method of script editing, such as Windows PowerShell. After you change the .ps1 file, use that file to rebuild the MED-V workspace package that you deploy to your enterprise. For more information, see [Configuring Advanced Settings by Using Windows PowerShell](configuring-advanced-settings-by-using-windows-powershell.md).

    However, after the MED-V workspace is deployed, you must edit configuration settings through the registry. For a list and description of the configuration settings, see [Managing MED-V Workspace Configuration Settings](managing-med-v-workspace-configuration-settings.md).
~~~



12. Нажмите кнопку **Закрыть** , чтобы закрыть мастер упаковки и вернуться в **Диспетчер рабочих областей MED-V**.

Пакет рабочей области для MED-V теперь готов к тестированию перед развертыванием.

## Статьи по теме


[Настройка дополнительных параметров с помощью Windows PowerShell](configuring-advanced-settings-by-using-windows-powershell.md)

[Тестирование пакета рабочих областей MED-V](testing-the-med-v-workspace-package.md)

[Подготовка образа MED-V](prepare-a-med-v-image.md)










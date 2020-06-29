---
title: Установка программного обеспечения MBAM 2.5 Server
description: Установка программного обеспечения MBAM 2.5 Server
author: dansimp
ms.assetid: b9dbe697-5400-4bac-acfb-ee6dc6586c30
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 6612bf52aa53ae693694d7ac02c5cab212d4e24f
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10823392"
---
# Установка программного обеспечения MBAM 2.5 Server


В этой статье описано, как установить серверное программное обеспечение Microsoft BitLocker Administration и Monitoring (MBAM) 2,5 с помощью мастера настройки администрирования и мониторинга Microsoft BitLocker либо с помощью параметров командной строки. Повторите процесс установки сервера для каждого сервера, на котором вы настраиваете MBAM 2,5 компонентов сервера. После завершения установки ознакомьтесь со статьей [Настройка сервера MBAM 2,5](configuring-the-mbam-25-server-features.md) для настройки функций сервера.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Прежде чем начать</th>
<th align="left">Описание</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Ознакомьтесь со сведениями о планировании MBAM 2,5</p></td>
<td align="left"><ul>
<li><p><a href="mbam-25-server-prerequisites-for-stand-alone-and-configuration-manager-integration-topologies.md" data-raw-source="[MBAM 2.5 Server Prerequisites for Stand-alone and Configuration Manager Integration Topologies](mbam-25-server-prerequisites-for-stand-alone-and-configuration-manager-integration-topologies.md)">Необходимые условия MBAM 2.5 Server для изолированной топологии и топологии интеграции диспетчера конфигураций</a></p></li>
<li><p><a href="mbam-25-supported-configurations.md" data-raw-source="[MBAM 2.5 Supported Configurations](mbam-25-supported-configurations.md)">Поддерживаемые конфигурации MBAM 2.5</a></p></li>
<li><p><a href="high-level-architecture-for-mbam-25.md" data-raw-source="[High-Level Architecture for MBAM 2.5](high-level-architecture-for-mbam-25.md)">Высокоуровневая архитектура для MBAM 2.5</a></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p>Сведения о получении файлов журнала</p></td>
<td align="left"><p>По умолчанию файлы журнала создаются в папке% Temp% локального компьютера. Чтобы создать файлы журнала в определенном месте, а не в <strong> папке% temp </strong> %, используйте <strong> </strong> &lt; <em> аргумент расположение/log </em> &gt; .</p>
<p>В журнале событий приложений и служб в Microsoft Windows регистрируются дополнительные события, которые могут быть занесены в журнал в <strong> MBAM- </strong> или <strong> MBAM-веб- </strong> узлы <strong> &gt; &gt; </strong> . Например, если вы удалите MBAM, программа удаления также удалит журналы MBAM-Setup и MBAM-Web в EventViewer.</p></td>
</tr>
</tbody>
</table>

 

## Установка программного обеспечения сервера MBAM 2,5 с помощью мастера настройки администрирования и мониторинга Microsoft BitLocker


Выполните указанные ниже действия, чтобы установить программное обеспечение сервера MBAM с помощью мастера настройки администрирования и мониторинга Microsoft BitLocker.

**Установка программного обеспечения сервера MBAM 2,5 с помощью мастера**

1.  На сервере, на котором вы хотите установить MBAM, запустите мастер настройки администрирования и наблюдения за помощью **MBAMserversetup.exe** Microsoft BitLocker.

2.  На странице **приветствия** нажмите кнопку **Далее**.

3.  Прочтите и подтвердите условия лицензионного соглашения на использование программного обеспечения корпорации Майкрософт, а затем нажмите кнопку **Далее** , чтобы продолжить установку.

4.  Укажите, следует ли использовать Microsoft Update при проверке обновлений, а затем нажмите кнопку **Далее**.

5.  Укажите, нужно ли принимать участие в программе улучшения качества программного обеспечения, и нажмите кнопку **Далее**.

6.  Чтобы начать установку, нажмите кнопку **установить**.

7.  Чтобы настроить компоненты сервера после завершения установки программного обеспечения сервера MBAM, установите флажок **выполнить настройку сервера MBAM после закрытия окна мастера** . Кроме того, вы можете настроить MBAM позже с помощью ярлыка **конфигурации сервера MBAM** , который будет создан при установке сервера в меню " **Пуск** ".

8.  Нажмите кнопку **Готово**.

## Установка программного обеспечения сервера MBAM 2,5 с помощью окна командной строки


Чтобы установить программное обеспечение сервера MBAM, в командной строке введите команду примерно так, как показано в следующей команде.

``` syntax
MbamServerSetup.exe MBAMServerInstall.log
CEIPENABLED=True OPTIN_FOR_MICROFOST_UPDATES=True INSTALLDIR=c:\mbaminstall
```

В приведенной ниже таблице описаны параметры командной строки для установки программного обеспечения сервера MBAM 2,5.

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Параметр</th>
<th align="left">Значение параметра</th>
<th align="left">Описание</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>CEIPENABLED</p></td>
<td align="left"><p>Истина ложь</p></td>
<td align="left"><p>Истина — участие в программе улучшения качества программного обеспечения, которая помогает корпорации Майкрософт определить, какие функции MBAM нужно улучшить.</p>
<p>Ложь – не принимать участие в программе улучшения качества программного обеспечения.</p></td>
</tr>
<tr class="even">
<td align="left"><p>OPTIN_FOR_MICROSOFT_UPDATES</p></td>
<td align="left"><p>Истина ложь</p></td>
<td align="left"><p>Истина — используйте Microsoft Update для обеспечения безопасности и актуальности вашего компьютера для Windows и других продуктов Майкрософт, включая MBAM.</p>
<p>False — не использовать центра обновления Майкрософт</p></td>
</tr>
<tr class="odd">
<td align="left"><p>INSTALLDIR</p></td>
<td align="left"><p>&lt;Путь&gt;</p></td>
<td align="left"><p>Расположение, в которое вы хотите установить MBAM.</p>
<p>Пример.</p>
<p>INSTALLDIR = c:\mbaminstall</p></td>
</tr>
<tr class="even">
<td align="left"><p>FORCE_UNINSTALL</p></td>
<td align="left"><p>Истина ложь</p></td>
<td align="left"><p>True-продолжить процесс удаления MBAM, даже если все компоненты не будут удалены.</p>
<p>False (значение по умолчанию) Если настраиваемое действие по удалению не может удалить добавленный компонент сервера MBAM, удаление завершается сбоем и MBAM остается установленным.</p>
<p>В обоих случаях все возможности, которые были успешно удалены при попытке удалить MBAM, не удаляются.</p></td>
</tr>
</tbody>
</table>

 



## Статьи по теме


[Развертывание MBAM 2.5](deploying-mbam-25.md)

[Настройка компонентов сервера MBAM 2.5 Server](configuring-the-mbam-25-server-features.md)

 

## У вас есть предложение MBAM?
- Здесь вы можете добавить предложения и проголосовать [здесь](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring). 
- Для MBAM проблемы используйте [MBAM Форум TechNet](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam). 






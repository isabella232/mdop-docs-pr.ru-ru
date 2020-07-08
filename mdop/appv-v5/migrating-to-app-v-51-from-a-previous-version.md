---
title: Миграция на App-V 5.1 с предыдущей версии
description: Миграция на App-V 5.1 с предыдущей версии
author: dansimp
ms.assetid: e7ee0edc-7544-4c0a-aaca-d922a33bc1bb
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 7fb6ddbfed4f6fd1ae9613d2ee86361a51918a65
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10813552"
---
# Миграция на App-V 5.1 с предыдущей версии


С помощью Microsoft Application Virtualization (App-V) 5,1 вы можете перенести существующую инфраструктуру App-V 4,6 или App-V 5,0 в более гибкую, интегрированную и удобную для управления инфраструктурой App-V 5,1.
Однако вы не можете выполнить миграцию непосредственно из App-V 4. x в App-V 5,1, поэтому сначала необходимо выполнить миграцию в App-v 5,0. Дополнительные сведения о переходе с App-V 4. x на App-V 5,0 можно найти в разделе [Переход с предыдущей версии](migrating-from-a-previous-version-app-v-50.md)  

**Примечание**  Пакеты App-V 5,1 точно так же, как пакеты App-V 5,0. В разных версиях пакетов не было изменений, поэтому нет необходимости преобразовывать пакеты 5,0 App-V в пакеты App-V 5,1.

Дополнительные сведения о различиях между App-V 4,6 и App-V 5,1 приведены в **разделе различия между разделом App-v 4,6 и App-v 5,0** [о приложении app-v 5,0](about-app-v-50.md).

 

## <a href="" id="bkmk-pkgconvimprove"></a>Улучшенные возможности преобразователя пакетов для App-V 5,1


Теперь можно использовать конвертер пакетов для преобразования пакетов приложений App-V 4,6, содержащих сценарии, а также сведений реестра и сценариев из исходного OSD-файлов, которые теперь включены в выходные данные преобразователя пакетов.

Вы также можете использовать `–OSDsToIncludeInPackage` параметр с `ConvertFrom-AppvLegacyPackage` командлетом, чтобы указать, какие сведения о OSD – файлах будут преобразованы и помещены в новый пакет.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Новые возможности App-V 5,1</th>
<th align="left">До версии App-V 5,1</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Новые XML-файлы создаются в соответствии с файлами OSD, связанными с пакетом. Эти файлы содержат следующие данные:</p>
<ul>
<li><p>переменные среды</p></li>
<li><p>Горячие</p></li>
<li><p>сопоставления типов файлов</p></li>
<li><p>сведения в реестре</p></li>
<li><p>сценарии</p></li>
</ul>
<p>Теперь вы можете добавлять данные из подмножества OSD-файлов из исходного каталога в пакет с помощью <code>-OSDsToIncludeInPackage</code> параметра.</p></td>
<td align="left"><p>Данные в реестре и сценарии, включенные в OSD-файлы, связанные с пакетом, не включены в выходные данные преобразователя пакетов.</p>
<p>Преобразователь пакетов выполнит заполнение нового пакета данными из всех OSD файлов в исходном каталоге.</p></td>
</tr>
</tbody>
</table>

 

### Пример оператора преобразования

Чтобы понять, как создан новый процесс, ознакомьтесь с приведенным ниже примером `ConvertFrom-AppvLegacyPackage` инструкции преобразователя пакетов.

**Если исходный каталог (\\\\OldPkgStore\\ContosoApp) включает следующее:**

-   ContosoApp. SFT

-   ContosoApp.msi

-   ContosoApp.sprj

-   ContosoApp\_manifest.xml

-   X. OSD

-   Y. OSD

-   Z. OSD

**И выполните следующую команду:**

``` syntax
ConvertFrom-AppvLegacyPackage –SourcePath \\OldPkgStore\ContosoApp\ 
-DestinationPath \\NewPkgStore\ContosoApp\
-OSDsToIncludeInPackage X.osd,Y.osd
```

**В целевом каталоге (\\\\NewPkgStore\\ContosoApp) будет создано следующее:**

-   ContosoApp. AppV

-   ContosoApp.msi

-   ContosoApp\_DeploymentConfig.xml

-   ContosoApp\_UserConfig.xml

-   X\_Config.xml

-   Y\_Config.xml

-   Z\_Config.xml

**В приведенном выше примере:**

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Эти файлы исходного каталога...</th>
<th align="left">... преобразуются в указанные конечные файлы каталогов...</th>
<th align="left">... и будут содержать эти элементы</th>
<th align="left">Описание</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><ul>
<li><p>X. OSD</p></li>
<li><p>Y. OSD</p></li>
<li><p>Z. OSD</p></li>
</ul></td>
<td align="left"><ul>
<li><p>X_Config.xml</p></li>
<li><p>Y_Config.xml</p></li>
<li><p>Z_Config.xml</p></li>
</ul></td>
<td align="left"><ul>
<li><p>Переменные среды</p></li>
<li><p>Горячие</p></li>
<li><p>Сопоставления типов файлов</p></li>
<li><p>Сведения в реестре</p></li>
<li><p>Скрипты</p></li>
</ul></td>
<td align="left"><p>Каждый файл. OSD преобразуется в отдельный соответствующий XML-файл, который содержит указанные здесь элементы в формате конфигурации развертывания App-V 5,1. Эти элементы затем можно скопировать из этих XML-файлов и поместить в конфигурацию развертывания или файлы конфигурации пользователя по мере необходимости.</p>
<p>В этом примере три XML-файла, соответствующие трем файлам OSD, находятся в исходном каталоге. Каждый XML-файл состоит из переменных среды, ярлыков, сопоставлений типов файлов, данных реестра и сценариев в соответствующем ей файле. OSD.</p></td>
</tr>
<tr class="even">
<td align="left"><ul>
<li><p>X. OSD</p></li>
<li><p>Y. OSD</p></li>
</ul></td>
<td align="left"><ul>
<li><p>ContosoApp. AppV</p></li>
<li><p>ContosoApp_DeploymentConfig.xml</p></li>
<li><p>ContosoApp_UserConfig.xml</p></li>
</ul></td>
<td align="left"><ul>
<li><p>Переменные среды</p></li>
<li><p>Горячие</p></li>
<li><p>Сопоставления типов файлов</p></li>
</ul></td>
<td align="left"><p>Сведения из OSD файлов, указанных в <code>-OSDsToIncludeInPackage</code> параметре, преобразуются в пакет и размещаются в нем. Затем преобразователь заполняет файл конфигурации развертывания и файл конфигурации пользователя содержимым пакета, так же как программа Sequencer App-V выполняет виртуализацию нового пакета.</p>
<p>В этом примере переменные среды, сочетания клавиш и сопоставления типов файлов, включенные в X. OSD и Y. OSD, были преобразованы и помещены в пакет App-V, а некоторые из этих сведений также включены в конфигурацию развертывания и файлы конфигурации пользователя. Используются X. OSD и Y. OSD, так как они были включены в параметр в качестве аргументов <code>-OSDsToIncludeInPackage</code> . Информация из Z. OSD не включена в пакет, так как она не указана как один из этих аргументов.</p></td>
</tr>
</tbody>
</table>

 

## Преобразование пакетов, созданных с помощью более ранней версии App-V


Используйте служебную программу преобразователя пакетов для обновления пакетов виртуальных приложений, созданных с помощью версий App-V, предшествующих приложению App-V 5,0. Преобразователь пакетов использует PowerShell для преобразования пакетов и может помочь автоматизировать процесс, если у вас много пакетов, требующих преобразования.

**Важно!**  После преобразования существующего пакета необходимо протестировать его перед развертыванием пакета, чтобы убедиться, что процесс преобразования прошел успешно.

 

**Что нужно знать перед преобразованием существующих пакетов**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Проблема</th>
<th align="left">Обходной путь</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Виртуальные пакеты с использованием DSC не связаны после преобразования.</p></td>
<td align="left"><p>Свяжите пакеты с помощью групп подключений. См <a href="managing-connection-groups51.md" data-raw-source="[Managing Connection Groups](managing-connection-groups51.md)"> .: Управление группами подключений </a> .</p></td>
</tr>
<tr class="even">
<td align="left"><p>Конфликты переменных среды обнаружены во время преобразования.</p></td>
<td align="left"><p>Устраните конфликты в связанном <strong> OSD </strong> файле.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>При преобразовании обнаруживаются жестко запрограммированные пути.</p></td>
<td align="left"><p>Жестко закодированные пути очень сложны для правильного преобразования. Преобразователь пакетов обнаружит и вернет пакеты с файлами, которые содержат жестко запрограммированные пути. Просмотрите файл с жестко заданным путем и определите, требуется ли для него файл. Если это так, рекомендуется повторно выполнить повторную последовательность пакета.</p></td>
</tr>
</tbody>
</table>

 

При преобразовании проверки пакета на наличие неудачных файлов или ярлыков. Найдите элемент в пакете App-V 4,6. Возможно, он является жестко запрограммированным путем. Преобразуйте путь.

**Примечание**  Рекомендуется использовать секвенсор App-V 5,1 для преобразования критических приложений или приложений, которые должны использовать преимущества функций. Посмотрите, [как последовательное создание нового приложения с помощью App-V 5,1](how-to-sequence-a-new-application-with-app-v-51-beta-gb18030.md).

Если преобразованный пакет не открывается после его преобразования, рекомендуется также выполнить повторную последовательное индексирование приложения с помощью секвенсора App-V 5,1.

 

[Преобразование пакета, созданного в предыдущей версии App-V](how-to-convert-a-package-created-in-a-previous-version-of-app-v51.md)

## Миграция клиентов


В приведенной ниже таблице показан рекомендуемый метод обновления клиентов.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Задача</th>
<th align="left">Дополнительные сведения</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Обновите среду до последней версии App-V 4.6</p></td>
<td align="left"><p><a href="../appv-v4/application-virtualization-deployment-and-upgrade-considerations-copy.md" data-raw-source="[Application Virtualization Deployment and Upgrade Considerations](../appv-v4/application-virtualization-deployment-and-upgrade-considerations-copy.md)">Рекомендации по развертыванию и обновлению Application Virtualization </a> .</p></td>
</tr>
<tr class="even">
<td align="left"><p>Установите клиент App-V 5,1 с включенным параметром совместного существования.</p></td>
<td align="left"><p><a href="how-to-deploy-the-app-v-46-and-the-app-v--51-client-on-the-same-computer.md" data-raw-source="[How to Deploy the App-V 4.6 and the App-V 5.1 Client on the Same Computer](how-to-deploy-the-app-v-46-and-the-app-v--51-client-on-the-same-computer.md)">Развертывание приложения App-V 4,6 и клиента App-V 5,1 на том же компьютере </a> .</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Последовательное и развертывание пакетов приложения App-V 5,1. При необходимости можно отменить публикацию пакетов App-V 4,6.</p></td>
<td align="left"><p><a href="how-to-sequence-a-new-application-with-app-v-51-beta-gb18030.md" data-raw-source="[How to Sequence a New Application with App-V 5.1](how-to-sequence-a-new-application-with-app-v-51-beta-gb18030.md)">Последовательность создания нового приложения с помощью App-V 5,1 </a> .</p></td>
</tr>
</tbody>
</table>

 

**Важно!**  Для использования режима совместного существования должна быть установлена новейшая версия App-V 4.6. Кроме того, при упорядочении пакета необходимо настроить параметр управления полномочиями, который находится в **конфигурации пользователя** , в разделе **Конфигурация пользователя** .

 

## Миграция полной инфраструктуры на сервер App-V 5,1


Прямой метод для обновления до полной инфраструктуры App-V 5,1 не существует. Сведения об обновлении сервера App-V можно получить, используя сведения из следующего раздела.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Задача</th>
<th align="left">Дополнительные сведения</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Обновите среду до последней версии App-V 4.6.</p></td>
<td align="left"><p><a href="../appv-v4/application-virtualization-deployment-and-upgrade-considerations-copy.md" data-raw-source="[Application Virtualization Deployment and Upgrade Considerations](../appv-v4/application-virtualization-deployment-and-upgrade-considerations-copy.md)">Рекомендации по развертыванию и обновлению Application Virtualization </a> .</p></td>
</tr>
<tr class="even">
<td align="left"><p>Развертывание версии приложения-V 5,1 клиента.</p></td>
<td align="left"><p><a href="how-to-deploy-the-app-v-client-51gb18030.md" data-raw-source="[How to Deploy the App-V Client](how-to-deploy-the-app-v-client-51gb18030.md)">Развертывание клиента App-V </a> .</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Установите приложение App-V 5,1 Server.</p></td>
<td align="left"><p><a href="how-to-deploy-the-app-v-51-server.md" data-raw-source="[How to Deploy the App-V 5.1 Server](how-to-deploy-the-app-v-51-server.md)">Развертывание сервера App-V 5,1 </a> .</p></td>
</tr>
<tr class="even">
<td align="left"><p>Миграция существующих пакетов.</p></td>
<td align="left"><p>Ознакомьтесь с <strong> пакетами преобразования, созданными в более ранней версии раздела App-V </strong> этой статьи.</p></td>
</tr>
</tbody>
</table>

 

## Дополнительные задачи миграции


Вы также можете выполнить дополнительные задачи миграции, например повторно настроить конечные точки, а также открыть пакет, созданный с помощью более ранней версии на компьютере с клиентом App-V 5,1. Ниже приведены ссылки на дополнительные сведения о выполнении этих задач.

[Перенос точек расширения из пакета App-V 4.6 в преобразованный пакет App-V 5.1 для всех пользователей на указанном компьютере](how-to-migrate-extension-points-from-an-app-v-46-package-to-a-converted-app-v-51-package-for-all-users-on-a-specific-computer.md)

[Перенос точек расширения из пакета App-V 4.6 в App-V 5.1 для конкретного пользователя](how-to-migrate-extension-points-from-an-app-v-46-package-to-app-v-51-for-a-specific-user.md)

[Возврат точек расширения из пакета App-V 5.1 в пакет App-V 4.6 для всех пользователей на указанном компьютере](how-to-revert-extension-points-from-an-app-v-51-package-to-an-app-v-46-package-for-all-users-on-a-specific-computer.md)

[Возврат точек расширения из пакета App-V 5.1 в пакет App-V 4.6 для конкретного пользователя](how-to-revert-extension-points-from-an-app-v-51-package-to-an-app-v-46-package-for-a-specific-user.md)







## Другие ресурсы для выполнения задач миграции App-V


[Операции, связанные с администрированием и использованием App-V 5.1](operations-for-app-v-51.md)

[Упрощенная процедура обновления сервера управления для Microsoft App-V 5,1](https://go.microsoft.com/fwlink/p/?LinkId=786330)

 

 






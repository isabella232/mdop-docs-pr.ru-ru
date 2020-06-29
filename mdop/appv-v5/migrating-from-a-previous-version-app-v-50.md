---
title: Перенос из предыдущей версии
description: Перенос из предыдущей версии
author: dansimp
ms.assetid: a13cd353-b22a-48f7-af1e-5d54ede2a7e5
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: a05bbd498cdb77a1ddf694b1aab6aeb42124775b
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10813557"
---
# Перенос из предыдущей версии


С помощью App-V 5,0 вы можете перенести существующую инфраструктуру App-V 4,6 на более гибкую, интегрированную и удобную для управления инфраструктурой App-V 5,0.

При планировании стратегии миграции учитывайте следующие разделы:

**Примечание**  Дополнительные сведения о различиях между App-V 4,6 и App-V 5,0 приведены в **разделе различия между разделом App-v 4,6 и App-v 5,0** [о приложении app-v 5,0](about-app-v-50.md).

 

## Преобразование пакетов, созданных с помощью более ранней версии App-V


Используйте служебную программу преобразователя пакетов, чтобы обновить пакеты виртуальных приложений, созданные в предыдущих версиях App-V. Преобразователь пакетов использует PowerShell для преобразования пакетов и может помочь автоматизировать процесс, если у вас много пакетов, требующих преобразования.

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
<td align="left"><p>Сценарии пакетов не преобразуются.</p></td>
<td align="left"><p>Протестируйте преобразованный пакет. При необходимости преобразуйте сценарий.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Переопределение параметров реестра пакета не преобразуется.</p></td>
<td align="left"><p>Протестируйте преобразованный пакет. При необходимости повторно добавьте переопределения в реестре.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Виртуальные пакеты с использованием DSC не связаны после преобразования.</p></td>
<td align="left"><p>Свяжите пакеты с помощью групп подключений. См <a href="managing-connection-groups.md" data-raw-source="[Managing Connection Groups](managing-connection-groups.md)"> .: Управление группами подключений </a> .</p></td>
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

 

При преобразовании проверки пакета на наличие неудачных файлов или ярлыков. Найдите элемент в пакете App-V 4,6. Возможно, это будет жестко запрограммированный путь. Преобразуйте путь.

**Примечание**  Рекомендуется использовать секвенсор App-V 5,0 для преобразования критических приложений или приложений, которые должны использовать преимущества функций. Посмотрите, [как последовательное создание нового приложения с помощью App-V 5,0](how-to-sequence-a-new-application-with-app-v-50-beta-gb18030.md).

Если преобразованный пакет не открывается после его преобразования, рекомендуется также выполнить повторную последовательное индексирование приложения с помощью секвенсора App-V 5,0.

 

[Преобразование пакета, созданного в предыдущей версии App-V](how-to-convert-a-package-created-in-a-previous-version-of-app-v.md)

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
<td align="left"><p>Обновите среду до App-V 4.6 SP2</p></td>
<td align="left"><p><a href="../appv-v4/application-virtualization-deployment-and-upgrade-considerations-copy.md" data-raw-source="[Application Virtualization Deployment and Upgrade Considerations](../appv-v4/application-virtualization-deployment-and-upgrade-considerations-copy.md)">Рекомендации по развертыванию и обновлению Application Virtualization </a> .</p></td>
</tr>
<tr class="even">
<td align="left"><p>Установите клиент App-V 5,0 с включенным параметром совместного существования.</p></td>
<td align="left"><p><a href="how-to-deploy-the-app-v-46-and-the-app-v--50-client-on-the-same-computer.md" data-raw-source="[How to Deploy the App-V 4.6 and the App-V 5.0 Client on the Same Computer](how-to-deploy-the-app-v-46-and-the-app-v--50-client-on-the-same-computer.md)">Развертывание приложения App-V 4,6 и клиента App-V 5,0 на том же компьютере </a> .</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Последовательное и развертывание пакетов приложения App-V 5,0. При необходимости можно отменить публикацию пакетов App-V 4,6.</p></td>
<td align="left"><p><a href="how-to-sequence-a-new-application-with-app-v-50-beta-gb18030.md" data-raw-source="[How to Sequence a New Application with App-V 5.0](how-to-sequence-a-new-application-with-app-v-50-beta-gb18030.md)">Последовательность создания нового приложения с помощью App-V 5,0 </a> .</p></td>
</tr>
</tbody>
</table>

 

**Важно!**  Для использования режима сосуществования необходимо, чтобы на компьютере было запущено приложение App-V 4.6 SP3. Кроме того, при упорядочении пакета необходимо настроить параметр управления полномочиями, который находится в **конфигурации пользователя** , в разделе **Конфигурация пользователя** .

 

## Миграция полной инфраструктуры на сервер App-V 5,0


Прямой метод для обновления до полной инфраструктуры App-V 5,0 не существует. Сведения об обновлении сервера App-V можно получить, используя сведения из следующего раздела.

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
<td align="left"><p>Обновите среду до App-V 4.6 SP3.</p></td>
<td align="left"><p><a href="../appv-v4/application-virtualization-deployment-and-upgrade-considerations-copy.md" data-raw-source="[Application Virtualization Deployment and Upgrade Considerations](../appv-v4/application-virtualization-deployment-and-upgrade-considerations-copy.md)">Рекомендации по развертыванию и обновлению Application Virtualization </a> .</p></td>
</tr>
<tr class="even">
<td align="left"><p>Развертывание версии приложения-V 5,0 клиента.</p></td>
<td align="left"><p><a href="how-to-deploy-the-app-v-client-gb18030.md" data-raw-source="[How to Deploy the App-V Client](how-to-deploy-the-app-v-client-gb18030.md)">Развертывание клиента App-V </a> .</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Установите приложение App-V 5,0 Server.</p></td>
<td align="left"><p><a href="how-to-deploy-the-app-v-50-server-50sp3.md" data-raw-source="[How to Deploy the App-V 5.0 Server](how-to-deploy-the-app-v-50-server-50sp3.md)">Развертывание сервера App-V 5,0 </a> .</p></td>
</tr>
<tr class="even">
<td align="left"><p>Миграция существующих пакетов.</p></td>
<td align="left"><p>Ознакомьтесь с <strong> пакетами преобразования, созданными в более ранней версии раздела App-V </strong> этой статьи.</p></td>
</tr>
</tbody>
</table>

 

## Дополнительные задачи миграции


Вы также можете выполнить дополнительные задачи миграции, например повторно настроить конечные точки, а также открыть пакет, созданный с помощью более ранней версии на компьютере с клиентом App-V 5,0. Ниже приведены ссылки на дополнительные сведения о выполнении этих задач.

[Перенос точек расширения из пакета App-V 4.6 в преобразованный пакет App-V 5.0 для всех пользователей на указанном компьютере](how-to-migrate-extension-points-from-an-app-v-46-package-to-a-converted-app-v-50-package-for-all-users-on-a-specific-computer.md)

[Перенос точек расширения из пакета App-V 4.6 в App-V 5.0 для конкретного пользователя](how-to-migrate-extension-points-from-an-app-v-46-package-to-app-v-50-for-a-specific-user.md)

[Возврат точек расширения из пакета App-V 5.0 в пакет App-V 4.6 для всех пользователей на указанном компьютере](how-to-revert-extension-points-from-an-app-v-50-package-to-an-app-v-46-package-for-all-users-on-a-specific-computer.md)

[Возврат точек расширения из пакета App-V 5.0 в пакет App-V 4.6 для конкретного пользователя](how-to-revert-extension-points-from-an-app-v-50-package-to-an-app-v-46-package-for-a-specific-user.md)







## Другие ресурсы для выполнения задач миграции App-V


[Операции, связанные с администрированием и использованием App-V 5.0](operations-for-app-v-50.md)

[Упрощенная процедура обновления сервера управления для Microsoft App-V 5,1](https://go.microsoft.com/fwlink/p/?LinkId=786330)

 

 






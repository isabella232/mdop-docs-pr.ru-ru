---
title: Скачивание и развертывание шаблонов групповой политики MDOP (ADMX-файл)
description: Скачивание и развертывание шаблонов групповой политики MDOP (ADMX-файл)
author: dansimp
ms.assetid: fdb64505-6c66-4fdf-ad74-a6a161191e3f
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/15/2018
ms.openlocfilehash: 5bc5f8d536c113ccbc0a1931e6c7e4ed3c7a9a37
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10826919"
---
# Скачивание и развертывание шаблонов групповой политики MDOP (ADMX-файл)


С помощью шаблонов групповых политик, файлов ADMX и ADML можно управлять параметрами некоторых технологий пакета оптимизации рабочего стола (MDOP) (например, App-V, UE-V или MBAM). Шаблоны групповой политики MDOP можно загрузить в виде самораспаковывающегося распакованного сжатого файла, сгруппированных по технологиям и версиям.

## Шаблоны групповой политики MDOP

**Загрузка и развертывание шаблонов групповой политики MDOP**

1. Скачайте последние [шаблоны групповой политики MDOP](https://www.microsoft.com/download/details.aspx?id=55531) 

2. Разверните загруженный CAB-файл, выполнив `expand <download_folder>\MDOP_ADMX_Templates.cab -F:* <destination_folder>`

   **Warning**  
   Не извлекайте шаблоны прямо в каталог развертывания групповой политики. В этом файле объединены различные технологии и версии.

3. В извлеченной папке найдите ADMX-файл с поддержкой технологии и версии. В некоторых технологиях MDOP есть несколько наборов объектов групповой политики (GPO). Например, MBAM включает параметры управления MBAM и параметры пользователя MBAM.

4. Найдите соответствующий файл. ADML по языку и региональным параметрам ( *en-US* для английских США).

5. Скопируйте файлы ADMX и ADML в папку определение политики. В зависимости от того, где хранятся шаблоны, вы можете настроить параметры групповой политики на локальном устройстве или на любом компьютере домена.

   - **Локальные файлы:** Чтобы настроить параметры групповой политики на локальном устройстве, скопируйте файлы шаблонов в указанные ниже места.

   <table>
   <colgroup>
   <col width="50%" />
   <col width="50%" />
   </colgroup>
   <thead>
   <tr class="header">
   <th align="left">Тип файла</th>
   <th align="left">Расположение файла</th>
   </tr>
   </thead>
   <tbody>
   <tr class="odd">
   <td align="left"><p>Шаблон групповой политики (ADMX)</p></td>
   <td align="left"><p><code>%systemroot%</code>&lt;strong &gt; PolicyDefinitions</strong></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p>Языковой файл групповой политики (ADML)</p></td>
   <td align="left"><p><code>%systemroot%</code>&lt;strong &gt; PolicyDefinitions</strong><code>[MUIculture]</code></p></td>
   </tr>
   </tbody>
   </table>

   - **Центральное хранилище домена:** Чтобы включить настройку параметров групповой политики администратором групповой политики с любого компьютера домена, скопируйте файлы в указанные ниже места на контроллере домена.

   <table>
   <colgroup>
   <col width="50%" />
   <col width="50%" />
   </colgroup>
   <thead>
   <tr class="header">
   <th align="left">Тип файла</th>
   <th align="left">Расположение файла</th>
   </tr>
   </thead>
   <tbody>
   <tr class="odd">
   <td align="left"><p>Шаблон групповой политики (ADMX)</p></td>
   <td align="left"><p><code>%systemroot%</code>&lt;strong &gt; sysvol\domain\policies\PolicyDefinitions</strong></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p>Языковой файл групповой политики (ADML)</p></td>
   <td align="left"><p><code>%systemroot%</code>&lt;strong &gt; sysvol\domain\policies\PolicyDefinitions [MUIculture]</strong><code>[MUIculture]</code></p>
   <p>Например, файл, зависящий от языковой версии для американского английского, будет храниться в%systemroot%\sysvol\domain\policies\PolicyDefinitions\en-us.</p></td>
   </tr>
   </tbody>
   </table>

6. Измените параметры групповой политики с помощью консоли управления групповыми политиками (GPMC) или расширенного управления групповыми политиками, чтобы настроить параметры групповой политики для технологии MDOP.

### Групповая политика MDOP по технологиям

Дополнительные сведения о поддерживаемой групповой политике MDOP можно найти в документации по технологии.

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Технология MDOP</th>
<th align="left">Наборы версий</th>
<th align="left">Заметки</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong>Виртуализация приложений (App-V)</strong></p></td>
<td align="left"><p>Пакеты обновления для App-V 5,0 и App-V 5,0</p></td>
<td align="left"><p><a href="../appv-v5/how-to-modify-app-v-50-client-configuration-using-the-admx-template-and-group-policy.md" data-raw-source="[How to Modify App-V 5.0 Client Configuration Using the ADMX Template and Group Policy](../appv-v5/how-to-modify-app-v-50-client-configuration-using-the-admx-template-and-group-policy.md)">Изменение конфигурации клиента App-V 5.0 с помощью шаблона ADMX и групповой политики</a></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Виртуализация взаимодействия с пользователем (UE-V)</strong></p></td>
<td align="left"><p>UE-V 2,0 и UE-V 2,1</p></td>
<td align="left"><p><a href="../uev-v2/configuring-ue-v-2x-with-group-policy-objects-both-uevv2.md" data-raw-source="[Configuring UE-V 2.x with Group Policy Objects](../uev-v2/configuring-ue-v-2x-with-group-policy-objects-both-uevv2.md)">Настройка UE-V 2. x с объектами групповой политики</a></p></td>
</tr>
<tr class="odd">
<td align="left"><p></p></td>
<td align="left"><p>UE-V 1,0, включая 1,0 SP1</p></td>
<td align="left"><p><a href="../uev-v1/configuring-ue-v-with-group-policy-objects.md" data-raw-source="[Configuring UE-V with Group Policy Objects](../uev-v1/configuring-ue-v-with-group-policy-objects.md)">Настройка UE-V с помощью объектов групповой политики</a></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Администрирование и мониторинг Microsoft BitLocker (MBAM)</strong></p></td>
<td align="left"><p>MBAM 2,5</p></td>
<td align="left"><p><a href="../mbam-v25/planning-for-mbam-25-group-policy-requirements.md" data-raw-source="[Planning for MBAM 2.5 Group Policy Requirements](../mbam-v25/planning-for-mbam-25-group-policy-requirements.md)">Планирование требований групповой политики MBAM 2.5</a></p></td>
</tr>
<tr class="odd">
<td align="left"><p></p></td>
<td align="left"><p>MBAM 2,0, включая 2,0 SP1</p></td>
<td align="left"><p><a href="../mbam-v2/planning-for-mbam-20-group-policy-requirements-mbam-2.md" data-raw-source="[Planning for MBAM 2.0 Group Policy Requirements](../mbam-v2/planning-for-mbam-20-group-policy-requirements-mbam-2.md)">Планирование требований групповой политики MBAM 2.0</a></p>
<p><a href="../mbam-v2/deploying-mbam-20-group-policy-objects-mbam-2.md" data-raw-source="[Deploying MBAM 2.0 Group Policy Objects](../mbam-v2/deploying-mbam-20-group-policy-objects-mbam-2.md)">Развертывание объектов групповой политики MBAM 2.0</a></p></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p>MBAM 1,0</p></td>
<td align="left"><p><a href="../mbam-v1/how-to-edit-mbam-10-gpo-settings.md" data-raw-source="[How to Edit MBAM 1.0 GPO Settings](../mbam-v1/how-to-edit-mbam-10-gpo-settings.md)">Изменение параметров объектов групповой политики MBAM 1.0</a></p></td>
</tr>
</tbody>
</table>

 

 

 






---
title: Копирование шаблонов групповой политики MBAM 2.5
description: Копирование шаблонов групповой политики MBAM 2.5
author: dansimp
ms.assetid: e526ecec-07ff-435e-bc90-3084b617b84b
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/28/2017
ms.openlocfilehash: a3436552256b1632a11037dc94751207cde89d5c
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10825222"
---
# Копирование шаблонов групповой политики MBAM 2.5


Перед развертыванием установки клиента MBAM необходимо скачать шаблоны групповой политики MBAM, которые содержат параметры настройки реализации MBAM для шифрования диска BitLocker. После загрузки шаблонов вы можете настроить параметры групповой политики для реализации в масштабах всего предприятия.

## Загрузка и развертывание шаблонов групповой политики MDOP


Шаблоны групповой политики MDOP можно загрузить в виде самораспаковывающегося распакованного сжатого файла, сгруппированных по технологиям и версиям.

**Загрузка и развертывание шаблонов групповой политики MDOP**

1. Скачайте шаблоны групповой политики MDOP из [административных шаблонов в групповой политике пакета оптимизации рабочей среды Майкрософт](https://www.microsoft.com/download/details.aspx?id=55531).

2. Запустите загруженный файл, чтобы извлечь папки шаблонов.

   **Warning**  
   Не извлекайте шаблоны прямо в каталог развертывания групповой политики. В этом файле объединены различные технологии и версии.



3. В извлеченной папке найдите ADMX-файл с поддержкой технологии и версии. В некоторых технологиях MDOP есть несколько наборов объектов групповой политики (GPO). Например, MBAM включает параметры управления MBAM и параметры пользователя MBAM.

4. Найдите соответствующий файл. ADML с помощью языка и региональных параметров ( *EN* для английского (США)).

5. Скопируйте файлы ADMX и ADML в папку определение политики. В зависимости от того, где хранятся шаблоны, вы можете настроить параметры групповой политики на локальном устройстве или на любом компьютере домена.

   **Локальные файлы.** Чтобы настроить параметры групповой политики на локальном устройстве, скопируйте файлы шаблонов в указанные ниже места.

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



~~~
**Domain central store.** To enable Group Policy settings configuration by a Group Policy administrator from any computer on the domain, copy files to the following locations on the domain controller:

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">File type</th>
<th align="left">File location</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Group Policy template (.admx)</p></td>
<td align="left"><p><code>%systemroot%</code>\<strong>sysvol\domain\policies\PolicyDefinitions</strong></p></td>
</tr>
<tr class="even">
<td align="left"><p>Group Policy language file (.adml)</p></td>
<td align="left"><p><code>%systemroot%</code>\<strong>sysvol\domain\policies\PolicyDefinitions\[MUIculture]</strong><code>\[MUIculture]</code></p>
<p>For example, the U.S. English ADML language-specific file will be stored in %systemroot%\sysvol\domain\policies\PolicyDefinitions\en-us.</p></td>
</tr>
</tbody>
</table>
~~~



6. Измените параметры групповой политики с помощью консоли управления групповыми политиками (GPMC) или расширенного управления групповыми политиками, чтобы настроить параметры групповой политики для технологии MDOP. Дополнительные сведения [MBAM в разделе Изменение параметров групповой политики в 2,5](editing-the-mbam-25-group-policy-settings.md) .

   Описание параметров групповой политики приведено в разделе [Планирование требований к групповой политике MBAM 2,5](planning-for-mbam-25-group-policy-requirements.md).


## Статьи по теме


[Развертывание объектов групповой политики MBAM 2.5](deploying-mbam-25-group-policy-objects.md)


## У вас есть предложение MBAM?
- Здесь вы можете добавить предложения и проголосовать [здесь](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring). 
- Для MBAM проблемы используйте [MBAM Форум TechNet](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).







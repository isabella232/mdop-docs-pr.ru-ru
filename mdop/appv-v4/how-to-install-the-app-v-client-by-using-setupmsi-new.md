---
title: Установка клиента App-V с помощью Setup.msi
description: Установка клиента App-V с помощью Setup.msi
author: dansimp
ms.assetid: 7221f384-36d6-409a-94a2-86f54fd75322
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 7fb3a145a6c57cccbae3f4e6b191b89d93278ff8
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10817332"
---
# Установка клиента App-V с помощью Setup.msi


В этой статье описано, как установить клиент App-V с помощью программы setup.msi. Прежде чем устанавливать клиент App-V с помощью программы setup.msi, необходимо сначала определить, нужно ли установить какое-либо необходимое программное обеспечение, а затем установить его. Чтобы установить необходимое программное обеспечение, ознакомьтесь с разделом [Установка программного](#prereq-sw) обеспечения, необходимых для этого раздела. Чтобы установить клиентское программное обеспечение, ознакомьтесь с разделом [Установка клиента App-V с помощью Setup.msi программы в](#msi-setup) этой статье.

## <a href="" id="prereq-sw"></a>Установка необходимого программного обеспечения


Чтобы установить необходимое программное обеспечение, можно воспользоваться приведенными ниже инструкциями. Вы можете создать командный файл и выполнить команды из командной строки, а также с помощью языка сценариев, например VBScript или Windows PowerShell, для выполнения команд.

**Примечание**  Версии x86 следующего программного обеспечения необходимы для версий x86 и x64 клиента App-V.

 

**Установка распространяемого пакета Microsoft VisualC + + 2005SP1 (x86)**

1. Скачайте пакет программного обеспечения для [пакета обновления Microsoft Visual C++ 2005 SP1 (x86)](https://go.microsoft.com/fwlink/?LinkId=119961) из центра загрузки Майкрософт ( <https://go.microsoft.com/fwlink/?LinkId=119961> ). \ [Значение маркера шаблона \] для версии 4,5 SP2 и более поздних версий клиента App-V Скачайте vcredist\_x86.exe с помощью [распространяемого пакета обновления безопасности ATL для Microsoft Visual C++ 2005](https://go.microsoft.com/fwlink/?LinkId=169360) ( https://go.microsoft.com/fwlink/?LinkId=169360).\ [значение маркера шаблона])

2. Для автоматической установки используйте параметр командной строки "/Q" с vcredist\_x86.exe (например, **vcredist\_x86.exe/q**.

3. Чтобы установить программное обеспечение с помощью файла vcredist\_x86.msi, используйте параметр командной строки "/C/T: &lt; fullpathtofolder", &gt; чтобы извлечь файлы vcredist.msi и vcredis1.cab из vcredist\_x86.exe во временную папку. Для автоматической установки используйте параметр командной строки/quiet (например, **msiexec/i vcredist.msi** /quiet.

### Установка распространяемого пакета Microsoft VisualC + + 2008SP1 (x86)

**Важно!**  Для версии 4.6 и более поздних версий клиента App-V необходимо также установить обновление безопасности ATL для Microsoft Visual C++ 2008 с пакетом обновления 1 (SP1).

 

****

1.  Скачайте [распространяемый пакет Microsoft Visual C++ 2008 с пакетом обновления 1 (SP1) для пакета обновления безопасности ATL](https://go.microsoft.com/fwlink/?LinkId=150700) из центра загрузки Майкрософт ( https://go.microsoft.com/fwlink/?LinkId=150700) .

2.  Для автоматической установки используйте параметр командной строки "/Q" с vcredist\_x86.exe (например, **vcredist\_x86.exe/q**.

### Установка Microsoft Core XML Services (MSXML) 6.0 SP1 (x86)

****

1.  Скачайте пакет программного обеспечения [Microsoft Core XML Services (MSXML) 6.0 с пакетом обновления 1 (x86)](https://go.microsoft.com/fwlink/?LinkId=63266) в центре загрузки Майкрософт ( https://go.microsoft.com/fwlink/?LinkId=63266) .

2.  Для автоматической установки используйте параметр командной строки/quiet, например **msiexec/i msxml6\_x86.msi/quiet**.

### Установка отчетов об ошибках в приложениях Microsoft

При установке отчетов об ошибках приложений Microsoft следует использовать параметр *APPGUID* для указания кода продукта App-V. Код продукта уникален для каждого типа клиента App-V и версии. Выберите правильный код продукта из приведенной ниже таблицы.

**Важно!**  Для App-V 4.6 SP2 и более поздних версий вам больше не нужно устанавливать отчеты об ошибках приложений Microsoft (dw20shared.msi). Теперь приложение App-V использует отчеты об ошибках Microsoft.

 

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Версия</th>
<th align="left">Код продукта для клиента для настольных систем</th>
<th align="left">Код продукта для клиента служб удаленных рабочих столов</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>App-V 4,5 CU1</p></td>
<td align="left"><p>FE495DBC-6D42-4698-B61F-86E655E0796D</p></td>
<td align="left"><p>8A97C241-D92A-47DC-B360-E716C1AAA929</p></td>
</tr>
<tr class="even">
<td align="left"><p>App-V 4,5 SP1</p></td>
<td align="left"><p>93468B43-C19D-44F9-8BCC-114076DB0443</p></td>
<td align="left"><p>0042AD3C-99A4-4E58-B5F0-744D5AD96E1C</p></td>
</tr>
<tr class="odd">
<td align="left"><p>App-V 4,5 SP2</p></td>
<td align="left"><p>C6FC75B9-7D86-4C44-8BDB-EAFE1F0E200D</p></td>
<td align="left"><p>ECF80BBA-CA07-4A74-9ED6-E064F38AF1F5</p></td>
</tr>
<tr class="even">
<td align="left"><p>App-V 4,6 x86</p></td>
<td align="left"><p>9E9D30B2-2065-4FDE-B756-8F1A6EABAFC3</p></td>
<td align="left"><p>439FAC21-B423-41D4-8126-54F9FCB70039</p></td>
</tr>
<tr class="odd">
<td align="left"><p>App-V 4,6 x64</p></td>
<td align="left"><p>E569E45F-7BA6-4C7F-B6BA-3FFCBE92FC22</p></td>
<td align="left"><p>D2977C18-D88A-47CB-AFD8-652DD36F4D0D</p></td>
</tr>
<tr class="even">
<td align="left"><p>App-V 4,6 x86 ¹</p></td>
<td align="left"><p>40C3258B-F9D1-46DF-AE97-72C1F86F2427</p></td>
<td align="left"><p>9915D911-CC73-4122-AF4F-564F89454655</p></td>
</tr>
<tr class="odd">
<td align="left"><p>App-V 4,6 x64 ¹</p></td>
<td align="left"><p>1650E31F-23B8-40B5-A60A-C5934F557E3B</p></td>
<td align="left"><p>7580D918-C621-49E7-9877-3CC59F9BD1DA</p></td>
</tr>
<tr class="even">
<td align="left"><p>App-V 4,6 x86 SP1</p></td>
<td align="left"><p>DB9F70CD-29BC-480B-8BA2-C9C2232C4553</p></td>
<td align="left"><p>1354855A-2298-4C73-9022-EF0686C65991</p></td>
</tr>
<tr class="odd">
<td align="left"><p>App-V 4,6 x64 SP1</p></td>
<td align="left"><p>342C9BB8-65A0-46DE-AB7A-8031E151AF69</p></td>
<td align="left"><p>B2C6C8D5-FE76-4056-A326-EE5D633EA175</p></td>
</tr>
</tbody>
</table>

 

выпуск пакета App-V "Languages".

**Примечание**  Если вам нужно найти код продукта, можно воспользоваться редактором базы данных Orca.exe или аналогичным средством для проверки файлов установщика Windows, чтобы найти значение свойства *ProductCode* . Дополнительные сведения об использовании Orca.exe можно найти в разделе [средства разработки установщика Windows](https://go.microsoft.com/fwlink/?LinkId=150008) ( https://go.microsoft.com/fwlink/?LinkId=150008) .

 

****

1.  Найдите программу установки отчетов об ошибках приложений Microsoft, dw20shared.msi, которую можно найти в папке **Support\\Watson** на выпускаемом носителе.

2.  Чтобы установить программное обеспечение, выполните следующую команду:

         **msiexec /i dw20shared.msi APPGUID={valuefromtable} REBOOT=Suppress REINSTALL=ALL REINSTALLMODE=vomus**

## <a href="" id="msi-setup"></a>Установка клиента App-V с помощью программы Setup.msi


Чтобы установить клиент App-V, выполните указанные ниже действия. Убедитесь, что установлены все необходимые программные компоненты. \ [Значение маркера шаблона \] для версии 4.6 и более поздних версий клиента App-V программа setup.msi проверяет систему, а если необходимое программное обеспечение не установлено, генерирует сообщение об ошибке, указывающий на то, что установка не может быть продолжена. \ [Значение маркера шаблона \]

**Установка клиента Application Virtualization с помощью Setup.msi**

1.  Убедитесь в том, что вы вошли в систему под учетной записью, обладающей правами администратора на компьютере.

2.  Откройте окно командной строки с повышенными правами и измените каталог на папку, содержащую установочные файлы. При установке версии 4.6 или более поздней версии клиента App-V необходимо использовать правильный установщик для операционной системы компьютера, 32-bit или 64-bit. Установка завершится сбоем и появится сообщение об ошибке, если вы используете неправильный установщик.

3.  Введите командную строку установки в командной строке. Кроме того, вы можете создать командный файл и запустить его из командной строки. Вы также можете использовать для выполнения команды язык сценариев, например VBScript или Windows PowerShell.

4.  В приведенном ниже примере кода показано, как setup.msi можно использовать с несколькими необязательными параметрами. Дополнительные сведения об этих параметрах можно найти в разделе [Параметры командной строки установщика клиента Application Virtualization](application-virtualization-client-installer-command-line-parameters.md).

    **msiexec.exe/i "setup.msi" SWICACHESIZE = "10240" SWIPUBSVRDISPLAY = "Production System" SWIPUBSVRTYPE = "HTTP/Secure" SWIPUBSVRHOST = "PRODSYS" SWIPUBSVRPORT = "443" SWIPUBSVRPATH = "/AppVirt/appsntype.xml" SWIPUBSVRREFRESH = "on" SWIGLOBALDATA = "D:\\AppVirt\\Global" SWIUSERDATA = "^% LOCALAPPDATA ^%\\Windows\\Application виртуализация" SWIFSDRIVE = "S",,/q**

    **Важно.**  
    -   Для автоматической установки используется параметр установщика Windows "**/q**".

    -   **%** Символу ""**% HomeDrive%**"должен предшествовать **^** знак" "". В противном случае Командная оболочка Windows задает значение для пользователя, который выполняет установку.

    -   Чтобы включить ведение журнала установки, воспользуйтесь переключателем msiexec **/l\ * v имя_файла. log**.

     

## Статьи по теме


[Установка клиента с помощью командной строки](how-to-install-the-client-by-using-the-command-line-new.md)

 

 






---
title: Справочник по схемам шаблонов приложений для UE-V 2. x
description: Справочник по схемам шаблонов приложений для UE-V 2. x
author: dansimp
ms.assetid: be8735a5-6a3e-4b1f-ba14-2a3bc3e5a8b6
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 03ff6eabae68f07c23d5977f901e6a90e292c6ac
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10827409"
---
# Справочник по схемам шаблонов приложений для UE-V 2. x


Виртуализация взаимодействия с пользователем Microsoft (UE-V) 2,0, 2,1 и 2,1 SP1 используют шаблоны расположения XML-параметров для определения параметров классического приложения, а также параметров Windows, которые регистрируются и применяются с UE-V. UE-V включает набор шаблонов расположения параметров по умолчанию. Вы также можете создавать шаблоны расположений с пользовательскими параметрами с помощью генератора UE-V.

Опытный пользователь может настроить XML-файл для шаблона расположения параметров. В этой статье описана структура XML для шаблонов расположения параметров UE-V 2,1 (SP1) и 2,0, а также инструкции по изменению этих файлов.

## Справочник по схеме шаблонов приложений для UE-V 2,1 и 2,1 SP1


В этом разделе подробно описана структура XML для шаблона расположения параметров UE-V 2,1 и 2,1 SP1 и приведены инструкции по изменению этого файла.

### В этом разделе

-   [Объявление XML и атрибут кодировки](#xml21)

-   [Пространство имен и корневой элемент](#namespace21)

-   [Типы данных](#data21)

-   [Элемент Name](#name21)

-   [Элемент ID](#id21)

-   [Элемент Version](#version21)

-   [Элемент Author](#author21)

-   [Обработка и обработка элементов](#processes21)

-   [Элемент приложения](#application21)

-   [Общий элемент](#common21)

-   [Элемент SettingsLocationTemplate](#settingslocationtemplate21)

-   [Приложение: SettingsLocationTemplate. xsd](#appendix21)

### <a href="" id="xml21"></a>Объявление XML и атрибут кодировки

**Обязательно: истина**

**Тип: строка**

В XML-объявлении должен быть указан атрибут версии 1,0 ( &lt; ? XML Version = "1.0" &gt; ). Шаблоны местоположения параметров, созданные генератором UE-V, сохраняются в кодировке UTF-8, хотя кодировка явно не указана. Рекомендуется включить в этот элемент атрибут Encoding = "UTF-8". Все шаблоны, включенные в продукт, задают этот тег (вы также увидите документы в%ProgramFiles%\\Microsoft взаимодействия с пользователем Virtualization\\Templates для справки). Пример

`<?xml version="1.0" encoding="UTF-8"?>`

### <a href="" id="namespace21"></a>Пространство имен и корневой элемент

**Обязательно: истина**

**Тип: строка**

UE-V использует https://schemas.microsoft.com/UserExperienceVirtualization/2012/SettingsLocationTemplate пространство имен для всех приложений. SettingsLocationTemplate является корневым элементом и содержит все остальные элементы. Ссылка на SettingsLocationTemplate во всех шаблонах, использующих этот тег:

`<SettingsLocationTemplate xmlns='https://schemas.microsoft.com/UserExperienceVirtualization/2012/SettingsLocationTemplate'>`

### <a href="" id="data21"></a>Типы данных

Это типы данных для схемы шаблонов приложений UE-V.

<a href="" id="guid"></a>**Идентификатор GUID** GUID описывает стандартное выражение глобального уникального идентификатора в форме "\ \ {\ [a-fA-F0-9 \] {8} -\ [a-FA-F0-9 \] {4} -\" [a-FA-F0-9 \] {4} -\ [a-FA-F0-9 \] {4} -\ [a – ОС – F0-9 \] {12} \ \} ". Используется в элементе Filesetting\\Root\\KnownFolder для проверки форматирования известных папок.

<a href="" id="filenamestring"></a>**FilenameString** FilenameString — имя файла отслеживаемого процесса. Его значения ограничены регулярным выражением \ [^ \ \ \ \ \ \ \ \ \ \ \ \ | &lt; &gt; /: \] + (это означает, что они не содержат знаков обратной косой черты, знака звездочки или символа подстановки с вопросительным знаком, символа вертикальной черты, знака "больше или меньше", знаков после запятой или двоеточия).

<a href="" id="idstring"></a>**IDString** IDString относится к значению идентификатора элементов приложения, SettingsLocationTemplate и часто используемых элементов (используется для описания наборов приложений с общими параметрами). Оно ограничено тем же регулярным выражением, что и FilenameString (\ [^ &lt; &gt; ] /:\]+).

<a href="" id="templateversion"></a>**TemplateVersion** TemplateVersion — это целочисленное значение, используемое для описания редакции шаблона расположения параметров. Его значение может находиться в диапазоне от 0 до 2147483647.

<a href="" id="empty"></a>**Пустой** Пустой объект ссылается на пустое значение. Используется в Process\\ShellProcess, чтобы указать, что отсутствует процесс для отслеживания. Это значение не следует использовать ни в каких шаблонах приложения.

<a href="" id="author"></a>**Автор** Тип данных Author — это сложный тип, который определяет автора шаблона. Он состоит из двух дочерних элементов: **имя** и **адрес электронной почты**. В типе данных Author элемент name является обязательным, а элемент электронной почты — необязательным. Этот тип подробно описан в элементе SettingsLocationTemplate.

<a href="" id="range"></a>**Range (диапазон** ) Диапазон. определяет целочисленный класс, состоящий из двух дочерних элементов: **минимума** и **максимума**. Этот тип данных реализован в типе данных ProcessVersion. Если задано значение, должно быть включено как минимальное, так и максимальное значения.

<a href="" id="processversion"></a>**ProcessVersion** ProcessVersion определяет тип с четырьмя дочерними элементами: **основными**, **дополнительными**, **сборками**и **исправлениями**. Этот тип данных используется элементом Process для заполнения его значений ProductVersion и FileVersion. Данными для этого типа является значение Range. Основной дочерний элемент является обязательным, а остальные являются необязательными.

<a href="" id="architecture"></a>**Архитектура** Архитектура перечисляет два возможных значения: **Win32** и **Win64**. Эти значения используются для определения архитектуры процесса.

<a href="" id="process"></a>**Процесс** Тип данных «процесс» — это контейнер, используемый для описания процессов, которые необходимо отслеживать с помощью UE-V. Он состоит из шести дочерних элементов: **имя файла**, **архитектура**, **ProductName**, **FileDescription**, **ProductVersion**и **FileVersion**. В этой таблице подробно описываются соответствующие типы данных каждого элемента.

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><strong>Элемент</strong></p></td>
<td align="left"><p><strong>Тип данных</strong></p></td>
<td align="left"><p><strong>Обязательное</strong></p></td>
</tr>
<tr class="even">
<td align="left"><p>Файла</p></td>
<td align="left"><p>FilenameString</p></td>
<td align="left"><p>True</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Архитектура</p></td>
<td align="left"><p>Архитектура</p></td>
<td align="left"><p>False</p></td>
</tr>
<tr class="even">
<td align="left"><p>ProductName</p></td>
<td align="left"><p>Строка</p></td>
<td align="left"><p>False</p></td>
</tr>
<tr class="odd">
<td align="left"><p>FileDescription</p></td>
<td align="left"><p>Строка</p></td>
<td align="left"><p>False</p></td>
</tr>
<tr class="even">
<td align="left"><p>ProductVersion</p></td>
<td align="left"><p>ProcessVersion</p></td>
<td align="left"><p>False</p></td>
</tr>
<tr class="odd">
<td align="left"><p>FileVersion</p></td>
<td align="left"><p>ProcessVersion</p></td>
<td align="left"><p>False</p></td>
</tr>
</tbody>
</table>

 

<a href="" id="processes"></a>**Процессы** Тип данных Process представляет контейнер для коллекции из одного или нескольких элементов процесса. В типе последовательности процессов поддерживаются два дочерних элемента: **Process** и **ShellProcess**. Процесс — это элемент типа процесс, и ShellProcess имеет пустой тип данных. В последовательности должно быть идентифицировано по крайней мере один элемент.

<a href="" id="path"></a>**Path (путь** ) Путь обрабатывается RegistrySetting и FileSetting, чтобы ссылаться на пути к реестру и файлам. Этот элемент поддерживает два необязательных атрибута: **recursive** и **DeleteIfNotFound**. Для обоих значений задано значение по умолчанию = "ложь".

Recursive указывает на то, что путь и все вложенные папки включены для параметров файла или все дочерние разделы реестра включены в параметры реестра. В обоих случаях все элементы на текущем уровне включаются в захваченные данные. Для объекта FileSettings все файлы в указанной папке включаются в данные, полученные UE-V, но папки не включаются. Для путей в реестре записываются все значения из текущего пути, но дочерние разделы реестра не фиксируются. В обоих случаях следует соблюдать осторожность, чтобы избежать захвата больших наборов данных или большого количества элементов.

Атрибут DeleteIfNotFound удаляет параметр из данных пути к хранилищу параметров пользователя. Это может быть предпочтительнее в случаях, когда при удалении этих параметров из пакета сохраняется большой объем дискового пространства на сервере файлов с путями хранилища параметров.

<a href="" id="filemask"></a>**FileMask** FileMask задает только определенные типы файлов для папки, определенной путем. Например, Path может быть `C:\users\username\files` и FileMask может `*.txt` содержать только текстовые файлы.

<a href="" id="registrysetting"></a>**RegistrySetting** RegistrySetting представляет контейнер для разделов реестра и значений, а также соответствующее требуемое поведение в части агента UE-V. В этом типе определено четыре дочерних элемента: **path**, **Name**, **Exclude**и последовательность значений **path** и **Name**.

<a href="" id="filesetting"></a>**FileSetting** FileSetting содержат параметры, связанные с путями к файлам и файлам. Определены четыре дочерних элемента: **root**, **path**, **FileMask**и **Exclude**. Root является обязательным условием, а другие — необязательными.

<a href="" id="settings"></a>**Параметры** Параметры — это контейнер для всех параметров, которые применяются к определенному шаблону. Она включает в себя экземпляры параметров реестра, файлов, SystemParameter и CustomAction, описанных выше. Кроме того, он также может содержать следующие дочерние элементы с описанными ниже поведениями.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><strong>Элемент</strong></p></td>
<td align="left"><p><strong>Описание</strong></p></td>
</tr>
<tr class="even">
<td align="left"><p>Асинхронная репликация</p></td>
<td align="left"><p>Пакеты асинхронных параметров применяются без блокирования запуска приложения, чтобы приложение не заблокировалось во время применения параметров. Это полезно для параметров, которые можно применять асинхронно, например с <code>get/set</code> помощью API-интерфейса, например SystemParameterSetting.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>PreventOverlappingSynchronization</p></td>
<td align="left"><p>По умолчанию UE-V сохраняет параметры для приложения только в том случае, если вы закрыли последний экземпляр приложения, использующего этот шаблон. Если для этого элемента задано значение false, UE-V экспортирует параметры, даже если запущены другие экземпляры приложения. Готовые шаблоны — те, которые включают раздел общего элемента, поставляемый с UE-V. Используйте этот флаг, чтобы разрешить общим параметрам возможность всегда экспортировать при закрытии приложения, а также запретить экспорт параметров приложения, пока не закроется последний экземпляр.</p></td>
</tr>
<tr class="even">
<td align="left"><p>AlwaysApplySettings</p></td>
<td align="left"><p>(введено в 2,1)</p>
<p>Этот параметр принудительно применяет импортированный пакет параметров, даже если между пакетом и текущим состоянием приложения никаких различий. Этот параметр следует использовать только в особых случаях, так как он может замедлить импорт параметров.</p></td>
</tr>
</tbody>
</table>

 

### <a href="" id="name21"></a>Элемент Name

**Обязательно: истина**

**Тип: строка**

Name указывает уникальное имя шаблона расположения параметров. Этот элемент используется для отображения в целях создания ссылки на шаблон в WMI, PowerShell, просмотре событий и журналах отладки. Как правило, не следует ссылаться на сведения о версии, так как это может быть объектом из элемента ProductVersion. Например, укажите, `<Name>My Application</Name>` а не `<Name>My Application 1.1</Name>` .

**Примечание**  UE-V не ссылается на внешние DTD, поэтому невозможно использовать именованные сущности в шаблоне расположения параметров. Например, не используйте &reg; для ссылки на зарегистрированный знак товарного знака®. Вместо этого используйте канонические нумерованные ссылки, чтобы включить эти типы специальных знаков, например & \ #174 для символа®. Это правило применимо ко всем строковым значениям в этом документе.

<http://www.w3.org/TR/xhtml1/dtds.html>Для получения полного списка сущностей знаков. Документы в кодировке UTF-8 могут содержать символы Юникода напрямую. Сохранение шаблонов с помощью UE-V Generator автоматически преобразует сущности знаков в их представления Unicode.

 

### <a href="" id="id21"></a>Элемент ID

**Обязательно: истина**

**Тип: строка**

Идентификатор заполняет уникальный идентификатор для определенного шаблона. Этот тег становится основным идентификатором, который агент UE-V использует для ссылки на шаблон во время выполнения (например, просмотр выходных данных командлетов PowerShell Get-UevTemplate и Get-UevTemplateProgram). В соответствии с соглашением этот тег не должен содержать пробелы, что упрощает сценарии. Номера версий приложений должны быть указаны в этом элементе, чтобы можно было легко идентифицировать шаблон, например `<ID>MicrosoftCalculator6</ID>` или `<ID>MicrosoftOffice2010Win64</ID>` .

### <a href="" id="version21"></a>Элемент Version

**Обязательно: истина**

**Тип: целое число**

**Минимальное значение: 0**

**Максимальное значение: 2147483647**

Version определяет версию шаблона расположения параметров для администрирования отслеживания изменений. Генератор UE-V автоматически получает это количество на единицу каждый раз при сохранении шаблона. Обратите внимание, что это поле должно быть целым числом. дробные значения, например, `<Version>2.5</Version>` недопустимы.

**Подсказка:** Вы можете сохранять заметки об изменениях в версии с помощью тегов комментариев XML `<!-- -->` , например:

```xml
  <!--
     Version History

     Version 1 Jul 05, 2012 Initial template created by Generator - Denise@Contoso.com
     Version 2 Jul 31, 2012 Added support for app.exe v2.1.3 - Mark@Contoso.com
     Version 3 Jan 01, 2013 Added font settings support - Mark@Contoso.com
     Version 4 Jan 31, 2013 Added support for plugin settings - Tony@Contoso.com
   -->
  <Version>4</Version>
```

**Важно!**  Это значение запрашивается, чтобы определить, следует ли применять новую версию шаблона к существующему шаблону в следующих экземплярах:

-   При выполнении задачи "автоматическое обновление шаблона" в расписании

-   При выполнении командлета PowerShell Update-UevTemplate

-   Когда метод microsoft\\uev: SettingsLocationTemplate Update вызывается через WMI

 

### <a href="" id="author21"></a>Элемент Author

**Обязательно: ложь**

**Тип: строка**

Автор определяет создателя шаблона расположения параметров. Поддерживаются два необязательных дочерних элемента: **имя** и **адрес электронной почты**. Оба атрибута являются необязательными, но если указан дочерний элемент электронной почты, он должен сопровождаться элементом name. Автор — это полное имя контакта в шаблоне расположения параметров, а адрес электронной почты должен указывать на адрес электронной почты автора. Мы рекомендуем использовать эти сведения в шаблонах, опубликованных в открытых источниках, например в [галерее Templates UE-V](https://gallery.technet.microsoft.com/site/search?f%5B0%5D.Type=RootCategory&f%5B0%5D.Value=UE-V).

### <a href="" id="processes21"></a>Обработка и обработка элементов

**Обязательно: истина**

**Тип: элемент**

Процессы содержат по крайней мере один `<Process>` элемент, который, в свою очередь, включает следующие дочерние элементы: **имя_файла**, **архитектура**, **ProductName**, **FileDescription**, **ProductVersion**и **FileVersion**. Дочерний элемент filename является обязательным, а другие — необязательными. Полностью заполненный элемент включает теги, похожие на приведенный ниже.

```xml
<Process>
  <Filename>MyApplication.exe</Filename>
  <Architecture>Win64</Architecture>
  <ProductName> MyApplication </ProductName>
  <FileDescription>MyApplication.exe</FileDescription>
  <ProductVersion>
    <Major Minimum="2" Maximum="2" />
    <Minor Minimum="0" Maximum="0" />
    <Build Minimum="0" Maximum="0" />
    <Patch Minimum="5" Maximum="5" />
  </ProductVersion>
  <FileVersion>
    <Major Minimum="2" Maximum="2" />
    <Minor Minimum="0" Maximum="0" />
    <Build Minimum="0" Maximum="0" />
    <Patch Minimum="5" Maximum="5" />
  </FileVersion>
</Process>
```

### Файла

**Обязательно: истина**

**Тип: строка**

Filename указывает фактическое имя исполняемого файла в том виде, в котором оно отображается в файловой системе. Этот элемент задает основной критерий, который используется UE-V для оценки того, применяется ли шаблон к процессу или нет. Этот элемент должен быть указан в XML-файле шаблона расположения параметров.

Допустимые имена файлов не должны соответствовать регулярному выражению \ [^ \ \ \ \ \? \ \ | &lt; &gt; /: \] +, то есть они не могут содержать символы обратной косой черты, звездочки и знаки подстановки вопросительного знака, символ вертикальной черты, знак "больше или меньше" и знак прямой или двоеточие (\ \? \* | &lt; &gt; /или: символы.).

**Подсказка:** Для проверки строки с помощью этого регулярного выражения используйте командное окно PowerShell и подставьте имя исполняемого файла для **YourFileName**:

`"YourFileName.exe" -match  "[\\\?\*\|<>/:]+"`

Значение **true** указывает на то, что строка содержит недопустимые символы. Ниже приведены некоторые примеры недопустимых значений.

-   \\\\server\\share\\program.exe

-   Программа \ *. exe

-   Pro? ram.exe

-   Программа &lt; 1 &gt; . exe

**Примечание**  Генератор UE-V кодирует символы "больше" и "меньше" &gt; и &lt; соответственно.

 

В редких случаях значение FileName не обязательно должно включать расширение EXE, но оно должно быть задано как часть значения. Например, `<Filename>MyApplictication.exe</Filename>` следует указать вместо `<Filename>MyApplictication</Filename>` . Второй пример не применяет шаблон к процессу, если фактическим именем исполняемого файла является "MyApplication.exe".

### Архитектура

**Обязательно: ложь**

**Тип: архитектура (строка)**

Архитектура — это архитектура процессора, для которой был скомпилирован целевой исполняемый файл. Допустимые значения: Win32 для 32-разрядных приложений или Win64 для 64-разрядных приложений. Если он есть, этот тег ограничивает применимость шаблона расположения параметров для определенной архитектуры приложения. Например, Сравните пользовательский интерфейс%ProgramFiles%\\Microsoft Virtualization\\templates\\ MicrosoftOffice2010Win32.xml и MicrosoftOffice2010Win64.xml файлов, включенных в UE-V. Это полезно, когда относительные пути меняются между различными версиями исполняемого файла, а также в случае, если параметры были добавлены или удалены при переходе с одной архитектуры процессора на другую.

Если этот элемент отсутствует, шаблон расположения параметров игнорирует архитектуру процесса и применяется как в 32, так и в 64-разрядных процессах, если применяются имя файла и другие атрибуты.

**Примечание**  UE-V не поддерживает процессоры ARM в этой версии.

 

### ProductName

**Обязательно: ложь**

**Тип: строка**

ProductName — это необязательный элемент, используемый для идентификации продукта в целях администрирования или создания отчетов. Значение ProductName отличается от имени файла тем, что в нем нет ограничений регулярных выражений. Это позволяет более понятное описание процесса, в котором имя исполняемого файла может быть очевидным. Пример

```xml
<Process>
  <Filename>MyApplication.exe</Filename>
  <ProductName>My Application 6.x by Contoso.com</ProductName>
  <ProductVersion>
    <Major Minimum="6" Maximum="6" />
  </ProductVersion>
</Process>
```

### FileDescription

**Обязательно: ложь**

**Тип: строка**

FileDescription — необязательный тег, позволяющий административному описанию исполняемого файла. Это поле с произвольным текстом, которое может быть полезно при различении нескольких исполняемых файлов в пакете программного обеспечения, где необходимо идентифицировать функцию исполняемого файла.

Например, в подходящем приложении может быть полезно получать напоминания о функции двух исполняемых файлов (MyApplication.exe и MyApplicationHelper.exe), как показано ниже.

```xml
<Processes>
  <Process>
    <Filename>MyApplication.exe</Filename>
    <FileDescription>My Application Main Engine</ FileDescription>
    <ProductVersion>
      <Major Minimum="6" Maximum="6" />
    </ProductVersion>
  </Process>
  <Process>
    <Filename>MyApplicationHelper.exe</Filename>
    <FileDescription>My Application Background Process Executable</FileDescription>
    <ProductVersion>
      <Major Minimum="6" Maximum="6" />
    </ProductVersion>
  </Process>
</Processes>
```

### ProductVersion

**Обязательно: ложь**

**Тип: строка**

ProductVersion — это основная и младшая версии файла, а также сборка и уровень исправлений. ProductVersion является необязательным элементом, но, если он указан, он должен содержать по крайней мере основной дочерний элемент. Значение должно выражать диапазон в форме Minimum = "X" максимум = "Y", где X и Y — целые числа. Минимальное и максимальное значения могут быть одинаковыми.

Элементы "продукт" и "версия файла" могут остаться не установленными. Таким образом, шаблон "зависит от версии", то есть шаблон будет применяться ко всем версиям указанного исполняемого файла.

**Пример 1:**

Версия продукта: 1,0, указанная в генераторе UE-V, создает следующий XML-код:

```xml
<ProductVersion>
  <Major Minimum="1" Maximum="1" />
  <Minor Minimum="0" Maximum="0" />
</ProductVersion>
```

**Пример 2:**

Версия файла: 5.0.2.1000, указанная в генераторе UE-V, создает следующий XML-код:

```xml
<FileVersion>
  <Major Minimum="5" Maximum="5" />
  <Minor Minimum="0" Maximum="0" />
  <Build Minimum="2" Maximum="2" />
  <Patch Minimum="1000" Maximum="1000" />
</FileVersion>
```

**Недопустимый пример 1 — неполный диапазон:**

Присутствует только атрибут Minimum. Максимальное значение также должно быть включено в диапазон.

```xml
<ProductVersion>
  <Major Minimum="2" />
</ProductVersion>
```

**Недопустимый пример 2 — дополнительный номер без основного элемента:**

Присутствует только младший элемент. Кроме того, необходимо включить основную версию.

```xml
<ProductVersion>
  <Minor Minimum="0" Maximum="0" />
</ProductVersion>
```

### FileVersion

**Обязательно: ложь**

**Тип: строка**

FileVersion различает окончательную версию опубликованного приложения и сведения о внутренних сборках для исполняемого компонента. Для большинства коммерческих приложений эти номера идентичны. Там, где они различаются, версия продукта файла обозначает универсальную версию файла, в то время как версия файла указывает определенную сборку файла (как в случае исправления или обновления). Это однозначно определяет файлы без логики обнаружения нарушений.

Чтобы определить версию продукта и версию файла, щелкните его правой кнопкой мыши в проводнике Windows, выберите пункт Свойства, а затем откройте вкладку сведения.

Включение элемента FileVersion для приложения позволяет более детально настроить логику обнаружения, но это не требуется для большинства приложений. Сначала проверяются параметры элемента ProductVersion, а затем FileVersion установлен. Будет применяться более строгие настройки.

Дочерние элементы и правила синтаксиса для FileVersion идентичны методам из ProductVersion.

```xml
<Process>
  <Filename>MSACCESS.EXE</Filename>
  <Architecture>Win32</Architecture>
  <ProductVersion>
    <Major Minimum="14" Maximum="14" />
    <Minor Minimum="0" Maximum="0" />
  </ProductVersion>
  <FileVersion>
    <Major Minimum="14" Maximum="14" />
    <Minor Minimum="0" Maximum="0" />
  </FileVersion>
</Process>
```

### <a href="" id="application21"></a>Элемент приложения

Приложение — это контейнер для параметров, которые применяются к определенному приложению. Это коллекция указанных ниже полей и типов.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><strong>Поле/Тип</strong></p></td>
<td align="left"><p><strong>Описание</strong></p></td>
</tr>
<tr class="even">
<td align="left"><p>Name</p></td>
<td align="left"><p>Задает уникальное имя для шаблона расположения параметров. Этот элемент используется для отображения в целях создания ссылки на шаблон в WMI, PowerShell, просмотре событий и журналах отладки. Дополнительные сведения можно найти в разделе <a href="#name21" data-raw-source="[Name](#name21)"> Name (имя) </a> .</p></td>
</tr>
<tr class="odd">
<td align="left"><p>ID</p></td>
<td align="left"><p>Заполнение уникального идентификатора для определенного шаблона. Этот тег становится основным идентификатором, который агент UE-V использует для ссылки на шаблон во время выполнения. Дополнительные сведения можно найти в разделе <a href="#id21" data-raw-source="[ID](#id21)"> ID </a> .</p></td>
</tr>
<tr class="even">
<td align="left"><p>Описание</p></td>
<td align="left"><p>Необязательное описание шаблона.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>LocalizedNames</p></td>
<td align="left"><p>Необязательное имя, отображаемое в пользовательском интерфейсе, локализованное на языковой стандарт.</p></td>
</tr>
<tr class="even">
<td align="left"><p>LocalizedDescriptions</p></td>
<td align="left"><p>Необязательное описание шаблона, локализованное на языковой стандарт.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Версия</p></td>
<td align="left"><p>Определяет версию шаблона расположения параметров для администрирования отслеживания изменений. Дополнительные сведения можно найти в разделе <a href="#version21" data-raw-source="[Version](#version21)"> Version (версия) </a> .</p></td>
</tr>
<tr class="even">
<td align="left"><p>DeferToMSAccount</p></td>
<td align="left"><p>Определяет, включен ли этот шаблон в сочетании с учетной записью Майкрософт или нет. Если для пользователя на компьютере включена синхронизация MSA, этот шаблон будет автоматически отключен.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>DeferToOffice365</p></td>
<td align="left"><p>Так же, как и MSA, это определяет, включен ли этот шаблон в сочетании с Office365. Если для синхронизации параметров используется Office 365, этот шаблон будет автоматически отключен.</p></td>
</tr>
<tr class="even">
<td align="left"><p>FixedProfile (введено в 2,1)</p></td>
<td align="left"><p>Указывает, что этот шаблон может быть связан только с профилем, указанным в этом элементе, и не может быть изменен с помощью WMI или PowerShell.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Процессы</p></td>
<td align="left"><p>Контейнер для коллекции из одного или нескольких элементов процесса. Дополнительные сведения можно найти в разделе <a href="#processes21" data-raw-source="[Processes](#processes21)"> процессы </a> .</p></td>
</tr>
<tr class="even">
<td align="left"><p>Параметры</p></td>
<td align="left"><p>Контейнер для всех параметров, которые применяются к определенному шаблону. Она включает в себя экземпляры параметров реестра, файлов, SystemParameter и CustomAction. Дополнительные сведения можно найти <strong> в разделе </strong> Параметры <a href="#data21" data-raw-source="[Data types](#data21)"> типов данных </a> .</p></td>
</tr>
</tbody>
</table>

 

### <a href="" id="common21"></a>Общий элемент

Общие похожи на элементы приложения, но всегда связаны с двумя или более элементами приложения. Общий раздел представляет набор параметров, которые совместно используются в этих экземплярах приложения. Это коллекция указанных ниже полей и типов.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><strong>Поле/Тип</strong></p></td>
<td align="left"><p><strong>Описание</strong></p></td>
</tr>
<tr class="even">
<td align="left"><p>Name</p></td>
<td align="left"><p>Задает уникальное имя для шаблона расположения параметров. Этот элемент используется для отображения в целях создания ссылки на шаблон в WMI, PowerShell, просмотре событий и журналах отладки. Дополнительные сведения можно найти в разделе <a href="#name21" data-raw-source="[Name](#name21)"> Name (имя) </a> .</p></td>
</tr>
<tr class="odd">
<td align="left"><p>ID</p></td>
<td align="left"><p>Заполнение уникального идентификатора для определенного шаблона. Этот тег становится основным идентификатором, который агент UE-V использует для ссылки на шаблон во время выполнения. Дополнительные сведения можно найти в разделе <a href="#id21" data-raw-source="[ID](#id21)"> ID </a> .</p></td>
</tr>
<tr class="even">
<td align="left"><p>Описание</p></td>
<td align="left"><p>Необязательное описание шаблона.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>LocalizedNames</p></td>
<td align="left"><p>Необязательное имя, отображаемое в пользовательском интерфейсе, локализованное на языковой стандарт.</p></td>
</tr>
<tr class="even">
<td align="left"><p>LocalizedDescriptions</p></td>
<td align="left"><p>Необязательное описание шаблона, локализованное на языковой стандарт.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Версия</p></td>
<td align="left"><p>Определяет версию шаблона расположения параметров для администрирования отслеживания изменений. Дополнительные сведения можно найти в разделе <a href="#version21" data-raw-source="[Version](#version21)"> Version (версия) </a> .</p></td>
</tr>
<tr class="even">
<td align="left"><p>DeferToMSAccount</p></td>
<td align="left"><p>Определяет, включен ли этот шаблон в сочетании с учетной записью Майкрософт или нет. Если для пользователя на компьютере включена синхронизация MSA, этот шаблон будет автоматически отключен.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>DeferToOffice365</p></td>
<td align="left"><p>Так же, как и MSA, это определяет, включен ли этот шаблон в сочетании с Office365. Если для синхронизации параметров используется Office 365, этот шаблон будет автоматически отключен.</p></td>
</tr>
<tr class="even">
<td align="left"><p>FixedProfile (введено в 2,1)</p></td>
<td align="left"><p>Указывает, что этот шаблон может быть связан только с профилем, указанным в этом элементе, и не может быть изменен с помощью WMI или PowerShell.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Параметры</p></td>
<td align="left"><p>Контейнер для всех параметров, которые применяются к определенному шаблону. Она включает в себя экземпляры параметров реестра, файлов, SystemParameter и CustomAction. Дополнительные сведения можно найти <strong> в разделе </strong> Параметры <a href="#data21" data-raw-source="[Data types](#data21)"> типов данных </a> .</p></td>
</tr>
</tbody>
</table>

 

### <a href="" id="settingslocationtemplate21"></a>Элемент SettingsLocationTemplate

Этот элемент определяет параметры отдельного приложения или набора приложений.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><strong>Поле/Тип</strong></p></td>
<td align="left"><p><strong>Описание</strong></p></td>
</tr>
<tr class="even">
<td align="left"><p>Name</p></td>
<td align="left"><p>Задает уникальное имя для шаблона расположения параметров. Этот элемент используется для отображения в целях создания ссылки на шаблон в WMI, PowerShell, просмотре событий и журналах отладки. Дополнительные сведения можно найти в разделе <a href="#name21" data-raw-source="[Name](#name21)"> Name (имя) </a> .</p></td>
</tr>
<tr class="odd">
<td align="left"><p>ID</p></td>
<td align="left"><p>Заполнение уникального идентификатора для определенного шаблона. Этот тег становится основным идентификатором, который агент UE-V использует для ссылки на шаблон во время выполнения. Дополнительные сведения можно найти в разделе <a href="#id21" data-raw-source="[ID](#id21)"> ID </a> .</p></td>
</tr>
<tr class="even">
<td align="left"><p>Описание</p></td>
<td align="left"><p>Необязательное описание шаблона.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>LocalizedNames</p></td>
<td align="left"><p>Необязательное имя, отображаемое в пользовательском интерфейсе, локализованное на языковой стандарт.</p></td>
</tr>
<tr class="even">
<td align="left"><p>LocalizedDescriptions</p></td>
<td align="left"><p>Необязательное описание шаблона, локализованное на языковой стандарт.</p></td>
</tr>
</tbody>
</table>

 

### <a href="" id="appendix21"></a>Приложение: SettingsLocationTemplate. xsd

Ниже приведен пример файла SettingsLocationTemplate. xsd, в котором показаны элементы, дочерние элементы, атрибуты и параметры.

```xml
<?xml version="1.0" encoding="utf-8"?>
<xs:schema id="UevSettingsLocationTemplate"
  targetNamespace="https://schemas.microsoft.com/UserExperienceVirtualization/2013A/SettingsLocationTemplate"
  elementFormDefault="qualified"
  xmlns="https://schemas.microsoft.com/UserExperienceVirtualization/2013A/SettingsLocationTemplate"
  xmlns:mstns="https://schemas.microsoft.com/UserExperienceVirtualization/2013A/SettingsLocationTemplate"
  xmlns:xs="http://www.w3.org/2001/XMLSchema">

    <xs:simpleType name="Guid">
        <xs:restriction base="xs:string">
            <xs:pattern value="\{[a-fA-F0-9]{8}-[a-fA-F0-9]{4}-[a-fA-F0-9]{4}-[a-fA-F0-9]{4}-[a-fA-F0-9]{12}\}" />
        </xs:restriction>
    </xs:simpleType>

    <xs:simpleType name="FilenameString">
        <xs:restriction base="xs:string">
            <xs:pattern value="[^\\\?\*\|&lt;&gt;/:]+" />
        </xs:restriction>
    </xs:simpleType>

    <xs:simpleType name="IDString">
        <xs:restriction base="xs:string">
            <xs:pattern value="[^\\\?\*\|&lt;&gt;/:.]+" />
        </xs:restriction>
    </xs:simpleType>

    <xs:simpleType name="CompositeIDString">
        <xs:restriction base="xs:string">
            <xs:pattern value="[^\\\?\*\|&lt;&gt;/:.]+([.][^\\\?\*\|&lt;&gt;/:.]+)?" />
        </xs:restriction>
    </xs:simpleType>

    <xs:simpleType name="TemplateVersion">
        <xs:restriction base="xs:integer">
            <xs:minInclusive value="0" />
            <xs:maxInclusive value="2147483647" />
        </xs:restriction>
    </xs:simpleType>

    <xs:complexType name="Empty">
        <xs:sequence/>
    </xs:complexType>

    <xs:complexType name="LocalizedString">
        <xs:simpleContent>
            <xs:extension base="xs:string">
                <xs:attribute name="Locale" type="xs:string" use="required"/>
            </xs:extension>
        </xs:simpleContent>
    </xs:complexType>

    <xs:complexType name="LocalizedName">
        <xs:sequence>
            <xs:element name="Name" type="LocalizedString" minOccurs="1" maxOccurs="unbounded" />
        </xs:sequence>
    </xs:complexType>

    <xs:complexType name="LocalizedDescription">
        <xs:sequence>
            <xs:element name="Description" type="LocalizedString" minOccurs="1" maxOccurs="unbounded" />
        </xs:sequence>
    </xs:complexType>

    <xs:complexType name="ReplacedTemplates">
      <xs:sequence>
        <xs:element name="ID" type="CompositeIDString" minOccurs="1" maxOccurs="unbounded" />
    </xs:sequence>
    </xs:complexType>

    <xs:complexType name="Author">
        <xs:all>
            <xs:element name="Name" type="xs:string" minOccurs="1" />
            <xs:element name="Email" type="xs:string" minOccurs="0" />
        </xs:all>
    </xs:complexType>

    <xs:complexType name="Range">
        <xs:attribute name="Minimum" type="xs:integer" use="required"/>
        <xs:attribute name="Maximum" type="xs:integer" use="required"/>
    </xs:complexType>

    <xs:complexType name="ProcessVersion">
        <xs:sequence>
            <xs:element name="Major" type="Range" minOccurs="1" />
            <xs:element name="Minor" type="Range" minOccurs="0" />
            <xs:element name="Build" type="Range" minOccurs="0" />
            <xs:element name="Patch" type="Range" minOccurs="0" />
        </xs:sequence>
    </xs:complexType>

    <xs:simpleType name="Architecture">
        <xs:restriction base="xs:string">
            <xs:enumeration value="Win32"/>
            <xs:enumeration value="Win64"/>
        </xs:restriction>
    </xs:simpleType>

    <xs:complexType name="Process">
        <xs:sequence>
            <xs:element name="Filename" type="FilenameString" minOccurs="1" />
            <xs:element name="Architecture" type="Architecture" minOccurs="0" />
            <xs:element name="ProductName" type="xs:string" minOccurs="0" />
            <xs:element name="FileDescription" type="xs:string" minOccurs="0" />
            <xs:element name="ProductVersion" type="ProcessVersion" minOccurs="0" maxOccurs="unbounded"/>
            <xs:element name="FileVersion" type="ProcessVersion" minOccurs="0" maxOccurs="unbounded"/>
        </xs:sequence>
    </xs:complexType>

    <xs:complexType name="Processes">
        <xs:sequence>
            <xs:choice minOccurs="1">
                <xs:element name="Process" type="Process" />
                <xs:element name="ShellProcess" type="Empty" />
            </xs:choice>
            <xs:element name="Process" type="Process" minOccurs="0" maxOccurs="unbounded" />
        </xs:sequence>
    </xs:complexType>

    <xs:complexType name="Path">
        <xs:simpleContent>
            <xs:extension base="xs:string">
                <xs:attribute name="Recursive" type="xs:boolean" default="false"/>
                <xs:attribute name="DeleteIfNotFound" type="xs:boolean" default="false"/>
            </xs:extension>
        </xs:simpleContent>
    </xs:complexType>

    <xs:complexType name="RegistrySetting">
        <xs:sequence>
            <xs:element name="Path" type="Path" />
            <xs:element name="Name" type="xs:string" minOccurs="0" maxOccurs="unbounded" />
            <xs:element name="Exclude" minOccurs="0" maxOccurs="unbounded">
                <xs:complexType>
                    <xs:sequence>
                        <xs:element name="Path" type="Path" minOccurs="0" />
                        <xs:element name="Name" type="xs:string" minOccurs="0" maxOccurs="unbounded" />
                    </xs:sequence>
                </xs:complexType>
            </xs:element>
        </xs:sequence>
    </xs:complexType>

    <xs:complexType name="FileSetting">
        <xs:sequence>

            <xs:element name="Root">
                <xs:complexType>
                    <xs:choice>
                        <xs:element name="KnownFolder" type="Guid" />
                        <xs:element name="RegistryEntry" type="xs:string" />
                        <xs:element name="EnvironmentVariable" type="xs:string" />
                    </xs:choice>
                </xs:complexType>
            </xs:element>

            <xs:element name="Path" minOccurs="0" type="Path" />
            <xs:element name="FileMask" type="xs:string" minOccurs="0" maxOccurs="unbounded"/>

            <xs:element name="Exclude" minOccurs="0" maxOccurs="unbounded">
                <xs:complexType>
                    <xs:sequence>
                        <xs:element name="Path" type="Path" minOccurs="0" />
                        <xs:element name="FileMask" type="xs:string" minOccurs="0" maxOccurs="unbounded" />
                    </xs:sequence>
                </xs:complexType>
            </xs:element>

        </xs:sequence>
    </xs:complexType>

    <xs:simpleType name="CustomActionSetting">
        <xs:restriction base="xs:anyURI"/>
    </xs:simpleType>

    <xs:simpleType name="SystemParameterSetting">
        <xs:restriction base="xs:string">

            <!-- Accessibility parameters -->
            <xs:enumeration value="AccessTimeout"/>
            <xs:enumeration value="AudioDescription"/>
            <xs:enumeration value="ClientAreaAnimation"/>
            <xs:enumeration value="DisableOverlappedContent"/>
            <xs:enumeration value="FilterKeys"/>
            <xs:enumeration value="FocusBorderHeight"/>
            <xs:enumeration value="FocusBorderWidth"/>
            <xs:enumeration value="HighContrast"/>
            <xs:enumeration value="MessageDuration"/>
            <xs:enumeration value="MouseClickLock"/>
            <xs:enumeration value="MouseClickLockTime"/>
            <xs:enumeration value="MouseKeys"/>
            <xs:enumeration value="MouseSonar"/>
            <xs:enumeration value="MouseVanish"/>
            <xs:enumeration value="ScreenReader"/>
            <xs:enumeration value="ShowSounds"/>
            <xs:enumeration value="SoundSentry"/>
            <xs:enumeration value="StickyKeys"/>
            <xs:enumeration value="ToggleKeys"/>

            <!-- Input parameters -->
            <xs:enumeration value="Beep"/>
            <xs:enumeration value="BlockSendInputResets"/>
            <xs:enumeration value="DefaultInputLang"/>
            <xs:enumeration value="DoubleClickTime"/>
            <xs:enumeration value="DoubleClkHeight"/>
            <xs:enumeration value="DoubleClkWidth"/>
            <xs:enumeration value="KeyboardCues"/>
            <xs:enumeration value="KeyboardDelay"/>
            <xs:enumeration value="KeyboardPref"/>
            <xs:enumeration value="KeyboardSpeed"/>
            <xs:enumeration value="Mouse"/>
            <xs:enumeration value="MouseButtonSwap"/>
            <xs:enumeration value="MouseHoverHeight"/>
            <xs:enumeration value="MouseHoverTime"/>
            <xs:enumeration value="MouseHoverWidth"/>
            <xs:enumeration value="MouseSpeed"/>
            <xs:enumeration value="MouseTrails"/>
            <xs:enumeration value="SnapToDefButton"/>
            <xs:enumeration value="WheelScrollChars"/>
            <xs:enumeration value="WheelScrollLines"/>

            <!-- Desktop parameters (limited subset) -->
            <xs:enumeration value="DeskWallpaper"/>
            <xs:enumeration value="DesktopColor"/>

        </xs:restriction>
    </xs:simpleType>

    <xs:complexType name="Settings">
        <xs:sequence>
            <xs:element name="Asynchronous" type="xs:boolean" minOccurs="0" />
            <xs:element name="PreventOverlappingSynchronization" type="xs:boolean" minOccurs="0" />
            <xs:element name="AlwaysApplySettings" type="xs:boolean" minOccurs="0" />
            <xs:choice minOccurs="0" maxOccurs="unbounded">
                <xs:element name="Registry" type="RegistrySetting" />
                <xs:element name="File" type="FileSetting" />
                <xs:element name="SystemParameter" type="SystemParameterSetting" />
                <xs:element name="CustomAction" type="CustomActionSetting" />
            </xs:choice>
        </xs:sequence>
    </xs:complexType>

    <xs:complexType name="Common">
        <xs:sequence>
            <xs:element name="Name" type="xs:string" />
            <xs:element name="ID" type="IDString" />
            <xs:element name="ReplacedTemplates" type="ReplacedTemplates" minOccurs="0" />
            <xs:element name="Description" type="xs:string" minOccurs="0" />
            <xs:element name="LocalizedNames" type="LocalizedName" minOccurs="0" />
            <xs:element name="LocalizedDescriptions" type="LocalizedDescription" minOccurs="0" />
            <xs:element name="Version" type="xs:integer" />
            <xs:element name="DeferToMSAccount" type="Empty"  minOccurs="0" />
            <xs:element name="DeferToOffice365" type="Empty" minOccurs="0" />
            <xs:element name="Settings" type="Settings" />
        </xs:sequence>
    </xs:complexType>

    <xs:complexType name="Application">
        <xs:sequence>
            <xs:element name="Name" type="xs:string" />
            <xs:element name="ID" type="IDString" />
            <xs:element name="ReplacedTemplates" type="ReplacedTemplates" minOccurs="0" />
            <xs:element name="Description" type="xs:string" minOccurs="0" />
            <xs:element name="LocalizedNames" type="LocalizedName" minOccurs="0" />
            <xs:element name="LocalizedDescriptions" type="LocalizedDescription" minOccurs="0" />
            <xs:element name="Version" type="xs:integer" />
            <xs:element name="DeferToMSAccount" type="Empty"  minOccurs="0" />
            <xs:element name="DeferToOffice365" type="Empty" minOccurs="0" />
            <xs:element name="Processes" type="Processes" />
            <xs:element name="Settings" type="Settings" />
        </xs:sequence>
    </xs:complexType>


    <xs:element name="SettingsLocationTemplate">
        <xs:complexType>
            <xs:sequence>

                <xs:element name="Name" type="xs:string" />
                <xs:element name="ID" type="IDString" />
                <xs:element name="Description" type="xs:string" minOccurs="0" />
                <xs:element name="LocalizedNames" type="LocalizedName" minOccurs="0" />
                <xs:element name="LocalizedDescriptions" type="LocalizedDescription" minOccurs="0" />

                <xs:choice>

                    <!-- Single application -->
                    <xs:sequence>
                        <xs:element name="ReplacedTemplates" type="ReplacedTemplates" minOccurs="0" />
                        <xs:element name="Version" type="TemplateVersion" />
                        <xs:element name="Author" type="Author" minOccurs="0" />
                        <xs:element name="FixedProfile" type="xs:string"  minOccurs="0" />
                        <xs:element name="DeferToMSAccount" type="Empty"  minOccurs="0" />
                        <xs:element name="DeferToOffice365" type="Empty" minOccurs="0" />
                        <xs:element name="Processes" type="Processes" />
                        <xs:element name="Settings" type="Settings" />
                    </xs:sequence>

                    <!-- Suite of applications -->
                    <xs:sequence>
                        <xs:element name="ManageSuiteOnly" type="xs:boolean" minOccurs="0" />
                        <xs:element name="Author" type="Author" minOccurs="0" />
                        <xs:element name="FixedProfile" type="xs:string"  minOccurs="0" />
                        <xs:element name="Common" type="Common" />
                        <xs:element name="Application" type="Application" minOccurs="2" maxOccurs="unbounded" />
                    </xs:sequence>

                </xs:choice>

            </xs:sequence>
        </xs:complexType>
    </xs:element>
    <!-- SettingsLocationTemplate -->

</xs:schema>
```

## Справочник по схемам шаблонов приложений UE-V 2,0


В этом разделе описана структура XML для шаблона расположения параметров UE-V 2,0 и приведены инструкции по изменению этого файла.

### В этом разделе

-   [Объявление XML и атрибут кодировки](#xml)

-   [Пространство имен и корневой элемент](#namespace)

-   [Типы данных](#data)

-   [Элемент Name](#name)

-   [Элемент ID](#id)

-   [Элемент Version](#version)

-   [Элемент Author](#author)

-   [Обработка и обработка элементов](#processes)

-   [Элемент приложения](#application)

-   [Общий элемент](#common)

-   [Элемент SettingsLocationTemplate](#settingslocationtemplate)

-   [Приложение: SettingsLocationTemplate. xsd](#appendix)

### <a href="" id="xml"></a>Объявление XML и атрибут кодировки

**Обязательно: истина**

**Тип: строка**

В XML-объявлении должен быть указан атрибут версии 1,0 ( &lt; ? XML Version = "1.0" &gt; ). Шаблоны местоположения параметров, созданные генератором UE-V, сохраняются в кодировке UTF-8, хотя кодировка явно не указана. Рекомендуется включить в этот элемент атрибут Encoding = "UTF-8". Все шаблоны, включенные в продукт, задают этот тег (вы также увидите документы в%ProgramFiles%\\Microsoft взаимодействия с пользователем Virtualization\\Templates для справки). Пример

`<?xml version="1.0" encoding="UTF-8"?>`

### <a href="" id="namespace"></a>Пространство имен и корневой элемент

**Обязательно: истина**

**Тип: строка**

UE-V использует https://schemas.microsoft.com/UserExperienceVirtualization/2012/SettingsLocationTemplate пространство имен для всех приложений. SettingsLocationTemplate является корневым элементом и содержит все остальные элементы. Ссылка на SettingsLocationTemplate во всех шаблонах, использующих этот тег:

`<SettingsLocationTemplate xmlns='https://schemas.microsoft.com/UserExperienceVirtualization/2012/SettingsLocationTemplate'>`

### <a href="" id="data"></a>Типы данных

Это типы данных для схемы шаблонов приложений UE-V.

<a href="" id="guid"></a>**Идентификатор GUID** GUID описывает стандартное выражение глобального уникального идентификатора в форме "\ \ {\ [a-fA-F0-9 \] {8} -\ [a-FA-F0-9 \] {4} -\" [a-FA-F0-9 \] {4} -\ [a-FA-F0-9 \] {4} -\ [a – ОС – F0-9 \] {12} \ \} ". Используется в элементе Filesetting\\Root\\KnownFolder для проверки форматирования известных папок.

<a href="" id="filenamestring"></a>**FilenameString** FilenameString — имя файла отслеживаемого процесса. Его значения ограничены регулярным выражением \ [^ \ \ \ \ \ \ \ \ \ \ \ \ | &lt; &gt; /: \] + (это означает, что они не содержат знаков обратной косой черты, знака звездочки или символа подстановки с вопросительным знаком, символа вертикальной черты, знака "больше или меньше", знаков после запятой или двоеточия).

<a href="" id="idstring"></a>**IDString** IDString относится к значению идентификатора элементов приложения, SettingsLocationTemplate и часто используемых элементов (используется для описания наборов приложений с общими параметрами). Оно ограничено тем же регулярным выражением, что и FilenameString (\ [^ &lt; &gt; ] /:\]+).

<a href="" id="templateversion"></a>**TemplateVersion** TemplateVersion — это целочисленное значение, используемое для описания редакции шаблона расположения параметров. Его значение может находиться в диапазоне от 0 до 2147483647.

<a href="" id="empty"></a>**Пустой** Пустой объект ссылается на пустое значение. Используется в Process\\ShellProcess, чтобы указать, что отсутствует процесс для отслеживания. Это значение не следует использовать ни в каких шаблонах приложения.

<a href="" id="author"></a>**Автор** Тип данных Author — это сложный тип, который определяет автора шаблона. Он состоит из двух дочерних элементов: **имя** и **адрес электронной почты**. В типе данных Author элемент name является обязательным, а элемент электронной почты — необязательным. Этот тип подробно описан в элементе SettingsLocationTemplate.

<a href="" id="range"></a>**Range (диапазон** ) Диапазон. определяет целочисленный класс, состоящий из двух дочерних элементов: **минимума** и **максимума**. Этот тип данных реализован в типе данных ProcessVersion. Если задано значение, должно быть включено как минимальное, так и максимальное значения.

<a href="" id="processversion"></a>**ProcessVersion** ProcessVersion определяет тип с четырьмя дочерними элементами: **основными**, **дополнительными**, **сборками**и **исправлениями**. Этот тип данных используется элементом Process для заполнения его значений ProductVersion и FileVersion. Данными для этого типа является значение Range. Основной дочерний элемент является обязательным, а остальные являются необязательными.

<a href="" id="architecture"></a>**Архитектура** Архитектура перечисляет два возможных значения: **Win32** и **Win64**. Эти значения используются для определения архитектуры процесса.

<a href="" id="process"></a>**Процесс** Тип данных «процесс» — это контейнер, используемый для описания процессов, которые необходимо отслеживать с помощью UE-V. Он состоит из шести дочерних элементов: **имя файла**, **архитектура**, **ProductName**, **FileDescription**, **ProductVersion**и **FileVersion**. В этой таблице подробно описываются соответствующие типы данных каждого элемента.

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Элемент</th>
<th align="left">Тип данных</th>
<th align="left">Обязательное</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Файла</p></td>
<td align="left"><p>FilenameString</p></td>
<td align="left"><p>True</p></td>
</tr>
<tr class="even">
<td align="left"><p>Архитектура</p></td>
<td align="left"><p>Архитектура</p></td>
<td align="left"><p>False</p></td>
</tr>
<tr class="odd">
<td align="left"><p>ProductName</p></td>
<td align="left"><p>Строка</p></td>
<td align="left"><p>False</p></td>
</tr>
<tr class="even">
<td align="left"><p>FileDescription</p></td>
<td align="left"><p>Строка</p></td>
<td align="left"><p>False</p></td>
</tr>
<tr class="odd">
<td align="left"><p>ProductVersion</p></td>
<td align="left"><p>ProcessVersion</p></td>
<td align="left"><p>False</p></td>
</tr>
<tr class="even">
<td align="left"><p>FileVersion</p></td>
<td align="left"><p>ProcessVersion</p></td>
<td align="left"><p>False</p></td>
</tr>
</tbody>
</table>

 

<a href="" id="processes"></a>**Процессы** Тип данных Process представляет контейнер для коллекции из одного или нескольких элементов процесса. В типе последовательности процессов поддерживаются два дочерних элемента: **Process** и **ShellProcess**. Процесс — это элемент типа процесс, и ShellProcess имеет пустой тип данных. В последовательности должно быть идентифицировано по крайней мере один элемент.

<a href="" id="path"></a>**Path (путь** ) Путь обрабатывается RegistrySetting и FileSetting, чтобы ссылаться на пути к реестру и файлам. Этот элемент поддерживает два необязательных атрибута: **recursive** и **DeleteIfNotFound**. Для обоих значений задано значение по умолчанию = "ложь".

Recursive указывает на то, что путь и все вложенные папки включены для параметров файла или все дочерние разделы реестра включены в параметры реестра. В обоих случаях все элементы на текущем уровне включаются в захваченные данные. Для объекта FileSettings все файлы в указанной папке включаются в данные, полученные UE-V, но папки не включаются. Для путей в реестре записываются все значения из текущего пути, но дочерние разделы реестра не фиксируются. В обоих случаях следует соблюдать осторожность, чтобы избежать захвата больших наборов данных или большого количества элементов.

Атрибут DeleteIfNotFound удаляет параметр из данных пути к хранилищу параметров пользователя. Это может быть предпочтительнее в случаях, когда при удалении этих параметров из пакета сохраняется большой объем дискового пространства на сервере файлов с путями хранилища параметров.

<a href="" id="filemask"></a>**FileMask** FileMask задает только определенные типы файлов для папки, определенной путем. Например, Path может быть `C:\users\username\files` и FileMask может `*.txt` содержать только текстовые файлы.

<a href="" id="registrysetting"></a>**RegistrySetting** RegistrySetting представляет контейнер для разделов реестра и значений, а также соответствующее требуемое поведение в части агента UE-V. В этом типе определено четыре дочерних элемента: **path**, **Name**, **Exclude**и последовательность значений **path** и **Name**.

<a href="" id="filesetting"></a>**FileSetting** FileSetting содержат параметры, связанные с путями к файлам и файлам. Определены четыре дочерних элемента: **root**, **path**, **FileMask**и **Exclude**. Root является обязательным условием, а другие — необязательными.

<a href="" id="settings"></a>**Параметры** Параметры — это контейнер для всех параметров, которые применяются к определенному шаблону. Она включает в себя экземпляры параметров реестра, файлов, SystemParameter и CustomAction, описанных выше. Кроме того, он также может содержать следующие дочерние элементы с описанными ниже поведениями.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Элемент</th>
<th align="left">Описание</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Асинхронная репликация</p></td>
<td align="left"><p>Пакеты асинхронных параметров применяются без блокирования запуска приложения, чтобы приложение не заблокировалось во время применения параметров. Это полезно для параметров, которые можно применять асинхронно, например с <code>get/set</code> помощью API-интерфейса, например SystemParameterSetting.</p></td>
</tr>
<tr class="even">
<td align="left"><p>PreventOverlappingSynchronization</p></td>
<td align="left"><p>По умолчанию UE-V сохраняет параметры для приложения только в том случае, если вы закрыли последний экземпляр приложения, использующего этот шаблон. Если для этого элемента задано значение false, UE-V экспортирует параметры, даже если запущены другие экземпляры приложения. Готовые шаблоны — те, которые включают раздел общего элемента, поставляемый с UE-V. Используйте этот флаг, чтобы разрешить общим параметрам возможность всегда экспортировать при закрытии приложения, а также запретить экспорт параметров приложения, пока не закроется последний экземпляр.</p></td>
</tr>
</tbody>
</table>

 

### <a href="" id="name"></a>Элемент Name

**Обязательно: истина**

**Тип: строка**

Name указывает уникальное имя шаблона расположения параметров. Этот элемент используется для отображения в целях создания ссылки на шаблон в WMI, PowerShell, просмотре событий и журналах отладки. Как правило, не следует ссылаться на сведения о версии, так как это может быть объектом из элемента ProductVersion. Например, укажите, `<Name>My Application</Name>` а не `<Name>My Application 1.1</Name>` .

**Примечание**  UE-V не ссылается на внешние DTD, поэтому невозможно использовать именованные сущности в шаблоне расположения параметров. Например, не используйте &reg; для ссылки на зарегистрированный знак товарного знака®. Вместо этого используйте канонические нумерованные ссылки, чтобы включить эти типы специальных знаков, например & \ #174 для символа®. Это правило применимо ко всем строковым значениям в этом документе.

<http://www.w3.org/TR/xhtml1/dtds.html>Для получения полного списка сущностей знаков. Документы в кодировке UTF-8 могут содержать символы Юникода напрямую. Сохранение шаблонов с помощью UE-V Generator автоматически преобразует сущности знаков в их представления Unicode.

 

### <a href="" id="id"></a>Элемент ID

**Обязательно: истина**

**Тип: строка**

Идентификатор заполняет уникальный идентификатор для определенного шаблона. Этот тег становится основным идентификатором, который агент UE-V использует для ссылки на шаблон во время выполнения (например, просмотр выходных данных командлетов PowerShell Get-UevTemplate и Get-UevTemplateProgram). В соответствии с соглашением этот тег не должен содержать пробелы, что упрощает сценарии. Номера версий приложений должны быть указаны в этом элементе, чтобы можно было легко идентифицировать шаблон, например `<ID>MicrosoftCalculator6</ID>` или `<ID>MicrosoftOffice2010Win64</ID>` .

### <a href="" id="version"></a>Элемент Version

**Обязательно: истина**

**Тип: целое число**

**Минимальное значение: 0**

**Максимальное значение: 2147483647**

Version определяет версию шаблона расположения параметров для администрирования отслеживания изменений. Генератор UE-V автоматически получает это количество на единицу каждый раз при сохранении шаблона. Обратите внимание, что это поле должно быть целым числом. дробные значения, например, `<Version>2.5</Version>` недопустимы.

**Подсказка:** Вы можете сохранять заметки об изменениях в версии с помощью тегов комментариев XML `<!-- -->` , например:

```xml
<!--
    Version History

    Version 1 Jul 05, 2012 Initial template created by Generator - Denise@Contoso.com
    Version 2 Jul 31, 2012 Added support for app.exe v2.1.3 - Mark@Contoso.com
    Version 3 Jan 01, 2013 Added font settings support - Mark@Contoso.com
    Version 4 Jan 31, 2013 Added support for plugin settings - Tony@Contoso.com
  -->
<Version>4</Version>
```

**Важно!**  Это значение запрашивается, чтобы определить, следует ли применять новую версию шаблона к существующему шаблону в следующих экземплярах:

-   При выполнении задачи "автоматическое обновление шаблона" в расписании

-   При выполнении командлета PowerShell Update-UevTemplate

-   Когда метод microsoft\\uev: SettingsLocationTemplate Update вызывается через WMI

 

### <a href="" id="author"></a>Элемент Author

**Обязательно: ложь**

**Тип: строка**

Автор определяет создателя шаблона расположения параметров. Поддерживаются два необязательных дочерних элемента: **имя** и **адрес электронной почты**. Оба атрибута являются необязательными, но если указан дочерний элемент электронной почты, он должен сопровождаться элементом name. Автор — это полное имя контакта в шаблоне расположения параметров, а адрес электронной почты должен указывать на адрес электронной почты автора. Мы рекомендуем использовать эти сведения в шаблонах, опубликованных в открытых источниках, например в [галерее Templates UE-V](https://gallery.technet.microsoft.com/site/search?f%5B0%5D.Type=RootCategory&f%5B0%5D.Value=UE-V).

### <a href="" id="processes"></a>Обработка и обработка элементов

**Обязательно: истина**

**Тип: элемент**

Процессы содержат по крайней мере один `<Process>` элемент, который, в свою очередь, включает следующие дочерние элементы: **имя_файла**, **архитектура**, **ProductName**, **FileDescription**, **ProductVersion**и **FileVersion**. Дочерний элемент filename является обязательным, а другие — необязательными. Полностью заполненный элемент включает теги, похожие на приведенный ниже.

```xml
<Process>
  <Filename>MyApplication.exe</Filename>
  <Architecture>Win64</Architecture>
  <ProductName> MyApplication </ProductName>
  <FileDescription>MyApplication.exe</FileDescription>
  <ProductVersion>
    <Major Minimum="2" Maximum="2" />
    <Minor Minimum="0" Maximum="0" />
    <Build Minimum="0" Maximum="0" />
    <Patch Minimum="5" Maximum="5" />
  </ProductVersion>
  <FileVersion>
    <Major Minimum="2" Maximum="2" />
    <Minor Minimum="0" Maximum="0" />
    <Build Minimum="0" Maximum="0" />
    <Patch Minimum="5" Maximum="5" />
  </FileVersion>
</Process>
```

### Файла

**Обязательно: истина**

**Тип: строка**

Filename указывает фактическое имя исполняемого файла в том виде, в котором оно отображается в файловой системе. Этот элемент задает основной критерий, который используется UE-V для оценки того, применяется ли шаблон к процессу или нет. Этот элемент должен быть указан в XML-файле шаблона расположения параметров.

Допустимые имена файлов не должны соответствовать регулярному выражению \ [^ \ \ \ \ \? \ \ | &lt; &gt; /: \] +, то есть они не могут содержать символы обратной косой черты, звездочки и знаки подстановки вопросительного знака, символ вертикальной черты, знак "больше или меньше" и знак прямой или двоеточие (\ \? \* | &lt; &gt; /или: символы.).

**Подсказка:** Для проверки строки с помощью этого регулярного выражения используйте командное окно PowerShell и подставьте имя исполняемого файла для **YourFileName**:

`"YourFileName.exe" -match  "[\\\?\*\|<>/:]+"`

Значение **true** указывает на то, что строка содержит недопустимые символы. Ниже приведены некоторые примеры недопустимых значений.

-   \\\\server\\share\\program.exe

-   Программа \ *. exe

-   Pro? ram.exe

-   Программа &lt; 1 &gt; . exe

**Примечание**  Генератор UE-V кодирует символы "больше" и "меньше" &gt; и &lt; соответственно.

 

В редких случаях значение FileName не обязательно должно включать расширение EXE, но оно должно быть задано как часть значения. Например, `<Filename>MyApplictication.exe</Filename>` следует указать вместо `<Filename>MyApplictication</Filename>` . Второй пример не применяет шаблон к процессу, если фактическим именем исполняемого файла является "MyApplication.exe".

### Архитектура

**Обязательно: ложь**

**Тип: архитектура (строка)**

Архитектура — это архитектура процессора, для которой был скомпилирован целевой исполняемый файл. Допустимые значения: Win32 для 32-разрядных приложений или Win64 для 64-разрядных приложений. Если он есть, этот тег ограничивает применимость шаблона расположения параметров для определенной архитектуры приложения. Например, Сравните пользовательский интерфейс%ProgramFiles%\\Microsoft Virtualization\\templates\\ MicrosoftOffice2010Win32.xml и MicrosoftOffice2010Win64.xml файлов, включенных в UE-V. Это полезно, когда относительные пути меняются между различными версиями исполняемого файла, а также в случае, если параметры были добавлены или удалены при переходе с одной архитектуры процессора на другую.

Если этот элемент отсутствует, шаблон расположения параметров игнорирует архитектуру процесса и применяется как в 32, так и в 64-разрядных процессах, если применяются имя файла и другие атрибуты.

**Примечание**  UE-V не поддерживает процессоры ARM в этой версии.

 

### ProductName

**Обязательно: ложь**

**Тип: строка**

ProductName — это необязательный элемент, используемый для идентификации продукта в целях администрирования или создания отчетов. Значение ProductName отличается от имени файла тем, что в нем нет ограничений регулярных выражений. Это позволяет более понятное описание процесса, в котором имя исполняемого файла может быть очевидным. Пример

```xml
<Process>
  <Filename>MyApplication.exe</Filename>
  <ProductName>My Application 6.x by Contoso.com</ProductName>
  <ProductVersion>
    <Major Minimum="6" Maximum="6" />
  </ProductVersion>
</Process>
```

### FileDescription

**Обязательно: ложь**

**Тип: строка**

FileDescription — необязательный тег, позволяющий административному описанию исполняемого файла. Это поле с произвольным текстом, которое может быть полезно при различении нескольких исполняемых файлов в пакете программного обеспечения, где необходимо идентифицировать функцию исполняемого файла.

Например, в подходящем приложении может быть полезно получать напоминания о функции двух исполняемых файлов (MyApplication.exe и MyApplicationHelper.exe), как показано ниже.

```xml
<Processes>
  <Process>
    <Filename>MyApplication.exe</Filename>
    <FileDescription>My Application Main Engine</ FileDescription>
    <ProductVersion>
      <Major Minimum="6" Maximum="6" />
    </ProductVersion>
  </Process>
  <Process>
    <Filename>MyApplicationHelper.exe</Filename>
    <FileDescription>My Application Background Process Executable</FileDescription>
    <ProductVersion>
      <Major Minimum="6" Maximum="6" />
    </ProductVersion>
  </Process>
</Processes>
```

### ProductVersion

**Обязательно: ложь**

**Тип: строка**

ProductVersion — это основная и младшая версии файла, а также сборка и уровень исправлений. ProductVersion является необязательным элементом, но, если он указан, он должен содержать по крайней мере основной дочерний элемент. Значение должно выражать диапазон в форме Minimum = "X" максимум = "Y", где X и Y — целые числа. Минимальное и максимальное значения могут быть одинаковыми.

Элементы "продукт" и "версия файла" могут остаться не установленными. Таким образом, шаблон "зависит от версии", то есть шаблон будет применяться ко всем версиям указанного исполняемого файла.

**Пример 1:**

Версия продукта: 1,0, указанная в генераторе UE-V, создает следующий XML-код:

```xml
<ProductVersion>
  <Major Minimum="1" Maximum="1" />
  <Minor Minimum="0" Maximum="0" />
</ProductVersion>
```

**Пример 2:**

Версия файла: 5.0.2.1000, указанная в генераторе UE-V, создает следующий XML-код:

```xml
<FileVersion>
  <Major Minimum="5" Maximum="5" />
  <Minor Minimum="0" Maximum="0" />
  <Build Minimum="2" Maximum="2" />
  <Patch Minimum="1000" Maximum="1000" />
</FileVersion>
```

**Недопустимый пример 1 — неполный диапазон:**

Присутствует только атрибут Minimum. Максимальное значение также должно быть включено в диапазон.

```xml
<ProductVersion>
  <Major Minimum="2" />
</ProductVersion>
```

**Недопустимый пример 2 — дополнительный номер без основного элемента:**

Присутствует только младший элемент. Кроме того, необходимо включить основную версию.

```xml
<ProductVersion>
  <Minor Minimum="0" Maximum="0" />
</ProductVersion>
```

### FileVersion

**Обязательно: ложь**

**Тип: строка**

FileVersion различает окончательную версию опубликованного приложения и сведения о внутренних сборках для исполняемого компонента. Для большинства коммерческих приложений эти номера идентичны. Там, где они различаются, версия продукта файла обозначает универсальную версию файла, в то время как версия файла указывает определенную сборку файла (как в случае исправления или обновления). Это однозначно определяет файлы без логики обнаружения нарушений.

Чтобы определить версию продукта и версию файла, щелкните его правой кнопкой мыши в проводнике Windows, выберите пункт Свойства, а затем откройте вкладку сведения.

Включение элемента FileVersion для приложения позволяет более детально настроить логику обнаружения, но это не требуется для большинства приложений. Сначала проверяются параметры элемента ProductVersion, а затем FileVersion установлен. Будет применяться более строгие настройки.

Дочерние элементы и правила синтаксиса для FileVersion идентичны методам из ProductVersion.

```xml
<Process>
  <Filename>MSACCESS.EXE</Filename>
  <Architecture>Win32</Architecture>
  <ProductVersion>
    <Major Minimum="14" Maximum="14" />
    <Minor Minimum="0" Maximum="0" />
  </ProductVersion>
  <FileVersion>
    <Major Minimum="14" Maximum="14" />
    <Minor Minimum="0" Maximum="0" />
  </FileVersion>
</Process>
```

### <a href="" id="application"></a>Элемент приложения

Приложение — это контейнер для параметров, которые применяются к определенному приложению. Это коллекция указанных ниже полей и типов.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Поле/Тип</th>
<th align="left">Описание</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Name</p></td>
<td align="left"><p>Задает уникальное имя для шаблона расположения параметров. Этот элемент используется для отображения в целях создания ссылки на шаблон в WMI, PowerShell, просмотре событий и журналах отладки. Дополнительные сведения можно найти в разделе <a href="#name" data-raw-source="[Name](#name)"> Name (имя) </a> .</p></td>
</tr>
<tr class="even">
<td align="left"><p>ID</p></td>
<td align="left"><p>Заполнение уникального идентификатора для определенного шаблона. Этот тег становится основным идентификатором, который агент UE-V использует для ссылки на шаблон во время выполнения. Дополнительные сведения можно найти в разделе <a href="#id" data-raw-source="[ID](#id)"> ID </a> .</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Описание</p></td>
<td align="left"><p>Необязательное описание шаблона.</p></td>
</tr>
<tr class="even">
<td align="left"><p>LocalizedNames</p></td>
<td align="left"><p>Необязательное имя, отображаемое в пользовательском интерфейсе, локализованное на языковой стандарт.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>LocalizedDescriptions</p></td>
<td align="left"><p>Необязательное описание шаблона, локализованное на языковой стандарт.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Версия</p></td>
<td align="left"><p>Определяет версию шаблона расположения параметров для администрирования отслеживания изменений. Дополнительные сведения можно найти в разделе <a href="#version" data-raw-source="[Version](#version)"> Version (версия) </a> .</p></td>
</tr>
<tr class="odd">
<td align="left"><p>DeferToMSAccount</p></td>
<td align="left"><p>Определяет, включен ли этот шаблон в сочетании с учетной записью Майкрософт или нет. Если для пользователя на компьютере включена синхронизация MSA, этот шаблон будет автоматически отключен.</p></td>
</tr>
<tr class="even">
<td align="left"><p>DeferToOffice365</p></td>
<td align="left"><p>Так же, как и MSA, это определяет, включен ли этот шаблон в сочетании с Office365. Если для синхронизации параметров используется Office 365, этот шаблон будет автоматически отключен.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Процессы</p></td>
<td align="left"><p>Контейнер для коллекции из одного или нескольких элементов процесса. Дополнительные сведения можно найти в разделе <a href="#processes" data-raw-source="[Processes](#processes)"> процессы </a> .</p></td>
</tr>
<tr class="even">
<td align="left"><p>Параметры</p></td>
<td align="left"><p>Контейнер для всех параметров, которые применяются к определенному шаблону. Она включает в себя экземпляры параметров реестра, файлов, SystemParameter и CustomAction. Дополнительные сведения можно найти <strong> в разделе </strong> Параметры <a href="#data" data-raw-source="[Data types](#data)"> типов данных </a> .</p></td>
</tr>
</tbody>
</table>

 

### <a href="" id="common"></a>Общий элемент

Общие похожи на элементы приложения, но всегда связаны с двумя или более элементами приложения. Общий раздел представляет набор параметров, которые совместно используются в этих экземплярах приложения. Это коллекция указанных ниже полей и типов.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Поле/Тип</th>
<th align="left">Описание</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Name</p></td>
<td align="left"><p>Задает уникальное имя для шаблона расположения параметров. Этот элемент используется для отображения в целях создания ссылки на шаблон в WMI, PowerShell, просмотре событий и журналах отладки. Дополнительные сведения можно найти в разделе <a href="#name" data-raw-source="[Name](#name)"> Name (имя) </a> .</p></td>
</tr>
<tr class="even">
<td align="left"><p>ID</p></td>
<td align="left"><p>Заполнение уникального идентификатора для определенного шаблона. Этот тег становится основным идентификатором, который агент UE-V использует для ссылки на шаблон во время выполнения. Дополнительные сведения можно найти в разделе <a href="#id" data-raw-source="[ID](#id)"> ID </a> .</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Описание</p></td>
<td align="left"><p>Необязательное описание шаблона.</p></td>
</tr>
<tr class="even">
<td align="left"><p>LocalizedNames</p></td>
<td align="left"><p>Необязательное имя, отображаемое в пользовательском интерфейсе, локализованное на языковой стандарт.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>LocalizedDescriptions</p></td>
<td align="left"><p>Необязательное описание шаблона, локализованное на языковой стандарт.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Версия</p></td>
<td align="left"><p>Определяет версию шаблона расположения параметров для администрирования отслеживания изменений. Дополнительные сведения можно найти в разделе <a href="#version" data-raw-source="[Version](#version)"> Version (версия) </a> .</p></td>
</tr>
<tr class="odd">
<td align="left"><p>DeferToMSAccount</p></td>
<td align="left"><p>Определяет, включен ли этот шаблон в сочетании с учетной записью Майкрософт или нет. Если для пользователя на компьютере включена синхронизация MSA, этот шаблон будет автоматически отключен.</p></td>
</tr>
<tr class="even">
<td align="left"><p>DeferToOffice365</p></td>
<td align="left"><p>Так же, как и MSA, это определяет, включен ли этот шаблон в сочетании с Office365. Если для синхронизации параметров используется Office 365, этот шаблон будет автоматически отключен.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Параметры</p></td>
<td align="left"><p>Контейнер для всех параметров, которые применяются к определенному шаблону. Она включает в себя экземпляры параметров реестра, файлов, SystemParameter и CustomAction. Дополнительные сведения можно найти <strong> в разделе </strong> Параметры <a href="#data" data-raw-source="[Data types](#data)"> типов данных </a> .</p></td>
</tr>
</tbody>
</table>

 

### <a href="" id="settingslocationtemplate"></a>Элемент SettingsLocationTemplate

Этот элемент определяет параметры отдельного приложения или набора приложений.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Поле/Тип</th>
<th align="left">Описание</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Name</p></td>
<td align="left"><p>Задает уникальное имя для шаблона расположения параметров. Этот элемент используется для отображения в целях создания ссылки на шаблон в WMI, PowerShell, просмотре событий и журналах отладки. Дополнительные сведения можно найти в разделе <a href="#name" data-raw-source="[Name](#name)"> Name (имя) </a> .</p></td>
</tr>
<tr class="even">
<td align="left"><p>ID</p></td>
<td align="left"><p>Заполнение уникального идентификатора для определенного шаблона. Этот тег становится основным идентификатором, который агент UE-V использует для ссылки на шаблон во время выполнения. Дополнительные сведения можно найти в разделе <a href="#id" data-raw-source="[ID](#id)"> ID </a> .</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Описание</p></td>
<td align="left"><p>Необязательное описание шаблона.</p></td>
</tr>
<tr class="even">
<td align="left"><p>LocalizedNames</p></td>
<td align="left"><p>Необязательное имя, отображаемое в пользовательском интерфейсе, локализованное на языковой стандарт.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>LocalizedDescriptions</p></td>
<td align="left"><p>Необязательное описание шаблона, локализованное на языковой стандарт.</p></td>
</tr>
</tbody>
</table>

 

### <a href="" id="appendix"></a>Приложение: SettingsLocationTemplate. xsd

Ниже приведен пример файла SettingsLocationTemplate. xsd, в котором показаны элементы, дочерние элементы, атрибуты и параметры.

```xml
<?xml version="1.0" encoding="utf-8"?>
<xs:schema id="UevSettingsLocationTemplate"
  targetNamespace="https://schemas.microsoft.com/UserExperienceVirtualization/2013/SettingsLocationTemplate"
  elementFormDefault="qualified"
  xmlns="https://schemas.microsoft.com/UserExperienceVirtualization/2013/SettingsLocationTemplate"
  xmlns:mstns="https://schemas.microsoft.com/UserExperienceVirtualization/2013/SettingsLocationTemplate"
  xmlns:xs="http://www.w3.org/2001/XMLSchema">

  <xs:simpleType name="Guid">
    <xs:restriction base="xs:string">
      <xs:pattern value="\{[a-fA-F0-9]{8}-[a-fA-F0-9]{4}-[a-fA-F0-9]{4}-[a-fA-F0-9]{4}-[a-fA-F0-9]{12}\}" />
    </xs:restriction>
  </xs:simpleType>

  <xs:simpleType name="FilenameString">
    <xs:restriction base="xs:string">
      <xs:pattern value="[^\\\?\*\|&lt;&gt;/:]+" />
    </xs:restriction>
  </xs:simpleType>

  <xs:simpleType name="IDString">
    <xs:restriction base="xs:string">
      <xs:pattern value="[^\\\?\*\|&lt;&gt;/:.]+" />
    </xs:restriction>
  </xs:simpleType>

  <xs:simpleType name="TemplateVersion">
    <xs:restriction base="xs:integer">
      <xs:minInclusive value="0" />
      <xs:maxInclusive value="2147483647" />
    </xs:restriction>
  </xs:simpleType>

  <xs:complexType name="Empty">
    <xs:sequence/>
  </xs:complexType>

  <xs:complexType name="LocalizedString">
    <xs:simpleContent>
      <xs:extension base="xs:string">
        <xs:attribute name="Locale" type="xs:string" use="required"/>
      </xs:extension>
    </xs:simpleContent>
  </xs:complexType>

  <xs:complexType name="LocalizedName">
    <xs:sequence>
      <xs:element name="Name" type="LocalizedString" minOccurs="1" maxOccurs="unbounded" />
    </xs:sequence>
  </xs:complexType>

  <xs:complexType name="LocalizedDescription">
    <xs:sequence>
      <xs:element name="Description" type="LocalizedString" minOccurs="1" maxOccurs="unbounded" />
    </xs:sequence>
  </xs:complexType>

  <xs:complexType name="Author">
    <xs:all>
      <xs:element name="Name" type="xs:string" minOccurs="1" />
      <xs:element name="Email" type="xs:string" minOccurs="0" />
    </xs:all>
  </xs:complexType>

  <xs:complexType name="Range">
    <xs:attribute name="Minimum" type="xs:integer" use="required"/>
    <xs:attribute name="Maximum" type="xs:integer" use="required"/>
  </xs:complexType>

  <xs:complexType name="ProcessVersion">
    <xs:sequence>
      <xs:element name="Major" type="Range" minOccurs="1" />
      <xs:element name="Minor" type="Range" minOccurs="0" />
      <xs:element name="Build" type="Range" minOccurs="0" />
      <xs:element name="Patch" type="Range" minOccurs="0" />
    </xs:sequence>
  </xs:complexType>

  <xs:simpleType name="Architecture">
    <xs:restriction base="xs:string">
      <xs:enumeration value="Win32"/>
      <xs:enumeration value="Win64"/>
    </xs:restriction>
  </xs:simpleType>

  <xs:complexType name="Process">
    <xs:sequence>
      <xs:element name="Filename" type="FilenameString" minOccurs="1" />
      <xs:element name="Architecture" type="Architecture" minOccurs="0" />
      <xs:element name="ProductName" type="xs:string" minOccurs="0" />
      <xs:element name="FileDescription" type="xs:string" minOccurs="0" />
      <xs:element name="ProductVersion" type="ProcessVersion" minOccurs="0" maxOccurs="unbounded"/>
      <xs:element name="FileVersion" type="ProcessVersion" minOccurs="0" maxOccurs="unbounded"/>
    </xs:sequence>
  </xs:complexType>

  <xs:complexType name="Processes">
    <xs:sequence>
      <xs:choice minOccurs="1">
        <xs:element name="Process" type="Process" />
        <xs:element name="ShellProcess" type="Empty" />
      </xs:choice>
      <xs:element name="Process" type="Process" minOccurs="0" maxOccurs="unbounded" />
    </xs:sequence>
  </xs:complexType>

  <xs:complexType name="Path">
    <xs:simpleContent>
      <xs:extension base="xs:string">
        <xs:attribute name="Recursive" type="xs:boolean" default="false"/>
        <xs:attribute name="DeleteIfNotFound" type="xs:boolean" default="false"/>
      </xs:extension>
    </xs:simpleContent>
  </xs:complexType>

  <xs:complexType name="RegistrySetting">
    <xs:sequence>
      <xs:element name="Path" type="Path" />
      <xs:element name="Name" type="xs:string" minOccurs="0" maxOccurs="unbounded" />
      <xs:element name="Exclude" minOccurs="0" maxOccurs="unbounded">
        <xs:complexType>
          <xs:sequence>
            <xs:element name="Path" type="Path" minOccurs="0" />
            <xs:element name="Name" type="xs:string" minOccurs="0" maxOccurs="unbounded" />
          </xs:sequence>
        </xs:complexType>
      </xs:element>
    </xs:sequence>
  </xs:complexType>

  <xs:complexType name="FileSetting">
    <xs:sequence>

      <xs:element name="Root">
        <xs:complexType>
          <xs:choice>
            <xs:element name="KnownFolder" type="Guid" />
            <xs:element name="RegistryEntry" type="xs:string" />
            <xs:element name="EnvironmentVariable" type="xs:string" />
          </xs:choice>
        </xs:complexType>
      </xs:element>

      <xs:element name="Path" minOccurs="0" type="Path" />
      <xs:element name="FileMask" type="xs:string" minOccurs="0" maxOccurs="unbounded"/>

      <xs:element name="Exclude" minOccurs="0" maxOccurs="unbounded">
        <xs:complexType>
          <xs:sequence>
            <xs:element name="Path" type="Path" minOccurs="0" />
            <xs:element name="FileMask" type="xs:string" minOccurs="0" maxOccurs="unbounded" />
          </xs:sequence>
        </xs:complexType>
      </xs:element>

    </xs:sequence>
  </xs:complexType>

  <xs:simpleType name="SystemParameterSetting">
    <xs:restriction base="xs:string">

      <!-- Accessibility parameters -->
      <xs:enumeration value="AccessTimeout"/>
      <xs:enumeration value="AudioDescription"/>
      <xs:enumeration value="ClientAreaAnimation"/>
      <xs:enumeration value="DisableOverlappedContent"/>
      <xs:enumeration value="FilterKeys"/>
      <xs:enumeration value="FocusBorderHeight"/>
      <xs:enumeration value="FocusBorderWidth"/>
      <xs:enumeration value="HighContrast"/>
      <xs:enumeration value="MessageDuration"/>
      <xs:enumeration value="MouseClickLock"/>
      <xs:enumeration value="MouseClickLockTime"/>
      <xs:enumeration value="MouseKeys"/>
      <xs:enumeration value="MouseSonar"/>
      <xs:enumeration value="MouseVanish"/>
      <xs:enumeration value="ScreenReader"/>
      <xs:enumeration value="ShowSounds"/>
      <xs:enumeration value="SoundSentry"/>
      <xs:enumeration value="StickyKeys"/>
      <xs:enumeration value="ToggleKeys"/>

      <!-- Input parameters -->
      <xs:enumeration value="Beep"/>
      <xs:enumeration value="BlockSendInputResets"/>
      <xs:enumeration value="DefaultInputLang"/>
      <xs:enumeration value="DoubleClickTime"/>
      <xs:enumeration value="DoubleClkHeight"/>
      <xs:enumeration value="DoubleClkWidth"/>
      <xs:enumeration value="KeyboardCues"/>
      <xs:enumeration value="KeyboardDelay"/>
      <xs:enumeration value="KeyboardPref"/>
      <xs:enumeration value="KeyboardSpeed"/>
      <xs:enumeration value="Mouse"/>
      <xs:enumeration value="MouseButtonSwap"/>
      <xs:enumeration value="MouseHoverHeight"/>
      <xs:enumeration value="MouseHoverTime"/>
      <xs:enumeration value="MouseHoverWidth"/>
      <xs:enumeration value="MouseSpeed"/>
      <xs:enumeration value="MouseTrails"/>
      <xs:enumeration value="SnapToDefButton"/>
      <xs:enumeration value="WheelScrollChars"/>
      <xs:enumeration value="WheelScrollLines"/>

      <!-- Desktop parameters (limited subset) -->
      <xs:enumeration value="DeskWallpaper"/>
      <xs:enumeration value="DesktopColor"/>

    </xs:restriction>
  </xs:simpleType>

  <xs:complexType name="Settings">
    <xs:sequence>
      <xs:element name="Asynchronous" type="xs:boolean" minOccurs="0" />
      <xs:element name="PreventOverlappingSynchronization" type="xs:boolean" minOccurs="0" />
      <xs:choice minOccurs="0" maxOccurs="unbounded">
        <xs:element name="Registry" type="RegistrySetting" />
        <xs:element name="File" type="FileSetting" />
        <xs:element name="SystemParameter" type="SystemParameterSetting" />
      </xs:choice>
    </xs:sequence>
  </xs:complexType>

  <xs:complexType name="Common">
    <xs:sequence>
      <xs:element name="Name" type="xs:string" />
      <xs:element name="ID" type="IDString" />
      <xs:element name="Description" type="xs:string" minOccurs="0" />
      <xs:element name="LocalizedNames" type="LocalizedName" minOccurs="0" />
      <xs:element name="LocalizedDescriptions" type="LocalizedDescription" minOccurs="0" />
      <xs:element name="Version" type="xs:integer" />
      <xs:element name="DeferToMSAccount" type="Empty"  minOccurs="0" />
      <xs:element name="Settings" type="Settings" />
    </xs:sequence>
  </xs:complexType>

  <xs:complexType name="Application">
    <xs:sequence>
      <xs:element name="Name" type="xs:string" />
      <xs:element name="ID" type="IDString" />
      <xs:element name="Description" type="xs:string" minOccurs="0" />
      <xs:element name="LocalizedNames" type="LocalizedName" minOccurs="0" />
      <xs:element name="LocalizedDescriptions" type="LocalizedDescription" minOccurs="0" />
      <xs:element name="Version" type="xs:integer" />
      <xs:element name="DeferToMSAccount" type="Empty"  minOccurs="0" />
      <xs:element name="Processes" type="Processes" />
      <xs:element name="Settings" type="Settings" />
    </xs:sequence>
  </xs:complexType>


  <xs:element name="SettingsLocationTemplate">
    <xs:complexType>
      <xs:sequence>

        <xs:element name="Name" type="xs:string" />
        <xs:element name="ID" type="IDString" />
        <xs:element name="Description" type="xs:string" minOccurs="0" />
        <xs:element name="LocalizedNames" type="LocalizedName" minOccurs="0" />
        <xs:element name="LocalizedDescriptions" type="LocalizedDescription" minOccurs="0" />

        <xs:choice>

          <!-- Single application -->
          <xs:sequence>
            <xs:element name="Version" type="TemplateVersion" />
            <xs:element name="Author" type="Author" minOccurs="0" />
            <xs:element name="DeferToMSAccount" type="Empty"  minOccurs="0" />
            <xs:element name="Processes" type="Processes" />
            <xs:element name="Settings" type="Settings" />
          </xs:sequence>

          <!-- Suite of applications -->
          <xs:sequence>
            <xs:element name="ManageSuiteOnly" type="xs:boolean" minOccurs="0" />
            <xs:element name="Author" type="Author" minOccurs="0" />
            <xs:element name="Common" type="Common" />
            <xs:element name="Application" type="Application" minOccurs="2" maxOccurs="unbounded" />
          </xs:sequence>

        </xs:choice>

      </xs:sequence>
    </xs:complexType>
  </xs:element>
  <!-- SettingsLocationTemplate -->

</xs:schema>
```






## Статьи по теме


[Работа с пользовательскими шаблонами UE-V 2. x и генератором UE-V 2. x](working-with-custom-ue-v-2x-templates-and-the-ue-v-2x-generator-new-uevv2.md)

[Технический справочник по UE-V 2.x](technical-reference-for-ue-v-2x-both-uevv2.md)

 

 






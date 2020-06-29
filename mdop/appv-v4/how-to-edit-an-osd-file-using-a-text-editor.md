---
title: Изменение файла OSD с помощью текстового редактора
description: Изменение файла OSD с помощью текстового редактора
author: dansimp
ms.assetid: f4263a1b-824f-49b9-8060-b8229c9d9960
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: c83547b38cee7e91e8348689583e0542a88dab83
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10817442"
---
# <span data-ttu-id="8dfa1-103">Изменение файла OSD с помощью текстового редактора</span><span class="sxs-lookup"><span data-stu-id="8dfa1-103">How to Edit an OSD File Using a Text Editor</span></span>


<span data-ttu-id="8dfa1-104">Чтобы изменить открытый файл дескриптора программного обеспечения (OSD) с помощью текстового редактора, выполните описанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="8dfa1-104">Use the following procedure to edit an Open Software Descriptor (OSD) file by using a text editor.</span></span>

**<span data-ttu-id="8dfa1-105">Редактирование OSD-файла с помощью текстового редактора</span><span class="sxs-lookup"><span data-stu-id="8dfa1-105">To edit an OSD file by using a text editor</span></span>**

1.  <span data-ttu-id="8dfa1-106">Откройте OSD-файл с помощью любого текстового редактора XML или ASCII — например, Microsoft Notepad.</span><span class="sxs-lookup"><span data-stu-id="8dfa1-106">Open the OSD file using any XML or ASCII text editor—for example, Microsoft Notepad.</span></span>

    <span data-ttu-id="8dfa1-107">**Примечание**  Перед изменением OSD-файла прочтите схему, предписанную XSD-файлом в каталоге установки.</span><span class="sxs-lookup"><span data-stu-id="8dfa1-107">**Note** Before modifying the OSD file, read the schema prescribed by the XSD file in the install directory.</span></span> <span data-ttu-id="8dfa1-108">Если не подписаться на эту схему, могут возникнуть ошибки, препятствующие запуску упорядоченного приложения.</span><span class="sxs-lookup"><span data-stu-id="8dfa1-108">Failing to follow this schema might introduce errors that prevent a sequenced application from starting successfully.</span></span>

     

2.  <span data-ttu-id="8dfa1-109">Измените файл OSD с помощью текстового редактора XML или ASCII, придерживаясь к предписанной схеме и следующим рекомендациям:</span><span class="sxs-lookup"><span data-stu-id="8dfa1-109">Edit the OSD file using your XML or ASCII text editor of choice, adhering to the prescribed schema and the following guidelines:</span></span>

    1.  <span data-ttu-id="8dfa1-110">Убедитесь, что именованные элементы вложены &lt; в &gt; корневой элемент SOFTPKG.</span><span class="sxs-lookup"><span data-stu-id="8dfa1-110">Ensure that named elements are nested within the &lt;SOFTPKG&gt; root element.</span></span>

    2.  <span data-ttu-id="8dfa1-111">Убедитесь в том, что имена элементов имеют все прописные буквы.</span><span class="sxs-lookup"><span data-stu-id="8dfa1-111">Ensure that element names are in all uppercase letters.</span></span>

    3.  <span data-ttu-id="8dfa1-112">Имейте в виду, что значения атрибутов чувствительны к регистру.</span><span class="sxs-lookup"><span data-stu-id="8dfa1-112">Be aware that attribute values are case sensitive.</span></span>

    4.  <span data-ttu-id="8dfa1-113">Вводите текст внимательно и проверяйте спецификацию XML.</span><span class="sxs-lookup"><span data-stu-id="8dfa1-113">Type carefully, and observe the XML specifications.</span></span>

## <span data-ttu-id="8dfa1-114">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="8dfa1-114">Related topics</span></span>


[<span data-ttu-id="8dfa1-115">Вкладка "Сведения об OSD"</span><span class="sxs-lookup"><span data-stu-id="8dfa1-115">About the OSD Tab</span></span>](about-the-osd-tab.md)

[<span data-ttu-id="8dfa1-116">Изменение файла OSD</span><span class="sxs-lookup"><span data-stu-id="8dfa1-116">How to Edit an OSD File</span></span>](how-to-edit-an-osd-file.md)

[<span data-ttu-id="8dfa1-117">Элементы файлов OSD</span><span class="sxs-lookup"><span data-stu-id="8dfa1-117">OSD File Elements</span></span>](osd-file-elements.md)

 

 






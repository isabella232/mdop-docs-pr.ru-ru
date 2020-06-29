---
title: Изменение размера кэша и букв дисков
description: Изменение размера кэша и букв дисков
author: dansimp
ms.assetid: e7d7b635-079e-41aa-a5e6-655f33b4e317
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: cf972f114845064ecf3027cf52d1a038dc6a5118
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10818039"
---
# <span data-ttu-id="ca0ee-103">Изменение размера кэша и букв дисков</span><span class="sxs-lookup"><span data-stu-id="ca0ee-103">How to Change the Cache Size and the Drive Letter Designation</span></span>


<span data-ttu-id="ca0ee-104">Изменить размер кэша и букву диска можно непосредственно из узла **Application Virtualization** в консоли управления клиентом Application Virtualization.</span><span class="sxs-lookup"><span data-stu-id="ca0ee-104">You can change the cache size and drive letter designation directly from the **Application Virtualization** node in the Application Virtualization Client Management Console.</span></span>

**<span data-ttu-id="ca0ee-105">Примечание.</span><span class="sxs-lookup"><span data-stu-id="ca0ee-105">Note</span></span>**  
<span data-ttu-id="ca0ee-106">После установки размера кэша его нельзя уменьшить.</span><span class="sxs-lookup"><span data-stu-id="ca0ee-106">After the cache size has been set, it cannot be made smaller.</span></span>



**<span data-ttu-id="ca0ee-107">Изменение размера кэша</span><span class="sxs-lookup"><span data-stu-id="ca0ee-107">To change the cache size</span></span>**

1.  <span data-ttu-id="ca0ee-108">Щелкните правой кнопкой мыши узел **Application Virtualization** и во всплывающем меню выберите пункт **свойства** .</span><span class="sxs-lookup"><span data-stu-id="ca0ee-108">Right-click the **Application Virtualization** node, and select **Properties** from the pop-up menu.</span></span>

2.  <span data-ttu-id="ca0ee-109">Выберите вкладку **Файловая система** в диалоговом окне **свойства** .</span><span class="sxs-lookup"><span data-stu-id="ca0ee-109">Select the **File System** tab on the **Properties** dialog box.</span></span> <span data-ttu-id="ca0ee-110">В разделе **Параметры конфигурации кэша клиента** выберите один из указанных ниже переключателей, чтобы выбрать способ управления пространством кэша.</span><span class="sxs-lookup"><span data-stu-id="ca0ee-110">In the **Client Cache Configuration Settings** section, click one of the following radio buttons to choose how to manage the cache space:</span></span>

    **<span data-ttu-id="ca0ee-111">Важно.</span><span class="sxs-lookup"><span data-stu-id="ca0ee-111">Important</span></span>**  
    <span data-ttu-id="ca0ee-112">Если вы выберете параметр " **использовать порог свободного места на диске** ", введенное значение будет указывать на общий размер кэша, а не на указанный вами порог свободного места на диске.</span><span class="sxs-lookup"><span data-stu-id="ca0ee-112">If you select the **Use free disk space threshold** setting, the value you enter will set the cache size to the total disk size minus the free disk space threshold number you entered.</span></span> <span data-ttu-id="ca0ee-113">Если вы хотите вернуться к использованию параметра **использовать максимальный размер кэша** , необходимо указать большее значение, чем существующий размер кэша.</span><span class="sxs-lookup"><span data-stu-id="ca0ee-113">If you then want revert to using the **Use maximum cache size** setting, you must specify a larger number than the existing cache size.</span></span> <span data-ttu-id="ca0ee-114">В противном случае появится сообщение об ошибке "новый размер должен быть больше существующего кэша".</span><span class="sxs-lookup"><span data-stu-id="ca0ee-114">Otherwise, the error “New size must be larger than the existing cache size” will appear.</span></span>



~~~
-   **Use maximum cache size**

    Enter a numeric value from 100 to 1,048,576 (1 TB) in the **Maximum size (MB)** field to specify the maximum size of the cache. The value shown in **Reserved Cache Size** indicates the amount of cache in use.

-   **Use free disk space threshold**

    Enter a numeric value to specify the amount of free disk space, in MB, that the cache must leave available on the disk. This allows the cache to grow until the amount of free disk space reaches this limit. The value shown in **Free disk space remaining** indicates how much disk space is unused.
~~~

3. <span data-ttu-id="ca0ee-115">Нажмите кнопку **ОК** или **Применить** , чтобы изменить параметр.</span><span class="sxs-lookup"><span data-stu-id="ca0ee-115">Click **OK** or **Apply** to change the setting.</span></span>

**<span data-ttu-id="ca0ee-116">Изменение обозначения диска</span><span class="sxs-lookup"><span data-stu-id="ca0ee-116">To change the drive letter designation</span></span>**

1.  <span data-ttu-id="ca0ee-117">Щелкните правой кнопкой мыши узел **Application Virtualization** и во всплывающем меню выберите пункт **свойства** .</span><span class="sxs-lookup"><span data-stu-id="ca0ee-117">Right-click the **Application Virtualization** node, and select **Properties** from the pop-up menu.</span></span>

2.  <span data-ttu-id="ca0ee-118">На вкладке **Файловая система** в диалоговом окне **свойства** в поле **диск для использования** выберите нужную букву диска из раскрывающегося списка доступных букв дисков.</span><span class="sxs-lookup"><span data-stu-id="ca0ee-118">On the **File System** tab in the **Properties** dialog box, in the **Drive to use** field, select the desired drive letter from the drop-down list of available drive letters.</span></span> <span data-ttu-id="ca0ee-119">Этот параметр вступает в силу после перезагрузки компьютера.</span><span class="sxs-lookup"><span data-stu-id="ca0ee-119">This setting becomes effective when the computer is rebooted.</span></span>

3.  <span data-ttu-id="ca0ee-120">Нажмите кнопку **ОК** или **Применить** , чтобы изменить параметр.</span><span class="sxs-lookup"><span data-stu-id="ca0ee-120">Click **OK** or **Apply** to change the setting.</span></span>

## <span data-ttu-id="ca0ee-121">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="ca0ee-121">Related topics</span></span>


[<span data-ttu-id="ca0ee-122">Настройка клиента в консоли управления клиентом Application Virtualization</span><span class="sxs-lookup"><span data-stu-id="ca0ee-122">How to Configure the Client in the Application Virtualization Client Management Console</span></span>](how-to-configure-the-client-in-the-application-virtualization-client-management-console.md)










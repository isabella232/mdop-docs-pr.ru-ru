---
title: Ограничение хранимых версий объекта групповой политики
description: Ограничение хранимых версий объекта групповой политики
author: dansimp
ms.assetid: da14edc5-0c36-4c54-b122-861c86b99eb1
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 20a3ae60cc330c27cbd19e943ba7f071d4ec60b1
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10820622"
---
# <span data-ttu-id="54acf-103">Ограничение хранимых версий объекта групповой политики</span><span class="sxs-lookup"><span data-stu-id="54acf-103">Limit the GPO Versions Stored</span></span>


<span data-ttu-id="54acf-104">По умолчанию все версии всех управляемых объектов групповой политики (GPO) сохраняются в архиве на сервере управления групповыми политиками.</span><span class="sxs-lookup"><span data-stu-id="54acf-104">By default, all versions of every controlled Group Policy Object (GPO) are retained in the archive on the AGPM Server.</span></span> <span data-ttu-id="54acf-105">Однако вы можете ограничить число хранимых версий для каждого объекта групповой политики и удалить старые версии при превышении этого ограничения.</span><span class="sxs-lookup"><span data-stu-id="54acf-105">However, you can limit the number of versions retained for each GPO and delete older versions when that limit is exceeded.</span></span> <span data-ttu-id="54acf-106">При удалении версий GPO запись версии сохраняется в истории объекта групповой политики, но сама версия GPO удаляется из архива.</span><span class="sxs-lookup"><span data-stu-id="54acf-106">When GPO versions are deleted, a record of the version remains in the history of the GPO, but the GPO version itself is deleted from the archive.</span></span>

<span data-ttu-id="54acf-107">Для выполнения этой процедуры требуется учетная запись пользователя с ролью администратора РАСШИРЕНного управления правами (полного доступа) или необходимых разрешений в расширенном управлении групповыми политиками.</span><span class="sxs-lookup"><span data-stu-id="54acf-107">A user account with the AGPM Administrator (Full Control) role or necessary permissions in Advanced Group Policy Management (AGPM) is required to complete this procedure.</span></span> <span data-ttu-id="54acf-108">Ознакомьтесь с подробными сведениями в разделе "Дополнительные сведения".</span><span class="sxs-lookup"><span data-stu-id="54acf-108">Review the details in "Additional considerations" in this topic.</span></span>

**<span data-ttu-id="54acf-109">Ограничение числа хранимых версий GPO</span><span class="sxs-lookup"><span data-stu-id="54acf-109">To limit the number of GPO versions stored</span></span>**

1.  <span data-ttu-id="54acf-110">В дереве **консоли управления групповыми политиками** нажмите кнопку **изменить элемент управления** в лесу и домене, в котором вы хотите управлять объектами групповой политики.</span><span class="sxs-lookup"><span data-stu-id="54acf-110">In the **Group Policy Management Console** tree, click **Change Control** in the forest and domain in which you want to manage GPOs.</span></span>

2.  <span data-ttu-id="54acf-111">В области сведений щелкните вкладку **сервер расширенного сервера** .</span><span class="sxs-lookup"><span data-stu-id="54acf-111">In the details pane, click the **AGPM Server** tab.</span></span>

3.  <span data-ttu-id="54acf-112">Установите флажок **удалить старые версии каждого объекта групповой политики из архива** и введите максимальное количество версий GPO, которое нужно сохранить для каждого объекта групповой политики, но не включая текущую версию.</span><span class="sxs-lookup"><span data-stu-id="54acf-112">Select the **Delete old versions of each GPO from the archive** check box, and type the maximum number of GPO versions to store for each GPO, not including the current version.</span></span> <span data-ttu-id="54acf-113">Чтобы сохранить только текущую версию, введите 0.</span><span class="sxs-lookup"><span data-stu-id="54acf-113">To retain only the current version, enter 0.</span></span> <span data-ttu-id="54acf-114">Максимальное значение должно быть не больше 999.</span><span class="sxs-lookup"><span data-stu-id="54acf-114">The maximum must be no greater than 999.</span></span>

    <span data-ttu-id="54acf-115">**Важно!**  Только версии объектов групповой политики, отображаемые на вкладке " **уникальные версии** " в окне **журнала** , предельное число.</span><span class="sxs-lookup"><span data-stu-id="54acf-115">**Important** Only GPO versions displayed on the **Unique Versions** tab of the **History** window count toward the limit.</span></span>

     

4.  <span data-ttu-id="54acf-116">Нажмите кнопку **Apply (применить** ).</span><span class="sxs-lookup"><span data-stu-id="54acf-116">Click the **Apply** button.</span></span>

### <span data-ttu-id="54acf-117">Дополнительные рекомендации</span><span class="sxs-lookup"><span data-stu-id="54acf-117">Additional considerations</span></span>

-   <span data-ttu-id="54acf-118">По умолчанию для выполнения этой процедуры необходимо быть администратором РАСШИРЕНной версии (полный доступ).</span><span class="sxs-lookup"><span data-stu-id="54acf-118">By default, you must be an AGPM Administrator (Full Control) to perform this procedure.</span></span> <span data-ttu-id="54acf-119">В частности, необходимо иметь **содержимое списка** и разрешения на **изменение параметров** домена.</span><span class="sxs-lookup"><span data-stu-id="54acf-119">Specifically, you must have **List Contents** and **Modify Options** permissions for the domain.</span></span>

-   <span data-ttu-id="54acf-120">Вы можете запретить удаление версии GPO, пометив ее в истории как непригодную для удаления.</span><span class="sxs-lookup"><span data-stu-id="54acf-120">You can prevent a GPO version from being deleted by marking it in the history as ineligible for deletion.</span></span> <span data-ttu-id="54acf-121">Для этого щелкните правой кнопкой мыши версию в истории объекта групповой политики и выберите пункт не **удалять**.</span><span class="sxs-lookup"><span data-stu-id="54acf-121">To do so, right-click the version in the history of the GPO and click **Do Not Delete**.</span></span>

### <span data-ttu-id="54acf-122">Дополнительные ссылки</span><span class="sxs-lookup"><span data-stu-id="54acf-122">Additional references</span></span>

-   [<span data-ttu-id="54acf-123">Управление архивами</span><span class="sxs-lookup"><span data-stu-id="54acf-123">Managing the Archive</span></span>](managing-the-archive.md)

 

 






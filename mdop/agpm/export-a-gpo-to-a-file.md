---
title: Экспорт объекта групповой политики в файл
description: Экспорт объекта групповой политики в файл
author: dansimp
ms.assetid: 0d01b1f7-a6a4-4d0d-9aa7-2d6f1ae93d9d
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 4622930cb0e5b439649cc0445ae2b3d02d7d3224
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10820852"
---
# <span data-ttu-id="40a4b-103">Экспорт объекта групповой политики в файл</span><span class="sxs-lookup"><span data-stu-id="40a4b-103">Export a GPO to a File</span></span>


<span data-ttu-id="40a4b-104">Вы можете экспортировать объект групповой политики (GPO) в CAB-файл, чтобы скопировать его в домен в другом лесе и импортировать этот объект в расширенном средстве управления групповыми политиками (ГРУППОВое управление) в этом домене.</span><span class="sxs-lookup"><span data-stu-id="40a4b-104">You can export a controlled Group Policy Object (GPO) to a CAB file so that you can copy it to a domain in another forest and import the GPO into Advanced Group Policy Management (AGPM) in that domain.</span></span> <span data-ttu-id="40a4b-105">Сведения о том, как импортировать параметры объекта групповой политики в новый или существующий объект групповой политики, приведены в разделе [Импорт объекта групповой политики из файла](import-a-gpo-from-a-file-ed.md).</span><span class="sxs-lookup"><span data-stu-id="40a4b-105">For information about how to import GPO settings into a new or existing GPO, see [Import a GPO from a File](import-a-gpo-from-a-file-ed.md).</span></span>

<span data-ttu-id="40a4b-106">Для выполнения этой процедуры требуется учетная запись пользователя с ролью редактора или администратора расширенного управления групповыми политиками (полный доступ) или необходимых разрешений в расширенном управлении групповой политикой (ГРУППОВое управление).</span><span class="sxs-lookup"><span data-stu-id="40a4b-106">A user account with the Editor or AGPM Administrator (Full Control) role or necessary permissions in Advanced Group Policy Management (AGPM) is required to complete this procedure.</span></span><span data-ttu-id="40a4b-107">Ознакомьтесь с подробными сведениями в разделе "Дополнительные сведения".</span><span class="sxs-lookup"><span data-stu-id="40a4b-107">Review the details in "Additional considerations" in this topic.</span></span>

**<span data-ttu-id="40a4b-108">Экспорт объекта групповой политики в файл</span><span class="sxs-lookup"><span data-stu-id="40a4b-108">To export a GPO to a file</span></span>**

1.  <span data-ttu-id="40a4b-109">В дереве **консоли управления групповыми политиками** нажмите кнопку **изменить элемент управления** в лесу и домене, в котором вы хотите управлять объектами групповой политики.</span><span class="sxs-lookup"><span data-stu-id="40a4b-109">In the **Group Policy Management Console** tree, click **Change Control** in the forest and domain in which you want to manage GPOs.</span></span>

2.  <span data-ttu-id="40a4b-110">На вкладке **содержание** откройте вкладку **Управление** , чтобы отобразить управляемые объекты групповой политики.</span><span class="sxs-lookup"><span data-stu-id="40a4b-110">On the **Contents** tab, click the **Controlled** tab to display the controlled GPOs.</span></span>

3.  <span data-ttu-id="40a4b-111">Щелкните объект групповой политики правой кнопкой мыши и выберите команду **Экспорт в**.</span><span class="sxs-lookup"><span data-stu-id="40a4b-111">Right-click the GPO, and then click **Export to**.</span></span>

4.  <span data-ttu-id="40a4b-112">Введите имя файла, в который нужно экспортировать объект групповой политики, и нажмите кнопку **Экспорт**.</span><span class="sxs-lookup"><span data-stu-id="40a4b-112">Enter a file name for the file to which you want to export the GPO, and then click **Export**.</span></span> <span data-ttu-id="40a4b-113">Если файл не существует, он будет создан.</span><span class="sxs-lookup"><span data-stu-id="40a4b-113">If the file does not exist, it is created.</span></span> <span data-ttu-id="40a4b-114">Если он уже существует, он заменяется.</span><span class="sxs-lookup"><span data-stu-id="40a4b-114">If it already exists, it is replaced.</span></span>

### <span data-ttu-id="40a4b-115">Дополнительные рекомендации</span><span class="sxs-lookup"><span data-stu-id="40a4b-115">Additional considerations</span></span>

-   <span data-ttu-id="40a4b-116">По умолчанию для выполнения этой процедуры необходимо быть редактором или администратором расширенного управления групповыми политиками (полный доступ).</span><span class="sxs-lookup"><span data-stu-id="40a4b-116">By default, you must be an Editor or an AGPM Administrator (Full Control) to perform this procedure.</span></span> <span data-ttu-id="40a4b-117">В частности, вы должны иметь разрешения на доступ к **списку**, **Чтение параметров**и **Экспорт** для GPO.</span><span class="sxs-lookup"><span data-stu-id="40a4b-117">Specifically, you must have **List Contents**, **Read Settings**, and **Export GPO** permissions for the GPO.</span></span>

### <span data-ttu-id="40a4b-118">Дополнительные ссылки</span><span class="sxs-lookup"><span data-stu-id="40a4b-118">Additional references</span></span>

-   [<span data-ttu-id="40a4b-119">Использование тестовой среды</span><span class="sxs-lookup"><span data-stu-id="40a4b-119">Using a Test Environment</span></span>](using-a-test-environment.md)

 

 






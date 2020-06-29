---
title: Изменение уровня ведения журнала сервера и параметров базы данных
description: Изменение уровня ведения журнала сервера и параметров базы данных
author: dansimp
ms.assetid: e3ebaee5-6c4c-4aa8-9766-c5aeb00f477a
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: bb35ac09c5e23f4847662171b68284f868e66dee
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10818032"
---
# <span data-ttu-id="4b3bc-103">Изменение уровня ведения журнала сервера и параметров базы данных</span><span class="sxs-lookup"><span data-stu-id="4b3bc-103">How to Change the Server Logging Level and the Database Parameters</span></span>


<span data-ttu-id="4b3bc-104">С помощью описанных ниже процедур вы можете изменить уровень ведения журнала и параметры журнала базы данных с помощью консоли управления сервером Application Virtualization.</span><span class="sxs-lookup"><span data-stu-id="4b3bc-104">You can use the following procedures to change the logging level and the database log parameters from the Application Virtualization Server Management Console.</span></span>

<span data-ttu-id="4b3bc-105">Доступны следующие уровни ведения журнала:</span><span class="sxs-lookup"><span data-stu-id="4b3bc-105">The following logging levels are available:</span></span>

-   <span data-ttu-id="4b3bc-106">Только транзакция</span><span class="sxs-lookup"><span data-stu-id="4b3bc-106">Transaction Only</span></span>

-   <span data-ttu-id="4b3bc-107">Неустранимые ошибки</span><span class="sxs-lookup"><span data-stu-id="4b3bc-107">Fatal Errors</span></span>

-   <span data-ttu-id="4b3bc-108">Ошибки</span><span class="sxs-lookup"><span data-stu-id="4b3bc-108">Errors</span></span>

-   <span data-ttu-id="4b3bc-109">Предупреждения и ошибки</span><span class="sxs-lookup"><span data-stu-id="4b3bc-109">Warnings/Errors</span></span>

-   <span data-ttu-id="4b3bc-110">Сведения, предупреждения и ошибки</span><span class="sxs-lookup"><span data-stu-id="4b3bc-110">Info/Warnings/Errors</span></span>

-   <span data-ttu-id="4b3bc-111">Подробный</span><span class="sxs-lookup"><span data-stu-id="4b3bc-111">Verbose</span></span>

<span data-ttu-id="4b3bc-112">**Примечание**  Из-за размера файла журнала, созданного при использовании режима **подробной информации** , рекомендуется не запускать рабочие серверы с таким уровнем набора журналов.</span><span class="sxs-lookup"><span data-stu-id="4b3bc-112">**Note** Because of the size of the log file produced when you use **Verbose** mode, the recommendation is that you do not run production servers with this level of logging set.</span></span>

 

<span data-ttu-id="4b3bc-113">Параметры ведения журнала базы данных определяют тип драйвера базы данных, учетные данные доступа и расположение базы данных протоколирования.</span><span class="sxs-lookup"><span data-stu-id="4b3bc-113">The database logging parameters determine the database driver type, access credentials, and location of the logging database.</span></span>

**<span data-ttu-id="4b3bc-114">Изменение уровня ведения журнала для серверов управления</span><span class="sxs-lookup"><span data-stu-id="4b3bc-114">To change the logging level for Management Servers</span></span>**

1.  <span data-ttu-id="4b3bc-115">Щелкните узел **группы серверов** , чтобы отобразить группы серверов.</span><span class="sxs-lookup"><span data-stu-id="4b3bc-115">Click the **Server Groups** node to display the server groups.</span></span>

2.  <span data-ttu-id="4b3bc-116">Щелкните группу сервера правой кнопкой мыши и выберите пункт **Свойства**.</span><span class="sxs-lookup"><span data-stu-id="4b3bc-116">Right-click the server group, and select **Properties**.</span></span>

3.  <span data-ttu-id="4b3bc-117">В диалоговом окне **Свойства** откройте вкладку **ведение журнала** .</span><span class="sxs-lookup"><span data-stu-id="4b3bc-117">In the **Properties** dialog box, select the **Logging** tab.</span></span>

4.  <span data-ttu-id="4b3bc-118">В диалоговом окне **Свойства группы серверов** выберите сервер и нажмите кнопку **изменить**.</span><span class="sxs-lookup"><span data-stu-id="4b3bc-118">In the **Server Group Properties** dialog box, select the server and then click **Edit**.</span></span>

5.  <span data-ttu-id="4b3bc-119">В диалоговом окне **Добавление и изменение модуля журнала** выберите уровень ведения журнала из раскрывающегося списка **Тип события** .</span><span class="sxs-lookup"><span data-stu-id="4b3bc-119">In the **Add/Edit Log Module** dialog box, select the logging level from the **Event Type** drop-down list.</span></span>

6.  <span data-ttu-id="4b3bc-120">Нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="4b3bc-120">Click **OK**.</span></span>

7.  <span data-ttu-id="4b3bc-121">В диалоговом окне **Свойства группы серверов** нажмите кнопку **ОК** или **Применить**.</span><span class="sxs-lookup"><span data-stu-id="4b3bc-121">In the **Server Group Properties** dialog box, click **OK** or **Apply**.</span></span>

**<span data-ttu-id="4b3bc-122">Изменение уровня ведения журнала для серверных потоков</span><span class="sxs-lookup"><span data-stu-id="4b3bc-122">To change the logging level for Streaming Servers</span></span>**

1.  <span data-ttu-id="4b3bc-123">Чтобы изменить уровень ведения журнала, измените значение в следующем разделе реестра:</span><span class="sxs-lookup"><span data-stu-id="4b3bc-123">Edit the following registry key value to change the logging level:</span></span>

    -   <span data-ttu-id="4b3bc-124">HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\DistributionServer\\LogLevel</span><span class="sxs-lookup"><span data-stu-id="4b3bc-124">HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\DistributionServer\\LogLevel</span></span>

2.  <span data-ttu-id="4b3bc-125">Выберите одно из следующих значений, чтобы задать уровень ведения журнала.</span><span class="sxs-lookup"><span data-stu-id="4b3bc-125">Select one of the following values to set the logging level.</span></span>

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left"><span data-ttu-id="4b3bc-126">Значение</span><span class="sxs-lookup"><span data-stu-id="4b3bc-126">Value</span></span></th>
    <th align="left"><span data-ttu-id="4b3bc-127">Уровень ведения журнала</span><span class="sxs-lookup"><span data-stu-id="4b3bc-127">Logging Level</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="4b3bc-128">до</span><span class="sxs-lookup"><span data-stu-id="4b3bc-128">0</span></span></p></td>
    <td align="left"><p><span data-ttu-id="4b3bc-129">Только транзакции</span><span class="sxs-lookup"><span data-stu-id="4b3bc-129">Transactions Only</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="4b3bc-130">1,1</span><span class="sxs-lookup"><span data-stu-id="4b3bc-130">1</span></span></p></td>
    <td align="left"><p><span data-ttu-id="4b3bc-131">Неустранимые ошибки</span><span class="sxs-lookup"><span data-stu-id="4b3bc-131">Fatal Errors</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="4b3bc-132">2</span><span class="sxs-lookup"><span data-stu-id="4b3bc-132">2</span></span></p></td>
    <td align="left"><p><span data-ttu-id="4b3bc-133">Ошибки</span><span class="sxs-lookup"><span data-stu-id="4b3bc-133">Errors</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="4b3bc-134">Трехконтактный</span><span class="sxs-lookup"><span data-stu-id="4b3bc-134">3</span></span></p></td>
    <td align="left"><p><span data-ttu-id="4b3bc-135">Предупреждения и ошибки</span><span class="sxs-lookup"><span data-stu-id="4b3bc-135">Warnings/Errors</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="4b3bc-136">четырехпроцессорном</span><span class="sxs-lookup"><span data-stu-id="4b3bc-136">4</span></span></p></td>
    <td align="left"><p><span data-ttu-id="4b3bc-137">Информация, предупреждения и ошибки</span><span class="sxs-lookup"><span data-stu-id="4b3bc-137">Information/ Warnings/Errors</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="4b3bc-138">5</span><span class="sxs-lookup"><span data-stu-id="4b3bc-138">5</span></span></p></td>
    <td align="left"><p><span data-ttu-id="4b3bc-139">Подробный</span><span class="sxs-lookup"><span data-stu-id="4b3bc-139">Verbose</span></span></p></td>
    </tr>
    </tbody>
    </table>

     

**<span data-ttu-id="4b3bc-140">Изменение параметров журнала базы данных</span><span class="sxs-lookup"><span data-stu-id="4b3bc-140">To change database log parameters</span></span>**

1.  <span data-ttu-id="4b3bc-141">Щелкните узел **группы серверов** , чтобы отобразить группы серверов.</span><span class="sxs-lookup"><span data-stu-id="4b3bc-141">Click the **Server Groups** node to display the server groups.</span></span>

2.  <span data-ttu-id="4b3bc-142">Щелкните группу сервера правой кнопкой мыши и выберите пункт **Свойства**.</span><span class="sxs-lookup"><span data-stu-id="4b3bc-142">Right-click the server group, and select **Properties**.</span></span>

3.  <span data-ttu-id="4b3bc-143">В диалоговом окне **Свойства** откройте вкладку **ведение журнала** .</span><span class="sxs-lookup"><span data-stu-id="4b3bc-143">In the **Properties** dialog box, select the **Logging** tab.</span></span>

4.  <span data-ttu-id="4b3bc-144">В диалоговом окне **Свойства группы серверов** выберите сервер и нажмите кнопку **изменить**.</span><span class="sxs-lookup"><span data-stu-id="4b3bc-144">In the **Server Group Properties** dialog box, select the server and then click **Edit**.</span></span>

5.  <span data-ttu-id="4b3bc-145">В диалоговом окне **Добавление и изменение модуля журнала** выберите драйвер базы данных из раскрывающегося списка **драйвер базы данных** .</span><span class="sxs-lookup"><span data-stu-id="4b3bc-145">In the **Add/Edit Log Module** dialog box, select a database driver from the **Database Driver** drop-down list.</span></span>

6.  <span data-ttu-id="4b3bc-146">Введите **имя узла DNS**.</span><span class="sxs-lookup"><span data-stu-id="4b3bc-146">Enter a **DNS Host Name**.</span></span>

7.  <span data-ttu-id="4b3bc-147">Установите флажок **динамически определять порт** или введите номер порта в поле " **порт** ".</span><span class="sxs-lookup"><span data-stu-id="4b3bc-147">Click the **Dynamically Determine Port** check box, or enter a port number in the **Port** field.</span></span>

8.  <span data-ttu-id="4b3bc-148">Введите **имя службы** в соответствующем поле.</span><span class="sxs-lookup"><span data-stu-id="4b3bc-148">Enter a **Service Name** in the corresponding field.</span></span>

9.  <span data-ttu-id="4b3bc-149">Нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="4b3bc-149">Click **OK**.</span></span>

10. <span data-ttu-id="4b3bc-150">В диалоговом окне **Свойства группы серверов** нажмите кнопку **ОК** или **Применить**.</span><span class="sxs-lookup"><span data-stu-id="4b3bc-150">On the **Server Group Properties** dialog box, click **OK** or **Apply**.</span></span>

## <span data-ttu-id="4b3bc-151">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="4b3bc-151">Related topics</span></span>


[<span data-ttu-id="4b3bc-152">Настройка системы Application Virtualization на консоли управления серверами</span><span class="sxs-lookup"><span data-stu-id="4b3bc-152">How to Customize an Application Virtualization System in the Server Management Console</span></span>](how-to-customize-an-application-virtualization-system-in-the-server-management-console.md)

 

 






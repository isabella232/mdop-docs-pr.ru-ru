---
title: Изменение размера кэша сервера
description: Изменение размера кэша сервера
author: dansimp
ms.assetid: 24e63744-21c3-458e-b137-9592f4fe785c
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 92e56a8a28f7a00d71805b497f9e404cca65919d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10818029"
---
# <span data-ttu-id="2beda-103">Изменение размера кэша сервера</span><span class="sxs-lookup"><span data-stu-id="2beda-103">How to Change the Server Cache Size</span></span>


<span data-ttu-id="2beda-104">Вы можете использовать описанную ниже процедуру, чтобы изменить размер кэша для любого сервера прямо из консоли управления сервером виртуализации приложений.</span><span class="sxs-lookup"><span data-stu-id="2beda-104">You can use the following procedure to change the cache size for any server directly from the Application Virtualization Server Management Console.</span></span>

<span data-ttu-id="2beda-105">**Примечание**  Несмотря на то, что вы можете изменить размер кэша, если только для вашей конфигурации вам не потребуется изменить размер, рекомендуется оставить для размера кэша значения, заданные по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="2beda-105">**Note** Although you can change the cache size, unless your configuration specifically requires you to change the size, it is recommended that you leave the cache size set to the default values.</span></span>

 

**<span data-ttu-id="2beda-106">Изменение размера кэша сервера</span><span class="sxs-lookup"><span data-stu-id="2beda-106">To change the server cache size</span></span>**

1.  <span data-ttu-id="2beda-107">Щелкните узел **группы серверов** на левой панели, чтобы развернуть список групп серверов.</span><span class="sxs-lookup"><span data-stu-id="2beda-107">Click the **Server Groups** node in the left pane to expand the list of server groups.</span></span>

2.  <span data-ttu-id="2beda-108">В области **результатов** дважды щелкните нужную группу серверов, чтобы отобразить список серверов в группе.</span><span class="sxs-lookup"><span data-stu-id="2beda-108">In the **Results** pane, double-click the desired server group to display the list of servers in the group.</span></span>

3.  <span data-ttu-id="2beda-109">В области **результатов** щелкните правой кнопкой мыши требуемый сервер и выберите пункт **свойства**.</span><span class="sxs-lookup"><span data-stu-id="2beda-109">In the **Results** pane, right-click the desired server and select **Properties**.</span></span>

4.  <span data-ttu-id="2beda-110">Откройте вкладку **Дополнительно** .</span><span class="sxs-lookup"><span data-stu-id="2beda-110">Select the **Advanced** tab.</span></span>

5.  <span data-ttu-id="2beda-111">Введите значение в поле **максимального выделения памяти** для кэша сервера и введите значение порога предупреждения в поле **предупреждать выделения памяти** .</span><span class="sxs-lookup"><span data-stu-id="2beda-111">Enter a value in the **Maximum Memory Allocation** field for the server cache, and enter a value for the threshold warning level in the **Warn Memory Allocation** field.</span></span>

6.  <span data-ttu-id="2beda-112">Введите значение в поле **максимального размера блока** .</span><span class="sxs-lookup"><span data-stu-id="2beda-112">Enter a value in the **Maximum Block Size** field.</span></span> <span data-ttu-id="2beda-113">Это число должно быть больше или равно максимальному размеру блока для максимального пакета, который будет передаваться на поток от сервера.</span><span class="sxs-lookup"><span data-stu-id="2beda-113">This number must be greater than or equal to the maximum block size of the largest package that will be streamed from the server.</span></span>

7.  <span data-ttu-id="2beda-114">Нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="2beda-114">Click **OK**.</span></span>

## <span data-ttu-id="2beda-115">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="2beda-115">Related topics</span></span>


[<span data-ttu-id="2beda-116">Изменение порта сервера</span><span class="sxs-lookup"><span data-stu-id="2beda-116">How to Change the Server Port</span></span>](how-to-change-the-server-port.md)

[<span data-ttu-id="2beda-117">Управление серверами на консоли управления серверами</span><span class="sxs-lookup"><span data-stu-id="2beda-117">How to Manage Servers in the Server Management Console</span></span>](how-to-manage-servers-in-the-server-management-console.md)

 

 






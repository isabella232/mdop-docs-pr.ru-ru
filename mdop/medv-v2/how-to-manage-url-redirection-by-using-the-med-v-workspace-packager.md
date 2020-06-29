---
title: Управление перенаправлением URL-адресов с помощью упаковщика рабочих областей MED-V
description: Управление перенаправлением URL-адресов с помощью упаковщика рабочих областей MED-V
author: dansimp
ms.assetid: 1a8d25af-479f-42d3-bf5f-c7fd974bbf8c
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 88167923e3bd47f2a3b0b3ada5e818715740dbe3
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10824819"
---
# <span data-ttu-id="97d70-103">Управление перенаправлением URL-адресов с помощью упаковщика рабочих областей MED-V</span><span class="sxs-lookup"><span data-stu-id="97d70-103">How to Manage URL Redirection by Using the MED-V Workspace Packager</span></span>


<span data-ttu-id="97d70-104">Вы можете использовать диспетчер рабочих областей MED-V для управления перенаправлением URL-адресов в рабочей области MED-V.</span><span class="sxs-lookup"><span data-stu-id="97d70-104">You can use the MED-V Workspace Packager to manage URL redirection in the MED-V workspace.</span></span>

**<span data-ttu-id="97d70-105">Управление перенаправлением веб-адресов в рабочей области MED-V</span><span class="sxs-lookup"><span data-stu-id="97d70-105">To manage web address redirection in a MED-V workspace</span></span>**

1.  <span data-ttu-id="97d70-106">Чтобы открыть **Диспетчер рабочих областей MED-V**, нажмите **кнопку Пуск**, выберите **все программы**, а затем — **Microsoft Enterprise Virtualization**, а затем — **Диспетчер рабочих областей med-v**.</span><span class="sxs-lookup"><span data-stu-id="97d70-106">To open the **MED-V Workspace Packager**, click **Start**, click **All Programs**, click **Microsoft Enterprise Desktop Virtualization**, and then click **MED-V Workspace Packager**.</span></span>

2.  <span data-ttu-id="97d70-107">На главной панели **диспетчера рабочих областей MED-V** выберите пункт **Управление перенаправлением веб-сайта**.</span><span class="sxs-lookup"><span data-stu-id="97d70-107">On the **MED-V Workspace Packager** main panel, click **Manage Web Redirection**.</span></span>

3.  <span data-ttu-id="97d70-108">В окне **Управление веб-перенаправлением** можно вводить, вставлять и импортировать список URL-адресов, перенаправленных в Internet Explorer в рабочей области MED-V.</span><span class="sxs-lookup"><span data-stu-id="97d70-108">In the **Manage Web Redirection** window, you can type, paste, or import a list of the URLs that are redirected to Internet Explorer in the MED-V workspace.</span></span>

    **<span data-ttu-id="97d70-109">Примечание.</span><span class="sxs-lookup"><span data-stu-id="97d70-109">Note</span></span>**  
    <span data-ttu-id="97d70-110">Перенаправление URL-адресов в MED-V поддерживает только протоколы HTTP и HTTPS.</span><span class="sxs-lookup"><span data-stu-id="97d70-110">URL redirection in MED-V only supports the protocols HTTP and HTTPS.</span></span> <span data-ttu-id="97d70-111">MED-V не обеспечивает поддержку FTP или других протоколов.</span><span class="sxs-lookup"><span data-stu-id="97d70-111">MED-V does not provide support for FTP or any other protocols.</span></span>



~~~
Enter each web address on a single line, for example:

http://www.contoso.com/webapps/webapp1

http://www.contoso.com/webapps/webapp2

http://\*.contoso.com

http://www.contoso.com/webapps/\*

**Important**  
If you import a text file that includes a URL that uses special characters (such as ~ ! @ \# and so on), make sure that you specify UTF-8 encoding when you save the text file. Special characters do not import correctly into the MED-V Workspace Packager if the text file was saved using the default ANSI encoding.
~~~



4. <span data-ttu-id="97d70-112">Нажмите кнопку **Сохранить как...**</span><span class="sxs-lookup"><span data-stu-id="97d70-112">Click **Save as…**</span></span> <span data-ttu-id="97d70-113">чтобы сохранить обновленные файлы перенаправления URL-адресов в указанной папке.</span><span class="sxs-lookup"><span data-stu-id="97d70-113">to save the updated URL redirection files in the specified folder.</span></span> <span data-ttu-id="97d70-114">MED-V создает файл реестра, содержащий обновленные сведения о перенаправлении URL-адреса.</span><span class="sxs-lookup"><span data-stu-id="97d70-114">MED-V creates a registry file that contains the updated URL redirection information.</span></span> <span data-ttu-id="97d70-115">Разверните обновленный раздел реестра с помощью групповой политики.</span><span class="sxs-lookup"><span data-stu-id="97d70-115">Deploy the updated registry key by using Group Policy.</span></span> <span data-ttu-id="97d70-116">Дополнительные сведения об использовании групповой политики можно найти в разделе [Установка программного обеспечения групповой политики](https://go.microsoft.com/fwlink/?LinkId=195931) ( https://go.microsoft.com/fwlink/?LinkId=195931) .</span><span class="sxs-lookup"><span data-stu-id="97d70-116">For more information about how to use Group Policy, see [Group Policy Software Installation](https://go.microsoft.com/fwlink/?LinkId=195931) (https://go.microsoft.com/fwlink/?LinkId=195931).</span></span>

   <span data-ttu-id="97d70-117">В заданной папке MED-V также создается сценарий Windows PowerShell, который можно использовать для повторного создания обновленного пакета рабочей области для MED-V.</span><span class="sxs-lookup"><span data-stu-id="97d70-117">MED-V also creates a Windows PowerShell script in the specified folder that you can use to re-create the updated MED-V workspace package.</span></span>

## <span data-ttu-id="97d70-118">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="97d70-118">Related topics</span></span>


[<span data-ttu-id="97d70-119">Добавление или удаление сведений о перенаправлении URL-адресов в развернутой рабочей области MED-V</span><span class="sxs-lookup"><span data-stu-id="97d70-119">How to Add or Remove URL Redirection Information in a Deployed MED-V Workspace</span></span>](how-to-add-or-remove-url-redirection-information-in-a-deployed-med-v-workspace.md)

[<span data-ttu-id="97d70-120">Управление перенаправлением URL-адресов MED-V</span><span class="sxs-lookup"><span data-stu-id="97d70-120">Manage MED-V URL Redirection</span></span>](manage-med-v-url-redirection.md)










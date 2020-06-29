---
title: Добавление пакета
description: Добавление пакета
author: dansimp
ms.assetid: 5407fdbe-e658-44f6-a9b8-a566b81dedce
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: c580d7d131017c52e278adda0208ffcb2e86ccf2
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10821399"
---
# <span data-ttu-id="7428c-103">Добавление пакета</span><span class="sxs-lookup"><span data-stu-id="7428c-103">How to Add a Package</span></span>


<span data-ttu-id="7428c-104">Вы можете добавить пакет из консоли управления сервером виртуализации приложений следующими способами:</span><span class="sxs-lookup"><span data-stu-id="7428c-104">You can add a package from the Application Virtualization Server Management Console in the following ways:</span></span>

-   <span data-ttu-id="7428c-105">Импортируйте приложение, которое автоматически создает пакет в процессе.</span><span class="sxs-lookup"><span data-stu-id="7428c-105">Import an application, which creates the package automatically in the process.</span></span>

-   <span data-ttu-id="7428c-106">Добавление пакета вручную.</span><span class="sxs-lookup"><span data-stu-id="7428c-106">Add a package manually.</span></span>

<span data-ttu-id="7428c-107">Рекомендуется импортировать приложения, а не добавлять их вручную.</span><span class="sxs-lookup"><span data-stu-id="7428c-107">It is recommended that you import applications instead of adding them manually.</span></span> <span data-ttu-id="7428c-108">Дополнительные сведения об импорте приложений вы узнаете, [как импортировать приложение](how-to-import-an-applicationserver.md).</span><span class="sxs-lookup"><span data-stu-id="7428c-108">For more information about importing applications, see [How to Import an Application](how-to-import-an-applicationserver.md).</span></span>

**<span data-ttu-id="7428c-109">Добавление пакета вручную</span><span class="sxs-lookup"><span data-stu-id="7428c-109">To add a package manually</span></span>**

1.  <span data-ttu-id="7428c-110">В консоли Управление сервером виртуализации приложений щелкните правой кнопкой мыши узел **пакеты** в левой области и выберите пункт **создать пакет**.</span><span class="sxs-lookup"><span data-stu-id="7428c-110">In the Application Virtualization Server Management Console, right-click the **Packages** node in the left pane and choose **New Package**.</span></span>

2.  <span data-ttu-id="7428c-111">В диалоговом окне **новый пакет** введите имя в поле **имя пакета** .</span><span class="sxs-lookup"><span data-stu-id="7428c-111">In the **New Package** dialog box, type a name in the **Package Name** field.</span></span>

3.  <span data-ttu-id="7428c-112">Найдите или введите имя пути в поле **полный путь к файлу пакета** .</span><span class="sxs-lookup"><span data-stu-id="7428c-112">Browse for or type a path name in the **Full path for package file** field.</span></span> <span data-ttu-id="7428c-113">Это должен быть SFT — файл.</span><span class="sxs-lookup"><span data-stu-id="7428c-113">This must be an SFT file.</span></span>

    <span data-ttu-id="7428c-114">**Примечание**  При переходе к SFT-файлу замените локальный путь (например, C:\\program Files Files\\User\ _Apps \\Virtual\ _App \ _Server \\Content) с помощью статического имени узла или IP-адреса сервера.</span><span class="sxs-lookup"><span data-stu-id="7428c-114">**Note** If you browse to the SFT file, replace the local path (such as C:\\Program Files\\User\_Apps\\Virtual\_App\_Server\\content) with the server's static host name or IP address.</span></span> <span data-ttu-id="7428c-115">Для использования переменной *% SFT \ _SOFTGRIDSERVER%* требуется конфигурация клиентского компьютера.</span><span class="sxs-lookup"><span data-stu-id="7428c-115">Using the variable *%SFT\_SOFTGRIDSERVER%* requires per-client computer configuration.</span></span>

    <span data-ttu-id="7428c-116">В диалоговых окнах, которые ссылаются на виртуальные серверы приложений, необходимо использовать сетевое расположение (например, имя или IP-адрес сервера), к которому пользователи могут получить доступ.</span><span class="sxs-lookup"><span data-stu-id="7428c-116">In dialog boxes that refer to Virtual Application Servers, you must use a network location, such as the server's static host name or IP address, that your users can access.</span></span> <span data-ttu-id="7428c-117">Открытый файл дескриптора программного обеспечения (OSD) приложения может заменить заполнитель переменную-заполнителем *% SFT \ _SOFTGRIDSERER%* с использованием статического имени узла или IP – адреса сервера.</span><span class="sxs-lookup"><span data-stu-id="7428c-117">The application's Open Software Descriptor (OSD) file can replace the placeholder variable *%SFT\_SOFTGRIDSERER%* with the server's static host name or IP address.</span></span> <span data-ttu-id="7428c-118">Если вы оставите заполнитель переменной, вы должны установить эту переменную на каждом клиентском компьютере, который будет иметь доступ к этому серверу.</span><span class="sxs-lookup"><span data-stu-id="7428c-118">If you leave the placeholder variable, you must set this variable on each client computer that will access that server.</span></span> <span data-ttu-id="7428c-119">Настройте пользовательскую или системную переменную на каждом компьютере для SFT \ _SOFTGRIDSERVER.</span><span class="sxs-lookup"><span data-stu-id="7428c-119">Set a User or System variable on each computer for SFT\_SOFTGRIDSERVER.</span></span> <span data-ttu-id="7428c-120">Значение переменной должно быть статическим именем узла или IP-адресом сервера.</span><span class="sxs-lookup"><span data-stu-id="7428c-120">The variable value must be the server's static host name or IP address.</span></span> <span data-ttu-id="7428c-121">Если вы задаете переменную, выйдите из сеанса клиента, выйдите из нее и вернитесь в Microsoft Windows, а затем перезапустите сеанс на всех компьютерах, на которых запущен сеанс, и у которого установлен параметр Variable.</span><span class="sxs-lookup"><span data-stu-id="7428c-121">If you set a variable, exit the Client session, log out of and back into Microsoft Windows, and then restart the session on each computer that had a session running and had the variable set.</span></span>

     

4.  <span data-ttu-id="7428c-122">Нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="7428c-122">Click **Next**.</span></span>

5.  <span data-ttu-id="7428c-123">В диалоговом окне **Сводка** показано расположение файла и запрос на его копирование, если он еще не указан.</span><span class="sxs-lookup"><span data-stu-id="7428c-123">The **Summary** dialog box shows the file location and prompts you to copy the file to the location if you have not already done so.</span></span> <span data-ttu-id="7428c-124">После проверки данных нажмите кнопку **Готово** .</span><span class="sxs-lookup"><span data-stu-id="7428c-124">Click **Finish** after you have verified the information.</span></span>

    <span data-ttu-id="7428c-125">**Примечание**  Если вы управляете приложениями на удаленном сервере, в следующем диалоговом окне введите путь к файлу относительно корневого элемента содержимого сервера.</span><span class="sxs-lookup"><span data-stu-id="7428c-125">**Note** If you are managing applications on a remote server, in the next dialog box, type only the path of the file relative to the server's content root.</span></span>

     

## <span data-ttu-id="7428c-126">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="7428c-126">Related topics</span></span>


[<span data-ttu-id="7428c-127">Импорт приложения</span><span class="sxs-lookup"><span data-stu-id="7428c-127">How to Import an Application</span></span>](how-to-import-an-applicationserver.md)

[<span data-ttu-id="7428c-128">Управление пакетами на консоли управления серверами</span><span class="sxs-lookup"><span data-stu-id="7428c-128">How to Manage Packages in the Server Management Console</span></span>](how-to-manage-packages-in-the-server-management-console.md)

 

 






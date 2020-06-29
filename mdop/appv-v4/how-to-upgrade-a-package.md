---
title: Обновление пакета
description: Обновление пакета
author: dansimp
ms.assetid: 831c7556-6f6c-4b3a-aefb-26889094dc1a
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 0a9b3eca2c996337d79e551784818a421f495316
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10816502"
---
# <span data-ttu-id="85356-103">Обновление пакета</span><span class="sxs-lookup"><span data-stu-id="85356-103">How to Upgrade a Package</span></span>


<span data-ttu-id="85356-104">Процесс автоматического обновления такой же, как и для добавления версии пакета в консоли управления сервером Application Virtualization.</span><span class="sxs-lookup"><span data-stu-id="85356-104">The process for an automatic upgrade is the same as for adding a package version in the Application Virtualization Server Management Console.</span></span> <span data-ttu-id="85356-105">Автоматическое обновление выполняется при переупорядочении приложения в существующем пакете.</span><span class="sxs-lookup"><span data-stu-id="85356-105">An automatic upgrade is performed when you resequence the application in an existing package.</span></span> <span data-ttu-id="85356-106">Затем вы можете добавить эту новую версию на серверы для потоковой передачи.</span><span class="sxs-lookup"><span data-stu-id="85356-106">Then you can add this new version to your servers for streaming.</span></span>

<span data-ttu-id="85356-107">Когда вы обновляете пакет с помощью новой версии, вы можете оставить существующую версию на своем место или удалить, а затем оставить только последнюю из них.</span><span class="sxs-lookup"><span data-stu-id="85356-107">When you upgrade a package with a new version, you can leave the existing version in place or delete it and leave only the newest one.</span></span> <span data-ttu-id="85356-108">Вы можете оставить старую версию для обеспечения совместимости с устаревшими документами или протестировать новую версию перед тем, как сделать ее доступной для всех пользователей.</span><span class="sxs-lookup"><span data-stu-id="85356-108">You might want to leave the old version in place for compatibility with legacy documents or so that you can test the new version before making it available to all users.</span></span>

**<span data-ttu-id="85356-109">Автоматическое обновление пакета</span><span class="sxs-lookup"><span data-stu-id="85356-109">To upgrade a package automatically</span></span>**

1.  <span data-ttu-id="85356-110">Скопируйте новый SFT-файл в папку содержимого сервера Application Virtualization.</span><span class="sxs-lookup"><span data-stu-id="85356-110">Copy the new SFT file to the Application Virtualization Server's content folder.</span></span>

    <span data-ttu-id="85356-111">**Примечание**  Если в ходе повторной последовательности не были добавлены функции, которые изменили файлы дескрипторов программного обеспечения (OSD), значка (ICO) или секвенсора (SPRJ), вам не нужно их копировать.</span><span class="sxs-lookup"><span data-stu-id="85356-111">**Note** If resequencing did not add features that changed the Open Software Descriptor (OSD), icon (ICO), or Sequencer Project (SPRJ) files, you do not need to copy those.</span></span> <span data-ttu-id="85356-112">Вы можете включить эти файлы, если хотите, чтобы все эти файлы отображались одинаковой датой.</span><span class="sxs-lookup"><span data-stu-id="85356-112">You can include these files if you want all these files to display the same date.</span></span>

     

2.  <span data-ttu-id="85356-113">В левой области консоли управления сервером виртуализации приложений разверните раздел **пакеты**.</span><span class="sxs-lookup"><span data-stu-id="85356-113">In left pane of the Application Virtualization Server Management Console, expand **Packages**.</span></span>

3.  <span data-ttu-id="85356-114">Щелкните правой кнопкой мыши пакет, который вы хотите обновить, и выберите команду **Добавить версию**.</span><span class="sxs-lookup"><span data-stu-id="85356-114">Right-click the package you want to upgrade, and select **Add Version**.</span></span>

4.  <span data-ttu-id="85356-115">В диалоговом окне **Добавить версию пакета** найдите и введите полный путь к новой версии приложения в поле **файл** .</span><span class="sxs-lookup"><span data-stu-id="85356-115">In the **Add Package Version** dialog box, browse for or type the full path name for the new application version in the **Full Path for the file** field.</span></span> <span data-ttu-id="85356-116">Это должен быть SFT — файл.</span><span class="sxs-lookup"><span data-stu-id="85356-116">This must be an SFT file.</span></span>

5.  <span data-ttu-id="85356-117">Нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="85356-117">Click **Next**.</span></span>

6.  <span data-ttu-id="85356-118">В диалоговом окне **Сводка** показано расположение файла и запрос на его копирование, если вы еще не сделали этого.</span><span class="sxs-lookup"><span data-stu-id="85356-118">The **Summary** dialog box shows the file location and prompts you to copy the file there if you have not already done so.</span></span> <span data-ttu-id="85356-119">После проверки данных нажмите кнопку **Готово** .</span><span class="sxs-lookup"><span data-stu-id="85356-119">Click **Finish** after you have verified the information.</span></span>

    <span data-ttu-id="85356-120">Новая версия теперь завершена и готова к потоку.</span><span class="sxs-lookup"><span data-stu-id="85356-120">The new version is now complete and ready to stream.</span></span>

## <span data-ttu-id="85356-121">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="85356-121">Related topics</span></span>


[<span data-ttu-id="85356-122">Управление пакетами на консоли управления серверами</span><span class="sxs-lookup"><span data-stu-id="85356-122">How to Manage Packages in the Server Management Console</span></span>](how-to-manage-packages-in-the-server-management-console.md)

 

 






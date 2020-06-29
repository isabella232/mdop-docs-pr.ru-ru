---
title: Добавление версии пакета
description: Добавление версии пакета
author: dansimp
ms.assetid: dbb829c1-e5cb-4a2f-bc17-9a9bb50c671c
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: a60252e8b43af61ad548df30a93d8fbc9bae0cb7
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10821402"
---
# <span data-ttu-id="fbb33-103">Добавление версии пакета</span><span class="sxs-lookup"><span data-stu-id="fbb33-103">How to Add a Package Version</span></span>


<span data-ttu-id="fbb33-104">С помощью описанной ниже процедуры вы можете добавить новую версию на серверы для потоковой передачи в консоли управления сервером Application Virtualization при переупорядочении пакета.</span><span class="sxs-lookup"><span data-stu-id="fbb33-104">In the Application Virtualization Server Management Console, when you resequence a package, you can use the following procedure to add the new version to your servers for streaming.</span></span>

<span data-ttu-id="fbb33-105">**Примечание**  Когда вы обновляете пакет с помощью новой версии, вы можете оставить существующую версию на своем место или удалить, а затем оставить только последнюю из них.</span><span class="sxs-lookup"><span data-stu-id="fbb33-105">**Note** When you upgrade a package with a new version, you can leave the existing version in place or delete it and leave only the newest one.</span></span> <span data-ttu-id="fbb33-106">Вы можете оставить старую версию для обеспечения совместимости с устаревшими документами или протестировать новую версию перед тем, как сделать ее доступной для всех пользователей.</span><span class="sxs-lookup"><span data-stu-id="fbb33-106">You might want to leave the old version in place for compatibility with legacy documents or so that you can test the new version before making it available to all users.</span></span>

 

**<span data-ttu-id="fbb33-107">Добавление версии пакета</span><span class="sxs-lookup"><span data-stu-id="fbb33-107">To add a package version</span></span>**

1.  <span data-ttu-id="fbb33-108">Скопируйте новый SFT-файл в папку содержимого сервера приложений.</span><span class="sxs-lookup"><span data-stu-id="fbb33-108">Copy the new SFT file to the application server's content folder.</span></span> <span data-ttu-id="fbb33-109">Если при повторной последовательности не были добавлены изменения в файлы Open дескриптор программного обеспечения (OSD), Icon (ICO) или Project Sequencer (SPRJ), их не нужно копировать.</span><span class="sxs-lookup"><span data-stu-id="fbb33-109">If resequencing did not add changes to the Open Software Descriptor (OSD), icon (ICO), or Sequencer Project (SPRJ) files, you do not need to copy those.</span></span> <span data-ttu-id="fbb33-110">Вы можете включить эти файлы, если хотите, чтобы все файлы отображались одинаковой датой.</span><span class="sxs-lookup"><span data-stu-id="fbb33-110">You can include those files if you want all the files to display the same date.</span></span>

2.  <span data-ttu-id="fbb33-111">В левой области консоли управления сервером виртуализации приложений разверните узел **пакеты** .</span><span class="sxs-lookup"><span data-stu-id="fbb33-111">In left pane of the Application Virtualization Server Management Console, expand the **Packages** node.</span></span>

3.  <span data-ttu-id="fbb33-112">Щелкните правой кнопкой мыши пакет, который вы хотите обновить, и выберите команду **Добавить версию**.</span><span class="sxs-lookup"><span data-stu-id="fbb33-112">Right-click the package you want to upgrade, and choose **Add Version**.</span></span>

4.  <span data-ttu-id="fbb33-113">В диалоговом окне **Добавить версию пакета** найдите или введите имя нового файла приложения в поле **полный путь к файлу пакета** .</span><span class="sxs-lookup"><span data-stu-id="fbb33-113">In the **Add Package Version** dialog box, browse for or type the path name for the new application file in the **Full path for package file** field.</span></span> <span data-ttu-id="fbb33-114">Это должен быть SFT — файл.</span><span class="sxs-lookup"><span data-stu-id="fbb33-114">This must be an SFT file.</span></span>

5.  <span data-ttu-id="fbb33-115">Нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="fbb33-115">Click **Next**.</span></span>

6.  <span data-ttu-id="fbb33-116">В диалоговом окне **Сводка** показано расположение файла и запрос на его копирование, если вы еще не сделали этого.</span><span class="sxs-lookup"><span data-stu-id="fbb33-116">The **Summary** dialog box shows the file location and prompts you to copy the file there if you have not already done so.</span></span> <span data-ttu-id="fbb33-117">После проверки данных нажмите кнопку **Готово** .</span><span class="sxs-lookup"><span data-stu-id="fbb33-117">Click **Finish** after you have verified the information.</span></span>

    <span data-ttu-id="fbb33-118">Новая версия теперь завершена и готова к потоку.</span><span class="sxs-lookup"><span data-stu-id="fbb33-118">The new version is now complete and ready to stream.</span></span>

## <span data-ttu-id="fbb33-119">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="fbb33-119">Related topics</span></span>


[<span data-ttu-id="fbb33-120">Удаление пакета</span><span class="sxs-lookup"><span data-stu-id="fbb33-120">How to Delete a Package</span></span>](how-to-delete-a-packageserver.md)

[<span data-ttu-id="fbb33-121">Управление пакетами на консоли управления серверами</span><span class="sxs-lookup"><span data-stu-id="fbb33-121">How to Manage Packages in the Server Management Console</span></span>](how-to-manage-packages-in-the-server-management-console.md)

 

 






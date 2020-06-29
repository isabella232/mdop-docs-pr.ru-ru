---
title: Добавление сервера
description: Добавление сервера
author: dansimp
ms.assetid: 1f31678a-8edf-4d35-a812-e4a2abfd979b
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 7d08b79bcbf34910ce357f39635431d11e3e99bd
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10821389"
---
# <span data-ttu-id="41a58-103">Добавление сервера</span><span class="sxs-lookup"><span data-stu-id="41a58-103">How to Add a Server</span></span>


<span data-ttu-id="41a58-104">Чтобы упростить управление серверами управления виртуализацией приложений, упорядочите их в группы сервера.</span><span class="sxs-lookup"><span data-stu-id="41a58-104">To help you manage your Application Virtualization Management Servers more efficiently, organize them into server groups.</span></span> <span data-ttu-id="41a58-105">После того как вы создадите группу серверов в консоли управления сервером Application Virtualization, вы можете добавить сервер в группу с помощью описанной ниже процедуры.</span><span class="sxs-lookup"><span data-stu-id="41a58-105">After you create a server group in the Application Virtualization Server Management Console, you can use the following procedure to add a server to the group.</span></span>

<span data-ttu-id="41a58-106">**Примечание**  Все серверы в группе сервера должны быть подключены к одному хранилищу данных.</span><span class="sxs-lookup"><span data-stu-id="41a58-106">**Note** All servers in a server group must be connected to the same data store.</span></span>

 

**<span data-ttu-id="41a58-107">Добавление сервера в группу</span><span class="sxs-lookup"><span data-stu-id="41a58-107">To add a server to a group</span></span>**

1.  <span data-ttu-id="41a58-108">Щелкните узел **группы серверов** на левой панели, чтобы развернуть список групп серверов.</span><span class="sxs-lookup"><span data-stu-id="41a58-108">Click the **Server Groups** node in the left pane to expand the list of server groups.</span></span>

2.  <span data-ttu-id="41a58-109">Щелкните правой кнопкой мыши нужную группу серверов и выберите пункт **создать сервер управления виртуализацией приложений**.</span><span class="sxs-lookup"><span data-stu-id="41a58-109">Right-click the desired server group, and select **New Application Virtualization Management Server**.</span></span>

3.  <span data-ttu-id="41a58-110">В **мастере создания новой группы серверов**введите **Отображаемое имя** и **имя узла DNS**.</span><span class="sxs-lookup"><span data-stu-id="41a58-110">In the **New Server Group Wizard**, enter the **Display Name** and the **DNS Host Name**.</span></span>

4.  <span data-ttu-id="41a58-111">Оставьте значения по умолчанию в поле **максимального выделения памяти** для серверного кэша и в поле **предупреждать о выделении памяти** укажите порог предупреждений.</span><span class="sxs-lookup"><span data-stu-id="41a58-111">Leave the default values in the **Maximum Memory Allocation** field for the server cache and the **Warn Memory Allocation** field to specify the threshold warning level.</span></span>

5.  <span data-ttu-id="41a58-112">Нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="41a58-112">Click **Next**.</span></span>

6.  <span data-ttu-id="41a58-113">В диалоговом окне **режим безопасности подключения** установите флажок **использовать повышенную** безопасность, если требуется.</span><span class="sxs-lookup"><span data-stu-id="41a58-113">In the **Connection Security Mode** dialog, check the **Use enhanced security** box to select enhanced security mode, if desired.</span></span> <span data-ttu-id="41a58-114">При необходимости завершите **работу мастера сертификатов** или просмотрите существующие сертификаты.</span><span class="sxs-lookup"><span data-stu-id="41a58-114">If necessary, complete the **Certificate Wizard** or view existing certificates.</span></span>

7.  <span data-ttu-id="41a58-115">Нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="41a58-115">Click **Next**.</span></span>

8.  <span data-ttu-id="41a58-116">В диалоговом окне **Параметры порта virt** выберите параметр **использовать порт по умолчанию** или переключатель **пользовательского порта** и введите номер пользовательского порта.</span><span class="sxs-lookup"><span data-stu-id="41a58-116">In the **App Virt Port Setting** dialog, select the **Use Default Port** or the **User Custom Port** radio button and enter the custom port number.</span></span>

9.  <span data-ttu-id="41a58-117">Нажмите кнопку **Готово**.</span><span class="sxs-lookup"><span data-stu-id="41a58-117">Click **Finish**.</span></span>

## <span data-ttu-id="41a58-118">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="41a58-118">Related topics</span></span>


[<span data-ttu-id="41a58-119">Создание группы серверов</span><span class="sxs-lookup"><span data-stu-id="41a58-119">How to Create a Server Group</span></span>](how-to-create-a-server-group.md)

[<span data-ttu-id="41a58-120">Удаление сервера</span><span class="sxs-lookup"><span data-stu-id="41a58-120">How to Remove a Server</span></span>](how-to-remove-a-server.md)

 

 






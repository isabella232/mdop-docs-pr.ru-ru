---
title: Режим изолированной работы
description: Режим изолированной работы
author: dansimp
ms.assetid: 3f9849ea-ba53-4c68-85d3-87a4218f59c6
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 6e9534b93f23b17e5258ef5e2d548eb93213f2f8
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10821622"
---
# <span data-ttu-id="da3a1-103">Режим изолированной работы</span><span class="sxs-lookup"><span data-stu-id="da3a1-103">Disconnected Operation Mode</span></span>


<span data-ttu-id="da3a1-104">Параметры режима разъединенных операций: доступ, щелкнув правой кнопкой мыши узел **Application Virtualization** , выбрав пункт **свойства**и нажав на вкладку **Подключение** , можно использовать клиент или клиент для служб удаленных рабочих столов Application Virtualization (ранее — службы терминалов) для запуска приложений, которые хранятся в кэше файловой системы клиента, когда клиент не может подключиться к серверу управления виртуализации приложений.</span><span class="sxs-lookup"><span data-stu-id="da3a1-104">The disconnected operation mode settings—accessible by right-clicking the **Application Virtualization** node, selecting **Properties**, and clicking the **Connectivity** tab—enables the Application Virtualization Desktop Client or Client for Remote Desktop Services (formerly Terminal Services) to run applications that are stored in the file system cache of the client when the client is unable to connect to the Application Virtualization Management Server.</span></span>

<span data-ttu-id="da3a1-105">Причины сбоя при подключении к серверу: отказ сервера, отключение от сети или соединение с сетью.</span><span class="sxs-lookup"><span data-stu-id="da3a1-105">Reasons for failure to connect to the server include server failure, network outage, or disconnection from the network.</span></span> <span data-ttu-id="da3a1-106">При возникновении сбоя клиент автоматически переключается на отключенную операцию.</span><span class="sxs-lookup"><span data-stu-id="da3a1-106">If any failure occurs, the client will automatically switch to disconnected operation.</span></span> <span data-ttu-id="da3a1-107">Если после отключения клиента требуется добавить дополнительные данные с сервера, чтобы продолжить выполнение приложения, а также в случае истечения времени ожидания отключенной операции, клиент попытается повторно подключиться к серверу.</span><span class="sxs-lookup"><span data-stu-id="da3a1-107">After it is disconnected, if the client needs additional data from the server to continue to run an application or if the disconnected operation time-out expires, the client will attempt to reconnect to the server.</span></span> <span data-ttu-id="da3a1-108">Если при попытке подключения происходит сбой, приложение будет закрыто.</span><span class="sxs-lookup"><span data-stu-id="da3a1-108">If this connection attempt fails, the application will be shut down.</span></span>

<span data-ttu-id="da3a1-109">По умолчанию отключенная операция включена, а время ожидания — 90 дней.</span><span class="sxs-lookup"><span data-stu-id="da3a1-109">By default, disconnected operation is enabled and the time-out is set to 90 days.</span></span> <span data-ttu-id="da3a1-110">Значение времени ожидания задается как количество дней, в которых вы хотите ограничить режим работы в режиме ожидания с подключением, и вы можете ввести значение от 1 до 999.</span><span class="sxs-lookup"><span data-stu-id="da3a1-110">The time-out value is specified as the number of days you want to limit disconnected operation mode, and you can enter a value from 1–999.</span></span>

## <span data-ttu-id="da3a1-111">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="da3a1-111">Related topics</span></span>


[<span data-ttu-id="da3a1-112">Отключение или изменение параметров режима изолированной работы</span><span class="sxs-lookup"><span data-stu-id="da3a1-112">How to Disable or Modify Disconnected Operation Mode Settings</span></span>](how-to-disable-or-modify-disconnected-operation-mode-settings.md)

 

 






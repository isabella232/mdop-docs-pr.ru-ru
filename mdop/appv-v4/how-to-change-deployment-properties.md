---
title: Изменение свойств развертывания
description: Изменение свойств развертывания
author: dansimp
ms.assetid: 0a214a7a-cc83-4d04-89f9-5727153be918
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: dfb42962d41159479db61da9c3beb3771ef35502
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10818062"
---
# <span data-ttu-id="a588d-103">Изменение свойств развертывания</span><span class="sxs-lookup"><span data-stu-id="a588d-103">How to Change Deployment Properties</span></span>


<span data-ttu-id="a588d-104">С помощью описанных ниже процедур вы можете изменить сведения на вкладке **развертывание** для приложения, которое вы используете, включая URL-адрес сервера Application Virtualization, операционные системы, необходимые для виртуализированных приложений, и параметры вывода для установленного виртуального приложения.</span><span class="sxs-lookup"><span data-stu-id="a588d-104">You can use the following procedures to change the **Deployment** tab information for an application you are sequencing, including the Application Virtualization server URL, the operating systems required by the virtualized applications, and the output options for the virtual application to be installed.</span></span>

**<span data-ttu-id="a588d-105">Изменение URL-адреса сервера</span><span class="sxs-lookup"><span data-stu-id="a588d-105">To change the server URL</span></span>**

1.  <span data-ttu-id="a588d-106">В раскрывающемся списке выберите протокол потоковой передачи.</span><span class="sxs-lookup"><span data-stu-id="a588d-106">Select the streaming protocol from the drop-down list box.</span></span>

2.  <span data-ttu-id="a588d-107">Введите имя узла виртуального сервера приложений или подсистемы балансировки нагрузки для серверной группы.</span><span class="sxs-lookup"><span data-stu-id="a588d-107">Enter the host name of the virtual application server or the server group's load balancer.</span></span> <span data-ttu-id="a588d-108">Вы можете использовать фактические имя узла или IP-адрес.</span><span class="sxs-lookup"><span data-stu-id="a588d-108">You can use the actual host name or IP address.</span></span>

3.  <span data-ttu-id="a588d-109">Укажите номер порта, на котором виртуальный сервер приложений или служба балансировки нагрузки будет прослушивать запросы клиента для рабочего стола Application Virtualization для потокового приложения.</span><span class="sxs-lookup"><span data-stu-id="a588d-109">Specify the port number on which the virtual application server or load balancer will listen for an Application Virtualization Desktop Client request for the streamed application.</span></span>

4.  <span data-ttu-id="a588d-110">Укажите относительный путь на виртуальном сервере приложений, где хранится пакет программного обеспечения.</span><span class="sxs-lookup"><span data-stu-id="a588d-110">Specify the relative path on the virtual application server where the software package is stored.</span></span>

**<span data-ttu-id="a588d-111">Изменение требований к операционным системам приложений</span><span class="sxs-lookup"><span data-stu-id="a588d-111">To change the application operating systems requirements</span></span>**

1.  <span data-ttu-id="a588d-112">Чтобы добавить требуемые операционные системы, выберите ее в списке **Доступные** и нажмите кнопку со стрелкой, указывающей на **выбранный** элемент управления списком операционных систем.</span><span class="sxs-lookup"><span data-stu-id="a588d-112">To add the required operating system(s), select it in the **Available** list and click the arrow button pointing to the **Selected** operating systems list control.</span></span>

2.  <span data-ttu-id="a588d-113">Чтобы удалить операционную систему, выберите ее **в списке,** а затем нажмите кнопку со стрелкой, указывающую на список **Доступные** операционные системы.</span><span class="sxs-lookup"><span data-stu-id="a588d-113">To remove an operating system, select it in the **Selected** list control, and click the arrow button pointing to the **Available** operating systems list control.</span></span>

**<span data-ttu-id="a588d-114">Изменение параметров вывода приложения</span><span class="sxs-lookup"><span data-stu-id="a588d-114">To change the application output options</span></span>**

1.  <span data-ttu-id="a588d-115">В раскрывающемся списке **алгоритм сжатия** выберите метод сжатия, который будет использоваться при потоковой передаче приложения.</span><span class="sxs-lookup"><span data-stu-id="a588d-115">From the **Compression Algorithm** drop-down list, select the compression method to use when streaming the application.</span></span>

2.  <span data-ttu-id="a588d-116">Установите флажок **включить дескрипторы безопасности** , чтобы гарантировать, что дескрипторы безопасности упакованных приложений принудительно применяются при развертывании.</span><span class="sxs-lookup"><span data-stu-id="a588d-116">Select the **Enforce Security Descriptors** check box to ensure security descriptors of the packaged applications are enforced when deployed.</span></span>

3.  <span data-ttu-id="a588d-117">Выберите **создать файл различий** , чтобы создать файл различий для приложения из предыдущей последовательной версии.</span><span class="sxs-lookup"><span data-stu-id="a588d-117">Select **Generate Difference File** to generate a difference file for the application from the previous sequenced version.</span></span>

4.  <span data-ttu-id="a588d-118">Выберите команду **создать пакет установщика Microsoft Windows (MSI)** , чтобы создать пакет установщика.</span><span class="sxs-lookup"><span data-stu-id="a588d-118">Select **Generate Microsoft Windows Installer (MSI) Package** to create an installer package.</span></span>

## <span data-ttu-id="a588d-119">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="a588d-119">Related topics</span></span>


[<span data-ttu-id="a588d-120">Вкладка "Сведения о развертывании"</span><span class="sxs-lookup"><span data-stu-id="a588d-120">About the Deployment Tab</span></span>](about-the-deployment-tab.md)

[<span data-ttu-id="a588d-121">Консоль Sequencer</span><span class="sxs-lookup"><span data-stu-id="a588d-121">Sequencer Console</span></span>](sequencer-console.md)

 

 






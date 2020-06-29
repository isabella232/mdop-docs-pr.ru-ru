---
title: Развертывание UE-V 1.0
description: Развертывание UE-V 1.0
author: dansimp
ms.assetid: 519598bb-8c81-4af7-bee7-357696bff880
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 1a1c515f9be950d8ca7b0a199344d34f7852073d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10827149"
---
# <span data-ttu-id="f234a-103">Развертывание UE-V 1.0</span><span class="sxs-lookup"><span data-stu-id="f234a-103">Deploying UE-V 1.0</span></span>


<span data-ttu-id="f234a-104">Существует ряд различных конфигураций развертывания, поддерживаемых Microsoft User Experience Virtualization (UE-V).</span><span class="sxs-lookup"><span data-stu-id="f234a-104">There are a number of different deployment configurations that Microsoft User Experience Virtualization (UE-V) supports.</span></span> <span data-ttu-id="f234a-105">В этом разделе содержатся общие сведения и пошаговые инструкции, которые помогут вам успешно выполнить задачи, которые необходимо выполнить на разных этапах развертывания.</span><span class="sxs-lookup"><span data-stu-id="f234a-105">This section includes general information and step-by-step procedures to help you successfully perform the tasks that you must complete at different stages of your deployment.</span></span>

## <span data-ttu-id="f234a-106">Сведения о развертывании UE-V</span><span class="sxs-lookup"><span data-stu-id="f234a-106">Deployment information for UE-V</span></span>


<span data-ttu-id="f234a-107">Для развертывания UE-V требуется место хранения параметров на общем сетевом ресурсе и агент UE-V, установленный на каждом компьютере, который синхронизирует параметры.</span><span class="sxs-lookup"><span data-stu-id="f234a-107">A UE-V deployment requires a settings storage location on a network share and a UE-V agent installed on every computer that synchronizes settings.</span></span> <span data-ttu-id="f234a-108">Для управления параметрами UE-V можно использовать шаблоны групповой политики UE-V.</span><span class="sxs-lookup"><span data-stu-id="f234a-108">The UE-V Group Policy templates can be used to manage UE-V settings.</span></span> <span data-ttu-id="f234a-109">В следующих разделах описано, как развертывать эти функции.</span><span class="sxs-lookup"><span data-stu-id="f234a-109">The following topics describe how to deploy these features.</span></span>

[<span data-ttu-id="f234a-110">Развертывание места хранения параметров для UE-V 1.0</span><span class="sxs-lookup"><span data-stu-id="f234a-110">Deploying the Settings Storage Location for UE-V 1.0</span></span>](deploying-the-settings-storage-location-for-ue-v-10.md)

<span data-ttu-id="f234a-111">Для всех развертываний UE-V требуется место хранения параметров, где находятся пакеты параметров, содержащие значения параметров синхронизации.</span><span class="sxs-lookup"><span data-stu-id="f234a-111">All UE-V deployments require a settings storage location where the settings packages that contain the synchronized setting values are located.</span></span>

[<span data-ttu-id="f234a-112">Развертывание агента UE-V</span><span class="sxs-lookup"><span data-stu-id="f234a-112">Deploying the UE-V Agent</span></span>](deploying-the-ue-v-agent.md)

<span data-ttu-id="f234a-113">Для синхронизации параметров с помощью UE-V на компьютере должны быть установлены и запущены агенты UE-V.</span><span class="sxs-lookup"><span data-stu-id="f234a-113">To synchronize settings by using UE-V, a computer must have the UE-V Agent installed and running.</span></span>

[<span data-ttu-id="f234a-114">Установка шаблонов ADMX групповой политики UE-V</span><span class="sxs-lookup"><span data-stu-id="f234a-114">Installing the UE-V Group Policy ADMX Templates</span></span>](installing-the-ue-v-group-policy-admx-templates.md)

<span data-ttu-id="f234a-115">Вы можете использовать групповую политику для предварительной настройки UE-V Settings, прежде чем развертывать агент UE-V и стандартную конфигурацию UE-V.</span><span class="sxs-lookup"><span data-stu-id="f234a-115">You can use Group Policy to preconfigure UE-V settings before you deploy the UE-V Agent as well as standard UE-V configuration.</span></span>

## <span data-ttu-id="f234a-116">Сведения о развертывании настраиваемого шаблона</span><span class="sxs-lookup"><span data-stu-id="f234a-116">Deployment information for custom template deployment</span></span>


<span data-ttu-id="f234a-117">Если вы планируете создавать пользовательские шаблоны расположений для приложений, отличных от приложений Microsoft, которые включены в UE-V (например, бизнес-приложения), вы можете развернуть каталог шаблонов параметров, а для создания этих шаблонов нужно установить генератор UE-V.</span><span class="sxs-lookup"><span data-stu-id="f234a-117">If you plan to create custom settings location templates for applications other than the Microsoft applications that are included in UE-V, such as line-of-business applications, then you can deploy a settings template catalog and you must install the UE-V Generator to create those templates.</span></span> <span data-ttu-id="f234a-118">Дополнительные сведения можно найти в разделе [Планирование развертывания настраиваемого шаблона для UE-V 1,0](planning-for-custom-template-deployment-for-ue-v-10.md).</span><span class="sxs-lookup"><span data-stu-id="f234a-118">For more information, see [Planning for Custom Template Deployment for UE-V 1.0](planning-for-custom-template-deployment-for-ue-v-10.md).</span></span>

[<span data-ttu-id="f234a-119">Установка генератора UE-V</span><span class="sxs-lookup"><span data-stu-id="f234a-119">Installing the UE-V Generator</span></span>](installing-the-ue-v-generator.md)

<span data-ttu-id="f234a-120">Используйте генератор UE-V для создания, изменения и проверки шаблонов расположений настраиваемых параметров, которые помогают синхронизировать параметры приложений, отличных от приложений по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="f234a-120">Use the UE-V Generator to create, edit, and validate custom settings location templates that help synchronize settings of applications other than the default applications.</span></span>

[<span data-ttu-id="f234a-121">Развертывание каталога шаблонов параметров для UE-V 1.0</span><span class="sxs-lookup"><span data-stu-id="f234a-121">Deploying the Settings Template Catalog for UE-V 1.0</span></span>](deploying-the-settings-template-catalog-for-ue-v-10.md)

<span data-ttu-id="f234a-122">Если вам нужно развернуть шаблоны расположений настраиваемых параметров для поддержки приложений, отличных от приложений по умолчанию, в агенте UE-V, необходимо настроить каталог шаблонов параметров, чтобы сохранить их.</span><span class="sxs-lookup"><span data-stu-id="f234a-122">If you need to deploy custom settings location templates to support applications other than the default applications in the UE-V Agent, you must configure a settings template catalog to store them.</span></span>

[<span data-ttu-id="f234a-123">Развертывание шаблонов расположения параметров UE-V для UE-V 1.0</span><span class="sxs-lookup"><span data-stu-id="f234a-123">Deploying UE-V Settings Location Templates for UE-V 1.0</span></span>](deploying-ue-v-settings-location-templates-for-ue-v-10.md)

<span data-ttu-id="f234a-124">Если необходимо синхронизировать приложения, отличные от приложений по умолчанию, в агенте UE-V, пользовательские шаблоны расположений, созданные с помощью генератора UE-V, могут быть распределены в каталог шаблонов параметров UE-v.</span><span class="sxs-lookup"><span data-stu-id="f234a-124">If you need to synchronize applications other than the default applications in the UE-V Agent, the custom setting location templates that are created with UE-V Generator can be distributed to the UE-V settings template catalog.</span></span>

<span data-ttu-id="f234a-125">**Примечание**  Для развертывания настраиваемых шаблонов требуется каталог шаблонов параметров.</span><span class="sxs-lookup"><span data-stu-id="f234a-125">**Note** Deploying custom templates requires a settings template catalog.</span></span> <span data-ttu-id="f234a-126">Шаблоны приложений Microsoft по умолчанию развертываются с помощью агента UE-V Agent.</span><span class="sxs-lookup"><span data-stu-id="f234a-126">The default Microsoft application templates are deployed with the UE-V Agent.</span></span>

 

## <span data-ttu-id="f234a-127">Темы для этого продукта</span><span class="sxs-lookup"><span data-stu-id="f234a-127">Topics for this product</span></span>


[<span data-ttu-id="f234a-128">Microsoft User Experience Virtualization (UE-V) 1.0</span><span class="sxs-lookup"><span data-stu-id="f234a-128">Microsoft User Experience Virtualization (UE-V) 1.0</span></span>](index.md)

[<span data-ttu-id="f234a-129">Начало работы с User Experience Virtualization 1.0</span><span class="sxs-lookup"><span data-stu-id="f234a-129">Getting Started With User Experience Virtualization 1.0</span></span>](getting-started-with-user-experience-virtualization-10.md)

[<span data-ttu-id="f234a-130">Планирование UE-V 1.0</span><span class="sxs-lookup"><span data-stu-id="f234a-130">Planning for UE-V 1.0</span></span>](planning-for-ue-v-10.md)

[<span data-ttu-id="f234a-131">Операции в UE-V 1.0</span><span class="sxs-lookup"><span data-stu-id="f234a-131">Operations for UE-V 1.0</span></span>](operations-for-ue-v-10.md)

[<span data-ttu-id="f234a-132">Устранение неполадок UE-V 1.0</span><span class="sxs-lookup"><span data-stu-id="f234a-132">Troubleshooting UE-V 1.0</span></span>](troubleshooting-ue-v-10.md)

 

 






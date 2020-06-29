---
title: Планирование конфигурации UE-V
description: Планирование конфигурации UE-V
author: dansimp
ms.assetid: db78dad4-78e0-45d6-a235-8b7345cb79f8
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: ce21afc7b7e8ee183b4fb86de7dea6eeaa58953e
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10826822"
---
# <span data-ttu-id="ec7b3-103">Планирование конфигурации UE-V</span><span class="sxs-lookup"><span data-stu-id="ec7b3-103">Planning for UE-V Configuration</span></span>


<span data-ttu-id="ec7b3-104">Вы можете настроить Microsoft User Experience Virtualization (UE-V) в соответствии с конкретными потребностями предприятия, определив, какие приложения развертываются и какие конфигурации определяют поведение UE-V.</span><span class="sxs-lookup"><span data-stu-id="ec7b3-104">You can configure Microsoft User Experience Virtualization (UE-V) to meet the specific needs of your enterprise by defining which applications are deployed and which configurations define the UE-V behavior.</span></span>

## <span data-ttu-id="ec7b3-105">Планирование приложений для синхронизации с UE-V</span><span class="sxs-lookup"><span data-stu-id="ec7b3-105">Plan which applications to synchronize with UE-V</span></span>


<span data-ttu-id="ec7b3-106">UE-V включает набор готовых шаблонов расположений параметров.</span><span class="sxs-lookup"><span data-stu-id="ec7b3-106">UE-V includes a set of predefined settings location templates.</span></span> <span data-ttu-id="ec7b3-107">UE-V также позволяет администраторам создавать пользовательские шаблоны расположений параметров для других приложений, в том числе из бизнес-приложений сторонних разработчиков, которые используются в корпоративной среде.</span><span class="sxs-lookup"><span data-stu-id="ec7b3-107">UE-V also allows administrators to create custom settings location templates for other applications, including third-party or line-of-business applications that are used in the enterprise.</span></span> <span data-ttu-id="ec7b3-108">Этот раздел содержит список приложений, включенных в клиент UE-V, и инструкции по включению шаблонов расположений о настраиваемых параметрах.</span><span class="sxs-lookup"><span data-stu-id="ec7b3-108">This topic includes a list of applications that are included with the UE-V client and guidance on how to include custom settings location templates.</span></span>

[<span data-ttu-id="ec7b3-109">Планирование того, какие приложения необходимо синхронизировать с UE-V 1.0</span><span class="sxs-lookup"><span data-stu-id="ec7b3-109">Planning Which Applications to Synchronize with UE-V 1.0</span></span>](planning-which-applications-to-synchronize-with-ue-v-10.md)

## <span data-ttu-id="ec7b3-110">Контрольный список для оценки бизнес-приложений для UE-V</span><span class="sxs-lookup"><span data-stu-id="ec7b3-110">Checklist for Evaluating Line-of-Business Applications for UE-V</span></span>


<span data-ttu-id="ec7b3-111">Руководство о том, следует ли синхронизировать бизнес-приложение.</span><span class="sxs-lookup"><span data-stu-id="ec7b3-111">Guidance on whether a line-of-business application should be synchronized.</span></span>

[<span data-ttu-id="ec7b3-112">Контрольный список для оценки бизнес-приложений для UE-V 1.0</span><span class="sxs-lookup"><span data-stu-id="ec7b3-112">Checklist for Evaluating Line-of-Business Applications for UE-V 1.0</span></span>](checklist-for-evaluating-line-of-business-applications-for-ue-v-10.md)

## <span data-ttu-id="ec7b3-113">Планирование развертывания настраиваемого шаблона</span><span class="sxs-lookup"><span data-stu-id="ec7b3-113">Plan custom template deployment</span></span>


<span data-ttu-id="ec7b3-114">Для поддержки других приложений, в том числе сторонних приложений, необходимо создать шаблоны расположений с пользовательскими параметрами с помощью генератора UE-V и развернуть их в каталоге шаблонов параметров.</span><span class="sxs-lookup"><span data-stu-id="ec7b3-114">In order to support other applications, including third-party applications, you must create custom settings location templates by using the UE-V Generator, and deploy them to a settings template catalog.</span></span>

[<span data-ttu-id="ec7b3-115">Планирование развертывания пользовательского шаблона для UE-V 1.0</span><span class="sxs-lookup"><span data-stu-id="ec7b3-115">Planning for Custom Template Deployment for UE-V 1.0</span></span>](planning-for-custom-template-deployment-for-ue-v-10.md)

## <span data-ttu-id="ec7b3-116">Планирование конфигурации UE-V</span><span class="sxs-lookup"><span data-stu-id="ec7b3-116">Plan for UE-V configuration</span></span>


<span data-ttu-id="ec7b3-117">Конфигурации UE-V определяют, как параметры синхронизируются в рамках всего предприятия.</span><span class="sxs-lookup"><span data-stu-id="ec7b3-117">UE-V configurations determine how settings are synchronized throughout the enterprise.</span></span> <span data-ttu-id="ec7b3-118">Эти конфигурации можно выполнить до, во время или после развертывания агента UE-V.</span><span class="sxs-lookup"><span data-stu-id="ec7b3-118">These configurations can be made before, during, or after the UE-V Agent is deployed.</span></span> <span data-ttu-id="ec7b3-119">UE-V предлагает разнообразные методы настройки.</span><span class="sxs-lookup"><span data-stu-id="ec7b3-119">UE-V provides a variety of configuration methods</span></span>

[<span data-ttu-id="ec7b3-120">Планирование методов конфигурации UE-V</span><span class="sxs-lookup"><span data-stu-id="ec7b3-120">Planning for UE-V Configuration Methods</span></span>](planning-for-ue-v-configuration-methods.md)

## <span data-ttu-id="ec7b3-121">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="ec7b3-121">Related topics</span></span>


[<span data-ttu-id="ec7b3-122">Планирование UE-V 1.0</span><span class="sxs-lookup"><span data-stu-id="ec7b3-122">Planning for UE-V 1.0</span></span>](planning-for-ue-v-10.md)

 

 






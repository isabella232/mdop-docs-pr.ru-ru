---
title: Развертывание шаблонов расположения параметров UE-V для UE-V 1.0
description: Развертывание шаблонов расположения параметров UE-V для UE-V 1.0
author: dansimp
ms.assetid: 7e0cc553-14f7-40fa-828a-281c8d2d1934
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: b276fb9d6c0b3749f9818483869dfe98bbc147c7
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10827122"
---
# <span data-ttu-id="d0ae9-103">Развертывание шаблонов расположения параметров UE-V для UE-V 1.0</span><span class="sxs-lookup"><span data-stu-id="d0ae9-103">Deploying UE-V Settings Location Templates for UE-V 1.0</span></span>


<span data-ttu-id="d0ae9-104">Виртуализация взаимодействия с пользователем Microsoft (UE-V) использует шаблоны расположений параметров (XML-файлы), которые определяют параметры, зафиксированные и применяемые с помощью виртуализации взаимодействия с пользователем.</span><span class="sxs-lookup"><span data-stu-id="d0ae9-104">Microsoft User Experience Virtualization (UE-V) uses settings location templates (XML files) that define the settings that are captured and applied by User Experience Virtualization.</span></span> <span data-ttu-id="d0ae9-105">UE-V включает набор стандартных шаблонов, а также средство, генератор UE-V, который позволяет создавать пользовательские шаблоны расположений параметров.</span><span class="sxs-lookup"><span data-stu-id="d0ae9-105">UE-V includes a set of standard templates, as well as a tool, the UE-V Generator, which allows you to create custom settings location templates.</span></span> <span data-ttu-id="d0ae9-106">После того как вы создадите шаблон расположения параметров, необходимо проверить его, чтобы убедиться в том, что параметры приложения правильно перемещены в тестовую среду.</span><span class="sxs-lookup"><span data-stu-id="d0ae9-106">After you create a settings location template, you should test it to ensure that the application settings roam correctly in a test environment.</span></span> <span data-ttu-id="d0ae9-107">Затем вы можете безопасно развернуть шаблон расположения параметров на компьютерах в предприятии.</span><span class="sxs-lookup"><span data-stu-id="d0ae9-107">You can then safely deploy the settings location template to computers in the enterprise.</span></span>

<span data-ttu-id="d0ae9-108">Шаблоны расположений параметров можно развертывать с помощью корпоративного распространения программного обеспечения (ESD), настроек групповой политики, а также путем настройки каталога шаблонов параметров UE-V.</span><span class="sxs-lookup"><span data-stu-id="d0ae9-108">Settings location templates can be deployed by using enterprise software distribution (ESD), Group Policy preferences, or by configuring a UE-V settings template catalog.</span></span> <span data-ttu-id="d0ae9-109">Шаблоны, развернутые с помощью ESD или групповой политики, должны быть зарегистрированы с помощью UE-V WMI или PowerShell.</span><span class="sxs-lookup"><span data-stu-id="d0ae9-109">Templates that are deployed by using an ESD or Group Policy must be registered through UE-V WMI or PowerShell.</span></span> <span data-ttu-id="d0ae9-110">Шаблоны, которые хранятся в расположении каталога шаблонов параметров, автоматически регистрируются агентом UE-V.</span><span class="sxs-lookup"><span data-stu-id="d0ae9-110">Templates that are stored in the settings template catalog location are automatically registered by the UE-V agent.</span></span>

## <span data-ttu-id="d0ae9-111">Развертывание шаблонов расположений параметров с помощью пути к каталогу шаблонов параметров</span><span class="sxs-lookup"><span data-stu-id="d0ae9-111">Deploy the settings location templates with a settings template catalog path</span></span>


<span data-ttu-id="d0ae9-112">Путь к каталогу шаблонов расположений параметров UE-V можно определить с помощью следующих методов: групповая политика, параметры командной строки для установки агента, WMI или PowerShell.</span><span class="sxs-lookup"><span data-stu-id="d0ae9-112">The UE-V settings location template catalog path can be defined by using the following methods: Group Policy, the agent install command-line parameters, WMI, or PowerShell.</span></span> <span data-ttu-id="d0ae9-113">После того как вы определили путь к каталогу шаблонов, агент UE-V Agent извлекает из этого расположения новые или обновленные шаблоны.</span><span class="sxs-lookup"><span data-stu-id="d0ae9-113">After the template catalog path has been defined, the UE-V agent retrieves the new or updated templates from this location.</span></span> <span data-ttu-id="d0ae9-114">Агент UE-V проверяет это расположение один раз в день и обновляет режим синхронизации на основе шаблонов, найденных в этой папке.</span><span class="sxs-lookup"><span data-stu-id="d0ae9-114">The UE-V agent checks this location once each day and updates its synchronization behavior based on the templates found in this folder.</span></span> <span data-ttu-id="d0ae9-115">Шаблоны, добавленные или обновленные в этой папке с момента последней проверки регистрируются агентом UE-V.</span><span class="sxs-lookup"><span data-stu-id="d0ae9-115">Templates that have been added or updated in this folder since the last check are registered by the UE-V agent.</span></span> <span data-ttu-id="d0ae9-116">Агент UE-V также отменяет регистрацию шаблонов, которые были удалены из этой папки.</span><span class="sxs-lookup"><span data-stu-id="d0ae9-116">The UE-V agent also unregisters templates that have been removed from this folder.</span></span> <span data-ttu-id="d0ae9-117">Шаблоны регистрируются и отменяются из регистрации один раз в день с помощью планировщика заданий.</span><span class="sxs-lookup"><span data-stu-id="d0ae9-117">Templates are registered and unregistered one time per day by the task scheduler.</span></span>

**<span data-ttu-id="d0ae9-118">Использование пути к каталогу шаблонов параметров для развертывания шаблонов расположений параметров UE-V</span><span class="sxs-lookup"><span data-stu-id="d0ae9-118">To use settings template catalog path to deploy UE-V settings location templates</span></span>**

1.  <span data-ttu-id="d0ae9-119">Перейдите к папке "сетевая папка", которая определена как каталог шаблонов параметров.</span><span class="sxs-lookup"><span data-stu-id="d0ae9-119">Navigate to the network share folder that is defined as the settings template catalog.</span></span>

2.  <span data-ttu-id="d0ae9-120">Добавьте, удалите или обновите шаблоны расположений параметров в каталоге шаблонов параметров в соответствии с требуемой конфигурацией шаблона агента UE-V для компьютеров UE-V.</span><span class="sxs-lookup"><span data-stu-id="d0ae9-120">Add, remove, or update settings location templates in the settings template catalog to reflect the desired UE-V agent template configuration for UE-V computers.</span></span>

3.  <span data-ttu-id="d0ae9-121">Шаблоны на компьютерах обновляются ежедневно в соответствии с изменениями, внесенными в каталог шаблонов параметров.</span><span class="sxs-lookup"><span data-stu-id="d0ae9-121">Templates on computers are updated daily based on changes to the settings template catalog.</span></span>

4.  <span data-ttu-id="d0ae9-122">Откройте командную команду с повышенными привилегиями и перейдите в раздел \*\*% Program Files%\\Microsoft виртуализация взаимодействия с пользователем \ \ &lt; x86 или x64 &gt; \*\*, а затем запустите **ApplySettingsTemplateCatalog.exe** , чтобы вручную обновить шаблоны на компьютере, на котором запущен агент UE-V Agent.</span><span class="sxs-lookup"><span data-stu-id="d0ae9-122">Open an elevated command prompt and navigate to **%program files%\\Microsoft user Experience Virtualization \\ Agent \\ &lt;x86 or x64 &gt;**, and then run **ApplySettingsTemplateCatalog.exe** to manually update templates on a computer that runs the UE-V agent.</span></span>

## <span data-ttu-id="d0ae9-123">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="d0ae9-123">Related topics</span></span>


[<span data-ttu-id="d0ae9-124">Microsoft User Experience Virtualization (UE-V) 1.0</span><span class="sxs-lookup"><span data-stu-id="d0ae9-124">Microsoft User Experience Virtualization (UE-V) 1.0</span></span>](index.md)

[<span data-ttu-id="d0ae9-125">Развертывание UE-V 1.0</span><span class="sxs-lookup"><span data-stu-id="d0ae9-125">Deploying UE-V 1.0</span></span>](deploying-ue-v-10.md)

[<span data-ttu-id="d0ae9-126">Планирование того, какие приложения необходимо синхронизировать с UE-V 1.0</span><span class="sxs-lookup"><span data-stu-id="d0ae9-126">Planning Which Applications to Synchronize with UE-V 1.0</span></span>](planning-which-applications-to-synchronize-with-ue-v-10.md)

 

 






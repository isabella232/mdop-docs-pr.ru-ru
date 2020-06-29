---
title: Развертывание DaRT 8.0 на компьютерах администраторов
description: Развертывание DaRT 8.0 на компьютерах администраторов
author: dansimp
ms.assetid: f918ead8-742e-464a-8bf6-1fcedde66cae
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 0ab001f612f2257ecbd77c39319cc99c17d36197
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10824122"
---
# <span data-ttu-id="0e07c-103">Развертывание DaRT 8.0 на компьютерах администраторов</span><span class="sxs-lookup"><span data-stu-id="0e07c-103">Deploying DaRT 8.0 to Administrator Computers</span></span>


<span data-ttu-id="0e07c-104">Прежде чем приступить к развертыванию набора средств диагностики и восстановления Microsoft (DaRT) 8,0, ознакомьтесь с требованиями для вашей среды.</span><span class="sxs-lookup"><span data-stu-id="0e07c-104">Before you begin the deployment of Microsoft Diagnostics and Recovery Toolset (DaRT) 8.0, review the requirements for your environment.</span></span> <span data-ttu-id="0e07c-105">Сюда входят требования к оборудованию для установки DaRT 8,0.</span><span class="sxs-lookup"><span data-stu-id="0e07c-105">This includes the hardware requirements for installing DaRT 8.0.</span></span> <span data-ttu-id="0e07c-106">Дополнительные сведения о требованиях к оборудованию и программному обеспечению DaRT можно найти в разделе [DaRT 8,0 поддерживаемые конфигурации](dart-80-supported-configurations-dart-8.md).</span><span class="sxs-lookup"><span data-stu-id="0e07c-106">For more information about DaRT hardware and software requirements, see [DaRT 8.0 Supported Configurations](dart-80-supported-configurations-dart-8.md).</span></span>

<span data-ttu-id="0e07c-107">Темы в этом разделе можно использовать для развертывания DaRT в корпоративной среде на основе вашей среды и стратегии развертывания.</span><span class="sxs-lookup"><span data-stu-id="0e07c-107">The topics in this section can be used to help you deploy DaRT in your enterprise based on your environment and deployment strategy.</span></span>

## <span data-ttu-id="0e07c-108">Развертывание DaRT 8,0</span><span class="sxs-lookup"><span data-stu-id="0e07c-108">Deploy DaRT 8.0</span></span>


<span data-ttu-id="0e07c-109">С помощью файла установщика Windows для DaRT можно установить DaRT на компьютере, который будет использоваться для первоначального создания образа для восстановления DaRT, а затем устранить неполадки и исправить компьютеры конечных пользователей.</span><span class="sxs-lookup"><span data-stu-id="0e07c-109">You can use the Windows Installer file for DaRT to install DaRT on a computer that you will use to first create the DaRT recovery image and then troubleshoot and fix end-user computers.</span></span> <span data-ttu-id="0e07c-110">Как правило, в рамках Организации вы можете установить на компьютер администратора только функцию DaRT, для которой необходимо создать изображение для восстановления DaRT.</span><span class="sxs-lookup"><span data-stu-id="0e07c-110">Frequently, across an organization, you might install on the administrator computer only the DaRT functionality that you need to create a DaRT recovery image.</span></span> <span data-ttu-id="0e07c-111">Затем на компьютере администратора службы поддержки вы можете установить только функцию DaRT, которая вам понадобится для устранения неполадок с компьютером, например средством просмотра удаленных подключений и анализатором аварийного восстановления DaRT.</span><span class="sxs-lookup"><span data-stu-id="0e07c-111">Then, on a help desk administrator’s computer, you might install only the DaRT functionality that you must have to troubleshoot a problem computer, such as the DaRT Remote Connection Viewer and the Crash Analyzer.</span></span>

<span data-ttu-id="0e07c-112">Кроме ручного запуска установочного файла Windows для установки DaRT, вы также можете установить DaRT в командной строке, чтобы поддерживать корпоративную систему развертывания программного обеспечения, например SystemCenterConfigurationManager2012.</span><span class="sxs-lookup"><span data-stu-id="0e07c-112">In addition to manually running the Windows Installer file to install DaRT, you can also install DaRT at the command prompt to support enterprise software deployment systems such as SystemCenterConfigurationManager2012.</span></span>

[<span data-ttu-id="0e07c-113">Развертывание DaRT 8.0</span><span class="sxs-lookup"><span data-stu-id="0e07c-113">How to Deploy DaRT 8.0</span></span>](how-to-deploy-dart-80-dart-8.md)

## <span data-ttu-id="0e07c-114">Изменение, восстановление и удаление DaRT 8,0</span><span class="sxs-lookup"><span data-stu-id="0e07c-114">Change, repair, or remove DaRT 8.0</span></span>


<span data-ttu-id="0e07c-115">Вы можете изменить, восстановить или удалить установку DaRT, дважды щелкнув установочный файл DaRT и нажав кнопку, соответствующую действию, которое вы хотите выполнить или на панели управления Windows.</span><span class="sxs-lookup"><span data-stu-id="0e07c-115">You can change, repair, or remove the DaRT installation by double-clicking the DaRT installation file and then clicking the button that corresponds to the action that you want to perform or through the Windows Control Panel.</span></span>

[<span data-ttu-id="0e07c-116">Изменение, восстановление или удаление DaRT 8.0</span><span class="sxs-lookup"><span data-stu-id="0e07c-116">How to Change, Repair, or Remove DaRT 8.0</span></span>](how-to-change-repair-or-remove-dart-80-dart-8.md)

## <span data-ttu-id="0e07c-117">Как получить DaRT 8,0</span><span class="sxs-lookup"><span data-stu-id="0e07c-117">How to get DaRT 8.0</span></span>


<span data-ttu-id="0e07c-118">Для получения программного обеспечения DaRT ознакомьтесь [со статьей получение MDOP](https://go.microsoft.com/fwlink/?LinkId=322049).</span><span class="sxs-lookup"><span data-stu-id="0e07c-118">To get the DaRT software, see [How to Get MDOP](https://go.microsoft.com/fwlink/?LinkId=322049).</span></span>

## <span data-ttu-id="0e07c-119">Другие ресурсы по развертыванию DaRT 8,0 на компьютерах администраторов</span><span class="sxs-lookup"><span data-stu-id="0e07c-119">Other resources for deploying the DaRT 8.0 to administrator computers</span></span>


[<span data-ttu-id="0e07c-120">Развертывание DaRT 8.0</span><span class="sxs-lookup"><span data-stu-id="0e07c-120">Deploying DaRT 8.0</span></span>](deploying-dart-80-dart-8.md)

 

 






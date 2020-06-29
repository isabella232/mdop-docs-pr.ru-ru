---
title: Развертывание DaRT 7.0 на компьютерах администраторов
description: Развертывание DaRT 7.0 на компьютерах администраторов
author: dansimp
ms.assetid: 8baf26aa-b168-463c-810f-a165918b9d9f
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 96eda08e28b915e30d88aa57cb19562958848cf4
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10812688"
---
# <span data-ttu-id="7c0e5-103">Развертывание DaRT 7.0 на компьютерах администраторов</span><span class="sxs-lookup"><span data-stu-id="7c0e5-103">Deploying DaRT 7.0 to Administrator Computers</span></span>


<span data-ttu-id="7c0e5-104">Прежде чем приступить к развертыванию набора средств диагностики и восстановления Microsoft (DaRT) 7, ознакомьтесь с требованиями для вашей среды.</span><span class="sxs-lookup"><span data-stu-id="7c0e5-104">Before you begin the deployment of Microsoft Diagnostics and Recovery Toolset (DaRT)7, review the requirements for your environment.</span></span> <span data-ttu-id="7c0e5-105">Сюда входят требования к оборудованию для установки DaRT.</span><span class="sxs-lookup"><span data-stu-id="7c0e5-105">This includes the hardware requirements for installing DaRT.</span></span> <span data-ttu-id="7c0e5-106">Дополнительные сведения о требованиях к оборудованию и программному обеспечению DaRT можно найти в разделе [DaRT 7,0 поддерживаемые конфигурации](dart-70-supported-configurations-dart-7.md).</span><span class="sxs-lookup"><span data-stu-id="7c0e5-106">For more information about DaRT hardware and software requirements, see [DaRT 7.0 Supported Configurations](dart-70-supported-configurations-dart-7.md).</span></span>

<span data-ttu-id="7c0e5-107">Темы в этом разделе можно использовать для развертывания DaRT в корпоративной среде на основе вашей среды и стратегии развертывания.</span><span class="sxs-lookup"><span data-stu-id="7c0e5-107">The topics in this section can be used to help you deploy DaRT in your enterprise based on your environment and deployment strategy.</span></span>

## <span data-ttu-id="7c0e5-108">Развертывание DaRT 7,0 на компьютерах администраторов</span><span class="sxs-lookup"><span data-stu-id="7c0e5-108">Deploy DaRT 7.0 to administrator computers</span></span>


<span data-ttu-id="7c0e5-109">С помощью файла установщика Windows для DaRT можно установить DaRT на компьютере, который будет использоваться для первоначального создания образа для восстановления DaRT, а затем устранить неполадки и исправить компьютеры конечных пользователей.</span><span class="sxs-lookup"><span data-stu-id="7c0e5-109">You can use the Windows Installer file for DaRT to install DaRT on a computer that you will use to first create the DaRT recovery image and then troubleshoot and fix end-user computers.</span></span> <span data-ttu-id="7c0e5-110">Как правило, в рамках Организации вы можете установить на компьютер администратора только функцию DaRT, для которой необходимо создать изображение для восстановления DaRT.</span><span class="sxs-lookup"><span data-stu-id="7c0e5-110">Frequently, across an organization, you might install on the administrator computer only the DaRT functionality that you need to create a DaRT recovery image.</span></span> <span data-ttu-id="7c0e5-111">Затем на компьютере администратора службы поддержки вы можете установить только функцию DaRT, которая необходима для устранения неполадок с компьютером, например средством просмотра удаленных подключений DaRT и анализатором сбоев.</span><span class="sxs-lookup"><span data-stu-id="7c0e5-111">Then, on a helpdesk administrator’s computer, you might install only the DaRT functionality that you must have to troubleshoot a problem computer, such as the DaRT Remote Connection Viewer and the Crash Analyzer.</span></span>

<span data-ttu-id="7c0e5-112">Кроме ручного запуска установочного файла Windows для установки DaRT, вы также можете установить DaRT в командной строке, чтобы поддерживать корпоративную систему развертывания программного обеспечения, например SystemCenterConfigurationManager2012.</span><span class="sxs-lookup"><span data-stu-id="7c0e5-112">In addition to manually running the Windows Installer file to install DaRT, you can also install DaRT at the command prompt to support enterprise software deployment systems such as SystemCenterConfigurationManager2012.</span></span>

[<span data-ttu-id="7c0e5-113">Развертывание DaRT 7.0</span><span class="sxs-lookup"><span data-stu-id="7c0e5-113">How to Deploy DaRT 7.0</span></span>](how-to-deploy-dart-70.md)

## <span data-ttu-id="7c0e5-114">Изменение, восстановление и удаление DaRT 7,0</span><span class="sxs-lookup"><span data-stu-id="7c0e5-114">Change, repair, or remove DaRT 7.0</span></span>


<span data-ttu-id="7c0e5-115">Вы можете изменить, восстановить или удалить установку DaRT, дважды щелкнув установочный файл DaRT и нажав кнопку, соответствующую действию, которое вы хотите выполнить или на панели управления Windows.</span><span class="sxs-lookup"><span data-stu-id="7c0e5-115">You can change, repair, or remove the DaRT installation by double-clicking the DaRT installation file and then clicking the button that corresponds to the action that you want to perform or through the Windows Control Panel.</span></span>

[<span data-ttu-id="7c0e5-116">Изменение, восстановление или удаление DaRT 7.0</span><span class="sxs-lookup"><span data-stu-id="7c0e5-116">How to Change, Repair, or Remove DaRT 7.0</span></span>](how-to-change-repair-or-remove-dart-70.md)

## <span data-ttu-id="7c0e5-117">Другие ресурсы по развертыванию DaRT 7,0 на компьютерах администраторов</span><span class="sxs-lookup"><span data-stu-id="7c0e5-117">Other resources for Deploying the DaRT 7.0 to Administrator Computers</span></span>


-   [<span data-ttu-id="7c0e5-118">Развертывание DaRT 7.0</span><span class="sxs-lookup"><span data-stu-id="7c0e5-118">Deploying DaRT 7.0</span></span>](deploying-dart-70-new-ia.md)

 

 






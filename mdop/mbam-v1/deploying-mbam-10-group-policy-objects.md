---
title: Развертывание объектов групповой политики MBAM 1.0
description: Развертывание объектов групповой политики MBAM 1.0
author: dansimp
ms.assetid: 2129291e-d2b2-41ed-b643-1e311c49fee7
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 8d14123f1d5b197146e425cba063e8ce4c180641
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10821219"
---
# <span data-ttu-id="76f30-103">Развертывание объектов групповой политики MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="76f30-103">Deploying MBAM 1.0 Group Policy Objects</span></span>


<span data-ttu-id="76f30-104">Чтобы успешно развернуть администрирование и мониторинг Microsoft BitLocker (MBAM), необходимо сначала определить групповые политики, которые будут использоваться в реализации MBAM.</span><span class="sxs-lookup"><span data-stu-id="76f30-104">To successfully deploy Microsoft BitLocker Administration and Monitoring (MBAM), you must first determine the Group Policies that you will use in your implementation of MBAM.</span></span> <span data-ttu-id="76f30-105">Более подробную информацию о различных доступных политиках можно найти в разделе [планирование для MBAM 1,0, предъявляемых групповой политикой](planning-for-mbam-10-group-policy-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="76f30-105">For more information about the various available policies, see [Planning for MBAM 1.0 Group Policy Requirements](planning-for-mbam-10-group-policy-requirements.md).</span></span> <span data-ttu-id="76f30-106">После определения политик, которые вы собираетесь использовать, необходимо использовать шаблон групповой политики MBAM 1,0 для создания и развертывания одного или нескольких объектов групповой политики (GPO), включающих в себя параметры политики MBAM.</span><span class="sxs-lookup"><span data-stu-id="76f30-106">When you have determined the policies that you are going to use, you must use the MBAM 1.0 Group Policy template to create and deploy one or more Group Policy objects (GPO) that include the MBAM policy settings.</span></span>

## <span data-ttu-id="76f30-107">Установка шаблона групповой политики MBAM 1,0</span><span class="sxs-lookup"><span data-stu-id="76f30-107">Install the MBAM 1.0 Group Policy template</span></span>


<span data-ttu-id="76f30-108">Помимо предоставления серверных функций MBAM, приложение настройки сервера включает шаблон групповой политики MBAM.</span><span class="sxs-lookup"><span data-stu-id="76f30-108">In addition to providing server-related features of MBAM, the server setup application includes an MBAM Group Policy template.</span></span> <span data-ttu-id="76f30-109">Вы можете установить этот шаблон на любой компьютер, на котором может быть запущена консоль управления групповыми политиками (GPMC) или расширенное управление групповыми политиками.</span><span class="sxs-lookup"><span data-stu-id="76f30-109">You can install this template on any computer that is able to run the Group Policy Management Console (GPMC) or Advanced Group Policy Management (AGPM).</span></span>

[<span data-ttu-id="76f30-110">Установка шаблона групповой политики MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="76f30-110">How to Install the MBAM 1.0 Group Policy Template</span></span>](how-to-install-the-mbam-10-group-policy-template.md)

## <span data-ttu-id="76f30-111">Развертывание параметров групповой политики MBAM 1,0</span><span class="sxs-lookup"><span data-stu-id="76f30-111">Deploy MBAM 1.0 Group Policy settings</span></span>


<span data-ttu-id="76f30-112">После создания необходимых GPO необходимо развернуть параметры групповой политики MBAM на клиентских компьютерах своей организации.</span><span class="sxs-lookup"><span data-stu-id="76f30-112">After you create the necessary GPOs, you must deploy the MBAM Group Policy settings to your organization’s client computers.</span></span>

[<span data-ttu-id="76f30-113">Изменение параметров объектов групповой политики MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="76f30-113">How to Edit MBAM 1.0 GPO Settings</span></span>](how-to-edit-mbam-10-gpo-settings.md)

## <span data-ttu-id="76f30-114">Отображение панели управления MBAM в Windows</span><span class="sxs-lookup"><span data-stu-id="76f30-114">Display the MBAM Control Panel in Windows</span></span>


<span data-ttu-id="76f30-115">Так как MBAM позволяет настроить панель управления Windows BitLocker по умолчанию, вы также можете скрыть панель управления по умолчанию BitLocker от конечных пользователей с помощью групповой политики.</span><span class="sxs-lookup"><span data-stu-id="76f30-115">Because MBAM offers a customized MBAM control panel that can replace the default Windows BitLocker control panel, you can also choose to hide the default BitLocker Control Panel from end users by using Group Policy.</span></span>

[<span data-ttu-id="76f30-116">Скрытие оснастки шифрования BitLocker по умолчанию в панели управления Windows</span><span class="sxs-lookup"><span data-stu-id="76f30-116">How to Hide Default BitLocker Encryption in The Windows Control Panel</span></span>](how-to-hide-default-bitlocker-encryption-in-the-windows-control-panel.md)

## <span data-ttu-id="76f30-117">Другие ресурсы по развертыванию объектов групповой политики MBAM 1,0</span><span class="sxs-lookup"><span data-stu-id="76f30-117">Other resources for deploying MBAM 1.0 Group Policy Objects</span></span>


[<span data-ttu-id="76f30-118">Развертывание MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="76f30-118">Deploying MBAM 1.0</span></span>](deploying-mbam-10.md)

 

 






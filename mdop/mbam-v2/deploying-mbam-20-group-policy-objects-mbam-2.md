---
title: Развертывание объектов групповой политики MBAM 2.0
description: Развертывание объектов групповой политики MBAM 2.0
author: dansimp
ms.assetid: f17f3897-73ab-431b-a6ec-5a6cff9f279a
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 1ce2c2a37631d9d678d6de7c1d66b7fdafb2ade9
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10823492"
---
# <span data-ttu-id="c0190-103">Развертывание объектов групповой политики MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="c0190-103">Deploying MBAM 2.0 Group Policy Objects</span></span>


<span data-ttu-id="c0190-104">Чтобы успешно развернуть администрирование и мониторинг Microsoft BitLocker (MBAM), необходимо сначала определить групповые политики, которые будут использоваться при реализации администрирования и мониторинга Microsoft BitLocker.</span><span class="sxs-lookup"><span data-stu-id="c0190-104">To successfully deploy Microsoft BitLocker Administration and Monitoring (MBAM), you first have to determine the Group Policies that you will use in your implementation of Microsoft BitLocker Administration and Monitoring.</span></span> <span data-ttu-id="c0190-105">Более подробную информацию о различных доступных политиках можно найти в разделе [планирование MBAM 2,0 с учетом требований к групповой политике](planning-for-mbam-20-group-policy-requirements-mbam-2.md) .</span><span class="sxs-lookup"><span data-stu-id="c0190-105">See [Planning for MBAM 2.0 Group Policy Requirements](planning-for-mbam-20-group-policy-requirements-mbam-2.md) for more information on the different policies that are available.</span></span> <span data-ttu-id="c0190-106">После определения политик, которые вы собираетесь использовать, необходимо создать и развернуть один или несколько объектов групповой политики (GPO), которые включают параметры политики для MBAM с помощью шаблона групповой политики MBAM 2,0.</span><span class="sxs-lookup"><span data-stu-id="c0190-106">When you have determined the policies that you are going to use, you then must create and deploy one or more Group Policy Objects (GPO) that include the policy settings for MBAM by using the MBAM 2.0 Group Policy template.</span></span>

## <span data-ttu-id="c0190-107">Установка шаблона групповой политики MBAM 2,0</span><span class="sxs-lookup"><span data-stu-id="c0190-107">Install the MBAM 2.0 Group Policy Template</span></span>


<span data-ttu-id="c0190-108">В дополнение к серверам, связанным со средствами администрирования и мониторинга Microsoft BitLocker, приложение настройки сервера содержит шаблон групповой политики MBAM.</span><span class="sxs-lookup"><span data-stu-id="c0190-108">In addition to the server-related Microsoft BitLocker Administration and Monitoring features, the server setup application includes a MBAM Group Policy template.</span></span> <span data-ttu-id="c0190-109">Этот шаблон можно установить на любом компьютере, на котором может выполняться консоль управления групповыми политиками (GPMC) или расширенное управление групповыми политиками.</span><span class="sxs-lookup"><span data-stu-id="c0190-109">This template can be installed on any computer able to run the Group Policy Management Console (GPMC) or Advanced Group Policy Management (AGPM).</span></span>

[<span data-ttu-id="c0190-110">Установка шаблона групповой политики MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="c0190-110">How to Install the MBAM 2.0 Group Policy Template</span></span>](how-to-install-the-mbam-20-group-policy-template-mbam-2.md)

## <span data-ttu-id="c0190-111">Развертывание параметров групповой политики MBAM 2,0</span><span class="sxs-lookup"><span data-stu-id="c0190-111">Deploy MBAM 2.0 Group Policy Settings</span></span>


<span data-ttu-id="c0190-112">После создания необходимых GPO необходимо развернуть параметры групповой политики MBAM на клиентских компьютерах своей организации.</span><span class="sxs-lookup"><span data-stu-id="c0190-112">After you create the necessary GPOs, you must deploy the MBAM Group Policy settings to your organization’s client computers.</span></span>

[<span data-ttu-id="c0190-113">Изменение параметров объектов групповой политики MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="c0190-113">How to Edit MBAM 2.0 GPO Settings</span></span>](how-to-edit-mbam-20-gpo-settings-mbam-2.md)

## <span data-ttu-id="c0190-114">Отображение панели управления MBAM в Windows</span><span class="sxs-lookup"><span data-stu-id="c0190-114">Display the MBAM Control Panel in Windows</span></span>


<span data-ttu-id="c0190-115">Так как MBAM позволяет настроить панель управления Windows BitLocker по умолчанию, вы также можете скрыть панель управления по умолчанию BitLocker от конечных пользователей с помощью групповой политики.</span><span class="sxs-lookup"><span data-stu-id="c0190-115">Because MBAM offers a customized MBAM control panel that can replace the default Windows BitLocker control panel, you can also choose to hide the default BitLocker Control Panel from end users by using Group Policy.</span></span>

[<span data-ttu-id="c0190-116">Скрытие оснастки шифрования BitLocker по умолчанию в панели управления Windows</span><span class="sxs-lookup"><span data-stu-id="c0190-116">How to Hide Default BitLocker Encryption in the Windows Control Panel</span></span>](how-to-hide-default-bitlocker-encryption-in-the-windows-control-panel-mbam-2.md)

## <span data-ttu-id="c0190-117">Другие ресурсы по развертыванию объектов групповой политики MBAM 2,0</span><span class="sxs-lookup"><span data-stu-id="c0190-117">Other Resources for Deploying MBAM 2.0 Group Policy Objects</span></span>


[<span data-ttu-id="c0190-118">Развертывание MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="c0190-118">Deploying MBAM 2.0</span></span>](deploying-mbam-20-mbam-2.md)

 

 






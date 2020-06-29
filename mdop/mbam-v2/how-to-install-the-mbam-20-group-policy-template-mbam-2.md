---
title: Установка шаблона групповой политики MBAM 2.0
description: Установка шаблона групповой политики MBAM 2.0
author: dansimp
ms.assetid: bc193232-d060-4285-842e-d194a74dd3c9
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 6420fc4d499de05ed740b038b40aff6a9cd8a05f
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10826252"
---
# <span data-ttu-id="e3c99-103">Установка шаблона групповой политики MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="e3c99-103">How to Install the MBAM 2.0 Group Policy Template</span></span>


<span data-ttu-id="e3c99-104">В дополнение к серверам, связанным со средствами администрирования и мониторинга Microsoft BitLocker (MBAM), в приложение установки сервера входит шаблон групповой политики администрирования Microsoft BitLocker и наблюдения за ними.</span><span class="sxs-lookup"><span data-stu-id="e3c99-104">In addition to the server-related Microsoft BitLocker Administration and Monitoring (MBAM) features, the server setup application includes an Microsoft BitLocker Administration and Monitoring Group Policy template.</span></span> <span data-ttu-id="e3c99-105">Этот шаблон можно установить на любом компьютере, на котором может выполняться консоль управления групповыми политиками (GPMC) или расширенное управление групповыми политиками.</span><span class="sxs-lookup"><span data-stu-id="e3c99-105">This template can be installed on any computer capable of running the Group Policy Management Console (GPMC) or Advanced Group Policy Management (AGPM).</span></span>

<span data-ttu-id="e3c99-106">Ниже описаны действия, которые необходимо выполнить, чтобы установить шаблон групповой политики MBAM.</span><span class="sxs-lookup"><span data-stu-id="e3c99-106">The following steps describe how to install the MBAM Group Policy template.</span></span>

<span data-ttu-id="e3c99-107">**Примечание**  Убедитесь, что вы используете 32-разрядную настройку на 32-разрядных серверах и на 64-разрядной установке на 64-разрядных серверах.</span><span class="sxs-lookup"><span data-stu-id="e3c99-107">**Note** Make sure that you use the 32-bit setup on 32-bit servers and the 64-bit setup on 64-bit servers.</span></span>

 

**<span data-ttu-id="e3c99-108">Установка шаблона групповой политики MBAM</span><span class="sxs-lookup"><span data-stu-id="e3c99-108">To install the MBAM Group Policy template</span></span>**

1.  <span data-ttu-id="e3c99-109">На сервере, на котором вы хотите установить MBAM, запустите мастер установки MBAM, выпуская **MBAMSetup.exe** .</span><span class="sxs-lookup"><span data-stu-id="e3c99-109">On the server where you want to install MBAM, run **MBAMSetup.exe** to start the MBAM installation wizard.</span></span>

2.  <span data-ttu-id="e3c99-110">На странице **приветствия** при необходимости выберите **программу улучшения качества программного**обеспечения, а затем нажмите кнопку **начать**.</span><span class="sxs-lookup"><span data-stu-id="e3c99-110">On the **Welcome** page, optionally select the **Customer Experience Improvement Program**, and then click **Start**.</span></span>

3.  <span data-ttu-id="e3c99-111">Прочтите и подтвердите условия лицензионного соглашения на использование программного обеспечения корпорации Майкрософт, а затем нажмите кнопку **Далее** , чтобы продолжить установку.</span><span class="sxs-lookup"><span data-stu-id="e3c99-111">Read and accept the Microsoft Software License Terms, and then click **Next** to continue the installation.</span></span>

4.  <span data-ttu-id="e3c99-112">По умолчанию для установки выбраны все функции администрирования и мониторинга Microsoft BitLocker.</span><span class="sxs-lookup"><span data-stu-id="e3c99-112">By default, all Microsoft BitLocker Administration and Monitoring features are selected for installation.</span></span> <span data-ttu-id="e3c99-113">Удалите все параметры компонента за исключением **шаблона политики**, а затем нажмите кнопку **Далее** , чтобы продолжить установку.</span><span class="sxs-lookup"><span data-stu-id="e3c99-113">Clear all feature options except for **Policy Template**, and then click **Next** to continue the installation.</span></span>

    <span data-ttu-id="e3c99-114">**Примечание**  Мастер установки проверяет предварительные требования для установки и выводит недостающие необходимые компоненты.</span><span class="sxs-lookup"><span data-stu-id="e3c99-114">**Note** The installation wizard checks the prerequisites for your installation and displays prerequisites that are missing.</span></span> <span data-ttu-id="e3c99-115">Если все необходимые условия выполнены, установка будет продолжена.</span><span class="sxs-lookup"><span data-stu-id="e3c99-115">If all the prerequisites are met, the installation continues.</span></span> <span data-ttu-id="e3c99-116">Если обнаружен отсутствующий предварительный компонент, необходимо устранить недостающие необходимые компоненты и нажать кнопку **проверить необходимые компоненты еще раз**.</span><span class="sxs-lookup"><span data-stu-id="e3c99-116">If a missing prerequisite is detected, you have to resolve the missing prerequisites, and then click **Check prerequisites again**.</span></span> <span data-ttu-id="e3c99-117">После того как все необходимые условия будут выполнены, установка будет возобновлена.</span><span class="sxs-lookup"><span data-stu-id="e3c99-117">Once all prerequisites are met, the installation will resume.</span></span>

     

5.  <span data-ttu-id="e3c99-118">Сведения о том, как и где устанавливать шаблоны, описаны в статье [Загрузка и развертывание шаблонов групповой политики для MDOP (ADMX)](https://technet.microsoft.com/library/dn659707.aspx).</span><span class="sxs-lookup"><span data-stu-id="e3c99-118">For specific steps about how and where to install the templates, see [How to Download and Deploy MDOP Group Policy (.admx) Templates](https://technet.microsoft.com/library/dn659707.aspx).</span></span>

6.  <span data-ttu-id="e3c99-119">После того как мастер настройки администрирования и наблюдения Microsoft BitLocker отобразит страницы установки для выбранных функций, нажмите кнопку **Готово** , чтобы закрыть окно настройки MBAM.</span><span class="sxs-lookup"><span data-stu-id="e3c99-119">After the Microsoft BitLocker Administration and Monitoring Setup wizard displays installation pages for the selected features, click **Finish** to close MBAM Setup.</span></span>

## <span data-ttu-id="e3c99-120">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="e3c99-120">Related topics</span></span>


[<span data-ttu-id="e3c99-121">Развертывание объектов групповой политики MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="e3c99-121">Deploying MBAM 2.0 Group Policy Objects</span></span>](deploying-mbam-20-group-policy-objects-mbam-2.md)

 

 






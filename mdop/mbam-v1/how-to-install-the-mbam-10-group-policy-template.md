---
title: Установка шаблона групповой политики MBAM 1.0
description: Установка шаблона групповой политики MBAM 1.0
author: dansimp
ms.assetid: 451a50b0-939c-47ad-9248-a138deade550
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 8a055c84fb6b1645592b53d957daf157a6055880
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10825339"
---
# <span data-ttu-id="3f03b-103">Установка шаблона групповой политики MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="3f03b-103">How to Install the MBAM 1.0 Group Policy Template</span></span>


<span data-ttu-id="3f03b-104">В дополнение к возможностям администрирования и мониторинга Microsoft BitLocker (MBAM), приложение настройки сервера содержит шаблон групповой политики MBAM.</span><span class="sxs-lookup"><span data-stu-id="3f03b-104">In addition to the server-related features of Microsoft BitLocker Administration and Monitoring (MBAM), the server setup application includes an MBAM Group Policy template.</span></span> <span data-ttu-id="3f03b-105">Вы можете установить этот шаблон на любом компьютере, на котором может выполняться консоль управления групповыми политиками (GPMC) или расширенное управление групповыми политиками.</span><span class="sxs-lookup"><span data-stu-id="3f03b-105">You can install this template on any computer that is capable of running the Group Policy Management Console (GPMC) or Advanced Group Policy Management (AGPM).</span></span>

<span data-ttu-id="3f03b-106">Ниже описаны действия, которые необходимо выполнить, чтобы установить шаблон групповой политики MBAM.</span><span class="sxs-lookup"><span data-stu-id="3f03b-106">The following steps describe how to install the MBAM Group Policy template.</span></span>

<span data-ttu-id="3f03b-107">**Примечание**  Убедитесь, что вы используете 32-разрядную настройку на 32-разрядных серверах и на 64-разрядной установке на 64-разрядных серверах.</span><span class="sxs-lookup"><span data-stu-id="3f03b-107">**Note** Make sure that you use the 32-bit setup on 32-bit servers and the 64-bit setup on 64-bit servers.</span></span>

 

**<span data-ttu-id="3f03b-108">Установка шаблона групповой политики MBAM</span><span class="sxs-lookup"><span data-stu-id="3f03b-108">To install the MBAM Group Policy template</span></span>**

1.  <span data-ttu-id="3f03b-109">Запустите мастер установки MBAM. затем на странице приветствия нажмите кнопку **установить** .</span><span class="sxs-lookup"><span data-stu-id="3f03b-109">Start the MBAM installation wizard; then, click **Install** on the Welcome page.</span></span>

2.  <span data-ttu-id="3f03b-110">Прочтите и подтвердите условия лицензионного соглашения на использование программного обеспечения корпорации Майкрософт, а затем нажмите кнопку **Далее** , чтобы продолжить установку.</span><span class="sxs-lookup"><span data-stu-id="3f03b-110">Read and accept the Microsoft Software License Terms, and then click **Next** to continue the installation.</span></span>

3.  <span data-ttu-id="3f03b-111">По умолчанию для установки выбраны все функции MBAM.</span><span class="sxs-lookup"><span data-stu-id="3f03b-111">By default, all MBAM features are selected for installation.</span></span> <span data-ttu-id="3f03b-112">Удалите все параметры компонента за исключением **шаблона политики**, а затем нажмите кнопку **Далее** , чтобы продолжить установку.</span><span class="sxs-lookup"><span data-stu-id="3f03b-112">Clear all feature options except for **Policy Template**, and then click **Next** to continue the installation.</span></span>

    <span data-ttu-id="3f03b-113">**Примечание**  Мастер установки проверяет предварительные требования для установки и выводит недостающие необходимые компоненты.</span><span class="sxs-lookup"><span data-stu-id="3f03b-113">**Note** The installation wizard checks the prerequisites for your installation and displays the prerequisites that are missing.</span></span> <span data-ttu-id="3f03b-114">Если все необходимые условия выполнены, установка будет продолжена.</span><span class="sxs-lookup"><span data-stu-id="3f03b-114">If all the prerequisites are met, the installation continues.</span></span> <span data-ttu-id="3f03b-115">Если обнаружен отсутствующий предварительный компонент, необходимо разрешить отсутствующий предварительный компонент и нажать кнопку **проверить необходимые компоненты еще раз**.</span><span class="sxs-lookup"><span data-stu-id="3f03b-115">If a missing prerequisite is detected, you must resolve the missing prerequisite and then click **Check prerequisites again**.</span></span> <span data-ttu-id="3f03b-116">После того как все необходимые условия будут выполнены, установка будет возобновлена.</span><span class="sxs-lookup"><span data-stu-id="3f03b-116">Once all prerequisites are met, the installation will resume.</span></span>

     

4.  <span data-ttu-id="3f03b-117">После того как мастер настройки MBAM отобразит страницы установки для выбранных функций, нажмите кнопку **Готово** , чтобы закрыть окно настройки MBAM.</span><span class="sxs-lookup"><span data-stu-id="3f03b-117">After the MBAM Setup wizard displays installation pages for the selected features, click **Finish** to close MBAM Setup.</span></span>

## <span data-ttu-id="3f03b-118">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="3f03b-118">Related topics</span></span>


[<span data-ttu-id="3f03b-119">Развертывание объектов групповой политики MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="3f03b-119">Deploying MBAM 1.0 Group Policy Objects</span></span>](deploying-mbam-10-group-policy-objects.md)

 

 






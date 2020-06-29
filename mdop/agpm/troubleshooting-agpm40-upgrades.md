---
title: Устранение неполадок, возникающих при обновлении
description: Устранение неполадок, возникающих при обновлении
author: dansimp
ms.assetid: 1abbf0c1-fd32-46a8-a3ba-c005f066523d
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 2089eac51803dca60da51f61ebdb112fbf0bda08
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10818249"
---
# <span data-ttu-id="15823-103">Устранение неполадок, возникающих при обновлении</span><span class="sxs-lookup"><span data-stu-id="15823-103">Troubleshooting AGPM Upgrades</span></span>

<span data-ttu-id="15823-104">В этом разделе перечислены распространенные проблемы, которые могут возникнуть при обновлении расширенного сервера управления групповыми политиками (ГРУППОВое Управление политикой) до более новой версии (например, с помощью РАСШИРЕНной политики для 4,0 в расширенный список типов 4,3).</span><span class="sxs-lookup"><span data-stu-id="15823-104">This section lists common issues that you may encounter when you upgrade your Advanced Group Policy Management (AGPM) server to a newer version (e.g. AGPM 4.0 to AGPM 4.3).</span></span> <span data-ttu-id="15823-105">Для диагностики проблем, которых нет в списке, может быть полезно просмотреть [сведения об устранении неполадок с помощью функции управления групповыми политиками](troubleshooting-agpm-agpm40.md) или для администратора расширенного доступа (полный доступ), чтобы использовать ведение журнала и трассировку.</span><span class="sxs-lookup"><span data-stu-id="15823-105">To diagnose issues not listed here, it may be helpful to view the [Troubleshooting AGPM](troubleshooting-agpm-agpm40.md) or for an AGPM Administrator (Full Control) to use logging and tracing.</span></span> <span data-ttu-id="15823-106">Дополнительные сведения можно найти в разделе [Настройка ведения журнала и трассировки](configure-logging-and-tracing-agpm40.md).</span><span class="sxs-lookup"><span data-stu-id="15823-106">For more information, see [Configure Logging and Tracing](configure-logging-and-tracing-agpm40.md).</span></span>

## <span data-ttu-id="15823-107">Какие неполадки возникают?</span><span class="sxs-lookup"><span data-stu-id="15823-107">What problems are you having?</span></span>

-   [<span data-ttu-id="15823-108">Не удалось создать отчет о различиях GPO HTML (код ошибки 80004003).</span><span class="sxs-lookup"><span data-stu-id="15823-108">Failed to generate a HTML GPO difference report (Error code 80004003)</span></span>](#bkmk-error-80004003)

### <a href="" id="bkmk-error-80004003"></a><span data-ttu-id="15823-109">Не удалось создать отчет о различиях GPO HTML (код ошибки 80004003).</span><span class="sxs-lookup"><span data-stu-id="15823-109">Failed to generate a HTML GPO difference report (Error code 80004003)</span></span>

-   <span data-ttu-id="15823-110">**Причина**: вы установили пакет обновления для расширенного набора номенклатур с неверной учетной записью.</span><span class="sxs-lookup"><span data-stu-id="15823-110">**Cause**: You have installed the AGPM upgrade package with an incorrect account.</span></span>

-   <span data-ttu-id="15823-111">**Решение**: для устранения этой проблемы вам потребуется быть АДМИНИСТРАТОРом расширенного разрешения.</span><span class="sxs-lookup"><span data-stu-id="15823-111">**Solution**: You will need to be an AGPM administrator in order to fix this issue.</span></span>
    
    -   <span data-ttu-id="15823-112">Убедитесь, что вы знаете имя пользователя & паролем **учетной записи службы расширенного**использования.</span><span class="sxs-lookup"><span data-stu-id="15823-112">Ensure you know the username & password of your **AGPM service account**.</span></span>

    -   <span data-ttu-id="15823-113">Войдите в систему на своем сервере с РАСШИРЕНным входом в качестве учетной записи службы РАСШИРЕНного протоколирования.</span><span class="sxs-lookup"><span data-stu-id="15823-113">Log onto your AGPM server interactively as your AGPM service account.</span></span>
        
        -   <span data-ttu-id="15823-114">Это важно, так как установка завершается сбоем, если вы используете другую учетную запись.</span><span class="sxs-lookup"><span data-stu-id="15823-114">This is critically important, as the install will fail if you use a different account.</span></span>

    -   <span data-ttu-id="15823-115">Завершите работу службы РАСШИРЕНного ключа.</span><span class="sxs-lookup"><span data-stu-id="15823-115">Shutdown the AGPM service.</span></span>
    
    -   <span data-ttu-id="15823-116">Установите требуемое исправление.</span><span class="sxs-lookup"><span data-stu-id="15823-116">Install the required hotfix.</span></span>
    
    -   <span data-ttu-id="15823-117">Подключитесь к РАСШИРЕНному элементу с помощью клиента с расширенным управлением групповыми политиками, чтобы проверить, что теперь ваши отчеты о</span><span class="sxs-lookup"><span data-stu-id="15823-117">Connect to AGPM using an AGPM client to test that your difference reports are now functioning.</span></span>
    
## <span data-ttu-id="15823-118">Установка пакета исправлений 1 для расширенного управления групповыми политиками Microsoft 4,0 SP3</span><span class="sxs-lookup"><span data-stu-id="15823-118">Install Hotfix Package 1 for Microsoft Advanced Group Policy Management 4.0 SP3</span></span>
    
<span data-ttu-id="15823-119">**Проблема, устраняемая этим исправлением**: Управление групповыми политиками не может создавать отчеты о различиях при управлении и управлением новыми объектами групповой политики (GPO).</span><span class="sxs-lookup"><span data-stu-id="15823-119">**Issue fixed in this hotfix**: AGPM can't generate difference reports when it controls or manages new Group Policy Objects (GPOs).</span></span>

<span data-ttu-id="15823-120">**Как получить это обновление**: установите последнюю версию пакета оптимизации рабочей среды (Майкрософт) ([выпуск за март 2017](https://www.microsoft.com/download/details.aspx?id=54967)).</span><span class="sxs-lookup"><span data-stu-id="15823-120">**How to get this update**: Install the latest version of Microsoft Desktop Optimization Pack ([March 2017 Servicing Release](https://www.microsoft.com/download/details.aspx?id=54967)).</span></span> <span data-ttu-id="15823-121">Дополнительные сведения приведены в [статьях KB 4014009](https://support.microsoft.com/help/4014009/) .</span><span class="sxs-lookup"><span data-stu-id="15823-121">See [KB 4014009](https://support.microsoft.com/help/4014009/) for more information.</span></span>

<span data-ttu-id="15823-122">В частности, в `AGPM4.0SP1_Server_X64_KB4014009.exe` списке после нажатия кнопки "Загрузить" можно выбрать загрузку только первого файла.</span><span class="sxs-lookup"><span data-stu-id="15823-122">More specifically, you can choose to download only the first file, `AGPM4.0SP1_Server_X64_KB4014009.exe`, from the list presented after pressing the download button.</span></span>
      
<span data-ttu-id="15823-123">[Здесь](https://www.microsoft.com/download/details.aspx?id=54967)вы можете найти ссылку Загрузить пакет оптимизации рабочего стола Майкрософт (выпуск за март 2017).</span><span class="sxs-lookup"><span data-stu-id="15823-123">The download link to the Microsoft Desktop Optimization Pack (March 2017 Servicing Release) can be found [here](https://www.microsoft.com/download/details.aspx?id=54967).</span></span>
      
      
## <span data-ttu-id="15823-124">Ссылка для ссылки</span><span class="sxs-lookup"><span data-stu-id="15823-124">Reference link</span></span>
https://support.microsoft.com/help/3127165/hotfix-package-1-for-microsoft-advanced-group-policy-management-4-0-sp
      

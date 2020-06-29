---
title: Управление совместимостью оборудования
description: Управление совместимостью оборудования
author: dansimp
ms.assetid: c74b96b9-8161-49bc-b5bb-4838734e7df5
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: cf9e2c5b2b33ea93d9834a81700bd2be8a9b9757
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10812984"
---
# <span data-ttu-id="ce7b8-103">Управление совместимостью оборудования</span><span class="sxs-lookup"><span data-stu-id="ce7b8-103">How to Manage Hardware Compatibility</span></span>


<span data-ttu-id="ce7b8-104">Администрирование и мониторинг Microsoft BitLocker (MBAM) может собирать сведения о производителе и модели клиентских компьютеров после развертывания политики разрешения проверки совместимости оборудования.</span><span class="sxs-lookup"><span data-stu-id="ce7b8-104">Microsoft BitLocker Administration and Monitoring (MBAM) can collect information about the manufacturer and model of client computers after you deploy the Allow Hardware Compatibility Checking Group Policy.</span></span> <span data-ttu-id="ce7b8-105">Если вы настраиваете этот параметр политики, агент MBAM сообщает сведения о том, что и на компьютере, на сервере MBAM, когда клиент MBAM развертывается на клиентском компьютере.</span><span class="sxs-lookup"><span data-stu-id="ce7b8-105">If you configure this policy, the MBAM agent reports the computer make and model information to the MBAM Server when the MBAM Client is deployed on a client computer.</span></span>

<span data-ttu-id="ce7b8-106">Функция совместимости оборудования полезна, если ваша организация имеет устаревшее оборудование компьютера или компьютеры, не поддерживающие микросхемы доверенного платформенного модуля (TPM).</span><span class="sxs-lookup"><span data-stu-id="ce7b8-106">The Hardware Compatibility feature is helpful when your organization has older computer hardware or computers that do not support Trusted Platform Module (TPM) chips.</span></span> <span data-ttu-id="ce7b8-107">В этих случаях вы можете использовать функцию совместимости оборудования, чтобы убедиться, что шифрование BitLocker применяется только к моделям компьютеров, которые поддерживают его.</span><span class="sxs-lookup"><span data-stu-id="ce7b8-107">In these cases, you can use the Hardware Compatibility feature to ensure that BitLocker encryption is applied only to computer models that support it.</span></span> <span data-ttu-id="ce7b8-108">Если все компьютеры в вашей организации будут поддерживать BitLocker, вам не нужно использовать функцию совместимости оборудования.</span><span class="sxs-lookup"><span data-stu-id="ce7b8-108">If all computers in your organization will support BitLocker, you do not have to use the Hardware Compatibility feature.</span></span>

<span data-ttu-id="ce7b8-109">**Примечание**  По умолчанию функция совместимости оборудования MBAM не включена.</span><span class="sxs-lookup"><span data-stu-id="ce7b8-109">**Note** By default, MBAM Hardware Compatibility feature is not enabled.</span></span> <span data-ttu-id="ce7b8-110">Чтобы включить его, выберите компонент " **Совместимость оборудования** " в разделе " **Сервер администрирования и мониторинга** " во время настройки.</span><span class="sxs-lookup"><span data-stu-id="ce7b8-110">To enable it, select the **Hardware Compatibility** feature under the **Administration and Monitoring Server** feature during setup.</span></span> <span data-ttu-id="ce7b8-111">Дополнительные сведения о настройке и настройке аппаратной совместимости можно найти [в разделе Развертывание инфраструктуры сервера MBAM 1,0](deploying-the-mbam-10-server-infrastructure.md).</span><span class="sxs-lookup"><span data-stu-id="ce7b8-111">For more information about how to set up and configure Hardware Compatibility, see [Deploying the MBAM 1.0 Server Infrastructure](deploying-the-mbam-10-server-infrastructure.md).</span></span>

 

<span data-ttu-id="ce7b8-112">Функция совместимости оборудования работает следующим образом.</span><span class="sxs-lookup"><span data-stu-id="ce7b8-112">The Hardware Compatibility feature works in the following way.</span></span>

****

1.  <span data-ttu-id="ce7b8-113">Агент клиента MBAM обнаружит основные сведения о компьютере, такие как производитель, модель, BIOS Maker, версию BIOS, студии TPM и версию доверенного платформенного модуля, а затем передает эти данные на сервер MBAM.</span><span class="sxs-lookup"><span data-stu-id="ce7b8-113">The MBAM client agent discovers basic computer information such as manufacturer, model, BIOS maker, BIOS version, TPM maker, and TPM version, and then passes this information to the MBAM server.</span></span>

2.  <span data-ttu-id="ce7b8-114">Сервер MBAM формирует список своих клиентских компьютеров и моделей, позволяющий отличать те из них, которые могут или не поддерживают BitLocker.</span><span class="sxs-lookup"><span data-stu-id="ce7b8-114">The MBAM server generates a list of client computer makes and models to enable you to differentiate between those that can or cannot support BitLocker</span></span>

3.  <span data-ttu-id="ce7b8-115">Агенты клиента MBAM, развернутые в корпоративной среде, автоматически обновляют этот список, чтобы все новые возможности компьютера и модели были обнаружены с **неизвестным**состоянием.</span><span class="sxs-lookup"><span data-stu-id="ce7b8-115">The MBAM client agents that are deployed in the enterprise automatically update this list with all new computer makes and models that are discovered with a state of **Unknown**.</span></span> <span data-ttu-id="ce7b8-116">Администратор может затем с помощью веб-сайта администрирования MBAM изменить элементы списка, чтобы указать, что определенный компьютер является **совместимым** или **несовместимым**.</span><span class="sxs-lookup"><span data-stu-id="ce7b8-116">An administrator can then use the MBAM administration website to change list entries to specify a particular computer make and model as **Compatible** or **Incompatible**.</span></span>

4.  <span data-ttu-id="ce7b8-117">Прежде чем агент клиента MBAM начнет шифрование диска, агент сначала проверяет совместимость шифрования BitLocker для оборудования, на котором он запущен.</span><span class="sxs-lookup"><span data-stu-id="ce7b8-117">Before the MBAM client agent begins encrypting a drive, the agent first verifies the BitLocker encryption compatibility of the hardware it is running on.</span></span>

    -   <span data-ttu-id="ce7b8-118">Если оборудование помечено как совместимое, начинается процесс шифрования BitLocker.</span><span class="sxs-lookup"><span data-stu-id="ce7b8-118">If the hardware is marked as compatible, the BitLocker encryption process starts.</span></span> <span data-ttu-id="ce7b8-119">MBAM также будет проверять состояние совместимости компьютера один раз в день.</span><span class="sxs-lookup"><span data-stu-id="ce7b8-119">MBAM will also recheck the hardware compatibility status of the computer one time per day.</span></span>

    -   <span data-ttu-id="ce7b8-120">Если оборудование помечено как несовместимое, агент регистрирует событие и передает ему состояние "аппаратное исключение" в составе отчета о соответствии требованиям.</span><span class="sxs-lookup"><span data-stu-id="ce7b8-120">If the hardware is marked as incompatible, the agent logs an event and passes a “hardware exempted” state as part of compliance reporting.</span></span> <span data-ttu-id="ce7b8-121">Агент проверяет каждые семь дней, чтобы узнать, изменилось ли состояние на "совместимо".</span><span class="sxs-lookup"><span data-stu-id="ce7b8-121">The agent checks every seven days to see whether the state has changed to “compatible.”</span></span>

    -   <span data-ttu-id="ce7b8-122">Если оборудование помечено как неизвестное, процесс шифрования BitLocker не начнется.</span><span class="sxs-lookup"><span data-stu-id="ce7b8-122">If the hardware is marked as unknown, the BitLocker encryption process will not begin.</span></span> <span data-ttu-id="ce7b8-123">Агент клиента MBAM будет проверять состояние совместимости компьютера один раз в день.</span><span class="sxs-lookup"><span data-stu-id="ce7b8-123">The MBAM client agent will recheck the hardware compatibility status of the computer one time per day.</span></span>

<span data-ttu-id="ce7b8-124">**Предупреждение**  Если агент клиента MBAM пытается зашифровать компьютер, который не поддерживает шифрование диска BitLocker, может быть поврежден компьютер.</span><span class="sxs-lookup"><span data-stu-id="ce7b8-124">**Warning** If the MBAM client agent tries to encrypt a computer that does not support BitLocker drive encryption, there is a possibility that the computer will become corrupted.</span></span> <span data-ttu-id="ce7b8-125">Убедитесь, что функция совместимости оборудования настроена правильно, если в вашей организации есть устаревшее оборудование, не поддерживающее BitLocker.</span><span class="sxs-lookup"><span data-stu-id="ce7b8-125">Ensure that the hardware compatibility feature is correctly configured when your organization has older hardware that does not support BitLocker.</span></span>

 

**<span data-ttu-id="ce7b8-126">Для управления совместимостью оборудования</span><span class="sxs-lookup"><span data-stu-id="ce7b8-126">To manage hardware compatibility</span></span>**

1.  <span data-ttu-id="ce7b8-127">Откройте веб-браузер и перейдите на веб-сайт администрирования и мониторинга Microsoft BitLocker.</span><span class="sxs-lookup"><span data-stu-id="ce7b8-127">Open a web browser and navigate to the Microsoft BitLocker Administration and Monitoring website.</span></span> <span data-ttu-id="ce7b8-128">В левой строке меню выберите пункт **оборудование** .</span><span class="sxs-lookup"><span data-stu-id="ce7b8-128">Select **Hardware** in the left menu bar.</span></span>

2.  <span data-ttu-id="ce7b8-129">На правой панели щелкните **Расширенный поиск**, а затем отфильтруйте список всех моделей компьютеров, у которых есть состояние **возможностей** **Unknown**.</span><span class="sxs-lookup"><span data-stu-id="ce7b8-129">On the right pane, click **Advanced Search**, and then filter to display a list of all computer models that have a **Capability** status of **Unknown**.</span></span> <span data-ttu-id="ce7b8-130">Откроется список моделей компьютеров, отвечающих условиям поиска.</span><span class="sxs-lookup"><span data-stu-id="ce7b8-130">A list of computer models matching the search criteria is displayed.</span></span> <span data-ttu-id="ce7b8-131">Администраторы могут добавлять, изменять и удалять новые типы компьютеров на этой странице.</span><span class="sxs-lookup"><span data-stu-id="ce7b8-131">Administrators can add, edit, or remove new computer types from this page.</span></span>

3.  <span data-ttu-id="ce7b8-132">Ознакомьтесь с каждой неизвестной конфигурацией оборудования, чтобы убедиться в том, что конфигурация установлена как **совместимая** или **несовместимая**.</span><span class="sxs-lookup"><span data-stu-id="ce7b8-132">Review each unknown hardware configuration to determine whether the configuration should be set to **Compatible** or **Incompatible**.</span></span>

4.  <span data-ttu-id="ce7b8-133">Выберите одну или несколько строк, а затем выберите команду **установить совместимые** или **установить несовместимые** , чтобы установить совместимость с BitLocker для выбранных моделей компьютеров.</span><span class="sxs-lookup"><span data-stu-id="ce7b8-133">Select one or more rows, and then click either **Set Compatible** or **Set Incompatible** to set the BitLocker compatibility, as appropriate, for the selected computer models.</span></span> <span data-ttu-id="ce7b8-134">Если установлено значение " **совместимый**", BitLocker пытается принудительно применить политику шифрования диска на компьютерах, которые соответствуют поддерживаемой модели.</span><span class="sxs-lookup"><span data-stu-id="ce7b8-134">If set to **Compatible**, BitLocker tries to enforce drive encryption policy on computers that match the supported model.</span></span> <span data-ttu-id="ce7b8-135">Если установлено значение " **несовместимо**", BitLocker не будет применять политику шифрования дисков на этих компьютерах.</span><span class="sxs-lookup"><span data-stu-id="ce7b8-135">If set to **Incompatible**, BitLocker will not enforce drive encryption policy on those computers.</span></span>

    <span data-ttu-id="ce7b8-136">**Примечание**  После того как вы настроили модель компьютера как совместимую, она может принимать более двадцати четырех часов, пока клиент MBAM не начнет шифрование BitLocker на компьютерах, отвечающих этой модели оборудования.</span><span class="sxs-lookup"><span data-stu-id="ce7b8-136">**Note** After you set a computer model as compatible, it can take more than twenty-four hours for the MBAM Client to begin BitLocker encryption on the computers matching that hardware model.</span></span>

     

5.  <span data-ttu-id="ce7b8-137">Администраторы должны регулярно отслеживать список совместимого оборудования, чтобы просмотреть новые модели, обнаруженные агентом MBAM, а затем обновить параметры совместимости с **совместимыми** или **несовместимыми** .</span><span class="sxs-lookup"><span data-stu-id="ce7b8-137">Administrators should regularly monitor the hardware compatibility list to review new models that are discovered by the MBAM agent, and then update their compatibility setting to **Compatible** or **Incompatible** as appropriate.</span></span>

## <span data-ttu-id="ce7b8-138">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="ce7b8-138">Related topics</span></span>


[<span data-ttu-id="ce7b8-139">Администрирование компонентов MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="ce7b8-139">Administering MBAM 1.0 Features</span></span>](administering-mbam-10-features.md)

 

 






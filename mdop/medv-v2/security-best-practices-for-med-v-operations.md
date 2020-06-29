---
title: Рекомендации по обеспечению безопасности операций MED-V
description: Рекомендации по обеспечению безопасности операций MED-V
author: dansimp
ms.assetid: 231e2b9a-8b49-42fe-93b5-2ef12fe17bac
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 4353a15c756dba8cf44f530c2077546e3f9288cd
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10825399"
---
# <span data-ttu-id="ae201-103">Рекомендации по обеспечению безопасности операций MED-V</span><span class="sxs-lookup"><span data-stu-id="ae201-103">Security Best Practices for MED-V Operations</span></span>


<span data-ttu-id="ae201-104">Авторизованный администратор несет ответственность за защиту данных пользователей и поддержание безопасности вашей организации во время и после развертывания рабочих областей MED-V.</span><span class="sxs-lookup"><span data-stu-id="ae201-104">As an authorized administrator, you are responsible to protect the information of the users and maintain security of your organization during and after the deployment of MED-V workspaces.</span></span> <span data-ttu-id="ae201-105">В частности, рассматривайте следующие моменты.</span><span class="sxs-lookup"><span data-stu-id="ae201-105">In particular, consider the following issues.</span></span>

<span data-ttu-id="ae201-106">**Настройка Internet Explorer в рабочей области для MED-V**.</span><span class="sxs-lookup"><span data-stu-id="ae201-106">**Customizing Internet Explorer in the MED-V workspace**.</span></span> <span data-ttu-id="ae201-107">Предыдущие версии операционной системы Windows и Internet Explorer не так защищены, как текущие версии.</span><span class="sxs-lookup"><span data-stu-id="ae201-107">Earlier versions of the Windows operating system and of Internet Explorer are not as secure as current versions.</span></span> <span data-ttu-id="ae201-108">Поэтому Internet Explorer в рабочей области MED-V настроен таким образом, чтобы не допустить Просмотр и другие действия, которые могут представлять угрозу безопасности.</span><span class="sxs-lookup"><span data-stu-id="ae201-108">Therefore, Internet Explorer in the MED-V workspace is configured to prevent browsing and other activities that can pose security risks.</span></span> <span data-ttu-id="ae201-109">Кроме того, параметр зоны безопасности Интернета для Internet Explorer в рабочей области MED-V установлен на самый высокий уровень.</span><span class="sxs-lookup"><span data-stu-id="ae201-109">In addition, the Internet security zone setting for Internet Explorer in the MED-V workspace is set to the highest level.</span></span> <span data-ttu-id="ae201-110">По умолчанию обе эти конфигурации устанавливаются в диспетчер рабочих областей MED-V при создании пакета рабочей области для MED-V.</span><span class="sxs-lookup"><span data-stu-id="ae201-110">By default, both of these configurations are set in the MED-V Workspace Packager when you create your MED-V workspace package.</span></span>

<span data-ttu-id="ae201-111">Используя пакет администрирования Internet Explorer (IEAK) или изменяя параметры по умолчанию в упаковщике рабочих областей MED-V, вы можете настроить Internet Explorer в рабочей области MED-V.</span><span class="sxs-lookup"><span data-stu-id="ae201-111">By using Internet Explorer Administration Kit (IEAK) or by changing the defaults in the MED-V Workspace Packager, you can customize Internet Explorer in the MED-V workspace.</span></span> <span data-ttu-id="ae201-112">Тем не менее, если вы настраиваете Internet Explorer в рабочей области MED-V таким образом, чтобы сделать его более безопасным, вы можете предоставить своей организации угрозу безопасности, которые присутствуют в более ранних версиях Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="ae201-112">However, realize that if you customize Internet Explorer in the MED-V workspace in such a way as to make it less secure, you can expose your organization to those security risks that are present in older versions of Internet Explorer.</span></span>

<span data-ttu-id="ae201-113">С точки зрения безопасности советы и рекомендации по управлению Internet Explorer в рабочей области MED-V описаны ниже.</span><span class="sxs-lookup"><span data-stu-id="ae201-113">From a security perspective, best practices for managing Internet Explorer in the MED-V workspace are as follows:</span></span>

-   <span data-ttu-id="ae201-114">При создании пакета рабочей области для MED-V оставьте значения по умолчанию, чтобы Internet Explorer в рабочей области MED-V был настроен таким образом, чтобы предотвратить просмотр и другие действия, которые могут представлять угрозу безопасности.</span><span class="sxs-lookup"><span data-stu-id="ae201-114">When creating your MED-V workspace package, leave the defaults set so that Internet Explorer in the MED-V workspace is configured to prevent browsing and other activities that can pose security risks.</span></span>

-   <span data-ttu-id="ae201-115">При создании пакета рабочей области для MED-V оставьте набор по умолчанию, чтобы параметры безопасности для зоны Интернет-безопасности оставались на самом верхнем уровне.</span><span class="sxs-lookup"><span data-stu-id="ae201-115">When creating your MED-V workspace package, leave the defaults set so that the security setting for the Internet security zone remains at the highest level.</span></span>

-   <span data-ttu-id="ae201-116">Настройте корпоративный прокси-сервер или ограничение доступа Internet Explorer, чтобы заблокировать домены, которые находятся за пределами интрасети вашей компании.</span><span class="sxs-lookup"><span data-stu-id="ae201-116">Configure your enterprise proxy or Internet Explorer Content Advisor to block domains that are outside your company’s intranet.</span></span>

**<span data-ttu-id="ae201-117">Настройка рабочей области MED-V для всех пользователей на общем компьютере.</span><span class="sxs-lookup"><span data-stu-id="ae201-117">Configuring a MED-V workspace for all users on a shared computer.</span></span>** <span data-ttu-id="ae201-118">Если вы настраиваете рабочую область MED-V таким образом, что она доступна всем пользователям на общем компьютере, убедитесь в том, что гостевая виртуальная машина (VHD) размещена в расположении, которое предоставляет доступ для чтения и записи для всех пользователей в этой системе.</span><span class="sxs-lookup"><span data-stu-id="ae201-118">When configuring a MED-V workspace so that it can be accessed by all users on a shared computer, realize that the guest virtual machine (VHD) is put in a location that gives Read and Write access to all users on that system.</span></span>

**<span data-ttu-id="ae201-119">Настройка учетной записи прокси-сервера для присоединения к домену.</span><span class="sxs-lookup"><span data-stu-id="ae201-119">Configuring a proxy account for domain joining.</span></span>** <span data-ttu-id="ae201-120">При настройке учетной записи прокси-сервера для присоединения виртуальных машин к домену необходимо знать, что конечный пользователь может получить учетные данные учетной записи-посредника.</span><span class="sxs-lookup"><span data-stu-id="ae201-120">When configuring a proxy account for joining virtual machines to the domain, you must know that it is possible for an end user to obtain the proxy account credentials.</span></span> <span data-ttu-id="ae201-121">Таким образом, необходимо предпринять определенные меры предосторожности, такие как ограничение прав пользователя для учетной записи, чтобы предотвратить использование учетных данных конечным пользователем для обеспечения ущерба.</span><span class="sxs-lookup"><span data-stu-id="ae201-121">Thus, necessary precautions must be taken, such as limiting account user rights, to prevent an end user from using the credentials for causing harm.</span></span>

**<span data-ttu-id="ae201-122">Настройка Sysprep.</span><span class="sxs-lookup"><span data-stu-id="ae201-122">Sysprep Configuration.</span></span>** <span data-ttu-id="ae201-123">Несмотря на то, что файл Sysprep. INF зашифрован по умолчанию, его содержимое может быть расшифровано и прочитано любым определенным конечным пользователем, который может успешно войти на виртуальную машину.</span><span class="sxs-lookup"><span data-stu-id="ae201-123">Although the Sysprep.inf file is encrypted by default, its contents can be decrypted and read by any determined end user who can successfully log on to the virtual machine.</span></span> <span data-ttu-id="ae201-124">Это вызывает проблемы безопасности, так как файл Sysprep. INF может содержать учетные данные в дополнение к ключу продукта Windows.</span><span class="sxs-lookup"><span data-stu-id="ae201-124">This raises security concerns because the Sysprep.inf file can contain credentials in addition to a Windows product key.</span></span>

<span data-ttu-id="ae201-125">Вы можете уменьшить этот риск, настроив ограниченную учетную запись для присоединения виртуальных машин к домену и указав учетные данные для этой учетной записи при настройке Sysprep.</span><span class="sxs-lookup"><span data-stu-id="ae201-125">You can lessen this risk by setting up a limited account for joining virtual machines to the domain and specifying the credentials for that account when configuring Sysprep.</span></span> <span data-ttu-id="ae201-126">Кроме того, вы также можете настроить программу Sysprep и запустить настройку, чтобы она выполнялась **в режиме ожидания** и потребовать от конечных пользователей предоставить свои учетные данные для присоединения виртуальной машины к домену.</span><span class="sxs-lookup"><span data-stu-id="ae201-126">Alternately, you can also configure Sysprep and first time setup to run in **Attended** mode and require end users to provide their credentials for joining the virtual machine to the domain.</span></span>

<span data-ttu-id="ae201-127">Рекомендуется указать, что FtsCompletion.exe выполняется под учетной записью, предоставляющей конечные пользователи для подключения к гостевой службе через клиент подключения к удаленному рабочему столу (RDC).</span><span class="sxs-lookup"><span data-stu-id="ae201-127">A MED-V best practice is to specify that FtsCompletion.exe is run under an account that gives the end user rights to connect to the guest through the Remote Desktop Connection (RDC) Client.</span></span>

**<span data-ttu-id="ae201-128">Проверка подлинности конечных пользователей.</span><span class="sxs-lookup"><span data-stu-id="ae201-128">End-user authentication.</span></span>** <span data-ttu-id="ae201-129">Включение кэширования учетных данных конечного пользователя обеспечивает наилучшее взаимодействие с пользователями MED-V, но создает потенциальный способ получить доступ к учетным данным конечного пользователя.</span><span class="sxs-lookup"><span data-stu-id="ae201-129">Enabling the caching of end-user credentials provides the best user experience of MED-V, but creates the potential that someone could gain access to the end user’s credentials.</span></span> <span data-ttu-id="ae201-130">Единственный способ уменьшить этот риск — указать в **упаковщике рабочих областей MED-V** , что учетные данные конечного пользователя не сохраняются.</span><span class="sxs-lookup"><span data-stu-id="ae201-130">The only way to lessen this risk is by specifying on the **MED-V Workspace Packager** that end-user credentials are not stored.</span></span> <span data-ttu-id="ae201-131">Дополнительные сведения о проверке подлинности конечных пользователей можно найти в разделе [Проверка подлинности конечных пользователей MED-V](authentication-of-med-v-end-users.md).</span><span class="sxs-lookup"><span data-stu-id="ae201-131">For more information about authentication of end users, see [Authentication of MED-V End Users](authentication-of-med-v-end-users.md).</span></span>

## <span data-ttu-id="ae201-132">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="ae201-132">Related topics</span></span>


[<span data-ttu-id="ae201-133">Устранение неполадок в операциях</span><span class="sxs-lookup"><span data-stu-id="ae201-133">Operations Troubleshooting</span></span>](operations-troubleshooting-medv2.md)

[<span data-ttu-id="ae201-134">Microsoft Enterprise Virtualization 2,0</span><span class="sxs-lookup"><span data-stu-id="ae201-134">Microsoft Enterprise Desktop Virtualization 2.0</span></span>](index.md)

 

 






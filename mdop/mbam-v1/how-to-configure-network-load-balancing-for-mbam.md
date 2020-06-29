---
title: Настройка балансировки сетевой нагрузки для MBAM
description: Настройка балансировки сетевой нагрузки для MBAM
author: dansimp
ms.assetid: df2208c3-352b-4a48-9722-237b0c8cd6a5
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: a04bc74a9dab7bfe18eed8e5a3c1b6ca64d88b5b
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10825512"
---
# <span data-ttu-id="5a580-103">Настройка балансировки сетевой нагрузки для MBAM</span><span class="sxs-lookup"><span data-stu-id="5a580-103">How to Configure Network Load Balancing for MBAM</span></span>


<span data-ttu-id="5a580-104">Чтобы убедиться в том, что требования к оборудованию и программному обеспечению, чтобы установить сервер администрирования и мониторинга, приведены в разделе Требования к [развертыванию MBAM 1,0](mbam-10-deployment-prerequisites.md) и [поддерживаемые конфигурации MBAM 1,0](mbam-10-supported-configurations.md).</span><span class="sxs-lookup"><span data-stu-id="5a580-104">To verify that you have met the prerequisites and hardware and software requirements to install the Administration and Monitoring Server feature, see [MBAM 1.0 Deployment Prerequisites](mbam-10-deployment-prerequisites.md) and [MBAM 1.0 Supported Configurations](mbam-10-supported-configurations.md).</span></span>

<span data-ttu-id="5a580-105">**Примечание**  Чтобы получить файлы журнала установки, необходимо установить администрирование и мониторинг Microsoft BitLocker (MBAM) с помощью пакета **msiexec** и параметра **/l** &lt; Location &gt; .</span><span class="sxs-lookup"><span data-stu-id="5a580-105">**Note** To obtain the setup log files, you must install Microsoft BitLocker Administration and Monitoring (MBAM) by using the **msiexec** package and the **/l** &lt;location&gt; option.</span></span> <span data-ttu-id="5a580-106">Файлы журнала создаются в указанном расположении.</span><span class="sxs-lookup"><span data-stu-id="5a580-106">The Log files are created in the location that you specify.</span></span>

<span data-ttu-id="5a580-107">Дополнительные файлы журнала установки создаются в папке% temp% пользователя, устанавливающего MBAM.</span><span class="sxs-lookup"><span data-stu-id="5a580-107">Additional setup log files are created in the %temp% folder of the user who installs MBAM.</span></span>

 

<span data-ttu-id="5a580-108">Кластеры балансировки сетевой нагрузки (NLB) для компонента администрирования и мониторинга сервера предоставляют масштабируемость в MBAM и поддерживает более 55 000 MBAM клиентских компьютеров.</span><span class="sxs-lookup"><span data-stu-id="5a580-108">The Network Load Balancing (NLB) clusters for the Administration and Monitoring Server feature provides scalability in MBAM and it should support more than 55,000 MBAM client computers.</span></span>

<span data-ttu-id="5a580-109">**Примечание**  Балансировка сетевой нагрузки Windows Server распределяет запросы клиентов по набору серверов, которые настроены в едином кластере серверов.</span><span class="sxs-lookup"><span data-stu-id="5a580-109">**Note** Windows Server Network Load Balancing distributes client requests across a set of servers that are configured into a single server cluster.</span></span> <span data-ttu-id="5a580-110">При установке компонента балансировки сетевой нагрузки на каждом сервере (узлах) в кластере кластер представляет виртуальный IP-адрес или полное доменное имя (FQDN) для клиентских запросов.</span><span class="sxs-lookup"><span data-stu-id="5a580-110">When Network Load Balancing is installed on each of the servers (hosts) in a cluster, the cluster presents a virtual IP address or fully qualified domain name (FQDN) to client requests.</span></span> <span data-ttu-id="5a580-111">Первоначальные запросы клиента поступают на все узлы в кластере, но только один узел принимает и обрабатывает запрос.</span><span class="sxs-lookup"><span data-stu-id="5a580-111">The initial client requests go to all the hosts in the cluster, but only one host accepts and handles the request.</span></span>

<span data-ttu-id="5a580-112">На всех компьютерах, которые будут входить в кластер NLB, необходимо выполнить указанные ниже требования.</span><span class="sxs-lookup"><span data-stu-id="5a580-112">All computers that will be part of a NLB cluster have the following requirements:</span></span>

-   <span data-ttu-id="5a580-113">Все компьютеры в кластере NLB должны находиться в одном домене.</span><span class="sxs-lookup"><span data-stu-id="5a580-113">All computers in the NLB cluster must be in the same domain.</span></span>

-   <span data-ttu-id="5a580-114">Каждый компьютер в кластере NLB должен использовать статический IP-адрес.</span><span class="sxs-lookup"><span data-stu-id="5a580-114">Each computer in the NLB cluster must use a static IP address.</span></span>

-   <span data-ttu-id="5a580-115">Для каждого компьютера в NLB-кластере должно быть включено средство балансировки нагрузки сети.</span><span class="sxs-lookup"><span data-stu-id="5a580-115">Each computer in the NLB cluster must have Network Load Balancing enabled.</span></span>

-   <span data-ttu-id="5a580-116">Кластеру NLB требуется статический IP-адрес, а в системе доменных имен (DNS) должна быть вручную создана запись узла.</span><span class="sxs-lookup"><span data-stu-id="5a580-116">The NLB cluster requires a static IP address, and a host record must be manually created in the domain name system (DNS).</span></span>

 

## <span data-ttu-id="5a580-117">Настройка балансировки нагрузки сети для серверов администрирования и мониторинга MBAM</span><span class="sxs-lookup"><span data-stu-id="5a580-117">Configuring Network Load Balancing for MBAM Administration and Monitoring Servers</span></span>


<span data-ttu-id="5a580-118">Ниже описана процедура настройки виртуального имени кластера NLB и IP-адреса для двух серверов администрирования и мониторинга MBAM и настройки клиентов MBAM на использование кластера NLB.</span><span class="sxs-lookup"><span data-stu-id="5a580-118">The following steps describe how to configure an NLB cluster virtual name and IP address for two MBAM Administration and Monitoring servers, and how to configure MBAM Clients to use the NLB Cluster.</span></span>

<span data-ttu-id="5a580-119">Перед выполнением процедур, описанных в этой статье, необходимо установить компонент сервера администрирования и мониторинга MBAM с помощью той же привязки для порта IIS на двух разных серверных компьютерах, которые соответствуют требованиям для настройки компонентов сервера MBAM и NLB-кластеров.</span><span class="sxs-lookup"><span data-stu-id="5a580-119">Before you begin the procedures described in this topic, you must have the MBAM Administration and Monitoring Server feature successfully installed by using the same IIS port binding on two separate server computers that meet the prerequisites for both MBAM Server feature installation and NLB Cluster configuration.</span></span>

<span data-ttu-id="5a580-120">**Примечание**  В этом разделе описан базовый процесс создания кластера NLB с помощью диспетчера балансировки сетевой нагрузки.</span><span class="sxs-lookup"><span data-stu-id="5a580-120">**Note** This topic describes the basic process of using Network Load Balancing Manager to create an NLB Cluster.</span></span> <span data-ttu-id="5a580-121">Точные действия, которые необходимо выполнить для настройки сервера Windows как части NLB-кластера, зависят от используемой версии Windows Server.</span><span class="sxs-lookup"><span data-stu-id="5a580-121">The exact steps to configure a Windows Server as part of an NLB cluster depend on the Windows Server version in use..</span></span> <span data-ttu-id="5a580-122">Дополнительные сведения о том, как создать NLBs на WindowsServer2008, можно найти в разделе [Создание кластеров балансировки нагрузки сети](https://go.microsoft.com/fwlink/?LinkId=197176) в библиотеке TechNet для Windows Server2008.</span><span class="sxs-lookup"><span data-stu-id="5a580-122">For more information about how to create NLBs on WindowsServer2008, see [Creating Network Load Balancing Clusters](https://go.microsoft.com/fwlink/?LinkId=197176) in the Windows Server2008 TechNet library.</span></span>

 

**<span data-ttu-id="5a580-123">Настройка виртуального имени кластера NLB и IP-адреса для двух серверов администрирования и мониторинга MBAM</span><span class="sxs-lookup"><span data-stu-id="5a580-123">To configure an NLB Cluster Virtual Name and IP address for two MBAM Administration and Monitoring Servers</span></span>**

1.  <span data-ttu-id="5a580-124">Нажмите кнопку **Пуск**, выберите **все программы**, а затем — **Администрирование**, а затем — **Диспетчер балансировки сетевой нагрузки**.</span><span class="sxs-lookup"><span data-stu-id="5a580-124">Click **Start**, click **All Programs**, click **Administrative Tools**, and then click **Network Load Balancing Manager**.</span></span>

    <span data-ttu-id="5a580-125">**Примечание**  Если диспетчер NLB отсутствует, вы можете установить его в качестве функции WindowsServer.</span><span class="sxs-lookup"><span data-stu-id="5a580-125">**Note** If the NLB Manager is not present, you can install it as a WindowsServer feature.</span></span> <span data-ttu-id="5a580-126">Вы должны установить эту функцию на серверах администрирования и мониторинга MBAM, если вы хотите настроить ее в NLB-кластере.</span><span class="sxs-lookup"><span data-stu-id="5a580-126">You must install this feature on both MBAM Administration and Monitoring servers if you want to configure it into the NLB cluster.</span></span>

     

2.  <span data-ttu-id="5a580-127">В строке меню нажмите кнопку **кластер**и выберите команду **создать** , чтобы открыть диалоговое окно **Параметры кластера** .</span><span class="sxs-lookup"><span data-stu-id="5a580-127">On the menu bar, click **Cluster**, and then click **New** to open the **Cluster Parameters** dialog box.</span></span>

3.  <span data-ttu-id="5a580-128">В диалоговом окне **Параметры кластера** введите данные для IP-конфигурации кластера NLB.</span><span class="sxs-lookup"><span data-stu-id="5a580-128">In the **Cluster Parameters** dialog box, enter the information for the NLB cluster IP configuration:</span></span>

    -   <span data-ttu-id="5a580-129">**IP-адрес:** IP-адрес кластера NLB, зарегистрированный в DNS</span><span class="sxs-lookup"><span data-stu-id="5a580-129">**IP address:** NLB cluster IP address registered in DNS</span></span>

    -   <span data-ttu-id="5a580-130">**Маска подсети:** Маска подсети IP-адреса кластера NLB, зарегистрированная в DNS</span><span class="sxs-lookup"><span data-stu-id="5a580-130">**Subnet mask:** NLB cluster IP address subnet mask registered in DNS</span></span>

    -   <span data-ttu-id="5a580-131">**Полное Интернет-имя:** Полное доменное имя кластера NLB, зарегистрированное в DNS</span><span class="sxs-lookup"><span data-stu-id="5a580-131">**Full Internet name:** FQDN of NLB cluster name registered in DNS</span></span>

4.  <span data-ttu-id="5a580-132">Убедитесь в том, что **одноадресная рассылка** выбрана в **режиме работы кластера**, и нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="5a580-132">Ensure that **Unicast** is selected in **Cluster operation mode**, and then click **Next**.</span></span>

5.  <span data-ttu-id="5a580-133">На странице **IP-адреса кластера** нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="5a580-133">On the **Cluster IP Addresses** page, click **Next**.</span></span>

6.  <span data-ttu-id="5a580-134">На странице **правила для порта** нажмите кнопку **изменить** , чтобы определить порты, на которые будет отвечать кластер NLB, и настройте порты, которые используются для связи между клиентом и сервером, как они определены для сайта, или нажмите кнопку **Далее** , чтобы разрешить IP-адрес кластера NLB для ответа на все порты TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="5a580-134">On the **Port Rules** page, click **Edit** to define the ports that the NLB cluster will respond to and configure the ports that are used for client-to-site system communication as they are defined for the site, or click **Next** to enable the NLB cluster IP address to respond to all TCP/IP ports.</span></span>

    <span data-ttu-id="5a580-135">**Примечание**  Убедитесь, что для **affinity** задано значение **Single**.</span><span class="sxs-lookup"><span data-stu-id="5a580-135">**Note** Ensure that **Affinity** is set to **Single**.</span></span>

     

7.  <span data-ttu-id="5a580-136">На странице **Connect (подключение** ) введите имя узла MBAM администрирования и сервера мониторинга, которое будет входить в NLB-кластер на **узле**, и нажмите кнопку **подключить**.</span><span class="sxs-lookup"><span data-stu-id="5a580-136">On the **Connect** page, enter an MBAM Administration and Monitoring server instance host name that will be part of the NLB cluster in **Host**, and then click **Connect**.</span></span>

8.  <span data-ttu-id="5a580-137">В разделе **интерфейсы, доступные для настройки нового кластера**выберите сетевой интерфейс, который будет настроен на взаимодействие с кластером NLB, и нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="5a580-137">In **Interfaces available for configuring a new cluster**, select the networking interface that will be configured to respond to NLB cluster communication, and then click **Next**.</span></span>

9.  <span data-ttu-id="5a580-138">На странице **Параметры узла** просмотрите сведения о том, что **ВЫДЕЛЕННЫЕ параметры IP-конфигурации** выводят на экран специальную конфигурацию IP-адреса для нужного узла кластера NLB, убедитесь, что **первоначально задано**состояние узла **по умолчанию** , и нажмите кнопку **Готово**.</span><span class="sxs-lookup"><span data-stu-id="5a580-138">On the **Host Parameters** page, review the information displayed to ensure that the **Dedicated IP configuration** settings display the dedicated host IP configuration for the correct NLB cluster host, check that the Initial host state **Default state:** is **Started**, and then click **Finish**.</span></span>

    <span data-ttu-id="5a580-139">**Примечание**  На странице **Параметры узла** также отображается приоритет узла NLB Clustered (от 1 до 32).</span><span class="sxs-lookup"><span data-stu-id="5a580-139">**Note** The **Host Parameters** page also displays the NLB cluster host priority, which is 1 through 32.</span></span> <span data-ttu-id="5a580-140">Поскольку новые узлы добавляются в NLB-кластер, приоритет узла должен отличаться от ранее добавленных узлов.</span><span class="sxs-lookup"><span data-stu-id="5a580-140">As new hosts are added to the NLB cluster, the host priority must differ from the previously added hosts.</span></span> <span data-ttu-id="5a580-141">Приоритет автоматически увеличивается при использовании диспетчера балансировки сетевой нагрузки.</span><span class="sxs-lookup"><span data-stu-id="5a580-141">The priority is automatically incremented when you use the Network Load Balancing Manager.</span></span>

     

10. <span data-ttu-id="5a580-142">Щелкните \*\* &lt; имя &gt; кластера NLB\*\* и убедитесь, **что перед** продолжением отображается **состояние** интерфейса узла NLB.</span><span class="sxs-lookup"><span data-stu-id="5a580-142">Click **&lt;NLB cluster name&gt;** and ensure that the NLB host interface **Status** displays **Converged** before you continue.</span></span> <span data-ttu-id="5a580-143">На этом этапе может потребоваться обновить конфигурацию кластера NLB в качестве конфигурации TCP/IP узла, которая изменяется диспетчером NLB.</span><span class="sxs-lookup"><span data-stu-id="5a580-143">This step might require that you refresh the NLB cluster display as the host TCP/IP configuration that is being modified by the NLB Manager.</span></span>

11. <span data-ttu-id="5a580-144">Чтобы добавить дополнительные узлы в NLB-кластер, щелкните правой кнопкой мыши \*\* &lt; &gt; имя кластера NLB\*\*, выберите команду **Добавить узел к кластеру,** а затем повторите действия 7 – 10 для каждой системы сайта, которая будет частью кластера NLB.</span><span class="sxs-lookup"><span data-stu-id="5a580-144">To add additional hosts to the NLB cluster, right-click **&lt;NLB cluster name&gt;**, click **Add Host to Cluster,** and then repeat steps 7 through 10 for each site system that will be part of the NLB cluster.</span></span>

12. <span data-ttu-id="5a580-145">На компьютере, на котором установлен шаблон групповой политики MBAM, измените параметры групповой политики MBAM, чтобы настроить конечные точки служб MBAM на использование имени кластера NLB и соответствующей привязки порта IIS для доступа к функциям сервера MBAM администрирования и мониторинга, установленным на компьютерах кластера NLB.</span><span class="sxs-lookup"><span data-stu-id="5a580-145">On a computer that has MBAM Group Policy template installed, modify the MBAM Group Policy settings to configure the MBAM services endpoints to use the NLB Cluster name and the appropriate IIS port binding to access the MBAM Administration and Monitoring Server features that are installed on the NLB Cluster computers.</span></span> <span data-ttu-id="5a580-146">Дополнительные сведения о том, как изменить параметры объекта групповой политики MBAM, можно найти [в разделе Изменение параметров GPO MBAM 1,0](how-to-edit-mbam-10-gpo-settings.md).</span><span class="sxs-lookup"><span data-stu-id="5a580-146">For more information about how to edit MBAM GPO settings, see [How to Edit MBAM 1.0 GPO Settings](how-to-edit-mbam-10-gpo-settings.md).</span></span> <span data-ttu-id="5a580-147">Если серверы администрирования и мониторинга MBAM являются новыми для вашей среды, убедитесь в том, что членство в локальной группе безопасности настроено должным образом.</span><span class="sxs-lookup"><span data-stu-id="5a580-147">If the MBAM Administration and Monitoring servers are new to your environment, ensure that the required local security group memberships have been properly configured.</span></span> <span data-ttu-id="5a580-148">Дополнительные сведения о требованиях к группе безопасности можно найти в разделе [Планирование ролей администратора для MBAM 1,0](planning-for-mbam-10-administrator-roles.md).</span><span class="sxs-lookup"><span data-stu-id="5a580-148">For more information about security group requirements, see [Planning for MBAM 1.0 Administrator Roles](planning-for-mbam-10-administrator-roles.md).</span></span>

13. <span data-ttu-id="5a580-149">После завершения настройки NLB-кластера рекомендуется проверить работоспособность кластера MBAM администрирования и мониторинга NLB.</span><span class="sxs-lookup"><span data-stu-id="5a580-149">When the NLB Cluster configuration is complete, we recommend that you validate that the MBAM Administration and Monitoring NLB Cluster is functional.</span></span> <span data-ttu-id="5a580-150">Для этого откройте веб-браузер на компьютере, отличном от серверов, настроенных в NLB, и убедитесь, что вы можете получить доступ к веб-сайту администрирования и мониторинга MBAM с помощью полного доменного имени NLB.</span><span class="sxs-lookup"><span data-stu-id="5a580-150">To do this, open a web browser on a computer other than the servers that are configured in the NLB, and ensure that you can access the MBAM Administration and Monitoring web site by using the NLB FQDN.</span></span>

## <span data-ttu-id="5a580-151">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="5a580-151">Related topics</span></span>


[<span data-ttu-id="5a580-152">Развертывание инфраструктуры сервера MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="5a580-152">Deploying the MBAM 1.0 Server Infrastructure</span></span>](deploying-the-mbam-10-server-infrastructure.md)

 

 






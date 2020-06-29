---
title: Настройка подключения к серверу AGPM
description: Настройка подключения к серверу AGPM
author: dansimp
ms.assetid: 9a42b5bc-41be-44ef-a6e2-6f56e2cf1996
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 88182f0e79f1a8bcce53e0d50c014e8d4aa29286
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10818912"
---
# <span data-ttu-id="42456-103">Настройка подключения к серверу AGPM</span><span class="sxs-lookup"><span data-stu-id="42456-103">Configure the AGPM Server Connection</span></span>


<span data-ttu-id="42456-104">Расширенное управление групповыми политиками хранит все версии всех управляемых объектов групповой политики (GPO) в центральном архиве, поэтому администраторы групповой политики могут просматривать и изменять GPO в автономном режиме без немедленного воздействия на развернутую версию каждого объекта групповой политики.</span><span class="sxs-lookup"><span data-stu-id="42456-104">Advanced Group Policy Management (AGPM) stores all versions of each controlled Group Policy object (GPO) in a central archive, so Group Policy administrators can view and modify GPOs offline without immediately impacting the deployed version of each GPO.</span></span>

<span data-ttu-id="42456-105">Учетная запись пользователя с ролью администратора РАСШИРЕНного управления правами (полного доступа), учетная запись пользователя утверждающего, создавшего объект групповой политики, которая использовалась в этих процедурах, или учетная запись пользователя с необходимыми разрешениями в расширенном управлении групповыми политиками, должна быть выполнена для централизованной настройки расположения архивов для всех администраторов групповой политики.</span><span class="sxs-lookup"><span data-stu-id="42456-105">A user account with the AGPM Administrator (Full Control) role, the user account of the Approver who created the GPO used in these procedures, or a user account with the necessary permissions in Advanced Group Policy Management is required to complete these procedures for centrally configuring archive locations for all Group Policy administrators.</span></span> <span data-ttu-id="42456-106">Ознакомьтесь с подробными сведениями в разделе "Дополнительные сведения".</span><span class="sxs-lookup"><span data-stu-id="42456-106">Review the details in "Additional considerations" in this topic.</span></span>

## <span data-ttu-id="42456-107">Настройка подключения к серверу РАСШИРЕНного конфигурирования</span><span class="sxs-lookup"><span data-stu-id="42456-107">Configuring the AGPM Server connection</span></span>


<span data-ttu-id="42456-108">Как Администратор расширенного управления групповыми политиками (полный доступ) вы можете гарантировать, что все администраторы групповой политики подключаются к одному и тому же серверу с помощью централизованной настройки параметров.</span><span class="sxs-lookup"><span data-stu-id="42456-108">As an AGPM Administrator (Full Control), you can ensure that all Group Policy administrators connect to the same AGPM Server by centrally configuring the setting.</span></span> <span data-ttu-id="42456-109">Если в вашей среде для некоторых или всех доменов требуется отдельный сервер РАСШИРЕНного доменных данных, настройте дополнительные серверы РАСШИРЕНного использования в качестве исключений по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="42456-109">If your environment requires separate AGPM Servers for some or all domains, configure those additional AGPM Servers as exceptions to the default.</span></span> <span data-ttu-id="42456-110">Если вы не настраиваете подключения к серверу РАСШИРЕНного управления правами, каждый администратор групповой политики должен вручную настроить отображение сервера расширенного управления групповыми политиками для каждого домена.</span><span class="sxs-lookup"><span data-stu-id="42456-110">If you do not centrally configure AGPM Server connections, each Group Policy administrator must manually configure the AGPM Server to be displayed for each domain.</span></span>

-   [<span data-ttu-id="42456-111">Настройка сервера РАСШИРЕНного администрирования для всех администраторов групповой политики</span><span class="sxs-lookup"><span data-stu-id="42456-111">Configure an AGPM Server for all Group Policy administrators</span></span>](#bkmk-defaultarchiveloc)

-   [<span data-ttu-id="42456-112">Настройка дополнительных серверов РАСШИРЕНного администрирования для всех администраторов групповой политики</span><span class="sxs-lookup"><span data-stu-id="42456-112">Configure additional AGPM Servers for all Group Policy administrators</span></span>](#bkmk-additionalarchiveloc)

-   [<span data-ttu-id="42456-113">Настройка сервера РАСШИРЕНного конфигурирования для учетной записи вручную</span><span class="sxs-lookup"><span data-stu-id="42456-113">Manually configure an AGPM Server for your account</span></span>](#bkmk-manuallyconfigurearchiveloc)

### <a href="" id="bkmk-defaultarchiveloc"></a>

**<span data-ttu-id="42456-114">Настройка сервера РАСШИРЕНного конфигурирования для всех администраторов групповой политики</span><span class="sxs-lookup"><span data-stu-id="42456-114">To configure an AGPM Server for all Group Policy administrators</span></span>**

1.  <span data-ttu-id="42456-115">В дереве **консоли управления групповыми политиками** измените объект групповой политики, который применяется ко всем администраторам групповой политики.</span><span class="sxs-lookup"><span data-stu-id="42456-115">In the **Group Policy Management Console** tree, edit a GPO that is applied to all Group Policy administrators.</span></span> <span data-ttu-id="42456-116">(Дополнительные сведения можно найти [в разделе изменение объекта групповой политики](editing-a-gpo.md).)</span><span class="sxs-lookup"><span data-stu-id="42456-116">(For more information, see [Editing a GPO](editing-a-gpo.md).)</span></span>

2.  <span data-ttu-id="42456-117">В **редакторе объектов групповой политики**выберите **Конфигурация пользователя**, **шаблоны**и **компоненты Windows**.</span><span class="sxs-lookup"><span data-stu-id="42456-117">In the **Group Policy Object Editor**, click **User Configuration**, **Administrative Templates**, and **Windows Components**.</span></span>

3.  <span data-ttu-id="42456-118">Если в разделе **компоненты Windows**отсутствует **Расширенное** руководство, выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="42456-118">If **AGPM** is not listed under **Windows Components**:</span></span>

    1.  <span data-ttu-id="42456-119">Щелкните правой кнопкой мыши **Административные шаблоны** и выберите команду **Добавить или удалить шаблоны**.</span><span class="sxs-lookup"><span data-stu-id="42456-119">Right-click **Administrative Templates** and click **Add/Remove Templates**.</span></span>

    2.  <span data-ttu-id="42456-120">Нажмите кнопку **Добавить**, выберите элемент **расширенного формата ADMX** или для **расширенного**расширения (ADM), нажмите кнопку **Открыть**, а затем — **Закрыть**.</span><span class="sxs-lookup"><span data-stu-id="42456-120">Click **Add**, select **agpm.admx** or **agpm.adm**, click **Open**, and then click **Close**.</span></span>

4.  <span data-ttu-id="42456-121">В разделе **компоненты Windows**дважды щелкните элемент **расширенной**учетной записью.</span><span class="sxs-lookup"><span data-stu-id="42456-121">Under **Windows Components**, double-click **AGPM**.</span></span>

5.  <span data-ttu-id="42456-122">В области сведений дважды щелкните **сервер расширенного доменных данных (все домены)**.</span><span class="sxs-lookup"><span data-stu-id="42456-122">In the details pane, double-click **AGPM Server (all domains)**.</span></span>

6.  <span data-ttu-id="42456-123">В окне **свойств сервера (все домены)** для настольных компьютеров установите флажок **включено** и введите полное имя компьютера и порт (например, Server.contoso.com:4600).</span><span class="sxs-lookup"><span data-stu-id="42456-123">In the **AGPM Server (all domains) Properties** window, select the **Enabled** check box, and type the fully-qualified computer name and port (for example, server.contoso.com:4600).</span></span>

7.  <span data-ttu-id="42456-124">Нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="42456-124">Click **OK**.</span></span> <span data-ttu-id="42456-125">Если вы не хотите настраивать дополнительные подключения к РАСШИРЕНному серверу, закройте **Редактор объектов групповой политики** и разверните объект GPO.</span><span class="sxs-lookup"><span data-stu-id="42456-125">Unless you want to configure additional AGPM Server connections, close the **Group Policy Object Editor** and deploy the GPO.</span></span> <span data-ttu-id="42456-126">(Дополнительные сведения можно найти [в разделе Развертывание объекта групповой политики](deploy-a-gpo.md).) При обновлении групповой политики подключение к серверу РАСШИРЕНного политики конфигурации выполняется для всех администраторов групповых политик.</span><span class="sxs-lookup"><span data-stu-id="42456-126">(For more information, see [Deploy a GPO](deploy-a-gpo.md).) When Group Policy is updated, the AGPM Server connection is configured for all Group Policy administrators.</span></span>

### <a href="" id="bkmk-additionalarchiveloc"></a>

**<span data-ttu-id="42456-127">Настройка дополнительных серверов РАСШИРЕНного администрирования для всех администраторов групповой политики</span><span class="sxs-lookup"><span data-stu-id="42456-127">To configure additional AGPM Servers for all Group Policy administrators</span></span>**

1.  <span data-ttu-id="42456-128">Если подключение к серверу РАСШИРЕНного конфигурирования не настроено, выполните описанные выше действия, чтобы настроить сервер по умолчанию для всех доменов.</span><span class="sxs-lookup"><span data-stu-id="42456-128">If no AGPM Server connection has been configured, follow the preceding procedure to configure a default AGPM Server for all domains.</span></span>

2.  <span data-ttu-id="42456-129">Чтобы настроить отдельные серверы расширенного управления групповыми политиками для некоторых или всех доменов (переопределение сервера РАСШИРЕНной политики по умолчанию), в дереве **консоли управления групповыми политиками** измените объект групповой политики, применяемый ко всем администраторам групповой политики.</span><span class="sxs-lookup"><span data-stu-id="42456-129">To configure separate AGPM Servers for some or all domains (overriding the default AGPM Server), in the **Group Policy Management Console** tree, edit a GPO that is applied to all Group Policy administrators.</span></span> <span data-ttu-id="42456-130">(Дополнительные сведения можно найти [в разделе изменение объекта групповой политики](editing-a-gpo.md).)</span><span class="sxs-lookup"><span data-stu-id="42456-130">(For more information, see [Editing a GPO](editing-a-gpo.md).)</span></span>

3.  <span data-ttu-id="42456-131">В разделе **Конфигурация пользователя** в **редакторе объектов групповой политики**дважды щелкните элемент **Административные шаблоны**, **компоненты Windows**, а затем выберите пункт **Расширенное**редактирование.</span><span class="sxs-lookup"><span data-stu-id="42456-131">Under **User Configuration** in the **Group Policy Object Editor**, double-click **Administrative Templates**, **Windows Components**, and then **AGPM**.</span></span>

4.  <span data-ttu-id="42456-132">В области сведений дважды щелкните **сервер с расширенным управлением групповыми политиками**.</span><span class="sxs-lookup"><span data-stu-id="42456-132">In the details pane, double-click **AGPM Server**.</span></span>

5.  <span data-ttu-id="42456-133">В окне **Свойства сервера расширенного выбора параметров** установите флажок **включено** и нажмите кнопку **Показать**.</span><span class="sxs-lookup"><span data-stu-id="42456-133">In the **AGPM Server Properties** window, select the **Enabled** check box, and click **Show**.</span></span>

6.  <span data-ttu-id="42456-134">В окне " **Показать содержимое** ":</span><span class="sxs-lookup"><span data-stu-id="42456-134">In the **Show Contents** window:</span></span>

    1.  <span data-ttu-id="42456-135">Щелкните **Добавить**.</span><span class="sxs-lookup"><span data-stu-id="42456-135">Click **Add**.</span></span>

    2.  <span data-ttu-id="42456-136">В поле " **имя параметра**" введите имя домена (например, Server1.contoso.com).</span><span class="sxs-lookup"><span data-stu-id="42456-136">For **Value Name**, type the domain name (for example, server1.contoso.com).</span></span>

    3.  <span data-ttu-id="42456-137">В поле " **значение**" введите имя и порт сервера расширенного использования для этого домена (например, Server2.contoso.com:4600), а затем нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="42456-137">For **Value**, type the AGPM Server name and port to use for this domain (for example, server2.contoso.com:4600), and then click **OK**.</span></span> <span data-ttu-id="42456-138">(По умолчанию служба РАСШИРЕНных аналитик прослушивает порт 4600.</span><span class="sxs-lookup"><span data-stu-id="42456-138">(By default, the AGPM Service listens on port 4600.</span></span> <span data-ttu-id="42456-139">Чтобы использовать другой порт, ознакомьтесь со сведениями о том, как [изменить порт, прослушиваемый службой расширенного выбора](modify-the-port-on-which-the-agpm-service-listens.md).</span><span class="sxs-lookup"><span data-stu-id="42456-139">To use a different port, see [Modify the Port on Which the AGPM Service Listens](modify-the-port-on-which-the-agpm-service-listens.md).)</span></span>

    4.  <span data-ttu-id="42456-140">Повторите эти действия для каждого домена, не использующего сервер по умолчанию для РАСШИРЕНного использования функций.</span><span class="sxs-lookup"><span data-stu-id="42456-140">Repeat for each domain not using the default AGPM Server.</span></span>

7.  <span data-ttu-id="42456-141">Нажмите кнопку **ОК** , чтобы закрыть окно " **Показать содержимое** " и " **Свойства сервера** в разделе".</span><span class="sxs-lookup"><span data-stu-id="42456-141">Click **OK** to close the **Show Contents** and **AGPM Server Properties** windows.</span></span>

8.  <span data-ttu-id="42456-142">Закройте **Редактор объектов групповой политики**.</span><span class="sxs-lookup"><span data-stu-id="42456-142">Close the **Group Policy Object Editor**.</span></span> <span data-ttu-id="42456-143">(Дополнительные сведения можно найти [в разделе Развертывание объекта групповой политики](deploy-a-gpo.md).) При обновлении групповой политики для всех администраторов групповой политики настраиваются новые подключения к серверам РАСШИРЕНного ключа.</span><span class="sxs-lookup"><span data-stu-id="42456-143">(For more information, see [Deploy a GPO](deploy-a-gpo.md).) When Group Policy is updated, the new AGPM Server connections are configured for all Group Policy administrators.</span></span>

### <a href="" id="bkmk-manuallyconfigurearchiveloc"></a>

<span data-ttu-id="42456-144">Если вы централизованно настроили подключение к серверу РАСШИРЕНного доступа, параметр вручную будет недоступен для всех администраторов групповой политики.</span><span class="sxs-lookup"><span data-stu-id="42456-144">If you have centrally configured the AGPM Server connection, the option to manually it is unavailable for all Group Policy administrators.</span></span>

**<span data-ttu-id="42456-145">Ручная настройка сервера РАСШИРЕНного отображения для учетной записи</span><span class="sxs-lookup"><span data-stu-id="42456-145">To manually configure the AGPM Server to display for your account</span></span>**

1.  <span data-ttu-id="42456-146">В дереве **консоли управления групповыми политиками** нажмите кнопку **изменить элемент управления** в лесу и домене, в котором вы хотите управлять объектами групповой политики.</span><span class="sxs-lookup"><span data-stu-id="42456-146">In the **Group Policy Management Console** tree, click **Change Control** in the forest and domain in which you want to manage GPOs.</span></span>

2.  <span data-ttu-id="42456-147">В области сведений щелкните вкладку **сервер расширенного сервера** .</span><span class="sxs-lookup"><span data-stu-id="42456-147">In the details pane, click the **AGPM Server** tab.</span></span>

3.  <span data-ttu-id="42456-148">Введите полное имя компьютера для сервера расширенного управления групповыми политиками, который управляет архивом, используемым для этого домена (например, server.contoso.com), и портом, по которому служба управления ГРУППОВыми операциями прослушивает (по умолчанию — порт 4600).</span><span class="sxs-lookup"><span data-stu-id="42456-148">Enter the fully-qualified computer name for the AGPM Server that manages the archive used for this domain (for example, server.contoso.com) and the port on which the AGPM Service listens (by default, port 4600).</span></span>

4.  <span data-ttu-id="42456-149">Нажмите кнопку **Применить**, а затем — **Да** для подтверждения.</span><span class="sxs-lookup"><span data-stu-id="42456-149">Click **Apply**, then click **Yes** to confirm.</span></span>

### <span data-ttu-id="42456-150">Дополнительные рекомендации</span><span class="sxs-lookup"><span data-stu-id="42456-150">Additional considerations</span></span>

-   <span data-ttu-id="42456-151">Вы должны иметь возможность изменить и развернуть объект групповой политики, чтобы выполнить процедуры централизованной настройки подключений к серверам расширенного управления групповыми политиками для всех администраторов групповой политики.</span><span class="sxs-lookup"><span data-stu-id="42456-151">You must be able to edit and deploy a GPO to perform the procedures for centrally configuring AGPM Server connections for all Group Policy administrators.</span></span> <span data-ttu-id="42456-152">Дополнительные сведения: [редактирование GPO](editing-a-gpo.md) и [Развертывание объекта групповой политики](deploy-a-gpo.md) .</span><span class="sxs-lookup"><span data-stu-id="42456-152">See [Editing a GPO](editing-a-gpo.md) and [Deploy a GPO](deploy-a-gpo.md) for additional detail.</span></span>

-   <span data-ttu-id="42456-153">Выбранный сервер РАСШИРЕНного доступа определяет объекты, которые будут отображаться на вкладке " **содержимое** ", и укажите расположение, в котором будут применяться параметры вкладки **делегирования домена** .</span><span class="sxs-lookup"><span data-stu-id="42456-153">The AGPM Server selected determines which GPOs are displayed on the **Contents** tab and to what location the **Domain Delegation** tab settings are applied.</span></span> <span data-ttu-id="42456-154">Если вы не управляете централизованно с помощью административного шаблона, каждый администратор групповой политики должен настроить этот параметр таким образом, чтобы он указывал на сервер РАСШИРЕНного управления правами для домена.</span><span class="sxs-lookup"><span data-stu-id="42456-154">If not centrally managed through the Administrative Template, each Group Policy administrator must configure this setting to point to the AGPM Server for the domain.</span></span>

-   <span data-ttu-id="42456-155">Членство в группе Владельцы создателей групповой политики должно быть ограничено, чтобы не использовать ее для обхода управления доступом к объектам групповой политики с помощью РАСШИРЕНного доступа к данным.</span><span class="sxs-lookup"><span data-stu-id="42456-155">Membership in the Group Policy Creator Owners group should be restricted so that it is not used to circumvent the management of access to GPOs by AGPM.</span></span> <span data-ttu-id="42456-156">(В **консоли управления групповыми политиками**щелкните **объекты групповой политики** в лесу и домене, в которых вы хотите управлять объектами GPO, выберите пункт **Делегирование**и настройте параметры в соответствии с потребностями Организации.)</span><span class="sxs-lookup"><span data-stu-id="42456-156">(In the **Group Policy Management Console**, click **Group Policy Objects** in the forest and domain in which you want to manage GPOs, click **Delegation**, and then configure the settings to meet the needs of your organization.)</span></span>

### <span data-ttu-id="42456-157">Дополнительные ссылки</span><span class="sxs-lookup"><span data-stu-id="42456-157">Additional references</span></span>

-   [<span data-ttu-id="42456-158">Выполнение задач администратора AGPM</span><span class="sxs-lookup"><span data-stu-id="42456-158">Performing AGPM Administrator Tasks</span></span>](performing-agpm-administrator-tasks.md)

 

 






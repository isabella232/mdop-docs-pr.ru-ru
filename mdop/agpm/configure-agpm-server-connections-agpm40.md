---
title: Настройка подключений к серверу AGPM
description: Настройка подключений к серверу AGPM
author: dansimp
ms.assetid: bbbb15e8-35e7-403c-b695-7a6ebeb87839
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 9b6b065b9855c6edf44456026baa32e8d9a4674f
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10819072"
---
# <span data-ttu-id="23931-103">Настройка подключений к серверу AGPM</span><span class="sxs-lookup"><span data-stu-id="23931-103">Configure AGPM Server Connections</span></span>


<span data-ttu-id="23931-104">Все версии всех управляемых объектов групповой политики (GPO) хранятся в центральном архиве, так что администраторы групповых политик могут просматривать и изменять GPO в автономном режиме без немедленного воздействия на развернутую версию каждого GPO.</span><span class="sxs-lookup"><span data-stu-id="23931-104">All versions of each controlled Group Policy Object (GPO) are stored in a central archive so that Group Policy administrators can view and modify GPOs offline without immediately impacting the deployed version of each GPO.</span></span>

<span data-ttu-id="23931-105">Учетная запись пользователя с ролью администратора РАСШИРЕНного управления правами (полного доступа), учетная запись пользователя утверждающего, создавшего объект групповой политики, которая использовалась в этих процедурах, или учетная запись пользователя с необходимыми разрешениями в расширенном управлении групповыми политиками (ГРУППОВое управление), необходимы для того, чтобы выполнить эти процедуры для централизованной настройки расположения архивов для всех администраторов</span><span class="sxs-lookup"><span data-stu-id="23931-105">A user account with the AGPM Administrator (Full Control) role, the user account of the Approver who created the GPO used in these procedures, or a user account with the necessary permissions in Advanced Group Policy Management (AGPM) is required to complete these procedures for centrally configuring archive locations for all Group Policy administrators.</span></span> <span data-ttu-id="23931-106">Ознакомьтесь с подробными сведениями в разделе "Дополнительные сведения".</span><span class="sxs-lookup"><span data-stu-id="23931-106">Review the details in "Additional considerations" in this topic.</span></span>

## <span data-ttu-id="23931-107">Настройка подключений к серверу с помощью РАСШИРЕНного конфигурирования</span><span class="sxs-lookup"><span data-stu-id="23931-107">Configuring AGPM Server connections</span></span>


<span data-ttu-id="23931-108">Как Администратор расширенного управления групповыми политиками, вы можете обеспечить подключение всех администраторов групповой политики к одному и тому же серверу с помощью централизованной настройки соответствующего параметра.</span><span class="sxs-lookup"><span data-stu-id="23931-108">As an AGPM Administrator, you can ensure that all Group Policy administrators connect to the same AGPM Server by centrally configuring the associated setting.</span></span> <span data-ttu-id="23931-109">Если в вашей среде для некоторых или всех доменов требуется отдельный сервер РАСШИРЕНного доменных данных, настройте дополнительные серверы РАСШИРЕНного использования в качестве исключений по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="23931-109">If your environment requires separate AGPM Servers for some or all domains, configure those additional AGPM Servers as exceptions to the default.</span></span> <span data-ttu-id="23931-110">Если вы не настраиваете подключения к серверу РАСШИРЕНного управления правами, каждый администратор групповой политики должен вручную настроить отображение сервера расширенного управления групповыми политиками для каждого домена.</span><span class="sxs-lookup"><span data-stu-id="23931-110">If you do not centrally configure AGPM Server connections, each Group Policy administrator must manually configure the AGPM Server to be displayed for each domain.</span></span>

-   [<span data-ttu-id="23931-111">Настройка подключения к серверу РАСШИРЕНного конфигурирования для всех администраторов групповой политики</span><span class="sxs-lookup"><span data-stu-id="23931-111">Configure an AGPM Server connection for all Group Policy administrators</span></span>](#bkmk-defaultarchiveloc)

-   [<span data-ttu-id="23931-112">Настройка дополнительных подключений к РАСШИРЕНным конфигурациям для всех администраторов групповой политики</span><span class="sxs-lookup"><span data-stu-id="23931-112">Configure additional AGPM Server connections for all Group Policy administrators</span></span>](#bkmk-additionalarchiveloc)

-   [<span data-ttu-id="23931-113">Настройка подключения к серверу РАСШИРЕНного конфигурирования для учетной записи вручную</span><span class="sxs-lookup"><span data-stu-id="23931-113">Manually configure an AGPM Server connection for your account</span></span>](#bkmk-manuallyconfigurearchiveloc)

### <a href="" id="bkmk-defaultarchiveloc"></a>

**<span data-ttu-id="23931-114">Настройка подключения к серверу РАСШИРЕНного конфигурирования для всех администраторов групповой политики</span><span class="sxs-lookup"><span data-stu-id="23931-114">To configure an AGPM Server connection for all Group Policy administrators</span></span>**

1.  <span data-ttu-id="23931-115">В дереве **консоли управления групповыми политиками** измените объект групповой политики, который применяется ко всем администраторам групповой политики.</span><span class="sxs-lookup"><span data-stu-id="23931-115">In the **Group Policy Management Console** tree, edit a GPO that is applied to all Group Policy administrators.</span></span> <span data-ttu-id="23931-116">(Дополнительные сведения можно найти [в разделе изменение объекта групповой политики](editing-a-gpo-agpm40.md).)</span><span class="sxs-lookup"><span data-stu-id="23931-116">(For more information, see [Editing a GPO](editing-a-gpo-agpm40.md).)</span></span>

2.  <span data-ttu-id="23931-117">В окне **редактора управления групповыми политиками** выберите элементы **Конфигурация пользователя**, **политики**, **Административные шаблоны**, **компоненты Windows**и управление **групповыми**политиками.</span><span class="sxs-lookup"><span data-stu-id="23931-117">In the **Group Policy Management Editor** window, click **User Configuration**, **Policies**, **Administrative Templates**, **Windows Components**, and **AGPM**.</span></span>

3.  <span data-ttu-id="23931-118">В области сведений дважды щелкните элемент расширенной настройки и выберите **сервер по умолчанию (все домены)**.</span><span class="sxs-lookup"><span data-stu-id="23931-118">In the details pane, double-click **AGPM: Specify default AGPM Server (all domains)**.</span></span>

4.  <span data-ttu-id="23931-119">В окне **Свойства** установите флажок **включено** и введите полное имя компьютера и порт (например, Server.contoso.com:4600).</span><span class="sxs-lookup"><span data-stu-id="23931-119">In the **Properties** window, select the **Enabled** check box, and type the fully-qualified computer name and port (for example, server.contoso.com:4600).</span></span>

5.  <span data-ttu-id="23931-120">Нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="23931-120">Click **OK**.</span></span> <span data-ttu-id="23931-121">Если вы не хотите настраивать дополнительные подключения к серверу РАСШИРЕНного управления правами, закройте окно **редактора групповых политик** и разверните объект групповой политики.</span><span class="sxs-lookup"><span data-stu-id="23931-121">Unless you want to configure additional AGPM Server connections, close the **Group Policy Management Editor** window and deploy the GPO.</span></span> <span data-ttu-id="23931-122">(Дополнительные сведения можно найти [в разделе Развертывание объекта групповой политики](deploy-a-gpo-agpm40.md).) При обновлении групповой политики подключение к серверу РАСШИРЕНного политики конфигурации выполняется для всех администраторов групповых политик.</span><span class="sxs-lookup"><span data-stu-id="23931-122">(For more information, see [Deploy a GPO](deploy-a-gpo-agpm40.md).) When Group Policy is updated, the AGPM Server connection is configured for all Group Policy administrators.</span></span>

### <a href="" id="bkmk-additionalarchiveloc"></a>

**<span data-ttu-id="23931-123">Настройка дополнительных подключений к серверу РАСШИРЕНного администрирования для всех администраторов групповой политики</span><span class="sxs-lookup"><span data-stu-id="23931-123">To configure additional AGPM Server connections for all Group Policy administrators</span></span>**

1.  <span data-ttu-id="23931-124">Если подключение к серверу РАСШИРЕНного конфигурирования не настроено, выполните описанные выше действия, чтобы настроить сервер по умолчанию для всех доменов.</span><span class="sxs-lookup"><span data-stu-id="23931-124">If no AGPM Server connection has been configured, follow the preceding procedure to configure a default AGPM Server for all domains.</span></span>

2.  <span data-ttu-id="23931-125">Чтобы настроить отдельные серверы расширенного управления групповыми политиками для некоторых или всех доменов (переопределение сервера РАСШИРЕНной политики по умолчанию), в дереве **консоли управления групповыми политиками** измените объект групповой политики, применяемый ко всем администраторам групповой политики.</span><span class="sxs-lookup"><span data-stu-id="23931-125">To configure separate AGPM Servers for some or all domains (overriding the default AGPM Server), in the **Group Policy Management Console** tree, edit a GPO that is applied to all Group Policy administrators.</span></span> <span data-ttu-id="23931-126">(Дополнительные сведения можно найти [в разделе изменение объекта групповой политики](editing-a-gpo-agpm40.md).)</span><span class="sxs-lookup"><span data-stu-id="23931-126">(For more information, see [Editing a GPO](editing-a-gpo-agpm40.md).)</span></span>

3.  <span data-ttu-id="23931-127">В окне **редактора управления групповыми политиками** щелкните **Конфигурация пользователя**, **политики**, **Административные шаблоны**, **компоненты Windows**, **а затем выберите**пункт многоязыковый интерфейс.</span><span class="sxs-lookup"><span data-stu-id="23931-127">In the **Group Policy Management Editor** window, click **User Configuration**, **Policies**, **Administrative Templates**, **Windows Components**, and then **AGPM**.</span></span>

4.  <span data-ttu-id="23931-128">В области сведений дважды щелкните элемент **групповое руководство: укажите серверы расширенного**выбора.</span><span class="sxs-lookup"><span data-stu-id="23931-128">In the details pane, double-click **AGPM: Specify AGPM Servers**.</span></span>

5.  <span data-ttu-id="23931-129">В окне **Свойства** установите флажок **включено** и нажмите кнопку **Показать**.</span><span class="sxs-lookup"><span data-stu-id="23931-129">In the **Properties** window, select the **Enabled** check box, and click **Show**.</span></span>

6.  <span data-ttu-id="23931-130">В окне " **Показать содержимое** ":</span><span class="sxs-lookup"><span data-stu-id="23931-130">In the **Show Contents** window:</span></span>

    1.  <span data-ttu-id="23931-131">Щелкните **Добавить**.</span><span class="sxs-lookup"><span data-stu-id="23931-131">Click **Add**.</span></span>

    2.  <span data-ttu-id="23931-132">В поле " **имя параметра**" введите имя домена (например, Server1.contoso.com).</span><span class="sxs-lookup"><span data-stu-id="23931-132">For **Value Name**, type the domain name (for example, server1.contoso.com).</span></span>

    3.  <span data-ttu-id="23931-133">В поле " **значение**" введите имя и порт сервера расширенного использования для этого домена (например, Server2.contoso.com:4600), а затем нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="23931-133">For **Value**, type the AGPM Server name and port to use for this domain (for example, server2.contoso.com:4600), and then click **OK**.</span></span> <span data-ttu-id="23931-134">(По умолчанию служба РАСШИРЕНных аналитик прослушивает порт 4600.</span><span class="sxs-lookup"><span data-stu-id="23931-134">(By default, the AGPM Service listens on port 4600.</span></span> <span data-ttu-id="23931-135">Чтобы использовать другой порт, ознакомьтесь со сведениями о том, как [изменить службу расширенного использования службы](modify-the-agpm-service-agpm40.md).)</span><span class="sxs-lookup"><span data-stu-id="23931-135">To use a different port, see [Modify the AGPM Service](modify-the-agpm-service-agpm40.md).)</span></span>

    4.  <span data-ttu-id="23931-136">Повторите эти действия для каждого домена, не использующего сервер по умолчанию для РАСШИРЕНного использования функций.</span><span class="sxs-lookup"><span data-stu-id="23931-136">Repeat for each domain not using the default AGPM Server.</span></span>

7.  <span data-ttu-id="23931-137">Нажмите кнопку **ОК** , чтобы закрыть окно " **Показать содержимое** и **Свойства** ".</span><span class="sxs-lookup"><span data-stu-id="23931-137">Click **OK** to close the **Show Contents** and **Properties** windows.</span></span>

8.  <span data-ttu-id="23931-138">Закройте окно **редактора управления групповыми политиками** .</span><span class="sxs-lookup"><span data-stu-id="23931-138">Close the **Group Policy Management Editor** window.</span></span> <span data-ttu-id="23931-139">(Дополнительные сведения можно найти [в разделе Развертывание объекта групповой политики](deploy-a-gpo-agpm40.md).) При обновлении групповой политики для всех администраторов групповой политики настраиваются новые подключения к серверам РАСШИРЕНного ключа.</span><span class="sxs-lookup"><span data-stu-id="23931-139">(For more information, see [Deploy a GPO](deploy-a-gpo-agpm40.md).) When Group Policy is updated, the new AGPM Server connections are configured for all Group Policy administrators.</span></span>

### <a href="" id="bkmk-manuallyconfigurearchiveloc"></a>

<span data-ttu-id="23931-140">Если вы централизованно настроили подключение к серверу РАСШИРЕНного доступа, параметр для его настройки вручную будет недоступен для всех администраторов групповой политики.</span><span class="sxs-lookup"><span data-stu-id="23931-140">If you have centrally configured the AGPM Server connection, the option to manually configure it is unavailable for all Group Policy administrators.</span></span>

**<span data-ttu-id="23931-141">Настройка сервера РАСШИРЕНного выбора, который будет отображаться для вашей учетной записи, вручную</span><span class="sxs-lookup"><span data-stu-id="23931-141">To manually configure which AGPM Server to display for your account</span></span>**

1.  <span data-ttu-id="23931-142">В дереве **консоли управления групповыми политиками** нажмите кнопку **изменить элемент управления** в лесу и домене, в котором вы хотите управлять объектами групповой политики.</span><span class="sxs-lookup"><span data-stu-id="23931-142">In the **Group Policy Management Console** tree, click **Change Control** in the forest and domain in which you want to manage GPOs.</span></span>

2.  <span data-ttu-id="23931-143">В области сведений щелкните вкладку **сервер расширенного сервера** .</span><span class="sxs-lookup"><span data-stu-id="23931-143">In the details pane, click the **AGPM Server** tab.</span></span>

3.  <span data-ttu-id="23931-144">Введите полное имя компьютера для сервера расширенного управления групповыми политиками, который управляет архивом, используемым для этого домена (например, server.contoso.com), и портом, по которому служба управления ГРУППОВыми операциями прослушивает (по умолчанию — порт 4600).</span><span class="sxs-lookup"><span data-stu-id="23931-144">Enter the fully-qualified computer name for the AGPM Server that manages the archive used for this domain (for example, server.contoso.com) and the port on which the AGPM Service listens (by default, port 4600).</span></span>

4.  <span data-ttu-id="23931-145">Нажмите кнопку **Применить**, а затем — **Да** для подтверждения.</span><span class="sxs-lookup"><span data-stu-id="23931-145">Click **Apply**, then click **Yes** to confirm.</span></span>

### <span data-ttu-id="23931-146">Дополнительные рекомендации</span><span class="sxs-lookup"><span data-stu-id="23931-146">Additional considerations</span></span>

-   <span data-ttu-id="23931-147">Вы должны иметь возможность изменить и развернуть объект групповой политики, чтобы выполнить процедуры централизованной настройки подключений к серверам расширенного управления групповыми политиками для всех администраторов групповой политики.</span><span class="sxs-lookup"><span data-stu-id="23931-147">You must be able to edit and deploy a GPO to perform the procedures for centrally configuring AGPM Server connections for all Group Policy administrators.</span></span> <span data-ttu-id="23931-148">Дополнительные сведения: [редактирование GPO](editing-a-gpo-agpm40.md) и [Развертывание объекта групповой политики](deploy-a-gpo-agpm40.md) .</span><span class="sxs-lookup"><span data-stu-id="23931-148">See [Editing a GPO](editing-a-gpo-agpm40.md) and [Deploy a GPO](deploy-a-gpo-agpm40.md) for additional detail.</span></span>

-   <span data-ttu-id="23931-149">Выбранный сервер РАСШИРЕНного доступа к сети определяет объекты, которые будут отображаться на вкладке " **содержимое** ", и укажите расположение, в которое будут применены параметры вкладки **делегирования домена** .</span><span class="sxs-lookup"><span data-stu-id="23931-149">The selected AGPM Server determines which GPOs are displayed on the **Contents** tab and to what location the **Domain Delegation** tab settings are applied.</span></span> <span data-ttu-id="23931-150">Если вы не управляете централизованно с помощью административного шаблона, каждый администратор групповой политики должен настроить этот параметр таким образом, чтобы он указывал на сервер РАСШИРЕНного управления правами для домена.</span><span class="sxs-lookup"><span data-stu-id="23931-150">If not centrally managed through the Administrative template, each Group Policy administrator must configure this setting to point to the AGPM Server for the domain.</span></span>

-   <span data-ttu-id="23931-151">Членство в группе "владельцы создателей групповой политики" должно быть ограничено, soit не используется для обхода управления доступом к GPO.</span><span class="sxs-lookup"><span data-stu-id="23931-151">Membership in the Group Policy Creator Owners group should be restricted, soit is not used to circumvent AGPM management of access to GPOs.</span></span> <span data-ttu-id="23931-152">(В **консоли управления групповыми политиками**щелкните **объекты групповой политики** в лесу и домене, в которых вы хотите управлять объектами GPO, выберите пункт **Делегирование**и настройте параметры в соответствии с потребностями Организации.)</span><span class="sxs-lookup"><span data-stu-id="23931-152">(In the **Group Policy Management Console**, click **Group Policy Objects** in the forest and domain in which you want to manage GPOs, click **Delegation**, and then configure the settings to meet the needs of your organization.)</span></span>

### <span data-ttu-id="23931-153">Дополнительные ссылки</span><span class="sxs-lookup"><span data-stu-id="23931-153">Additional references</span></span>

-   [<span data-ttu-id="23931-154">Настройка средства расширенного управления групповыми политиками</span><span class="sxs-lookup"><span data-stu-id="23931-154">Configuring Advanced Group Policy Management</span></span>](configuring-advanced-group-policy-management-agpm40.md)

 

 






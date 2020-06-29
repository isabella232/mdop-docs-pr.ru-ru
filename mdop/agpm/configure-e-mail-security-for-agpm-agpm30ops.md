---
title: Настройка безопасности электронной почты для AGPM
description: Настройка безопасности электронной почты для AGPM
author: dansimp
ms.assetid: 4850ed8e-a1c6-43f0-95c5-853aa66a94ae
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 3694662fd0ed81edacd16cf55ac9760b1be2ba97
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10818989"
---
# <span data-ttu-id="746cf-103">Настройка безопасности электронной почты для AGPM</span><span class="sxs-lookup"><span data-stu-id="746cf-103">Configure E-Mail Security for AGPM</span></span>


<span data-ttu-id="746cf-104">По умолчанию уведомления по электронной почте, отправленные из-за действий в расширенном средстве управления групповыми политиками, не шифруются и отправляются через порт SMTP 25.</span><span class="sxs-lookup"><span data-stu-id="746cf-104">By default, e-mail notifications sent because of actions in Advanced Group Policy Management (AGPM) are not encrypted and are sent through SMTP port 25.</span></span> <span data-ttu-id="746cf-105">Однако вы можете настроить параметры безопасности электронной почты для РАСШИРЕНного доступа с помощью параметров реестра, чтобы указать, нужно ли использовать шифрование SSL (Secure Sockets Layer) и какой порт SMTP использовать.</span><span class="sxs-lookup"><span data-stu-id="746cf-105">However, you can configure e-mail security for AGPM by using registry settings to specify whether to use Secure Sockets Layer (SSL) encryption and which SMTP port to use.</span></span>

<span data-ttu-id="746cf-106">При шифровании уведомлений с помощью РАСШИРЕНного управления правами на доступ к данным электронной почты можно улучшить защиту пользователей, которые могут раскрывать конфиденциальную информацию о безопасности вашей организации.</span><span class="sxs-lookup"><span data-stu-id="746cf-106">By encrypting AGPM e-mail notifications, you can better protect those that could reveal sensitive information about your organization’s security.</span></span> <span data-ttu-id="746cf-107">Шифрование уведомлений по электронной почте рекомендуется при ретранслируется через удаленные почтовые серверы и может потребоваться для некоторых правил соответствия требованиям.</span><span class="sxs-lookup"><span data-stu-id="746cf-107">Encrypting e-mail notifications is recommended when they are being relayed through remote mail servers, and may be required by some compliance regulations.</span></span>

<span data-ttu-id="746cf-108">**Внимание!**  Неправильное редактирование реестра может серьезно повредить систему.</span><span class="sxs-lookup"><span data-stu-id="746cf-108">**Caution** Incorrectly editing the registry may severely damage your system.</span></span> <span data-ttu-id="746cf-109">Прежде чем вносить изменения в реестр, необходимо создать резервную копию всех важных данных на компьютере.</span><span class="sxs-lookup"><span data-stu-id="746cf-109">Before making changes to the registry, you should back up any valued data on the computer.</span></span>

 

<span data-ttu-id="746cf-110">Для выполнения описанных ниже действий необходимо иметь учетную запись пользователя с ролью администратора (полного доступа), учетная запись пользователя утверждающего, который создал объект групповой политики (GPO) или учетную запись пользователя с необходимыми разрешениями для управления ГРУППОВыми политиками.</span><span class="sxs-lookup"><span data-stu-id="746cf-110">A user account that has the AGPM Administrator (Full Control) role, the user account of the Approver who created the Group Policy Object (GPO) used in these procedures, or a user account that has the necessary permissions in AGPM is required to complete these procedures.</span></span> <span data-ttu-id="746cf-111">Ознакомьтесь с подробными сведениями в разделе "Дополнительные сведения".</span><span class="sxs-lookup"><span data-stu-id="746cf-111">Review the details in "Additional considerations" in this topic.</span></span>

**<span data-ttu-id="746cf-112">Настройка безопасности электронной почты для РАСШИРЕНного доступа с помощью настроек групповой политики</span><span class="sxs-lookup"><span data-stu-id="746cf-112">To configure e-mail security for AGPM by using Group Policy preferences</span></span>**

1.  <span data-ttu-id="746cf-113">В дереве **консоли управления групповыми политиками** измените объект групповой политики, который применяется ко всем серверам с расширенным доступом, для которых вы хотите настроить безопасность электронной почты.</span><span class="sxs-lookup"><span data-stu-id="746cf-113">In the **Group Policy Management Console** tree, edit a GPO that is applied to all AGPM Servers for which you want to configure e-mail security.</span></span> <span data-ttu-id="746cf-114">(Дополнительные сведения можно найти [в разделе изменение объекта групповой политики](editing-a-gpo-agpm30ops.md).)</span><span class="sxs-lookup"><span data-stu-id="746cf-114">(For more information, see [Editing a GPO](editing-a-gpo-agpm30ops.md).)</span></span>

2.  <span data-ttu-id="746cf-115">В окне **редактора управления групповыми политиками** разверните раздел **Конфигурация компьютера**, **Параметры**, **Параметры Windows**и папки **реестра** .</span><span class="sxs-lookup"><span data-stu-id="746cf-115">In the **Group Policy Management Editor** window, expand the **Computer Configuration**, **Preferences**, **Windows Settings**, and **Registry** folders.</span></span>

3.  <span data-ttu-id="746cf-116">В дереве консоли щелкните правой кнопкой мыши **раздел реестр**, выберите **создать**, щелкните **элемент коллекции**и введите **Параметры Безопасность электронной почты для расширенного управления безопасностью**.</span><span class="sxs-lookup"><span data-stu-id="746cf-116">In the console tree, right-click **Registry**, point to **New**, click **Collection Item**, and type **AGPM e-mail security**.</span></span>

4.  <span data-ttu-id="746cf-117">Создание элемента предпочтения реестра для включения шифрования:</span><span class="sxs-lookup"><span data-stu-id="746cf-117">Create a Registry preference item to turn on encryption:</span></span>

    1.  <span data-ttu-id="746cf-118">В дереве консоли щелкните правой кнопкой мыши пункт **Безопасность электронной почты**, выберите команду **создать**, а затем — пункт **элемент реестра**.</span><span class="sxs-lookup"><span data-stu-id="746cf-118">In the console tree, right-click **AGPM e-mail security**, point to **New**, and then click **Registry Item**.</span></span>

    2.  <span data-ttu-id="746cf-119">В диалоговом окне **Создание свойств в реестре** выберите действие " **Обновить** ".</span><span class="sxs-lookup"><span data-stu-id="746cf-119">In the **New Registry Properties** dialog box, select the **Update** action.</span></span>

    3.  <span data-ttu-id="746cf-120">В качестве **куста**выберите раздел **hKey \ _LOCAL \ _MACHINE**.</span><span class="sxs-lookup"><span data-stu-id="746cf-120">For **Hive**, select **HKEY\_LOCAL\_MACHINE**.</span></span>

    4.  <span data-ttu-id="746cf-121">В качестве **ключевого пути**введите **SOFTWARE\\Microsoft\\AGPM**.</span><span class="sxs-lookup"><span data-stu-id="746cf-121">For **Key Path**, type **SOFTWARE\\Microsoft\\AGPM**.</span></span>

    5.  <span data-ttu-id="746cf-122">В качестве **значения value (имя**) введите **EncryptSmtp**.</span><span class="sxs-lookup"><span data-stu-id="746cf-122">For **Value name**, type **EncryptSmtp**.</span></span>

    6.  <span data-ttu-id="746cf-123">В качестве **типа значения**выберите **reg \ _DWORD**.</span><span class="sxs-lookup"><span data-stu-id="746cf-123">For **Value type**, select **REG\_DWORD**.</span></span>

    7.  <span data-ttu-id="746cf-124">В параметре " **базис**" выберите " **десятичные**", а для **параметра "значение**" введите " **1** ", чтобы использовать шифрование SSL, или **0** , чтобы отправить сообщение электронной почты без шифрования.</span><span class="sxs-lookup"><span data-stu-id="746cf-124">For **Base**, select **Decimal**, and for **Value data**, type **1** to use SSL encryption, or **0** to let e-mail to be sent without encryption.</span></span> <span data-ttu-id="746cf-125">По умолчанию электронная почта отправляется без шифрования.</span><span class="sxs-lookup"><span data-stu-id="746cf-125">By default, e-mail is sent without encryption.</span></span>

    8.  <span data-ttu-id="746cf-126">Нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="746cf-126">Click **OK**.</span></span>

5.  <span data-ttu-id="746cf-127">Создание элемента предпочтения реестра для указания порта SMTP:</span><span class="sxs-lookup"><span data-stu-id="746cf-127">Create a Registry preference item to specify the SMTP port:</span></span>

    1.  <span data-ttu-id="746cf-128">В дереве консоли щелкните правой кнопкой мыши пункт **Безопасность электронной почты**, выберите команду **создать**, а затем — пункт **элемент реестра**.</span><span class="sxs-lookup"><span data-stu-id="746cf-128">In the console tree, right-click **AGPM E-mail security**, point to **New**, and then click **Registry Item**.</span></span>

    2.  <span data-ttu-id="746cf-129">В диалоговом окне **Создание свойств в реестре** выберите действие " **Обновить** ".</span><span class="sxs-lookup"><span data-stu-id="746cf-129">In the **New Registry Properties** dialog box, select the **Update** action.</span></span>

    3.  <span data-ttu-id="746cf-130">В качестве **куста**выберите раздел **hKey \ _LOCAL \ _MACHINE**.</span><span class="sxs-lookup"><span data-stu-id="746cf-130">For **Hive**, select **HKEY\_LOCAL\_MACHINE**.</span></span>

    4.  <span data-ttu-id="746cf-131">В диалоговом окне " **путь к разделу** " введите **SOFTWARE\\Microsoft\\AGPM**.</span><span class="sxs-lookup"><span data-stu-id="746cf-131">For **Key Path** dialog box, type **SOFTWARE\\Microsoft\\AGPM**.</span></span>

    5.  <span data-ttu-id="746cf-132">В качестве **значения value (имя**) введите **SMTPPORT**.</span><span class="sxs-lookup"><span data-stu-id="746cf-132">For **Value name**, type **SmtpPort**.</span></span>

    6.  <span data-ttu-id="746cf-133">В качестве **типа значения**выберите **reg \ _DWORD**.</span><span class="sxs-lookup"><span data-stu-id="746cf-133">For **Value type**, select **REG\_DWORD**.</span></span>

    7.  <span data-ttu-id="746cf-134">В поле « **базовое**» выберите параметр « **десятичные**» и введите в поле « **значение**» номер порта для порта SMTP.</span><span class="sxs-lookup"><span data-stu-id="746cf-134">For **Base**, select **Decimal**, and for **Value data**, type a port number for the SMTP port.</span></span> <span data-ttu-id="746cf-135">По умолчанию порт SMTP имеет порт 25, если шифрование не включено, или порт 587, если включено шифрование SSL.</span><span class="sxs-lookup"><span data-stu-id="746cf-135">By default, the SMTP port is port 25 if encryption is not enabled or port 587 if SSL encryption is enabled.</span></span>

    8.  <span data-ttu-id="746cf-136">Нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="746cf-136">Click **OK**.</span></span>

6.  <span data-ttu-id="746cf-137">Закройте окно **редактора управления групповыми политиками** , а затем снова установите и разверните объект групповой политики.</span><span class="sxs-lookup"><span data-stu-id="746cf-137">Close the **Group Policy Management Editor** window, and then check in and deploy the GPO.</span></span> <span data-ttu-id="746cf-138">Дополнительные сведения можно найти [в разделе Развертывание объекта групповой политики](deploy-a-gpo-agpm30ops.md).</span><span class="sxs-lookup"><span data-stu-id="746cf-138">For more information, see [Deploy a GPO](deploy-a-gpo-agpm30ops.md).</span></span>

### <span data-ttu-id="746cf-139">Дополнительные рекомендации</span><span class="sxs-lookup"><span data-stu-id="746cf-139">Additional considerations</span></span>

-   <span data-ttu-id="746cf-140">Вы должны иметь возможность изменять и развертывать объект групповой политики, чтобы настроить параметры реестра с помощью настроек для групповых политик.</span><span class="sxs-lookup"><span data-stu-id="746cf-140">You must be able to edit and deploy a GPO to configure registry settings by using Group Policy Preferences.</span></span> <span data-ttu-id="746cf-141">Дополнительные сведения: [редактирование GPO](editing-a-gpo-agpm30ops.md) и [Развертывание объекта групповой политики](deploy-a-gpo-agpm30ops.md) .</span><span class="sxs-lookup"><span data-stu-id="746cf-141">See [Editing a GPO](editing-a-gpo-agpm30ops.md) and [Deploy a GPO](deploy-a-gpo-agpm30ops.md) for additional detail.</span></span>

### <span data-ttu-id="746cf-142">Дополнительные ссылки</span><span class="sxs-lookup"><span data-stu-id="746cf-142">Additional references</span></span>

-   [<span data-ttu-id="746cf-143">Настройка средства расширенного управления групповыми политиками</span><span class="sxs-lookup"><span data-stu-id="746cf-143">Configuring Advanced Group Policy Management</span></span>](configuring-advanced-group-policy-management.md)

 

 






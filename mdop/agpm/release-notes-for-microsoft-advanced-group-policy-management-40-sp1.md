---
title: Заметки о выпуске для средства расширенного управления групповыми политиками Майкрософт4.0 с пакетом обновления1 (SP1)
description: Заметки о выпуске для средства расширенного управления групповыми политиками Майкрософт4.0 с пакетом обновления1 (SP1)
author: dansimp
ms.assetid: 91835bf8-e53c-4202-986e-8d37050d1267
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: ff9ce0405df766aef9b30e67d07ceb579c4fa89f
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10818532"
---
# <span data-ttu-id="48f22-103">Заметки о выпуске для средства расширенного управления групповыми политиками Майкрософт4.0 с пакетом обновления1 (SP1)</span><span class="sxs-lookup"><span data-stu-id="48f22-103">Release Notes for Microsoft Advanced Group Policy Management 4.0 SP1</span></span>


<span data-ttu-id="48f22-104">Чтобы найти заметки о выпуске, нажмите клавиши CTRL + F.</span><span class="sxs-lookup"><span data-stu-id="48f22-104">To search these release notes, press Ctrl+F.</span></span>

<span data-ttu-id="48f22-105">Внимательно ознакомьтесь с заметками о выпуске перед установкой расширенного управления групповыми политиками Microsoft 4,0 с пакетом обновления 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="48f22-105">Read these release notes thoroughly before you install Microsoft Advanced Group Policy Management (AGPM) 4.0 SP1.</span></span> <span data-ttu-id="48f22-106">Эти заметки о выпуске содержат сведения, необходимые для успешной установки РАСШИРЕНного ключа для 4,0 SP1 и содержащие сведения, недоступные в документации по продукту.</span><span class="sxs-lookup"><span data-stu-id="48f22-106">These release notes contain information that is required to successfully install AGPM 4.0 SP1 and contain information that is not available in the product documentation.</span></span> <span data-ttu-id="48f22-107">Если существует разница между этими заметками о выпуске и другой документацией по РАСШИРЕНным данным, Последнее изменение должно считаться полномочным.</span><span class="sxs-lookup"><span data-stu-id="48f22-107">If there is a difference between these release notes and other AGPM documentation, the latest change should be considered authoritative.</span></span> <span data-ttu-id="48f22-108">Эти заметки о выпуске заменяют контент, включенный в этот продукт.</span><span class="sxs-lookup"><span data-stu-id="48f22-108">These release notes supersede the content included with this product.</span></span>

## <span data-ttu-id="48f22-109">Известные проблемы с РАСШИРЕНным препакетом 4,0</span><span class="sxs-lookup"><span data-stu-id="48f22-109">AGPM 4.0 SP1 known issues</span></span>


<span data-ttu-id="48f22-110">В этом разделе содержатся заметки о выпуске для РАСШИРЕНного на4,0 SP1.</span><span class="sxs-lookup"><span data-stu-id="48f22-110">This section contains release notes for AGPM 4.0 SP1.</span></span>

### <a href="" id="control-panel-s--uninstall--tool-may-not-work-when-you-try-to-change-agpm-server-settings"></a><span data-ttu-id="48f22-111">При попытке изменить параметры сервера расширенного управления групповыми политиками не работает средство удаления "Удалить"</span><span class="sxs-lookup"><span data-stu-id="48f22-111">Control Panel’s “Uninstall” tool may not work when you try to change AGPM Server settings</span></span>

<span data-ttu-id="48f22-112">Средство на панели управления, позволяющее удалить или изменить программу, может не работать при попытке изменить параметры сервера расширенного управления групповыми политиками.</span><span class="sxs-lookup"><span data-stu-id="48f22-112">The tool in Control Panel that lets you uninstall or change a program may not work when you try to change AGPM server settings.</span></span>

<span data-ttu-id="48f22-113">ВРЕМЕННОе решение: перед изменением параметров сервера с помощью панели управления создайте копию папки архива с РАСШИРЕНным доступом к каталогу.</span><span class="sxs-lookup"><span data-stu-id="48f22-113">WORKAROUND: Before you try to change AGPM server settings by using Control Panel, make a copy of the AGPM Archive folder.</span></span> <span data-ttu-id="48f22-114">Затем вы можете использовать Setup.exe для переустановки сервера РАСШИРЕНного использования службы и выбора нужных параметров конфигурации.</span><span class="sxs-lookup"><span data-stu-id="48f22-114">You can then use Setup.exe to reinstall the AGPM server and choose the configuration parameters that you want.</span></span>

### <span data-ttu-id="48f22-115">В отчетах не отображаются ссылки, добавленные в объект групповой политики.</span><span class="sxs-lookup"><span data-stu-id="48f22-115">Reports do not display the links that were added to a Group Policy Object</span></span>

<span data-ttu-id="48f22-116">В отчетах "Параметры РАСШИРЕНного ключа" и "разница" не отображаются ссылки, добавленные в объект групповой политики (GPO).</span><span class="sxs-lookup"><span data-stu-id="48f22-116">The AGPM settings and difference reports do not display the links that were added to a Group Policy Object (GPO).</span></span>

<span data-ttu-id="48f22-117">ВРЕМЕННОе решение: чтобы просмотреть ссылки в отчетах, выберите GPO в консоли управления групповыми политиками, а затем откройте вкладку **Параметры** в области справа.</span><span class="sxs-lookup"><span data-stu-id="48f22-117">WORKAROUND: To view the links in the reports, select the GPO in the Group Policy Management Console (GPMC), and click the **Settings** tab in the right pane.</span></span>

### <a href="" id="reports-do-not-display-all--choice-options-properties--settings"></a><span data-ttu-id="48f22-118">В отчетах отображаются не все параметры "свойства выбора"</span><span class="sxs-lookup"><span data-stu-id="48f22-118">Reports do not display all “Choice Options Properties” settings</span></span>

<span data-ttu-id="48f22-119">В отчетах "Параметры РАСШИРЕНного ключа" и "разница" отображаются не все параметры, выбранные в окне свойств параметров выбора в редакторе объектов групповой политики.</span><span class="sxs-lookup"><span data-stu-id="48f22-119">The AGPM settings and difference reports do not display all of the settings that were selected on the Choice Options Properties window in the Group Policy Object Editor.</span></span>

<span data-ttu-id="48f22-120">ВРЕМЕННОе решение: используйте GPMC для просмотра выбранных параметров свойств выбора в отчетах.</span><span class="sxs-lookup"><span data-stu-id="48f22-120">WORKAROUND: Use the GPMC to view the selected Choice Options Properties settings in the reports.</span></span>

### <span data-ttu-id="48f22-121">В некоторых браузерах в отчетах не отображаются вкладки "Показать" и "скрыть"</span><span class="sxs-lookup"><span data-stu-id="48f22-121">Reports do not display the Show and Hide tabs in certain browsers</span></span>

<span data-ttu-id="48f22-122">Вкладки Показать и скрыть, показанные в правой части параметров РАСШИРЕНного аналитического отчета и в отчетах о различиях, не отображаются при просмотре отчетов в Google Chrome или Mozilla Firefox.</span><span class="sxs-lookup"><span data-stu-id="48f22-122">The Show and Hide tabs, shown on the right side of the AGPM settings and difference reports, are not displayed when you view the reports in Google Chrome or Mozilla Firefox.</span></span>

<span data-ttu-id="48f22-123">ВРЕМЕННОе решение: Просмотр отчетов с помощью Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="48f22-123">WORKAROUND: View the reports by using Internet Explorer.</span></span>

### <span data-ttu-id="48f22-124">Параметры расширенного управления групповыми политиками и отчеты о различиях могут показывать различные данные из отчетов GPMC</span><span class="sxs-lookup"><span data-stu-id="48f22-124">AGPM settings and difference reports may show different content from GPMC reports</span></span>

<span data-ttu-id="48f22-125">В параметрах расширенного управления групповыми политиками и отчетах о различиях не отображаются те же данные, что и отчеты, которые находятся в консоли GPMC.</span><span class="sxs-lookup"><span data-stu-id="48f22-125">The AGPM settings and difference reports may not show the same content as reports in the Group Policy Management Console (GPMC).</span></span>

<span data-ttu-id="48f22-126">ВРЕМЕННОе решение: используйте GPMC для просмотра отчетов расширенного управления групповыми политиками.</span><span class="sxs-lookup"><span data-stu-id="48f22-126">WORKAROUND: Use the GPMC to view the AGPM reports.</span></span>

### <span data-ttu-id="48f22-127">Служба расширенного управления групповыми политиками не запускается, если контроллер домена не подключен к сети</span><span class="sxs-lookup"><span data-stu-id="48f22-127">AGPM Service does not start if the domain controller is not online</span></span>

<span data-ttu-id="48f22-128">Если на контроллере домена в Windows 8 установлена служба расширенного управления групповыми политиками, служба не запускается, если контроллер домена не подключен к сети.</span><span class="sxs-lookup"><span data-stu-id="48f22-128">When the AGPM Service is installed on a domain controller on Windows 8, the Service does not start if the domain controller is not online.</span></span>

<span data-ttu-id="48f22-129">ВРЕМЕННОе решение: запустите службу расширенного управления групповыми политиками вручную после того, как контроллер домена в сети.</span><span class="sxs-lookup"><span data-stu-id="48f22-129">WORKAROUND: Manually start the AGPM Service after the domain controller is online.</span></span>

### <span data-ttu-id="48f22-130">Обновление сервера с расширенным набором программного разгрузки до расширенного уровня 4,0 (SP1) блокируется при обновлении из выпуска 4,0 расширенного</span><span class="sxs-lookup"><span data-stu-id="48f22-130">Upgrade of AGPM Server to AGPM 4.0 SP1 is blocked when you upgrade from the AGPM 4.0 release plus the hotfix</span></span>

<span data-ttu-id="48f22-131">Если вы попытаетесь обновить сервер РАСШИРЕНного обновления до РАСШИРЕНного уровня для 4,0.</span><span class="sxs-lookup"><span data-stu-id="48f22-131">If you try to upgrade the AGPM server to AGPM 4.0.</span></span> <span data-ttu-id="48f22-132">Пакет обновления 1 (SP1) после установки РАСШИРЕНного ключа для 4,0 и установки исправления для РАСШИРЕНного обновления (см. статью базы знаний Майкрософт [2643502](https://go.microsoft.com/fwlink/?LinkId=254474)) обновление завершается сбоем и не может завершиться.</span><span class="sxs-lookup"><span data-stu-id="48f22-132">SP1 after installing AGPM 4.0 and then installing the AGPM hotfix (see Knowledge Base article [2643502](https://go.microsoft.com/fwlink/?LinkId=254474)), the upgrade fails and cannot be completed.</span></span>

<span data-ttu-id="48f22-133">ВРЕМЕННОе решение: удалите сервер РАСШИРЕНной версии 4,0, а затем установите РАСШИРЕНное значение: 4,0.</span><span class="sxs-lookup"><span data-stu-id="48f22-133">WORKAROUND: Uninstall the AGPM 4.0 Server and then install AGPM 4.0 SP1.</span></span>

### <span data-ttu-id="48f22-134">В отчетах не отображаются ссылки на подразделение</span><span class="sxs-lookup"><span data-stu-id="48f22-134">Reports do not display organizational unit links</span></span>

<span data-ttu-id="48f22-135">Если вы привязать недоступный объект групповой политики к организационному подразделению, а затем управлять этим объектом групповой политики с помощью расширенного управления групповыми политиками, в отчетах параметров и отличий не отображаются ссылки на подразделение.</span><span class="sxs-lookup"><span data-stu-id="48f22-135">If you link an uncontrolled GPO to an organizational unit and then control that GPO using AGPM, the AGPM settings and difference reports do not display the organizational unit links.</span></span>

<span data-ttu-id="48f22-136">ВРЕМЕННОе решение: на вкладке **управляемые** **Параметры узла изменения параметров** щелкните правой кнопкой мыши GPO и выберите пункт **Параметры** , а затем — **ссылки GPO** для просмотра ссылок Организации.</span><span class="sxs-lookup"><span data-stu-id="48f22-136">WORKAROUND: From the **Controlled** tab of the **Change Settings** node, right-click the GPO and click **Settings** and then click **GPO Links** to view the organizational links.</span></span> <span data-ttu-id="48f22-137">Кроме того, вы можете использовать GPMC для просмотра ссылок на объект групповой политики на вкладке **область** .</span><span class="sxs-lookup"><span data-stu-id="48f22-137">Alternatively, you can use the GPMC to view the links to a GPO from the **Scope** tab.</span></span>

## <span data-ttu-id="48f22-138">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="48f22-138">Related topics</span></span>


[<span data-ttu-id="48f22-139">Расширенное управление групповыми политиками (AGPM)</span><span class="sxs-lookup"><span data-stu-id="48f22-139">Advanced Group Policy Management</span></span>](index.md)

[<span data-ttu-id="48f22-140">Новые возможности в AGPM 4.0 с пакетом обновления 1 (SP1)</span><span class="sxs-lookup"><span data-stu-id="48f22-140">What's New in AGPM 4.0 SP1</span></span>](whats-new-in-agpm-40-sp1.md)

 

 






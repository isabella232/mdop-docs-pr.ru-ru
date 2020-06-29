---
title: Заметки о выпуске для средства расширенного управления групповыми политиками Майкрософт4.0 с пакетом обновления3 (SP3)
description: Заметки о выпуске для средства расширенного управления групповыми политиками Майкрософт4.0 с пакетом обновления3 (SP3)
author: dansimp
ms.assetid: 955d7674-a8d9-4fc5-b18a-5a1639e38014
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 09/27/2016
ms.openlocfilehash: 6e0da04d67b3d29135071e0bc82b8e01789e4e81
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10818522"
---
# <span data-ttu-id="95cae-103">Заметки о выпуске для средства расширенного управления групповыми политиками Майкрософт4.0 с пакетом обновления3 (SP3)</span><span class="sxs-lookup"><span data-stu-id="95cae-103">Release Notes for Microsoft Advanced Group Policy Management 4.0 SP3</span></span>


<span data-ttu-id="95cae-104">Чтобы найти заметки о выпуске, нажмите клавиши CTRL + F.</span><span class="sxs-lookup"><span data-stu-id="95cae-104">To search these release notes, press Ctrl+F.</span></span>

<span data-ttu-id="95cae-105">Внимательно прочитайте эти заметки о выпуске, прежде чем устанавливать службу расширенного управления групповыми политиками (Pack3) 4.0 Service Management (SP3).</span><span class="sxs-lookup"><span data-stu-id="95cae-105">Read these release notes thoroughly before you install Microsoft Advanced Group Policy Management (AGPM)4.0 Service Pack3 (SP3).</span></span> <span data-ttu-id="95cae-106">Эти заметки о выпуске содержат сведения, необходимые для успешной установки РАСШИРЕНного доступа к данным с пакетом обновления (SP3) и содержащие сведения, недоступные в документации по продукту.</span><span class="sxs-lookup"><span data-stu-id="95cae-106">These release notes contain information that is required to successfully install AGPM4.0 SP3 and contain information that is not available in the product documentation.</span></span> <span data-ttu-id="95cae-107">Если существует разница между этими заметками о выпуске и другой документацией по РАСШИРЕНным анализом, рассматривайте Последнее изменение в полномочном виде.</span><span class="sxs-lookup"><span data-stu-id="95cae-107">If there is a difference between these release notes and other AGPM documentation, consider the latest change authoritative.</span></span> <span data-ttu-id="95cae-108">Эти заметки о выпуске заменяют контент, включенный в этот продукт.</span><span class="sxs-lookup"><span data-stu-id="95cae-108">These release notes supersede the content included with this product.</span></span>

## <span data-ttu-id="95cae-109">Известные проблемы с РАСШИРЕНным управлением ПАКЕТами</span><span class="sxs-lookup"><span data-stu-id="95cae-109">AGPM4.0 SP3 known issues</span></span>


<span data-ttu-id="95cae-110">В этом разделе описаны известные проблемы, возникающие при работе с РАСШИРЕНным поиском, 4,0 SP3.</span><span class="sxs-lookup"><span data-stu-id="95cae-110">This section describes the known issues for AGPM 4.0 SP3.</span></span>

### <span data-ttu-id="95cae-111">Не удается установить РАСШИРЕНную версию Office в Windows 10</span><span class="sxs-lookup"><span data-stu-id="95cae-111">AGPM installation fails in Windows 10</span></span>

<span data-ttu-id="95cae-112">Функция "РАСШИРЕНная функциональность" обеспечивает возможность активации Windows Communication Foundation (WCF), не поддерживающей HTTP, во время установки.</span><span class="sxs-lookup"><span data-stu-id="95cae-112">AGPM internally enables the Windows Communication Foundation (WCF)-NonHTTP-Activation feature during installation.</span></span> <span data-ttu-id="95cae-113">В Windows 10 в WCF включены требования для перезапуска Windows после включения функции активации WCF по протоколу HTTP.</span><span class="sxs-lookup"><span data-stu-id="95cae-113">In Windows 10, WCF now includes a requirement to restart Windows after enabling the WCF NonHTTP-Activation feature.</span></span> <span data-ttu-id="95cae-114">Однако текущий код установщика расширенного управления групповыми аналитиками не обрабатывает эти требования и перестает отвечать на запросы, пока служба не будет активирована.</span><span class="sxs-lookup"><span data-stu-id="95cae-114">However, the current AGPM installer code does not handle this restart requirement and stops responding while it waits for the service to be activated.</span></span>

<span data-ttu-id="95cae-115">**Временное решение:** Перед запуском установщика РАСШИРЕНного ключа установите флажок WCF не для активации HTTP, а затем перезапустите Windows.</span><span class="sxs-lookup"><span data-stu-id="95cae-115">**Workaround:** Before you run the AGPM installer, enable the WCF Non-HTTP Activation feature and then restart Windows.</span></span>

### <a href="" id="control-panel-s--uninstall--tool-may-not-work-when-you-try-to-change-agpm-server-settings"></a><span data-ttu-id="95cae-116">При попытке изменить параметры сервера расширенного управления групповыми политиками не работает средство удаления "Удалить"</span><span class="sxs-lookup"><span data-stu-id="95cae-116">Control Panel’s “Uninstall” tool may not work when you try to change AGPM Server settings</span></span>

<span data-ttu-id="95cae-117">Средство на панели управления, используемое для удаления или изменения программы, может не работать при попытке изменить параметры сервера расширенного управления групповыми политиками.</span><span class="sxs-lookup"><span data-stu-id="95cae-117">The tool in Control Panel that you use to uninstall or change a program may not work when you try to change AGPM Server settings.</span></span>

<span data-ttu-id="95cae-118">**Временное решение:** Перед изменением параметров сервера с помощью панели управления создайте копию папки архива с РАСШИРЕНным доступом к каталогу.</span><span class="sxs-lookup"><span data-stu-id="95cae-118">**Workaround:** Before you try to change AGPM Server settings by using Control Panel, make a copy of the AGPM Archive folder.</span></span> <span data-ttu-id="95cae-119">Затем вы можете использовать Setup.exe для переустановки сервера РАСШИРЕНного использования службы и выбора нужных параметров конфигурации.</span><span class="sxs-lookup"><span data-stu-id="95cae-119">You can then use Setup.exe to reinstall the AGPM Server and choose the configuration parameters that you want.</span></span>

### <span data-ttu-id="95cae-120">В отчетах не отображаются ссылки, добавленные в объект групповой политики.</span><span class="sxs-lookup"><span data-stu-id="95cae-120">Reports do not display the links that were added to a Group Policy Object</span></span>

<span data-ttu-id="95cae-121">В отчетах "Параметры РАСШИРЕНного ключа" и "разница" не отображаются ссылки, добавленные в объект групповой политики (GPO).</span><span class="sxs-lookup"><span data-stu-id="95cae-121">The AGPM settings and difference reports do not display the links that were added to a Group Policy Object (GPO).</span></span>

<span data-ttu-id="95cae-122">**Временное решение:** Чтобы просмотреть ссылки в отчетах, выберите GPO в консоли управления групповыми политиками, а затем откройте вкладку **Параметры** в области справа.</span><span class="sxs-lookup"><span data-stu-id="95cae-122">**Workaround:** To view the links in the reports, select the GPO in the Group Policy Management Console (GPMC), and then click the **Settings** tab in the right pane.</span></span>

### <span data-ttu-id="95cae-123">В отчетах не отображаются все параметры свойств параметров выбора</span><span class="sxs-lookup"><span data-stu-id="95cae-123">Reports do not display all Choice Options Properties settings</span></span>

<span data-ttu-id="95cae-124">В отчетах "Параметры РАСШИРЕНного ключа" и "разница" отображаются не все параметры, выбранные в окне **свойств параметров выбора** в редакторе объектов групповой политики.</span><span class="sxs-lookup"><span data-stu-id="95cae-124">The AGPM settings and difference reports do not display all of the settings that were selected in the **Choice Options Properties** window in the Group Policy Object Editor.</span></span>

<span data-ttu-id="95cae-125">**Временное решение:** Используйте GPMC для просмотра выбранных параметров **свойств выбора** в отчетах.</span><span class="sxs-lookup"><span data-stu-id="95cae-125">**Workaround:** Use the GPMC to view the selected **Choice Options Properties** settings in the reports.</span></span>

### <span data-ttu-id="95cae-126">В некоторых браузерах в отчетах не отображаются вкладки "Показать" и "скрыть"</span><span class="sxs-lookup"><span data-stu-id="95cae-126">Reports may not display the Show and Hide tabs in certain browsers</span></span>

<span data-ttu-id="95cae-127">Вкладки **Показать** и **Скрыть** в правой части параметров расширенного аналитического отчета и в отчете о различиях могут не отображаться при просмотре отчетов в Google Chrome или Mozilla Firefox.</span><span class="sxs-lookup"><span data-stu-id="95cae-127">The **Show** and **Hide** tabs, on the right side of the AGPM settings and difference reports, may not appear when you view the reports in Google Chrome or Mozilla Firefox.</span></span>

<span data-ttu-id="95cae-128">**Временное решение:** Просмотр отчетов с помощью браузера Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="95cae-128">**Workaround:** View the reports by using the Internet Explorer browser.</span></span>

### <span data-ttu-id="95cae-129">Параметры расширенного управления групповыми политиками и отчеты о различиях могут показывать различные данные из отчетов GPMC</span><span class="sxs-lookup"><span data-stu-id="95cae-129">AGPM settings and difference reports may show different content from GPMC reports</span></span>

<span data-ttu-id="95cae-130">В отчетах "Параметры РАСШИРЕНного управления и разница" могут отображаться не те же данные, что и отчеты в GPMC.</span><span class="sxs-lookup"><span data-stu-id="95cae-130">The AGPM settings and difference reports may not show the same content as reports in the GPMC.</span></span>

<span data-ttu-id="95cae-131">**Временное решение:** Используйте GPMC для просмотра отчетов расширенного управления групповыми политиками.</span><span class="sxs-lookup"><span data-stu-id="95cae-131">**Workaround:** Use the GPMC to view the AGPM reports.</span></span>

### <span data-ttu-id="95cae-132">Служба расширенного управления групповыми политиками не запускается, если контроллер домена не в сети</span><span class="sxs-lookup"><span data-stu-id="95cae-132">AGPM Service does not start if the domain controller is offline</span></span>

<span data-ttu-id="95cae-133">Если служба расширенного управления групповыми политиками установлена на контроллере домена в операционной системе Windows® 8 или более поздней версии операционной системы, служба не запускается, если контроллер домена не в сети.</span><span class="sxs-lookup"><span data-stu-id="95cae-133">When the AGPM Service is installed on a domain controller on the Windows® 8 operating systems or later operating systems, the service does not start if the domain controller is offline.</span></span>

<span data-ttu-id="95cae-134">**Временное решение:** Запустите службу расширенного управления групповыми политиками вручную после того, как контроллер домена в сети.</span><span class="sxs-lookup"><span data-stu-id="95cae-134">**Workaround:** Manually start the AGPM Service after the domain controller is online.</span></span>

### <span data-ttu-id="95cae-135">При переходе с выпуска РАСШИРЕНного набора данных версии 4.0 и Hotfix1 будет заблокировано обновление сервера с расширенным управлением разгрузкой для РАСШИРЕНного обновления</span><span class="sxs-lookup"><span data-stu-id="95cae-135">Upgrade of AGPM Server to AGPM4.0 SP2 is blocked when you upgrade from the AGPM4.0 release plus hotfix1</span></span>

<span data-ttu-id="95cae-136">Если вы попытаетесь обновить сервер РАСШИРЕНного обновления до РАСШИРЕНного уровня для 4,0.</span><span class="sxs-lookup"><span data-stu-id="95cae-136">If you try to upgrade the AGPM server to AGPM 4.0.</span></span> <span data-ttu-id="95cae-137">Пакет обновления 2 (SP2) после установки многоязыкового сервера РАСШИРЕНной версии 4,0, а затем Установка исправления для расширенного ключа с именем с помощью 4,0 РАСШИРЕНного проверки появления неверных различий в отчете HTML (см. статью базы знаний, статья [2643502](https://go.microsoft.com/fwlink/?LinkId=254474)), обновить</span><span class="sxs-lookup"><span data-stu-id="95cae-137">SP2 after installing AGPM 4.0 Server and then installing the AGPM hotfix named AGPM 4.0 reports incorrect differences in the HTML report (see Knowledge Base article [2643502](https://go.microsoft.com/fwlink/?LinkId=254474)), the upgrade fails and cannot be completed.</span></span>

<span data-ttu-id="95cae-138">**Временное решение:** Удалите сервер РАСШИРЕНной версии 4,0, а затем установите пакет обновления 2 (SP2) для 4,0.</span><span class="sxs-lookup"><span data-stu-id="95cae-138">**Workaround:** Uninstall the AGPM 4.0 Server and then install AGPM 4.0 SP2.</span></span>

### <span data-ttu-id="95cae-139">В отчетах не отображаются ссылки на подразделение</span><span class="sxs-lookup"><span data-stu-id="95cae-139">Reports do not display organizational unit links</span></span>

<span data-ttu-id="95cae-140">Если вы привязать недоступный объект групповой политики к организационному подразделению, а затем управлять этим объектом групповой политики с помощью расширенного управления групповыми политиками, в отчетах "Параметры и разница" не отображаются ссылки на подразделение.</span><span class="sxs-lookup"><span data-stu-id="95cae-140">If you link an uncontrolled GPO to an organizational unit and then control that GPO by using AGPM, the AGPM settings and difference reports do not display the organizational unit links.</span></span>

<span data-ttu-id="95cae-141">**Временное решение:** На вкладке **Управление** узлом **изменить параметры** щелкните объект групповой политики правой кнопкой мыши, выберите пункт **Параметры**, а затем — **ссылки GPO** для просмотра ссылок Организации.</span><span class="sxs-lookup"><span data-stu-id="95cae-141">**Workaround:** On the **Controlled** tab of the **Change Settings** node, right-click the GPO, click **Settings**, and then click **GPO Links** to view the organizational links.</span></span> <span data-ttu-id="95cae-142">Кроме того, вы можете использовать GPMC для просмотра ссылок на объект групповой политики на вкладке **область** .</span><span class="sxs-lookup"><span data-stu-id="95cae-142">Alternatively, you can use the GPMC to view the links to a GPO from the **Scope** tab.</span></span>

### <span data-ttu-id="95cae-143">При нажатии кнопки "назад" в диалоговом окне "изменение", "восстановление" или "удаление клиента с расширенным управлением групповыми политиками" отображается ошибка</span><span class="sxs-lookup"><span data-stu-id="95cae-143">AGPM displays an error if you click the Back button from the Change, Repair, or Remove AGPM Client dialog box</span></span>

<span data-ttu-id="95cae-144">Если вы открываете компонент " **программы и компоненты** " на панели управления, а затем выбираете пункт " **Дополнительные параметры групповой политики Майкрософт" — клиент**, функция расширенного управления версиями выводит сообщение об ошибке, если нажать кнопку **изменить** , а затем нажать кнопку **назад** в диалоговом окне **изменение, восстановление или удаление клиента с расширенным** доступом</span><span class="sxs-lookup"><span data-stu-id="95cae-144">If you browse to **Programs and Features** in Control Panel and then select **Microsoft Advanced Group Policy Management – Client**, AGPM displays an error if you click **Modify** and then click the **Back** button in the **Change, Repair, or Remove AGPM Client** dialog box.</span></span>

<span data-ttu-id="95cae-145">**Временное решение:** Нажмите кнопку **Отмена** , чтобы очистить сообщение об ошибке, а затем запустите процесс еще раз.</span><span class="sxs-lookup"><span data-stu-id="95cae-145">**Workaround:** Click **Cancel** to clear the error, and then start the process again.</span></span> <span data-ttu-id="95cae-146">Не нажимайте кнопку " **назад** " после нажатия кнопки " **изменить** ".</span><span class="sxs-lookup"><span data-stu-id="95cae-146">Do not click the **Back** button after you click **Modify** .</span></span>

### <span data-ttu-id="95cae-147">В окне журнала не отображается Примечание, когда утверждающий развертывает объект групповой политики и вводит Примечание.</span><span class="sxs-lookup"><span data-stu-id="95cae-147">Comment fails to appear in the History window when the Approver deploys a GPO and enters a comment</span></span>

<span data-ttu-id="95cae-148">Если пользователь, у которого есть роль редактора, отправляет запрос на развертывание объекта групповой политики, а пользователь, который имеет роль утверждающего, разворачивает объект GPO и вводит Примечание, этот комментарий не отображается в окне **журнала** .</span><span class="sxs-lookup"><span data-stu-id="95cae-148">If a user who has the Editor role submits a request to deploy a GPO, and the user who has the Approver role then deploys the GPO and enters a comment, the comment fails to appear in the **History** window.</span></span>

<span data-ttu-id="95cae-149">**Временное решение:** Ничего.</span><span class="sxs-lookup"><span data-stu-id="95cae-149">**Workaround:** None.</span></span>

### <span data-ttu-id="95cae-150">Добавлен механизм для переопределения поведения по умолчанию для удаления изменений разрешений GPO</span><span class="sxs-lookup"><span data-stu-id="95cae-150">Added mechanism to override AGPM default behavior of removing GPO permission changes</span></span>

<span data-ttu-id="95cae-151">По мере HF02 элемент РАСШИРЕНного доступа к групповой политики добавил раздел реестра для переопределения поведения разрешений GPO по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="95cae-151">As of HF02, AGPM has added a registry key to enable overriding the default AGPM GPO permission behavior.</span></span> <span data-ttu-id="95cae-152">Дополнительные сведения можно найти в разделе [изменения разрешений объекта групповой политики с помощью расширенного доступа](https://support.microsoft.com/kb/3174540) .</span><span class="sxs-lookup"><span data-stu-id="95cae-152">For more information, please see [Changes to Group Policy object permissions through AGPM are ignored](https://support.microsoft.com/kb/3174540)</span></span>

## <span data-ttu-id="95cae-153">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="95cae-153">Related topics</span></span>


[<span data-ttu-id="95cae-154">Расширенное управление групповыми политиками (AGPM)</span><span class="sxs-lookup"><span data-stu-id="95cae-154">Advanced Group Policy Management</span></span>](index.md)

[<span data-ttu-id="95cae-155">Новые возможности в AGPM 4.0 с пакетом обновления 3 (SP3)</span><span class="sxs-lookup"><span data-stu-id="95cae-155">What's New in AGPM 4.0 SP3</span></span>](whats-new-in-agpm-40-sp3.md)

 

 






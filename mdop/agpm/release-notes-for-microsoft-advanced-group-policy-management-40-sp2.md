---
title: Заметки о выпуске для средства расширенного управления групповыми политиками Майкрософт4.0 с пакетом обновления2 (SP2)
description: Заметки о выпуске для средства расширенного управления групповыми политиками Майкрософт4.0 с пакетом обновления2 (SP2)
author: dansimp
ms.assetid: 0593cd11-3308-4942-bf19-8a7bb9447f01
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 736eb8d41cbb72b274a2941c60b0357bbc948c9d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10820389"
---
# <span data-ttu-id="c9346-103">Заметки о выпуске для средства расширенного управления групповыми политиками Майкрософт4.0 с пакетом обновления2 (SP2)</span><span class="sxs-lookup"><span data-stu-id="c9346-103">Release Notes for Microsoft Advanced Group Policy Management 4.0 SP2</span></span>


<span data-ttu-id="c9346-104">Чтобы найти заметки о выпуске, нажмите клавиши CTRL + F.</span><span class="sxs-lookup"><span data-stu-id="c9346-104">To search these release notes, press Ctrl+F.</span></span>

<span data-ttu-id="c9346-105">Внимательно прочитайте эти заметки о выпуске, прежде чем устанавливать службу расширенного управления групповыми политиками (Pack2) 4.0 Service Management (SP2).</span><span class="sxs-lookup"><span data-stu-id="c9346-105">Read these release notes thoroughly before you install Microsoft Advanced Group Policy Management (AGPM)4.0 Service Pack2 (SP2).</span></span> <span data-ttu-id="c9346-106">Эти заметки о выпуске содержат сведения, необходимые для успешной установки многоключового пакета обновления 2 (SP2) и содержащие сведения, недоступные в документации по продукту.</span><span class="sxs-lookup"><span data-stu-id="c9346-106">These release notes contain information that is required to successfully install AGPM4.0 SP2 and contain information that is not available in the product documentation.</span></span> <span data-ttu-id="c9346-107">Если существует разница между этими заметками о выпуске и другой документацией по РАСШИРЕНным анализом, рассматривайте Последнее изменение в полномочном виде.</span><span class="sxs-lookup"><span data-stu-id="c9346-107">If there is a difference between these release notes and other AGPM documentation, consider the latest change authoritative.</span></span> <span data-ttu-id="c9346-108">Эти заметки о выпуске заменяют контент, включенный в этот продукт.</span><span class="sxs-lookup"><span data-stu-id="c9346-108">These release notes supersede the content included with this product.</span></span>

## <span data-ttu-id="c9346-109">Известные проблемы с расширенным управлением групповостью 4.0</span><span class="sxs-lookup"><span data-stu-id="c9346-109">AGPM4.0 SP2 known issues</span></span>


<span data-ttu-id="c9346-110">В этом разделе описаны известные проблемы, возникающие при работе с РАСШИРЕНным поиском, 4,0 SP2.</span><span class="sxs-lookup"><span data-stu-id="c9346-110">This section describes the known issues for AGPM 4.0 SP2.</span></span>

### <a href="" id="control-panel-s--uninstall--tool-may-not-work-when-you-try-to-change-agpm-server-settings"></a><span data-ttu-id="c9346-111">При попытке изменить параметры сервера расширенного управления групповыми политиками не работает средство удаления "Удалить"</span><span class="sxs-lookup"><span data-stu-id="c9346-111">Control Panel’s “Uninstall” tool may not work when you try to change AGPM Server settings</span></span>

<span data-ttu-id="c9346-112">Средство на панели управления, используемое для удаления или изменения программы, может не работать при попытке изменить параметры сервера расширенного управления групповыми политиками.</span><span class="sxs-lookup"><span data-stu-id="c9346-112">The tool in Control Panel that you use to uninstall or change a program may not work when you try to change AGPM Server settings.</span></span>

<span data-ttu-id="c9346-113">**Временное решение:** Перед изменением параметров сервера с помощью панели управления создайте копию папки архива с РАСШИРЕНным доступом к каталогу.</span><span class="sxs-lookup"><span data-stu-id="c9346-113">**Workaround:** Before you try to change AGPM Server settings by using Control Panel, make a copy of the AGPM Archive folder.</span></span> <span data-ttu-id="c9346-114">Затем вы можете использовать Setup.exe для переустановки сервера РАСШИРЕНного использования службы и выбора нужных параметров конфигурации.</span><span class="sxs-lookup"><span data-stu-id="c9346-114">You can then use Setup.exe to reinstall the AGPM Server and choose the configuration parameters that you want.</span></span>

### <span data-ttu-id="c9346-115">В отчетах не отображаются ссылки, добавленные в объект групповой политики.</span><span class="sxs-lookup"><span data-stu-id="c9346-115">Reports do not display the links that were added to a Group Policy Object</span></span>

<span data-ttu-id="c9346-116">В отчетах "Параметры РАСШИРЕНного ключа" и "разница" не отображаются ссылки, добавленные в объект групповой политики (GPO).</span><span class="sxs-lookup"><span data-stu-id="c9346-116">The AGPM settings and difference reports do not display the links that were added to a Group Policy Object (GPO).</span></span>

<span data-ttu-id="c9346-117">**Временное решение:** Чтобы просмотреть ссылки в отчетах, выберите GPO в консоли управления групповыми политиками, а затем откройте вкладку **Параметры** в области справа.</span><span class="sxs-lookup"><span data-stu-id="c9346-117">**Workaround:** To view the links in the reports, select the GPO in the Group Policy Management Console (GPMC), and then click the **Settings** tab in the right pane.</span></span>

### <span data-ttu-id="c9346-118">В отчетах не отображаются все параметры свойств параметров выбора</span><span class="sxs-lookup"><span data-stu-id="c9346-118">Reports do not display all Choice Options Properties settings</span></span>

<span data-ttu-id="c9346-119">В отчетах "Параметры РАСШИРЕНного ключа" и "разница" отображаются не все параметры, выбранные в окне **свойств параметров выбора** в редакторе объектов групповой политики.</span><span class="sxs-lookup"><span data-stu-id="c9346-119">The AGPM settings and difference reports do not display all of the settings that were selected in the **Choice Options Properties** window in the Group Policy Object Editor.</span></span>

<span data-ttu-id="c9346-120">**Временное решение:** Используйте GPMC для просмотра выбранных параметров **свойств выбора** в отчетах.</span><span class="sxs-lookup"><span data-stu-id="c9346-120">**Workaround:** Use the GPMC to view the selected **Choice Options Properties** settings in the reports.</span></span>

### <span data-ttu-id="c9346-121">В некоторых браузерах в отчетах не отображаются вкладки "Показать" и "скрыть"</span><span class="sxs-lookup"><span data-stu-id="c9346-121">Reports may not display the Show and Hide tabs in certain browsers</span></span>

<span data-ttu-id="c9346-122">Вкладки **Показать** и **Скрыть** в правой части параметров расширенного аналитического отчета и в отчете о различиях могут не отображаться при просмотре отчетов в Google Chrome или Mozilla Firefox.</span><span class="sxs-lookup"><span data-stu-id="c9346-122">The **Show** and **Hide** tabs, on the right side of the AGPM settings and difference reports, may not appear when you view the reports in Google Chrome or Mozilla Firefox.</span></span>

<span data-ttu-id="c9346-123">**Временное решение:** Просмотр отчетов с помощью браузера Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="c9346-123">**Workaround:** View the reports by using the Internet Explorer browser.</span></span>

### <span data-ttu-id="c9346-124">Параметры расширенного управления групповыми политиками и отчеты о различиях могут показывать различные данные из отчетов GPMC</span><span class="sxs-lookup"><span data-stu-id="c9346-124">AGPM settings and difference reports may show different content from GPMC reports</span></span>

<span data-ttu-id="c9346-125">В отчетах "Параметры РАСШИРЕНного управления и разница" могут отображаться не те же данные, что и отчеты в GPMC.</span><span class="sxs-lookup"><span data-stu-id="c9346-125">The AGPM settings and difference reports may not show the same content as reports in the GPMC.</span></span>

<span data-ttu-id="c9346-126">**Временное решение:** Используйте GPMC для просмотра отчетов расширенного управления групповыми политиками.</span><span class="sxs-lookup"><span data-stu-id="c9346-126">**Workaround:** Use the GPMC to view the AGPM reports.</span></span>

### <span data-ttu-id="c9346-127">Служба расширенного управления групповыми политиками не запускается, если контроллер домена не в сети</span><span class="sxs-lookup"><span data-stu-id="c9346-127">AGPM Service does not start if the domain controller is offline</span></span>

<span data-ttu-id="c9346-128">Если служба расширенного управления групповыми политиками установлена на контроллере домена в операционной системе Windows® 8 или более поздней версии операционной системы, служба не запускается, если контроллер домена не в сети.</span><span class="sxs-lookup"><span data-stu-id="c9346-128">When the AGPM Service is installed on a domain controller on the Windows® 8 operating systems or later operating systems, the service does not start if the domain controller is offline.</span></span>

<span data-ttu-id="c9346-129">**Временное решение:** Запустите службу расширенного управления групповыми политиками вручную после того, как контроллер домена в сети.</span><span class="sxs-lookup"><span data-stu-id="c9346-129">**Workaround:** Manually start the AGPM Service after the domain controller is online.</span></span>

### <span data-ttu-id="c9346-130">При переходе с выпуска РАСШИРЕНного набора данных версии 4.0 и Hotfix1 будет заблокировано обновление сервера с расширенным управлением разгрузкой для РАСШИРЕНного обновления</span><span class="sxs-lookup"><span data-stu-id="c9346-130">Upgrade of AGPM Server to AGPM4.0 SP2 is blocked when you upgrade from the AGPM4.0 release plus hotfix1</span></span>

<span data-ttu-id="c9346-131">Если вы попытаетесь обновить сервер РАСШИРЕНного обновления до РАСШИРЕНного уровня для 4,0.</span><span class="sxs-lookup"><span data-stu-id="c9346-131">If you try to upgrade the AGPM server to AGPM 4.0.</span></span> <span data-ttu-id="c9346-132">Пакет обновления 2 (SP2) после установки многоязыкового сервера РАСШИРЕНной версии 4,0, а затем Установка исправления для расширенного ключа с именем с помощью 4,0 РАСШИРЕНного проверки появления неверных различий в отчете HTML (см. статью базы знаний, статья [2643502](https://go.microsoft.com/fwlink/?LinkId=254474)), обновить</span><span class="sxs-lookup"><span data-stu-id="c9346-132">SP2 after installing AGPM 4.0 Server and then installing the AGPM hotfix named AGPM 4.0 reports incorrect differences in the HTML report (see Knowledge Base article [2643502](https://go.microsoft.com/fwlink/?LinkId=254474)), the upgrade fails and cannot be completed.</span></span>

<span data-ttu-id="c9346-133">**Временное решение:** Удалите сервер РАСШИРЕНной версии 4,0, а затем установите пакет обновления 2 (SP2) для 4,0.</span><span class="sxs-lookup"><span data-stu-id="c9346-133">**Workaround:** Uninstall the AGPM 4.0 Server and then install AGPM 4.0 SP2.</span></span>

### <span data-ttu-id="c9346-134">В отчетах не отображаются ссылки на подразделение</span><span class="sxs-lookup"><span data-stu-id="c9346-134">Reports do not display organizational unit links</span></span>

<span data-ttu-id="c9346-135">Если вы привязать недоступный объект групповой политики к организационному подразделению, а затем управлять этим объектом групповой политики с помощью расширенного управления групповыми политиками, в отчетах "Параметры и разница" не отображаются ссылки на подразделение.</span><span class="sxs-lookup"><span data-stu-id="c9346-135">If you link an uncontrolled GPO to an organizational unit and then control that GPO by using AGPM, the AGPM settings and difference reports do not display the organizational unit links.</span></span>

<span data-ttu-id="c9346-136">**Временное решение:** На вкладке **Управление** узлом **изменить параметры** щелкните объект групповой политики правой кнопкой мыши, выберите пункт **Параметры**, а затем — **ссылки GPO** для просмотра ссылок Организации.</span><span class="sxs-lookup"><span data-stu-id="c9346-136">**Workaround:** On the **Controlled** tab of the **Change Settings** node, right-click the GPO, click **Settings**, and then click **GPO Links** to view the organizational links.</span></span> <span data-ttu-id="c9346-137">Кроме того, вы можете использовать GPMC для просмотра ссылок на объект групповой политики на вкладке **область** .</span><span class="sxs-lookup"><span data-stu-id="c9346-137">Alternatively, you can use the GPMC to view the links to a GPO from the **Scope** tab.</span></span>

### <span data-ttu-id="c9346-138">При нажатии кнопки "назад" в диалоговом окне "изменение", "восстановление" или "удаление клиента с расширенным управлением групповыми политиками" отображается ошибка</span><span class="sxs-lookup"><span data-stu-id="c9346-138">AGPM displays an error if you click the Back button from the Change, Repair, or Remove AGPM Client dialog box</span></span>

<span data-ttu-id="c9346-139">Если вы открываете компонент " **программы и компоненты** " на панели управления, а затем выбираете пункт " **Дополнительные параметры групповой политики Майкрософт" — клиент**, функция расширенного управления версиями выводит сообщение об ошибке, если нажать кнопку **изменить** , а затем нажать кнопку **назад** в диалоговом окне **изменение, восстановление или удаление клиента с расширенным** доступом</span><span class="sxs-lookup"><span data-stu-id="c9346-139">If you browse to **Programs and Features** in Control Panel and then select **Microsoft Advanced Group Policy Management – Client**, AGPM displays an error if you click **Modify** and then click the **Back** button in the **Change, Repair, or Remove AGPM Client** dialog box.</span></span>

<span data-ttu-id="c9346-140">**Временное решение:** Нажмите кнопку **Отмена** , чтобы очистить сообщение об ошибке, а затем запустите процесс еще раз.</span><span class="sxs-lookup"><span data-stu-id="c9346-140">**Workaround:** Click **Cancel** to clear the error, and then start the process again.</span></span> <span data-ttu-id="c9346-141">Не нажимайте кнопку " **назад** " после нажатия кнопки " **изменить** ".</span><span class="sxs-lookup"><span data-stu-id="c9346-141">Do not click the **Back** button after you click **Modify** .</span></span>

### <span data-ttu-id="c9346-142">В окне журнала не отображается Примечание, когда утверждающий развертывает объект групповой политики и вводит Примечание.</span><span class="sxs-lookup"><span data-stu-id="c9346-142">Comment fails to appear in the History window when the Approver deploys a GPO and enters a comment</span></span>

<span data-ttu-id="c9346-143">Если пользователь, у которого есть роль редактора, отправляет запрос на развертывание объекта групповой политики, а пользователь, который имеет роль утверждающего, разворачивает объект GPO и вводит Примечание, этот комментарий не отображается в окне **журнала** .</span><span class="sxs-lookup"><span data-stu-id="c9346-143">If a user who has the Editor role submits a request to deploy a GPO, and the user who has the Approver role then deploys the GPO and enters a comment, the comment fails to appear in the **History** window.</span></span>

<span data-ttu-id="c9346-144">**Временное решение:** Ничего.</span><span class="sxs-lookup"><span data-stu-id="c9346-144">**Workaround:** None.</span></span>

## <span data-ttu-id="c9346-145">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="c9346-145">Related topics</span></span>


[<span data-ttu-id="c9346-146">Расширенное управление групповыми политиками (AGPM)</span><span class="sxs-lookup"><span data-stu-id="c9346-146">Advanced Group Policy Management</span></span>](index.md)

[<span data-ttu-id="c9346-147">Новые возможности в AGPM 4.0 с пакетом обновления 2 (SP2)</span><span class="sxs-lookup"><span data-stu-id="c9346-147">What's New in AGPM 4.0 SP2</span></span>](whats-new-in-agpm-40-sp2.md)

 

 






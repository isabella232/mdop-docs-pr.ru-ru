---
title: Параметры подключения к серверу AGPM
description: Параметры подключения к серверу AGPM
author: dansimp
ms.assetid: faf78e5b-2b0d-4069-9b8c-910add892200
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: d63163de0a1adf744e6d442b8073e5b32352ed67
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10813021"
---
# <span data-ttu-id="f2506-103">Параметры подключения к серверу AGPM</span><span class="sxs-lookup"><span data-stu-id="f2506-103">AGPM Server Connection Settings</span></span>


<span data-ttu-id="f2506-104">Вы можете использовать параметры шаблона для расширенного управления групповыми политиками, чтобы централизованно настроить подключения к серверу РАСШИРЕНной политики для администраторов групповых политик, которым применен объект групповой политики (GPO) с этими параметрами.</span><span class="sxs-lookup"><span data-stu-id="f2506-104">You can use Administrative template settings for Advanced Group Policy Management (AGPM) to centrally configure AGPM Server connections for Group Policy administrators to whom a Group Policy object (GPO) with these settings is applied.</span></span>

<span data-ttu-id="f2506-105">Следующие параметры доступны в разделе User Configuration\\Administrative Templates\\Windows Components\\AGPM при редактировании объекта групповой политики.</span><span class="sxs-lookup"><span data-stu-id="f2506-105">The following settings are available under User Configuration\\Administrative Templates\\Windows Components\\AGPM when editing a GPO.</span></span> <span data-ttu-id="f2506-106">Если этот путь не отображается, щелкните правой кнопкой мыши папку **Административные шаблоны**и добавьте шаблон для расширенного управления групповыми политиками (, ADMX. adm).</span><span class="sxs-lookup"><span data-stu-id="f2506-106">If this path is not visible, right-click **Administrative Templates**, and add the agpm.admx or agpm.adm template.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="f2506-107">Параметр</span><span class="sxs-lookup"><span data-stu-id="f2506-107">Setting</span></span></th>
<th align="left"><span data-ttu-id="f2506-108">Эффект</span><span class="sxs-lookup"><span data-stu-id="f2506-108">Effect</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="f2506-109">Сервер РАСШИРЕНного доменных областей (все домены)</span><span class="sxs-lookup"><span data-stu-id="f2506-109">AGPM Server (all domains)</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="f2506-110">При включенном параметре эта настройка централизованно настраивает одно соединение с использованием РАСШИРЕНных политик доменных подключений для всех доменов и отключает параметры на <strong> вкладке сервера расширенной </strong> политики для администраторов группового управления.</span><span class="sxs-lookup"><span data-stu-id="f2506-110">If enabled, this setting centrally configures one AGPM Server connection for use by all domains and disables the settings on the <strong>AGPM Server</strong> tab for Group Policy administrators.</span></span> <span data-ttu-id="f2506-111">Для нескольких серверов расширенного управления групповыми политиками настройте этот параметр с помощью сервера по умолчанию, а затем настройте <strong> Параметры сервера расширенного </strong> шаблона в административном шаблоне, чтобы переопределить этот сервер для других доменов.</span><span class="sxs-lookup"><span data-stu-id="f2506-111">For multiple AGPM Servers, configure this setting with a default server and then configure the <strong>AGPM Server</strong> setting in the Administrative template to override this server for other domains.</span></span></p>
<p><span data-ttu-id="f2506-112">Если этот параметр отключен или не настроен, каждый администратор групповой политики должен выбрать сервер, который будет отображаться для каждого домена на вкладке Сервер расширенного администрирования <strong> </strong> .</span><span class="sxs-lookup"><span data-stu-id="f2506-112">If disabled or not configured, each Group Policy administrator must select the AGPM Server to display for each domain on the <strong>AGPM Server</strong> tab in AGPM.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="f2506-113">Сервер РАСШИРЕНного нав</span><span class="sxs-lookup"><span data-stu-id="f2506-113">AGPM Server</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="f2506-114">Если этот параметр включен, эта политика используется для централизованного управления несколькими доменными серверами с определенными доменами, переопределяя <strong> параметр сервера MARS (все домены) </strong> в административном шаблоне.</span><span class="sxs-lookup"><span data-stu-id="f2506-114">If enabled, this setting centrally configures multiple domain-specific AGPM Servers, overriding the <strong>AGPM Server (all domains)</strong> setting in the Administrative template.</span></span> <span data-ttu-id="f2506-115">Если в вашей среде требуется только один сервер расширенного управления групповыми политиками, используйте <strong> </strong> в административном шаблоне только сервер (все домены) с расширенным набором доменов.</span><span class="sxs-lookup"><span data-stu-id="f2506-115">If your environment requires only a single AGPM Server, use only the <strong>AGPM Server (all domains)</strong> setting in the Administrative template.</span></span></p>
<p><span data-ttu-id="f2506-116">Если этот параметр отключен или не задан, <strong> </strong> в административном шаблоне настраивается подключение к серверу расширенного управления групповыми политиками (все домены).</span><span class="sxs-lookup"><span data-stu-id="f2506-116">If disabled or not configured, the <strong>AGPM Server (all domains)</strong> setting in the Administrative template configures the AGPM Server connection.</span></span></p></td>
</tr>
</tbody>
</table>

 

### <span data-ttu-id="f2506-117">Дополнительные ссылки</span><span class="sxs-lookup"><span data-stu-id="f2506-117">Additional references</span></span>

-   [<span data-ttu-id="f2506-118">Параметры административных шаблонов</span><span class="sxs-lookup"><span data-stu-id="f2506-118">Administrative Template Settings</span></span>](administrative-template-settings.md)

-   [<span data-ttu-id="f2506-119">Выполнение задач администратора AGPM</span><span class="sxs-lookup"><span data-stu-id="f2506-119">Performing AGPM Administrator Tasks</span></span>](performing-agpm-administrator-tasks.md)

 

 






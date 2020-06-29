---
title: Заметки о выпуске App-V 5.0
description: Заметки о выпуске App-V 5.0
author: dansimp
ms.assetid: 68a6a5a1-4b3c-4c09-b00c-9ca4237695d5
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: e49f6072d738b45afe25de24f2ee9a2d09d64a2e
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10813320"
---
# <span data-ttu-id="92e87-103">Заметки о выпуске App-V 5.0</span><span class="sxs-lookup"><span data-stu-id="92e87-103">Release Notes for App-V 5.0</span></span>


**<span data-ttu-id="92e87-104">Чтобы найти определенную ошибку в этих заметках о выпуске, нажмите клавиши CTRL + F.</span><span class="sxs-lookup"><span data-stu-id="92e87-104">To search for a specific issue in these release notes, press CTRL+F.</span></span>**

<span data-ttu-id="92e87-105">Внимательно прочтите эти заметки о выпуске перед установкой App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="92e87-105">Read these release notes thoroughly before you install App-V 5.0.</span></span>

<span data-ttu-id="92e87-106">Эти заметки о выпуске содержат сведения, необходимые для успешной установки App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="92e87-106">These release notes contain information that is required to successfully install App-V 5.0.</span></span> <span data-ttu-id="92e87-107">Заметки о выпуске также содержат сведения, недоступные в документации по продукту.</span><span class="sxs-lookup"><span data-stu-id="92e87-107">The release notes also contain information that is not available in the product documentation.</span></span> <span data-ttu-id="92e87-108">Если существует разница между этими заметками о выпуске и другой документацией приложения App-V 5,0, Последнее изменение должно считаться полномочным.</span><span class="sxs-lookup"><span data-stu-id="92e87-108">If there is a difference between these release notes and other App-V 5.0 documentation, the latest change should be considered authoritative.</span></span> <span data-ttu-id="92e87-109">Эти заметки о выпуске заменяют содержимое, которое входит в состав этого продукта.</span><span class="sxs-lookup"><span data-stu-id="92e87-109">These release notes supersede the content that is included with this product.</span></span>

## <span data-ttu-id="92e87-110">Сведения о документации по продукту</span><span class="sxs-lookup"><span data-stu-id="92e87-110">About the Product Documentation</span></span>


<span data-ttu-id="92e87-111">Сведения о документации App-V 5,0 можно найти на домашней странице App-V 5,0 на сайте Microsoft TechNet.</span><span class="sxs-lookup"><span data-stu-id="92e87-111">For information about App-V 5.0 documentation, see the App-V 5.0 home page on Microsoft TechNet.</span></span>

## <span data-ttu-id="92e87-112">Отправить отзыв</span><span class="sxs-lookup"><span data-stu-id="92e87-112">Provide Feedback</span></span>


<span data-ttu-id="92e87-113">Мы заинтересованы в ваших отзывах о приложении App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="92e87-113">We are interested in your feedback on App-V 5.0.</span></span> <span data-ttu-id="92e87-114">Вы можете отправить свой отзыв <mdopdocs@microsoft.com> .</span><span class="sxs-lookup"><span data-stu-id="92e87-114">You can send your feedback to <mdopdocs@microsoft.com>.</span></span>

<span data-ttu-id="92e87-115">**Примечание**  Этот адрес электронной почты не является каналом поддержки, но ваш отзыв поможет нам спланировать будущие изменения в документации и выпусках продуктов.</span><span class="sxs-lookup"><span data-stu-id="92e87-115">**Note** This email address is not a support channel, but your feedback will help us to plan for future changes in our documentation and product releases.</span></span>

 

<span data-ttu-id="92e87-116">Последние сведения о MDOP и дополнительных учебных материалах можно найти на странице [сведения о MDOP](https://go.microsoft.com/fwlink/p/?LinkId=236032) .</span><span class="sxs-lookup"><span data-stu-id="92e87-116">For the latest information about MDOP and additional learning resources, see the [MDOP Information Experience](https://go.microsoft.com/fwlink/p/?LinkId=236032) page.</span></span>

<span data-ttu-id="92e87-117">Дополнительные сведения о новых обновлениях и отзыве можно получить, выполнив следующие действия в [Facebook](https://go.microsoft.com/fwlink/p/?LinkId=242445) или [Twitter](https://go.microsoft.com/fwlink/p/?LinkId=242447).</span><span class="sxs-lookup"><span data-stu-id="92e87-117">For more information about new updates or to provide feedback, follow us on [Facebook](https://go.microsoft.com/fwlink/p/?LinkId=242445) or [Twitter](https://go.microsoft.com/fwlink/p/?LinkId=242447).</span></span>

## <span data-ttu-id="92e87-118">Известные проблемы с приложением-V 5,0</span><span class="sxs-lookup"><span data-stu-id="92e87-118">Known Issues with App-V 5.0</span></span>


<span data-ttu-id="92e87-119">В этом разделе содержатся заметки о выпуске известных проблем с приложением-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="92e87-119">This section contains release notes about the known issues with App-V 5.0.</span></span>

### <span data-ttu-id="92e87-120">Не удается завершить добавление пакетов при использовании командлетов PowerShell сервера</span><span class="sxs-lookup"><span data-stu-id="92e87-120">Unable to terminate adding packages when using server PowerShell cmdlets</span></span>

<span data-ttu-id="92e87-121">При добавлении пакета с помощью PowerShell отсутствует метод для выхода из добавления новых пакетов.</span><span class="sxs-lookup"><span data-stu-id="92e87-121">When you add a package using PowerShell, there is no method to exit adding new packages.</span></span>

<span data-ttu-id="92e87-122">ВРЕМЕННОе решение: чтобы прекратить Добавление пакетов, нажмите клавишу **Ввод** , чтобы добавить конечный пакет.</span><span class="sxs-lookup"><span data-stu-id="92e87-122">WORKAROUND: To stop adding packages, press **enter** after you have added the final package.</span></span>

### <a href="" id="-------------app-v-5-0-client-rejects-packages-from-servers-whose-ssl-certificate-has-been-revoked"></a> <span data-ttu-id="92e87-123">Клиент App-V 5,0 отклоняет пакеты с серверов, сертификат SSL которых был отозван</span><span class="sxs-lookup"><span data-stu-id="92e87-123">App-V 5.0 client rejects packages from servers whose SSL certificate has been revoked</span></span>

<span data-ttu-id="92e87-124">При использовании протокола HTTPS клиент App-V 5,0 будет по умолчанию отклонять пакеты с серверов, сертификат SSL которых был отозван.</span><span class="sxs-lookup"><span data-stu-id="92e87-124">When using the HTTPS protocol, the App-V 5.0 client will by default reject packages from servers whose SSL certificate has been revoked.</span></span> <span data-ttu-id="92e87-125">Это поведение можно отключить с помощью конфигурации, изменив параметр **VerifyCertificateRevocationList** .</span><span class="sxs-lookup"><span data-stu-id="92e87-125">This behavior can be turned off through configuration by modifying the **VerifyCertificateRevocationList** setting.</span></span> <span data-ttu-id="92e87-126">Применение новой конфигурации для этого параметра вступит в силу только после перезапуска службы App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="92e87-126">Applying new configuration for this setting will not take effect until the App-V 5.0 service is restarted.</span></span>

<span data-ttu-id="92e87-127">ВРЕМЕННОе решение: перезапустите службу App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="92e87-127">WORKAROUND: Restart the App-V 5.0 service.</span></span>

## <span data-ttu-id="92e87-128">Сведения о заметках об авторском праве</span><span class="sxs-lookup"><span data-stu-id="92e87-128">Release Notes Copyright Information</span></span>


<span data-ttu-id="92e87-129">Microsoft, Active Directory, ActiveX, Bing, Excel, Silverlight, SQLServer, Windows, MicrosoftIntune и WindowsPowerShell являются товарными знаками группы компании Microsoft.</span><span class="sxs-lookup"><span data-stu-id="92e87-129">Microsoft, Active Directory, ActiveX, Bing, Excel, Silverlight, SQLServer, Windows, MicrosoftIntune, and WindowsPowerShell are trademarks of the Microsoft group of companies.</span></span> <span data-ttu-id="92e87-130">Все прочие товарные знаки являются собственностью соответствующих владельцев.</span><span class="sxs-lookup"><span data-stu-id="92e87-130">All other trademarks are property of their respective owners.</span></span>








## <span data-ttu-id="92e87-131">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="92e87-131">Related topics</span></span>


[<span data-ttu-id="92e87-132">Сведения о App-V 5.0</span><span class="sxs-lookup"><span data-stu-id="92e87-132">About App-V 5.0</span></span>](about-app-v-50.md)

 

 






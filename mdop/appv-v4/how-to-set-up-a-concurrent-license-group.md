---
title: Установка группы параллельных лицензий
description: Установка группы параллельных лицензий
author: dansimp
ms.assetid: 031abcf6-d8ed-49be-bddb-91b2c695d411
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 6e3035362cd645b6488b07408d6a9444f632fc88
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10816629"
---
# <span data-ttu-id="e7ed1-103">Установка группы параллельных лицензий</span><span class="sxs-lookup"><span data-stu-id="e7ed1-103">How to Set Up a Concurrent License Group</span></span>


<span data-ttu-id="e7ed1-104">Вы можете использовать описанную ниже процедуру в консоли управления сервером Application Virtualization для настройки параллельной лицензионной группы.</span><span class="sxs-lookup"><span data-stu-id="e7ed1-104">You can use the following procedure in the Application Virtualization Server Management Console to set up a concurrent license group.</span></span> <span data-ttu-id="e7ed1-105">Если вы настроили параллельную группу лицензий, вы можете ограничить доступ к приложениям определенным количеством пользователей.</span><span class="sxs-lookup"><span data-stu-id="e7ed1-105">When you set up a concurrent license group, you can limit access to applications to a specific number of concurrent users.</span></span>

**<span data-ttu-id="e7ed1-106">Настройка параллельной группы лицензий</span><span class="sxs-lookup"><span data-stu-id="e7ed1-106">To set up a concurrent license group</span></span>**

1.  <span data-ttu-id="e7ed1-107">В левой области консоли управления сервером виртуализации приложений щелкните правой кнопкой мыши узел **лицензии приложений** .</span><span class="sxs-lookup"><span data-stu-id="e7ed1-107">In the left pane of the Application Virtualization Server Management Console, right-click the **Application Licenses** node.</span></span>

2.  <span data-ttu-id="e7ed1-108">Выберите " **Новая лицензия для параллельных**".</span><span class="sxs-lookup"><span data-stu-id="e7ed1-108">Select **New Concurrent License**.</span></span>

3.  <span data-ttu-id="e7ed1-109">Введите имя в поле **имя группы лицензирования приложений** .</span><span class="sxs-lookup"><span data-stu-id="e7ed1-109">Enter a name in the **Application License Group Name** field.</span></span>

4.  <span data-ttu-id="e7ed1-110">Введите значение (в минутах) в поле **предупреждения об истечении срока действия лицензии** .</span><span class="sxs-lookup"><span data-stu-id="e7ed1-110">Enter a value (in minutes) in the **License Expiration Warning** field.</span></span>

5.  <span data-ttu-id="e7ed1-111">Нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="e7ed1-111">Click **Next**.</span></span>

6.  <span data-ttu-id="e7ed1-112">Введите описательный текст в поле **Описание лицензии** .</span><span class="sxs-lookup"><span data-stu-id="e7ed1-112">Enter descriptive text in the **License Description** field.</span></span>

7.  <span data-ttu-id="e7ed1-113">Введите значение в поле « **количество одновременных лицензий** ».</span><span class="sxs-lookup"><span data-stu-id="e7ed1-113">Enter a value in the **Concurrent License Quantity** field.</span></span>

8.  <span data-ttu-id="e7ed1-114">Установите флажок **включено** , чтобы включить лицензию.</span><span class="sxs-lookup"><span data-stu-id="e7ed1-114">Select the **Enabled** check box to enable the license.</span></span>

9.  <span data-ttu-id="e7ed1-115">Установите флажок **Дата окончания срока** действия (если вы хотите задать дату окончания срока действия) и введите дату окончания срока действия или выберите дату с помощью служебной программы "Календарь".</span><span class="sxs-lookup"><span data-stu-id="e7ed1-115">Select the **Expiration Date** check box (if you want to set an expiration date), and enter the expiration date or use the calendar utility to select a date.</span></span>

10. <span data-ttu-id="e7ed1-116">Если необходимо связать ключ с лицензией, введите данные ключа лицензии в поле **License Key** .</span><span class="sxs-lookup"><span data-stu-id="e7ed1-116">If you need to associate a key with the license, enter the license key information in the **License Key** field.</span></span>

11. <span data-ttu-id="e7ed1-117">Нажмите кнопку **Готово**.</span><span class="sxs-lookup"><span data-stu-id="e7ed1-117">Click **Finish**.</span></span>

## <span data-ttu-id="e7ed1-118">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="e7ed1-118">Related topics</span></span>


[<span data-ttu-id="e7ed1-119">Связывание приложения с группой лицензий</span><span class="sxs-lookup"><span data-stu-id="e7ed1-119">How to Associate an Application with a License Group</span></span>](how-to-associate-an-application-with-a-license-group.md)

[<span data-ttu-id="e7ed1-120">Создание группы лицензий приложений</span><span class="sxs-lookup"><span data-stu-id="e7ed1-120">How to Create an Application License Group</span></span>](how-to-create-an-application-license-group.md)

[<span data-ttu-id="e7ed1-121">Удаление приложения из группы лицензий</span><span class="sxs-lookup"><span data-stu-id="e7ed1-121">How to Remove an Application from a License Group</span></span>](how-to-remove-an-application-from-a-license-group.md)

[<span data-ttu-id="e7ed1-122">Установка группы именованных лицензий</span><span class="sxs-lookup"><span data-stu-id="e7ed1-122">How to Set Up a Named License Group</span></span>](how-to-set-up-a-named-license-group.md)

[<span data-ttu-id="e7ed1-123">Установка группы неограниченных лицензий</span><span class="sxs-lookup"><span data-stu-id="e7ed1-123">How to Set Up an Unlimited License Group</span></span>](how-to-set-up-an-unlimited-license-group.md)

 

 






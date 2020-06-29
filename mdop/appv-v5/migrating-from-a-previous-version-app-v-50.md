---
title: Перенос из предыдущей версии
description: Перенос из предыдущей версии
author: dansimp
ms.assetid: a13cd353-b22a-48f7-af1e-5d54ede2a7e5
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: a05bbd498cdb77a1ddf694b1aab6aeb42124775b
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10813557"
---
# <span data-ttu-id="c7cc2-103">Перенос из предыдущей версии</span><span class="sxs-lookup"><span data-stu-id="c7cc2-103">Migrating from a Previous Version</span></span>


<span data-ttu-id="c7cc2-104">С помощью App-V 5,0 вы можете перенести существующую инфраструктуру App-V 4,6 на более гибкую, интегрированную и удобную для управления инфраструктурой App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="c7cc2-104">With App-V 5.0 you can migrate your existing App-V 4.6 infrastructure to the more flexible, integrated, and easier to manage App-V 5.0 infrastructure.</span></span>

<span data-ttu-id="c7cc2-105">При планировании стратегии миграции учитывайте следующие разделы:</span><span class="sxs-lookup"><span data-stu-id="c7cc2-105">Consider the following sections when you plan your migration strategy:</span></span>

<span data-ttu-id="c7cc2-106">**Примечание**  Дополнительные сведения о различиях между App-V 4,6 и App-V 5,0 приведены в **разделе различия между разделом App-v 4,6 и App-v 5,0** [о приложении app-v 5,0](about-app-v-50.md).</span><span class="sxs-lookup"><span data-stu-id="c7cc2-106">**Note** For more information about the differences between App-V 4.6 and App-V 5.0, see the **Differences between App-V 4.6 and App-V 5.0 section** of [About App-V 5.0](about-app-v-50.md).</span></span>

 

## <span data-ttu-id="c7cc2-107">Преобразование пакетов, созданных с помощью более ранней версии App-V</span><span class="sxs-lookup"><span data-stu-id="c7cc2-107">Converting packages created using a prior version of App-V</span></span>


<span data-ttu-id="c7cc2-108">Используйте служебную программу преобразователя пакетов, чтобы обновить пакеты виртуальных приложений, созданные в предыдущих версиях App-V.</span><span class="sxs-lookup"><span data-stu-id="c7cc2-108">Use the package converter utility to upgrade virtual application packages created using previous versions of App-V.</span></span> <span data-ttu-id="c7cc2-109">Преобразователь пакетов использует PowerShell для преобразования пакетов и может помочь автоматизировать процесс, если у вас много пакетов, требующих преобразования.</span><span class="sxs-lookup"><span data-stu-id="c7cc2-109">The package converter uses PowerShell to convert packages and can help automate the process if you have many packages that require conversion.</span></span>

<span data-ttu-id="c7cc2-110">**Важно!**  После преобразования существующего пакета необходимо протестировать его перед развертыванием пакета, чтобы убедиться, что процесс преобразования прошел успешно.</span><span class="sxs-lookup"><span data-stu-id="c7cc2-110">**Important** After you convert an existing package you should test the package prior to deploying the package to ensure the conversion process was successful.</span></span>

 

**<span data-ttu-id="c7cc2-111">Что нужно знать перед преобразованием существующих пакетов</span><span class="sxs-lookup"><span data-stu-id="c7cc2-111">What to know before you convert existing packages</span></span>**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="c7cc2-112">Проблема</span><span class="sxs-lookup"><span data-stu-id="c7cc2-112">Issue</span></span></th>
<th align="left"><span data-ttu-id="c7cc2-113">Обходной путь</span><span class="sxs-lookup"><span data-stu-id="c7cc2-113">Workaround</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c7cc2-114">Сценарии пакетов не преобразуются.</span><span class="sxs-lookup"><span data-stu-id="c7cc2-114">Package scripts are not converted.</span></span></p></td>
<td align="left"><p><span data-ttu-id="c7cc2-115">Протестируйте преобразованный пакет.</span><span class="sxs-lookup"><span data-stu-id="c7cc2-115">Test the converted package.</span></span> <span data-ttu-id="c7cc2-116">При необходимости преобразуйте сценарий.</span><span class="sxs-lookup"><span data-stu-id="c7cc2-116">If necessary convert the script.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="c7cc2-117">Переопределение параметров реестра пакета не преобразуется.</span><span class="sxs-lookup"><span data-stu-id="c7cc2-117">Package registry setting overrides are not converted.</span></span></p></td>
<td align="left"><p><span data-ttu-id="c7cc2-118">Протестируйте преобразованный пакет.</span><span class="sxs-lookup"><span data-stu-id="c7cc2-118">Test the converted package.</span></span> <span data-ttu-id="c7cc2-119">При необходимости повторно добавьте переопределения в реестре.</span><span class="sxs-lookup"><span data-stu-id="c7cc2-119">If necessary, re-add registry overrides.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c7cc2-120">Виртуальные пакеты с использованием DSC не связаны после преобразования.</span><span class="sxs-lookup"><span data-stu-id="c7cc2-120">Virtual packages using DSC are not linked after conversion.</span></span></p></td>
<td align="left"><p><span data-ttu-id="c7cc2-121">Свяжите пакеты с помощью групп подключений.</span><span class="sxs-lookup"><span data-stu-id="c7cc2-121">Link the packages using connection groups.</span></span> <span data-ttu-id="c7cc2-122">См <a href="managing-connection-groups.md" data-raw-source="[Managing Connection Groups](managing-connection-groups.md)"> .: Управление группами подключений </a> .</span><span class="sxs-lookup"><span data-stu-id="c7cc2-122">See <a href="managing-connection-groups.md" data-raw-source="[Managing Connection Groups](managing-connection-groups.md)">Managing Connection Groups</a>.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="c7cc2-123">Конфликты переменных среды обнаружены во время преобразования.</span><span class="sxs-lookup"><span data-stu-id="c7cc2-123">Environment variable conflicts are detected during conversion.</span></span></p></td>
<td align="left"><p><span data-ttu-id="c7cc2-124">Устраните конфликты в связанном <strong> OSD </strong> файле.</span><span class="sxs-lookup"><span data-stu-id="c7cc2-124">Resolve any conflicts in the associated <strong>.osd</strong> file.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c7cc2-125">При преобразовании обнаруживаются жестко запрограммированные пути.</span><span class="sxs-lookup"><span data-stu-id="c7cc2-125">Hard-coded paths are detected during conversion.</span></span></p></td>
<td align="left"><p><span data-ttu-id="c7cc2-126">Жестко закодированные пути очень сложны для правильного преобразования.</span><span class="sxs-lookup"><span data-stu-id="c7cc2-126">Hard-coded paths are difficult to convert correctly.</span></span> <span data-ttu-id="c7cc2-127">Преобразователь пакетов обнаружит и вернет пакеты с файлами, которые содержат жестко запрограммированные пути.</span><span class="sxs-lookup"><span data-stu-id="c7cc2-127">The package converter will detect and return packages with files that contain hard-coded paths.</span></span> <span data-ttu-id="c7cc2-128">Просмотрите файл с жестко заданным путем и определите, требуется ли для него файл.</span><span class="sxs-lookup"><span data-stu-id="c7cc2-128">View the file with the hard-coded path, and determine whether the package requires the file.</span></span> <span data-ttu-id="c7cc2-129">Если это так, рекомендуется повторно выполнить повторную последовательность пакета.</span><span class="sxs-lookup"><span data-stu-id="c7cc2-129">If so, it is recommended to re-sequence the package.</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="c7cc2-130">При преобразовании проверки пакета на наличие неудачных файлов или ярлыков.</span><span class="sxs-lookup"><span data-stu-id="c7cc2-130">When converting a package check for failing files or shortcuts.</span></span> <span data-ttu-id="c7cc2-131">Найдите элемент в пакете App-V 4,6.</span><span class="sxs-lookup"><span data-stu-id="c7cc2-131">Locate the item in App-V 4.6 package.</span></span> <span data-ttu-id="c7cc2-132">Возможно, это будет жестко запрограммированный путь.</span><span class="sxs-lookup"><span data-stu-id="c7cc2-132">It could possibly be hard-coded path.</span></span> <span data-ttu-id="c7cc2-133">Преобразуйте путь.</span><span class="sxs-lookup"><span data-stu-id="c7cc2-133">Convert the path.</span></span>

<span data-ttu-id="c7cc2-134">**Примечание**  Рекомендуется использовать секвенсор App-V 5,0 для преобразования критических приложений или приложений, которые должны использовать преимущества функций.</span><span class="sxs-lookup"><span data-stu-id="c7cc2-134">**Note** It is recommended that you use the App-V 5.0 sequencer for converting critical applications or applications that need to take advantage of features.</span></span> <span data-ttu-id="c7cc2-135">Посмотрите, [как последовательное создание нового приложения с помощью App-V 5,0](how-to-sequence-a-new-application-with-app-v-50-beta-gb18030.md).</span><span class="sxs-lookup"><span data-stu-id="c7cc2-135">See, [How to Sequence a New Application with App-V 5.0](how-to-sequence-a-new-application-with-app-v-50-beta-gb18030.md).</span></span>

<span data-ttu-id="c7cc2-136">Если преобразованный пакет не открывается после его преобразования, рекомендуется также выполнить повторную последовательное индексирование приложения с помощью секвенсора App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="c7cc2-136">If a converted package does not open after you convert it, it is also recommended that you re-sequence the application using the App-V 5.0 sequencer.</span></span>

 

[<span data-ttu-id="c7cc2-137">Преобразование пакета, созданного в предыдущей версии App-V</span><span class="sxs-lookup"><span data-stu-id="c7cc2-137">How to Convert a Package Created in a Previous Version of App-V</span></span>](how-to-convert-a-package-created-in-a-previous-version-of-app-v.md)

## <span data-ttu-id="c7cc2-138">Миграция клиентов</span><span class="sxs-lookup"><span data-stu-id="c7cc2-138">Migrating Clients</span></span>


<span data-ttu-id="c7cc2-139">В приведенной ниже таблице показан рекомендуемый метод обновления клиентов.</span><span class="sxs-lookup"><span data-stu-id="c7cc2-139">The following table displays the recommended method for upgrading clients.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="c7cc2-140">Задача</span><span class="sxs-lookup"><span data-stu-id="c7cc2-140">Task</span></span></th>
<th align="left"><span data-ttu-id="c7cc2-141">Дополнительные сведения</span><span class="sxs-lookup"><span data-stu-id="c7cc2-141">More Information</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c7cc2-142">Обновите среду до App-V 4.6 SP2</span><span class="sxs-lookup"><span data-stu-id="c7cc2-142">Upgrade your environment to App-V4.6SP2</span></span></p></td>
<td align="left"><p><a href="../appv-v4/application-virtualization-deployment-and-upgrade-considerations-copy.md" data-raw-source="[Application Virtualization Deployment and Upgrade Considerations](../appv-v4/application-virtualization-deployment-and-upgrade-considerations-copy.md)"><span data-ttu-id="c7cc2-143">Рекомендации по развертыванию и обновлению Application Virtualization </a> .</span><span class="sxs-lookup"><span data-stu-id="c7cc2-143">Application Virtualization Deployment and Upgrade Considerations</a>.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="c7cc2-144">Установите клиент App-V 5,0 с включенным параметром совместного существования.</span><span class="sxs-lookup"><span data-stu-id="c7cc2-144">Install the App-V 5.0 client with co-existence enabled.</span></span></p></td>
<td align="left"><p><a href="how-to-deploy-the-app-v-46-and-the-app-v--50-client-on-the-same-computer.md" data-raw-source="[How to Deploy the App-V 4.6 and the App-V 5.0 Client on the Same Computer](how-to-deploy-the-app-v-46-and-the-app-v--50-client-on-the-same-computer.md)"><span data-ttu-id="c7cc2-145">Развертывание приложения App-V 4,6 и клиента App-V 5,0 на том же компьютере </a> .</span><span class="sxs-lookup"><span data-stu-id="c7cc2-145">How to Deploy the App-V 4.6 and the App-V 5.0 Client on the Same Computer</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c7cc2-146">Последовательное и развертывание пакетов приложения App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="c7cc2-146">Sequence and roll out App-V 5.0 packages.</span></span> <span data-ttu-id="c7cc2-147">При необходимости можно отменить публикацию пакетов App-V 4,6.</span><span class="sxs-lookup"><span data-stu-id="c7cc2-147">As needed, unpublish App-V 4.6 packages.</span></span></p></td>
<td align="left"><p><a href="how-to-sequence-a-new-application-with-app-v-50-beta-gb18030.md" data-raw-source="[How to Sequence a New Application with App-V 5.0](how-to-sequence-a-new-application-with-app-v-50-beta-gb18030.md)"><span data-ttu-id="c7cc2-148">Последовательность создания нового приложения с помощью App-V 5,0 </a> .</span><span class="sxs-lookup"><span data-stu-id="c7cc2-148">How to Sequence a New Application with App-V 5.0</a>.</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="c7cc2-149">**Важно!**  Для использования режима сосуществования необходимо, чтобы на компьютере было запущено приложение App-V 4.6 SP3.</span><span class="sxs-lookup"><span data-stu-id="c7cc2-149">**Important** You must be running App-V4.6SP3 to use coexistence mode.</span></span> <span data-ttu-id="c7cc2-150">Кроме того, при упорядочении пакета необходимо настроить параметр управления полномочиями, который находится в **конфигурации пользователя** , в разделе **Конфигурация пользователя** .</span><span class="sxs-lookup"><span data-stu-id="c7cc2-150">Additionally, when you sequence a package, you must configure the Managing Authority setting, which is in the **User Configuration** is located in the **User Configuration** section.</span></span>

 

## <span data-ttu-id="c7cc2-151">Миграция полной инфраструктуры на сервер App-V 5,0</span><span class="sxs-lookup"><span data-stu-id="c7cc2-151">Migrating the App-V 5.0 Server Full Infrastructure</span></span>


<span data-ttu-id="c7cc2-152">Прямой метод для обновления до полной инфраструктуры App-V 5,0 не существует.</span><span class="sxs-lookup"><span data-stu-id="c7cc2-152">There is no direct method to upgrade to a full App-V 5.0 infrastructure.</span></span> <span data-ttu-id="c7cc2-153">Сведения об обновлении сервера App-V можно получить, используя сведения из следующего раздела.</span><span class="sxs-lookup"><span data-stu-id="c7cc2-153">Use the information in the following section for information about upgrading the App-V server.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="c7cc2-154">Задача</span><span class="sxs-lookup"><span data-stu-id="c7cc2-154">Task</span></span></th>
<th align="left"><span data-ttu-id="c7cc2-155">Дополнительные сведения</span><span class="sxs-lookup"><span data-stu-id="c7cc2-155">More Information</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c7cc2-156">Обновите среду до App-V 4.6 SP3.</span><span class="sxs-lookup"><span data-stu-id="c7cc2-156">Upgrade your environment to App-V4.6SP3.</span></span></p></td>
<td align="left"><p><a href="../appv-v4/application-virtualization-deployment-and-upgrade-considerations-copy.md" data-raw-source="[Application Virtualization Deployment and Upgrade Considerations](../appv-v4/application-virtualization-deployment-and-upgrade-considerations-copy.md)"><span data-ttu-id="c7cc2-157">Рекомендации по развертыванию и обновлению Application Virtualization </a> .</span><span class="sxs-lookup"><span data-stu-id="c7cc2-157">Application Virtualization Deployment and Upgrade Considerations</a>.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="c7cc2-158">Развертывание версии приложения-V 5,0 клиента.</span><span class="sxs-lookup"><span data-stu-id="c7cc2-158">Deploy App-V 5.0 version of the client.</span></span></p></td>
<td align="left"><p><a href="how-to-deploy-the-app-v-client-gb18030.md" data-raw-source="[How to Deploy the App-V Client](how-to-deploy-the-app-v-client-gb18030.md)"><span data-ttu-id="c7cc2-159">Развертывание клиента App-V </a> .</span><span class="sxs-lookup"><span data-stu-id="c7cc2-159">How to Deploy the App-V Client</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c7cc2-160">Установите приложение App-V 5,0 Server.</span><span class="sxs-lookup"><span data-stu-id="c7cc2-160">Install App-V 5.0 server.</span></span></p></td>
<td align="left"><p><a href="how-to-deploy-the-app-v-50-server-50sp3.md" data-raw-source="[How to Deploy the App-V 5.0 Server](how-to-deploy-the-app-v-50-server-50sp3.md)"><span data-ttu-id="c7cc2-161">Развертывание сервера App-V 5,0 </a> .</span><span class="sxs-lookup"><span data-stu-id="c7cc2-161">How to Deploy the App-V 5.0 Server</a>.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="c7cc2-162">Миграция существующих пакетов.</span><span class="sxs-lookup"><span data-stu-id="c7cc2-162">Migrate existing packages.</span></span></p></td>
<td align="left"><p><span data-ttu-id="c7cc2-163">Ознакомьтесь с <strong> пакетами преобразования, созданными в более ранней версии раздела App-V </strong> этой статьи.</span><span class="sxs-lookup"><span data-stu-id="c7cc2-163">See the <strong>Converting packages created using a prior version of App-V</strong> section of this article.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="c7cc2-164">Дополнительные задачи миграции</span><span class="sxs-lookup"><span data-stu-id="c7cc2-164">Additional Migration tasks</span></span>


<span data-ttu-id="c7cc2-165">Вы также можете выполнить дополнительные задачи миграции, например повторно настроить конечные точки, а также открыть пакет, созданный с помощью более ранней версии на компьютере с клиентом App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="c7cc2-165">You can also perform additional migration tasks such as reconfiguring end points as well as opening a package created using a prior version on a computer running the App-V 5.0 client.</span></span> <span data-ttu-id="c7cc2-166">Ниже приведены ссылки на дополнительные сведения о выполнении этих задач.</span><span class="sxs-lookup"><span data-stu-id="c7cc2-166">The following links provide more information about performing these tasks.</span></span>

[<span data-ttu-id="c7cc2-167">Перенос точек расширения из пакета App-V 4.6 в преобразованный пакет App-V 5.0 для всех пользователей на указанном компьютере</span><span class="sxs-lookup"><span data-stu-id="c7cc2-167">How to Migrate Extension Points From an App-V 4.6 Package to a Converted App-V 5.0 Package for All Users on a Specific Computer</span></span>](how-to-migrate-extension-points-from-an-app-v-46-package-to-a-converted-app-v-50-package-for-all-users-on-a-specific-computer.md)

[<span data-ttu-id="c7cc2-168">Перенос точек расширения из пакета App-V 4.6 в App-V 5.0 для конкретного пользователя</span><span class="sxs-lookup"><span data-stu-id="c7cc2-168">How to Migrate Extension Points From an App-V 4.6 Package to App-V 5.0 for a Specific User</span></span>](how-to-migrate-extension-points-from-an-app-v-46-package-to-app-v-50-for-a-specific-user.md)

[<span data-ttu-id="c7cc2-169">Возврат точек расширения из пакета App-V 5.0 в пакет App-V 4.6 для всех пользователей на указанном компьютере</span><span class="sxs-lookup"><span data-stu-id="c7cc2-169">How to Revert Extension Points from an App-V 5.0 Package to an App-V 4.6 Package For All Users on a Specific Computer</span></span>](how-to-revert-extension-points-from-an-app-v-50-package-to-an-app-v-46-package-for-all-users-on-a-specific-computer.md)

[<span data-ttu-id="c7cc2-170">Возврат точек расширения из пакета App-V 5.0 в пакет App-V 4.6 для конкретного пользователя</span><span class="sxs-lookup"><span data-stu-id="c7cc2-170">How to Revert Extension Points From an App-V 5.0 Package to an App-V 4.6 Package for a Specific User</span></span>](how-to-revert-extension-points-from-an-app-v-50-package-to-an-app-v-46-package-for-a-specific-user.md)







## <span data-ttu-id="c7cc2-171">Другие ресурсы для выполнения задач миграции App-V</span><span class="sxs-lookup"><span data-stu-id="c7cc2-171">Other resources for performing App-V migration tasks</span></span>


[<span data-ttu-id="c7cc2-172">Операции, связанные с администрированием и использованием App-V 5.0</span><span class="sxs-lookup"><span data-stu-id="c7cc2-172">Operations for App-V 5.0</span></span>](operations-for-app-v-50.md)

[<span data-ttu-id="c7cc2-173">Упрощенная процедура обновления сервера управления для Microsoft App-V 5,1</span><span class="sxs-lookup"><span data-stu-id="c7cc2-173">A simplified Microsoft App-V 5.1 Management Server upgrade procedure</span></span>](https://go.microsoft.com/fwlink/p/?LinkId=786330)

 

 






---
title: Сообщения журнала событий MED-V
description: Сообщения журнала событий MED-V
author: dansimp
ms.assetid: 7ba7344d-153b-4cc4-a00a-5d42aee9986b
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: b5d8dcf1cce48d6c1e29d46b4db7ac1550aa9477
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10823079"
---
# <span data-ttu-id="b5251-103">Сообщения журнала событий MED-V</span><span class="sxs-lookup"><span data-stu-id="b5251-103">MED-V Event Log Messages</span></span>


<span data-ttu-id="b5251-104">Файлы журналов для Microsoft Enterprise Virtualization (MED-V) 2,0 содержат подробные сведения о том, как развертывать MED-V и управлять ими в вашей организации, а также помогают устранять проблемы.</span><span class="sxs-lookup"><span data-stu-id="b5251-104">The log files for Microsoft Enterprise Desktop Virtualization (MED-V) 2.0 provide detailed information about how to deploy and manage MED-V in your enterprise and help verify functionality or help troubleshoot issues.</span></span>

## <span data-ttu-id="b5251-105">Коды событий</span><span class="sxs-lookup"><span data-stu-id="b5251-105">Event IDs</span></span>


<span data-ttu-id="b5251-106">Ниже приведен список кодов событий MED-V, помогающих устранить проблемы, которые могут возникнуть при развертывании и управлении MED-V.</span><span class="sxs-lookup"><span data-stu-id="b5251-106">The following are a list of MED-V event IDs to help troubleshoot issues that you might encounter when you deploy or manage MED-V.</span></span>

### <span data-ttu-id="b5251-107">Fts</span><span class="sxs-lookup"><span data-stu-id="b5251-107">Fts</span></span>

<span data-ttu-id="b5251-108">Коды событий при первом запуске программы установки.</span><span class="sxs-lookup"><span data-stu-id="b5251-108">Shows the event IDs for first time setup.</span></span>

### <span data-ttu-id="b5251-109">Событие с кодом 3066</span><span class="sxs-lookup"><span data-stu-id="b5251-109">Event ID 3066</span></span>

<span data-ttu-id="b5251-110">Не удалось запустить операцию виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="b5251-110">Start virtual machine operation failed.</span></span>

<a href="" id="description"></a>**<span data-ttu-id="b5251-111">Описание</span><span class="sxs-lookup"><span data-stu-id="b5251-111">Description</span></span>**  
<span data-ttu-id="b5251-112">Существует потенциальная проблема с виртуальным жестким диском (VHD), который вы используете для создания рабочей области MED-V.</span><span class="sxs-lookup"><span data-stu-id="b5251-112">A potential problem exists with the virtual hard disk (VHD) that you are using to create a MED-V workspace.</span></span>

<a href="" id="solution"></a>**<span data-ttu-id="b5251-113">Решение</span><span class="sxs-lookup"><span data-stu-id="b5251-113">Solution</span></span>**  
<span data-ttu-id="b5251-114">Убедитесь, что вы можете создать виртуальную машину с помощью виртуального жесткого диска для MED-V и что она может быть запущена.</span><span class="sxs-lookup"><span data-stu-id="b5251-114">Verify that you can create a virtual machine with the VHD for MED-V and that it can be started.</span></span>

### <span data-ttu-id="b5251-115">Событие с кодом 3071</span><span class="sxs-lookup"><span data-stu-id="b5251-115">Event ID 3071</span></span>

<span data-ttu-id="b5251-116">Подготовка виртуальной машины завершилась сбоем.</span><span class="sxs-lookup"><span data-stu-id="b5251-116">Virtual machine preparation failed.</span></span>

<a href="" id="description"></a>**<span data-ttu-id="b5251-117">Описание</span><span class="sxs-lookup"><span data-stu-id="b5251-117">Description</span></span>**  
<span data-ttu-id="b5251-118">Произошла ошибка при первом запуске программы установки, которая может быть вызвана многими разными проблемами.</span><span class="sxs-lookup"><span data-stu-id="b5251-118">A problem occurred with first time setup that might have been caused by many different issues.</span></span> <span data-ttu-id="b5251-119">Сюда входят проблемы с подключением к сети.</span><span class="sxs-lookup"><span data-stu-id="b5251-119">These include problems with network connectivity.</span></span>

<a href="" id="solution"></a>**<span data-ttu-id="b5251-120">Решение</span><span class="sxs-lookup"><span data-stu-id="b5251-120">Solution</span></span>**  
<span data-ttu-id="b5251-121">Перезапустите агент узла MED-V, чтобы запустить программу установки в первый раз.</span><span class="sxs-lookup"><span data-stu-id="b5251-121">Restart the MED-V Host Agent to rerun first time setup.</span></span>

### <span data-ttu-id="b5251-122">Событие с кодом 3078</span><span class="sxs-lookup"><span data-stu-id="b5251-122">Event ID 3078</span></span>

<span data-ttu-id="b5251-123">Подготовка виртуальной машины завершилась сбоем.</span><span class="sxs-lookup"><span data-stu-id="b5251-123">Virtual machine preparation failed.</span></span>

<a href="" id="description"></a>**<span data-ttu-id="b5251-124">Описание</span><span class="sxs-lookup"><span data-stu-id="b5251-124">Description</span></span>**  
<span data-ttu-id="b5251-125">Возможно, возникла проблема с VHD, который вы используете для создания рабочей области MED-V.</span><span class="sxs-lookup"><span data-stu-id="b5251-125">A potential problem exists with the VHD that you are using to create a MED-V workspace.</span></span>

<a href="" id="solution"></a>**<span data-ttu-id="b5251-126">Решение</span><span class="sxs-lookup"><span data-stu-id="b5251-126">Solution</span></span>**  
<span data-ttu-id="b5251-127">Убедитесь, что вы можете создать виртуальную машину с помощью виртуального жесткого диска для MED-V и что она может быть запущена.</span><span class="sxs-lookup"><span data-stu-id="b5251-127">Verify that you can create a virtual machine with the VHD for MED-V and that it can be started.</span></span>

### <span data-ttu-id="b5251-128">Событие с кодом 3079</span><span class="sxs-lookup"><span data-stu-id="b5251-128">Event ID 3079</span></span>

<span data-ttu-id="b5251-129">Повторное выполнение подготовки виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="b5251-129">Retrying virtual machine preparation.</span></span>

<a href="" id="description"></a>**<span data-ttu-id="b5251-130">Описание</span><span class="sxs-lookup"><span data-stu-id="b5251-130">Description</span></span>**  
<span data-ttu-id="b5251-131">MED-V пытается подготовить виртуальную машину.</span><span class="sxs-lookup"><span data-stu-id="b5251-131">MED-V is trying to prepare the virtual machine.</span></span>

<a href="" id="solution"></a>**<span data-ttu-id="b5251-132">Решение</span><span class="sxs-lookup"><span data-stu-id="b5251-132">Solution</span></span>**  
<span data-ttu-id="b5251-133">Никаких действий не требуется.</span><span class="sxs-lookup"><span data-stu-id="b5251-133">No action is required.</span></span> <span data-ttu-id="b5251-134">Начало установки первого раза.</span><span class="sxs-lookup"><span data-stu-id="b5251-134">Let first time setup finish.</span></span>

### <span data-ttu-id="b5251-135">Событие с кодом 3080</span><span class="sxs-lookup"><span data-stu-id="b5251-135">Event ID 3080</span></span>

<span data-ttu-id="b5251-136">Работа клиента была остановлена при подготовке виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="b5251-136">The client was stopped when preparing the virtual machine.</span></span>

<a href="" id="description"></a>**<span data-ttu-id="b5251-137">Описание</span><span class="sxs-lookup"><span data-stu-id="b5251-137">Description</span></span>**  
<span data-ttu-id="b5251-138">При попытке подготовить виртуальную машину была неожиданно остановлена MED-V.</span><span class="sxs-lookup"><span data-stu-id="b5251-138">MED-V stops unexpectedly when it tries to prepare the virtual machine.</span></span>

<a href="" id="solution"></a>**<span data-ttu-id="b5251-139">Решение</span><span class="sxs-lookup"><span data-stu-id="b5251-139">Solution</span></span>**  
<span data-ttu-id="b5251-140">Запуск агента хоста MED-V и пошаговое выполнение установки в первый раз</span><span class="sxs-lookup"><span data-stu-id="b5251-140">Start the MED-V Host Agent and let first time setup complete</span></span>

### <span data-ttu-id="b5251-141">Событие с кодом 3084</span><span class="sxs-lookup"><span data-stu-id="b5251-141">Event ID 3084</span></span>

<span data-ttu-id="b5251-142">Виртуальная машина является недействительной.</span><span class="sxs-lookup"><span data-stu-id="b5251-142">Virtual machine is not valid.</span></span> <span data-ttu-id="b5251-143">При первом запуске программы установки необходимо повторно запустить ее.</span><span class="sxs-lookup"><span data-stu-id="b5251-143">First time setup needs to be re-run.</span></span>

<a href="" id="description"></a>**<span data-ttu-id="b5251-144">Описание</span><span class="sxs-lookup"><span data-stu-id="b5251-144">Description</span></span>**  
<span data-ttu-id="b5251-145">Агент узла MED-V обнаружил проблему с виртуальной машиной.</span><span class="sxs-lookup"><span data-stu-id="b5251-145">The MED-V Host Agent detected a problem with the virtual machine.</span></span>

<a href="" id="solution"></a>**<span data-ttu-id="b5251-146">Решение</span><span class="sxs-lookup"><span data-stu-id="b5251-146">Solution</span></span>**  
<span data-ttu-id="b5251-147">Никаких действий не требуется.</span><span class="sxs-lookup"><span data-stu-id="b5251-147">No action is required.</span></span> <span data-ttu-id="b5251-148">Начало установки первого раза.</span><span class="sxs-lookup"><span data-stu-id="b5251-148">Let first time setup finish.</span></span>

### <span data-ttu-id="b5251-149">Событие с кодом 3099</span><span class="sxs-lookup"><span data-stu-id="b5251-149">Event ID 3099</span></span>

<span data-ttu-id="b5251-150">Не удалось вызвать запуск виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="b5251-150">Call to start virtual machine failed.</span></span>

<a href="" id="description"></a>**<span data-ttu-id="b5251-151">Описание</span><span class="sxs-lookup"><span data-stu-id="b5251-151">Description</span></span>**  
<span data-ttu-id="b5251-152">Для создания рабочей области MED-V существует потенциальная проблема с VHD, который вы используете.</span><span class="sxs-lookup"><span data-stu-id="b5251-152">A potential problem exists with the VHD you are using to create a MED-V workspace.</span></span>

<a href="" id="solution"></a>**<span data-ttu-id="b5251-153">Решение</span><span class="sxs-lookup"><span data-stu-id="b5251-153">Solution</span></span>**  
<span data-ttu-id="b5251-154">Убедитесь, что вы можете создать виртуальную машину с VHD для MED-V и ее можно открыть.</span><span class="sxs-lookup"><span data-stu-id="b5251-154">Verify that you can create a virtual machine with the VHD for MED-V and that it can be opened.</span></span>

### <span data-ttu-id="b5251-155">Управление ВМ</span><span class="sxs-lookup"><span data-stu-id="b5251-155">VM Management</span></span>

### <span data-ttu-id="b5251-156">Событие с кодом 4022</span><span class="sxs-lookup"><span data-stu-id="b5251-156">Event ID 4022</span></span>

<span data-ttu-id="b5251-157">VMManagerException Неустранимая ошибка при выдаче команды ВМ.</span><span class="sxs-lookup"><span data-stu-id="b5251-157">VMManagerException Fatal error while issuing command to VM.</span></span>

<a href="" id="description"></a>**<span data-ttu-id="b5251-158">Описание</span><span class="sxs-lookup"><span data-stu-id="b5251-158">Description</span></span>**  
<span data-ttu-id="b5251-159">Конечный пользователь попытался выйти из MED-V, выполнив выход из системы или заключив его, а параметр конфигурации VMTaskTimeout был превышен.</span><span class="sxs-lookup"><span data-stu-id="b5251-159">The end user tried to exit MED-V by logging off or by shutting down the MED-V host, and the VMTaskTimeout configuration setting was exceeded.</span></span>

<a href="" id="solution"></a>**<span data-ttu-id="b5251-160">Решение</span><span class="sxs-lookup"><span data-stu-id="b5251-160">Solution</span></span>**  
<span data-ttu-id="b5251-161">Перезапустите MED-V.</span><span class="sxs-lookup"><span data-stu-id="b5251-161">Restart MED-V.</span></span>

### <span data-ttu-id="b5251-162">Событие с кодом 4028</span><span class="sxs-lookup"><span data-stu-id="b5251-162">Event ID 4028</span></span>

<span data-ttu-id="b5251-163">Истекло время ожидания операции с виртуальной машиной.</span><span class="sxs-lookup"><span data-stu-id="b5251-163">VM Operation timed out.</span></span>

<a href="" id="description"></a>**<span data-ttu-id="b5251-164">Описание</span><span class="sxs-lookup"><span data-stu-id="b5251-164">Description</span></span>**  
<span data-ttu-id="b5251-165">Конечный пользователь попытался выйти из MED-V, выполнив выход из системы или заключив его, а параметр конфигурации VMTaskTimeout был превышен.</span><span class="sxs-lookup"><span data-stu-id="b5251-165">The end user tried to exit MED-V by logging off or by shutting down the host, and the VMTaskTimeout configuration setting was exceeded.</span></span>

<a href="" id="solution"></a>**<span data-ttu-id="b5251-166">Решение</span><span class="sxs-lookup"><span data-stu-id="b5251-166">Solution</span></span>**  
<span data-ttu-id="b5251-167">Перезапустите MED-V.</span><span class="sxs-lookup"><span data-stu-id="b5251-167">Restart MED-V.</span></span>

### <span data-ttu-id="b5251-168">Событие с кодом 4038</span><span class="sxs-lookup"><span data-stu-id="b5251-168">Event ID 4038</span></span>

<span data-ttu-id="b5251-169">VMSAL отправляет пользователю сообщение об ошибке.</span><span class="sxs-lookup"><span data-stu-id="b5251-169">Vmsal posted an error message to the user.</span></span>

<a href="" id="description"></a>**<span data-ttu-id="b5251-170">Описание</span><span class="sxs-lookup"><span data-stu-id="b5251-170">Description</span></span>**  
<span data-ttu-id="b5251-171">Для конечного пользователя отображается сообщение об ошибке, в котором говорится, что MED-V не удалось запустить виртуальное приложение.</span><span class="sxs-lookup"><span data-stu-id="b5251-171">An error message is displayed to the end user stating that MED-V could not start the virtual application.</span></span>

<a href="" id="solution"></a>**<span data-ttu-id="b5251-172">Решение</span><span class="sxs-lookup"><span data-stu-id="b5251-172">Solution</span></span>**  
<span data-ttu-id="b5251-173">Если ошибка регистрируется в строке два или более значений, остановите MED-V и подключитесь к виртуальной машине с помощью консоли Windows Virtual PC и попробуйте запустить приложение в полноэкранном режиме.</span><span class="sxs-lookup"><span data-stu-id="b5251-173">If the error is logged two or more times in a row, stop MED-V and connect to the virtual machine by using Windows Virtual PC console and attempt to start the application in Full Screen.</span></span>

### <span data-ttu-id="b5251-174">Событие с кодом 4040</span><span class="sxs-lookup"><span data-stu-id="b5251-174">Event ID 4040</span></span>

<span data-ttu-id="b5251-175">Повторное использование дополнений, так как TerminalServices не инициализирован в гостевой системе.</span><span class="sxs-lookup"><span data-stu-id="b5251-175">Recycling Additions because TerminalServices is not initialized in the guest.</span></span>

<a href="" id="description"></a>**<span data-ttu-id="b5251-176">Описание</span><span class="sxs-lookup"><span data-stu-id="b5251-176">Description</span></span>**  
<span data-ttu-id="b5251-177">Служба MED-V перезагрузила виртуальную машину, так как службы удаленных рабочих столов не были инициализированы на виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="b5251-177">MED-V rebooted the virtual machine because Remote Desktop Services was not initialized on the virtual machine.</span></span>

<a href="" id="solution"></a>**<span data-ttu-id="b5251-178">Решение</span><span class="sxs-lookup"><span data-stu-id="b5251-178">Solution</span></span>**  
<span data-ttu-id="b5251-179">Если ошибка регистрируется в строке два или более значений, остановите MED-V и подключитесь к виртуальной машине с помощью консоли Windows Virtual PC.</span><span class="sxs-lookup"><span data-stu-id="b5251-179">If the error is logged two or more times in a row, stop MED-V and connect to the virtual machine by using Windows Virtual PC console.</span></span>

### <span data-ttu-id="b5251-180">Событие с кодом 4042</span><span class="sxs-lookup"><span data-stu-id="b5251-180">Event ID 4042</span></span>

<span data-ttu-id="b5251-181">Не удалось выполнить повторное добавление в гостевой учетной записью.</span><span class="sxs-lookup"><span data-stu-id="b5251-181">Failed to recycle additions in the guest.</span></span>

<a href="" id="description"></a>**<span data-ttu-id="b5251-182">Описание</span><span class="sxs-lookup"><span data-stu-id="b5251-182">Description</span></span>**  
<span data-ttu-id="b5251-183">MED-V не удалось повторно запустить дополнения виртуальной машины на виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="b5251-183">MED-V failed to recycle virtual machine additions on the virtual machine.</span></span>

<a href="" id="solution"></a>**<span data-ttu-id="b5251-184">Решение</span><span class="sxs-lookup"><span data-stu-id="b5251-184">Solution</span></span>**  
<span data-ttu-id="b5251-185">Если ошибка регистрируется в строке два или более значений, остановите MED-V и подключитесь к виртуальной машине с помощью консоли Windows Virtual PC.</span><span class="sxs-lookup"><span data-stu-id="b5251-185">If the error is logged two or more times in a row, stop MED-V and connect to the virtual machine by using Windows Virtual PC console.</span></span>

### <span data-ttu-id="b5251-186">Событие с кодом 4043</span><span class="sxs-lookup"><span data-stu-id="b5251-186">Event ID 4043</span></span>

<span data-ttu-id="b5251-187">Не удалось сбросить пароль с истекшим сроком действия на виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="b5251-187">Failed to reset expired password in the virtual machine.</span></span>

<a href="" id="description"></a>**<span data-ttu-id="b5251-188">Описание</span><span class="sxs-lookup"><span data-stu-id="b5251-188">Description</span></span>**  
<span data-ttu-id="b5251-189">Конечный пользователь не сбросил пароль на виртуальной машине до истечения срока действия.</span><span class="sxs-lookup"><span data-stu-id="b5251-189">The end user did not reset the password in the virtual machine before it expired.</span></span> <span data-ttu-id="b5251-190">В результате пользователь не может получить доступ к сетевым ресурсам или сохранить работу.</span><span class="sxs-lookup"><span data-stu-id="b5251-190">As a result, the user might not be able to access network resources or save work.</span></span>

<a href="" id="solution"></a>**<span data-ttu-id="b5251-191">Решение</span><span class="sxs-lookup"><span data-stu-id="b5251-191">Solution</span></span>**  
<span data-ttu-id="b5251-192">Завершите работу гостя MED-V и перезапустите его.</span><span class="sxs-lookup"><span data-stu-id="b5251-192">Shut down the MED-V guest and restart it.</span></span>

### <span data-ttu-id="b5251-193">Перенаправление URL-адресов</span><span class="sxs-lookup"><span data-stu-id="b5251-193">URL Redirection</span></span>

### <span data-ttu-id="b5251-194">Событие с кодом 5005</span><span class="sxs-lookup"><span data-stu-id="b5251-194">Event ID 5005</span></span>

<span data-ttu-id="b5251-195">Не удается получить имя ВМ из конфигурации. не удается запустить браузер гостевой системы.</span><span class="sxs-lookup"><span data-stu-id="b5251-195">Couldn’t get VM name from configuration; can’t launch guest browser.</span></span>

<a href="" id="description"></a>**<span data-ttu-id="b5251-196">Описание</span><span class="sxs-lookup"><span data-stu-id="b5251-196">Description</span></span>**  
<span data-ttu-id="b5251-197">Перенаправление URL-адреса не удалось получить из конфигурации имя рабочей области для MED-V.</span><span class="sxs-lookup"><span data-stu-id="b5251-197">URL Redirection could not obtain the MED-V workspace name from the configuration.</span></span> <span data-ttu-id="b5251-198">Поэтому он не может информировать Virtual PC для Windows, чтобы открыть перенаправленный URL-адрес в браузере рабочей области MED-V.</span><span class="sxs-lookup"><span data-stu-id="b5251-198">As a result, it cannot inform Windows Virtual PC to open the redirected URL in the MED-V workspace browser.</span></span>

<a href="" id="solution"></a>**<span data-ttu-id="b5251-199">Решение</span><span class="sxs-lookup"><span data-stu-id="b5251-199">Solution</span></span>**  
<span data-ttu-id="b5251-200">Убедитесь, что имя рабочей области для MED-V задано и соответствует имени виртуальной машины в каталоге C:\\Users\\ &lt; *User* &gt; \\Virtual Machines.</span><span class="sxs-lookup"><span data-stu-id="b5251-200">Ensure that the MED-V workspace name is set and that it matches a virtual machine name in the C:\\Users\\&lt;*user*&gt;\\Virtual Machines directory.</span></span> <span data-ttu-id="b5251-201">Имя рабочей области для MED-V расположено по адресу HKLM\\SOFTWARE\\Microsoft\\Medv\\v2\\VM\\Name.</span><span class="sxs-lookup"><span data-stu-id="b5251-201">The MED-V workspace name is located at HKLM\\SOFTWARE\\Microsoft\\Medv\\v2\\VM\\Name.</span></span>

<span data-ttu-id="b5251-202">Например, если пользователь является "Мэтт", а имя рабочей области — "mattsworkspace", то значение HKLM\\SOFTWARE\\Microsoft\\Medv\\v2\\VM\\Name должно быть "mattsworkspace", а файл с именем C:\\Users\\Matt\\Virtual Machines\\mattsworkspace.vcmx.</span><span class="sxs-lookup"><span data-stu-id="b5251-202">For example, if the user is "Matt" and the workspace name is "mattsworkspace", the value of HKLM\\SOFTWARE\\Microsoft\\Medv\\v2\\VM\\Name should be "mattsworkspace", and there should be a file that is named C:\\Users\\Matt\\Virtual Machines\\mattsworkspace.vcmx.</span></span>

### <span data-ttu-id="b5251-203">Событие с кодом 5006</span><span class="sxs-lookup"><span data-stu-id="b5251-203">Event ID 5006</span></span>

<span data-ttu-id="b5251-204">Не удалось создать сервер канала.</span><span class="sxs-lookup"><span data-stu-id="b5251-204">Failed to create pipe server.</span></span>

<a href="" id="description"></a>**<span data-ttu-id="b5251-205">Описание</span><span class="sxs-lookup"><span data-stu-id="b5251-205">Description</span></span>**  
<span data-ttu-id="b5251-206">Службе перенаправления URL-адресов не удалось создать сервер канала для связи с Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="b5251-206">The URL Redirection service could not create the pipe server to communicate with Internet Explorer.</span></span>

<a href="" id="solution"></a>**<span data-ttu-id="b5251-207">Решение</span><span class="sxs-lookup"><span data-stu-id="b5251-207">Solution</span></span>**  
<span data-ttu-id="b5251-208">Проверьте журналы системных событий, чтобы попытаться создать файл или ресурс, путь которого начинается примерно так: "\\\\.\\pipe\\MEDVUrlRedirectionPipe\_" и заканчивается именем пользователя и доменным именем пользователя.</span><span class="sxs-lookup"><span data-stu-id="b5251-208">Check system event logs for attempts to create a file or resource whose path begins similar to the following: "\\\\.\\pipe\\MEDVUrlRedirectionPipe\_" and ends with the user’s user name and domain name.</span></span> <span data-ttu-id="b5251-209">Если это не пойдет в журнал событий, перезагрузите компьютер.</span><span class="sxs-lookup"><span data-stu-id="b5251-209">If this is not present in the event log, restart the computer.</span></span>

### <span data-ttu-id="b5251-210">Configuration Manager (гость)</span><span class="sxs-lookup"><span data-stu-id="b5251-210">ConfigMgr (Guest)</span></span>

### <span data-ttu-id="b5251-211">Событие с кодом 7001</span><span class="sxs-lookup"><span data-stu-id="b5251-211">Event ID 7001</span></span>

<span data-ttu-id="b5251-212">Данные конфигурации сети узла неправильно отформатированы.</span><span class="sxs-lookup"><span data-stu-id="b5251-212">The host network configuration data is not properly formatted.</span></span>

<a href="" id="description"></a>**<span data-ttu-id="b5251-213">Описание</span><span class="sxs-lookup"><span data-stu-id="b5251-213">Description</span></span>**  
<span data-ttu-id="b5251-214">Либо сетевая конфигурация, полученная от узла, имеет неверный формат XML-строки, либо в документ XML не удается записать сведения о сети, возвращенные из узла.</span><span class="sxs-lookup"><span data-stu-id="b5251-214">Either the network configuration received from the host is an incorrectly formatted XML string, or the network information returned from the host cannot be written to an XML document.</span></span>

<a href="" id="solution"></a>**<span data-ttu-id="b5251-215">Решение</span><span class="sxs-lookup"><span data-stu-id="b5251-215">Solution</span></span>**  
<span data-ttu-id="b5251-216">Перезагрузите узел компьютера и виртуальная машина.</span><span class="sxs-lookup"><span data-stu-id="b5251-216">Restart the host computer and the virtual machine.</span></span>

### <span data-ttu-id="b5251-217">Событие с кодом 7005</span><span class="sxs-lookup"><span data-stu-id="b5251-217">Event ID 7005</span></span>

<span data-ttu-id="b5251-218">Обнаружено изменение конфигурации сети узла, но его не удалось применить из-за того, что данные конфигурации сети узла неправильно отформатированы.</span><span class="sxs-lookup"><span data-stu-id="b5251-218">A change to the host network configuration was detected, but was not able to be applied because the host network configuration data was not properly formatted.</span></span>

<a href="" id="description"></a>**<span data-ttu-id="b5251-219">Описание</span><span class="sxs-lookup"><span data-stu-id="b5251-219">Description</span></span>**  
<span data-ttu-id="b5251-220">Изменение конфигурации сети узла было перенаправлено на виртуальную машину, но его не удалось обработать на виртуальной машине из-за ошибки.</span><span class="sxs-lookup"><span data-stu-id="b5251-220">A change to the host network configuration was communicated to the virtual machine, but could not be processed in the virtual machine because of an error.</span></span> <span data-ttu-id="b5251-221">Эта ошибка может возникать из-за неправильного формата данных или невозможности указать данные в экземпляре CCMNetworkAdapter WMI (инструментарий управления Windows).</span><span class="sxs-lookup"><span data-stu-id="b5251-221">This error could be caused by incorrectly formatted data or the inability to set the information into the Windows Management Instrumentation (WMI) CCMNetworkAdapter instance.</span></span>

<a href="" id="solution"></a>**<span data-ttu-id="b5251-222">Решение</span><span class="sxs-lookup"><span data-stu-id="b5251-222">Solution</span></span>**  
<span data-ttu-id="b5251-223">Перезапустите узел и виртуальную машину.</span><span class="sxs-lookup"><span data-stu-id="b5251-223">Restart the host and virtual machine.</span></span>

### <span data-ttu-id="b5251-224">Configuration Manager (узел)</span><span class="sxs-lookup"><span data-stu-id="b5251-224">ConfigMgr (Host)</span></span>

### <span data-ttu-id="b5251-225">Событие с кодом 8006</span><span class="sxs-lookup"><span data-stu-id="b5251-225">Event ID 8006</span></span>

<span data-ttu-id="b5251-226">Виртуальная машина не найдена.</span><span class="sxs-lookup"><span data-stu-id="b5251-226">The virtual machine cannot be found.</span></span>

<a href="" id="description"></a>**<span data-ttu-id="b5251-227">Описание</span><span class="sxs-lookup"><span data-stu-id="b5251-227">Description</span></span>**  
<span data-ttu-id="b5251-228">Windows Virtual PC 7 не может найти виртуальную машину.</span><span class="sxs-lookup"><span data-stu-id="b5251-228">Windows Virtual PC 7 cannot locate the virtual machine.</span></span> <span data-ttu-id="b5251-229">Возможно, виртуальная машина удалена, перемещена, удалена или в доступе отказано.</span><span class="sxs-lookup"><span data-stu-id="b5251-229">The virtual machine might have been deleted, moved, removed, or access was denied.</span></span>

<a href="" id="solution"></a>**<span data-ttu-id="b5251-230">Решение</span><span class="sxs-lookup"><span data-stu-id="b5251-230">Solution</span></span>**  
<span data-ttu-id="b5251-231">Переустановите виртуальную машину.</span><span class="sxs-lookup"><span data-stu-id="b5251-231">Reinstall the virtual machine.</span></span>

### <span data-ttu-id="b5251-232">Событие с кодом 8008</span><span class="sxs-lookup"><span data-stu-id="b5251-232">Event ID 8008</span></span>

<span data-ttu-id="b5251-233">Не удалось получить сведения о сетевой конфигурации рабочей станции.</span><span class="sxs-lookup"><span data-stu-id="b5251-233">The workstation's network configuration information could not be retrieved.</span></span>

<a href="" id="description"></a>**<span data-ttu-id="b5251-234">Описание</span><span class="sxs-lookup"><span data-stu-id="b5251-234">Description</span></span>**  
<span data-ttu-id="b5251-235">Сведения о конфигурации сети не удалось получить с узла MED-V, скорее всего, из-за ошибки системного вызова в .NET Framework.</span><span class="sxs-lookup"><span data-stu-id="b5251-235">Network configuration information could not be collected from the MED-V host, most likely because of a system call failure in the .NET Framework.</span></span> <span data-ttu-id="b5251-236">Эта проблема также может возникать, если сетевая информация, возвращенная из хоста MED-V, не может быть помещена в документ XML.</span><span class="sxs-lookup"><span data-stu-id="b5251-236">This failure can also occur if the network information returned from the MED-V host cannot be written to an XML document.</span></span>

<a href="" id="solution"></a>**<span data-ttu-id="b5251-237">Решение</span><span class="sxs-lookup"><span data-stu-id="b5251-237">Solution</span></span>**  
<span data-ttu-id="b5251-238">Перезагрузите рабочую станцию узла.</span><span class="sxs-lookup"><span data-stu-id="b5251-238">Restart the host workstation.</span></span>

### <span data-ttu-id="b5251-239">Событие с кодом 8010</span><span class="sxs-lookup"><span data-stu-id="b5251-239">Event ID 8010</span></span>

<span data-ttu-id="b5251-240">Не удалось настроить данные конфигурации сети на виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="b5251-240">The network configuration data could not be set in the virtual machine.</span></span>

<a href="" id="description"></a>**<span data-ttu-id="b5251-241">Описание</span><span class="sxs-lookup"><span data-stu-id="b5251-241">Description</span></span>**  
<span data-ttu-id="b5251-242">Приложение MED-V hostnetwork Address (NAT) не может быть подключено к виртуальной машине, скорее всего, из-за того, что виртуальная машина находится в поврежденном состоянии, или на компьютере не установлены или не включены дополнительные устройства для Windows.</span><span class="sxs-lookup"><span data-stu-id="b5251-242">The MED-V hostnetwork address translation (NAT) could not be communicated to the virtual machine, most likely because the virtual machine is in a bad state or the Windows Virtual PC Additions were not installed or enabled.</span></span>

<a href="" id="solution"></a>**<span data-ttu-id="b5251-243">Решение</span><span class="sxs-lookup"><span data-stu-id="b5251-243">Solution</span></span>**  
<span data-ttu-id="b5251-244">Закройте и перезапустите виртуальную машину.</span><span class="sxs-lookup"><span data-stu-id="b5251-244">Shut down and restart the virtual machine.</span></span> <span data-ttu-id="b5251-245">Кроме того, может потребоваться переустановка виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="b5251-245">In addition, you might have to reinstall the virtual machine.</span></span>

### <span data-ttu-id="b5251-246">Событие с кодом 8011</span><span class="sxs-lookup"><span data-stu-id="b5251-246">Event ID 8011</span></span>

<span data-ttu-id="b5251-247">Не удалось сбросить данные конфигурации сети на виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="b5251-247">The network configuration data could not be reset in the virtual machine.</span></span>

<a href="" id="description"></a>**<span data-ttu-id="b5251-248">Описание</span><span class="sxs-lookup"><span data-stu-id="b5251-248">Description</span></span>**  
<span data-ttu-id="b5251-249">Hostnetwork конфигурации MED-V (мост) не может быть передана виртуальной машине, скорее всего, из-за неправильного состояния виртуальной машины или недоступности дополнений Virtual PC для Windows.</span><span class="sxs-lookup"><span data-stu-id="b5251-249">The MED-V hostnetwork configuration (BRIDGED) could not be communicated to the virtual machine, most likely because the virtual machine is in a bad state or the Windows Virtual PC Additions were not installed or enabled.</span></span>

<a href="" id="solution"></a>**<span data-ttu-id="b5251-250">Решение</span><span class="sxs-lookup"><span data-stu-id="b5251-250">Solution</span></span>**  
<span data-ttu-id="b5251-251">Закройте и перезапустите виртуальную машину.</span><span class="sxs-lookup"><span data-stu-id="b5251-251">Shut down and restart the virtual machine.</span></span> <span data-ttu-id="b5251-252">Кроме того, может потребоваться переустановка виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="b5251-252">In addition, you might have to reinstall the virtual machine.</span></span>

### <span data-ttu-id="b5251-253">Перенаправление принтеров</span><span class="sxs-lookup"><span data-stu-id="b5251-253">Printer Redirection</span></span>

### <span data-ttu-id="b5251-254">Событие с кодом 9001</span><span class="sxs-lookup"><span data-stu-id="b5251-254">Event ID 9001</span></span>

<span data-ttu-id="b5251-255">Ошибка разрешения на доступ к файлу.</span><span class="sxs-lookup"><span data-stu-id="b5251-255">File Permission Error.</span></span>

<a href="" id="description"></a>**<span data-ttu-id="b5251-256">Описание</span><span class="sxs-lookup"><span data-stu-id="b5251-256">Description</span></span>**  
<span data-ttu-id="b5251-257">Конечному пользователю не разрешен доступ к папке, необходимой для открытия или создания файла принтера MED-V для чтения.</span><span class="sxs-lookup"><span data-stu-id="b5251-257">The end user is not authorized to access the folder required to open or create the MED-V printer file for reading.</span></span>

<a href="" id="solution"></a>**<span data-ttu-id="b5251-258">Решение</span><span class="sxs-lookup"><span data-stu-id="b5251-258">Solution</span></span>**  
<span data-ttu-id="b5251-259">Убедитесь в том, что путь к User\\AppData\\ доступен и у пользователя есть разрешение на чтение и запись.</span><span class="sxs-lookup"><span data-stu-id="b5251-259">Verify that the User\\AppData\\ path can be accessed and that the user has permission to read and write to it.</span></span> <span data-ttu-id="b5251-260">Например, если пользователь является "Мэтт", в нем C:\\Users\\Matt\\AppData\\ путь и все файлы должны иметь разрешения на чтение и запись.</span><span class="sxs-lookup"><span data-stu-id="b5251-260">For example, if the user is "Matt", the path C:\\Users\\Matt\\AppData\\, and all files therein should have Read and Write permissions.</span></span> <span data-ttu-id="b5251-261">И если он существует, на пути C:\\Users\\Matt\\AppData\\Local\\Microsoft\\MEDV\\v2\\ и всех файлов в нем должны быть разрешения на чтение и запись.</span><span class="sxs-lookup"><span data-stu-id="b5251-261">And if it exists, the path C:\\Users\\Matt\\AppData\\Local\\Microsoft\\MEDV\\v2\\ and all files therein should have Read and Write permissions.</span></span>

### <span data-ttu-id="b5251-262">Событие с кодом 9002</span><span class="sxs-lookup"><span data-stu-id="b5251-262">Event ID 9002</span></span>

<span data-ttu-id="b5251-263">Ошибка разрешения на доступ к файлу.</span><span class="sxs-lookup"><span data-stu-id="b5251-263">File Permission Error.</span></span>

<a href="" id="description"></a>**<span data-ttu-id="b5251-264">Описание</span><span class="sxs-lookup"><span data-stu-id="b5251-264">Description</span></span>**  
<span data-ttu-id="b5251-265">Конечному пользователю не разрешен доступ к папке, необходимой для открытия или создания файла принтера MED-V для записи.</span><span class="sxs-lookup"><span data-stu-id="b5251-265">The end user is not authorized to access the folder required to open or create the MED-V printer file for writing.</span></span>

<a href="" id="solution"></a>**<span data-ttu-id="b5251-266">Решение</span><span class="sxs-lookup"><span data-stu-id="b5251-266">Solution</span></span>**  
<span data-ttu-id="b5251-267">Убедитесь в том, что путь User\\AppData\\ доступен и что пользователь имеет разрешение на чтение и запись.</span><span class="sxs-lookup"><span data-stu-id="b5251-267">Ensure that the User\\AppData\\ path can be accessed, and that the user has permission to read and write to it.</span></span> <span data-ttu-id="b5251-268">Например, если пользователь является "Мэтт", на пути C:\\Users\\Matt\\AppData\\ и всех файлов в нем должны быть разрешения на чтение и запись.</span><span class="sxs-lookup"><span data-stu-id="b5251-268">For example, if the user is "Matt", the path C:\\Users\\Matt\\AppData\\ and all files therein should have Read and Write permissions.</span></span> <span data-ttu-id="b5251-269">И если он существует, на пути C:\\Users\\Matt\\AppData\\Local\\Microsoft\\MEDV\\v2\\ и всех файлов в нем должны быть разрешения на чтение и запись.</span><span class="sxs-lookup"><span data-stu-id="b5251-269">And if it exists, the path C:\\Users\\Matt\\AppData\\Local\\Microsoft\\MEDV\\v2\\ and all files therein should have Read and Write permissions.</span></span>

### <span data-ttu-id="b5251-270">Событие с кодом 9004</span><span class="sxs-lookup"><span data-stu-id="b5251-270">Event ID 9004</span></span>

<span data-ttu-id="b5251-271">Не удалось создать путь для хранения файлов принтера MEDV.</span><span class="sxs-lookup"><span data-stu-id="b5251-271">Could not create path for storing MEDV printer files.</span></span>

<a href="" id="description"></a>**<span data-ttu-id="b5251-272">Описание</span><span class="sxs-lookup"><span data-stu-id="b5251-272">Description</span></span>**  
<span data-ttu-id="b5251-273">Служба переадресации принтеров не может получить доступ к файлам или создавать каталоги, необходимые для хранения сведений о принтерах.</span><span class="sxs-lookup"><span data-stu-id="b5251-273">The printer redirection service could not access files or create directories required for storing the printer information.</span></span>

<a href="" id="solution"></a>**<span data-ttu-id="b5251-274">Решение</span><span class="sxs-lookup"><span data-stu-id="b5251-274">Solution</span></span>**  
<span data-ttu-id="b5251-275">Убедитесь в том, что путь к User\\AppData\\ доступен и у пользователя есть разрешение на чтение и запись.</span><span class="sxs-lookup"><span data-stu-id="b5251-275">Verify that the User\\AppData\\ path can be accessed and that the user has permission to read and write to it.</span></span> <span data-ttu-id="b5251-276">Например, если пользователь является "Мэтт", на пути C:\\Users\\Matt\\AppData\\ и всех файлов в нем должны быть разрешения на чтение и запись.</span><span class="sxs-lookup"><span data-stu-id="b5251-276">For example, if the user is "Matt", the path C:\\Users\\Matt\\AppData\\ and all files therein should have Read and Write permissions.</span></span> <span data-ttu-id="b5251-277">И если он существует, на пути C:\\Users\\Matt\\AppData\\Local\\Microsoft\\MEDV\\v2\\ и всех файлов в нем должны быть разрешения на чтение и запись.</span><span class="sxs-lookup"><span data-stu-id="b5251-277">And if it exists, the path C:\\Users\\Matt\\AppData\\Local\\Microsoft\\MEDV\\v2\\ and all files therein should have Read and Write permissions.</span></span>

### <span data-ttu-id="b5251-278">Событие с кодом 9005</span><span class="sxs-lookup"><span data-stu-id="b5251-278">Event ID 9005</span></span>

<span data-ttu-id="b5251-279">Не удается получить имя ВМ из конфигурации. не удается запустить установщик гостевой системы.</span><span class="sxs-lookup"><span data-stu-id="b5251-279">Couldn’t get VM name from configuration; cannot launch guest installer.</span></span> <span data-ttu-id="b5251-280">Не удается обновить MED-V — сеть узла не обнаружена.</span><span class="sxs-lookup"><span data-stu-id="b5251-280">Cannot update MED-V – No host network detected.</span></span>

<a href="" id="description"></a>**<span data-ttu-id="b5251-281">Описание</span><span class="sxs-lookup"><span data-stu-id="b5251-281">Description</span></span>**  
<span data-ttu-id="b5251-282">Службе переадресации принтеров не удалось получить имя рабочей области MED-V из конфигурации MED-V и не может проинформировать Virtual PC о Windows, чтобы запустить установщик на гостевой машине MED-V.</span><span class="sxs-lookup"><span data-stu-id="b5251-282">The printer redirection service was not able to obtain the MED-V workspace name from the MED-V configuration and cannot inform Windows Virtual PC to start the installer on the MED-V guest.</span></span>

<a href="" id="solution"></a>**<span data-ttu-id="b5251-283">Решение</span><span class="sxs-lookup"><span data-stu-id="b5251-283">Solution</span></span>**  
<span data-ttu-id="b5251-284">Убедитесь, что имя рабочей области для MED-V задано и соответствует имени виртуальной машины в каталоге C:\\Users\\ &lt; *User* &gt; \\Virtual Machines.</span><span class="sxs-lookup"><span data-stu-id="b5251-284">Ensure that the MED-V workspace name is set and that it matches a virtual machine name in the C:\\Users\\&lt;*user*&gt;\\Virtual Machines directory.</span></span> <span data-ttu-id="b5251-285">Имя рабочей области для MED-V расположено по адресу HKLM\\SOFTWARE\\Microsoft\\Medv\\v2\\VM\\Name.</span><span class="sxs-lookup"><span data-stu-id="b5251-285">The MED-V workspace name is located at HKLM\\SOFTWARE\\Microsoft\\Medv\\v2\\VM\\Name.</span></span>

<span data-ttu-id="b5251-286">Например, если пользователь является "Мэтт", а имя рабочей области — "mattsworkspace", значение HKLM\\SOFTWARE\\Microsoft\\Medv\\v2\\VM\\Name должно быть "mattsworkspace", а файл с именем C:\\Users\\Matt\\Virtual Machines\\mattsworkspace.vcmx.</span><span class="sxs-lookup"><span data-stu-id="b5251-286">For example, if the user is "Matt" and the workspace name is "mattsworkspace", the value of HKLM\\SOFTWARE\\Microsoft\\Medv\\v2\\VM\\Name should be "mattsworkspace" and there should be a file that is named C:\\Users\\Matt\\Virtual Machines\\mattsworkspace.vcmx.</span></span>

### <span data-ttu-id="b5251-287">Публикация приложений</span><span class="sxs-lookup"><span data-stu-id="b5251-287">Application Publishing</span></span>

### <span data-ttu-id="b5251-288">Событие с кодом 10015</span><span class="sxs-lookup"><span data-stu-id="b5251-288">Event ID 10015</span></span>

<span data-ttu-id="b5251-289">Во время процесса выверки произошла ошибка файловой системы.</span><span class="sxs-lookup"><span data-stu-id="b5251-289">A file system error occurred during the reconcile process.</span></span> <span data-ttu-id="b5251-290">Процесс выверки не будет обрабатывать имя файла, &lt; *filename* &gt; но будет продолжать обрабатывать любые другие изменения.</span><span class="sxs-lookup"><span data-stu-id="b5251-290">The reconcile process will not process the file &lt;*filename*&gt; but will continue to process any other changes.</span></span>

<a href="" id="description"></a>**<span data-ttu-id="b5251-291">Описание</span><span class="sxs-lookup"><span data-stu-id="b5251-291">Description</span></span>**  
<span data-ttu-id="b5251-292">При создании или удалении ярлыка произошла ошибка несанкционированного доступа или ввода-вывода.</span><span class="sxs-lookup"><span data-stu-id="b5251-292">An unauthorized access or I/O error occurred when a shortcut was being created or deleted.</span></span>

<a href="" id="solution"></a>**<span data-ttu-id="b5251-293">Решение</span><span class="sxs-lookup"><span data-stu-id="b5251-293">Solution</span></span>**  
<span data-ttu-id="b5251-294">Убедитесь в том, что путь к файлу доступен и что у пользователя есть разрешения на создание или удаление указанного файла.</span><span class="sxs-lookup"><span data-stu-id="b5251-294">Check that the file path can be accessed and that the user has permissions to create or delete the specified file.</span></span>

### <span data-ttu-id="b5251-295">Событие с кодом 10021</span><span class="sxs-lookup"><span data-stu-id="b5251-295">Event ID 10021</span></span>

<span data-ttu-id="b5251-296">Ошибка "% &lt; *_information* &gt; операции с файлом для операции &lt; с *_name* &gt; &lt; *именем*файла &gt; .</span><span class="sxs-lookup"><span data-stu-id="b5251-296">Error &lt;*error\_information*&gt; for file operation &lt;*operation\_name*&gt; on file &lt;*filename*&gt;.</span></span>

<a href="" id="description"></a>**<span data-ttu-id="b5251-297">Описание</span><span class="sxs-lookup"><span data-stu-id="b5251-297">Description</span></span>**  
<span data-ttu-id="b5251-298">При создании или удалении ярлыка произошла ошибка несанкционированного доступа или ввода-вывода.</span><span class="sxs-lookup"><span data-stu-id="b5251-298">An unauthorized access or I/O error occurred when a shortcut was being created or deleted.</span></span>

<a href="" id="solution"></a>**<span data-ttu-id="b5251-299">Решение</span><span class="sxs-lookup"><span data-stu-id="b5251-299">Solution</span></span>**  
<span data-ttu-id="b5251-300">Убедитесь в том, что путь к файлу доступен и что у пользователя есть разрешения на создание или удаление указанного файла.</span><span class="sxs-lookup"><span data-stu-id="b5251-300">Check that the file path can be accessed and that the user has permissions to create or delete the specified file.</span></span>

### <span data-ttu-id="b5251-301">Гостевая установка исправлений</span><span class="sxs-lookup"><span data-stu-id="b5251-301">Guest Patching</span></span>

### <span data-ttu-id="b5251-302">Событие с кодом 11001</span><span class="sxs-lookup"><span data-stu-id="b5251-302">Event ID 11001</span></span>

<span data-ttu-id="b5251-303">Сообщение об использовании задачи пробуждения гостя.</span><span class="sxs-lookup"><span data-stu-id="b5251-303">Guest wakeup task usage message.</span></span>

<a href="" id="description"></a>**<span data-ttu-id="b5251-304">Описание</span><span class="sxs-lookup"><span data-stu-id="b5251-304">Description</span></span>**  
<span data-ttu-id="b5251-305">MedvHost.exe с параметром/GuestWakeup был выполнен неправильно или неправильно отформатирован.</span><span class="sxs-lookup"><span data-stu-id="b5251-305">MedvHost.exe with the /GuestWakeup option was executed incorrectly, or the command is formatted incorrectly.</span></span>

<a href="" id="solution"></a>**<span data-ttu-id="b5251-306">Решение</span><span class="sxs-lookup"><span data-stu-id="b5251-306">Solution</span></span>**  
<span data-ttu-id="b5251-307">Убедитесь, что команда выполняется в следующем формате:</span><span class="sxs-lookup"><span data-stu-id="b5251-307">Ensure that the command is executed with the following format:</span></span>

<span data-ttu-id="b5251-308">Medvhost.exe/GuestWakeup/d: &lt; *duration \ _in \ _minutes* &gt; /v: " &lt; *Рабочая область \ _name* &gt; " где</span><span class="sxs-lookup"><span data-stu-id="b5251-308">Medvhost.exe /GuestWakeup /d:&lt; *duration\_in\_minutes*&gt; /v:”&lt; *workspace\_name*&gt;” where</span></span>

<span data-ttu-id="b5251-309">&lt;*duration _IN \ _minutes* &gt; — количество минут, в течение которых виртуальная машина должна оставаться в спящем (значение по умолчанию — 240).</span><span class="sxs-lookup"><span data-stu-id="b5251-309">&lt;*duration\_in\_minutes*&gt; is the number of minutes that the virtual machine should stay awake (default is 240) and</span></span>

<span data-ttu-id="b5251-310">&lt;*Рабочая область \ _name* &gt; — имя виртуальной машины, которая должна быть пробуждена.</span><span class="sxs-lookup"><span data-stu-id="b5251-310">&lt;*workspace\_name*&gt; is the name of the virtual machine that should be awakened.</span></span>

### <span data-ttu-id="b5251-311">Событие с кодом 11002</span><span class="sxs-lookup"><span data-stu-id="b5251-311">Event ID 11002</span></span>

<span data-ttu-id="b5251-312">Не удается обновить MED-V — сеть узла не обнаружена.</span><span class="sxs-lookup"><span data-stu-id="b5251-312">Cannot update MED-V – No host network detected.</span></span>

<a href="" id="description"></a>**<span data-ttu-id="b5251-313">Описание</span><span class="sxs-lookup"><span data-stu-id="b5251-313">Description</span></span>**  
<span data-ttu-id="b5251-314">Не удалось завершить гостевой патч, так как не обнаружено сетевое соединение с узлом.</span><span class="sxs-lookup"><span data-stu-id="b5251-314">Guest patching could not finish because no host network connection was detected.</span></span>

<a href="" id="solution"></a>**<span data-ttu-id="b5251-315">Решение</span><span class="sxs-lookup"><span data-stu-id="b5251-315">Solution</span></span>**  
<span data-ttu-id="b5251-316">Подключите узел MED-V к активному сетевому подключению, прежде чем выполнять исправление гостя.</span><span class="sxs-lookup"><span data-stu-id="b5251-316">Connect the MED-V host to an active network connection before you run guest patching.</span></span>

### <span data-ttu-id="b5251-317">Событие с кодом 11003</span><span class="sxs-lookup"><span data-stu-id="b5251-317">Event ID 11003</span></span>

<span data-ttu-id="b5251-318">Не удается обновить MED-V — узел не запущен на powerFailed/C, чтобы создать сервер канала.</span><span class="sxs-lookup"><span data-stu-id="b5251-318">Cannot update MED-V – Host not running on A/C powerFailed to create pipe server.</span></span>

<a href="" id="description"></a>**<span data-ttu-id="b5251-319">Описание</span><span class="sxs-lookup"><span data-stu-id="b5251-319">Description</span></span>**  
<span data-ttu-id="b5251-320">Гостевая установка не может быть завершена, так как на нем не работает питание от аккумулятора, а не с кабеля питания.</span><span class="sxs-lookup"><span data-stu-id="b5251-320">Guest patching could not finish because the host appears to be running on battery power instead of from a power cord.</span></span>

<a href="" id="solution"></a>**<span data-ttu-id="b5251-321">Решение</span><span class="sxs-lookup"><span data-stu-id="b5251-321">Solution</span></span>**  
<span data-ttu-id="b5251-322">Перед запуском гостевых исправлений Подключите главный компьютер к кабелю питания.</span><span class="sxs-lookup"><span data-stu-id="b5251-322">Connect the host computer to a power cord before you run guest patching.</span></span>

### <span data-ttu-id="b5251-323">UI клиента</span><span class="sxs-lookup"><span data-stu-id="b5251-323">Client UX</span></span>

### <span data-ttu-id="b5251-324">Событие с кодом 14003</span><span class="sxs-lookup"><span data-stu-id="b5251-324">Event ID 14003</span></span>

<span data-ttu-id="b5251-325">Следующее сообщение о состоянии слишком длинное, и его не удалось отобразить: &lt; *табло \ _status \ _message*&gt;</span><span class="sxs-lookup"><span data-stu-id="b5251-325">The following tray status message was too long and could not be displayed: &lt;*tray\_status\_message*&gt;</span></span>

<a href="" id="description"></a>**<span data-ttu-id="b5251-326">Описание</span><span class="sxs-lookup"><span data-stu-id="b5251-326">Description</span></span>**  
<span data-ttu-id="b5251-327">MED-V создал непредвиденную строку, которая слишком длинна для всплывающей подсказки или всплывающего сообщения.</span><span class="sxs-lookup"><span data-stu-id="b5251-327">MED-V created an unanticipated string that was too long for the tray tooltip or balloon message.</span></span> <span data-ttu-id="b5251-328">В результате отображенное сообщение было усечено.</span><span class="sxs-lookup"><span data-stu-id="b5251-328">As a result, the displayed message was truncated.</span></span>

<a href="" id="solution"></a>**<span data-ttu-id="b5251-329">Решение</span><span class="sxs-lookup"><span data-stu-id="b5251-329">Solution</span></span>**  
<span data-ttu-id="b5251-330">Это редкие ошибки, которые могут возникать, если MED-V создает случайным образом текст всплывающей подсказки.</span><span class="sxs-lookup"><span data-stu-id="b5251-330">This is a rare error that can occur when MED-V is randomly creating the tooltip text.</span></span> <span data-ttu-id="b5251-331">Решение отсутствует.</span><span class="sxs-lookup"><span data-stu-id="b5251-331">There is no solution.</span></span>

### <span data-ttu-id="b5251-332">Событие с кодом 14004</span><span class="sxs-lookup"><span data-stu-id="b5251-332">Event ID 14004</span></span>

<span data-ttu-id="b5251-333">MED-V остановлен из-за неуправляемого исключения.</span><span class="sxs-lookup"><span data-stu-id="b5251-333">MED-V stopped due to an unhandled exception.</span></span>

<a href="" id="description"></a>**<span data-ttu-id="b5251-334">Описание</span><span class="sxs-lookup"><span data-stu-id="b5251-334">Description</span></span>**  
<span data-ttu-id="b5251-335">Неуправляемое исключение привело к неожиданной остановке MED-V.</span><span class="sxs-lookup"><span data-stu-id="b5251-335">An unhandled exception caused MED-V to stop unexpectedly.</span></span>

<a href="" id="solution"></a>**<span data-ttu-id="b5251-336">Решение</span><span class="sxs-lookup"><span data-stu-id="b5251-336">Solution</span></span>**  
<span data-ttu-id="b5251-337">Перезапустите MED-V.</span><span class="sxs-lookup"><span data-stu-id="b5251-337">Restart MED-V.</span></span>

### <span data-ttu-id="b5251-338">Событие с кодом 14005</span><span class="sxs-lookup"><span data-stu-id="b5251-338">Event ID 14005</span></span>

<span data-ttu-id="b5251-339">Сервер попытался создать мьютекс, но он уже существует.</span><span class="sxs-lookup"><span data-stu-id="b5251-339">Server attempted to create mutex but it already existed.</span></span>

<a href="" id="description"></a>**<span data-ttu-id="b5251-340">Описание</span><span class="sxs-lookup"><span data-stu-id="b5251-340">Description</span></span>**  
<span data-ttu-id="b5251-341">Второй экземпляр MedvHost.exe зависает в памяти.</span><span class="sxs-lookup"><span data-stu-id="b5251-341">A second instance of MedvHost.exe is stuck in memory.</span></span>

<a href="" id="solution"></a>**<span data-ttu-id="b5251-342">Решение</span><span class="sxs-lookup"><span data-stu-id="b5251-342">Solution</span></span>**  
<span data-ttu-id="b5251-343">Откройте TaskManager и завершите все процессы MedvHost.exe.</span><span class="sxs-lookup"><span data-stu-id="b5251-343">Open TaskManager and end all MedvHost.exe processes.</span></span>

### <span data-ttu-id="b5251-344">Событие с кодом 14006</span><span class="sxs-lookup"><span data-stu-id="b5251-344">Event ID 14006</span></span>

<span data-ttu-id="b5251-345">Ошибка при изменении или удалении значения реестра &lt; *\ _Value* &gt; .</span><span class="sxs-lookup"><span data-stu-id="b5251-345">Error modifying or deleting registry value &lt;*registry\_value*&gt;.</span></span>

<a href="" id="description"></a>**<span data-ttu-id="b5251-346">Описание</span><span class="sxs-lookup"><span data-stu-id="b5251-346">Description</span></span>**  
<span data-ttu-id="b5251-347">MED-V не удается изменить указанный элемент в реестре.</span><span class="sxs-lookup"><span data-stu-id="b5251-347">MED-V is unable to modify the specified entry in the registry.</span></span>

<a href="" id="solution"></a>**<span data-ttu-id="b5251-348">Решение</span><span class="sxs-lookup"><span data-stu-id="b5251-348">Solution</span></span>**  
<span data-ttu-id="b5251-349">Убедитесь, что вы установили и удалите MED-V с учетными данными администратора.</span><span class="sxs-lookup"><span data-stu-id="b5251-349">Ensure that you install or uninstall MED-V with administrative credentials.</span></span>

### <span data-ttu-id="b5251-350">Событие с кодом 14007</span><span class="sxs-lookup"><span data-stu-id="b5251-350">Event ID 14007</span></span>

<span data-ttu-id="b5251-351">Указанный файл ( &lt; *имя файла* &gt; ) является недопустимым.</span><span class="sxs-lookup"><span data-stu-id="b5251-351">The file specified (&lt;*filename*&gt;) is not valid.</span></span>

<a href="" id="description"></a>**<span data-ttu-id="b5251-352">Описание</span><span class="sxs-lookup"><span data-stu-id="b5251-352">Description</span></span>**  
<span data-ttu-id="b5251-353">Во время установки или удаления поврежденный временный файл был передан узлу MED-V.</span><span class="sxs-lookup"><span data-stu-id="b5251-353">During install or uninstall, a corrupted temp file was passed to MED-V host.</span></span>

<a href="" id="solution"></a>**<span data-ttu-id="b5251-354">Решение</span><span class="sxs-lookup"><span data-stu-id="b5251-354">Solution</span></span>**  
<span data-ttu-id="b5251-355">Удалите все файлы в папке TEMP и переустановите или удалите MED-V.</span><span class="sxs-lookup"><span data-stu-id="b5251-355">Delete all files in the Temp folder and reinstall or uninstall MED-V.</span></span>

### <span data-ttu-id="b5251-356">Событие с кодом 14008</span><span class="sxs-lookup"><span data-stu-id="b5251-356">Event ID 14008</span></span>

<span data-ttu-id="b5251-357">Файл не найден: &lt; *имя файла* &gt; .</span><span class="sxs-lookup"><span data-stu-id="b5251-357">File not found: &lt;*filename*&gt;.</span></span>

<a href="" id="description"></a>**<span data-ttu-id="b5251-358">Описание</span><span class="sxs-lookup"><span data-stu-id="b5251-358">Description</span></span>**  
<span data-ttu-id="b5251-359">Во время установки или удаления не найден путь требуемого временного файла.</span><span class="sxs-lookup"><span data-stu-id="b5251-359">During install or uninstall, a path of a required temp file was not found.</span></span>

<a href="" id="solution"></a>**<span data-ttu-id="b5251-360">Решение</span><span class="sxs-lookup"><span data-stu-id="b5251-360">Solution</span></span>**  
<span data-ttu-id="b5251-361">Удалите все файлы в папке TEMP и переустановите или удалите MED-V.</span><span class="sxs-lookup"><span data-stu-id="b5251-361">Delete all files in the Temp folder and reinstall or uninstall MED-V.</span></span>

### <span data-ttu-id="b5251-362">Событие с кодом 14009</span><span class="sxs-lookup"><span data-stu-id="b5251-362">Event ID 14009</span></span>

<span data-ttu-id="b5251-363">Не удалось прочитать имя файла параметров &lt; *filename* &gt; .</span><span class="sxs-lookup"><span data-stu-id="b5251-363">Unable to read parameter file &lt;*filename*&gt;.</span></span>

<a href="" id="description"></a>**<span data-ttu-id="b5251-364">Описание</span><span class="sxs-lookup"><span data-stu-id="b5251-364">Description</span></span>**  
<span data-ttu-id="b5251-365">В процессе установки или удаления MED-V не удалось прочитать временный файл.</span><span class="sxs-lookup"><span data-stu-id="b5251-365">During the install or uninstall process, MED-V was unable to read a temp file.</span></span>

<a href="" id="solution"></a>**<span data-ttu-id="b5251-366">Решение</span><span class="sxs-lookup"><span data-stu-id="b5251-366">Solution</span></span>**  
<span data-ttu-id="b5251-367">Удалите все файлы в папке TEMP и переустановите или удалите MED-V.</span><span class="sxs-lookup"><span data-stu-id="b5251-367">Delete all files in the Temp folder and reinstall or uninstall MED-V.</span></span> <span data-ttu-id="b5251-368">Кроме того, убедитесь, что у пользователя есть необходимые права и разрешения на доступ к папке Temp.</span><span class="sxs-lookup"><span data-stu-id="b5251-368">In addition, verify that the user has the necessary rights and permissions to the Temp folder.</span></span>

### <span data-ttu-id="b5251-369">Событие с кодом 14010</span><span class="sxs-lookup"><span data-stu-id="b5251-369">Event ID 14010</span></span>

<span data-ttu-id="b5251-370">Ошибка при десериализации имени файла параметров &lt; *filename* &gt; .</span><span class="sxs-lookup"><span data-stu-id="b5251-370">Error deserializing parameter file &lt;*filename*&gt;.</span></span>

<a href="" id="description"></a>**<span data-ttu-id="b5251-371">Описание</span><span class="sxs-lookup"><span data-stu-id="b5251-371">Description</span></span>**  
<span data-ttu-id="b5251-372">В процессе установки или удаления в MED-V обнаружен поврежденный временный файл.</span><span class="sxs-lookup"><span data-stu-id="b5251-372">During the install or uninstall process, MED-V encountered a corrupted temp file.</span></span>

<a href="" id="solution"></a>**<span data-ttu-id="b5251-373">Решение</span><span class="sxs-lookup"><span data-stu-id="b5251-373">Solution</span></span>**  
<span data-ttu-id="b5251-374">Удалите все файлы в папке TEMP и переустановите или удалите MED-V.</span><span class="sxs-lookup"><span data-stu-id="b5251-374">Delete all files in the Temp folder and reinstall or uninstall MED-V.</span></span> <span data-ttu-id="b5251-375">Кроме того, убедитесь, что у пользователя есть необходимые права и разрешения на доступ к папке Temp.</span><span class="sxs-lookup"><span data-stu-id="b5251-375">In addition, verify that the user has the necessary rights and permissions to the Temp folder.</span></span>

### <span data-ttu-id="b5251-376">Событие с кодом 14011</span><span class="sxs-lookup"><span data-stu-id="b5251-376">Event ID 14011</span></span>

<span data-ttu-id="b5251-377">Непредвиденная ошибка при десериализации &lt; *имени*файла параметра &gt; .</span><span class="sxs-lookup"><span data-stu-id="b5251-377">Unexpected error deserializing parameter file &lt;*filename*&gt;.</span></span>

<a href="" id="description"></a>**<span data-ttu-id="b5251-378">Описание</span><span class="sxs-lookup"><span data-stu-id="b5251-378">Description</span></span>**  
<span data-ttu-id="b5251-379">В процессе установки или удаления в MED-V обнаружен поврежденный временный файл.</span><span class="sxs-lookup"><span data-stu-id="b5251-379">During the install or uninstall process, MED-V encountered a corrupted temp file.</span></span>

<a href="" id="solution"></a>**<span data-ttu-id="b5251-380">Решение</span><span class="sxs-lookup"><span data-stu-id="b5251-380">Solution</span></span>**  
<span data-ttu-id="b5251-381">Удалите все файлы в папке TEMP и переустановите или удалите MED-V.</span><span class="sxs-lookup"><span data-stu-id="b5251-381">Delete all files in the Temp folder and reinstall or uninstall MED-V.</span></span> <span data-ttu-id="b5251-382">Кроме того, убедитесь, что у пользователя есть необходимые права и разрешения на доступ к папке Temp.</span><span class="sxs-lookup"><span data-stu-id="b5251-382">In addition, verify that the user has the necessary rights and permissions to the Temp folder.</span></span>

### <span data-ttu-id="b5251-383">Событие с кодом 14012</span><span class="sxs-lookup"><span data-stu-id="b5251-383">Event ID 14012</span></span>

<span data-ttu-id="b5251-384">Непредвиденная ошибка, когда права на параметры для папки "папка" &lt; *\ _name* &gt; для &lt; *имени*пользователя &gt; .</span><span class="sxs-lookup"><span data-stu-id="b5251-384">Unexpected error when settings rights on folder &lt;*folder\_name*&gt; for user &lt;*username*&gt;.</span></span>

<a href="" id="description"></a>**<span data-ttu-id="b5251-385">Описание</span><span class="sxs-lookup"><span data-stu-id="b5251-385">Description</span></span>**  
<span data-ttu-id="b5251-386">Если при установке служб MED-V не удается установить права и разрешения на доступ к определенным папкам, возникает ошибка.</span><span class="sxs-lookup"><span data-stu-id="b5251-386">An error occurs when MED-V is unable to set rights and permissions on certain folders during installation.</span></span>

<a href="" id="solution"></a>**<span data-ttu-id="b5251-387">Решение</span><span class="sxs-lookup"><span data-stu-id="b5251-387">Solution</span></span>**  
<span data-ttu-id="b5251-388">Убедитесь в том, что права администратора указаны в следующих папках:</span><span class="sxs-lookup"><span data-stu-id="b5251-388">Check the administrator rights to the following folders:</span></span>

<span data-ttu-id="b5251-389">@"%ProgramData%\\Microsoft\\Medv\\AllUsers"</span><span class="sxs-lookup"><span data-stu-id="b5251-389">@"%ProgramData%\\Microsoft\\Medv\\AllUsers"</span></span>

<span data-ttu-id="b5251-390">@"%ProgramData%\\Microsoft\\Medv\\MedvLock"</span><span class="sxs-lookup"><span data-stu-id="b5251-390">@"%ProgramData%\\Microsoft\\Medv\\MedvLock"</span></span>

<span data-ttu-id="b5251-391">@"%ProgramData%\\Microsoft\\Medv\\Monitoring"</span><span class="sxs-lookup"><span data-stu-id="b5251-391">@"%ProgramData%\\Microsoft\\Medv\\Monitoring"</span></span>

### <span data-ttu-id="b5251-392">Событие с кодом 14013</span><span class="sxs-lookup"><span data-stu-id="b5251-392">Event ID 14013</span></span>

<span data-ttu-id="b5251-393">Произошла непредвиденная ошибка при создании файла блокировки.</span><span class="sxs-lookup"><span data-stu-id="b5251-393">Unexpected error when creating lock file.</span></span>

<a href="" id="description"></a>**<span data-ttu-id="b5251-394">Описание</span><span class="sxs-lookup"><span data-stu-id="b5251-394">Description</span></span>**  
<span data-ttu-id="b5251-395">Ошибка возникает, когда MED-V не удается создать файл в папке @ "%ProgramData%\\Microsoft\\Medv\\MedvLock" во время установки.</span><span class="sxs-lookup"><span data-stu-id="b5251-395">An error occurs when MED-V is unable to create a file in the @"%ProgramData%\\Microsoft\\Medv\\MedvLock" folder during installation.</span></span>

<a href="" id="solution"></a>**<span data-ttu-id="b5251-396">Решение</span><span class="sxs-lookup"><span data-stu-id="b5251-396">Solution</span></span>**  
<span data-ttu-id="b5251-397">Убедитесь, что права администратора находятся в папке MedvLock.</span><span class="sxs-lookup"><span data-stu-id="b5251-397">Check the administrator rights to the MedvLock folder.</span></span>

## <span data-ttu-id="b5251-398">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="b5251-398">Related topics</span></span>


[<span data-ttu-id="b5251-399">Устранение неполадок MED-V</span><span class="sxs-lookup"><span data-stu-id="b5251-399">Troubleshooting MED-V</span></span>](troubleshooting-med-vmedv2.md)

 

 






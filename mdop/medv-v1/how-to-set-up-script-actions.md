---
title: Настройка действий сценариев
description: Настройка действий сценариев
author: dansimp
ms.assetid: 367e28f1-d8c2-4845-a01b-2fff9128ccfd
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 2bfa264be447a0a8560e4af16ccaadc2ec1db3f6
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10812389"
---
# <span data-ttu-id="1bc68-103">Настройка действий сценариев</span><span class="sxs-lookup"><span data-stu-id="1bc68-103">How to Set Up Script Actions</span></span>


<span data-ttu-id="1bc68-104">Редактор действий со сценариями позволяет администратору создавать действия, которые должны выполняться во время настройки MED-V Workspace, а также определять порядок их выполнения.</span><span class="sxs-lookup"><span data-stu-id="1bc68-104">The script actions editor allows the administrator to create actions to be performed during MED-V workspace setup, as well as to define the order in which they are performed.</span></span>

<span data-ttu-id="1bc68-105">Ниже приведен список действий, которые можно добавить в сценарий настройки домена.</span><span class="sxs-lookup"><span data-stu-id="1bc68-105">The following is a list of actions that can be added to the domain setup script:</span></span>

-   <span data-ttu-id="1bc68-106">**Перезагрузите Windows**, перезапустите Windows.</span><span class="sxs-lookup"><span data-stu-id="1bc68-106">**Restart Windows**—Restart Windows.</span></span>

-   <span data-ttu-id="1bc68-107">**Присоединение к**домену — если присоединиться к домену, включите это действие и настройте имя пользователя, пароль, полное доменное имя, NetBIOS-имя домена и организационное подразделение (необязательно).</span><span class="sxs-lookup"><span data-stu-id="1bc68-107">**Join Domain**—If joining a domain, include this action and configure the user name, password, fully qualified domain name, NetBIOS domain name, and organization unit (optional).</span></span>

-   <span data-ttu-id="1bc68-108">**Проверьте подключение**, настройте сервер для подключения и убедитесь, что Рабочая область MED-V может подключаться к сетевому ресурсу (например, серверу домена).</span><span class="sxs-lookup"><span data-stu-id="1bc68-108">**Check Connectivity**—Configure a server to connect to and verify that the MED-V workspace can connect to a network resource (such as the domain server).</span></span>

-   <span data-ttu-id="1bc68-109">**Командная строка**— настройте сценарий в рабочей области MED-V и введите командную строку, содержащую путь к скрипту и аргументы сценария.</span><span class="sxs-lookup"><span data-stu-id="1bc68-109">**Command Line**—Configure a script in the MED-V workspace, and enter a command line that includes the path of the script and the script arguments.</span></span>

-   <span data-ttu-id="1bc68-110">**Переименование компьютера**— переименование компьютера виртуальной машины в соответствии с заданными параметрами.</span><span class="sxs-lookup"><span data-stu-id="1bc68-110">**Rename Computer**—Rename the virtual machine computer based on the defined settings.</span></span>

-   <span data-ttu-id="1bc68-111">**Отключение автоматического входа в систему**— отключите функцию автоматического входа в Windows.</span><span class="sxs-lookup"><span data-stu-id="1bc68-111">**Disable Auto-Logon**—Disable Windows Auto-Logon.</span></span> <span data-ttu-id="1bc68-112">Это действие необходимо добавить в конце сценариев, которые добавляют компьютер в домен.</span><span class="sxs-lookup"><span data-stu-id="1bc68-112">This action should be added at the end of scripts that add the computer to the domain.</span></span>

## <a href="" id="how-to-set-up-script-actions-"></a><span data-ttu-id="1bc68-113">Настройка действий сценариев</span><span class="sxs-lookup"><span data-stu-id="1bc68-113">How to Set Up Script Actions</span></span>


**<span data-ttu-id="1bc68-114">Настройка действий сценария</span><span class="sxs-lookup"><span data-stu-id="1bc68-114">To set up script actions</span></span>**

1.  <span data-ttu-id="1bc68-115">На вкладке **Настройка виртуальной машины** нажмите кнопку **Редактор скриптов**.</span><span class="sxs-lookup"><span data-stu-id="1bc68-115">On the **VM Setup** tab, click **Script Editor**.</span></span>

2.  <span data-ttu-id="1bc68-116">В диалоговом окне **действия со сценарием** нажмите кнопку **Добавить**, а затем в подменю выберите нужные действия.</span><span class="sxs-lookup"><span data-stu-id="1bc68-116">In the **Script Actions** dialog box, click **Add**, and on the submenu, click the desired actions.</span></span>

3.  <span data-ttu-id="1bc68-117">Настройте действия, как описано в приведенных ниже таблицах.</span><span class="sxs-lookup"><span data-stu-id="1bc68-117">Configure the actions as described in the following tables.</span></span>

    <span data-ttu-id="1bc68-118">**Примечание** 
     **Переименование компьютера** настроено на вкладке **Параметры виртуальной машины** . Дополнительные сведения [можно найти в разделе Настройка свойств шаблона имени компьютера виртуальной машины](how-to-configure-vm-computer-name-pattern-propertiesmedvv2.md).</span><span class="sxs-lookup"><span data-stu-id="1bc68-118">**Note**
**Rename Computer** is configured in the **VM Settings** tab. For more information, see [How to Configure VM Computer Name Pattern Properties](how-to-configure-vm-computer-name-pattern-propertiesmedvv2.md).</span></span>

     

~~~
**Note**  
To rename a computer, Windows must be restarted. It is recommended to add a Restart Windows action following a Rename Computer action.
~~~



4. <span data-ttu-id="1bc68-119">Чтобы настроить порядок действий, выберите нужное действие и нажмите кнопку **вверх** или **вниз**.</span><span class="sxs-lookup"><span data-stu-id="1bc68-119">Set the order of the actions by selecting an action and clicking **Up** or **Down**.</span></span>

5. <span data-ttu-id="1bc68-120">Нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="1bc68-120">Click **OK**.</span></span>

**<span data-ttu-id="1bc68-121">Примечание</span><span class="sxs-lookup"><span data-stu-id="1bc68-121">Note</span></span>**  
<span data-ttu-id="1bc68-122">При выполнении сценария присоединения к домену, чтобы сценарий работал, пользователь, вошедшего в виртуальную машину рабочей области MED-V, должен иметь права локального администратора.</span><span class="sxs-lookup"><span data-stu-id="1bc68-122">When running the Join Domain script, for the script to work, the user logged into the MED-V workspace virtual machine must have local administrator rights.</span></span>



**<span data-ttu-id="1bc68-123">Примечание.</span><span class="sxs-lookup"><span data-stu-id="1bc68-123">Note</span></span>**  
<span data-ttu-id="1bc68-124">При запуске автоматического входа в систему рекомендуется отключить локальную гостевую учетную запись, используемую для автовхода, после завершения первоначальной настройки.</span><span class="sxs-lookup"><span data-stu-id="1bc68-124">When running the Disable Auto-Logon script, it is recommended to disable the local guest account used for the auto-logon once the initial setup is complete.</span></span>



### <a href="" id="bkmk-joindomainproperties"></a>

**<span data-ttu-id="1bc68-125">Присоединение свойств домена</span><span class="sxs-lookup"><span data-stu-id="1bc68-125">Join Domain Properties</span></span>**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="1bc68-126">Свойство</span><span class="sxs-lookup"><span data-stu-id="1bc68-126">Property</span></span></th>
<th align="left"><span data-ttu-id="1bc68-127">Описание</span><span class="sxs-lookup"><span data-stu-id="1bc68-127">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="1bc68-128">Учетные данные, которые следует использовать при присоединении виртуальной машины к домену.</span><span class="sxs-lookup"><span data-stu-id="1bc68-128">Credentials to use when joining the VM to the domain</span></span></p></td>
<td align="left"><p><span data-ttu-id="1bc68-129">Выберите один из следующих учетных данных, которые нужно использовать при присоединении виртуальной машины к домену.</span><span class="sxs-lookup"><span data-stu-id="1bc68-129">Select one of the following credentials to use when joining the VM to the domain:</span></span></p>
<ul>
<li><p><strong><span data-ttu-id="1bc68-130">С помощью учетных данных </strong> для пользователей MED-V — учетные данные конечного пользователя.</span><span class="sxs-lookup"><span data-stu-id="1bc68-130">Use MED-V credentials</strong>—The end-user credentials.</span></span></p></li>
<li><p><strong><span data-ttu-id="1bc68-131">Используйте указанные ниже учетные данные </strong> , а затем введите имя пользователя и пароль в соответствующих полях.</span><span class="sxs-lookup"><span data-stu-id="1bc68-131">Use the following credentials</strong>—The credentials specified; enter a user name and password in the corresponding fields.</span></span></p></li>
</ul>
<div class="alert">
<strong><span data-ttu-id="1bc68-132">Примечание.</span><span class="sxs-lookup"><span data-stu-id="1bc68-132">Note</span></span></strong><br/><p><span data-ttu-id="1bc68-133">Введенные учетные данные видны всем пользователям рабочей области MED-V.</span><span class="sxs-lookup"><span data-stu-id="1bc68-133">The credentials you enter are visible to all MED-V workspace users.</span></span> <span data-ttu-id="1bc68-134">Не рекомендуется предоставлять учетные данные администратора домена.</span><span class="sxs-lookup"><span data-stu-id="1bc68-134">It is not recommended to provide domain administrator credentials.</span></span></p>
</div>
<div>

</div></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="1bc68-135">Домен, к которому присоединяется домен</span><span class="sxs-lookup"><span data-stu-id="1bc68-135">Domain to join</span></span></p></td>
<td align="left"><p><span data-ttu-id="1bc68-136">Выберите один из следующих вариантов:</span><span class="sxs-lookup"><span data-stu-id="1bc68-136">Select one of the following:</span></span></p>
<ul>
<li><p><strong><span data-ttu-id="1bc68-137">Использовать доменное имя, используемое в начале рабочей области </strong> — присоединиться к домену, введенному конечным пользователем при входе в клиент MED-V.</span><span class="sxs-lookup"><span data-stu-id="1bc68-137">Use the domain name utilized in starting the Workspace</strong>—Join the domain entered by the end user when logging into the MED-V client.</span></span></p>
<p><span data-ttu-id="1bc68-138">Чтобы определить сопоставление из NetBIOS для полных доменных имен, выберите вариант <strong> Глобальная таблица сопоставления доменов </strong> .</span><span class="sxs-lookup"><span data-stu-id="1bc68-138">To define the mapping from NetBIOS to fully qualified domain names, click <strong>Global domain mapping table</strong>.</span></span> <span data-ttu-id="1bc68-139">В таблице глобальный домен сопоставления нажмите кнопку <strong> Добавить </strong> , введите NetBIOS- <strong> имя домена </strong> и полное <strong> доменное имя </strong> и нажмите кнопку <strong> ОК </strong> .</span><span class="sxs-lookup"><span data-stu-id="1bc68-139">In the global domain mapping table, click <strong>Add</strong>, enter a <strong>NetBIOS domain name</strong> and a <strong>Fully qualified domain name</strong>, and click <strong>OK</strong>.</span></span></p></li>
<li><p><strong><span data-ttu-id="1bc68-140">Используйте следующее доменное имя </strong> — присоединиться к указанному домену; введите доменное имя и доменное имя NetBIOS в соответствующие поля.</span><span class="sxs-lookup"><span data-stu-id="1bc68-140">Use the following domain name</strong>—Join the domain specified; enter a domain name and NetBIOS domain name in the corresponding fields.</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="1bc68-141">Организационное подразделение</span><span class="sxs-lookup"><span data-stu-id="1bc68-141">Organization Unit</span></span></p></td>
<td align="left"><p><span data-ttu-id="1bc68-142">Для присоединения компьютера к определенному подразделению может быть задано подразделение Организации (OU).</span><span class="sxs-lookup"><span data-stu-id="1bc68-142">An organization unit (OU) may be specified to join the computer to a specific OU.</span></span> <span data-ttu-id="1bc68-143">Формат должен следовать за различающимся именем в подразделении: OU = &lt; подразделение &gt; , &lt; контроллер домена &gt; (например, OU = QATest, DC = IL, DC = MED-V, DC = "com").</span><span class="sxs-lookup"><span data-stu-id="1bc68-143">The format must follow an OU distinguished name: OU=&lt;Organization Unit&gt;,&lt;Domain Controller&gt; (for example, OU=QATest, DC=il, DC=MED-V, DC=com).</span></span></p>
<div class="alert">
<strong><span data-ttu-id="1bc68-144">Warning</span><span class="sxs-lookup"><span data-stu-id="1bc68-144">Warning</span></span></strong><br/><p><span data-ttu-id="1bc68-145">Поддерживается только подразделение одного уровня, как показано в примере выше.</span><span class="sxs-lookup"><span data-stu-id="1bc68-145">Only a single level OU is supported as is shown in the example above.</span></span></p>
</div>
<div>
 
</div></td>
</tr>
</tbody>
</table>

 

### <a href="" id="bkmk-checkconnectivityproperties"></a>

**<span data-ttu-id="1bc68-146">Проверка свойств подключения</span><span class="sxs-lookup"><span data-stu-id="1bc68-146">Check Connectivity Properties</span></span>**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="1bc68-147">Свойство</span><span class="sxs-lookup"><span data-stu-id="1bc68-147">Property</span></span></th>
<th align="left"><span data-ttu-id="1bc68-148">Описание</span><span class="sxs-lookup"><span data-stu-id="1bc68-148">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="1bc68-149">IP-адрес</span><span class="sxs-lookup"><span data-stu-id="1bc68-149">IP Address</span></span></p></td>
<td align="left"><p><span data-ttu-id="1bc68-150">IP-адрес сервера, на который проверяется соединение.</span><span class="sxs-lookup"><span data-stu-id="1bc68-150">The IP Address of the server that you are verifying connection to.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="1bc68-151">Port</span><span class="sxs-lookup"><span data-stu-id="1bc68-151">Port</span></span></p></td>
<td align="left"><p><span data-ttu-id="1bc68-152">Порт сервера, на который проверяется соединение.</span><span class="sxs-lookup"><span data-stu-id="1bc68-152">The port of the server that you are verifying connection to.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="1bc68-153">Превышено время ожидания</span><span class="sxs-lookup"><span data-stu-id="1bc68-153">Timeout</span></span></p></td>
<td align="left"><p><span data-ttu-id="1bc68-154">Время ожидания ответа (в секундах).</span><span class="sxs-lookup"><span data-stu-id="1bc68-154">The number of seconds to wait for a response before timing out.</span></span></p></td>
</tr>
</tbody>
</table>

 

### <a href="" id="bkmk-commandlineproperties"></a>

**<span data-ttu-id="1bc68-155">Свойства командной строки</span><span class="sxs-lookup"><span data-stu-id="1bc68-155">Command-Line Properties</span></span>**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="1bc68-156">Свойство</span><span class="sxs-lookup"><span data-stu-id="1bc68-156">Property</span></span></th>
<th align="left"><span data-ttu-id="1bc68-157">Описание</span><span class="sxs-lookup"><span data-stu-id="1bc68-157">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="1bc68-158">Путь</span><span class="sxs-lookup"><span data-stu-id="1bc68-158">Path</span></span></p></td>
<td align="left"><p><span data-ttu-id="1bc68-159">Путь к командной строке.</span><span class="sxs-lookup"><span data-stu-id="1bc68-159">The path of the command line.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="1bc68-160">Arguments</span><span class="sxs-lookup"><span data-stu-id="1bc68-160">Arguments</span></span></p></td>
<td align="left"><p><span data-ttu-id="1bc68-161">Аргументы командной строки.</span><span class="sxs-lookup"><span data-stu-id="1bc68-161">Command-line arguments.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="1bc68-162">Ожидание выхода</span><span class="sxs-lookup"><span data-stu-id="1bc68-162">Wait for exit</span></span></p></td>
<td align="left"><p><span data-ttu-id="1bc68-163">Установите флажок, чтобы дождаться возврата, прежде чем продолжить выполнение действий сценария.</span><span class="sxs-lookup"><span data-stu-id="1bc68-163">Select the check box to wait for a return before continuing with the script actions.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="1bc68-164">Сбой при ошибке</span><span class="sxs-lookup"><span data-stu-id="1bc68-164">Fail on error</span></span></p></td>
<td align="left"><p><span data-ttu-id="1bc68-165">Установите этот флажок, если возвращено ничего, но не указанное значение.</span><span class="sxs-lookup"><span data-stu-id="1bc68-165">Select this check box if the return is anything but the value specified.</span></span></p>
<p><span data-ttu-id="1bc68-166">Введите значение, которое будет указывать на команду как успешное.</span><span class="sxs-lookup"><span data-stu-id="1bc68-166">Enter the value that will indicate the command as a success.</span></span></p>
<p><span data-ttu-id="1bc68-167">По умолчанию: <strong> 0</span><span class="sxs-lookup"><span data-stu-id="1bc68-167">Default: <strong>0</span></span></strong></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="1bc68-168">Однократное выполнение</span><span class="sxs-lookup"><span data-stu-id="1bc68-168">Perform only once</span></span></p></td>
<td align="left"><p><span data-ttu-id="1bc68-169">Установите этот флажок, чтобы запустить командную строку только один раз.</span><span class="sxs-lookup"><span data-stu-id="1bc68-169">Select this check box to run the command line only once.</span></span> <span data-ttu-id="1bc68-170">Если сценарий завершается сбоем или будет отменен, эта команда не будет выполнена повторно.</span><span class="sxs-lookup"><span data-stu-id="1bc68-170">If the script fails or is canceled, this command will not be performed again.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="1bc68-171">Эта командная строка приводит к перезапуску Windows в рабочей области</span><span class="sxs-lookup"><span data-stu-id="1bc68-171">This command line causes a restart of Windows in the Workspace</span></span></p></td>
<td align="left"><p><span data-ttu-id="1bc68-172">Установите этот флажок, если Командная строка приводит к перезапуску после завершения.</span><span class="sxs-lookup"><span data-stu-id="1bc68-172">Select this check box if the command line causes a restart after completion.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="1bc68-173">Разрешить взаимодействие</span><span class="sxs-lookup"><span data-stu-id="1bc68-173">Allow interaction</span></span></p></td>
<td align="left"><p><span data-ttu-id="1bc68-174">Установите этот флажок, если для команды потребуется вмешательство пользователя.</span><span class="sxs-lookup"><span data-stu-id="1bc68-174">Select this check box if the command will require user interaction.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="1bc68-175">Сообщение о ходе выполнения</span><span class="sxs-lookup"><span data-stu-id="1bc68-175">Progress message</span></span></p></td>
<td align="left"><p><span data-ttu-id="1bc68-176">Сообщение, отображаемое пользователю во время выполнения команды.</span><span class="sxs-lookup"><span data-stu-id="1bc68-176">Message to be displayed to the user while the command is running.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="1bc68-177">Сообщение об ошибке</span><span class="sxs-lookup"><span data-stu-id="1bc68-177">Failure message</span></span></p></td>
<td align="left"><p><span data-ttu-id="1bc68-178">Сообщение, которое отображается для пользователя, если не удается выполнить команду.</span><span class="sxs-lookup"><span data-stu-id="1bc68-178">Message to be displayed to the user if the command fails.</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="1bc68-179">При настройке действия командной строки можно использовать несколько переменных, как указано в таблице ниже.</span><span class="sxs-lookup"><span data-stu-id="1bc68-179">When configuring the command-line action, several variables can be used as defined in the following table.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="1bc68-180">Параметр</span><span class="sxs-lookup"><span data-stu-id="1bc68-180">Parameter</span></span></th>
<th align="left"><span data-ttu-id="1bc68-181">Значение</span><span class="sxs-lookup"><span data-stu-id="1bc68-181">Value</span></span></th>
<th align="left"><span data-ttu-id="1bc68-182">Описание</span><span class="sxs-lookup"><span data-stu-id="1bc68-182">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="1bc68-183">%MEDVUser%</span><span class="sxs-lookup"><span data-stu-id="1bc68-183">%MEDVUser%</span></span></p></td>
<td align="left"><p><span data-ttu-id="1bc68-184">Имя пользователя, прошедшего проверку подлинности.</span><span class="sxs-lookup"><span data-stu-id="1bc68-184">An authenticated user name.</span></span></p></td>
<td align="left"><p><span data-ttu-id="1bc68-185">Имя пользователя, прошедшего проверку подлинности в MED-V.</span><span class="sxs-lookup"><span data-stu-id="1bc68-185">MED-V authenticated user name.</span></span> <span data-ttu-id="1bc68-186">Имя пользователя и пароль можно использовать в сценарии настройки виртуальной машины "присоединение к домену".</span><span class="sxs-lookup"><span data-stu-id="1bc68-186">The user name and password can be used in the join domain VM setup script.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="1bc68-187">%MEDVPassword%</span><span class="sxs-lookup"><span data-stu-id="1bc68-187">%MEDVPassword%</span></span></p></td>
<td align="left"><p><span data-ttu-id="1bc68-188">Пароль, прошедший проверку подлинности.</span><span class="sxs-lookup"><span data-stu-id="1bc68-188">An authenticated password.</span></span></p></td>
<td align="left"><p><span data-ttu-id="1bc68-189">Пароль, прошедший проверку подлинности в MED-V.</span><span class="sxs-lookup"><span data-stu-id="1bc68-189">MED-V authenticated password.</span></span> <span data-ttu-id="1bc68-190">Имя пользователя и пароль можно использовать в сценарии настройки виртуальной машины "присоединение к домену".</span><span class="sxs-lookup"><span data-stu-id="1bc68-190">The user name and password can be used in the join domain VM setup script.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="1bc68-191">%MEDVDomain%</span><span class="sxs-lookup"><span data-stu-id="1bc68-191">%MEDVDomain%</span></span></p></td>
<td align="left"><p><span data-ttu-id="1bc68-192">Настраиваемый домен.</span><span class="sxs-lookup"><span data-stu-id="1bc68-192">Configured domain.</span></span></p></td>
<td align="left"><p><span data-ttu-id="1bc68-193">Домен, настроенный для проверки подлинности в MED-V.</span><span class="sxs-lookup"><span data-stu-id="1bc68-193">The domain configured in the MED-V authentication.</span></span> <span data-ttu-id="1bc68-194">Его можно использовать в сценарии настройки виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="1bc68-194">It can be used on the VM setup script.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="1bc68-195">%DesiredMachineName%</span><span class="sxs-lookup"><span data-stu-id="1bc68-195">%DesiredMachineName%</span></span></p></td>
<td align="left"><p><span data-ttu-id="1bc68-196">Имя компьютера.</span><span class="sxs-lookup"><span data-stu-id="1bc68-196">Computer name.</span></span></p></td>
<td align="left"><p><span data-ttu-id="1bc68-197">Уникальное имя компьютера, настроенное в приложении управления.</span><span class="sxs-lookup"><span data-stu-id="1bc68-197">The unique computer name configured in the management application.</span></span> <span data-ttu-id="1bc68-198">Его можно использовать в сценарии настройки виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="1bc68-198">It can be used in the VM setup script.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="1bc68-199">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="1bc68-199">Related topics</span></span>


[<span data-ttu-id="1bc68-200">Настройка параметров виртуальной машины для рабочей области MED-V</span><span class="sxs-lookup"><span data-stu-id="1bc68-200">How to Configure the Virtual Machine Setup for a MED-V Workspace</span></span>](how-to-configure-the-virtual-machine-setup-for-a-med-v-workspacemedvv2.md)

[<span data-ttu-id="1bc68-201">Настройка свойств шаблона имени компьютера виртуальной машины</span><span class="sxs-lookup"><span data-stu-id="1bc68-201">How to Configure VM Computer Name Pattern Properties</span></span>](how-to-configure-vm-computer-name-pattern-propertiesmedvv2.md)

 

 






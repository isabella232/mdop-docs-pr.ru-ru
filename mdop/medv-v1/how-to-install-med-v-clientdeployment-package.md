---
title: Установка клиента MED-V
description: Установка клиента MED-V
author: dansimp
ms.assetid: bfac6de7-d96d-4b3e-bd8b-183e051e53c8
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: b2e4468b15c0c196bf605b1b5d129ab38678ec74
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10827192"
---
# <span data-ttu-id="b552f-103">Установка клиента MED-V</span><span class="sxs-lookup"><span data-stu-id="b552f-103">How to Install MED-V Client</span></span>


<span data-ttu-id="b552f-104">В сценарии, основанном на пакете развертывания, установка клиента MED-V входит в пакет развертывания и устанавливается непосредственно из пакета.</span><span class="sxs-lookup"><span data-stu-id="b552f-104">In a deployment package-based scenario, the MED-V client installation is included in the deployment package and installed directly from the package.</span></span>

**<span data-ttu-id="b552f-105">Важно.</span><span class="sxs-lookup"><span data-stu-id="b552f-105">Important</span></span>**  
<span data-ttu-id="b552f-106">При использовании пакета развертывания, не включающего изображение, убедитесь, что изображение загружено в веб-сайт или помещается в папку предварительной подготовки перед установкой пакета развертывания.</span><span class="sxs-lookup"><span data-stu-id="b552f-106">When using a deployment package that does not include an image, ensure that the image is uploaded to the Web or pushed to the pre-stage folder prior to installing the deployment package.</span></span>



**<span data-ttu-id="b552f-107">Установка пакета развертывания</span><span class="sxs-lookup"><span data-stu-id="b552f-107">To install a deployment package</span></span>**

1.  <span data-ttu-id="b552f-108">Выполните одно из следующих действий.</span><span class="sxs-lookup"><span data-stu-id="b552f-108">Do one of the following:</span></span>

    -   <span data-ttu-id="b552f-109">Скачайте пакет MED-V из Интернета.</span><span class="sxs-lookup"><span data-stu-id="b552f-109">Download the MED-V package from the Web.</span></span>

    -   <span data-ttu-id="b552f-110">Вставьте USB-или DVD-диск в развертывание на несущем устройстве.</span><span class="sxs-lookup"><span data-stu-id="b552f-110">Insert the deployment USB or DVD into the host drive.</span></span>

2.  <span data-ttu-id="b552f-111">Если MED-V не запускается автоматически, дважды щелкните MED-VAutoInstaller.exe.</span><span class="sxs-lookup"><span data-stu-id="b552f-111">If MED-V does not launch automatically, double-click MED-VAutoInstaller.exe.</span></span>

    <span data-ttu-id="b552f-112">Откроется диалоговое окно со списком компонентов, которые уже установлены и которые в данный момент устанавливаются.</span><span class="sxs-lookup"><span data-stu-id="b552f-112">A dialog box appears listing the components that are already installed and those that are currently being installed.</span></span>

    **<span data-ttu-id="b552f-113">Примечание.</span><span class="sxs-lookup"><span data-stu-id="b552f-113">Note</span></span>**  
    <span data-ttu-id="b552f-114">Если на главном компьютере установлена неподдерживаемая версия Microsoft Virtual PC, появится сообщение о том, что вы удалите существующую версию и снова запустите установщик.</span><span class="sxs-lookup"><span data-stu-id="b552f-114">If a version of the Microsoft Virtual PC that is not supported exists on the host computer, a message will appear telling you to uninstall the existing version and run the installer again.</span></span>



~~~
**Note**  
If an older version of the MED-V client exists, it will prompt you asking whether you want to upgrade.



Depending on the components that have been installed, you might need to reboot. If rebooting is necessary, a message appears notifying you that you must reboot.
~~~

3. <span data-ttu-id="b552f-115">При необходимости перезагрузите компьютер.</span><span class="sxs-lookup"><span data-stu-id="b552f-115">If necessary, reboot the computer.</span></span>

   <span data-ttu-id="b552f-116">После завершения установки MED-V запустится и появится сообщение о том, что установка завершена.</span><span class="sxs-lookup"><span data-stu-id="b552f-116">When the installation is complete, MED-V starts and a message appears notifying you that the installation is complete.</span></span>

4. <span data-ttu-id="b552f-117">Войдите в MED-V, используя следующие имя пользователя и пароль:</span><span class="sxs-lookup"><span data-stu-id="b552f-117">Log in to MED-V using the following user name and password:</span></span>

   -   <span data-ttu-id="b552f-118">Введите имя домена и имя пользователя, а затем пароль пользователя домена, которому разрешено работать с MED-V.</span><span class="sxs-lookup"><span data-stu-id="b552f-118">Type in the domain name and user name followed by the password of the domain user who is permitted to work with MED-V.</span></span>

       <span data-ttu-id="b552f-119">Пример: "Domain \ _name \\user\ _name", "Password"</span><span class="sxs-lookup"><span data-stu-id="b552f-119">Example: "domain\_name\\user\_name", "password"</span></span>

## <span data-ttu-id="b552f-120">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="b552f-120">Related topics</span></span>


[<span data-ttu-id="b552f-121">Настройка пакета развертывания</span><span class="sxs-lookup"><span data-stu-id="b552f-121">How to Configure a Deployment Package</span></span>](how-to-configure-a-deployment-package.md)

[<span data-ttu-id="b552f-122">Отправка образа MED-V на сервер</span><span class="sxs-lookup"><span data-stu-id="b552f-122">How to Upload a MED-V Image to the Server</span></span>](how-to-upload-a-med-v-image-to-the-server.md)

[<span data-ttu-id="b552f-123">Справочник по командной строке установки клиента</span><span class="sxs-lookup"><span data-stu-id="b552f-123">Client Installation Command Line Reference</span></span>](client-installation-command-line-reference.md)










---
title: Настройка MED-V для удаленных сетей
description: Настройка MED-V для удаленных сетей
author: dansimp
ms.assetid: 4d2f0081-622f-4a6f-8d73-f8c2108036e0
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 328376046ee5213f3d5bb09be7adf8c81f8508b1
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10826722"
---
# <span data-ttu-id="9696e-103">Настройка MED-V для удаленных сетей</span><span class="sxs-lookup"><span data-stu-id="9696e-103">Configuring MED-V for Remote Networks</span></span>


<span data-ttu-id="9696e-104">Вы можете настроить MED-V для работы в сети, удаленно или одновременно из нее и удаленно.</span><span class="sxs-lookup"><span data-stu-id="9696e-104">You can configure MED-V to work from inside a network, remotely, or both from inside the network and remotely.</span></span>

## <a href="" id="bkmk-howtoconfiguremedvtoworkfrominsideanetworkorremotely"></a>


**<span data-ttu-id="9696e-105">Настройка MED-V для работы в сети</span><span class="sxs-lookup"><span data-stu-id="9696e-105">To configure MED-V to work from inside a network</span></span>**

-   <span data-ttu-id="9696e-106">Настройте сервер MED-V и распространение изображений в сети.</span><span class="sxs-lookup"><span data-stu-id="9696e-106">Configure a MED-V server and image distribution inside the network.</span></span>

**<span data-ttu-id="9696e-107">Настройка MED-V для работы с удаленным подключением</span><span class="sxs-lookup"><span data-stu-id="9696e-107">To configure MED-V to work remotely</span></span>**

1.  <span data-ttu-id="9696e-108">Настройка сервера MED-V и сервера распространения изображений, доступ к которому осуществляется через Интернет.</span><span class="sxs-lookup"><span data-stu-id="9696e-108">Configure a MED-V server and an image distribution server that are accessible from the Internet.</span></span>

2.  <span data-ttu-id="9696e-109">При необходимости настройте промежуточную сеть (также называемую демилитаризованной зоной) в качестве обратного прокси-сервера.</span><span class="sxs-lookup"><span data-stu-id="9696e-109">If needed, configure a perimeter network (also called a DMZ) reverse proxy.</span></span>

3.  <span data-ttu-id="9696e-110">Задайте способ проверки подлинности в файле *ClientSettings.xml* , который можно найти в папке **Server\\ Servers\\Configuration** .</span><span class="sxs-lookup"><span data-stu-id="9696e-110">Set the authentication method, in the *ClientSettings.xml* file, which can be found in the **Servers\\Configuration Server\\** folder.</span></span>

**<span data-ttu-id="9696e-111">Настройка MED-V для работы в сети и удаленно</span><span class="sxs-lookup"><span data-stu-id="9696e-111">To configure MED-V to work both from inside a network and remotely</span></span>**

1.  <span data-ttu-id="9696e-112">Настройте сервер MED-V и сервер распространения изображений в сети.</span><span class="sxs-lookup"><span data-stu-id="9696e-112">Configure a MED-V server and image distribution server inside the network.</span></span>

2.  <span data-ttu-id="9696e-113">Убедитесь, что серверы доступны через Интернет.</span><span class="sxs-lookup"><span data-stu-id="9696e-113">Ensure that the servers are accessible from the Internet.</span></span>

3.  <span data-ttu-id="9696e-114">Настройте разрешение DNS таким образом, чтобы при попытке клиента подключиться к серверу он автоматически подключается к нужному серверу (в сети или через Интернет) в зависимости от расположения клиента.</span><span class="sxs-lookup"><span data-stu-id="9696e-114">Configure the DNS resolution so that when the client attempts to connect to a server, it automatically connects to the correct server (within the network or over the Internet) based on the client location.</span></span>

4.  <span data-ttu-id="9696e-115">При необходимости настройте обратный прокси для пограничной сети.</span><span class="sxs-lookup"><span data-stu-id="9696e-115">If needed, configure a perimeter network reverse proxy.</span></span>

5.  <span data-ttu-id="9696e-116">Задайте способ проверки подлинности в файле *ClientSettings.xml* , который можно найти в папке **Server\\ Servers\\Configuration** .</span><span class="sxs-lookup"><span data-stu-id="9696e-116">Set the authentication method, in the *ClientSettings.xml* file, which can be found in the **Servers\\Configuration Server\\** folder.</span></span>

<span data-ttu-id="9696e-117">**Примечание**  При применении новых параметров службу необходимо перезапустить.</span><span class="sxs-lookup"><span data-stu-id="9696e-117">**Note** When applying new settings, the service must be restarted.</span></span>

 

-   <span data-ttu-id="9696e-118">Вы можете изменить схему проверки подлинности IIS одним из следующих способов: BASIC, DIGEST, NTLM или NEGOTIATE.</span><span class="sxs-lookup"><span data-stu-id="9696e-118">You can change the IIS authentication scheme to one of the following: BASIC, DIGEST, NTLM, or NEGOTIATE.</span></span> <span data-ttu-id="9696e-119">По умолчанию используется значение NEGOTIATE и используется следующая запись:</span><span class="sxs-lookup"><span data-stu-id="9696e-119">The default is NEGOTIATE and uses the following entry:</span></span>

    ```xml
    <ImageDistribution>
    <!-- The authentication used for image download. Basic and digest authentication should be used only under SSL.-->
       <!-- The line below can be one of the following: -->
       <!--BG_AUTH_SCHEME>BG_AUTH_SCHEME_BASIC</BG_AUTH_SCHEME-->
       <!--BG_AUTH_SCHEME>BG_AUTH_SCHEME_DIGEST</BG_AUTH_SCHEME-->
       <!--BG_AUTH_SCHEME>BG_AUTH_SCHEME_NTLM</BG_AUTH_SCHEME-->
       <!--BG_AUTH_SCHEME>BG_AUTH_SCHEME_NEGOTIATE</BG_AUTH_SCHEME-->
       <Authentication type="Kidaro.Foundation.Bits.BG_AUTH_SCHEME">
          <BG_AUTH_SCHEME>BG_AUTH_SCHEME_NEGOTIATE</BG_AUTH_SCHEME>
       </Authentication>
    </ImageDistribution>
    ```

## <span data-ttu-id="9696e-120">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="9696e-120">Related topics</span></span>


[<span data-ttu-id="9696e-121">Планирование и проектирование инфраструктуры MED-V</span><span class="sxs-lookup"><span data-stu-id="9696e-121">MED-V Infrastructure Planning and Design</span></span>](med-v-infrastructure-planning-and-design.md)

 

 






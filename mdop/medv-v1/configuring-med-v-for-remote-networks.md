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
# Настройка MED-V для удаленных сетей


Вы можете настроить MED-V для работы в сети, удаленно или одновременно из нее и удаленно.

## <a href="" id="bkmk-howtoconfiguremedvtoworkfrominsideanetworkorremotely"></a>


**Настройка MED-V для работы в сети**

-   Настройте сервер MED-V и распространение изображений в сети.

**Настройка MED-V для работы с удаленным подключением**

1.  Настройка сервера MED-V и сервера распространения изображений, доступ к которому осуществляется через Интернет.

2.  При необходимости настройте промежуточную сеть (также называемую демилитаризованной зоной) в качестве обратного прокси-сервера.

3.  Задайте способ проверки подлинности в файле *ClientSettings.xml* , который можно найти в папке **Server\\ Servers\\Configuration** .

**Настройка MED-V для работы в сети и удаленно**

1.  Настройте сервер MED-V и сервер распространения изображений в сети.

2.  Убедитесь, что серверы доступны через Интернет.

3.  Настройте разрешение DNS таким образом, чтобы при попытке клиента подключиться к серверу он автоматически подключается к нужному серверу (в сети или через Интернет) в зависимости от расположения клиента.

4.  При необходимости настройте обратный прокси для пограничной сети.

5.  Задайте способ проверки подлинности в файле *ClientSettings.xml* , который можно найти в папке **Server\\ Servers\\Configuration** .

**Примечание**  При применении новых параметров службу необходимо перезапустить.

 

-   Вы можете изменить схему проверки подлинности IIS одним из следующих способов: BASIC, DIGEST, NTLM или NEGOTIATE. По умолчанию используется значение NEGOTIATE и используется следующая запись:

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

## Статьи по теме


[Планирование и проектирование инфраструктуры MED-V](med-v-infrastructure-planning-and-design.md)

 

 






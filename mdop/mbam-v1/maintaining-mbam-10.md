---
title: Обслуживание MBAM 1.0
description: Обслуживание MBAM 1.0
author: dansimp
ms.assetid: 02ffb093-c364-4837-bbe8-23d4c09fbd3d
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 7eecef4e82680b08fde1b1bef88487a6fc156fe4
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10825772"
---
# <span data-ttu-id="34cc7-103">Обслуживание MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="34cc7-103">Maintaining MBAM 1.0</span></span>


<span data-ttu-id="34cc7-104">После того как вы закончите все необходимое планирование, а затем развернуть администрирование и мониторинг Microsoft BitLocker (MBAM), вы можете настроить MBAM для работы в высокодоступном режиме, а затем использовать его для управления операциями шифрования в корпоративной среде BitLocker.</span><span class="sxs-lookup"><span data-stu-id="34cc7-104">After you complete all the necessary planning and then deploy Microsoft BitLocker Administration and Monitoring (MBAM), you can configure MBAM to run in a highly available fashion while using it to manage enterprise BitLocker encryption operations.</span></span> <span data-ttu-id="34cc7-105">В этом разделе описаны параметры высокой доступности MBAM, а также способы перемещения функций сервера MBAM при необходимости.</span><span class="sxs-lookup"><span data-stu-id="34cc7-105">The information in this section describes high availability options for MBAM, as well as how to move MBAM Server features if necessary.</span></span>

## <span data-ttu-id="34cc7-106">Пакет управления MBAM</span><span class="sxs-lookup"><span data-stu-id="34cc7-106">MBAM Management Pack</span></span>


<span data-ttu-id="34cc7-107">Пакет управления MicrosoftSystemCenterOperationsManager для MBAM доступен для загрузки в центре загрузки Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="34cc7-107">The MicrosoftSystemCenterOperationsManager Management Pack for MBAM is available for download from the Microsoft Download Center.</span></span>

<span data-ttu-id="34cc7-108">Этот пакет управления отслеживает критические взаимодействия в серверной инфраструктуре, например соединения между веб-службами и базами данных, а также операционные вызовы между сайтами и поддержкой веб-службы.</span><span class="sxs-lookup"><span data-stu-id="34cc7-108">This management pack monitors the critical interactions in the server-side infrastructure, such as the connections between the web services and databases and the operational calls between websites and their supportive web service.</span></span> <span data-ttu-id="34cc7-109">Кроме того, он отправляет запросы между настольными клиентами и соответствующими конечными точками веб-служб.</span><span class="sxs-lookup"><span data-stu-id="34cc7-109">It also uploads the requests between desktop clients and their respective receiving web service endpoints.</span></span>

[<span data-ttu-id="34cc7-110">Пакет управления для администрирования и мониторинга Microsoft BitLocker</span><span class="sxs-lookup"><span data-stu-id="34cc7-110">Microsoft BitLocker Administration And Monitoring Management Pack</span></span>](https://go.microsoft.com/fwlink/p/?LinkId=258390)

## <span data-ttu-id="34cc7-111">Обеспечение высокой доступности для MBAM 1,0</span><span class="sxs-lookup"><span data-stu-id="34cc7-111">Ensure high availability for MBAM 1.0</span></span>


<span data-ttu-id="34cc7-112">MBAM разработана для обеспечения отказоустойчивости.</span><span class="sxs-lookup"><span data-stu-id="34cc7-112">MBAM is designed to be fault-tolerant.</span></span> <span data-ttu-id="34cc7-113">Если сервер становится недоступен, пользователи не должны иметь негативных изменений.</span><span class="sxs-lookup"><span data-stu-id="34cc7-113">If a server becomes unavailable, the users should not be negatively affected.</span></span> <span data-ttu-id="34cc7-114">Данные в этом разделе можно использовать для настройки установки MBAM с высокой доступностью.</span><span class="sxs-lookup"><span data-stu-id="34cc7-114">The information in this section can be used to configure a highly available MBAM installation.</span></span>

[<span data-ttu-id="34cc7-115">Высокая доступность для MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="34cc7-115">High Availability for MBAM 1.0</span></span>](high-availability-for-mbam-10.md)

## <span data-ttu-id="34cc7-116">Перемещение функций 1,0 MBAM на другой сервер</span><span class="sxs-lookup"><span data-stu-id="34cc7-116">Move MBAM 1.0 features to another server</span></span>


<span data-ttu-id="34cc7-117">Если вам нужно переместить компонент сервера MBAM на другой компьютер, необходимо выполнить определенные действия, чтобы избежать потери производительности или данных.</span><span class="sxs-lookup"><span data-stu-id="34cc7-117">When you need to move an MBAM Server feature from one server computer to another, there is a specific order and required steps that you should follow to avoid loss of productivity or data.</span></span> <span data-ttu-id="34cc7-118">В этом разделе описаны действия, которые необходимо выполнить, чтобы переместить один или несколько функций сервера MBAM на другой компьютер.</span><span class="sxs-lookup"><span data-stu-id="34cc7-118">This section describes the steps that you should take to move one or more MBAM Server features to a different computer.</span></span>

[<span data-ttu-id="34cc7-119">Перемещение компонентов MBAM 1.0 на другой компьютер</span><span class="sxs-lookup"><span data-stu-id="34cc7-119">How to Move MBAM 1.0 Features to Another Computer</span></span>](how-to-move-mbam-10-features-to-another-computer.md)

## <span data-ttu-id="34cc7-120">Другие ресурсы для обслуживания MBAM</span><span class="sxs-lookup"><span data-stu-id="34cc7-120">Other resources for maintaining MBAM</span></span>


[<span data-ttu-id="34cc7-121">Операции MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="34cc7-121">Operations for MBAM 1.0</span></span>](operations-for-mbam-10.md)

 

 






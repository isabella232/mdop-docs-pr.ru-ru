---
title: Высокоуровневая архитектура
description: Высокоуровневая архитектура
author: dansimp
ms.assetid: a78e12ad-5aa6-40e0-ae8b-51acaf005712
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 00df29c751653645ab4bee9762af57576a40092a
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10826202"
---
# <span data-ttu-id="0eeb6-103">Высокоуровневая архитектура</span><span class="sxs-lookup"><span data-stu-id="0eeb6-103">High-Level Architecture</span></span>


<span data-ttu-id="0eeb6-104">Решение MED-V состоит из следующих элементов:</span><span class="sxs-lookup"><span data-stu-id="0eeb6-104">The MED-V solution comprises the following elements:</span></span>

-   <span data-ttu-id="0eeb6-105">**Виртуальная машина, определенная администратором**— инкапсулирует среду полного рабочего стола, в том числе операционную систему, приложения и дополнительные средства управления и безопасности.</span><span class="sxs-lookup"><span data-stu-id="0eeb6-105">**Administrator-defined virtual machine**—Encapsulates a full desktop environment, including an operating system, applications, and optional management and security tools.</span></span>

-   <span data-ttu-id="0eeb6-106">**Репозиторий изображений**— хранит все виртуальные образы на стандартном сервере IIS и включает виртуальные образы, получение данных, прошедших проверку подлинности клиента, и эффективную загрузку (нового образа или обновления) с помощью технологии передачи обрезки.</span><span class="sxs-lookup"><span data-stu-id="0eeb6-106">**Image repository**—Stores all virtual images on a standard IIS server and enables virtual images version management, client-authenticated image retrieval, and efficient download (of a new image or updates) via Trim Transfer technology.</span></span>

-   <span data-ttu-id="0eeb6-107">**Сервер управления**— связывает виртуальные образы из репозитория образов вместе с политиками использования администратора в Active Directory® пользователей или групп.</span><span class="sxs-lookup"><span data-stu-id="0eeb6-107">**Management server**—Associates virtual images from the image repository along with administrator usage policies to Active Directory® users or groups.</span></span> <span data-ttu-id="0eeb6-108">Сервер управления также объединяет события клиентов и сохраняет их во внешней базе данных (Microsoft SQL Server®) для мониторинга и создания отчетов.</span><span class="sxs-lookup"><span data-stu-id="0eeb6-108">The management server also aggregates clients' events and stores them in an external database (Microsoft SQL Server®) for monitoring and reporting purposes.</span></span>

-   <span data-ttu-id="0eeb6-109">**Консоль управления**— позволяет администраторам управлять сервером управления и хранилищем изображений.</span><span class="sxs-lookup"><span data-stu-id="0eeb6-109">**Management console**—Enables administrators to control the management server and the image repository.</span></span>

-   **<span data-ttu-id="0eeb6-110">Клиент для конечных пользователей</span><span class="sxs-lookup"><span data-stu-id="0eeb6-110">End-user client</span></span>**

    1.  <span data-ttu-id="0eeb6-111">Жизненный цикл виртуальных изображений — проверка подлинности, получение изображений, принудительное использование политик использования.</span><span class="sxs-lookup"><span data-stu-id="0eeb6-111">Virtual image life-cycle—Authentication, image retrieval, enforcement of usage policies.</span></span>

    2.  <span data-ttu-id="0eeb6-112">Управление сеансами виртуальной машины — запуск, остановка и блокировка виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="0eeb6-112">Virtual machine session management—Start, stop, lock the virtual machine.</span></span>

    3.  <span data-ttu-id="0eeb6-113">Возможности единого рабочего стола — приложения, установленные на виртуальной машине, легко доступны через стандартное меню "Пуск" в классическом виде и интегрируются с другими приложениями в рабочем столе пользователя.</span><span class="sxs-lookup"><span data-stu-id="0eeb6-113">Single desktop experience—Applications installed in the virtual machine seamlessly available through the standard desktop Start menu and integrated with other applications on the user desktop.</span></span>

<span data-ttu-id="0eeb6-114">Весь обмен данными между клиентом и серверами (сервер управления и репозиторий изображений) выполняется в верхней части стандартного канала HTTP или HTTPS.</span><span class="sxs-lookup"><span data-stu-id="0eeb6-114">All communication between the client and the servers (management server and image repository) is carried on top of a standard HTTP or HTTPS channel.</span></span>

![](images/506f54d0-38fa-446a-8070-17ae26da5355.gif)

 

 






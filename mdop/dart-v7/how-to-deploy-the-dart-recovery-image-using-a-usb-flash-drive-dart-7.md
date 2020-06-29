---
title: Развертывание образа для восстановления DaRT с помощью USB-устройства флэш-памяти
description: Развертывание образа для восстановления DaRT с помощью USB-устройства флэш-памяти
author: dansimp
ms.assetid: 5b7aa843-731e-47e7-b5f9-48d08da732d6
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 1228c9cb5f870162f285d726d48721dde1185107
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10823669"
---
# <span data-ttu-id="45f80-103">Развертывание образа для восстановления DaRT с помощью USB-устройства флэш-памяти</span><span class="sxs-lookup"><span data-stu-id="45f80-103">How to Deploy the DaRT Recovery Image Using a USB Flash Drive</span></span>


<span data-ttu-id="45f80-104">После того как вы закончите работу **мастера переноса изображений**с помощью DaRT, вы можете <https://go.microsoft.com/fwlink/?LinkId=218888> скопировать файл образа ISO на USB-накопитель (UFD).</span><span class="sxs-lookup"><span data-stu-id="45f80-104">After you have finished running the **DaRT Recovery Image Wizard**, you can use the tool at <https://go.microsoft.com/fwlink/?LinkId=218888> to copy the ISO image file to a USB flash drive (UFD).</span></span>

<span data-ttu-id="45f80-105">Вы также можете вручную скопировать файл образа ISO на устройство флэш-памяти, выполнив действия, описанные в этом разделе.</span><span class="sxs-lookup"><span data-stu-id="45f80-105">You can also manually copy the ISO image file to a UFD by following the steps provided in this section.</span></span>

**<span data-ttu-id="45f80-106">Сохранение изображения для восстановления DaRT на USB-накопителе</span><span class="sxs-lookup"><span data-stu-id="45f80-106">To save the DaRT recovery image to a USB flash drive</span></span>**

1.  <span data-ttu-id="45f80-107">Отформатируйте USB-накопитель.</span><span class="sxs-lookup"><span data-stu-id="45f80-107">Format the USB flash drive.</span></span>

    1.  <span data-ttu-id="45f80-108">Вставьте флэш-память из работающей действующей операционной системы или сеанса WindowsPE.</span><span class="sxs-lookup"><span data-stu-id="45f80-108">From a running valid operating system or WindowsPE session, insert your UFD.</span></span>

    2.  <span data-ttu-id="45f80-109">В командной строке с разрешениями администратора введите **DiskPart** и введите **List Disk**.</span><span class="sxs-lookup"><span data-stu-id="45f80-109">At the command prompt with administrator permissions, type **DISKPART** and then type **LIST DISK**.</span></span>

        <span data-ttu-id="45f80-110">В окне командной строки отображается номер диска USB, например **диск 1**.</span><span class="sxs-lookup"><span data-stu-id="45f80-110">The Command Prompt window displays the disk number of your UFD, for example **DISK 1**.</span></span>

    3.  <span data-ttu-id="45f80-111">Введите в командной строке одну из следующих команд.</span><span class="sxs-lookup"><span data-stu-id="45f80-111">Enter the following commands one at a time at the command prompt.</span></span>

        ``` syntax
        SELECT DISK 1
        CLEAN
        CREATE PARTITION PRIMARY
        SELECT PARTITION 1
        ACTIVE
        FORMAT FS=NTFS
        ASSIGN
        EXIT
        ```

        <span data-ttu-id="45f80-112">**Примечание**  В предыдущем примере кода предполагается, что disk1 является USB-накопителем.</span><span class="sxs-lookup"><span data-stu-id="45f80-112">**Note** The previous code example assumes Disk1 is the UFD.</span></span> <span data-ttu-id="45f80-113">При необходимости замените диск 1 номером диска.</span><span class="sxs-lookup"><span data-stu-id="45f80-113">If it is necessary, replace DISK 1 with your disk number.</span></span>

         

2.  <span data-ttu-id="45f80-114">Используя предпочтительный способ подключения образа для компании, подключите его к файлу образа ISO, созданному в диалоговом окне **Создание образа для запуска** **мастера подготовки изображений для восстановления**с помощью DaRT.</span><span class="sxs-lookup"><span data-stu-id="45f80-114">By using your company’s preferred method of mounting an image, mount the ISO image file that you created in the **Create Startup Image** dialog box of the **DaRT Recovery Image Wizard**.</span></span> <span data-ttu-id="45f80-115">Для этого требуется метод, который можно использовать для подключения файла изображения.</span><span class="sxs-lookup"><span data-stu-id="45f80-115">This requires that you have a method available to mount an image file.</span></span>

3.  <span data-ttu-id="45f80-116">Откройте подключенный файл образа ISO и скопируйте все его содержимое в отформатированный USB-накопитель.</span><span class="sxs-lookup"><span data-stu-id="45f80-116">Open the mounted ISO image file and copy all its contents to the formatted USB flash drive.</span></span>

    <span data-ttu-id="45f80-117">**Примечание**  Если вы записываюте компакт-диск или DVD-диск в образ восстановления, вы можете открыть файлы на нем с компакт-диска или DVD-диска и скопировать содержимое на устройство UFD.</span><span class="sxs-lookup"><span data-stu-id="45f80-117">**Note** If you burned a CD or DVD of the recovery image, you can open the files on the CD or DVD and copy the contents to the UFD.</span></span> <span data-ttu-id="45f80-118">Это позволяет пропустить необходимость монтировать образ.</span><span class="sxs-lookup"><span data-stu-id="45f80-118">This lets you skip the need to mount the image.</span></span>

     

## <span data-ttu-id="45f80-119">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="45f80-119">Related topics</span></span>


[<span data-ttu-id="45f80-120">Развертывание образа для восстановления DaRT 7.0</span><span class="sxs-lookup"><span data-stu-id="45f80-120">Deploying the DaRT 7.0 Recovery Image</span></span>](deploying-the-dart-70-recovery-image-dart-7.md)

 

 






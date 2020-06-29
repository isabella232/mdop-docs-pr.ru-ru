---
title: Настройка промежуточного размещения образа
description: Настройка промежуточного размещения образа
author: dansimp
ms.assetid: 92781b5a-208f-45a4-a078-ee90cf9efd9d
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 38ddb7a69845aa4dbcb9cbd16b84dedc04438732
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10826409"
---
# Настройка промежуточного размещения образа


**Примечание**  Предварительный тест для образа полезен только для начальной загрузки изображения. Оно не поддерживается для обновления изображений.

 

## Настройка промежуточного размещения образа


**Настройка предварительного размещения изображений**

1.  На клиентском компьютере в папке хранилища изображений создайте папку для предварительного промежуточного изображения и назовите его *Images MED-V*.

    **Примечание**  Эта папка должна называться *изображениями MED-V*.

     

2.  В папке Images MED-V создайте вложенную папку и назовите ее *PrestagedImages*.

    **Примечание**  Эта папка должна называться *PrestagedImages*.

     

3.  Чтобы применить безопасность списков управления доступом (ACL) к папке *изображений MED-V* , установите следующий список ACL:

    **Пользователи NT AUTHORITY\\Authenticated: (OI) (CI) (Специальный доступ:)**

                                             **READ\_CONTROL**

                                    **SYNCHRONIZE**

                                    **FILE\_GENERIC\_READ**

                                    **FILE\_READ\_DATA**

    **                                 ФАЙЛ \ _APPEND \ _DATA**

                                    **FILE\_READ\_EA**

                                    **FILE\_READ\_ATTRIBUTES**

    **NT AUTHORITY\\SYSTEM: (OI) F**

    **BUILTIN\\Administrators: (OI) (CI) F**

    **Примечание**  Рекомендуется применять безопасность ACL к папке *изображений MED-V* .

     

4.  Чтобы применить безопасность ACL к папке *PrestagedImages* , установите следующий список ACL:

    **Пользователи NT AUTHORITY\\Authenticated: (OI) (CI) (Специальный доступ:)**

    **ЧТЕНИЕ \ _CONTROL**

    **СИНХРОНИЗАТОРОМ**

    **ФАЙЛ \ _GENERIC \ _READ**

    **ФАЙЛ \ _READ \ _DATA**

    **ФАЙЛ \ _READ \ _EA**

    **ФАЙЛ \ _READ \ _ATTRIBUTES**

    **NT AUTHORITY\\SYSTEM: (OI) F**

    **BUILTIN\\Administrators: (OI) (CI) F**

    **Примечание**  Рекомендуется применять безопасность ACL к папке *PrestagedImages* .

     

5.  Помещает файлы изображений (CKM и ИНДЕКСные файлы) в папку *PrestagedImages* .

    **Примечание**  После того как файлы изображений будут помещены в папку, предшествующую этапам, рекомендуется выполнить проверку целостности данных и помечать их как файлы только для чтения.

     

6.  Включите следующий параметр в установку клиента MED-V: *Client.MSI VMSFOLDER = "C:\\MED-V Images"*.

## Как обновить расположение до этапа


**Обновление расположения для предварительного этапа**

1.  Раздел реестра *PrestagedImagesPath*указывает на расположение изображений по умолчанию. Она находится в следующей папке:

    -   На платформе x86 `KEY_LOCAL_MACHINE\SOFTWARE\Kidaro`

    -   На 64-разрядной версии `HKEY_LOCAL_MACHINE\SOFTWARE\WOW6432node`

2.  Если изображение находится в другом месте, измените путь.

 

 






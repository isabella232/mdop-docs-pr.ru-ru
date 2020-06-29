---
title: Применение ускорителя пакетов для создания виртуального пакета приложения (App-V 4,6 SP1)
description: Применение ускорителя пакетов для создания виртуального пакета приложения (App-V 4,6 SP1)
author: dansimp
ms.assetid: ca0bd514-2bbf-4130-8c77-98d991cbe016
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: ce6960fb95cce7f5e0eeb111412f27f945b0c1a5
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10821382"
---
# Применение ускорителя пакетов для создания виртуального пакета приложения (App-V 4,6 SP1)


Вы можете использовать акселераторы пакетов App-V для автоматического создания нового пакета виртуальных приложений. Дополнительные сведения о ускорителях пакетов смотрите в разделе [ускорители пакетов App-v (App-v 4,6 SP1)](about-app-v-package-accelerators--app-v-46-sp1-.md).

**Важно.**  
Заявление об отказе: Программа Application Virtualization Sequencer не предоставляет вам никаких прав лицензии на программное приложение, которое вы используете для создания ускорителя пакетов. Вы обязаны соблюдать все условия лицензии конечных пользователей для этого приложения. Ответственность за то, что условия лицензионного соглашения на использование программного обеспечения позволяют создать пакетный ускоритель с помощью Application Virtualization Sequencer.



**Примечание.**  
Прежде чем приступать к этой процедуре, скопируйте требуемый ускоритель пакетов локально на компьютер с секвенсором App-V. Кроме того, необходимо скопировать все необходимые файлы установки для пакета в локальный каталог на компьютере, на котором запущен секвенсор. Это каталог, который нужно задать в действии 5 этой процедуры.



Чтобы создать виртуальный пакет приложения с помощью ускорителя пакетов, выполните описанные ниже действия.

**Создание виртуального пакета приложения с помощью ускорителя пакетов App-V**

1. Чтобы запустить секвенсор App-v на компьютере, на котором работает секвенсор App-v, нажмите кнопку **запустить**  /  **все программы**  /  **Microsoft**Application Virtualization  /  **Sequencer Microsoft**Application Virtualization.

2. Чтобы запустить **Мастер создания пакета**, нажмите **создать новый виртуальный пакет приложения**. Чтобы создать пакет, установите флажок **создать пакет с помощью ускорителя пакетов** и нажмите кнопку **Далее**.

3. На странице **Выбор ускорителя пакетов** , чтобы указать ускоритель пакетов, который будет использоваться для создания нового виртуального пакета приложений, нажмите кнопку **Обзор** , чтобы найти ускоритель пакетов, который вы хотите использовать. Нажмите кнопку **Далее**.

   **Важно.**  
   Если издатель ускорителя пакетов не может пройти проверку и не содержит действительной цифровой подписи, в диалоговом окне **предупреждение системы безопасности** перед нажатием кнопки **выполнить**необходимо подтвердить, что вы доверяете источнику ускорителя пакетов.



4. На странице " **руководство** " Проверьте сведения о публикации, отображаемые в области сведений. Отображаемые сведения были добавлены при создании ускорителя пакетов и содержат сведения о создании и публикации пакета. Чтобы экспортировать сведения о руководстве в текстовый файл (txt), нажмите кнопку **Экспорт** и укажите расположение, в котором нужно сохранить файл, и нажмите кнопку **Далее**.

5. На странице " **Выбор установочных файлов** ", чтобы создать локальную папку, которая включает все необходимые файлы для установки пакета, щелкните **создать папку** и укажите, где следует сохранить папку. Кроме того, необходимо указать имя, которое будет назначаться папке. Затем необходимо скопировать все необходимые файлы установки в указанное вами расположение. Если папка, содержащая установочные файлы, уже есть на компьютере с секвенсором, нажмите кнопку **Обзор** , чтобы выбрать папку.

   Кроме того, если вы уже скопировали файлы установки в каталог на этом компьютере, щелкните **создать папку**, перейдите в папку, содержащую установочные файлы, и нажмите кнопку **Далее**.

   **Примечание.**  
   Вы можете указать следующие типы файлов, которые поддерживаются при установке:

   -   Файлы установщика Windows (**MSI** -файл)

   -   файлы. cab

   -   Сжатые файлы с расширением имени ZIP-файла

   -   Файлы реальных приложений

   Следующие типы файлов не поддерживаются: **MSP** и <strong> exe </strong> . Если указан **exe** файл, необходимо извлечь установочные файлы вручную.



~~~
If the Package Accelerator requires an application be installed prior to applying the Package Accelerator and you have installed the application, on the **Local Installation** page, select the check box **I have installed all applications**, and then click **Next**.
~~~

6. На странице **имя пакета** укажите имя, которое будет сопоставлено с пакетом. Указанное имя идентифицирует пакет в консоли управления App-V. Нажмите кнопку **Далее**.

7. На странице " **Создание пакета** " Введите примечания, которые будут связаны с пакетом. Примечания должны содержать идентификационные данные о создаваемом пакете. Для подтверждения места создания пакета ознакомьтесь со сведениями, которые отображаются в папке для **сохранения**. Чтобы сжать пакет, выберите пункт **сжать пакет**. Установите флажок **сжимать пакет** , если пакет будет передаваться по сети или если размер пакета ПРЕВЫШАЕТ 4 ГБ.

   Чтобы создать пакет, нажмите кнопку **создать**. После создания пакета нажмите кнопку **Далее**.

8. На странице " **Настройка программного обеспечения** " для включения секвенсора для настройки приложений, содержащихся в пакете, выберите пункт " **Настройка программного обеспечения**". Этот шаг полезен для настройки связанных задач, которые должны быть выполнены для запуска приложения на конечных компьютерах, например для настройки каких – либо связанных лицензионных соглашений.

   Если выбрать параметр **настроить программное обеспечение**, то следующие элементы будут сконфигурированы секвенсором в рамках этого этапа:

   -   **Загрузить пакет**. Программа Sequencer загружает файлы, связанные с пакетом. Декодирование пакета может занять от нескольких секунд до часа.

   -   **Запустите каждую программу**. При необходимости запустите программы, содержащиеся в пакете. Этот шаг полезен для завершения задач, связанных с лицензией или конфигурацией, которые необходимы для запуска приложения перед развертыванием и запуском пакета на целевом компьютере. Чтобы запустить все программы за один раз, выберите хотя бы одну программу, а затем нажмите кнопку **выполнить все**. Чтобы запустить определенные программы, выберите программу или программы, которые вы хотите запустить, и нажмите кнопку **выполнить выбрано**. Заполните необходимые задачи настройки, а затем закройте приложения. Для запуска всех программ может потребоваться несколько минут. Нажмите кнопку **Далее**.

   -   **Сохранить пакет**. Секвенсор сохраняет пакет.

   -   **Основной блок функций**. Секвенсор оптимизирует пакет для потоковой передачи, перестраивая основной блок функций.

   Если вы не хотите настраивать приложения, нажмите **пропустить этот шаг**и перейдите к действию 9, а затем нажмите кнопку **Далее**.

9. На странице **завершения** после просмотра данных, отображаемых в области **отчета "виртуальный пакет приложения** ", нажмите кнопку **Закрыть**.

   Пакет теперь доступен в секвенсоре. Чтобы изменить свойства пакета, нажмите **изменить \ [имя пакета \]**. Дополнительные сведения об изменении пакета можно найти в разделе [как изменить существующий пакет виртуального приложения (App-V 4,6 SP1)](how-to-modify-an-existing-virtual-application-package--app-v-46-sp1-.md).

## Статьи по теме


[Настройка Application Virtualization Sequencer (App-V 4.6 с пакетом обновления 1 (SP1))](configuring-the-application-virtualization-sequencer--app-v-46-sp1-.md)

[Создание ускорителей пакетов App-V (App-V 4.6 с пакетом обновления 1 (SP1))](how-to-create-app-v-package-accelerators--app-v-46-sp1-.md)









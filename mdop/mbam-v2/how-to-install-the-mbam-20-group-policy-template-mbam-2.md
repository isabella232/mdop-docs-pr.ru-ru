---
title: Установка шаблона групповой политики MBAM 2.0
description: Установка шаблона групповой политики MBAM 2.0
author: dansimp
ms.assetid: bc193232-d060-4285-842e-d194a74dd3c9
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 6420fc4d499de05ed740b038b40aff6a9cd8a05f
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10826252"
---
# Установка шаблона групповой политики MBAM 2.0


В дополнение к серверам, связанным со средствами администрирования и мониторинга Microsoft BitLocker (MBAM), в приложение установки сервера входит шаблон групповой политики администрирования Microsoft BitLocker и наблюдения за ними. Этот шаблон можно установить на любом компьютере, на котором может выполняться консоль управления групповыми политиками (GPMC) или расширенное управление групповыми политиками.

Ниже описаны действия, которые необходимо выполнить, чтобы установить шаблон групповой политики MBAM.

**Примечание**  Убедитесь, что вы используете 32-разрядную настройку на 32-разрядных серверах и на 64-разрядной установке на 64-разрядных серверах.

 

**Установка шаблона групповой политики MBAM**

1.  На сервере, на котором вы хотите установить MBAM, запустите мастер установки MBAM, выпуская **MBAMSetup.exe** .

2.  На странице **приветствия** при необходимости выберите **программу улучшения качества программного**обеспечения, а затем нажмите кнопку **начать**.

3.  Прочтите и подтвердите условия лицензионного соглашения на использование программного обеспечения корпорации Майкрософт, а затем нажмите кнопку **Далее** , чтобы продолжить установку.

4.  По умолчанию для установки выбраны все функции администрирования и мониторинга Microsoft BitLocker. Удалите все параметры компонента за исключением **шаблона политики**, а затем нажмите кнопку **Далее** , чтобы продолжить установку.

    **Примечание**  Мастер установки проверяет предварительные требования для установки и выводит недостающие необходимые компоненты. Если все необходимые условия выполнены, установка будет продолжена. Если обнаружен отсутствующий предварительный компонент, необходимо устранить недостающие необходимые компоненты и нажать кнопку **проверить необходимые компоненты еще раз**. После того как все необходимые условия будут выполнены, установка будет возобновлена.

     

5.  Сведения о том, как и где устанавливать шаблоны, описаны в статье [Загрузка и развертывание шаблонов групповой политики для MDOP (ADMX)](https://technet.microsoft.com/library/dn659707.aspx).

6.  После того как мастер настройки администрирования и наблюдения Microsoft BitLocker отобразит страницы установки для выбранных функций, нажмите кнопку **Готово** , чтобы закрыть окно настройки MBAM.

## Статьи по теме


[Развертывание объектов групповой политики MBAM 2.0](deploying-mbam-20-group-policy-objects-mbam-2.md)

 

 





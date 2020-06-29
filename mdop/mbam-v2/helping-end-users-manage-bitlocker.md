---
title: Помощь конечным пользователям в управлении BitLocker
description: Помощь конечным пользователям в управлении BitLocker
author: dansimp
ms.assetid: 47776fb3-2d94-4970-b687-c35ec3dd6c64
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 26ef2bc33a75ff7773b75807ab0e10e5aa67b109
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10824779"
---
# Помощь конечным пользователям в управлении BitLocker


Содержимое потерянного или украденного компьютера уязвимо для несанкционированного доступа, что может представлять угрозу безопасности как для людей, так и для компаний. Администрирование и мониторинг Microsoft BitLocker (MBAM) использует BitLocker, чтобы предотвратить несанкционированный доступ, заблокируя компьютер, чтобы защитить конфиденциальные данные от вредоносных пользователей.

## Что такое BitLocker?


Шифрование диска BitLocker обеспечивает защиту дисков операционной системы, дисков данных и съемных носителей (например, USB-накопителей), шифруя диски. В зависимости от того, как настроена программа BitLocker, пользователям может потребоваться предоставить ключ (пароль или ПИН-код), чтобы разблокировать данные, хранящиеся на зашифрованных дисках.

При добавлении новых файлов на диск, зашифрованный с помощью BitLocker, BitLocker шифрует их автоматически. Файлы будут зашифрованы только в том случае, если они хранятся на зашифрованном диске. Файлы, которые копируются на другой диск или компьютер, расшифровываются. Если вы предоставляете общий доступ к файлам другим пользователям, например по сети, эти файлы шифруются при сохранении на зашифрованном диске, но доступ к ним можно получить с помощью уполномоченных пользователей.

Если вы зашифруете диск операционной системы, при запуске BitLocker проверяет его во время запуска, чтобы убедиться, что это может представлять угрозу безопасности (например, изменение BIOS или изменение любых файлов автозагрузки). Если обнаружена потенциальная угроза безопасности, BitLocker блокирует диск операционной системы и требует специального ключа восстановления BitLocker, чтобы разблокировать его. Убедитесь, что вы создали этот ключ восстановления при первом запуске BitLocker. В противном случае доступ к своим файлам будет потерян.

Если вы записываете данные на съемные диски (стационарные или сменные), вы можете разблокировать зашифрованный диск с помощью пароля или смарт-карты или настроить автоматическое снятие блокировки при входе в систему на компьютере.

В дополнение к паролям и контактам, BitLocker может использовать микросхему доверенного платформенного модуля (TPM), которая предоставляется на многих современных компьютерах. Микросхема TPM используется для того, чтобы убедиться в том, что компьютер не был подменен, пока BitLocker не заблокирует диск операционной системы. В процессе шифрования может потребоваться включить микросхему доверенного платформенного модуля. При запуске компьютера BitLocker запрашивает у доверенного платформенного модуля ключи на диск и разблокирует его. Для включения микросхемы TPM вам потребуется перезагрузить компьютер, а затем изменить параметры в BIOS (предварительно установленный уровень программного обеспечения компьютера). Дополнительные сведения о TPM можно найти в разделе [о микросхеме TPM компьютера](about-the-computer-tpm-chip.md).

После того как компьютер защищен BitLocker, вам может потребоваться ввести ПИН-код или пароль при каждом выходе компьютера из спящего режима или с самого начала. Если вы забыли свой ПИН-код или пароль, вы можете помочь службе поддержки компании или организации.

Вы можете отключать BitLocker, временно приостанавливать или постоянно, выполнив расшифровку диска.

**Примечание**  Поскольку BitLocker шифрует весь диск, а не только отдельные файлы, будьте внимательны при перемещении конфиденциальных данных между дисками. Если вы перемещаете файл с диска, защищенного BitLocker, на незашифрованный диск, он больше не будет зашифрован.

 

## О приложении параметров шифрования BitLocker


Чтобы разблокировать жесткие диски на компьютере, а также управлять PIN-кодом и паролями, используйте приложение параметров шифрования BitLocker на панели управления Windows, выполнив описанные ниже действия. Вы можете ввести пароли, чтобы разблокировать защищенные диски и проверить состояние BitLocker подключенных дисков с помощью этого приложения.

**Открытие приложения параметров шифрования BitLocker**

1.  Нажмите кнопку **Пуск**и выберите пункт **Панель управления**. Панель управления откроется в новом окне.

2.  На **панели управления**выберите элемент **система и безопасность**.

3.  Выберите **Параметры шифрования BitLocker** , чтобы открыть приложение параметров шифрования BitLocker.

    Описание доступных параметров можно найти в следующем разделе.

## Параметры в приложении параметров шифрования BitLocker


Приложение "параметры шифрования BitLocker" на панели управления позволяет управлять PIN-кодом и паролями, которые BitLocker использует для защиты компьютера.

**Шифрование диска BitLocker — несъемные диски:**

В этом разделе вы можете просмотреть сведения о жестких дисках, подключенных к компьютеру, а также о текущем состоянии шифрования BitLocker.

-   **Управление ПИН** -кодом — меняет ПИН-код, используемый BitLocker, для разблокировки диска операционной системы.

-   **Управление паролем** — изменяет пароль, который используется программой BitLocker для разблокировки других внутренних дисков.

**Шифрование диска BitLocker — внешние диски:**

В этом разделе вы можете просмотреть сведения о внешних дисках (например, USB-накопителе, подключенных к компьютеру) и о текущем состоянии шифрования BitLocker.

-   **Управление паролем** — изменяет пароль, который используется программой BitLocker для разблокировки других внутренних дисков.

**Дополнительно**

-   **Администрирование доверенного платформенного модуля** — открывает средство администрирования TPM в отдельном окне. Здесь вы можете настроить общие задачи TPM и получить сведения о наборе микросхем TPM. Чтобы получить доступ к этому средству, необходимо обладать правами администратора на вашем компьютере.

-   **Управление дисками** : Откройте средство управления дисками. Здесь вы можете просмотреть сведения обо всех жестких дисках, подключенных к компьютеру, и настроить разделы и параметры диска. Чтобы получить доступ к этому средству, необходимо иметь права администратора на вашем компьютере.

 

 





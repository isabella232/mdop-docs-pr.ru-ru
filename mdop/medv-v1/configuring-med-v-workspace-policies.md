---
title: Настройка политик рабочей области MED-V
description: Настройка политик рабочей области MED-V
author: dansimp
ms.assetid: 0eaed981-cbf3-4b16-a4b7-4705c5705dc7
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 84bdae38b1c801e2c2be2a3dd1d12dd2ca7d932d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10824859"
---
# Настройка политик рабочей области MED-V


Политика рабочей области MED-V — это группа настраиваемых параметров, определяющих способ выполнения виртуализированной среды и приложений на хост-компьютере. В этом разделе описаны все настраиваемые параметры в политике рабочей области для MED-V и параметры, влияющие на рабочую область MED-V.

Доступны следующие типы рабочих областей MED-V:

-   **Persistent**— в постоянной рабочей области MED-v все изменения и дополнения, внесенные пользователем в рабочую область MED-v, сохраняются в рабочей области MED-v между сеансами. Кроме того, постоянная рабочая область MED-V обычно используется в среде домена.

-   **Revertible**— в рабочей области Revertible med-v по завершении каждого сеанса (то есть при остановке рабочей области MED-v) при развертывании восстанавливается исходное состояние рабочей области MED-v. Изменения и дополнения, внесенные пользователем, сохраняются в рабочей области MED-V между сеансами. Рабочую область revertible MED-V нельзя использовать в среде домена.

Важно выбрать тип рабочей области MED-V, которую вы создаете, прежде чем развертывать рабочую область MED-V, так как не рекомендуется перенастраивать тип рабочей области MED-V после развертывания политики для пользователей.

**Примечание**  При настройке политики рядом с полями обязательных полей, которые не заполнены, появляется предупреждающий символ. Если обязательное поле не заполнено, на вкладке также отображается символ.

 

## В этом разделе


<a href="" id="how-to-apply-general-settings-to-a-med-v-workspace"></a>[Применение общих параметров к рабочей области MED-V](how-to-apply-general-settings-to-a-med-v-workspace.md)  
В этой статье описаны общие параметры рабочей области MED-V и способы их применения к политике.

<a href="" id="how-to-apply-virtual-machine-settings-to-a-med-v-workspace"></a>[Применение параметров виртуальной машины к рабочей области MED-V](how-to-apply-virtual-machine-settings-to-a-med-v-workspace.md)  
Описание параметров виртуальной машины для рабочей области MED-V и инструкции по его применению к политике.

<a href="" id="how-to-configure-a-domain-user-or-group"></a>[Настройка пользователя или группы домена](how-to-configure-a-domain-user-or-groupmedvv2.md)  
В этой статье описано, как настроить пользователей и группы домена.

<a href="" id="how-to-configure-published-applications"></a>[Настройка опубликованных приложений](how-to-configure-published-applicationsmedvv2.md)  
В этой статье описаны опубликованные приложения и меню, а также способы их применения к политике.

<a href="" id="how-to-configure-web-settings-for-a-med-v-workspace"></a>[Настройка веб-параметров для рабочей области MED-V](how-to-configure-web-settings-for-a-med-v-workspace.md)  
В этой статье описаны веб-параметры, доступные для рабочей области MED-V, и способы их применения к политике.

<a href="" id="how-to-configure-the-virtual-machine-setup-for-a-med-v-workspace"></a>[Настройка параметров виртуальной машины для рабочей области MED-V](how-to-configure-the-virtual-machine-setup-for-a-med-v-workspace.md)  
Описание настройки виртуальной машины для рабочей области MED-V и инструкции по ее применению к политике.

<a href="" id="how-to-apply-network-settings-to-a-med-v-workspace"></a>[Применение параметров сети к рабочей области MED-V](how-to-apply-network-settings-to-a-med-v-workspace.md)  
В этой статье описаны сетевые параметры рабочей области MED-V и способы их применения к политике.

<a href="" id="how-to-apply-performance-settings-to-a-med-v-workspace"></a>[Применение параметров производительности к рабочей области MED-V](how-to-apply-performance-settings-to-a-med-v-workspace.md)  
В этой статье описаны параметры производительности рабочей области MED-V и способы их применения к политике.

<a href="" id="how-to-import-and-export-a-policy"></a>[Импорт и экспорт политики](how-to-import-and-export-a-policy.md)  
Инструкции по импорту и экспорту политики.

 

 






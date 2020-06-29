---
title: Настройка балансировки сетевой нагрузки для MBAM
description: Настройка балансировки сетевой нагрузки для MBAM
author: dansimp
ms.assetid: df2208c3-352b-4a48-9722-237b0c8cd6a5
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: a04bc74a9dab7bfe18eed8e5a3c1b6ca64d88b5b
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10825512"
---
# Настройка балансировки сетевой нагрузки для MBAM


Чтобы убедиться в том, что требования к оборудованию и программному обеспечению, чтобы установить сервер администрирования и мониторинга, приведены в разделе Требования к [развертыванию MBAM 1,0](mbam-10-deployment-prerequisites.md) и [поддерживаемые конфигурации MBAM 1,0](mbam-10-supported-configurations.md).

**Примечание**  Чтобы получить файлы журнала установки, необходимо установить администрирование и мониторинг Microsoft BitLocker (MBAM) с помощью пакета **msiexec** и параметра **/l** &lt; Location &gt; . Файлы журнала создаются в указанном расположении.

Дополнительные файлы журнала установки создаются в папке% temp% пользователя, устанавливающего MBAM.

 

Кластеры балансировки сетевой нагрузки (NLB) для компонента администрирования и мониторинга сервера предоставляют масштабируемость в MBAM и поддерживает более 55 000 MBAM клиентских компьютеров.

**Примечание**  Балансировка сетевой нагрузки Windows Server распределяет запросы клиентов по набору серверов, которые настроены в едином кластере серверов. При установке компонента балансировки сетевой нагрузки на каждом сервере (узлах) в кластере кластер представляет виртуальный IP-адрес или полное доменное имя (FQDN) для клиентских запросов. Первоначальные запросы клиента поступают на все узлы в кластере, но только один узел принимает и обрабатывает запрос.

На всех компьютерах, которые будут входить в кластер NLB, необходимо выполнить указанные ниже требования.

-   Все компьютеры в кластере NLB должны находиться в одном домене.

-   Каждый компьютер в кластере NLB должен использовать статический IP-адрес.

-   Для каждого компьютера в NLB-кластере должно быть включено средство балансировки нагрузки сети.

-   Кластеру NLB требуется статический IP-адрес, а в системе доменных имен (DNS) должна быть вручную создана запись узла.

 

## Настройка балансировки нагрузки сети для серверов администрирования и мониторинга MBAM


Ниже описана процедура настройки виртуального имени кластера NLB и IP-адреса для двух серверов администрирования и мониторинга MBAM и настройки клиентов MBAM на использование кластера NLB.

Перед выполнением процедур, описанных в этой статье, необходимо установить компонент сервера администрирования и мониторинга MBAM с помощью той же привязки для порта IIS на двух разных серверных компьютерах, которые соответствуют требованиям для настройки компонентов сервера MBAM и NLB-кластеров.

**Примечание**  В этом разделе описан базовый процесс создания кластера NLB с помощью диспетчера балансировки сетевой нагрузки. Точные действия, которые необходимо выполнить для настройки сервера Windows как части NLB-кластера, зависят от используемой версии Windows Server. Дополнительные сведения о том, как создать NLBs на WindowsServer2008, можно найти в разделе [Создание кластеров балансировки нагрузки сети](https://go.microsoft.com/fwlink/?LinkId=197176) в библиотеке TechNet для Windows Server2008.

 

**Настройка виртуального имени кластера NLB и IP-адреса для двух серверов администрирования и мониторинга MBAM**

1.  Нажмите кнопку **Пуск**, выберите **все программы**, а затем — **Администрирование**, а затем — **Диспетчер балансировки сетевой нагрузки**.

    **Примечание**  Если диспетчер NLB отсутствует, вы можете установить его в качестве функции WindowsServer. Вы должны установить эту функцию на серверах администрирования и мониторинга MBAM, если вы хотите настроить ее в NLB-кластере.

     

2.  В строке меню нажмите кнопку **кластер**и выберите команду **создать** , чтобы открыть диалоговое окно **Параметры кластера** .

3.  В диалоговом окне **Параметры кластера** введите данные для IP-конфигурации кластера NLB.

    -   **IP-адрес:** IP-адрес кластера NLB, зарегистрированный в DNS

    -   **Маска подсети:** Маска подсети IP-адреса кластера NLB, зарегистрированная в DNS

    -   **Полное Интернет-имя:** Полное доменное имя кластера NLB, зарегистрированное в DNS

4.  Убедитесь в том, что **одноадресная рассылка** выбрана в **режиме работы кластера**, и нажмите кнопку **Далее**.

5.  На странице **IP-адреса кластера** нажмите кнопку **Далее**.

6.  На странице **правила для порта** нажмите кнопку **изменить** , чтобы определить порты, на которые будет отвечать кластер NLB, и настройте порты, которые используются для связи между клиентом и сервером, как они определены для сайта, или нажмите кнопку **Далее** , чтобы разрешить IP-адрес кластера NLB для ответа на все порты TCP/IP.

    **Примечание**  Убедитесь, что для **affinity** задано значение **Single**.

     

7.  На странице **Connect (подключение** ) введите имя узла MBAM администрирования и сервера мониторинга, которое будет входить в NLB-кластер на **узле**, и нажмите кнопку **подключить**.

8.  В разделе **интерфейсы, доступные для настройки нового кластера**выберите сетевой интерфейс, который будет настроен на взаимодействие с кластером NLB, и нажмите кнопку **Далее**.

9.  На странице **Параметры узла** просмотрите сведения о том, что **ВЫДЕЛЕННЫЕ параметры IP-конфигурации** выводят на экран специальную конфигурацию IP-адреса для нужного узла кластера NLB, убедитесь, что **первоначально задано**состояние узла **по умолчанию** , и нажмите кнопку **Готово**.

    **Примечание**  На странице **Параметры узла** также отображается приоритет узла NLB Clustered (от 1 до 32). Поскольку новые узлы добавляются в NLB-кластер, приоритет узла должен отличаться от ранее добавленных узлов. Приоритет автоматически увеличивается при использовании диспетчера балансировки сетевой нагрузки.

     

10. Щелкните ** &lt; имя &gt; кластера NLB** и убедитесь, **что перед** продолжением отображается **состояние** интерфейса узла NLB. На этом этапе может потребоваться обновить конфигурацию кластера NLB в качестве конфигурации TCP/IP узла, которая изменяется диспетчером NLB.

11. Чтобы добавить дополнительные узлы в NLB-кластер, щелкните правой кнопкой мыши ** &lt; &gt; имя кластера NLB**, выберите команду **Добавить узел к кластеру,** а затем повторите действия 7 – 10 для каждой системы сайта, которая будет частью кластера NLB.

12. На компьютере, на котором установлен шаблон групповой политики MBAM, измените параметры групповой политики MBAM, чтобы настроить конечные точки служб MBAM на использование имени кластера NLB и соответствующей привязки порта IIS для доступа к функциям сервера MBAM администрирования и мониторинга, установленным на компьютерах кластера NLB. Дополнительные сведения о том, как изменить параметры объекта групповой политики MBAM, можно найти [в разделе Изменение параметров GPO MBAM 1,0](how-to-edit-mbam-10-gpo-settings.md). Если серверы администрирования и мониторинга MBAM являются новыми для вашей среды, убедитесь в том, что членство в локальной группе безопасности настроено должным образом. Дополнительные сведения о требованиях к группе безопасности можно найти в разделе [Планирование ролей администратора для MBAM 1,0](planning-for-mbam-10-administrator-roles.md).

13. После завершения настройки NLB-кластера рекомендуется проверить работоспособность кластера MBAM администрирования и мониторинга NLB. Для этого откройте веб-браузер на компьютере, отличном от серверов, настроенных в NLB, и убедитесь, что вы можете получить доступ к веб-сайту администрирования и мониторинга MBAM с помощью полного доменного имени NLB.

## Статьи по теме


[Развертывание инфраструктуры сервера MBAM 1.0](deploying-the-mbam-10-server-infrastructure.md)

 

 





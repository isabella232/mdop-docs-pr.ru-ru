---
title: Установка и настройка MBAM на распределенных серверах
description: Установка и настройка MBAM на распределенных серверах
author: dansimp
ms.assetid: 9ee766aa-6339-422a-8d00-4f58e4646a5e
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 51f56a12d4e59226f834c7e474af0f1e96c1e8e9
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10825659"
---
# Установка и настройка MBAM на распределенных серверах


Процедуры, описанные в этом разделе, описывают полную установку функций администрирования и мониторинга Microsoft BitLocker (MBAM) на распределенных серверах.

Каждый компонент сервера имеет определенные предварительные условия. Чтобы убедиться в том, что требования к оборудованию и программному обеспечению соблюдены, ознакомьтесь с требованиями к [развертыванию MBAM 1,0](mbam-10-deployment-prerequisites.md) и [MBAM 1,0 поддерживаемые конфигурации](mbam-10-supported-configurations.md). Кроме того, для успешного развертывания компонента некоторым функциям потребуется предоставить определенные сведения в процессе установки.

**Примечание.**  
Чтобы получить файлы журнала установки, необходимо установить MBAM с помощью пакета **msiexec** и параметра **/l &lt; Location &gt; ** . Файлы журнала создаются в указанном расположении.

Дополнительные файлы журнала установки создаются в папке% temp% пользователя, на котором выполняется установка MBAM.



## <a href="" id="deploy-the-mbam-server-features-"></a>Развертывание функций сервера MBAM


Ниже описаны действия, которые необходимо выполнить, чтобы установить общие функции MBAM.

**Примечание.**  
Убедитесь, что вы используете 32-разрядную настройку на 32-разрядных серверах и на 64-разрядной установке на 64-разрядных серверах.



**Развертывание функций сервера MBAM**

1.  Запустите мастер установки MBAM и нажмите кнопку **установить** на странице приветствия.

2.  Прочтите и подтвердите условия лицензионного соглашения на использование программного обеспечения корпорации Майкрософт, а затем нажмите кнопку **Далее** , чтобы продолжить установку.

3.  По умолчанию для установки выбраны все функции MBAM. Снимите флажки для компонентов, которые вы хотите установить на другом месте. Возможности, которые необходимо установить на одном и том же компьютере, должны быть установлены в любой момент. Функции MBAM должны устанавливаться в следующем порядке:

    -   База данных восстановления и оборудования

    -   База данных соответствия требованиям и аудита

    -   Аудит соответствия требованиям и отчеты

    -   Сервер администрирования и мониторинга

    -   Шаблон групповой политики MBAM

    **Примечание.**  
    Мастер установки проверяет предварительные требования для установки и выводит недостающие необходимые компоненты. Если все необходимые условия выполнены, установка будет продолжена. Если обнаружен отсутствующий предварительный компонент, необходимо устранить недостающие необходимые компоненты и нажать кнопку **проверить необходимые компоненты еще раз**. Если все необходимые условия выполнены, установка будет возобновлена.



4.  В мастере настройки MBAM будут отображены страницы установки для выбранных функций. В следующих разделах описаны процедуры установки для каждой функции.

    **Примечание.**  
    Как правило, каждый компонент устанавливается на отдельном сервере. Если вы хотите установить несколько функций на один сервер, вы можете изменить или устранить некоторые из описанных ниже действий.



~~~
**To install the Recovery and Hardware Database**

1.  Choose an option for MBAM communication encryption. MBAM can encrypt the communication between the Recovery and Hardware Database and the Administration and Monitoring servers. If you choose the option to encrypt communication, you are asked to select the authority-provisioned certificate that is used for encryption.

2.  Click **Next** to continue.

3.  Specify the names of the computers that will be running the Administration and Monitoring Server feature, to configure access to the Recovery and Hardware Database.. Once the Administration and Monitoring Server feature is deployed, it connects to the database by using its domain account.

4.  Click **Next** to continue.

5.  Specify the **Database Configuration** for the SQL Server instance that stores the recovery and hardware data. You must also specify where the database will be located and where the log information will be located.

6.  Click **Next** to continue with the MBAM Setup wizard.

**To install the Compliance and Audit Database**

1.  Choose an option for the MBAM communication encryption. MBAM can encrypt the communication between the Compliance and Audit Database and the Administration and Monitoring servers. If you choose the option to encrypt communication, you are asked to select the authority-provisioned certificate that will be used for encryption.

2.  Click **Next** to continue.

3.  Specify the user account that will be used to access the database for reports.

4.  Click **Next** to continue.

5.  Specify the computer names of the computers that you want to run the Administration and Monitoring Server and the Compliance and Audit Reports, to configure the access to the Compliance and Audit Database.. After the Administration and Monitoring and the Compliance and Audit Reports Server are deployed, they will connect to the databases by using their domain accounts.

6.  Specify the **Database Configuration** for the SQL Server instance that will store the compliance and audit data. You must also specify where the database will be located and where the log information will be located.

7.  Click **Next** to continue with the MBAM Setup wizard.

**To install the Compliance and Audit Reports**

1.  Specify the remote SQL Server instance. For example, *&lt;ServerName&gt;*,where the Compliance and Audit Database are installed.

2.  Specify the name of the Compliance and Audit Database. By default, the database name is “MBAM Compliance Status”, but you can change the name when you install the Compliance and Audit Database.

3.  Click **Next** to continue.

4.  Select the SQL Server Reporting Services instance where the Compliance and Audit Reports will be installed. Provide the username and password used to access the compliance database.

5.  Click **Next** to continue with the MBAM Setup wizard.

**To install the Administration and Monitoring Server feature**

1.  Choose an option for the MBAM communication encryption. MBAM can encrypt the communication between the Recovery and Hardware Database and the Administration and Monitoring servers. If you choose the option to encrypt communication, you are asked to select the authority-provisioned certificate that is used for encryption.

2.  Click **Next** to continue.

3.  Specify the remote SQL Server instance, For example, *&lt;ServerName&gt;*, where the Compliance and Audit Database are installed.

4.  Specify the name of the Compliance and Audit Database. By default, the database name is MBAM Compliance Status, but, you can change the name when you install the Compliance and Audit Database.

5.  Click **Next** to continue.

6.  Specify the remote SQL Server instance. For example, *&lt;ServerName&gt;*,where the Recovery and Hardware Database are installed.

7.  Specify the name of the Recovery and Hardware Database. By default, the database name is **MBAM Recovery and Hardware**, but you can change the name when you install the Recovery and Hardware Database feature.

8.  Click **Next** to continue.

9.  Specify the URL for the “Home” of the SQL Server Reporting Services (SRS) site. The default Home location of a SQL Server Reporting Services site instance is at:

    http://*&lt;NameofMBAMReportsServer&gt;/*ReportServer

    **Note**  
    If you configured the SQL Server Reporting Services as a named instance, the URL resembles the following:http://*&lt;NameofMBAMReportsServer&gt;*/ReportServer\_*&lt;SRSInstanceName&gt;*



10. Click **Next** to continue.

11. Enter the **Port Number**, the **Host Name** (optional), and the **Installation Path** for the MBAM Administration and Monitoring server

    **Warning**  
    The port number that you specify must be an unused port number on the Administration and Monitoring server, unless you specify a unique host header name.



12. Click **Next** to continue with the MBAM Setup wizard.
~~~

5. 

   Укажите, следует ли использовать обновления Microsoft, чтобы обеспечить безопасность компьютера, и нажмите кнопку **Далее**.

6. После того как выбранные сведения о компоненте MBAM будут завершены, вы можете приступить к установке MBAM с помощью мастера настройки. Чтобы проанализировать или изменить параметры установки, нажмите кнопку **назад** для перемещения по мастеру. Нажмите кнопку " **установить** ", чтобы начать установку. Нажмите кнопку **Отмена** , чтобы завершить работу мастера. При установке устанавливаются выбранные компоненты MBAM и уведомляются о том, что установка завершена.

7. Нажмите кнопку **Готово** , чтобы завершить работу мастера.

8. После установки функций сервера MBAM вы можете добавлять пользователей к подходящим MBAM ролям. Дополнительные сведения можно найти в разделе [Планирование ролей администратора для MBAM 1,0](planning-for-mbam-10-administrator-roles.md).

**Настройка после установки**

1.  После завершения настройки MBAM необходимо добавить роли пользователей, чтобы пользователи могли получать доступ к функциям на веб-сайте администрирования MBAM. На сервере администрирования и мониторинга добавьте пользователей в следующие локальные группы.

    -   **Пользователи оборудования MBAM**: участники этой локальной группы могут получить доступ к компоненту "оборудование" на веб-сайте администрирования MBAM.

    -   **Пользователи службы поддержки MBAM**: участники этой локальной группы могут получить доступ к восстановлению диска и управлять функциями доверенных платформенных модулей (TPM) на веб-сайте администрирования MBAM. Все поля в восстановлении диска и Управление TPM являются обязательными полями для пользователя службы поддержки.

    -   **MBAM опытных пользователей службы поддержки**: участники этой локальной группы имеют расширенный доступ к восстановлению диска и управляют функциями доверенного платформенного модуля на веб-сайте администрирования MBAM. Для опытных пользователей службы поддержки требуется только поле "ИД ключа" в восстановлении диска. В разделе Управление доверенными платформенными модулями требуется только поле компьютера домена и имя компьютера.

2.  В базе данных "Администрирование", "соответствие" и "Аудит", а также на сервере, на котором размещаются отчеты о соответствии и аудите, добавьте пользователей в следующую локальную группу, чтобы предоставить им доступ к функции "отчеты" на веб-сайте администрирования MBAM.

    -   **Пользователи отчетов MBAM**: участники этой локальной группы могут получать доступ к отчетам на веб-сайте администрирования MBAM.

    **Примечание.**  
    Идентичные пользователи или члены группы в **отчете MBAM** локальная группа пользователей должны поддерживаться на всех компьютерах, на которых администрирование MBAM и наблюдение за базой данных функций сервера, соответствие требованиям и аудитом, а также отчеты о соответствии и аудите установлены.



## Проверка установки компонентов сервера MBAM


После завершения установки компонента сервера MBAM вы должны убедиться, что установка успешно настроила все необходимые функции для MBAM. Чтобы убедиться в том, что служба MBAM работает, выполните описанные ниже действия.

**Проверка установки MBAM**

1. На каждом сервере, где развернута функция MBAM, откройте **Панель управления**, нажмите кнопку **программы**и выберите пункт **программы и компоненты**. Убедитесь в том, что в списке **программы и компоненты** отображается элемент **Администрирование и мониторинг Microsoft BitLocker** .

   **Примечание.**  
   Для проверки установки MBAM необходимо использовать учетную запись домена, которая содержит учетные данные администратора локального компьютера на каждом сервере.



2. На сервере, на котором установлена база данных восстановления и оборудования, откройте SQL Server Management Studio и убедитесь, что установлена **Восстановление MBAM и** база данных оборудования.

3. На сервере, на котором установлена база данных соответствия и аудита, откройте центр администрирования SQL Server и убедитесь, что установлена база данных **состояния соответствия MBAM** .

4. На сервере, на котором установлены отчеты о соответствии и аудите, откройте веб-браузер с правами администратора и перейдите на веб-сайт служб SQL Server Reporting Services на домашнюю страницу.

   Расположение по умолчанию для экземпляра служб SQL Server Reporting Services можно найти на сайте http:// <em> &lt; NameofMBAMReportsServer &gt; </em> /Reports.aspx. Чтобы найти фактический URL-адрес, используйте Диспетчер конфигураций служб Reporting Services и выберите экземпляры, заданные во время настройки.

   Убедитесь в том, что в списке указана папка **Отчеты соответствие требованиям** , и что она содержит пять отчетов и один источник данных.

   **Примечание.**  
   Если службы отчетов SQL Server были настроены как именованный экземпляр, URL-адрес должен выглядеть следующим образом: http://* &lt; NameofMBAMReportsServer &gt; */Reports\_* &lt; SRSInstanceName &gt; *



5. На сервере, на котором установлен компонент "Администрирование и наблюдение", запустите **Диспетчер серверов** и перейдите к пункту " **роли**", выберите **веб-сервер (IIS)**, а затем — **Диспетчер служб Internet Information Services (IIS)**. В окне **подключения** перейдите на * &lt; компьютер имя_компьютера &gt; *, нажмите **сайты**, а затем — **Администрирование и мониторинг Microsoft BitLocker**. Убедитесь в том, что указаны **MBAMAdministrationService**, **MBAMComplianceStatusService**и **MBAMRecoveryAndHardwareService** .

6. На сервере, на котором установлен компонент "Администрирование" и "наблюдение", откройте веб-браузер с правами администратора и перейдите по следующим адресам на веб-сайте MBAM, чтобы убедиться в том, что они успешно загружены.

   -   *http:// &lt; имя_компьютера &gt; /Default.aspx* и убедитесь в том, что все ссылки для навигации и отчетов

   -   *http:// &lt; имя_компьютера &gt; /MBAMAdministrationService/AdministrationService.svc*

   -   *http:// &lt; имя_компьютера &gt; /MBAMComplianceStatusService/StatusReportingService.svc*

   -   *http:// &lt; имя_компьютера &gt; /MBAMRecoveryAndHardwareService/CoreService.svc*

   **Примечание.**  
   Обычно службы устанавливаются на порт по умолчанию 80 без сетевого шифрования. Если службы установлены на другом порту, измените URL-адреса, чтобы включить соответствующий порт. Например, http://* &lt; имя_компьютера &gt; : &lt; Port &gt; */Default.aspx или http:// <em> &lt; hostheadername &gt; / </em> Default. aspx

   Если службы были установлены с сетевым шифрованием, измените http://на https://.



~~~
Verify that each web page loads successfully.
~~~

## Статьи по теме


[Развертывание инфраструктуры сервера MBAM 1.0](deploying-the-mbam-10-server-infrastructure.md)










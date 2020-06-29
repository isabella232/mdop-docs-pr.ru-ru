---
title: Установка баз данных App-V и преобразование сопоставленных идентификаторов безопасности с помощью PowerShell
description: Установка баз данных App-V и преобразование сопоставленных идентификаторов безопасности с помощью PowerShell
author: dansimp
ms.assetid: 2be6fb72-f3a6-4550-bba1-6defa78ca08a
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 39651df4d62971e39c4228ffce665386d5c9769d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10814037"
---
# <span data-ttu-id="0a890-103">Установка баз данных App-V и преобразование сопоставленных идентификаторов безопасности с помощью PowerShell</span><span class="sxs-lookup"><span data-stu-id="0a890-103">How to Install the App-V Databases and Convert the Associated Security Identifiers by Using PowerShell</span></span>

<span data-ttu-id="0a890-104">Чтобы преобразовать все учетные записи пользователей и компьютеров доменных служб Active Directory (AD DS) в отформатированные идентификаторы безопасности (SID) в стандартном формате и в шестнадцатеричном формате, используемом в Microsoft SQL Server при выполнении сценариев SQL, используйте следующую процедуру PowerShell.</span><span class="sxs-lookup"><span data-stu-id="0a890-104">Use the following PowerShell procedure to convert any number of Active Directory Domain Services (AD DS) user or machine accounts into formatted Security Identifiers (SIDs) both in the standard format and in the hexadecimal format used by Microsoft SQL Server when running SQL scripts.</span></span>

<span data-ttu-id="0a890-105">Перед выполнением этой процедуры следует ознакомиться со сведениями и примерами, представленными в следующем списке.</span><span class="sxs-lookup"><span data-stu-id="0a890-105">Before attempting this procedure, you should read and understand the information and examples displayed in the following list:</span></span>

- <span data-ttu-id="0a890-106">**. ВХОДные данные** — учетная запись или учетные записи, которые используются для преобразования в формат SID.</span><span class="sxs-lookup"><span data-stu-id="0a890-106">**.INPUTS** – The account or accounts used to convert to SID format.</span></span> <span data-ttu-id="0a890-107">Это может быть одно имя учетной записи или массив имен учетных записей.</span><span class="sxs-lookup"><span data-stu-id="0a890-107">This can be a single account name or an array of account names.</span></span>

- <span data-ttu-id="0a890-108">**. OUTPUTs** — список имен учетных записей с СООТВЕТСТВУЮЩИМ SID в стандартном и шестнадцатеричном форматах.</span><span class="sxs-lookup"><span data-stu-id="0a890-108">**.OUTPUTS** - A list of account names with the corresponding SID in standard and hexadecimal formats.</span></span>

- <span data-ttu-id="0a890-109">**Иллюстрируют** -</span><span class="sxs-lookup"><span data-stu-id="0a890-109">**Examples** -</span></span>

    <span data-ttu-id="0a890-110">**.\\ConvertToSID.ps1 DOMAIN\\user\ _account1 DOMAIN\\machine\ _account1 $ DOMAIN\\user\ _account2 | Формат списка**.</span><span class="sxs-lookup"><span data-stu-id="0a890-110">**.\\ConvertToSID.ps1 DOMAIN\\user\_account1 DOMAIN\\machine\_account1$ DOMAIN\\user\_account2 | Format-List**.</span></span>

    **<span data-ttu-id="0a890-111">$accountsArray = @ ("DOMAIN\\user\ _account1"; "DOMAIN\\machine\ _account1 $", "DOMAIN \ _user \ _account2")</span><span class="sxs-lookup"><span data-stu-id="0a890-111">$accountsArray = @("DOMAIN\\user\_account1", "DOMAIN\\machine\_account1$", "DOMAIN\_user\_account2")</span></span>**

    **<span data-ttu-id="0a890-112">.\\ConvertToSID.ps1 $accountsArray | Файл с выводом на печать-FilePath .\\SIDs.txt — ширина 200</span><span class="sxs-lookup"><span data-stu-id="0a890-112">.\\ConvertToSID.ps1 $accountsArray | Write-Output -FilePath .\\SIDs.txt -Width 200</span></span>**

## <span data-ttu-id="0a890-113">Преобразование количества учетных записей пользователей и компьютеров доменных служб Active Directory (AD DS) в отформатированные идентификаторы безопасности (SID)</span><span class="sxs-lookup"><span data-stu-id="0a890-113">To convert any number of Active Directory Domain Services (AD DS) user or machine accounts into formatted Security Identifiers (SIDs)</span></span>

1. <span data-ttu-id="0a890-114">Скопируйте приведенный ниже сценарий в текстовый редактор и сохраните его в виде файла сценария PowerShell, например **ConvertToSIDs.ps1**.</span><span class="sxs-lookup"><span data-stu-id="0a890-114">Copy the following script into a text editor and save it as a PowerShell script file, for example **ConvertToSIDs.ps1**.</span></span>
1. <span data-ttu-id="0a890-115">Чтобы открыть консоль PowerShell, нажмите кнопку **Пуск** и введите **PowerShell**.</span><span class="sxs-lookup"><span data-stu-id="0a890-115">To open a PowerShell console click **Start** and type **PowerShell**.</span></span> <span data-ttu-id="0a890-116">Щелкните правой кнопкой мыши элемент **Windows PowerShell** и выберите пункт **Запуск от имени администратора**.</span><span class="sxs-lookup"><span data-stu-id="0a890-116">Right-click **Windows PowerShell** and select **Run as Administrator**.</span></span>

   ```powershell
   <#
   .SYNOPSIS
   This PowerShell script will take an array of account names and try to convert each of them to the corresponding SID in standard and hexadecimal formats.
   .DESCRIPTION
   This is a PowerShell script that converts any number of Active Directory (AD) user or machine accounts into formatted Security Identifiers (SIDs) both in the standard format and in the hexadecimal format used by SQL server when running SQL scripts.
   .INPUTS
   The account(s) to convert to SID format. This can be a single account name or an array of account names. Please see examples below.
   .OUTPUTS
   A list of account names with the corresponding SID in standard and hexadecimal formats
   .EXAMPLE
   .\ConvertToSID.ps1 DOMAIN\user_account1 DOMAIN\machine_account1$ DOMAIN\user_account2 | Format-List
   .EXAMPLE
   $accountsArray = @("DOMAIN\user_account1", "DOMAIN\machine_account1$", "DOMAIN_user_account2")
   .\ConvertToSID.ps1 $accountsArray | Write-Output -FilePath .\SIDs.txt -Width 200
   #>

   function ConvertSIDToHexFormat
   {

      param([System.Security.Principal.SecurityIdentifier]$sidToConvert)

      $sb = New-Object System.Text.StringBuilder
      [int] $binLength = $sidToConvert.BinaryLength
      [Byte[]] $byteArray = New-Object Byte[] $binLength
      $sidToConvert.GetBinaryForm($byteArray, 0)
      foreach($byte in $byteArray)
      {
          $sb.Append($byte.ToString("X2")) |Out-Null
      }
      return $sb.ToString()
   }
    [string[]]$myArgs = $args
   if(($myArgs.Length -lt 1) -or ($myArgs[0].CompareTo("/?") -eq 0))
   {

    [string]::Format("{0}====== Description ======{0}{0}" +
                  "  Converts any number of user or machine account names to string and hexadecimal SIDs.{0}" +
                  "  Pass the account(s) as space separated command line parameters. (For example 'ConvertToSID.ps1 DOMAIN\Account1 DOMAIN\Account2 ...'){0}" +
                  "  The output is written to the console in the format 'Account name    SID as string   SID as hexadecimal'{0}" +
                  "  And can be written out to a file using standard PowerShell redirection{0}" +
                  "  Please specify user accounts in the format 'DOMAIN\username'{0}" +
                  "  Please specify machine accounts in the format 'DOMAIN\machinename$'{0}" +
                  "  For more help content, please run 'Get-Help ConvertToSID.ps1'{0}" +
                  "{0}====== Arguments ======{0}" +
                  "{0}  /?    Show this help message", [Environment]::NewLine)
   }
   else
   {
       #If an array was passed in, try to split it
       if($myArgs.Length -eq 1)
       {
           $myArgs = $myArgs.Split(' ')
       }

       #Parse the arguments for account names
       foreach($accountName in $myArgs)
       {
           [string[]] $splitString = $accountName.Split('\')  # We're looking for the format "DOMAIN\Account" so anything that does not match, we reject
           if($splitString.Length -ne 2)
           {
               $message = [string]::Format("{0} is not a valid account name. Expected format 'Domain\username' for user accounts or 'DOMAIN\machinename$' for machine accounts.", $accountName)
               Write-Error -Message $message
               continue
           }

           #Convert any account names to SIDs
           try
           {
               [System.Security.Principal.NTAccount] $account = New-Object System.Security.Principal.NTAccount($splitString[0], $splitString[1])
               [System.Security.Principal.SecurityIdentifier] $SID = [System.Security.Principal.SecurityIdentifier]($account.Translate([System.Security.Principal.SecurityIdentifier]))
           }
           catch [System.Security.Principal.IdentityNotMappedException]
           {
               $message = [string]::Format("Failed to translate account object '{0}' to a SID. Please verify that this is a valid user or machine account.", $account.ToString())
               Write-Error -Message $message
               continue
           }

           #Convert regular SID to binary format used by SQL
           $hexSIDString = ConvertSIDToHexFormat $SID

           $SIDs = New-Object PSObject
           $SIDs | Add-Member NoteProperty Account $accountName
           $SIDs | Add-Member NoteProperty SID $SID.ToString()
           $SIDs | Add-Member NoteProperty Hexadecimal $hexSIDString

           Write-Output $SIDs
       }
   }
   ```

1. <span data-ttu-id="0a890-117">Запустите сценарий, сохраненный на шаге один из этих процедур, передавая учетные записи для преобразования в качестве аргументов.</span><span class="sxs-lookup"><span data-stu-id="0a890-117">Run the script you saved in step one of this procedure passing the accounts to convert as arguments.</span></span>

   <span data-ttu-id="0a890-118">Например:</span><span class="sxs-lookup"><span data-stu-id="0a890-118">For example,</span></span>

   **<span data-ttu-id="0a890-119">.\\ConvertToSID.ps1 DOMAIN\\user\ _account1 DOMAIN\\machine\ _account1 $ DOMAIN\\user\ _account2 | Формат: список</span><span class="sxs-lookup"><span data-stu-id="0a890-119">.\\ConvertToSID.ps1 DOMAIN\\user\_account1 DOMAIN\\machine\_account1$ DOMAIN\\user\_account2 | Format-List</span></span>**
   
   <span data-ttu-id="0a890-120">или</span><span class="sxs-lookup"><span data-stu-id="0a890-120">or</span></span>
   
   <span data-ttu-id="0a890-121">**$accountsArray = @ ("DOMAIN\\user\ _account1"; "DOMAIN\\machine\ _account1 $", "Domain \ _USER \ _account2")** 
    **.\\ConvertToSID.ps1 $accountsArray | Файл с выводом на печать-FilePath .\\SIDs.txt — ширина 200**</span><span class="sxs-lookup"><span data-stu-id="0a890-121">**$accountsArray = @("DOMAIN\\user\_account1", "DOMAIN\\machine\_account1$", "DOMAIN\_user\_account2")**
 **.\\ConvertToSID.ps1 $accountsArray | Write-Output -FilePath .\\SIDs.txt -Width 200**</span></span>

**<span data-ttu-id="0a890-122">У вас возникла ошибка App-V?</span><span class="sxs-lookup"><span data-stu-id="0a890-122">Got an App-V issue?</span></span>** <span data-ttu-id="0a890-123">Используйте [Форум TechNet App-V](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span><span class="sxs-lookup"><span data-stu-id="0a890-123">Use the [App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span></span>

## <span data-ttu-id="0a890-124">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="0a890-124">Related topics</span></span>

[<span data-ttu-id="0a890-125">Администрирование App-V 5.1 с помощью PowerShell</span><span class="sxs-lookup"><span data-stu-id="0a890-125">Administering App-V 5.1 by Using PowerShell</span></span>](administering-app-v-51-by-using-powershell.md)

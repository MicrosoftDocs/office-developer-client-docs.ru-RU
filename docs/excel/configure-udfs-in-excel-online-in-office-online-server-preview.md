---
title: Настройка пользовательских функций в Excel Online в Office Online Server
manager: soliver
ms.date: 03/18/2016
ms.audience: ITPro
localization_priority: Normal
ms.assetid: 3e0ca274-e9cd-48a1-8cfc-9d5053738972
description: Используйте пользовательские функции (UDF) в Excel Online в Office Online Server, чтобы вызывать пользовательские функции.
ms.openlocfilehash: dbba60a62a1a4783b47c3f1fe40a118dd8ed0d6d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32311062"
---
# <a name="configure-udfs-in-excel-online-in-office-online-server"></a>Настройка пользовательских функций в Excel Online в Office Online Server

Используйте пользовательские функции (UDF) в Excel Online в Office Online Server, чтобы вызывать пользовательские функции. 
  
Пользовательские функции (UDF) в Excel Online позволяют вызывать пользовательские функции, написанные в управляемом коде, с помощью формул в ячейках. Пользовательские функции можно использовать для следующих функций:
  
- Call custom mathematical functions.
    
- Get data from custom data sources into worksheets.
    
- Вызов веб-служб.
    
Двоичные файлы UDF можно установить в одном из двух расположений:
  
- Локальный каталог. Пример: 
    
    К:\удфс\мисамплеудф.длл
    
- Глобальный кэш сборок. Пример: 
    
    CompanyName.Hierarchichal.MyUdfNamespace.MyUdfClassName.dll, Version=1.1.0.0, Culture=en, PublicKeyToken=e8123117d7ba9ae38
    
Ссылайтесь на расположение при создании определения **New-оффицевебаппсексцелусердефинедфунктион** на сервере Office Online Server. 
  
> [!NOTE]
> Office Online Server не поддерживает пользовательские функции, расположенные в сетевых ресурсах. 
  
## <a name="enable-udfs-on-office-online-server"></a>Включение пользовательских функций в Office Online Server 

Когда администратор создает новую ферму серверов Office Web Apps с помощью командлета Windows PowerShell [New-OfficeWebAppsFarm](https://technet.microsoft.com/en-us/library/jj219436.aspx) , сборки UDF по умолчанию отключены. Значение по умолчанию для флага **ексцелудфсалловед** — false. 
  
Чтобы включить UDF, выполните следующую команду Windows PowerShell на сервере Office Online Server после создания фермы серверов Office Web Apps.
  
`Set-OfficeWebAppsFarm - ExcelUdfsAllowed:$true`
  
## <a name="create-udf-definitions-on-office-online-server"></a>Создание определений UDF в Office Online Server

После включения UDF необходимо создать определение двоичного файла, содержащего пользовательские функции. Чтобы создать определение для двоичной функции UDF на сервере Office Online Server, используйте командлет **New-оффицевебаппсексцелусердефинедфунктион** . Этот командлет включает следующие параметры: 
  
- **Сборок**
    
- **Ассемблилокатион**
    
- **Включение** (по умолчанию задано значение false) 
    
- **Описание**
    
В следующих примерах показано, как создать определения UDF.
  
`New-OfficeWebAppsExcelUserDefinedFunction -Assembly c:\myudf.dll -AssemblyLocation LocalFile -Enable:$true -Description "My Server UDFs"`
  
`New-OfficeWebAppsExcelUserDefinedFunction -Assembly "CompanyName.Hierarchichal.MyUdfNamespace.MyUdfClassName.dll, Version=1.1.0.0, Culture=en, PublicKeyToken=e8123117d7ba9ae38" -AssemblyLocation GAC -Enable:$true -Description "My GAC Server UDFs"`
  
После создания новой ссылки на UDF запустите **iisreset** на сервере для немедленного получения ссылки. 
  
## <a name="additional-office-online-server-udf-windows-powershell-commands"></a>Дополнительные команды Windows PowerShell для UDF на сервере Office Online Server

Используйте следующие командлеты Windows PowerShell для работы с UDF:
  
- **Get — оффицевебаппсексцелусердефинедфунктион** (нет обязательных параметров) — возвращает список определений UDF, настроенных на сервере Office Online Server. 
    
- **Set — оффицевебаппсексцелусердефинедфунктион** (Обязательный параметр Identity) — задает свойства существующих определений UDF. 
    
- **Remove — оффицевебаппсексцелусердефинедфунктион** (Обязательный параметр Identity) — удаляет существующие определения UDF. 
    
## <a name="udf-sample"></a>Пример использования UDF

В следующих файлах представлена пример книги, в которой используется UDF и двоичный файл UDF:
  
- [Булеандататипе. xlsx](https://download.microsoft.com/download/6/7/F/67F724FD-1186-4209-BFF1-FBFD99E959D9/User%20Defined%20Function%20Assemblies/BooleanDataType.xlsx): образец книги, ИСПОЛЬЗУЮЩей UDF  
- [Ексудфскоммонсет. dll](https://www.microsoft.com/en-us/search/result.aspx?q=EcsUdfsCommonSet.dll): двоичный файл UDF 
    
## <a name="see-also"></a>См. также

- [Настройка параметров администрирования Excel Online](https://docs.microsoft.com/officeonlineserver/configure-excel-online-administrative-settings)  
- [Office Online Server](https://docs.microsoft.com/officeonlineserver/office-online-server)
    


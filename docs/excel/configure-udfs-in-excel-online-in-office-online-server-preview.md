---
title: Настройка UDF в Excel Online в Office Online Server
manager: lindalu
ms.date: 12/03/2019
ms.audience: ITPro
localization_priority: Normal
ms.assetid: 3e0ca274-e9cd-48a1-8cfc-9d5053738972
description: Использование пользовательских функций (UDF) в Excel Online в Office Online Server для вызова пользовательских функций.
ms.openlocfilehash: e1b005079c03ae3028ba6bf9ee1156c6ae2eae80
ms.sourcegitcommit: 007aa2ceb4f569201c3f4372de5c83b6c61f8875
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/02/2020
ms.locfileid: "43102935"
---
# <a name="configure-udfs-in-excel-online-in-office-online-server"></a>Настройка UDF в Excel Online в Office Online Server

Использование пользовательских функций (UDF) в Excel Online в Office Online Server для вызова пользовательских функций. 
  
Пользовательские функции в Excel Online позволяют вызывать пользовательские функции, написанные в управляемом коде, с помощью формул в ячейках. You can use UDFs to:
  
- вызова специальных математических функций;
    
- загрузки на листы данных из специальных источников;
    
- Вызов веб-служб.
    
Двоики UDF можно установить в одном из двух мест:
  
- Локальный каталог. Например: 
    
    C:\UDFs\MySampleUdf.dll
    
- Глобальный кэш сборок. Например: 
    
    CompanyName.Hierarchichal.MyUdfNamespace.MyUdfClassName.dll, Version=1.1.0.0, Culture=en, PublicKeyToken=e8123117d7ba9ae38
    
Ссылка на расположение при создании определения **New-OfficeWebAppsExcelUserDefinedFunction** на сервере Office Online Server. 
  
> [!NOTE]
> Office Online Server не поддерживаетudfs, расположенные на сетевых серверах. 
  
## <a name="enable-udfs-on-office-online-server"></a>Enable UDFs on Office Online Server 

Когда администратор создает новую ферму серверов Office Web Apps с помощью Windows PowerShell [New-OfficeWebAppsFarm,](https://docs.microsoft.com/powershell/module/officewebapps/new-officewebappsfarm?view=officewebapps-ps) сборки UDF по умолчанию отключаются. Значение по умолчанию для **флага ExcelUdfsAllowed** — false. 
  
Чтобы включить UDF, запустите следующую Windows PowerShell на сервере Office Online Server после создания фермы серверов Office Web Apps.
  
`Set-OfficeWebAppsFarm - ExcelUdfsAllowed:$true`
  
## <a name="create-udf-definitions-on-office-online-server"></a>Создание определений UDF в Office Online Server

После этого необходимо создать определение двоичного файла, который содержит эти UDF. Чтобы создать определение для двоичного файла UDF на сервере Office Online Server, используйте cmdlet **New-OfficeWebAppsExcelUserDefinedFunction.** Этот cmdlet включает следующие параметры: 
  
- **Сборка**
    
- **AssemblyLocation**
    
- **Включить** (по умолчанию установлено значение False) 
    
- **Описание**
    
В следующих примерах покажем, как создавать определения UDF.
  
`New-OfficeWebAppsExcelUserDefinedFunction -Assembly c:\myudf.dll -AssemblyLocation LocalFile -Enable:$true -Description "My Server UDFs"`
  
`New-OfficeWebAppsExcelUserDefinedFunction -Assembly "CompanyName.Hierarchichal.MyUdfNamespace.MyUdfClassName.dll, Version=1.1.0.0, Culture=en, PublicKeyToken=e8123117d7ba9ae38" -AssemblyLocation GAC -Enable:$true -Description "My GAC Server UDFs"`
  
После создания новой ссылки UDF запустите **iisreset** на сервере, чтобы немедленно получить ссылку. 
  
## <a name="additional-office-online-server-udf-windows-powershell-commands"></a>Дополнительные команды office Online Server UDF Windows PowerShell office Online Server

Используйте следующие Windows PowerShell для работы сudfs:
  
- **Get-OfficeWebAppsExcelUserDefinedFunction** (без требуемых параметров) — возвращает список определений UDF, настроенных на сервере Office Online Server. 
    
- **Set-OfficeWebAppsExcelUserDefinedFunction** (требуется параметр Identity) — задает свойства существующих определений UDF. 
    
- **Remove-OfficeWebAppsExcelUserDefinedFunction** (требуется параметр Identity) — удаляет существующие определения UDF. 
    
## <a name="udf-sample"></a>Пример UDF

В следующем примере файла предоставляется пример книги, использующей UDF и двоичный файл UDF:
  
- [BooleanDataType.xlsx](https://download.microsoft.com/download/6/7/F/67F724FD-1186-4209-BFF1-FBFD99E959D9/User%20Defined%20Function%20Assemblies/BooleanDataType.xlsx): пример книги, использующей UDF  
    
## <a name="see-also"></a>См. также

- [Настройка параметров администрирования Excel Online](https://docs.microsoft.com/officeonlineserver/configure-excel-online-administrative-settings)  
- [Office Online Server](https://docs.microsoft.com/officeonlineserver/office-online-server)
    


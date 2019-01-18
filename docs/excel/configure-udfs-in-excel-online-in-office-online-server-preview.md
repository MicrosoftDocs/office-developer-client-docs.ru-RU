---
title: Настройка пользовательских функций в Excel Online в Office Online Server
manager: soliver
ms.date: 03/18/2016
ms.audience: ITPro
localization_priority: Normal
ms.assetid: 3e0ca274-e9cd-48a1-8cfc-9d5053738972
description: Используйте пользовательские функции (UDF) в Excel Online в Office Online Server для вызова пользовательских функций.
ms.openlocfilehash: dbba60a62a1a4783b47c3f1fe40a118dd8ed0d6d
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28722790"
---
# <a name="configure-udfs-in-excel-online-in-office-online-server"></a>Настройка пользовательских функций в Excel Online в Office Online Server

Используйте пользовательские функции (UDF) в Excel Online в Office Online Server для вызова пользовательских функций. 
  
Пользовательские функции (UDF) в Excel Online дают возможность вызова пользовательских функций, написанных в управляемом коде с помощью формулы в ячейках. Вы можете использовать пользовательских функций:
  
- вызова специальных математических функций;
    
- загрузки на листы данных из специальных источников;
    
- Вызов веб-служб.
    
Можно установить двоичные файлы пользовательских Функций в одном из двух местоположений:
  
- Локальный каталог. Пример: 
    
    C:\UDFs\MySampleUdf.dll 
    
- В глобальном кэше сборок. Пример: 
    
    CompanyName.Hierarchichal.MyUdfNamespace.MyUdfClassName.dll, Version=1.1.0.0, Culture=en, PublicKeyToken=e8123117d7ba9ae38
    
Справочник по месту при создании определения **New-OfficeWebAppsExcelUserDefinedFunction** на сервере Office Online. 
  
> [!NOTE]
> Office Online Server не поддерживает пользовательских функций, расположенных в сетевых папках. 
  
## <a name="enable-udfs-on-office-online-server"></a>Включение пользовательских функций на сервере Office Online 

Когда администратор создает новую ферму сервера Office Web Apps с помощью командлета [New-OfficeWebAppsFarm](https://technet.microsoft.com/en-us/library/jj219436.aspx) Windows PowerShell, по умолчанию отключены сборки пользовательских Функций. Значение по умолчанию флаг **ExcelUdfsAllowed** имеет значение false. 
  
Включение пользовательских функций, выполните следующую команду Windows PowerShell на сервере Office Online, после создания фермы сервера Office Web Apps.
  
`Set-OfficeWebAppsFarm - ExcelUdfsAllowed:$true`
  
## <a name="create-udf-definitions-on-office-online-server"></a>Создание определений пользовательских Функций на сервере Office Online

После включения пользовательских функций, необходимо создать определение двоичный файл, содержащий пользовательских функций. Для создания определения для вашей UDF двоичные на сервере Office Online, используйте командлет **New-OfficeWebAppsExcelUserDefinedFunction** . Этот командлет включает в себя следующие параметры: 
  
- **Сборки**
    
- **Расположение_сборки**
    
- **Включение** (присвоено значение False, по умолчанию) 
    
- **Описание**
    
В следующем примере показано, как создать определения пользовательских Функций.
  
`New-OfficeWebAppsExcelUserDefinedFunction -Assembly c:\myudf.dll -AssemblyLocation LocalFile -Enable:$true -Description "My Server UDFs"`
  
`New-OfficeWebAppsExcelUserDefinedFunction -Assembly "CompanyName.Hierarchichal.MyUdfNamespace.MyUdfClassName.dll, Version=1.1.0.0, Culture=en, PublicKeyToken=e8123117d7ba9ae38" -AssemblyLocation GAC -Enable:$true -Description "My GAC Server UDFs"`
  
После создания новой ссылки UDF, выполните **команду iisreset** на сервере для сбора ссылки сразу же. 
  
## <a name="additional-office-online-server-udf-windows-powershell-commands"></a>Дополнительные команды Office Online Server UDF Windows PowerShell

Используйте следующие командлеты Windows PowerShell для работы с помощью пользовательских функций:
  
- **Get-OfficeWebAppsExcelUserDefinedFunction** (без обязательных параметров) — возвращает список определений пользовательских Функций, которые настроены на сервере Office Online. 
    
- **Set-OfficeWebAppsExcelUserDefinedFunction** (Параметра identity требуется) - задаются свойства существующего определения пользовательских Функций. 
    
- **Remove-OfficeWebAppsExcelUserDefinedFunction** (Параметра identity требуется) — удаляет существующие определения пользовательских Функций. 
    
## <a name="udf-sample"></a>Пример пользовательских Функций

Следующие файлы содержат пример книги с использованием пользовательской функции и двоичные UDF.
  
- [BooleanDataType.xlsx](https://download.microsoft.com/download/6/7/F/67F724FD-1186-4209-BFF1-FBFD99E959D9/User%20Defined%20Function%20Assemblies/BooleanDataType.xlsx): пример книги, с помощью пользовательской функции  
- [EcsUdfsCommonSet.dll](https://www.microsoft.com/en-us/search/result.aspx?q=EcsUdfsCommonSet.dll): двоичный пользовательских Функций 
    
## <a name="see-also"></a>См. также

- [Настройка Excel Online административных параметров](https://docs.microsoft.com/officeonlineserver/configure-excel-online-administrative-settings)  
- [Office Online Server](https://docs.microsoft.com/officeonlineserver/office-online-server)
    


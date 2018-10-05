---
title: Настройка пользовательских функций в Excel Online в Office Online Server Preview
manager: soliver
ms.date: 03/18/2016
ms.audience: ITPro
localization_priority: Normal
ms.assetid: 3e0ca274-e9cd-48a1-8cfc-9d5053738972
description: Используйте пользовательские функции (UDF) в Excel Online в Office Online предварительной версии сервера для вызова пользовательских функций.
ms.openlocfilehash: 2b76b7351a0882762165e37b55c8fbe78f657c34
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25384824"
---
# <a name="configure-udfs-in-excel-online-in-office-online-server-preview"></a>Настройка пользовательских функций в Excel Online в Office Online Server Preview

[Этот раздел предварительной документации и может быть изменен в будущих выпусках.] Используйте пользовательские функции (UDF) в Excel Online в Office Online предварительной версии сервера для вызова пользовательских функций. 
  
Пользовательские функции (UDF) в Excel Online дают возможность вызова пользовательских функций, написанных в управляемом коде с помощью формулы в ячейках. Вы можете использовать пользовательских функций:
  
- Call custom mathematical functions.
    
- Get data from custom data sources into worksheets.
    
- Вызов веб-служб.
    
Можно установить двоичные файлы пользовательских Функций в одном из двух местоположений:
  
- Локальный каталог. Пример: 
    
    C:\UDFs\MySampleUdf.dll 
    
- В глобальном кэше сборок. Пример: 
    
    CompanyName.Hierarchichal.MyUdfNamespace.MyUdfClassName.dll, Version=1.1.0.0, Culture=en, PublicKeyToken=e8123117d7ba9ae38
    
Ссылка на расположение при создании определения **New-OfficeWebAppsExcelUserDefinedFunction** в предварительной версии Microsoft Office Online Server. 
  
> [!NOTE]
> Предварительная версия сервера Office Online не поддерживает пользовательских функций, расположенных в сетевых папках. 
  
## <a name="enable-udfs-on-office-online-server-preview"></a>Включение пользовательских функций в предварительной версии Microsoft Office Online Server

Когда администратор создает новую ферму сервера Office Web Apps с помощью командлета [New-OfficeWebAppsFarm](https://technet.microsoft.com/en-us/library/jj219436.aspx) Windows PowerShell, по умолчанию отключены сборки пользовательских Функций. Значение по умолчанию флаг **ExcelUdfsAllowed** имеет значение false. 
  
Включение пользовательских функций, выполните следующую команду Windows PowerShell на Office Online Server предварительного просмотра, после создания фермы сервера Office Web Apps.
  
`Set-OfficeWebAppsFarm - ExcelUdfsAllowed:$true`
  
## <a name="create-udf-definitions-on-office-online-server-preview"></a>Создание определений пользовательских Функций на Предварительная версия сервера Office Online

После включения пользовательских функций, необходимо создать определение двоичный файл, содержащий пользовательских функций. Для создания определения для вашей UDF двоичные на Office Online Server Preview, используйте командлет **New-OfficeWebAppsExcelUserDefinedFunction** . Этот командлет включает в себя следующие параметры: 
  
- **Сборки**
    
- **Расположение_сборки**
    
- **Включение** (присвоено значение False, по умолчанию) 
    
- **Описание**
    
В следующем примере показано, как создать определения пользовательских Функций.
  
`New-OfficeWebAppsExcelUserDefinedFunction -Assembly c:\myudf.dll -AssemblyLocation LocalFile -Enable:$true -Description "My Server UDFs"`
  
`New-OfficeWebAppsExcelUserDefinedFunction -Assembly "CompanyName.Hierarchichal.MyUdfNamespace.MyUdfClassName.dll, Version=1.1.0.0, Culture=en, PublicKeyToken=e8123117d7ba9ae38" -AssemblyLocation GAC -Enable:$true -Description "My GAC Server UDFs"`
  
После создания новой ссылки UDF, выполните **команду iisreset** на сервере для сбора ссылки сразу же. 
  
## <a name="additional-office-online-server-preview-udf-windows-powershell-commands"></a>Дополнительные команды Office Online Server Preview UDF Windows PowerShell

Используйте следующие командлеты Windows PowerShell для работы с помощью пользовательских функций:
  
- **Get-OfficeWebAppsExcelUserDefinedFunction** (без обязательных параметров) — возвращает список определений пользовательских Функций, которые будут настроены для предварительной версии Office Online Server. 
    
- **Set-OfficeWebAppsExcelUserDefinedFunction** (Параметра identity требуется) - задаются свойства существующего определения пользовательских Функций. 
    
- **Remove-OfficeWebAppsExcelUserDefinedFunction** (Параметра identity требуется) — удаляет существующие определения пользовательских Функций. 
    
## <a name="udf-sample"></a>Пример пользовательских Функций

Следующие файлы содержат пример книги с использованием пользовательской функции и двоичные UDF.
  
- [BooleanDataType.xlsx](https://download.microsoft.com/download/6/7/F/67F724FD-1186-4209-BFF1-FBFD99E959D9/User%20Defined%20Function%20Assemblies/BooleanDataType.xlsx) — пример книги, с помощью пользовательской функции  
- [EcsUdfsCommonSet.dll](https://www.microsoft.com/en-us/search/result.aspx?q=EcsUdfsCommonSet.dll) --двоичный пользовательских Функций 
    
## <a name="see-also"></a>См. также

- [Настройка Excel Online административных параметров](https://docs.microsoft.com/officeonlineserver/configure-excel-online-administrative-settings)  
- [Office Online Server](https://docs.microsoft.com/officeonlineserver/office-online-server)
    


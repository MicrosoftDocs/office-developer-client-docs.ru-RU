---
title: Настройка UDF в Excel Online в Office Online Server
manager: lindalu
ms.date: 12/03/2019
ms.audience: ITPro
localization_priority: Normal
ms.assetid: 3e0ca274-e9cd-48a1-8cfc-9d5053738972
description: Используйте пользовательские функции (UDF) в Excel Online в Office Online Server для вызова пользовательских функций.
ms.openlocfilehash: e1b005079c03ae3028ba6bf9ee1156c6ae2eae80
ms.sourcegitcommit: 007aa2ceb4f569201c3f4372de5c83b6c61f8875
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/02/2020
ms.locfileid: "43102935"
---
# <a name="configure-udfs-in-excel-online-in-office-online-server"></a>Настройка UDF в Excel Online в Office Online Server

Используйте пользовательские функции (UDF) в Excel Online в Office Online Server для вызова пользовательских функций. 
  
Пользовательские функции (UDF) в Excel Online позволяют вызывать настраиваемые функции, написанные в управляемом коде с помощью формул в ячейках. Вы можете использовать UDFs для:
  
- вызова специальных математических функций;
    
- загрузки на листы данных из специальных источников;
    
- Вызов веб-служб.
    
Вы можете установить двоики UDF в одном из двух местоположений:
  
- Локальный каталог. Пример. 
    
    C:\UDFs\MySampleUdf.dll
    
- Кэш глобальной сборки. Пример. 
    
    CompanyName.Hierarchichal.MyUdfNamespace.MyUdfClassName.dll, Version=1.1.0.0, Culture=en, PublicKeyToken=e8123117d7ba9ae38
    
Ссылка на расположение при создании **определения New-OfficeWebAppsExcelUserDefinedFunction** на Office Online Server. 
  
> [!NOTE]
> Office Online Server не поддерживает UDF, расположенные на сетевых акциях. 
  
## <a name="enable-udfs-on-office-online-server"></a>Включить UDF на Office Online Server 

Когда администратор создает новую ферму Office серверов веб-приложений с помощью командулета [New-OfficeWebAppsFarm](https://docs.microsoft.com/powershell/module/officewebapps/new-officewebappsfarm?view=officewebapps-ps) Windows PowerShell, сборки UDF отключены по умолчанию. Значение по умолчанию **флага ExcelUdfsAllowed** является ложным. 
  
Чтобы включить UDF, запустите следующую команду Windows PowerShell в Office Online Server после создания фермы Office веб-приложений Server.
  
`Set-OfficeWebAppsFarm - ExcelUdfsAllowed:$true`
  
## <a name="create-udf-definitions-on-office-online-server"></a>Создание определений UDF на Office Online Server

После того как вы включаете UDFs, необходимо создать определение для двоичного, который содержит UDFs. Чтобы создать определение для двоичного двоичного файла UDF на Office Online Server, используйте комлет **New-OfficeWebAppsExcelUserDefinedFunction.** В этом комлете содержатся следующие параметры: 
  
- **Assembly**
    
- **AssemblyLocation**
    
- **Включить** (установить значение False по умолчанию) 
    
- **Описание**
    
В следующих примерах покажите, как создавать определения UDF.
  
`New-OfficeWebAppsExcelUserDefinedFunction -Assembly c:\myudf.dll -AssemblyLocation LocalFile -Enable:$true -Description "My Server UDFs"`
  
`New-OfficeWebAppsExcelUserDefinedFunction -Assembly "CompanyName.Hierarchichal.MyUdfNamespace.MyUdfClassName.dll, Version=1.1.0.0, Culture=en, PublicKeyToken=e8123117d7ba9ae38" -AssemblyLocation GAC -Enable:$true -Description "My GAC Server UDFs"`
  
После создания новой ссылки UDF запустите **iisreset** на сервере, чтобы немедленно получить ссылку. 
  
## <a name="additional-office-online-server-udf-windows-powershell-commands"></a>Дополнительные Office Online Server UDF Windows PowerShell команд

Используйте следующие Windows PowerShell для работы с UDFs:
  
- **Get-OfficeWebAppsExcelUserDefinedFunction** (без необходимых параметров) — возвращает список определений UDF, настроенных на Office Online Server. 
    
- **Set-OfficeWebAppsExcelUserDefinedFunction** (необходимый параметр identity) — задает свойства для существующих определений UDF. 
    
- **Remove-OfficeWebAppsExcelUserDefinedFunction** (необходимый параметр identity) — удаляет существующие определения UDF. 
    
## <a name="udf-sample"></a>Пример UDF

В следующем примере файла приводится пример книги с использованием двоичного файла UDF и UDF:
  
- [BooleanDataType.xlsx](https://download.microsoft.com/download/6/7/F/67F724FD-1186-4209-BFF1-FBFD99E959D9/User%20Defined%20Function%20Assemblies/BooleanDataType.xlsx): пример книги, использующей UDF  
    
## <a name="see-also"></a>См. также

- [Настройка параметров администрирования Excel Online](https://docs.microsoft.com/officeonlineserver/configure-excel-online-administrative-settings)  
- [Office Online Server](https://docs.microsoft.com/officeonlineserver/office-online-server)
    


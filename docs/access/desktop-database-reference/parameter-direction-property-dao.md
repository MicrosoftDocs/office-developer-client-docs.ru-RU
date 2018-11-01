---
title: Parameter.Direction Property (DAO)
TOCTitle: Direction Property
ms:assetid: b78c87ff-1181-21ef-7126-92d309751005
ms:mtpsurl: https://msdn.microsoft.com/library/Ff822422(v=office.15)
ms:contentKeyID: 48547300
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1053586
f1_categories:
- Office.Version=v15
ms.openlocfilehash: c06fbf6bb3424e776e21f32343c8cdb8a795b604
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25877109"
---
# <a name="parameterdirection-property-dao"></a>Parameter.Direction Property (DAO)


**Применимо к**: Access 2013, Office 2013


## <a name="syntax"></a>Синтаксис

*выражение* . Направление

*выражение* Переменная, которая представляет собой объект- **параметр** .

## <a name="remarks"></a>Замечания

Параметр или возвращаемое значение — это значение типа Long, которое может быть установлено одно из констант **[ParameterDirectionEnum](parameterdirectionenum-enumeration-dao.md)** .

Используйте свойство **направление** для определения, является ли параметр входного параметра, выходного параметра, или возвращаемое значение из процедуры. Некоторые драйвера ODBC не предоставляют сведения о направление параметров ВЫБЕРИТЕ оператор или вызов процедуры. В таких случаях необходимо установить направление до выполнения запроса.

Например, следующая процедура возвращает значение из хранимую процедуру с именем «Начало\_Сотрудники»:

{? = вызов get\_сотрудников}

Этот вызов создает один параметр — возвращаемое значение. Необходимо задать направление для этого параметра **dbParamOutput** или **dbParamReturnValue** перед выполнением **[QueryDef](querydef-object-dao.md)**.

Необходимо установить все указания параметра за исключением **dbParamInput** перед доступ к или установки значений параметров и перед выполнением **QueryDef**.

Следует использовать **dbParamReturnValue** возвращаемые значения, но в тех случаях, где этот параметр не поддерживается драйвер или на сервере, можно использовать **dbParamOutput** вместо этого.

Драйвер Microsoft SQL Server автоматически устанавливает свойство **направление** для всех параметров процедуры. Не все драйверы ODBC можно определить направление параметра запроса. В таких случаях необходимо установить направление до выполнения запроса.

## <a name="example"></a>Пример

В этом примере используется свойство **направление** для настройки параметров запроса к источнику данных ODBC.

```vb 
Sub DirectionX() 
 
 Dim wrkMain As Workspace 
 Dim conMain As Connection 
 Dim qdfTemp As QueryDef 
 Dim rstTemp As Recordset 
 Dim strSQL As String 
 Dim intLoop As Integer 
 
 ' Create ODBC workspace and open a connection to a 
 ' Microsoft SQL Server database. 
 Set wrkMain = CreateWorkspace("ODBCWorkspace", _ 
 "admin", "", dbUseODBC) 
 
 ' Note: The DSN referenced below must be configured to 
 ' use Microsoft Windows NT Authentication Mode to 
 ' authorize user access to the Microsoft SQL Server. 
 Set conMain = wrkMain.OpenConnection("Publishers", _ 
 dbDriverNoPrompt, False, _ 
 "ODBC;DATABASE=pubs;DSN=Publishers") 
 
 ' Set SQL string to call the stored procedure 
 ' getempsperjob. 
 strSQL = "{ call getempsperjob (?, ?) }" 
 
 Set qdfTemp = conMain.CreateQueryDef("", strSQL) 
 
 With qdfTemp 
 ' Indicate that the two query parameters will only 
 ' pass information to the stored procedure. 
 .Parameters(0).Direction = dbParamInput 
 .Parameters(1).Direction = dbParamInput 
 
 ' Assign initial parameter values. 
 .Parameters(0) = "0877" 
 .Parameters(1) = 0 
 
 Set rstTemp = .OpenRecordset() 
 
 With rstTemp 
 ' Loop through all valid values for the second 
 ' parameter. For each value, requery the recordset 
 ' to obtain the correct results and then print out 
 ' the contents of the recordset. 
 For intLoop = 1 To 14 
 qdfTemp.Parameters(1) = intLoop 
 .Requery 
 Debug.Print "Publisher = " & _ 
 qdfTemp.Parameters(0) & _ 
 ", job = " & intLoop 
 Do While Not .EOF 
 Debug.Print , .Fields(0), .Fields(1) 
 .MoveNext 
 Loop 
 Next intLoop 
 .Close 
 End With 
 
 End With 
 
 conMain.Close 
 wrkMain.Close 
 
End Sub 
 
```


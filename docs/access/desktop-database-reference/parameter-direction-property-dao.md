---
title: Свойство Parameter.Direction (DAO)
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
localization_priority: Normal
ms.openlocfilehash: 3260fd3f01e8ca22d5be4f8d14f6376c31e2735a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32288093"
---
# <a name="parameterdirection-property-dao"></a>Свойство Parameter.Direction (DAO)


**Область применения**: Access 2013, Office 2013


## <a name="syntax"></a>Синтаксис

*выражение .* Направление

*выражение* Переменная, представляюная объект **Parameter.**

## <a name="remarks"></a>Заметки

Значение параметра или возвращаемого значения — long, которое можно установить как одну из **[констант ParameterDirectionEnum.](parameterdirectionenum-enumeration-dao.md)**

Используйте свойство **Direction,** чтобы определить, является ли параметр входным параметром, выходным параметром, и тем, и другим, или возвращаемого значения из процедуры. Некоторые драйверы ODBC не предоставляют сведения о направлении параметров для вызова инструкции или процедуры SELECT. В таких случаях необходимо установить направление перед выполнением запроса.

Например, следующая процедура возвращает значение из хранимой процедуры с именем "get \_ employees":

{? = call get \_ employees}

При этом вызове создается один параметр — возвращаемая величина. Перед выполнением **[QueryDef](querydef-object-dao.md)** необходимо установить для этого параметра направление **dbParamOutput** или **dbParamReturnValue.**

Необходимо установить все направления параметров, кроме **dbParamInput,** перед доступом или установкой значений параметров и перед выполнением **QueryDef.**

Для возвращаемого значения следует использовать **dbParamReturnValue,** но в случаях, когда этот параметр не поддерживается драйвером или сервером, вместо него можно использовать **dbParamOutput.**

Драйвер Microsoft SQL Server автоматически задает свойство **Direction** для всех параметров процедуры. Не все драйверы ODBC могут определить направление параметра запроса. В таких случаях необходимо установить направление перед выполнением запроса.

## <a name="example"></a>Пример

В этом примере **свойство Direction** используется для настройки параметров запроса для источника данных ODBC.

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


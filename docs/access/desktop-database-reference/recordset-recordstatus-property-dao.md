---
title: Recordset.RecordStatus Property (DAO)
TOCTitle: RecordStatus Property
ms:assetid: 6fbd6909-6191-d7be-9a3a-1e9908dacc2b
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195591(v=office.15)
ms:contentKeyID: 48545543
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1102617
f1_categories:
- Office.Version=v15
ms.openlocfilehash: d1300538f1373929b4ed2bcd4fcd0be78574ae21
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25871922"
---
# <a name="recordsetrecordstatus-property-dao"></a>Recordset.RecordStatus Property (DAO)


**Применимо к**: Access 2013, Office 2013

## <a name="syntax"></a>Синтаксис

*выражение* . RecordStatus

*выражение* Переменная, которая представляет собой объект **набора записей** .

## <a name="remarks"></a>Замечания

Значение свойства **RecordStatus** указывает ли текущей записи будут принимать участие в следующее обновление оптимистичный пакета.

Когда пользователь изменяет запись, **RecordStatus** для этой записи автоматически изменяет **dbRecordModified**. Аналогично Если добавить или удалить записи **RecordStatus** отражает соответствующие константу. При использовании метода **[обновления](recordset-update-method-dao.md)** пакетного режима DAO будут отправлять соответствующие операции к удаленному серверу для каждой записи на основе свойства **RecordStatus** эту запись.

## <a name="example"></a>Пример

В этом примере с помощью свойства **RecordStatus** и **DefaultCursorDriver** для отображения способ отслеживания изменений в локальном **набора записей** во время обновления пакета. Функция RecordStatusOutput является обязательным для выполнения этой процедуры.

```vb 
Sub RecordStatusX() 
 
 Dim wrkMain As Workspace 
 Dim conMain As Connection 
 Dim rstTemp As Recordset 
 
 Set wrkMain = CreateWorkspace("ODBCWorkspace", _ 
 "admin", "", dbUseODBC) 
 ' This DefaultCursorDriver setting is required for 
 ' batch updating. 
 wrkMain.DefaultCursorDriver = dbUseClientBatchCursor 
 
 ' Note: The DSN referenced below must be configured to 
 ' use Microsoft Windows NT Authentication Mode to 
 ' authorize user access to the Microsoft SQL Server. 
 Set conMain = wrkMain.OpenConnection("Publishers", _ 
 dbDriverNoPrompt, False, _ 
 "ODBC;DATABASE=pubs;DSN=Publishers") 
 
 ' The following locking argument is required for 
 ' batch updating. 
 Set rstTemp = conMain.OpenRecordset( _ 
 "SELECT * FROM authors", dbOpenDynaset, 0, _ 
 dbOptimisticBatch) 
 
 With rstTemp 
 .MoveFirst 
 Debug.Print "Original record: " & !au_lname 
 Debug.Print , RecordStatusOutput2(.RecordStatus) 
 
 .Edit 
 !au_lname = "Bowen" 
 .Update 
 Debug.Print "Edited record: " & !au_lname 
 Debug.Print , RecordStatusOutput2(.RecordStatus) 
 
 .AddNew 
 !au_lname = "NewName" 
 .Update 
 Debug.Print "New record: " & !au_lname 
 Debug.Print , RecordStatusOutput2(.RecordStatus) 
 
 .Delete 
 Debug.Print "Deleted record: " & !au_lname 
 Debug.Print , RecordStatusOutput2(.RecordStatus) 
 
 ' Close the local recordset without updating the 
 ' data on the server. 
 .Close 
 End With 
 
 conMain.Close 
 wrkMain.Close 
 
End Sub 
 
Function RecordStatusOutput(lngTemp As Long) As String 
 
 Dim strTemp As String 
 
 strTemp = "" 
 
 ' Construct an output string based on the RecordStatus 
 ' value. 
If lngTemp = dbRecordUnmodified Then _ 
 strTemp = "[dbRecordUnmodified]" 
 If lngTemp = dbRecordModified Then _ 
 strTemp = "[dbRecordModified]" 
 If lngTemp = dbRecordNew Then _ 
 strTemp = "[dbRecordNew]" 
 If lngTemp = dbRecordDeleted Then _ 
 strTemp = "[dbRecordDeleted]" 
 If lngTemp = dbRecordDBDeleted Then _ 
 strTemp = "[dbRecordDBDeleted]" 
 
 RecordStatusOutput = strTemp 
 
End Function 
 
```


---
title: Свойство Recordset. Рекордстатус (DAO)
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
localization_priority: Normal
ms.openlocfilehash: 85790f92258b0851762337c2f74f281546e3526a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32307611"
---
# <a name="recordsetrecordstatus-property-dao"></a>Свойство Recordset. Рекордстатус (DAO)


**Область применения**: Access 2013, Office 2013

## <a name="syntax"></a>Синтаксис

*Expression* . Рекордстатус

*expression*: переменная, представляющая объект **Recordset**.

## <a name="remarks"></a>Примечания

Значение свойства **рекордстатус** указывает, будет ли и как будет использоваться текущая запись в ходе следующего пакетного обновления с нежесткими пакетами.

Когда пользователь изменяет запись, **рекордстатус** для этой записи автоматически изменяется на **дбрекордмодифиед**. Аналогично, при добавлении или удалении записи **рекордстатус** отражает соответствующую константу. После этого при использовании метода **[обновления](recordset-update-method-dao.md)** в пакетном режиме DAO передает соответствующую операцию удаленному серверу для каждой записи на основе свойства **рекордстатус** записи.

## <a name="example"></a>Пример

В этом примере используются свойства **рекордстатус** и **дефаулткурсордривер** , чтобы показать, как изменения локального **набора записей** отслеживаются во время пакетного обновления. Для выполнения этой процедуры требуется функция Рекордстатусаутпут.

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


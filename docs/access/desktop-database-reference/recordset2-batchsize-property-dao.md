---
title: Свойство Recordset2. BatchSize (DAO)
TOCTitle: BatchSize Property
ms:assetid: fa7f12f6-36c8-5aad-31d2-668cfe46f9f7
ms:mtpsurl: https://msdn.microsoft.com/library/Ff837054(v=office.15)
ms:contentKeyID: 48548846
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: f615823f99e2fdaa50a051d89a90c8f85a6ec841
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32307471"
---
# <a name="recordset2batchsize-property-dao"></a>Свойство Recordset2. BatchSize (DAO)


**Область применения**: Access 2013, Office 2013

## <a name="syntax"></a>Синтаксис

*Expression* . BatchSize

*Expression (выражение* ) Переменная, представляющая объект **Recordset2** .

## <a name="remarks"></a>Замечания

Свойство **BatchSize** определяет размер пакета, используемый при отправке инструкций на сервер при пакетном обновлении. Значение свойства определяет количество операторов, отправляемых на сервер, в одном буфере команд. По умолчанию 15 операторов отправляются на сервер в каждом пакете. Это свойство можно изменить в любое время. Если сервер базы данных не поддерживает пакетную обработку инструкций, для этого свойства можно задать значение 1, в результате чего каждый оператор будет отправлен отдельно.

## <a name="example"></a>Пример

В этом примере используются свойства **BatchSize** и **UpdateOptions** для управления аспектами обновления пакетов для указанного объекта Recordset.

```vb
Sub BatchSizeX() 
 
 Dim wrkMain As Workspace 
 Dim conMain As Connection 
 Dim rstTemp As Recordset2 
 
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
 "SELECT * FROM roysched", dbOpenDynaset, 0, _ 
 dbOptimisticBatch) 
 
 With rstTemp 
 ' Increase the number of statements sent to the server 
 ' during a single batch update, thereby reducing the 
 ' number of times an update would have to access the 
 ' server. 
 .BatchSize = 25 
 
 ' Change the UpdateOptions property so that the WHERE 
 ' clause of any batched statements going to the server 
 ' will include any updated columns in addition to the 
 ' key column(s). Also, any modifications to records 
 ' will be made by deleting the original record 
 ' and adding a modified version rather than just 
 ' modifying the original record. 
 .UpdateOptions = dbCriteriaModValues + _ 
 dbCriteriaDeleteInsert 
 
 ' Engage in batch updating using the new settings 
 ' above. 
 ' ... 
 
 .Close 
 End With 
 
 conMain.Close 
 wrkMain.Close 
 
End Sub 
 
```


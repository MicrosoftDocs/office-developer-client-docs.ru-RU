---
title: Recordset.UpdateOptions Property (DAO)
TOCTitle: UpdateOptions Property
ms:assetid: 14ab955d-1c5a-dc76-8dbf-dbca49816bc8
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845468(v=office.15)
ms:contentKeyID: 48543391
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1101185
f1_categories:
- Office.Version=v15
ms.openlocfilehash: b39b9920625d970a51feadc706a3c5ff62359e53
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25884354"
---
# <a name="recordsetupdateoptions-property-dao"></a>Recordset.UpdateOptions Property (DAO)


**Применимо к**: Access 2013, Office 2013

## <a name="syntax"></a>Синтаксис

*выражение* . UpdateOptions

*выражение* Переменная, которая представляет собой объект **набора записей** .

## <a name="remarks"></a>Замечания

При выполнении пакетного режима **[обновления](recordset-update-method-dao.md)** DAO и текущей позиции пакета клиентской библиотеки создать ряд инструкций SQL UPDATE, внесите необходимые изменения. Для каждого обновления для изоляции записей, которые помечены как измененный свойством **[RecordStatus](recordset-recordstatus-property-dao.md)** создается инструкцию SQL. Так как некоторые удаленных серверов с помощью триггеров или другие способы целостность данных, он часто необходимо ограничить поля обновляется только теми, которые повлияет переход. 

Чтобы сделать это, присвойте свойству **UpdateOptions** к одной из констант **dbCriteriaKey**, **dbCriteriaModValues**, **dbCriteriaAllCols**или **dbCriteriaTimeStamp**. Таким образом, выполняется только абсолютный минимальный объем кода триггер. В результате операции обновления выполняется быстрее и с меньшим количеством возможных ошибок.

Также можно объединять константы **dbCriteriaDeleteInsert** или **dbCriteriaUpdate** , чтобы определить, следует ли использовать набор SQL DELETE и инструкций INSERT или инструкции SQL UPDATE для каждого обновления при отправке пакетные изменения на сервере. В первом случае две отдельные операции требуются для обновления записи. В некоторых случаях особенно где удаленная система implements удаления, вставки и обновления триггеров, выбрав правильное значение свойства **UpdateOptions** можно значительно повысить производительность.

Если не указать любой константы, будет использоваться **dbCriteriaUpdate** и **dbCriteriaKey** .

Недавно добавленных записей всегда будет выдавать инструкции INSERT и удаленных записей всегда будет выдавать инструкций DELETE, поэтому это свойство применяется только к как библиотека курсора обновляет измененные записи.

## <a name="example"></a>Пример

В этом примере использует **BatchSize** и **UpdateOptions** свойства для доступа к параметрам обновление любого пакета для указанного объекта **набора записей** .

```vb 
Sub BatchSizeX() 
 
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


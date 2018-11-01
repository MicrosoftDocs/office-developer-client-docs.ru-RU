---
title: Recordset2.BatchSize Property (DAO)
TOCTitle: BatchSize Property
ms:assetid: fa7f12f6-36c8-5aad-31d2-668cfe46f9f7
ms:mtpsurl: https://msdn.microsoft.com/library/Ff837054(v=office.15)
ms:contentKeyID: 48548846
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: edb0f18e68021bf6e23e006d5d8e37e6eb6d816c
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25867953"
---
# <a name="recordset2batchsize-property-dao"></a>Recordset2.BatchSize Property (DAO)


**Применимо к**: Access 2013, Office 2013

## <a name="syntax"></a>Синтаксис

*выражение* . Размер пакета

*выражение* Переменная, которая представляет собой объект- **Recordset2** .

## <a name="remarks"></a>Замечания

Свойство **BatchSize** определяет пакет размер, используемый при отправке операторов на сервер в пакет обновления. Значение свойства определяет число операторов, отправляемых на сервер в один буфер команд. По умолчанию 15 операторы отправляются на сервер в каждом пакете. Это свойство можно изменить в любое время. Если сервер базы данных не поддерживает оператор пакетной обработки, можно этому свойству присвоено значение 1, вызывающие каждого оператора отправить отдельно.

## <a name="example"></a>Пример

В этом примере используются **BatchSize** и **UpdateOptions** свойства для доступа к параметрам любого пакета обновления для указанного объекта набора записей.

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


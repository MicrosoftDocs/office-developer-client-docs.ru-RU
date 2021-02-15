---
title: Recordset2.BatchCollisionCount (DAO)
TOCTitle: BatchCollisionCount Property
ms:assetid: 997dfbb3-673c-8813-f51b-ab8d95093c4f
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197961(v=office.15)
ms:contentKeyID: 48546514
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 33650b9fdbaf7fbc9266c8c778199e1138cd5b21
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32307485"
---
# <a name="recordset2batchcollisioncount-property-dao"></a>Recordset2.BatchCollisionCount (DAO)


**Область применения**: Access 2013, Office 2013

## <a name="syntax"></a>Синтаксис

*выражение .* BatchCollisionCount

*выражение* Переменная, представляюная объект **Recordset2.**

## <a name="remarks"></a>Заметки

Это свойство указывает, сколько записей столкнулось с столкновениями или не удалось обновить их во время последней попытки пакетного обновления. Значение этого свойства соответствует количеству закладок в свойстве **[BatchCollisions.](recordset2-batchcollisions-property-dao.md)**

Если для свойства **[bookmark](recordset2-bookmark-property-dao.md)** рабочего объекта **Recordset** задаваются значения закладок в массиве **BatchCollisions,** можно перейти **[](recordset2-update-method-dao.md)** к каждой записи, которая не прошла последние пакетные операции обновления.

После исправления записей столкновений можно повторно  использовать метод обновления в пакетном режиме. На этом этапе DAO пытается повторить пакетное обновление, и свойство **BatchCollisions** снова отражает набор записей, которые не удалось вторую попытку. Все записи, которые были успешными в предыдущей попытке, не отправляются в текущей попытке, так как теперь у них есть свойство **[RecordStatus](recordset2-recordstatus-property-dao.md)** **dbRecordUnmodified.** Этот процесс может продолжаться до тех пор, пока возникают конфликты, или до тех пор, пока вы не закроете набор результатов и откажутся от обновлений.

## <a name="example"></a>Пример

В этом примере используются свойство **BatchCollisionCount** и метод **Update**, чтобы продемонстрировать пакетное обновление с разрешением всех конфликтов путем принудительного пакетного обновления.

```vb 
Sub BatchX() 
 
 Dim wrkMain As Workspace 
 Dim conMain As Connection 
 Dim rstTemp As Recordset2 
 Dim intLoop As Integer 
 Dim strPrompt As String 
 
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
 ' batch updating. It is also required that a table 
 ' with a primary key is used. 
 Set rstTemp = conMain.OpenRecordset( _ 
 "SELECT * FROM roysched", dbOpenDynaset, 0, _ 
 dbOptimisticBatch) 
 
 With rstTemp 
 ' Modify data in local recordset. 
 Do While Not .EOF 
 .Edit 
 If !royalty <= 20 Then 
 !royalty = !royalty - 4 
 Else 
 !royalty = !royalty + 2 
 End If 
 .Update 
 .MoveNext 
 Loop 
 
 ' Attempt a batch update. 
 .Update dbUpdateBatch 
 
 ' If there are collisions, give the user the option 
 ' of forcing the changes or resolving them 
 ' individually. 
 If .BatchCollisionCount > 0 Then 
 strPrompt = "There are collisions. " & vbCr & _ 
 "Do you want the program to force " & _ 
 vbCr & "an update using the local data?" 
 If MsgBox(strPrompt, vbYesNo) = vbYes Then _ 
 .Update dbUpdateBatch, True 
 End If 
 
 .Close 
 End With 
 
 conMain.Close 
 wrkMain.Close 
 
End Sub 
 
```


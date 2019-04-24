---
title: Свойство Recordset2. Батчколлисионкаунт (DAO)
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
# <a name="recordset2batchcollisioncount-property-dao"></a>Свойство Recordset2. Батчколлисионкаунт (DAO)


**Область применения**: Access 2013, Office 2013

## <a name="syntax"></a>Синтаксис

*Expression* . Батчколлисионкаунт

*Expression (выражение* ) Переменная, представляющая объект **Recordset2** .

## <a name="remarks"></a>Замечания

Это свойство указывает, сколько записей столкнулось с конфликтами или в противном случае не удалось выполнить обновление во время последней попытки пакетного обновления. Значение этого свойства соответствует количеству закладок в свойстве **[батчколлисионс](recordset2-batchcollisions-property-dao.md)** .

Если присвоить свойству **[закладки](recordset2-bookmark-property-dao.md)** рабочего объекта **Recordset** значения закладки в массиве **батчколлисионс** , можно перейти к каждой записи, для которой не удалось выполнить последнюю операцию пакетного **[обновления](recordset2-update-method-dao.md)** .

После исправления записей о конфликтах можно повторно вызвать метод **обновления** в пакетном режиме. На этом шаге DAO предпринимает попытку выполнить еще одно пакетное обновление, а свойство **батчколлисионс** еще раз отражает набор записей, которые не удалось выполнить вторую попытку. Все записи, которые были успешно выполнены в предыдущей попытке, не отправляются в текущей попытке, так как теперь у них есть свойство **[Рекордстатус](recordset2-recordstatus-property-dao.md)** **дбрекордунмодифиед**. Этот процесс может продолжаться до тех пор, пока не будут выполнены конфликты, или пока не будут отменены все изменения и закрыть результирующий набор.

## <a name="example"></a>Пример

В этом примере используется свойство **батчколлисионкаунт** и метод **Update** для демонстрации пакетного обновления на то, какие конфликты разрешаются путем принудительного обновления пакета.

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


---
title: Свойство Connection.StillExecuting (DAO)
TOCTitle: StillExecuting Property
ms:assetid: 0121f98a-cc23-5b5e-9a75-28307404a9a3
ms:mtpsurl: https://msdn.microsoft.com/library/Ff844743(v=office.15)
ms:contentKeyID: 48542927
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 616e2bc6e374d7aba17c5cd07030469d8941014c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32295795"
---
# <a name="connectionstillexecuting-property-dao"></a>Свойство Connection.StillExecuting (DAO)

**Область применения**: Access 2013, Office 2013

## <a name="syntax"></a>Синтаксис

*выражения* . StillExecuting

*выражение*: переменная, представляющая объект **Connection**.

## <a name="remarks"></a>Примечания

Используйте **свойство StillExecuting,** чтобы определить, завершен ли  последний метод асинхронного выполнения или **OpenConnection** (то есть метод, выполненный с помощью параметра **dbRunAsync).** Несмотря на то, что свойство **StillExecuting** **является True,** доступ к любому возвращенного объекта невозможно получить.

После возвращения **свойства StillExecuting** **False** после вызова **OpenConnection,**  возвращаемого связанному объекту Подключения, можно ссылаться на объект. До тех пор, пока **StillExecuting** остается **True,** объект может не ссылаться, кроме как на чтение свойства **StillExecuting.**

Чтобы завершить выполнение задачи в процессе выполнения, используйте метод **[Cancel.](connection-cancel-method-dao.md)**

## <a name="example"></a>Пример

В этом примере свойство **StillExecuting** и метод **Cancel** используются для асинхронного открытия объекта **Подключения.**

```vb
    Sub CancelConnectionX() 
     
     Dim wrkMain As Workspace 
     Dim conMain As Connection 
     Dim sngTime As Single 
     
     Set wrkMain = CreateWorkspace("ODBCWorkspace", _ 
     "admin", "", dbUseODBC) 
     ' Open the connection asynchronously. 
     
     ' Note: The DSN referenced below must be configured to 
     ' use Microsoft Windows NT Authentication Mode to 
     ' authorize user access to the Microsoft SQL Server. 
     Set conMain = wrkMain.OpenConnection("Publishers", _ 
     dbDriverNoPrompt + dbRunAsync, False, _ 
     "ODBC;DATABASE=pubs;DSN=Publishers") 
     
     sngTime = Timer 
     
     ' Wait five seconds. 
     Do While Timer - sngTime < 5 
     Loop 
     
     ' If the connection has not been made, ask the user 
     ' if she wants to keep waiting. If she does not, cancel 
     ' the connection and exit the procedure. 
     Do While conMain.StillExecuting 
     
     If MsgBox("No connection yet--keep waiting?", _ 
     vbYesNo) = vbNo Then 
     conMain.Cancel 
     MsgBox "Connection cancelled!" 
     wrkMain.Close 
     Exit Sub 
     End If 
     
     Loop 
     
     With conMain 
     ' Use the Connection object conMain. 
     .Close 
     End With 
     
     wrkMain.Close 
     
    End Sub
```

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
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28719934"
---
# <a name="connectionstillexecuting-property-dao"></a>Свойство Connection.StillExecuting (DAO)

**Применимо к**: Access 2013, Office 2013

## <a name="syntax"></a>Синтаксис

*выражение* . StillExecuting

*выражение* Переменная, которая содержит объект **подключения** .

## <a name="remarks"></a>Замечания

Свойство **StillExecuting** определяет наиболее недавно вызванный асинхронный метод **OpenConnection** (то есть, метод выполнен с помощью параметра **dbRunAsync** ) или **выполнить** завершена. Хотя свойство **StillExecuting** имеет **значение True**, любой возвращенный объект не были доступны.

Как только свойство **StillExecuting** возвращает **значение False**, следующий за вызовом **OpenConnection** , которое возвращает связанный объект **подключения** можно ссылка на объект. До тех пор, пока **StillExecuting** остается равным **True**, объект не может существовать ссылок, отличный от для чтения свойство **StillExecuting** .

Используйте метод **[Cancel](connection-cancel-method-dao.md)** для завершения выполнения задачи в процессе выполнения.

## <a name="example"></a>Пример

В этом примере используется свойство **StillExecuting** и метод **Cancel** асинхронно Открытие объект **подключения** .

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

---
title: Connection.Cancel Method (DAO)
TOCTitle: Cancel Method
ms:assetid: 43ad7b64-823d-3fac-e4d4-5e9514f60011
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192953(v=office.15)
ms:contentKeyID: 48544509
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: e81c73b7dd42d437eecdc3bd8e2ef36f0ef49489
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25882751"
---
# <a name="connectioncancel-method-dao"></a>Connection.Cancel Method (DAO)

**Применимо к**: Access 2013, Office 2013

## <a name="syntax"></a>Синтаксис

*выражение* . Отмена

*выражение* Переменная, которая содержит объект **подключения** .

## <a name="remarks"></a>Замечания

Использование метода **Cancel** для завершения выполнения асинхронного вызова метода **Execute** или **OpenConnection** (то есть, метод был вызван с параметром dbRunAsync). **Отменить** возвращает ошибку времени выполнения, если в метод, который вы пытаетесь прерывания не используется dbRunAsync.

Приводит к ошибке при после вызова метода **Отменить** , попробуйте для ссылки на объект, который будет создан с асинхронный вызов **OpenConnection** (то есть, объект **подключения** из которого вызывается **Отмена** метод).

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

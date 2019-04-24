---
title: Свойство Connection. Стиллексекутинг (DAO)
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
# <a name="connectionstillexecuting-property-dao"></a>Свойство Connection. Стиллексекутинг (DAO)

**Область применения**: Access 2013, Office 2013

## <a name="syntax"></a>Синтаксис

*Expression* . Стиллексекутинг

*Expression (выражение* ) Переменная, представляющая объект **Connection** .

## <a name="remarks"></a>Замечания

Используйте свойство **стиллексекутинг** , чтобы определить, завершен ли последний вызов метода асинхронного **выполнения** или **OpenConnection** (то есть метод, выполняемый с параметром **дбрунасинк** ). Несмотря на то, что свойство **стиллексекутинг** имеет **значение true**, доступ к возвращенному объекту невозможен.

После того как свойство **стиллексекутинг** возвращает **значение false**, после вызова **OpenConnection** , возвращающего связанный объект **Connection** , можно ссылаться на объект. До тех пор пока **стиллексекутинг** остается **true**, на объект не может быть ссылок, кроме чтения свойства **стиллексекутинг** .

Используйте метод **[Cancel](connection-cancel-method-dao.md)** , чтобы прекратить выполнение задачи в ходе выполнения.

## <a name="example"></a>Пример

В этом примере используется свойство **стиллексекутинг** и метод **Cancel** для асинхронного открытия объекта **Connection** .

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

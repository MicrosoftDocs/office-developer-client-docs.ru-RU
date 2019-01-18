---
title: Метод Connection.Cancel (DAO)
TOCTitle: Cancel Method
ms:assetid: 43ad7b64-823d-3fac-e4d4-5e9514f60011
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192953(v=office.15)
ms:contentKeyID: 48544509
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: a0826a30f22cc46eb6ff9a114dbf02cab1d9f76a
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28718933"
---
# <a name="connectioncancel-method-dao"></a><span data-ttu-id="54e6e-102">Метод Connection.Cancel (DAO)</span><span class="sxs-lookup"><span data-stu-id="54e6e-102">Connection.Cancel method (DAO)</span></span>

<span data-ttu-id="54e6e-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="54e6e-103">**Applies to**: Access 2013, Office 2013</span></span>

## <a name="syntax"></a><span data-ttu-id="54e6e-104">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="54e6e-104">Syntax</span></span>

<span data-ttu-id="54e6e-105">*выражение* . Отмена</span><span class="sxs-lookup"><span data-stu-id="54e6e-105">*expression* .Cancel</span></span>

<span data-ttu-id="54e6e-106">*выражение* Переменная, которая содержит объект **подключения** .</span><span class="sxs-lookup"><span data-stu-id="54e6e-106">*expression* A variable that represents a **Connection** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="54e6e-107">Замечания</span><span class="sxs-lookup"><span data-stu-id="54e6e-107">Remarks</span></span>

<span data-ttu-id="54e6e-108">Использование метода **Cancel** для завершения выполнения асинхронного вызова метода **Execute** или **OpenConnection** (то есть, метод был вызван с параметром dbRunAsync).</span><span class="sxs-lookup"><span data-stu-id="54e6e-108">Use the **Cancel** method to terminate execution of an asynchronous **Execute** or **OpenConnection** method call (that is, the method was invoked with the dbRunAsync option).</span></span> <span data-ttu-id="54e6e-109">**Отменить** возвращает ошибку времени выполнения, если в метод, который вы пытаетесь прерывания не используется dbRunAsync.</span><span class="sxs-lookup"><span data-stu-id="54e6e-109">**Cancel** will return a run-time error if dbRunAsync was not used in the method you're trying to terminate.</span></span>

<span data-ttu-id="54e6e-110">Приводит к ошибке при после вызова метода **Отменить** , попробуйте для ссылки на объект, который будет создан с асинхронный вызов **OpenConnection** (то есть, объект **подключения** из которого вызывается **Отмена** метод).</span><span class="sxs-lookup"><span data-stu-id="54e6e-110">An error will occur if, following a **Cancel** method call, you try to reference the object that would have been created by an asynchronous **OpenConnection** call (that is, the **Connection** object from which you called the **Cancel** method).</span></span>

## <a name="example"></a><span data-ttu-id="54e6e-111">Пример</span><span class="sxs-lookup"><span data-stu-id="54e6e-111">Example</span></span>

<span data-ttu-id="54e6e-112">В этом примере используется свойство **StillExecuting** и метод **Cancel** асинхронно Открытие объект **подключения** .</span><span class="sxs-lookup"><span data-stu-id="54e6e-112">This example uses the **StillExecuting** property and the **Cancel** method to asynchronously open a **Connection** object.</span></span>

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

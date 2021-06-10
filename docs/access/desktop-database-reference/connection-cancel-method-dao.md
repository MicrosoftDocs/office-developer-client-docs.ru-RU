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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32295970"
---
# <a name="connectioncancel-method-dao"></a><span data-ttu-id="d6f6d-102">Метод Connection.Cancel (DAO)</span><span class="sxs-lookup"><span data-stu-id="d6f6d-102">Connection.Cancel method (DAO)</span></span>

<span data-ttu-id="d6f6d-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="d6f6d-103">**Applies to**: Access 2013, Office 2013</span></span>

## <a name="syntax"></a><span data-ttu-id="d6f6d-104">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d6f6d-104">Syntax</span></span>

<span data-ttu-id="d6f6d-105">*выражения* . Отмена</span><span class="sxs-lookup"><span data-stu-id="d6f6d-105">*expression* .Cancel</span></span>

<span data-ttu-id="d6f6d-106">*выражение*: переменная, представляющая объект **Connection**.</span><span class="sxs-lookup"><span data-stu-id="d6f6d-106">*expression* A variable that represents a **Connection** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="d6f6d-107">Примечания</span><span class="sxs-lookup"><span data-stu-id="d6f6d-107">Remarks</span></span>

<span data-ttu-id="d6f6d-108">Используйте метод **Cancel** для прекращения выполнения асинхронного вызова метода **Выполнения** или **OpenConnection** (то есть метод вызывался с помощью параметра dbRunAsync).</span><span class="sxs-lookup"><span data-stu-id="d6f6d-108">Use the **Cancel** method to terminate execution of an asynchronous **Execute** or **OpenConnection** method call (that is, the method was invoked with the dbRunAsync option).</span></span> <span data-ttu-id="d6f6d-109">**Отмена** возвращает временную ошибку, если dbRunAsync не использовался в методе, который вы пытаетесь завершить.</span><span class="sxs-lookup"><span data-stu-id="d6f6d-109">**Cancel** will return a run-time error if dbRunAsync was not used in the method you're trying to terminate.</span></span>

<span data-ttu-id="d6f6d-110">Ошибка будет возникать,  если после вызова метода Отмены вы попытайтесь ссылаться на объект, созданный асинхронным вызовом **OpenConnection** (то есть объектом Подключения, из которого вы назвали метод  **Отмены).**</span><span class="sxs-lookup"><span data-stu-id="d6f6d-110">An error will occur if, following a **Cancel** method call, you try to reference the object that would have been created by an asynchronous **OpenConnection** call (that is, the **Connection** object from which you called the **Cancel** method).</span></span>

## <a name="example"></a><span data-ttu-id="d6f6d-111">Пример</span><span class="sxs-lookup"><span data-stu-id="d6f6d-111">Example</span></span>

<span data-ttu-id="d6f6d-112">В этом примере свойство **StillExecuting** и метод **Cancel** используются для асинхронного открытия объекта **Подключения.**</span><span class="sxs-lookup"><span data-stu-id="d6f6d-112">This example uses the **StillExecuting** property and the **Cancel** method to asynchronously open a **Connection** object.</span></span>

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

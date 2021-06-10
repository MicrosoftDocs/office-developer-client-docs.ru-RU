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
# <a name="connectionstillexecuting-property-dao"></a><span data-ttu-id="0ff35-102">Свойство Connection.StillExecuting (DAO)</span><span class="sxs-lookup"><span data-stu-id="0ff35-102">Connection.StillExecuting property (DAO)</span></span>

<span data-ttu-id="0ff35-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="0ff35-103">**Applies to**: Access 2013, Office 2013</span></span>

## <a name="syntax"></a><span data-ttu-id="0ff35-104">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="0ff35-104">Syntax</span></span>

<span data-ttu-id="0ff35-105">*выражения* . StillExecuting</span><span class="sxs-lookup"><span data-stu-id="0ff35-105">*expression* .StillExecuting</span></span>

<span data-ttu-id="0ff35-106">*выражение*: переменная, представляющая объект **Connection**.</span><span class="sxs-lookup"><span data-stu-id="0ff35-106">*expression* A variable that represents a **Connection** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="0ff35-107">Примечания</span><span class="sxs-lookup"><span data-stu-id="0ff35-107">Remarks</span></span>

<span data-ttu-id="0ff35-108">Используйте **свойство StillExecuting,** чтобы определить, завершен ли  последний метод асинхронного выполнения или **OpenConnection** (то есть метод, выполненный с помощью параметра **dbRunAsync).**</span><span class="sxs-lookup"><span data-stu-id="0ff35-108">Use the **StillExecuting** property to determine if the most recently called asynchronous **Execute** or **OpenConnection** method (that is, a method executed with the **dbRunAsync** option) is complete.</span></span> <span data-ttu-id="0ff35-109">Несмотря на то, что свойство **StillExecuting** **является True,** доступ к любому возвращенного объекта невозможно получить.</span><span class="sxs-lookup"><span data-stu-id="0ff35-109">While the **StillExecuting** property is **True**, any returned object cannot be accessed.</span></span>

<span data-ttu-id="0ff35-110">После возвращения **свойства StillExecuting** **False** после вызова **OpenConnection,**  возвращаемого связанному объекту Подключения, можно ссылаться на объект.</span><span class="sxs-lookup"><span data-stu-id="0ff35-110">Once the **StillExecuting** property returns **False**, following the **OpenConnection** call that returns the associated **Connection** object, the object can be referenced.</span></span> <span data-ttu-id="0ff35-111">До тех пор, пока **StillExecuting** остается **True,** объект может не ссылаться, кроме как на чтение свойства **StillExecuting.**</span><span class="sxs-lookup"><span data-stu-id="0ff35-111">So long as **StillExecuting** remains **True**, the object may not be referenced, other than to read the **StillExecuting** property.</span></span>

<span data-ttu-id="0ff35-112">Чтобы завершить выполнение задачи в процессе выполнения, используйте метод **[Cancel.](connection-cancel-method-dao.md)**</span><span class="sxs-lookup"><span data-stu-id="0ff35-112">Use the **[Cancel](connection-cancel-method-dao.md)** method to terminate execution of a task in progress.</span></span>

## <a name="example"></a><span data-ttu-id="0ff35-113">Пример</span><span class="sxs-lookup"><span data-stu-id="0ff35-113">Example</span></span>

<span data-ttu-id="0ff35-114">В этом примере свойство **StillExecuting** и метод **Cancel** используются для асинхронного открытия объекта **Подключения.**</span><span class="sxs-lookup"><span data-stu-id="0ff35-114">This example uses the **StillExecuting** property and the **Cancel** method to asynchronously open a **Connection** object.</span></span>

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

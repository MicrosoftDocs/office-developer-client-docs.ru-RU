---
title: Свойство Connection.StillExecuting (DAO)
TOCTitle: StillExecuting Property
ms:assetid: 0121f98a-cc23-5b5e-9a75-28307404a9a3
ms:mtpsurl: https://msdn.microsoft.com/library/Ff844743(v=office.15)
ms:contentKeyID: 48542927
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: efcac1b95fe4f58a6ebef39a51c57dda4f9866a3
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/02/2018
ms.locfileid: "25921070"
---
# <a name="connectionstillexecuting-property-dao"></a><span data-ttu-id="798c4-102">Свойство Connection.StillExecuting (DAO)</span><span class="sxs-lookup"><span data-stu-id="798c4-102">Connection.StillExecuting property (DAO)</span></span>

<span data-ttu-id="798c4-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="798c4-103">**Applies to**: Access 2013, Office 2013</span></span>

## <a name="syntax"></a><span data-ttu-id="798c4-104">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="798c4-104">Syntax</span></span>

<span data-ttu-id="798c4-105">*выражение* . StillExecuting</span><span class="sxs-lookup"><span data-stu-id="798c4-105">*expression* .StillExecuting</span></span>

<span data-ttu-id="798c4-106">*выражение* Переменная, которая содержит объект **подключения** .</span><span class="sxs-lookup"><span data-stu-id="798c4-106">*expression* A variable that represents a **Connection** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="798c4-107">Примечания</span><span class="sxs-lookup"><span data-stu-id="798c4-107">Remarks</span></span>

<span data-ttu-id="798c4-108">Свойство **StillExecuting** определяет наиболее недавно вызванный асинхронный метод **OpenConnection** (то есть, метод выполнен с помощью параметра **dbRunAsync** ) или **выполнить** завершена.</span><span class="sxs-lookup"><span data-stu-id="798c4-108">Use the **StillExecuting** property to determine if the most recently called asynchronous **Execute** or **OpenConnection** method (that is, a method executed with the **dbRunAsync** option) is complete.</span></span> <span data-ttu-id="798c4-109">Хотя свойство **StillExecuting** имеет **значение True**, любой возвращенный объект не были доступны.</span><span class="sxs-lookup"><span data-stu-id="798c4-109">While the **StillExecuting** property is **True**, any returned object cannot be accessed.</span></span>

<span data-ttu-id="798c4-110">Как только свойство **StillExecuting** возвращает **значение False**, следующий за вызовом **OpenConnection** , которое возвращает связанный объект **подключения** можно ссылка на объект.</span><span class="sxs-lookup"><span data-stu-id="798c4-110">Once the **StillExecuting** property returns **False**, following the **OpenConnection** call that returns the associated **Connection** object, the object can be referenced.</span></span> <span data-ttu-id="798c4-111">До тех пор, пока **StillExecuting** остается равным **True**, объект не может существовать ссылок, отличный от для чтения свойство **StillExecuting** .</span><span class="sxs-lookup"><span data-stu-id="798c4-111">So long as **StillExecuting** remains **True**, the object may not be referenced, other than to read the **StillExecuting** property.</span></span>

<span data-ttu-id="798c4-112">Используйте метод **[Cancel](connection-cancel-method-dao.md)** для завершения выполнения задачи в процессе выполнения.</span><span class="sxs-lookup"><span data-stu-id="798c4-112">Use the **[Cancel](connection-cancel-method-dao.md)** method to terminate execution of a task in progress.</span></span>

## <a name="example"></a><span data-ttu-id="798c4-113">Пример</span><span class="sxs-lookup"><span data-stu-id="798c4-113">Example</span></span>

<span data-ttu-id="798c4-114">В этом примере используется свойство **StillExecuting** и метод **Cancel** асинхронно Открытие объект **подключения** .</span><span class="sxs-lookup"><span data-stu-id="798c4-114">This example uses the **StillExecuting** property and the **Cancel** method to asynchronously open a **Connection** object.</span></span>

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

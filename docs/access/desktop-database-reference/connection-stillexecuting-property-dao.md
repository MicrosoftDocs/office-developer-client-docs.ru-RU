---
title: Connection.StillExecuting Property (DAO)
TOCTitle: StillExecuting Property
ms:assetid: 0121f98a-cc23-5b5e-9a75-28307404a9a3
ms:mtpsurl: https://msdn.microsoft.com/library/Ff844743(v=office.15)
ms:contentKeyID: 48542927
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 2ba2444146a0174e643c7ba98cbfd46225c5a491
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25874267"
---
# <a name="connectionstillexecuting-property-dao"></a><span data-ttu-id="804ad-102">Connection.StillExecuting Property (DAO)</span><span class="sxs-lookup"><span data-stu-id="804ad-102">Connection.StillExecuting Property (DAO)</span></span>

<span data-ttu-id="804ad-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="804ad-103">**Applies to**: Access 2013, Office 2013</span></span>

## <a name="syntax"></a><span data-ttu-id="804ad-104">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="804ad-104">Syntax</span></span>

<span data-ttu-id="804ad-105">*выражение* . StillExecuting</span><span class="sxs-lookup"><span data-stu-id="804ad-105">*expression* .StillExecuting</span></span>

<span data-ttu-id="804ad-106">*выражение* Переменная, которая содержит объект **подключения** .</span><span class="sxs-lookup"><span data-stu-id="804ad-106">*expression* A variable that represents a **Connection** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="804ad-107">Замечания</span><span class="sxs-lookup"><span data-stu-id="804ad-107">Remarks</span></span>

<span data-ttu-id="804ad-108">Свойство **StillExecuting** определяет наиболее недавно вызванный асинхронный метод **OpenConnection** (то есть, метод выполнен с помощью параметра **dbRunAsync** ) или **выполнить** завершена.</span><span class="sxs-lookup"><span data-stu-id="804ad-108">Use the **StillExecuting** property to determine if the most recently called asynchronous **Execute** or **OpenConnection** method (that is, a method executed with the **dbRunAsync** option) is complete.</span></span> <span data-ttu-id="804ad-109">Хотя свойство **StillExecuting** имеет **значение True**, любой возвращенный объект не были доступны.</span><span class="sxs-lookup"><span data-stu-id="804ad-109">While the **StillExecuting** property is **True**, any returned object cannot be accessed.</span></span>

<span data-ttu-id="804ad-110">Как только свойство **StillExecuting** возвращает **значение False**, следующий за вызовом **OpenConnection** , которое возвращает связанный объект **подключения** можно ссылка на объект.</span><span class="sxs-lookup"><span data-stu-id="804ad-110">Once the **StillExecuting** property returns **False**, following the **OpenConnection** call that returns the associated **Connection** object, the object can be referenced.</span></span> <span data-ttu-id="804ad-111">До тех пор, пока **StillExecuting** остается равным **True**, объект не может существовать ссылок, отличный от для чтения свойство **StillExecuting** .</span><span class="sxs-lookup"><span data-stu-id="804ad-111">So long as **StillExecuting** remains **True**, the object may not be referenced, other than to read the **StillExecuting** property.</span></span>

<span data-ttu-id="804ad-112">Используйте метод **[Cancel](connection-cancel-method-dao.md)** для завершения выполнения задачи в процессе выполнения.</span><span class="sxs-lookup"><span data-stu-id="804ad-112">Use the **[Cancel](connection-cancel-method-dao.md)** method to terminate execution of a task in progress.</span></span>

## <a name="example"></a><span data-ttu-id="804ad-113">Пример</span><span class="sxs-lookup"><span data-stu-id="804ad-113">Example</span></span>

<span data-ttu-id="804ad-114">В этом примере используется свойство **StillExecuting** и метод **Cancel** асинхронно Открытие объект **подключения** .</span><span class="sxs-lookup"><span data-stu-id="804ad-114">This example uses the **StillExecuting** property and the **Cancel** method to asynchronously open a **Connection** object.</span></span>

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

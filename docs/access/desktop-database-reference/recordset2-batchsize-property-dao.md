---
title: Свойство Recordset2.BATCHSIZE (DAO)
TOCTitle: BatchSize Property
ms:assetid: fa7f12f6-36c8-5aad-31d2-668cfe46f9f7
ms:mtpsurl: https://msdn.microsoft.com/library/Ff837054(v=office.15)
ms:contentKeyID: 48548846
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: f615823f99e2fdaa50a051d89a90c8f85a6ec841
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28711275"
---
# <a name="recordset2batchsize-property-dao"></a><span data-ttu-id="53f9d-102">Свойство Recordset2.BATCHSIZE (DAO)</span><span class="sxs-lookup"><span data-stu-id="53f9d-102">Recordset2.BatchSize property (DAO)</span></span>


<span data-ttu-id="53f9d-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="53f9d-103">**Applies to**: Access 2013, Office 2013</span></span>

## <a name="syntax"></a><span data-ttu-id="53f9d-104">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="53f9d-104">Syntax</span></span>

<span data-ttu-id="53f9d-105">*выражение* . Размер пакета</span><span class="sxs-lookup"><span data-stu-id="53f9d-105">*expression* .BatchSize</span></span>

<span data-ttu-id="53f9d-106">*выражение* Переменная, которая представляет собой объект- **Recordset2** .</span><span class="sxs-lookup"><span data-stu-id="53f9d-106">*expression* A variable that represents a **Recordset2** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="53f9d-107">Замечания</span><span class="sxs-lookup"><span data-stu-id="53f9d-107">Remarks</span></span>

<span data-ttu-id="53f9d-108">Свойство **BatchSize** определяет пакет размер, используемый при отправке операторов на сервер в пакет обновления.</span><span class="sxs-lookup"><span data-stu-id="53f9d-108">The **BatchSize** property determines the batch size used when sending statements to the server in a batch update.</span></span> <span data-ttu-id="53f9d-109">Значение свойства определяет число операторов, отправляемых на сервер в один буфер команд.</span><span class="sxs-lookup"><span data-stu-id="53f9d-109">The value of the property determines the number of statements sent to the server in one command buffer.</span></span> <span data-ttu-id="53f9d-110">По умолчанию 15 операторы отправляются на сервер в каждом пакете.</span><span class="sxs-lookup"><span data-stu-id="53f9d-110">By default, 15 statements are sent to the server in each batch.</span></span> <span data-ttu-id="53f9d-111">Это свойство можно изменить в любое время.</span><span class="sxs-lookup"><span data-stu-id="53f9d-111">This property can be changed at any time.</span></span> <span data-ttu-id="53f9d-112">Если сервер базы данных не поддерживает оператор пакетной обработки, можно этому свойству присвоено значение 1, вызывающие каждого оператора отправить отдельно.</span><span class="sxs-lookup"><span data-stu-id="53f9d-112">If a database server doesn't support statement batching, you can set this property to 1, causing each statement to be sent separately.</span></span>

## <a name="example"></a><span data-ttu-id="53f9d-113">Пример</span><span class="sxs-lookup"><span data-stu-id="53f9d-113">Example</span></span>

<span data-ttu-id="53f9d-114">В этом примере используются **BatchSize** и **UpdateOptions** свойства для доступа к параметрам любого пакета обновления для указанного объекта набора записей.</span><span class="sxs-lookup"><span data-stu-id="53f9d-114">This example uses the **BatchSize** and **UpdateOptions** properties to control aspects of any batch updating for the specified Recordset object.</span></span>

```vb
Sub BatchSizeX() 
 
 Dim wrkMain As Workspace 
 Dim conMain As Connection 
 Dim rstTemp As Recordset2 
 
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
 ' batch updating. 
 Set rstTemp = conMain.OpenRecordset( _ 
 "SELECT * FROM roysched", dbOpenDynaset, 0, _ 
 dbOptimisticBatch) 
 
 With rstTemp 
 ' Increase the number of statements sent to the server 
 ' during a single batch update, thereby reducing the 
 ' number of times an update would have to access the 
 ' server. 
 .BatchSize = 25 
 
 ' Change the UpdateOptions property so that the WHERE 
 ' clause of any batched statements going to the server 
 ' will include any updated columns in addition to the 
 ' key column(s). Also, any modifications to records 
 ' will be made by deleting the original record 
 ' and adding a modified version rather than just 
 ' modifying the original record. 
 .UpdateOptions = dbCriteriaModValues + _ 
 dbCriteriaDeleteInsert 
 
 ' Engage in batch updating using the new settings 
 ' above. 
 ' ... 
 
 .Close 
 End With 
 
 conMain.Close 
 wrkMain.Close 
 
End Sub 
 
```


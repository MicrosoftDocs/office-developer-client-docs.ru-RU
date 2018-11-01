---
title: Recordset.BatchSize Property (DAO)
TOCTitle: BatchSize Property
ms:assetid: f03dc505-682f-4b60-62f2-1bd088d873c4
ms:mtpsurl: https://msdn.microsoft.com/library/Ff836544(v=office.15)
ms:contentKeyID: 48548599
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1101179
f1_categories:
- Office.Version=v15
ms.openlocfilehash: e07a948a22a8101db2b2bffce3e6cde94c852668
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/01/2018
ms.locfileid: "25891235"
---
# <a name="recordsetbatchsize-property-dao"></a><span data-ttu-id="84b25-102">Recordset.BatchSize Property (DAO)</span><span class="sxs-lookup"><span data-stu-id="84b25-102">Recordset.BatchSize Property (DAO)</span></span>


<span data-ttu-id="84b25-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="84b25-103">**Applies to**: Access 2013, Office 2013</span></span>

## <a name="syntax"></a><span data-ttu-id="84b25-104">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="84b25-104">Syntax</span></span>

<span data-ttu-id="84b25-105">*выражение* . Размер пакета</span><span class="sxs-lookup"><span data-stu-id="84b25-105">*expression* .BatchSize</span></span>

<span data-ttu-id="84b25-106">*выражение* Переменная, которая представляет собой объект **набора записей** .</span><span class="sxs-lookup"><span data-stu-id="84b25-106">*expression* A variable that represents a **Recordset** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="84b25-107">Замечания</span><span class="sxs-lookup"><span data-stu-id="84b25-107">Remarks</span></span>

<span data-ttu-id="84b25-108">Свойство **BatchSize** определяет пакет размер, используемый при отправке операторов на сервер в пакет обновления.</span><span class="sxs-lookup"><span data-stu-id="84b25-108">The **BatchSize** property determines the batch size used when sending statements to the server in a batch update.</span></span> <span data-ttu-id="84b25-109">Значение свойства определяет число операторов, отправляемых на сервер в один буфер команд.</span><span class="sxs-lookup"><span data-stu-id="84b25-109">The value of the property determines the number of statements sent to the server in one command buffer.</span></span> <span data-ttu-id="84b25-110">По умолчанию 15 операторы отправляются на сервер в каждом пакете.</span><span class="sxs-lookup"><span data-stu-id="84b25-110">By default, 15 statements are sent to the server in each batch.</span></span> <span data-ttu-id="84b25-111">Это свойство можно изменить в любое время.</span><span class="sxs-lookup"><span data-stu-id="84b25-111">This property can be changed at any time.</span></span> <span data-ttu-id="84b25-112">Если сервер базы данных не поддерживает оператор пакетной обработки, можно этому свойству присвоено значение 1, вызывающие каждого оператора отправить отдельно.</span><span class="sxs-lookup"><span data-stu-id="84b25-112">If a database server doesn't support statement batching, you can set this property to 1, causing each statement to be sent separately.</span></span>

## <a name="example"></a><span data-ttu-id="84b25-113">Пример</span><span class="sxs-lookup"><span data-stu-id="84b25-113">Example</span></span>

<span data-ttu-id="84b25-114">В этом примере используются **BatchSize** и **UpdateOptions** свойства для доступа к параметрам любого пакета обновления для указанного объекта набора записей.</span><span class="sxs-lookup"><span data-stu-id="84b25-114">This example uses the **BatchSize** and **UpdateOptions** properties to control aspects of any batch updating for the specified Recordset object.</span></span>

```vb 
Sub BatchSizeX() 
 
 Dim wrkMain As Workspace 
 Dim conMain As Connection 
 Dim rstTemp As Recordset 
 
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


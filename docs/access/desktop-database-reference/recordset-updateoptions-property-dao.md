---
title: Recordset.UpdateOptions Property (DAO)
TOCTitle: UpdateOptions Property
ms:assetid: 14ab955d-1c5a-dc76-8dbf-dbca49816bc8
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845468(v=office.15)
ms:contentKeyID: 48543391
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1101185
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 065ca41d46f50911835d79989e39636b62b30b97
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25481733"
---
# <a name="recordsetupdateoptions-property-dao"></a><span data-ttu-id="5fa18-102">Recordset.UpdateOptions Property (DAO)</span><span class="sxs-lookup"><span data-stu-id="5fa18-102">Recordset.UpdateOptions Property (DAO)</span></span>


<span data-ttu-id="5fa18-103">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="5fa18-103">**Applies to**: Access 2013 | Office 2013</span></span>

## <a name="syntax"></a><span data-ttu-id="5fa18-104">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="5fa18-104">Syntax</span></span>

<span data-ttu-id="5fa18-105">*выражение* . UpdateOptions</span><span class="sxs-lookup"><span data-stu-id="5fa18-105">*expression* .UpdateOptions</span></span>

<span data-ttu-id="5fa18-106">*выражение* Переменная, которая представляет собой объект **набора записей** .</span><span class="sxs-lookup"><span data-stu-id="5fa18-106">*expression* A variable that represents a **Recordset** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="5fa18-107">Замечания</span><span class="sxs-lookup"><span data-stu-id="5fa18-107">Remarks</span></span>

<span data-ttu-id="5fa18-108">При выполнении пакетного режима **[обновления](recordset-update-method-dao.md)** DAO и текущей позиции пакета клиентской библиотеки создать ряд инструкций SQL UPDATE, внесите необходимые изменения.</span><span class="sxs-lookup"><span data-stu-id="5fa18-108">When a batch-mode **[Update](recordset-update-method-dao.md)** is executed, DAO and the client batch cursor library create a series of SQL UPDATE statements to make the needed changes.</span></span> <span data-ttu-id="5fa18-109">Для каждого обновления для изоляции записей, которые помечены как измененный свойством **[RecordStatus](recordset-recordstatus-property-dao.md)** создается инструкцию SQL.</span><span class="sxs-lookup"><span data-stu-id="5fa18-109">An SQL WHERE clause is created for each update to isolate the records that are marked as changed by the **[RecordStatus](recordset-recordstatus-property-dao.md)** property.</span></span> <span data-ttu-id="5fa18-110">Так как некоторые удаленных серверов с помощью триггеров или другие способы целостность данных, он часто необходимо ограничить поля обновляется только теми, которые повлияет переход.</span><span class="sxs-lookup"><span data-stu-id="5fa18-110">Because some remote servers use triggers or other ways to enforce referential integrity, is it often important to limit the fields being updated to just those affected by the change.</span></span> 

<span data-ttu-id="5fa18-111">Чтобы сделать это, присвойте свойству **UpdateOptions** к одной из констант **dbCriteriaKey**, **dbCriteriaModValues**, **dbCriteriaAllCols**или **dbCriteriaTimeStamp**.</span><span class="sxs-lookup"><span data-stu-id="5fa18-111">To do this, set the **UpdateOptions** property to one of the constants **dbCriteriaKey**, **dbCriteriaModValues**, **dbCriteriaAllCols**, or **dbCriteriaTimeStamp**.</span></span> <span data-ttu-id="5fa18-112">Таким образом, выполняется только абсолютный минимальный объем кода триггер.</span><span class="sxs-lookup"><span data-stu-id="5fa18-112">This way, only the absolute minimum amount of trigger code is executed.</span></span> <span data-ttu-id="5fa18-113">В результате операции обновления выполняется быстрее и с меньшим количеством возможных ошибок.</span><span class="sxs-lookup"><span data-stu-id="5fa18-113">As a result, the update operation is executed more quickly, and with fewer potential errors.</span></span>

<span data-ttu-id="5fa18-114">Также можно объединять константы **dbCriteriaDeleteInsert** или **dbCriteriaUpdate** , чтобы определить, следует ли использовать набор SQL DELETE и инструкций INSERT или инструкции SQL UPDATE для каждого обновления при отправке пакетные изменения на сервере.</span><span class="sxs-lookup"><span data-stu-id="5fa18-114">You can also concatenate either of the constants **dbCriteriaDeleteInsert** or **dbCriteriaUpdate** to determine whether to use a set of SQL DELETE and INSERT statements or an SQL UPDATE statement for each update when sending batched modifications back to the server.</span></span> <span data-ttu-id="5fa18-115">В первом случае две отдельные операции требуются для обновления записи.</span><span class="sxs-lookup"><span data-stu-id="5fa18-115">In the former case, two separate operations are required to update the record.</span></span> <span data-ttu-id="5fa18-116">В некоторых случаях особенно где удаленная система implements удаления, вставки и обновления триггеров, выбрав правильное значение свойства **UpdateOptions** можно значительно повысить производительность.</span><span class="sxs-lookup"><span data-stu-id="5fa18-116">In some cases, especially where the remote system implements DELETE, INSERT, and UPDATE triggers, choosing the correct **UpdateOptions** property setting can significantly impact performance.</span></span>

<span data-ttu-id="5fa18-117">Если не указать любой константы, будет использоваться **dbCriteriaUpdate** и **dbCriteriaKey** .</span><span class="sxs-lookup"><span data-stu-id="5fa18-117">If you don't specify any constants, **dbCriteriaUpdate** and **dbCriteriaKey** will be used.</span></span>

<span data-ttu-id="5fa18-118">Недавно добавленных записей всегда будет выдавать инструкции INSERT и удаленных записей всегда будет выдавать инструкций DELETE, поэтому это свойство применяется только к как библиотека курсора обновляет измененные записи.</span><span class="sxs-lookup"><span data-stu-id="5fa18-118">Newly added records will always generate INSERT statements and deleted records will always generate DELETE statements, so this property only applies to how the cursor library updates modified records.</span></span>

## <a name="example"></a><span data-ttu-id="5fa18-119">Пример</span><span class="sxs-lookup"><span data-stu-id="5fa18-119">Example</span></span>

<span data-ttu-id="5fa18-120">В этом примере использует **BatchSize** и **UpdateOptions** свойства для доступа к параметрам обновление любого пакета для указанного объекта **набора записей** .</span><span class="sxs-lookup"><span data-stu-id="5fa18-120">This example uses the **BatchSize** and **UpdateOptions** properties to control aspects of any batch updating for the specified **Recordset** object.</span></span>

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


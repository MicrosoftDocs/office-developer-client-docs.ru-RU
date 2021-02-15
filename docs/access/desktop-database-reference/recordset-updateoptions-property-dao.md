---
title: Свойство Recordset.UpdateOptions (DAO)
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
localization_priority: Normal
ms.openlocfilehash: ced8fc78729924ce271aa0fe38d77d287a131f13
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32307534"
---
# <a name="recordsetupdateoptions-property-dao"></a><span data-ttu-id="c8a43-102">Свойство Recordset.UpdateOptions (DAO)</span><span class="sxs-lookup"><span data-stu-id="c8a43-102">Recordset.UpdateOptions property (DAO)</span></span>


<span data-ttu-id="c8a43-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="c8a43-103">**Applies to**: Access 2013, Office 2013</span></span>

## <a name="syntax"></a><span data-ttu-id="c8a43-104">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c8a43-104">Syntax</span></span>

<span data-ttu-id="c8a43-105">*выражение .* UpdateOptions</span><span class="sxs-lookup"><span data-stu-id="c8a43-105">*expression* .UpdateOptions</span></span>

<span data-ttu-id="c8a43-106">*expression*: переменная, представляющая объект **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="c8a43-106">*expression* A variable that represents a **Recordset** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="c8a43-107">Примечания</span><span class="sxs-lookup"><span data-stu-id="c8a43-107">Remarks</span></span>

<span data-ttu-id="c8a43-108">При выполнении **[](recordset-update-method-dao.md)** обновления в пакетном режиме DAO и клиентская пакетная библиотека курсоров создают серию SQL update, чтобы внести необходимые изменения.</span><span class="sxs-lookup"><span data-stu-id="c8a43-108">When a batch-mode **[Update](recordset-update-method-dao.md)** is executed, DAO and the client batch cursor library create a series of SQL UPDATE statements to make the needed changes.</span></span> <span data-ttu-id="c8a43-109">Для каждого SQL создается предложение WHERE для каждого обновления, чтобы изолировать записи, помеченные как измененные **[свойством RecordStatus.](recordset-recordstatus-property-dao.md)**</span><span class="sxs-lookup"><span data-stu-id="c8a43-109">An SQL WHERE clause is created for each update to isolate the records that are marked as changed by the **[RecordStatus](recordset-recordstatus-property-dao.md)** property.</span></span> <span data-ttu-id="c8a43-110">Так как некоторые удаленные серверы используют триггеры или другие способы обеспечения целостности данных, часто важно ограничить поля, обновляемые только теми, на которые влияет изменение.</span><span class="sxs-lookup"><span data-stu-id="c8a43-110">Because some remote servers use triggers or other ways to enforce referential integrity, is it often important to limit the fields being updated to just those affected by the change.</span></span> 

<span data-ttu-id="c8a43-111">Для этого установите для свойства **UpdateOptions** одну из констант **dbCriteriaKey,** **dbCriteriaModValues,** **dbCriteriaAllCols** или **dbCriteriaTimeStamp.**</span><span class="sxs-lookup"><span data-stu-id="c8a43-111">To do this, set the **UpdateOptions** property to one of the constants **dbCriteriaKey**, **dbCriteriaModValues**, **dbCriteriaAllCols**, or **dbCriteriaTimeStamp**.</span></span> <span data-ttu-id="c8a43-112">Таким образом выполняется только абсолютный минимальный объем кода триггера.</span><span class="sxs-lookup"><span data-stu-id="c8a43-112">This way, only the absolute minimum amount of trigger code is executed.</span></span> <span data-ttu-id="c8a43-113">В результате операция обновления выполняется быстрее и с меньшем количеством потенциальных ошибок.</span><span class="sxs-lookup"><span data-stu-id="c8a43-113">As a result, the update operation is executed more quickly, and with fewer potential errors.</span></span>

<span data-ttu-id="c8a43-114">Вы также можете совмедить константы **dbCriteriaDeleteInsert** или **dbCriteriaUpdate,** чтобы определить, следует ли использовать набор SQL DELETE и INSERT или SQL UPDATE для каждого обновления при отправке пакетных изменений обратно на сервер.</span><span class="sxs-lookup"><span data-stu-id="c8a43-114">You can also concatenate either of the constants **dbCriteriaDeleteInsert** or **dbCriteriaUpdate** to determine whether to use a set of SQL DELETE and INSERT statements or an SQL UPDATE statement for each update when sending batched modifications back to the server.</span></span> <span data-ttu-id="c8a43-115">В этом случае для обновления записи требуются две отдельные операции.</span><span class="sxs-lookup"><span data-stu-id="c8a43-115">In the former case, two separate operations are required to update the record.</span></span> <span data-ttu-id="c8a43-116">В некоторых случаях, особенно если удаленная система реализует триггеры DELETE, INSERT и UPDATE, выбор правильного параметра **свойства UpdateOptions** может значительно повлиять на производительность.</span><span class="sxs-lookup"><span data-stu-id="c8a43-116">In some cases, especially where the remote system implements DELETE, INSERT, and UPDATE triggers, choosing the correct **UpdateOptions** property setting can significantly impact performance.</span></span>

<span data-ttu-id="c8a43-117">Если не указать константы, будут использованы **dbCriteriaUpdate** и **dbCriteriaKey.**</span><span class="sxs-lookup"><span data-stu-id="c8a43-117">If you don't specify any constants, **dbCriteriaUpdate** and **dbCriteriaKey** will be used.</span></span>

<span data-ttu-id="c8a43-118">Добавленные записи всегда будут создавать записи INSERT, а удаленные записи всегда будут создавать заявления DELETE, поэтому это свойство применяется только к обновлению измененных записей библиотекой курсора.</span><span class="sxs-lookup"><span data-stu-id="c8a43-118">Newly added records will always generate INSERT statements and deleted records will always generate DELETE statements, so this property only applies to how the cursor library updates modified records.</span></span>

## <a name="example"></a><span data-ttu-id="c8a43-119">Пример</span><span class="sxs-lookup"><span data-stu-id="c8a43-119">Example</span></span>

<span data-ttu-id="c8a43-120">В этом примере свойства **BatchSize** и **UpdateOptions** используются для управления аспектами пакетного обновления для указанного объекта **Recordset.**</span><span class="sxs-lookup"><span data-stu-id="c8a43-120">This example uses the **BatchSize** and **UpdateOptions** properties to control aspects of any batch updating for the specified **Recordset** object.</span></span>

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


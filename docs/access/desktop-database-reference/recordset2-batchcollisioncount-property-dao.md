---
title: Recordset2.BatchCollisionCount (DAO)
TOCTitle: BatchCollisionCount Property
ms:assetid: 997dfbb3-673c-8813-f51b-ab8d95093c4f
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197961(v=office.15)
ms:contentKeyID: 48546514
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 33650b9fdbaf7fbc9266c8c778199e1138cd5b21
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32307485"
---
# <a name="recordset2batchcollisioncount-property-dao"></a><span data-ttu-id="51463-102">Recordset2.BatchCollisionCount (DAO)</span><span class="sxs-lookup"><span data-stu-id="51463-102">Recordset2.BatchCollisionCount property (DAO)</span></span>


<span data-ttu-id="51463-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="51463-103">**Applies to**: Access 2013, Office 2013</span></span>

## <a name="syntax"></a><span data-ttu-id="51463-104">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="51463-104">Syntax</span></span>

<span data-ttu-id="51463-105">*выражения* . BatchCollisionCount</span><span class="sxs-lookup"><span data-stu-id="51463-105">*expression* .BatchCollisionCount</span></span>

<span data-ttu-id="51463-106">*выражение* Переменная, представляюная объект **Recordset2.**</span><span class="sxs-lookup"><span data-stu-id="51463-106">*expression* A variable that represents a **Recordset2** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="51463-107">Примечания</span><span class="sxs-lookup"><span data-stu-id="51463-107">Remarks</span></span>

<span data-ttu-id="51463-108">Это свойство указывает, сколько записей столкнулись с столкновениями или не удалось обновить во время последней попытки обновления пакета.</span><span class="sxs-lookup"><span data-stu-id="51463-108">This property indicates how many records encountered collisions or otherwise failed to update during the last batch update attempt.</span></span> <span data-ttu-id="51463-109">Значение этого свойства соответствует количеству закладок в свойстве **[BatchCollisions.](recordset2-batchcollisions-property-dao.md)**</span><span class="sxs-lookup"><span data-stu-id="51463-109">The value of this property corresponds to the number of bookmarks in the **[BatchCollisions](recordset2-batchcollisions-property-dao.md)** property.</span></span>

<span data-ttu-id="51463-110">Если свойство закладки рабочего объекта **[](recordset2-bookmark-property-dao.md)** **Recordset** задавалось значениям закладки в массиве **BatchCollisions,** можно перейти **[](recordset2-update-method-dao.md)** к каждой записи, не завершив последней операции обновления пакета.</span><span class="sxs-lookup"><span data-stu-id="51463-110">If you set the working **Recordset** object's **[Bookmark](recordset2-bookmark-property-dao.md)** property to bookmark values in the **BatchCollisions** array, you can move to each record that failed to complete the most recent batch **[Update](recordset2-update-method-dao.md)** operation.</span></span>

<span data-ttu-id="51463-111">После исправления записей столкновений метод обновления  пакетного режима может быть вызван повторно.</span><span class="sxs-lookup"><span data-stu-id="51463-111">After the collision records are corrected, a batch-mode **Update** method can be called again.</span></span> <span data-ttu-id="51463-112">На этом этапе DAO пытается еще одно пакетное обновление, и свойство **BatchCollisions** снова отражает набор записей, которые потерпели неудачу во второй попытке.</span><span class="sxs-lookup"><span data-stu-id="51463-112">At this point DAO attempts another batch update, and the **BatchCollisions** property again reflects the set of records that failed the second attempt.</span></span> <span data-ttu-id="51463-113">Все записи, которые удалось добиться в предыдущей попытке, не отправляются в текущей попытке, так как теперь они имеют свойство **[RecordStatus](recordset2-recordstatus-property-dao.md)** **dbRecordUnmodified.**</span><span class="sxs-lookup"><span data-stu-id="51463-113">Any records that succeeded in the previous attempt are not sent in the current attempt, because they now have a **[RecordStatus](recordset2-recordstatus-property-dao.md)** property of **dbRecordUnmodified**.</span></span> <span data-ttu-id="51463-114">Этот процесс может продолжаться до тех пор, пока возникают столкновения, или до тех пор, пока вы не откажете от обновлений и не закроет набор результатов.</span><span class="sxs-lookup"><span data-stu-id="51463-114">This process can continue as long as collisions occur, or until you abandon the updates and close the result set.</span></span>

## <a name="example"></a><span data-ttu-id="51463-115">Пример</span><span class="sxs-lookup"><span data-stu-id="51463-115">Example</span></span>

<span data-ttu-id="51463-116">В этом примере используются свойство **BatchCollisionCount** и метод **Update**, чтобы продемонстрировать пакетное обновление с разрешением всех конфликтов путем принудительного пакетного обновления.</span><span class="sxs-lookup"><span data-stu-id="51463-116">This example uses the **BatchCollisionCount** property and the **Update** method to demonstrate batch updating where any collisions are resolved by forcing the batch update.</span></span>

```vb 
Sub BatchX() 
 
 Dim wrkMain As Workspace 
 Dim conMain As Connection 
 Dim rstTemp As Recordset2 
 Dim intLoop As Integer 
 Dim strPrompt As String 
 
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
 ' batch updating. It is also required that a table 
 ' with a primary key is used. 
 Set rstTemp = conMain.OpenRecordset( _ 
 "SELECT * FROM roysched", dbOpenDynaset, 0, _ 
 dbOptimisticBatch) 
 
 With rstTemp 
 ' Modify data in local recordset. 
 Do While Not .EOF 
 .Edit 
 If !royalty <= 20 Then 
 !royalty = !royalty - 4 
 Else 
 !royalty = !royalty + 2 
 End If 
 .Update 
 .MoveNext 
 Loop 
 
 ' Attempt a batch update. 
 .Update dbUpdateBatch 
 
 ' If there are collisions, give the user the option 
 ' of forcing the changes or resolving them 
 ' individually. 
 If .BatchCollisionCount > 0 Then 
 strPrompt = "There are collisions. " & vbCr & _ 
 "Do you want the program to force " & _ 
 vbCr & "an update using the local data?" 
 If MsgBox(strPrompt, vbYesNo) = vbYes Then _ 
 .Update dbUpdateBatch, True 
 End If 
 
 .Close 
 End With 
 
 conMain.Close 
 wrkMain.Close 
 
End Sub 
 
```


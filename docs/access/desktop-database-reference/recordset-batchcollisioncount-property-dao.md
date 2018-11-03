---
title: Свойство Recordset.BatchCollisionCount (DAO)
TOCTitle: BatchCollisionCount Property
ms:assetid: 9d166463-8313-c0f5-8389-5d5ad933eb33
ms:mtpsurl: https://msdn.microsoft.com/library/Ff198240(v=office.15)
ms:contentKeyID: 48546617
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1101181
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 7d2100fb9803de406eca258b1d1093b343a6e88d
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/02/2018
ms.locfileid: "25929659"
---
# <a name="recordsetbatchcollisioncount-property-dao"></a><span data-ttu-id="7514c-102">Свойство Recordset.BatchCollisionCount (DAO)</span><span class="sxs-lookup"><span data-stu-id="7514c-102">Recordset.BatchCollisionCount property (DAO)</span></span>


<span data-ttu-id="7514c-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="7514c-103">**Applies to**: Access 2013, Office 2013</span></span>

## <a name="syntax"></a><span data-ttu-id="7514c-104">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="7514c-104">Syntax</span></span>

<span data-ttu-id="7514c-105">*выражение* . BatchCollisionCount</span><span class="sxs-lookup"><span data-stu-id="7514c-105">*expression* .BatchCollisionCount</span></span>

<span data-ttu-id="7514c-106">*выражение* Переменная, которая представляет собой объект **набора записей** .</span><span class="sxs-lookup"><span data-stu-id="7514c-106">*expression* A variable that represents a **Recordset** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="7514c-107">Примечания</span><span class="sxs-lookup"><span data-stu-id="7514c-107">Remarks</span></span>

<span data-ttu-id="7514c-108">Это свойство показывает количество записей обнаружил конфликтов или в противном случае — не удалось обновить во время последней попытки обновления пакета.</span><span class="sxs-lookup"><span data-stu-id="7514c-108">This property indicates how many records encountered collisions or otherwise failed to update during the last batch update attempt.</span></span> <span data-ttu-id="7514c-109">Значение этого свойства соответствует номеру закладки в свойстве **[BatchCollisions](recordset-batchcollisions-property-dao.md)** .</span><span class="sxs-lookup"><span data-stu-id="7514c-109">The value of this property corresponds to the number of bookmarks in the **[BatchCollisions](recordset-batchcollisions-property-dao.md)** property.</span></span>

<span data-ttu-id="7514c-110">Если значение рабочего объекта **[набора записей](recordset-object-dao.md)** свойства **[Bookmark](recordset-bookmark-property-dao.md)** значений закладку в массиве **BatchCollisions** , можно переместить в каждой записи, которая не удалось завершить пакета последнюю операцию **[обновления](recordset-update-method-dao.md)** .</span><span class="sxs-lookup"><span data-stu-id="7514c-110">If you set the working **[Recordset](recordset-object-dao.md)** object's **[Bookmark](recordset-bookmark-property-dao.md)** property to bookmark values in the **BatchCollisions** array, you can move to each record that failed to complete the most recent batch **[Update](recordset-update-method-dao.md)** operation.</span></span>

<span data-ttu-id="7514c-111">После исправления записей конфликта еще раз может быть вызван метод **Update** пакетном режиме.</span><span class="sxs-lookup"><span data-stu-id="7514c-111">After the collision records are corrected, a batch-mode **Update** method can be called again.</span></span> <span data-ttu-id="7514c-112">На этом этапе DAO пытается другого пакета обновления, и свойство **BatchCollisions** еще раз отражает набора записей, которые не удалось второй раз.</span><span class="sxs-lookup"><span data-stu-id="7514c-112">At this point DAO attempts another batch update, and the **BatchCollisions** property again reflects the set of records that failed the second attempt.</span></span> <span data-ttu-id="7514c-113">Записи, в которых завершена успешно Предыдущая попытка не отправляются в текущем попытки, так как теперь у них есть свойство **[RecordStatus](recordset-recordstatus-property-dao.md)** dbRecordUnmodified.</span><span class="sxs-lookup"><span data-stu-id="7514c-113">Any records that succeeded in the previous attempt are not sent in the current attempt, because they now have a **[RecordStatus](recordset-recordstatus-property-dao.md)** property of dbRecordUnmodified.</span></span> <span data-ttu-id="7514c-114">Этот процесс может продолжаться до тех пор, пока происходит конфликт или пока отказаться от обновления и закройте набора результатов.</span><span class="sxs-lookup"><span data-stu-id="7514c-114">This process can continue as long as collisions occur, or until you abandon the updates and close the result set.</span></span>

## <a name="example"></a><span data-ttu-id="7514c-115">Пример</span><span class="sxs-lookup"><span data-stu-id="7514c-115">Example</span></span>

<span data-ttu-id="7514c-116">В этом примере используется свойство **BatchCollisionCount** и метод **Update** для демонстрации пакетного обновления, где разрешены все конфликты с помощью принудительной пакетного обновления.</span><span class="sxs-lookup"><span data-stu-id="7514c-116">This example uses the **BatchCollisionCount** property and the **Update** method to demonstrate batch updating where any collisions are resolved by forcing the batch update.</span></span>

```vb 
Sub BatchX() 
 
 Dim wrkMain As Workspace 
 Dim conMain As Connection 
 Dim rstTemp As Recordset 
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


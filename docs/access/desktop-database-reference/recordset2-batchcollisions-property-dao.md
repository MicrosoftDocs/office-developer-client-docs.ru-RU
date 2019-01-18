---
title: Свойство Recordset2.BatchCollisions (DAO)
TOCTitle: BatchCollisions Property
ms:assetid: 07d6c25f-baf5-f7d6-d225-0447e0f78fe6
ms:mtpsurl: https://msdn.microsoft.com/library/Ff844993(v=office.15)
ms:contentKeyID: 48543085
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1101180
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: ea75da06c0db4eeb4e846bacfddc9f125c03fc84
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28699760"
---
# <a name="recordset2batchcollisions-property-dao"></a><span data-ttu-id="db93f-102">Свойство Recordset2.BatchCollisions (DAO)</span><span class="sxs-lookup"><span data-stu-id="db93f-102">Recordset2.BatchCollisions property (DAO)</span></span>


<span data-ttu-id="db93f-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="db93f-103">**Applies to**: Access 2013, Office 2013</span></span>

## <a name="syntax"></a><span data-ttu-id="db93f-104">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="db93f-104">Syntax</span></span>

<span data-ttu-id="db93f-105">*выражение* . BatchCollisions</span><span class="sxs-lookup"><span data-stu-id="db93f-105">*expression* .BatchCollisions</span></span>

<span data-ttu-id="db93f-106">*выражение* Переменная, которая представляет собой объект- **Recordset2** .</span><span class="sxs-lookup"><span data-stu-id="db93f-106">*expression* A variable that represents a **Recordset2** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="db93f-107">Замечания</span><span class="sxs-lookup"><span data-stu-id="db93f-107">Remarks</span></span>

<span data-ttu-id="db93f-108">Это свойство содержит массив закладки строк, которые столкнулись с конфликтом во время последнего вызова **[обновления](recordset2-update-method-dao.md)** попытка пакета.</span><span class="sxs-lookup"><span data-stu-id="db93f-108">This property contains an array of bookmarks to rows that encountered a collision during the last attempted batch **[Update](recordset2-update-method-dao.md)** call.</span></span> <span data-ttu-id="db93f-109">Свойство **[BatchCollisionCount](recordset2-batchcollisioncount-property-dao.md)** указывает число элементов в массиве.</span><span class="sxs-lookup"><span data-stu-id="db93f-109">The **[BatchCollisionCount](recordset2-batchcollisioncount-property-dao.md)** property indicates the number of elements in the array.</span></span>

<span data-ttu-id="db93f-110">Если значение рабочего объекта **набора записей** свойства **[Bookmark](recordset2-bookmark-property-dao.md)** значений закладку в массиве **BatchCollisions** , можно переместить в каждой записи, которая не удалось завершить последнюю операцию обновления пакетного режима.</span><span class="sxs-lookup"><span data-stu-id="db93f-110">If you set the working **Recordset** object's **[Bookmark](recordset2-bookmark-property-dao.md)** property to bookmark values in the **BatchCollisions** array, you can move to each record that failed to complete the most recent batch-mode Update operation.</span></span>

<span data-ttu-id="db93f-111">После исправления записей конфликта пакетном режиме метод **Update** можно позвонить еще раз.</span><span class="sxs-lookup"><span data-stu-id="db93f-111">After the collision records are corrected, you can call the batch mode **Update** method again.</span></span> <span data-ttu-id="db93f-112">На этом этапе DAO пытается другого пакета обновления, и свойство **BatchCollisions** еще раз отражает набора записей, которые не удалось второй раз.</span><span class="sxs-lookup"><span data-stu-id="db93f-112">At this point DAO attempts another batch update, and the **BatchCollisions** property again reflects the set of records that failed the second attempt.</span></span> <span data-ttu-id="db93f-113">Записи, в которых завершена успешно Предыдущая попытка не отправляются в текущем попытки как теперь у них есть свойство **[RecordStatus](recordset2-recordstatus-property-dao.md)** dbRecordUnmodified.</span><span class="sxs-lookup"><span data-stu-id="db93f-113">Any records that succeeded in the previous attempt are not sent in the current attempt, as they now have a **[RecordStatus](recordset2-recordstatus-property-dao.md)** property of dbRecordUnmodified.</span></span> <span data-ttu-id="db93f-114">Этот процесс может продолжаться до тех пор, пока происходит конфликт или пока отказаться от обновления и закройте набора результатов.</span><span class="sxs-lookup"><span data-stu-id="db93f-114">This process can continue as long as collisions occur, or until you abandon the updates and close the result set.</span></span>

<span data-ttu-id="db93f-115">Этот массив повторно создается при каждом выполнении метода **Update** пакетном режиме.</span><span class="sxs-lookup"><span data-stu-id="db93f-115">This array is re-created each time you execute a batch-mode **Update** method.</span></span>


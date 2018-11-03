---
title: Свойство Recordset.BatchCollisions (DAO)
TOCTitle: BatchCollisions Property
ms:assetid: 53e5572b-770c-9ea5-31a5-984abdf66faa
ms:mtpsurl: https://msdn.microsoft.com/library/Ff194079(v=office.15)
ms:contentKeyID: 48544881
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: c151868e349621d964f61058cfe82458764cf443
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/02/2018
ms.locfileid: "25929092"
---
# <a name="recordsetbatchcollisions-property-dao"></a><span data-ttu-id="f860f-102">Свойство Recordset.BatchCollisions (DAO)</span><span class="sxs-lookup"><span data-stu-id="f860f-102">Recordset.BatchCollisions property (DAO)</span></span>


<span data-ttu-id="f860f-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="f860f-103">**Applies to**: Access 2013, Office 2013</span></span>

## <a name="syntax"></a><span data-ttu-id="f860f-104">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f860f-104">Syntax</span></span>

<span data-ttu-id="f860f-105">*выражение* . BatchCollisions</span><span class="sxs-lookup"><span data-stu-id="f860f-105">*expression* .BatchCollisions</span></span>

<span data-ttu-id="f860f-106">*выражение* Переменная, которая представляет собой объект **набора записей** .</span><span class="sxs-lookup"><span data-stu-id="f860f-106">*expression* A variable that represents a **Recordset** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="f860f-107">Примечания</span><span class="sxs-lookup"><span data-stu-id="f860f-107">Remarks</span></span>

<span data-ttu-id="f860f-108">Это свойство содержит массив закладки строк, которые столкнулись с конфликтом во время последнего вызова **[обновления](recordset-update-method-dao.md)** попытка пакета.</span><span class="sxs-lookup"><span data-stu-id="f860f-108">This property contains an array of bookmarks to rows that encountered a collision during the last attempted batch **[Update](recordset-update-method-dao.md)** call.</span></span> <span data-ttu-id="f860f-109">Свойство **[BatchCollisionCount](recordset-batchcollisioncount-property-dao.md)** указывает число элементов в массиве.</span><span class="sxs-lookup"><span data-stu-id="f860f-109">The **[BatchCollisionCount](recordset-batchcollisioncount-property-dao.md)** property indicates the number of elements in the array.</span></span>

<span data-ttu-id="f860f-110">Если значение рабочего объекта **[набора записей](recordset-object-dao.md)** свойства **[Bookmark](recordset-bookmark-property-dao.md)** значений закладку в массиве **BatchCollisions** , можно переместить в каждой записи, которая не удалось завершить последнюю операцию обновления пакетного режима.</span><span class="sxs-lookup"><span data-stu-id="f860f-110">If you set the working **[Recordset](recordset-object-dao.md)** object's **[Bookmark](recordset-bookmark-property-dao.md)** property to bookmark values in the **BatchCollisions** array, you can move to each record that failed to complete the most recent batch-mode Update operation.</span></span>

<span data-ttu-id="f860f-111">После исправления записей конфликта пакетном режиме метод **Update** можно позвонить еще раз.</span><span class="sxs-lookup"><span data-stu-id="f860f-111">After the collision records are corrected, you can call the batch mode **Update** method again.</span></span> <span data-ttu-id="f860f-112">На этом этапе DAO пытается другого пакета обновления, и свойство **BatchCollisions** еще раз отражает набора записей, которые не удалось второй раз.</span><span class="sxs-lookup"><span data-stu-id="f860f-112">At this point DAO attempts another batch update, and the **BatchCollisions** property again reflects the set of records that failed the second attempt.</span></span> <span data-ttu-id="f860f-113">Записи, в которых завершена успешно Предыдущая попытка не отправляются в текущем попытки как теперь у них есть свойство **[RecordStatus](recordset-recordstatus-property-dao.md)** dbRecordUnmodified.</span><span class="sxs-lookup"><span data-stu-id="f860f-113">Any records that succeeded in the previous attempt are not sent in the current attempt, as they now have a **[RecordStatus](recordset-recordstatus-property-dao.md)** property of dbRecordUnmodified.</span></span> <span data-ttu-id="f860f-114">Этот процесс может продолжаться до тех пор, пока происходит конфликт или пока отказаться от обновления и закройте набора результатов.</span><span class="sxs-lookup"><span data-stu-id="f860f-114">This process can continue as long as collisions occur, or until you abandon the updates and close the result set.</span></span>

<span data-ttu-id="f860f-115">Этот массив повторно создается при каждом выполнении метода **Update** пакетном режиме.</span><span class="sxs-lookup"><span data-stu-id="f860f-115">This array is re-created each time you execute a batch-mode **Update** method.</span></span>


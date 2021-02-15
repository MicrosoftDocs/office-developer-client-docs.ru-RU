---
title: Свойство Recordset.BatchCollisions (DAO)
TOCTitle: BatchCollisions Property
ms:assetid: 53e5572b-770c-9ea5-31a5-984abdf66faa
ms:mtpsurl: https://msdn.microsoft.com/library/Ff194079(v=office.15)
ms:contentKeyID: 48544881
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 61f60567ac170a0ecde2d4bd46589d2308b7788f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32300863"
---
# <a name="recordsetbatchcollisions-property-dao"></a><span data-ttu-id="faceb-102">Свойство Recordset.BatchCollisions (DAO)</span><span class="sxs-lookup"><span data-stu-id="faceb-102">Recordset.BatchCollisions property (DAO)</span></span>


<span data-ttu-id="faceb-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="faceb-103">**Applies to**: Access 2013, Office 2013</span></span>

## <a name="syntax"></a><span data-ttu-id="faceb-104">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="faceb-104">Syntax</span></span>

<span data-ttu-id="faceb-105">*выражение .* BatchCollisions</span><span class="sxs-lookup"><span data-stu-id="faceb-105">*expression* .BatchCollisions</span></span>

<span data-ttu-id="faceb-106">*expression*: переменная, представляющая объект **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="faceb-106">*expression* A variable that represents a **Recordset** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="faceb-107">Примечания</span><span class="sxs-lookup"><span data-stu-id="faceb-107">Remarks</span></span>

<span data-ttu-id="faceb-108">Это свойство содержит массив закладок для строк, которые столкнулись с конфликтом во время последней попытки пакетного вызова **[Update.](recordset-update-method-dao.md)**</span><span class="sxs-lookup"><span data-stu-id="faceb-108">This property contains an array of bookmarks to rows that encountered a collision during the last attempted batch **[Update](recordset-update-method-dao.md)** call.</span></span> <span data-ttu-id="faceb-109">Свойство **[BatchCollisionCount](recordset-batchcollisioncount-property-dao.md)** указывает количество элементов в массиве.</span><span class="sxs-lookup"><span data-stu-id="faceb-109">The **[BatchCollisionCount](recordset-batchcollisioncount-property-dao.md)** property indicates the number of elements in the array.</span></span>

<span data-ttu-id="faceb-110">Если для свойства **[bookmark](recordset-bookmark-property-dao.md)** объекта **[Recordset](recordset-object-dao.md)** задаются значения закладок в массиве **BatchCollisions,** можно перейти к каждой записи, которая не прошла последние операции обновления в пакетном режиме.</span><span class="sxs-lookup"><span data-stu-id="faceb-110">If you set the working **[Recordset](recordset-object-dao.md)** object's **[Bookmark](recordset-bookmark-property-dao.md)** property to bookmark values in the **BatchCollisions** array, you can move to each record that failed to complete the most recent batch-mode Update operation.</span></span>

<span data-ttu-id="faceb-111">После исправления записей столкновений можно снова вызвать метод обновления в **пакетном** режиме.</span><span class="sxs-lookup"><span data-stu-id="faceb-111">After the collision records are corrected, you can call the batch mode **Update** method again.</span></span> <span data-ttu-id="faceb-112">На этом этапе DAO пытается повторить пакетное обновление, и свойство **BatchCollisions** снова отражает набор записей, которые не удалось вторую попытку.</span><span class="sxs-lookup"><span data-stu-id="faceb-112">At this point DAO attempts another batch update, and the **BatchCollisions** property again reflects the set of records that failed the second attempt.</span></span> <span data-ttu-id="faceb-113">Все записи, которые были успешными в предыдущей попытке, не отправляются в текущей попытке, так как теперь у них есть свойство **[RecordStatus](recordset-recordstatus-property-dao.md)** dbRecordUnmodified.</span><span class="sxs-lookup"><span data-stu-id="faceb-113">Any records that succeeded in the previous attempt are not sent in the current attempt, as they now have a **[RecordStatus](recordset-recordstatus-property-dao.md)** property of dbRecordUnmodified.</span></span> <span data-ttu-id="faceb-114">Этот процесс может продолжаться до тех пор, пока возникают конфликты, или до тех пор, пока вы не закроете набор результатов и откажутся от обновлений.</span><span class="sxs-lookup"><span data-stu-id="faceb-114">This process can continue as long as collisions occur, or until you abandon the updates and close the result set.</span></span>

<span data-ttu-id="faceb-115">Этот массив создается повторно при каждом выполнении метода обновления в пакетном **режиме.**</span><span class="sxs-lookup"><span data-stu-id="faceb-115">This array is re-created each time you execute a batch-mode **Update** method.</span></span>


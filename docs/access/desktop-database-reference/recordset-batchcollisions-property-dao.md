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
# <a name="recordsetbatchcollisions-property-dao"></a><span data-ttu-id="24701-102">Свойство Recordset.BatchCollisions (DAO)</span><span class="sxs-lookup"><span data-stu-id="24701-102">Recordset.BatchCollisions property (DAO)</span></span>


<span data-ttu-id="24701-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="24701-103">**Applies to**: Access 2013, Office 2013</span></span>

## <a name="syntax"></a><span data-ttu-id="24701-104">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="24701-104">Syntax</span></span>

<span data-ttu-id="24701-105">*Expression* . батчколлисионс</span><span class="sxs-lookup"><span data-stu-id="24701-105">*expression* .BatchCollisions</span></span>

<span data-ttu-id="24701-106">*expression*: переменная, представляющая объект **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="24701-106">*expression* A variable that represents a **Recordset** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="24701-107">Примечания</span><span class="sxs-lookup"><span data-stu-id="24701-107">Remarks</span></span>

<span data-ttu-id="24701-108">Это свойство содержит массив закладок на строки, которые вызвали конфликт во время последнего попытки вызова пакетного **[обновления](recordset-update-method-dao.md)** .</span><span class="sxs-lookup"><span data-stu-id="24701-108">This property contains an array of bookmarks to rows that encountered a collision during the last attempted batch **[Update](recordset-update-method-dao.md)** call.</span></span> <span data-ttu-id="24701-109">Свойство **[батчколлисионкаунт](recordset-batchcollisioncount-property-dao.md)** указывает количество элементов в массиве.</span><span class="sxs-lookup"><span data-stu-id="24701-109">The **[BatchCollisionCount](recordset-batchcollisioncount-property-dao.md)** property indicates the number of elements in the array.</span></span>

<span data-ttu-id="24701-110">Если присвоить свойству **[закладки](recordset-bookmark-property-dao.md)** рабочего объекта **[Recordset](recordset-object-dao.md)** значения закладки в массиве **батчколлисионс** , можно перейти к каждой записи, которая не смогла выполнить последнюю операцию обновления в пакетном режиме.</span><span class="sxs-lookup"><span data-stu-id="24701-110">If you set the working **[Recordset](recordset-object-dao.md)** object's **[Bookmark](recordset-bookmark-property-dao.md)** property to bookmark values in the **BatchCollisions** array, you can move to each record that failed to complete the most recent batch-mode Update operation.</span></span>

<span data-ttu-id="24701-111">После исправления записей о конфликтах можно снова вызвать метод обновления в режиме пакетного **обновления** .</span><span class="sxs-lookup"><span data-stu-id="24701-111">After the collision records are corrected, you can call the batch mode **Update** method again.</span></span> <span data-ttu-id="24701-112">На этом шаге DAO предпринимает попытку выполнить еще одно пакетное обновление, а свойство **батчколлисионс** еще раз отражает набор записей, которые не удалось выполнить вторую попытку.</span><span class="sxs-lookup"><span data-stu-id="24701-112">At this point DAO attempts another batch update, and the **BatchCollisions** property again reflects the set of records that failed the second attempt.</span></span> <span data-ttu-id="24701-113">Все записи, которые были успешно выполнены в предыдущей попытке, не отправляются в текущей попытке, так как теперь у них есть свойство **[Рекордстатус](recordset-recordstatus-property-dao.md)** дбрекордунмодифиед.</span><span class="sxs-lookup"><span data-stu-id="24701-113">Any records that succeeded in the previous attempt are not sent in the current attempt, as they now have a **[RecordStatus](recordset-recordstatus-property-dao.md)** property of dbRecordUnmodified.</span></span> <span data-ttu-id="24701-114">Этот процесс может продолжаться до тех пор, пока не будут выполнены конфликты, или пока не будут отменены все изменения и закрыть результирующий набор.</span><span class="sxs-lookup"><span data-stu-id="24701-114">This process can continue as long as collisions occur, or until you abandon the updates and close the result set.</span></span>

<span data-ttu-id="24701-115">Этот массив повторно создается каждый раз при выполнении метода **обновления** в пакетном режиме.</span><span class="sxs-lookup"><span data-stu-id="24701-115">This array is re-created each time you execute a batch-mode **Update** method.</span></span>


---
title: Свойство Recordset2. Батчколлисионс (DAO)
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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32307492"
---
# <a name="recordset2batchcollisions-property-dao"></a><span data-ttu-id="b2ebe-102">Свойство Recordset2. Батчколлисионс (DAO)</span><span class="sxs-lookup"><span data-stu-id="b2ebe-102">Recordset2.BatchCollisions property (DAO)</span></span>


<span data-ttu-id="b2ebe-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="b2ebe-103">**Applies to**: Access 2013, Office 2013</span></span>

## <a name="syntax"></a><span data-ttu-id="b2ebe-104">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b2ebe-104">Syntax</span></span>

<span data-ttu-id="b2ebe-105">*Expression* . батчколлисионс</span><span class="sxs-lookup"><span data-stu-id="b2ebe-105">*expression* .BatchCollisions</span></span>

<span data-ttu-id="b2ebe-106">*Expression (выражение* ) Переменная, представляющая объект **Recordset2** .</span><span class="sxs-lookup"><span data-stu-id="b2ebe-106">*expression* A variable that represents a **Recordset2** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="b2ebe-107">Примечания</span><span class="sxs-lookup"><span data-stu-id="b2ebe-107">Remarks</span></span>

<span data-ttu-id="b2ebe-108">Это свойство содержит массив закладок на строки, которые вызвали конфликт во время последнего попытки вызова пакетного **[обновления](recordset2-update-method-dao.md)** .</span><span class="sxs-lookup"><span data-stu-id="b2ebe-108">This property contains an array of bookmarks to rows that encountered a collision during the last attempted batch **[Update](recordset2-update-method-dao.md)** call.</span></span> <span data-ttu-id="b2ebe-109">Свойство **[батчколлисионкаунт](recordset2-batchcollisioncount-property-dao.md)** указывает количество элементов в массиве.</span><span class="sxs-lookup"><span data-stu-id="b2ebe-109">The **[BatchCollisionCount](recordset2-batchcollisioncount-property-dao.md)** property indicates the number of elements in the array.</span></span>

<span data-ttu-id="b2ebe-110">Если присвоить свойству **[закладки](recordset2-bookmark-property-dao.md)** рабочего объекта **Recordset** значения закладки в массиве **батчколлисионс** , можно перейти к каждой записи, которая не смогла выполнить последнюю операцию обновления в пакетном режиме.</span><span class="sxs-lookup"><span data-stu-id="b2ebe-110">If you set the working **Recordset** object's **[Bookmark](recordset2-bookmark-property-dao.md)** property to bookmark values in the **BatchCollisions** array, you can move to each record that failed to complete the most recent batch-mode Update operation.</span></span>

<span data-ttu-id="b2ebe-111">После исправления записей о конфликтах можно снова вызвать метод обновления в режиме пакетного **обновления** .</span><span class="sxs-lookup"><span data-stu-id="b2ebe-111">After the collision records are corrected, you can call the batch mode **Update** method again.</span></span> <span data-ttu-id="b2ebe-112">На этом шаге DAO предпринимает попытку выполнить еще одно пакетное обновление, а свойство **батчколлисионс** еще раз отражает набор записей, которые не удалось выполнить вторую попытку.</span><span class="sxs-lookup"><span data-stu-id="b2ebe-112">At this point DAO attempts another batch update, and the **BatchCollisions** property again reflects the set of records that failed the second attempt.</span></span> <span data-ttu-id="b2ebe-113">Все записи, которые были успешно выполнены в предыдущей попытке, не отправляются в текущей попытке, так как теперь у них есть свойство **[Рекордстатус](recordset2-recordstatus-property-dao.md)** дбрекордунмодифиед.</span><span class="sxs-lookup"><span data-stu-id="b2ebe-113">Any records that succeeded in the previous attempt are not sent in the current attempt, as they now have a **[RecordStatus](recordset2-recordstatus-property-dao.md)** property of dbRecordUnmodified.</span></span> <span data-ttu-id="b2ebe-114">Этот процесс может продолжаться до тех пор, пока не будут выполнены конфликты, или пока не будут отменены все изменения и закрыть результирующий набор.</span><span class="sxs-lookup"><span data-stu-id="b2ebe-114">This process can continue as long as collisions occur, or until you abandon the updates and close the result set.</span></span>

<span data-ttu-id="b2ebe-115">Этот массив повторно создается каждый раз при выполнении метода **обновления** в пакетном режиме.</span><span class="sxs-lookup"><span data-stu-id="b2ebe-115">This array is re-created each time you execute a batch-mode **Update** method.</span></span>


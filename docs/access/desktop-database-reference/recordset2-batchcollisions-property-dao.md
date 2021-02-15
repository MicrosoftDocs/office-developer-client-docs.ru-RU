---
title: Recordset2.BatchCollisions property (DAO)
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
# <a name="recordset2batchcollisions-property-dao"></a><span data-ttu-id="61649-102">Recordset2.BatchCollisions property (DAO)</span><span class="sxs-lookup"><span data-stu-id="61649-102">Recordset2.BatchCollisions property (DAO)</span></span>


<span data-ttu-id="61649-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="61649-103">**Applies to**: Access 2013, Office 2013</span></span>

## <a name="syntax"></a><span data-ttu-id="61649-104">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="61649-104">Syntax</span></span>

<span data-ttu-id="61649-105">*выражение .* BatchCollisions</span><span class="sxs-lookup"><span data-stu-id="61649-105">*expression* .BatchCollisions</span></span>

<span data-ttu-id="61649-106">*выражение* Переменная, представляюная объект **Recordset2.**</span><span class="sxs-lookup"><span data-stu-id="61649-106">*expression* A variable that represents a **Recordset2** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="61649-107">Заметки</span><span class="sxs-lookup"><span data-stu-id="61649-107">Remarks</span></span>

<span data-ttu-id="61649-108">Это свойство содержит массив закладок для строк, которые столкнулись с конфликтом во время последней попытки пакетного вызова **[Update.](recordset2-update-method-dao.md)**</span><span class="sxs-lookup"><span data-stu-id="61649-108">This property contains an array of bookmarks to rows that encountered a collision during the last attempted batch **[Update](recordset2-update-method-dao.md)** call.</span></span> <span data-ttu-id="61649-109">Свойство **[BatchCollisionCount](recordset2-batchcollisioncount-property-dao.md)** указывает количество элементов в массиве.</span><span class="sxs-lookup"><span data-stu-id="61649-109">The **[BatchCollisionCount](recordset2-batchcollisioncount-property-dao.md)** property indicates the number of elements in the array.</span></span>

<span data-ttu-id="61649-110">Если для свойства **[bookmark](recordset2-bookmark-property-dao.md)** объекта **Recordset** задаются значения закладок в массиве **BatchCollisions,** можно перейти к каждой записи, которая не прошла последние операции обновления в пакетном режиме.</span><span class="sxs-lookup"><span data-stu-id="61649-110">If you set the working **Recordset** object's **[Bookmark](recordset2-bookmark-property-dao.md)** property to bookmark values in the **BatchCollisions** array, you can move to each record that failed to complete the most recent batch-mode Update operation.</span></span>

<span data-ttu-id="61649-111">После исправления записей столкновений можно снова вызвать метод обновления в **пакетном** режиме.</span><span class="sxs-lookup"><span data-stu-id="61649-111">After the collision records are corrected, you can call the batch mode **Update** method again.</span></span> <span data-ttu-id="61649-112">На этом этапе DAO пытается повторить пакетное обновление, и свойство **BatchCollisions** снова отражает набор записей, которые не удалось вторую попытку.</span><span class="sxs-lookup"><span data-stu-id="61649-112">At this point DAO attempts another batch update, and the **BatchCollisions** property again reflects the set of records that failed the second attempt.</span></span> <span data-ttu-id="61649-113">Все записи, которые были успешными в предыдущей попытке, не отправляются в текущей попытке, так как теперь у них есть свойство **[RecordStatus](recordset2-recordstatus-property-dao.md)** dbRecordUnmodified.</span><span class="sxs-lookup"><span data-stu-id="61649-113">Any records that succeeded in the previous attempt are not sent in the current attempt, as they now have a **[RecordStatus](recordset2-recordstatus-property-dao.md)** property of dbRecordUnmodified.</span></span> <span data-ttu-id="61649-114">Этот процесс может продолжаться до тех пор, пока возникают конфликты, или до тех пор, пока вы не закроете набор результатов и откажутся от обновлений.</span><span class="sxs-lookup"><span data-stu-id="61649-114">This process can continue as long as collisions occur, or until you abandon the updates and close the result set.</span></span>

<span data-ttu-id="61649-115">Этот массив создается повторно при каждом выполнении метода обновления в пакетном **режиме.**</span><span class="sxs-lookup"><span data-stu-id="61649-115">This array is re-created each time you execute a batch-mode **Update** method.</span></span>


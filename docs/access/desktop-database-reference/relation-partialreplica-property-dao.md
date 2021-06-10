---
title: Свойство Relation.PartialReplica (DAO)
TOCTitle: PartialReplica Property
ms:assetid: 3cb15639-371e-06e3-e2ba-30466ce09a72
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192692(v=office.15)
ms:contentKeyID: 48544324
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1053557
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: fef48902b806f13947ae4b81728af4c5704c2b8e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32307016"
---
# <a name="relationpartialreplica-property-dao"></a><span data-ttu-id="c7bc1-102">Свойство Relation.PartialReplica (DAO)</span><span class="sxs-lookup"><span data-stu-id="c7bc1-102">Relation.PartialReplica property (DAO)</span></span>

<span data-ttu-id="c7bc1-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="c7bc1-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="c7bc1-104">Задает или возвращает значение объекта **Relation,** указывающее, следует ли учитывать это отношение при заполнении частичной реплики из полной реплики.</span><span class="sxs-lookup"><span data-stu-id="c7bc1-104">Sets or returns a value on a **Relation** object indicating whether that relation should be considered when populating a partial replica from a full replica.</span></span> <span data-ttu-id="c7bc1-105">(Только базы данных баз данных Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="c7bc1-105">(Microsoft Access database engine databases only).</span></span> <span data-ttu-id="c7bc1-106">Для чтения и записи, **Boolean**.</span><span class="sxs-lookup"><span data-stu-id="c7bc1-106">Read/write **Boolean**.</span></span>

## <a name="syntax"></a><span data-ttu-id="c7bc1-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c7bc1-107">Syntax</span></span>

<span data-ttu-id="c7bc1-108">*выражения* . PartialReplica</span><span class="sxs-lookup"><span data-stu-id="c7bc1-108">*expression* .PartialReplica</span></span>

<span data-ttu-id="c7bc1-109">*выражение* Выражение, возвращаемая **объекту Relation.**</span><span class="sxs-lookup"><span data-stu-id="c7bc1-109">*expression* An expression that returns a **Relation** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="c7bc1-110">Примечания</span><span class="sxs-lookup"><span data-stu-id="c7bc1-110">Remarks</span></span>

<span data-ttu-id="c7bc1-111">Значение параметра или возврата — это тип данных Boolean, который является **true,** если при синхронизации необходимо применять отношение.</span><span class="sxs-lookup"><span data-stu-id="c7bc1-111">The setting or return value is a Boolean data type that is **True** when the relation should be enforced during synchronization.</span></span>

<span data-ttu-id="c7bc1-112">Это свойство позволяет реплицировать данные из полной реплики в частичную реплику на основе взаимосвязей между таблицами.</span><span class="sxs-lookup"><span data-stu-id="c7bc1-112">This property enables you to replicate data from the full replica to the partial replica based on relationships between tables.</span></span> <span data-ttu-id="c7bc1-113">Свойство **PartialReplica** можно использовать при настройке свойства **ReplicaFilter** только при недостаточном указании, какие данные следует реплицировать в частичную.</span><span class="sxs-lookup"><span data-stu-id="c7bc1-113">You can use the **PartialReplica** property when setting the **ReplicaFilter** property alone can't adequately specify what data should be replicated to the partial.</span></span> <span data-ttu-id="c7bc1-114">Например, предположим, что у вас есть база данных, в которой таблица Клиентов имеет отношение один к многим со таблицей Заказы, и необходимо настроить частичную реплику, которая реплицирует заказы только от клиентов в регионе Калифорния (вместо всех заказов).</span><span class="sxs-lookup"><span data-stu-id="c7bc1-114">For example, suppose you have a database in which the Customers table has a one-to-many relationship with the Orders table, and you want to configure a partial replica that only replicates orders from customers in the California region (instead of all orders).</span></span> <span data-ttu-id="c7bc1-115">Невозможно задать свойство **ReplicaFilter** в таблице Заказы к Региону = "CA", так как поле Region находится в таблице Клиенты, а не в таблице Заказы.</span><span class="sxs-lookup"><span data-stu-id="c7bc1-115">It is not possible to set the **ReplicaFilter** property on the Orders table to Region = 'CA' because the Region field is in the Customers table, not the Orders table.</span></span>

<span data-ttu-id="c7bc1-116">Чтобы реплицировать все заказы из региона Калифорния, необходимо указать, что связь между таблицами "Заказы" и "Клиенты" будет активна во время репликации.</span><span class="sxs-lookup"><span data-stu-id="c7bc1-116">To replicate all orders from the California region, you must indicate that the relation between the Orders and Customers tables will be active during replication.</span></span> <span data-ttu-id="c7bc1-117">После создания частичной реплики следующие действия заполнят ее всеми заказами из региона Калифорния:</span><span class="sxs-lookup"><span data-stu-id="c7bc1-117">Once you've created a partial replica, the following steps will populate it with all orders from the California region:</span></span>

1.  <span data-ttu-id="c7bc1-118">Установите свойство **ReplicaFilter** в объекте **Customers TableDef** на "Region = "CA".</span><span class="sxs-lookup"><span data-stu-id="c7bc1-118">Set the **ReplicaFilter** property on the Customers **TableDef** object to "Region = 'CA'".</span></span>

2.  <span data-ttu-id="c7bc1-119">Установите значение свойства **PartialReplica** **true** на **объекте Relation,** соответствующем отношениям между заказами и клиентами.</span><span class="sxs-lookup"><span data-stu-id="c7bc1-119">Set the value of the **PartialReplica** property to **True** on the **Relation** object corresponding to the relationship between Orders and Customers.</span></span>

3.  <span data-ttu-id="c7bc1-120">Вызов метода **PopulatePartial.**</span><span class="sxs-lookup"><span data-stu-id="c7bc1-120">Invoke the **PopulatePartial** method.</span></span>
    

> [!NOTE]
> <span data-ttu-id="c7bc1-121">При наборе отношения реплики или фильтра реплики следует помнить, что записи частичной реплики, не удовлетворяющие критериям ограничения, будут удалены из частичной реплики, но не из полной реплики.</span><span class="sxs-lookup"><span data-stu-id="c7bc1-121">When you set a replica filter or replica relation, be aware that records in the partial replica that don't satisfy the restriction criteria will be removed from the partial replica, but not from the full replica.</span></span> <span data-ttu-id="c7bc1-122">Например, предположим, что вы установите свойство **ReplicaFilter** в таблице Customers **TableDef** в частичной реплике на "Region = "CA", а затем перенаселенность базы данных.</span><span class="sxs-lookup"><span data-stu-id="c7bc1-122">For example, suppose you set the **ReplicaFilter** property on the Customers **TableDef** in the partial replica to "Region = 'CA'" and you then repopulate the database.</span></span> <span data-ttu-id="c7bc1-123">Это позволит вставить или обновить все записи для клиентов из Калифорнии.</span><span class="sxs-lookup"><span data-stu-id="c7bc1-123">This will insert or update all records for California-based customers.</span></span> 
> 
> <span data-ttu-id="c7bc1-124">Если затем сбросить свойство **ReplicaFilter** в "Region = "FL" и перенаселить базу данных, все записи региона Калифорнии в частичной реплике будут удалены, а все записи клиентов из Флориды будут вставлены из полной реплики.</span><span class="sxs-lookup"><span data-stu-id="c7bc1-124">If you then reset the **ReplicaFilter** property to "Region = 'FL'" and repopulate the database, all California region records in the partial replica will be removed, and all records from Florida-based customers will be inserted from the full replica.</span></span> <span data-ttu-id="c7bc1-125">Записи в полной реплике не будут удалены.</span><span class="sxs-lookup"><span data-stu-id="c7bc1-125">No records in the full replica will be deleted.</span></span> 
>
> <span data-ttu-id="c7bc1-126">Перед установкой свойства **ReplicaFilter** или **PartialReplica** лучше синхронизировать частичную реплику, в которой вы устанавливаете эти свойства, с полной репликой.</span><span class="sxs-lookup"><span data-stu-id="c7bc1-126">Before setting either the **ReplicaFilter** or **PartialReplica** property, it's a good idea to synchronize the partial replica in which you are setting these properties with the full replica.</span></span> <span data-ttu-id="c7bc1-127">Это гарантирует, что ожидающих изменений частичной реплики будут объединены в полную реплику до удаления каких-либо записей в частичной реплике.</span><span class="sxs-lookup"><span data-stu-id="c7bc1-127">This will ensure that pending changes in the partial replica will be merged into the full replica before any records are removed in the partial replica.</span></span>



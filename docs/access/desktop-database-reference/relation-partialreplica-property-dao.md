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
# <a name="relationpartialreplica-property-dao"></a><span data-ttu-id="1615a-102">Свойство Relation.PartialReplica (DAO)</span><span class="sxs-lookup"><span data-stu-id="1615a-102">Relation.PartialReplica property (DAO)</span></span>

<span data-ttu-id="1615a-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="1615a-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="1615a-104">Задает или возвращает значение объекта **Relation,** указывающее, следует ли учитывать это отношение при заполнении частичной реплики из полной реплики.</span><span class="sxs-lookup"><span data-stu-id="1615a-104">Sets or returns a value on a **Relation** object indicating whether that relation should be considered when populating a partial replica from a full replica.</span></span> <span data-ttu-id="1615a-105">(Только для баз данных яд баз данных Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="1615a-105">(Microsoft Access database engine databases only).</span></span> <span data-ttu-id="1615a-106">Для чтения и записи, **Boolean**.</span><span class="sxs-lookup"><span data-stu-id="1615a-106">Read/write **Boolean**.</span></span>

## <a name="syntax"></a><span data-ttu-id="1615a-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="1615a-107">Syntax</span></span>

<span data-ttu-id="1615a-108">*выражение .* PartialReplica</span><span class="sxs-lookup"><span data-stu-id="1615a-108">*expression* .PartialReplica</span></span>

<span data-ttu-id="1615a-109">*выражение* Выражение, которое возвращает объект **Relation.**</span><span class="sxs-lookup"><span data-stu-id="1615a-109">*expression* An expression that returns a **Relation** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="1615a-110">Заметки</span><span class="sxs-lookup"><span data-stu-id="1615a-110">Remarks</span></span>

<span data-ttu-id="1615a-111">Значение параметра или возвращаемого значения — это boolean data type, значение **True,** если отношение должно быть принудительно применено во время синхронизации.</span><span class="sxs-lookup"><span data-stu-id="1615a-111">The setting or return value is a Boolean data type that is **True** when the relation should be enforced during synchronization.</span></span>

<span data-ttu-id="1615a-112">Это свойство позволяет реплицировать данные из полной реплики в частичную реплику на основе связей между таблицами.</span><span class="sxs-lookup"><span data-stu-id="1615a-112">This property enables you to replicate data from the full replica to the partial replica based on relationships between tables.</span></span> <span data-ttu-id="1615a-113">Свойство **PartialReplica** можно использовать, если установка только свойства **ReplicaFilter** не может адекватно указать, какие данные следует реплицировать на часть.</span><span class="sxs-lookup"><span data-stu-id="1615a-113">You can use the **PartialReplica** property when setting the **ReplicaFilter** property alone can't adequately specify what data should be replicated to the partial.</span></span> <span data-ttu-id="1615a-114">Например, предположим, что у вас есть база данных, в которой таблица Customers имеет отношение "один к многим" с таблицей "Заказы", и вы хотите настроить частичную реплику, которая реплицирует заказы только от клиентов в Калифорнии (вместо всех заказов).</span><span class="sxs-lookup"><span data-stu-id="1615a-114">For example, suppose you have a database in which the Customers table has a one-to-many relationship with the Orders table, and you want to configure a partial replica that only replicates orders from customers in the California region (instead of all orders).</span></span> <span data-ttu-id="1615a-115">Невозможно установить для свойства **ReplicaFilter** в таблице Orders (Заказы) задав для свойства Region = 'CA' (ЦС), так как поле Region находится в таблице Customers, а не в таблице Orders (Заказы).</span><span class="sxs-lookup"><span data-stu-id="1615a-115">It is not possible to set the **ReplicaFilter** property on the Orders table to Region = 'CA' because the Region field is in the Customers table, not the Orders table.</span></span>

<span data-ttu-id="1615a-116">Чтобы реплицировать все заказы из региона Калифорнии, необходимо указать, что отношение между таблицами "Заказы" и "Клиенты" будет активно во время репликации.</span><span class="sxs-lookup"><span data-stu-id="1615a-116">To replicate all orders from the California region, you must indicate that the relation between the Orders and Customers tables will be active during replication.</span></span> <span data-ttu-id="1615a-117">После создания частичной реплики в ней будут заполнены все заказы из области Калифорнии:</span><span class="sxs-lookup"><span data-stu-id="1615a-117">Once you've created a partial replica, the following steps will populate it with all orders from the California region:</span></span>

1.  <span data-ttu-id="1615a-118">Установите для **свойства ReplicaFilter** объекта Customers **TableDef** свойство "Region = 'CA'".</span><span class="sxs-lookup"><span data-stu-id="1615a-118">Set the **ReplicaFilter** property on the Customers **TableDef** object to "Region = 'CA'".</span></span>

2.  <span data-ttu-id="1615a-119">Установите для свойства **PartialReplica** значение **True** в **объекте Relation,** соответствующем отношениям между Заказы и Клиенты.</span><span class="sxs-lookup"><span data-stu-id="1615a-119">Set the value of the **PartialReplica** property to **True** on the **Relation** object corresponding to the relationship between Orders and Customers.</span></span>

3.  <span data-ttu-id="1615a-120">Вызов метода **PopulatePartial.**</span><span class="sxs-lookup"><span data-stu-id="1615a-120">Invoke the **PopulatePartial** method.</span></span>
    

> [!NOTE]
> <span data-ttu-id="1615a-121">При этом следует помнить, что записи в частичной реплике, не удовлетворяющие условиям ограничения, будут удалены из частичной реплики, но не из полной реплики.</span><span class="sxs-lookup"><span data-stu-id="1615a-121">When you set a replica filter or replica relation, be aware that records in the partial replica that don't satisfy the restriction criteria will be removed from the partial replica, but not from the full replica.</span></span> <span data-ttu-id="1615a-122">Например, предположим, что для свойства **ReplicaFilter** в Customers **TableDef** в частичной реплике задалось "Region = 'CA'" и затем повторное переполнение базы данных.</span><span class="sxs-lookup"><span data-stu-id="1615a-122">For example, suppose you set the **ReplicaFilter** property on the Customers **TableDef** in the partial replica to "Region = 'CA'" and you then repopulate the database.</span></span> <span data-ttu-id="1615a-123">При этом будут вставлены или обновлены все записи для клиентов из Калифорнии.</span><span class="sxs-lookup"><span data-stu-id="1615a-123">This will insert or update all records for California-based customers.</span></span> 
> 
> <span data-ttu-id="1615a-124">Если затем сбросить свойство **ReplicaFilter** в "Region = 'FL'" и повторно заселить базу данных, все записи региона Калифорнии в частичной реплике будут удалены, а все записи клиентов на основе флажков будут вставлены из полной реплики.</span><span class="sxs-lookup"><span data-stu-id="1615a-124">If you then reset the **ReplicaFilter** property to "Region = 'FL'" and repopulate the database, all California region records in the partial replica will be removed, and all records from Florida-based customers will be inserted from the full replica.</span></span> <span data-ttu-id="1615a-125">Записи в полной реплике не удаляются.</span><span class="sxs-lookup"><span data-stu-id="1615a-125">No records in the full replica will be deleted.</span></span> 
>
> <span data-ttu-id="1615a-126">Перед настройкой свойства **ReplicaFilter** или **PartialReplica** лучше синхронизировать частичную реплику, в которой эти свойства задаются, с полной репликой.</span><span class="sxs-lookup"><span data-stu-id="1615a-126">Before setting either the **ReplicaFilter** or **PartialReplica** property, it's a good idea to synchronize the partial replica in which you are setting these properties with the full replica.</span></span> <span data-ttu-id="1615a-127">Это обеспечит слияние ожидающих изменений в частичной реплике в полную реплику перед удалением каких-либо записей в частичной реплике.</span><span class="sxs-lookup"><span data-stu-id="1615a-127">This will ensure that pending changes in the partial replica will be merged into the full replica before any records are removed in the partial replica.</span></span>



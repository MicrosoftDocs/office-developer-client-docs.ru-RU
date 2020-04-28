---
title: Свойство relation. Партиалреплика (DAO)
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
# <a name="relationpartialreplica-property-dao"></a><span data-ttu-id="d3338-102">Свойство relation. Партиалреплика (DAO)</span><span class="sxs-lookup"><span data-stu-id="d3338-102">Relation.PartialReplica property (DAO)</span></span>

<span data-ttu-id="d3338-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="d3338-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="d3338-104">Задает или возвращает значение объекта **relation** , указывающее, следует ли учитывать это отношение при заполнении частичной реплики из полной реплики.</span><span class="sxs-lookup"><span data-stu-id="d3338-104">Sets or returns a value on a **Relation** object indicating whether that relation should be considered when populating a partial replica from a full replica.</span></span> <span data-ttu-id="d3338-105">(Только базы данных ядра СУБД Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="d3338-105">(Microsoft Access database engine databases only).</span></span> <span data-ttu-id="d3338-106">Для чтения и записи, **Boolean**.</span><span class="sxs-lookup"><span data-stu-id="d3338-106">Read/write **Boolean**.</span></span>

## <a name="syntax"></a><span data-ttu-id="d3338-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d3338-107">Syntax</span></span>

<span data-ttu-id="d3338-108">*Expression* . партиалреплика</span><span class="sxs-lookup"><span data-stu-id="d3338-108">*expression* .PartialReplica</span></span>

<span data-ttu-id="d3338-109">*Expression (выражение* ) Выражение, возвращающее объект **relation** .</span><span class="sxs-lookup"><span data-stu-id="d3338-109">*expression* An expression that returns a **Relation** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="d3338-110">Примечания</span><span class="sxs-lookup"><span data-stu-id="d3338-110">Remarks</span></span>

<span data-ttu-id="d3338-111">Параметр или возвращаемое значение — это тип данных Boolean, который имеет **значение true** , если отношение должно применяться во время синхронизации.</span><span class="sxs-lookup"><span data-stu-id="d3338-111">The setting or return value is a Boolean data type that is **True** when the relation should be enforced during synchronization.</span></span>

<span data-ttu-id="d3338-112">Это свойство позволяет реплицировать данные из полной реплики в частичную реплику на основе связей между таблицами.</span><span class="sxs-lookup"><span data-stu-id="d3338-112">This property enables you to replicate data from the full replica to the partial replica based on relationships between tables.</span></span> <span data-ttu-id="d3338-113">Свойство **партиалреплика** можно использовать, если установка свойства **репликафилтер** не может адекватно указывать, какие данные следует реплицировать в частичный.</span><span class="sxs-lookup"><span data-stu-id="d3338-113">You can use the **PartialReplica** property when setting the **ReplicaFilter** property alone can't adequately specify what data should be replicated to the partial.</span></span> <span data-ttu-id="d3338-114">Например, предположим, что у вас есть база данных, в которой таблица Customers имеет связь "один ко многим" с таблицей "заказы", и вы хотите настроить частичную реплику, которая реплицирует заказы только от клиентов в регионе Калифорния (а не во всех заказах).</span><span class="sxs-lookup"><span data-stu-id="d3338-114">For example, suppose you have a database in which the Customers table has a one-to-many relationship with the Orders table, and you want to configure a partial replica that only replicates orders from customers in the California region (instead of all orders).</span></span> <span data-ttu-id="d3338-115">Невозможно задать для свойства **репликафилтер** таблицы Orders значение Region = ' Ca ', так как поле область находится в таблице клиентов, а не в таблице Orders.</span><span class="sxs-lookup"><span data-stu-id="d3338-115">It is not possible to set the **ReplicaFilter** property on the Orders table to Region = 'CA' because the Region field is in the Customers table, not the Orders table.</span></span>

<span data-ttu-id="d3338-116">Для репликации всех заказов из региона Калифорния необходимо указать, что связь между таблицами Orders и Customers будет активна во время репликации.</span><span class="sxs-lookup"><span data-stu-id="d3338-116">To replicate all orders from the California region, you must indicate that the relation between the Orders and Customers tables will be active during replication.</span></span> <span data-ttu-id="d3338-117">После создания частичной реплики приведенные ниже действия будут заполняться всеми заказами из региона Калифорния:</span><span class="sxs-lookup"><span data-stu-id="d3338-117">Once you've created a partial replica, the following steps will populate it with all orders from the California region:</span></span>

1.  <span data-ttu-id="d3338-118">Задайте для свойства **репликафилтер** объекта Customers **tabledef** значение "Region = ' Ca '".</span><span class="sxs-lookup"><span data-stu-id="d3338-118">Set the **ReplicaFilter** property on the Customers **TableDef** object to "Region = 'CA'".</span></span>

2.  <span data-ttu-id="d3338-119">Присвойте свойству **партиалреплика** значение **true** для объекта **relation** , соответствующего связи между Orders и Customers.</span><span class="sxs-lookup"><span data-stu-id="d3338-119">Set the value of the **PartialReplica** property to **True** on the **Relation** object corresponding to the relationship between Orders and Customers.</span></span>

3.  <span data-ttu-id="d3338-120">Вызовите метод **популатепартиал** .</span><span class="sxs-lookup"><span data-stu-id="d3338-120">Invoke the **PopulatePartial** method.</span></span>
    

> [!NOTE]
> <span data-ttu-id="d3338-121">При задании фильтра реплики или связи реплики следует учитывать, что записи в частичной реплике, которые не удовлетворяют условиям ограничения, будут удалены из частичной реплики, но не из полной реплики.</span><span class="sxs-lookup"><span data-stu-id="d3338-121">When you set a replica filter or replica relation, be aware that records in the partial replica that don't satisfy the restriction criteria will be removed from the partial replica, but not from the full replica.</span></span> <span data-ttu-id="d3338-122">Например, предположим, что вы установили свойство **репликафилтер** для клиентов **tabledef** в частичной реплике на "Region = ' Ca '", а затем повторно заполните базу данных.</span><span class="sxs-lookup"><span data-stu-id="d3338-122">For example, suppose you set the **ReplicaFilter** property on the Customers **TableDef** in the partial replica to "Region = 'CA'" and you then repopulate the database.</span></span> <span data-ttu-id="d3338-123">При этом будут вставлены или обновлены все записи для клиентов с учетом Калифорнии.</span><span class="sxs-lookup"><span data-stu-id="d3338-123">This will insert or update all records for California-based customers.</span></span> 
> 
> <span data-ttu-id="d3338-124">Если затем сбросить свойство **репликафилтер** в значение "Region = ' FL '" и повторно заполнить базу данных, все записи областей штата Калифорния в частичной реплике будут удалены, а все записи из клиентов на основе Флорида будут вставлены из полной реплики.</span><span class="sxs-lookup"><span data-stu-id="d3338-124">If you then reset the **ReplicaFilter** property to "Region = 'FL'" and repopulate the database, all California region records in the partial replica will be removed, and all records from Florida-based customers will be inserted from the full replica.</span></span> <span data-ttu-id="d3338-125">Никакие записи в полной реплике не будут удалены.</span><span class="sxs-lookup"><span data-stu-id="d3338-125">No records in the full replica will be deleted.</span></span> 
>
> <span data-ttu-id="d3338-126">Перед настройкой свойства **репликафилтер** или **партиалреплика** рекомендуется синхронизировать частичную реплику, в которой вы настраиваете эти свойства с помощью полной реплики.</span><span class="sxs-lookup"><span data-stu-id="d3338-126">Before setting either the **ReplicaFilter** or **PartialReplica** property, it's a good idea to synchronize the partial replica in which you are setting these properties with the full replica.</span></span> <span data-ttu-id="d3338-127">Это гарантирует, что ожидающие изменения частичной реплики будут объединены в полную реплику перед удалением записей в частичной реплике.</span><span class="sxs-lookup"><span data-stu-id="d3338-127">This will ensure that pending changes in the partial replica will be merged into the full replica before any records are removed in the partial replica.</span></span>



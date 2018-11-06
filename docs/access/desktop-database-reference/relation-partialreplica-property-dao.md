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
ms.openlocfilehash: 11f8017c01cec9af2da26bedaf689d69554e554c
ms.sourcegitcommit: 1dd744993ecb4bed241ace874ad26edaef1778b8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/06/2018
ms.locfileid: "25998194"
---
# <a name="relationpartialreplica-property-dao"></a><span data-ttu-id="72d1c-102">Свойство Relation.PartialReplica (DAO)</span><span class="sxs-lookup"><span data-stu-id="72d1c-102">Relation.PartialReplica property (DAO)</span></span>

<span data-ttu-id="72d1c-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="72d1c-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="72d1c-104">Задает или возвращает значение, указывающее, следует ли этого отношения учитывать при заполнении реплику из полной реплики объекта **связи** .</span><span class="sxs-lookup"><span data-stu-id="72d1c-104">Sets or returns a value on a **Relation** object indicating whether that relation should be considered when populating a partial replica from a full replica.</span></span> <span data-ttu-id="72d1c-105">(База данных ядра базы данных Microsoft Access только).</span><span class="sxs-lookup"><span data-stu-id="72d1c-105">(Microsoft Access database engine databases only).</span></span> <span data-ttu-id="72d1c-106">Для чтения и записи, **Boolean**.</span><span class="sxs-lookup"><span data-stu-id="72d1c-106">Read/write **Boolean**.</span></span>

## <a name="syntax"></a><span data-ttu-id="72d1c-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="72d1c-107">Syntax</span></span>

<span data-ttu-id="72d1c-108">*выражение* . Значений этих</span><span class="sxs-lookup"><span data-stu-id="72d1c-108">*expression* .PartialReplica</span></span>

<span data-ttu-id="72d1c-109">*выражение* Выражение, возвращающее объект **связи** .</span><span class="sxs-lookup"><span data-stu-id="72d1c-109">*expression* An expression that returns a **Relation** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="72d1c-110">Примечания</span><span class="sxs-lookup"><span data-stu-id="72d1c-110">Remarks</span></span>

<span data-ttu-id="72d1c-111">Параметр или возвращаемое значение — это тип данных Boolean, которое имеет **значение True** , когда отношение должно быть реализовано во время синхронизации.</span><span class="sxs-lookup"><span data-stu-id="72d1c-111">The setting or return value is a Boolean data type that is **True** when the relation should be enforced during synchronization.</span></span>

<span data-ttu-id="72d1c-112">Это свойство можно реплицировать данные из полной реплики реплику на основе отношений между таблицами.</span><span class="sxs-lookup"><span data-stu-id="72d1c-112">This property enables you to replicate data from the full replica to the partial replica based on relationships between tables.</span></span> <span data-ttu-id="72d1c-113">**Значений этих** свойств можно использовать, когда установка **этого** сам по себе он не может указать соответствующим образом какие данные следует реплицировать на partial.</span><span class="sxs-lookup"><span data-stu-id="72d1c-113">You can use the **PartialReplica** property when setting the **ReplicaFilter** property alone can't adequately specify what data should be replicated to the partial.</span></span> <span data-ttu-id="72d1c-114">Предположим, например, у вас есть базы данных, в котором таблице Customers содержит один ко многим связь с таблицей заказов и необходимо настроить реплику, который реплицирует только заказы от клиентов в области Калифорния (а не все заказы).</span><span class="sxs-lookup"><span data-stu-id="72d1c-114">For example, suppose you have a database in which the Customers table has a one-to-many relationship with the Orders table, and you want to configure a partial replica that only replicates orders from customers in the California region (instead of all orders).</span></span> <span data-ttu-id="72d1c-115">Невозможно задать **этого** на таблице Orders области = «Центр сертификации» из-за область поля в таблице Customers не в таблице заказов.</span><span class="sxs-lookup"><span data-stu-id="72d1c-115">It is not possible to set the **ReplicaFilter** property on the Orders table to Region = 'CA' because the Region field is in the Customers table, not the Orders table.</span></span>

<span data-ttu-id="72d1c-116">Чтобы реплицировать все заказы из области Калифорния, необходимо указать, что отношения между таблицами заказов и клиентов будет активным во время репликации.</span><span class="sxs-lookup"><span data-stu-id="72d1c-116">To replicate all orders from the California region, you must indicate that the relation between the Orders and Customers tables will be active during replication.</span></span> <span data-ttu-id="72d1c-117">После создания частичные реплики следующие шаги будут внесите в нее все заказы из области Калифорния:</span><span class="sxs-lookup"><span data-stu-id="72d1c-117">Once you've created a partial replica, the following steps will populate it with all orders from the California region:</span></span>

1.  <span data-ttu-id="72d1c-118">Установка **этого** объекта клиенты **TableDef** в «область = «Центр сертификации»».</span><span class="sxs-lookup"><span data-stu-id="72d1c-118">Set the **ReplicaFilter** property on the Customers **TableDef** object to "Region = 'CA'".</span></span>

2.  <span data-ttu-id="72d1c-119">Задайте значение **значений этих** свойств **значения true** на объект **связи** , соответствующий связи между заказов и клиентов.</span><span class="sxs-lookup"><span data-stu-id="72d1c-119">Set the value of the **PartialReplica** property to **True** on the **Relation** object corresponding to the relationship between Orders and Customers.</span></span>

3.  <span data-ttu-id="72d1c-120">Вызовите метод **PopulatePartial** .</span><span class="sxs-lookup"><span data-stu-id="72d1c-120">Invoke the **PopulatePartial** method.</span></span>
    

> [!NOTE]
> <span data-ttu-id="72d1c-121">При установке фильтра реплики или реплики отношение Обратите внимание, что записей частичное реплики, не соответствующие заданным условиям ограничение будет удален из частичные реплики, а не из полной реплики.</span><span class="sxs-lookup"><span data-stu-id="72d1c-121">When you set a replica filter or replica relation, be aware that records in the partial replica that don't satisfy the restriction criteria will be removed from the partial replica, but not from the full replica.</span></span> <span data-ttu-id="72d1c-122">Предположим, например, присвойте свойству **этого** на клиенты **TableDef** в реплику для «область = «Центр сертификации»» и затем повторного заполнения базы данных.</span><span class="sxs-lookup"><span data-stu-id="72d1c-122">For example, suppose you set the **ReplicaFilter** property on the Customers **TableDef** in the partial replica to "Region = 'CA'" and you then repopulate the database.</span></span> <span data-ttu-id="72d1c-123">Будут Вставка или обновление всех записей для клиентов на основе Калифорния.</span><span class="sxs-lookup"><span data-stu-id="72d1c-123">This will insert or update all records for California-based customers.</span></span> 
> 
> <span data-ttu-id="72d1c-124">Затем Сброс **этого** свойства «область = «FL»» и повторного заполнения базы данных, всех записей региона Калифорния частичное реплики будет удален и все записи из клиентов на основе Флорида будет вставлена из полной реплики.</span><span class="sxs-lookup"><span data-stu-id="72d1c-124">If you then reset the **ReplicaFilter** property to "Region = 'FL'" and repopulate the database, all California region records in the partial replica will be removed, and all records from Florida-based customers will be inserted from the full replica.</span></span> <span data-ttu-id="72d1c-125">Нет записи в полной реплики будут удалены.</span><span class="sxs-lookup"><span data-stu-id="72d1c-125">No records in the full replica will be deleted.</span></span> 
>
> <span data-ttu-id="72d1c-126">Прежде чем задать свойство **этого** или **значений этих** , рекомендуется синхронизировать реплику, в которой задаются эти свойства с полной реплики.</span><span class="sxs-lookup"><span data-stu-id="72d1c-126">Before setting either the **ReplicaFilter** or **PartialReplica** property, it's a good idea to synchronize the partial replica in which you are setting these properties with the full replica.</span></span> <span data-ttu-id="72d1c-127">Это гарантирует, что ожидающих изменений в реплику будут объединены в полной реплики перед удаляются все записи в частичные реплики.</span><span class="sxs-lookup"><span data-stu-id="72d1c-127">This will ensure that pending changes in the partial replica will be merged into the full replica before any records are removed in the partial replica.</span></span>



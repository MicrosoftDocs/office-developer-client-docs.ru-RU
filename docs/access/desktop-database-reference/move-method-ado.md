---
title: Метод Move — объекты данных ActiveX (ADO)
TOCTitle: Move method (ADO)
ms:assetid: 1f858654-5fa3-273d-7cdc-574c5f09a420
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248982(v=office.15)
ms:contentKeyID: 48543645
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 6c7db661e590bc21605d9c289b1de6d4ae9f46e2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32288836"
---
# <a name="move-method-ado"></a><span data-ttu-id="b7670-102">Метод Move (ADO)</span><span class="sxs-lookup"><span data-stu-id="b7670-102">Move method (ADO)</span></span>

<span data-ttu-id="b7670-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="b7670-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="b7670-104">Перемещает положение текущей записи в объекте [Recordset](recordset-object-ado.md).</span><span class="sxs-lookup"><span data-stu-id="b7670-104">Moves the position of the current record in a [Recordset](recordset-object-ado.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="b7670-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b7670-105">Syntax</span></span>

<span data-ttu-id="b7670-106">*набор записей*. Перемещение *нумрекордс*, *Пуск*</span><span class="sxs-lookup"><span data-stu-id="b7670-106">*recordset*.Move *NumRecords*, *Start*</span></span>

## <a name="parameters"></a><span data-ttu-id="b7670-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="b7670-107">Parameters</span></span>

|<span data-ttu-id="b7670-108">Параметр</span><span class="sxs-lookup"><span data-stu-id="b7670-108">Parameter</span></span>|<span data-ttu-id="b7670-109">Описание</span><span class="sxs-lookup"><span data-stu-id="b7670-109">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="b7670-110">*нумрекордс*</span><span class="sxs-lookup"><span data-stu-id="b7670-110">*NumRecords*</span></span> |<span data-ttu-id="b7670-111">Выражение со знаком **Long** , задающее количество записей, на которые перемещается положение текущей записи.</span><span class="sxs-lookup"><span data-stu-id="b7670-111">A signed **Long** expression that specifies the number of records that the current record position moves.</span></span>|
|<span data-ttu-id="b7670-112">*Начало*</span><span class="sxs-lookup"><span data-stu-id="b7670-112">*Start*</span></span> |<span data-ttu-id="b7670-113">Необязательное.</span><span class="sxs-lookup"><span data-stu-id="b7670-113">Optional.</span></span> <span data-ttu-id="b7670-114">**Строковое** значение или **Variant** , вычисление которого дает закладку.</span><span class="sxs-lookup"><span data-stu-id="b7670-114">A **String** value or **Variant** that evaluates to a bookmark.</span></span> <span data-ttu-id="b7670-115">Вы также можете использовать значение [букмаркенум](bookmarkenum.md) .</span><span class="sxs-lookup"><span data-stu-id="b7670-115">You can also use a [BookmarkEnum](bookmarkenum.md) value.</span></span>|

## <a name="remarks"></a><span data-ttu-id="b7670-116">Примечания</span><span class="sxs-lookup"><span data-stu-id="b7670-116">Remarks</span></span>

<span data-ttu-id="b7670-117">Метод **Move** поддерживается для всех объектов **Recordset** .</span><span class="sxs-lookup"><span data-stu-id="b7670-117">The **Move** method is supported on all **Recordset** objects.</span></span>

<span data-ttu-id="b7670-118">Если значение аргумента *нумрекордс* больше нуля, текущее положение текущей записи перемещается вперед (ближе к концу **набора записей**).</span><span class="sxs-lookup"><span data-stu-id="b7670-118">If the *NumRecords* argument is greater than zero, the current record position moves forward (toward the end of the **Recordset**).</span></span> <span data-ttu-id="b7670-119">Если *нумрекордс* меньше нуля, текущее положение текущей записи перемещается назад (к началу **набора записей**).</span><span class="sxs-lookup"><span data-stu-id="b7670-119">If *NumRecords* is less than zero, the current record position moves backward (toward the beginning of the **Recordset**).</span></span>

<span data-ttu-id="b7670-120">Если при вызове **Move** положение текущей записи перемещается в точку до первой записи, ADO устанавливает текущую запись в позицию перед первой записью в наборе записей ([BOF](bof-eof-properties-ado.md) имеет **значение true**).</span><span class="sxs-lookup"><span data-stu-id="b7670-120">If the **Move** call would move the current record position to a point before the first record, ADO sets the current record to the position before the first record in the recordset ([BOF](bof-eof-properties-ado.md) is **True**).</span></span> <span data-ttu-id="b7670-121">Попытка перемещения назад, если свойство **BOF** уже имеет **значение true** , приводит к ошибке.</span><span class="sxs-lookup"><span data-stu-id="b7670-121">An attempt to move backward when the **BOF** property is already **True** generates an error.</span></span>

<span data-ttu-id="b7670-122">Если при вызове **Move** положение текущей записи перемещается к точке после последней записи, ADO устанавливает текущую запись в позицию после последней записи в наборе записей ([EOF](bof-eof-properties-ado.md) имеет **значение true**).</span><span class="sxs-lookup"><span data-stu-id="b7670-122">If the **Move** call would move the current record position to a point after the last record, ADO sets the current record to the position after the last record in the recordset ([EOF](bof-eof-properties-ado.md) is **True**).</span></span> <span data-ttu-id="b7670-123">Попытка перемещения вперед, если свойство **EOF** уже имеет **значение true** , приводит к ошибке.</span><span class="sxs-lookup"><span data-stu-id="b7670-123">An attempt to move forward when the **EOF** property is already **True** generates an error.</span></span>

<span data-ttu-id="b7670-124">При вызове метода **Move** из пустого объекта **Recordset** возникает ошибка.</span><span class="sxs-lookup"><span data-stu-id="b7670-124">Calling the **Move** method from an empty **Recordset** object generates an error.</span></span>

<span data-ttu-id="b7670-125">При передаче аргумента *Start* перемещение задается относительно записи с этой закладкой, предполагая, что объект **Recordset** поддерживает закладки.</span><span class="sxs-lookup"><span data-stu-id="b7670-125">If you pass the *Start* argument, the move is relative to the record with this bookmark, assuming the **Recordset** object supports bookmarks.</span></span> <span data-ttu-id="b7670-126">Если этот параметр не указан, то перемещение выполняется относительно текущей записи.</span><span class="sxs-lookup"><span data-stu-id="b7670-126">If not specified, the move is relative to the current record.</span></span>

<span data-ttu-id="b7670-127">Если для локального кэширования записей из поставщика используется свойство [CacheSize](cachesize-property-ado.md) , передача аргумента *нумрекордс* , который перемещает текущую запись за прев КЭШЕ записи, заставляет ADO получить новую группу записей, начиная с целевой записи.</span><span class="sxs-lookup"><span data-stu-id="b7670-127">If you are using the [CacheSize](cachesize-property-ado.md) property to locally cache records from the provider, passing a *NumRecords* argument that moves the current record position outside the current group of cached records forces ADO to retrieve a new group of records, starting from the destination record.</span></span> <span data-ttu-id="b7670-128">Свойство **CacheSize** определяет размер вновь извлеченной группы, а конечную запись — первую извлеченную запись.</span><span class="sxs-lookup"><span data-stu-id="b7670-128">The **CacheSize** property determines the size of the newly retrieved group, and the destination record is the first record retrieved.</span></span>

<span data-ttu-id="b7670-129">Если объект **Recordset** предназначен только для переадресации, то пользователь по-прежнему может передавать аргумент *нумрекордс* , значение которого меньше нуля, при условии, что целевой объект находится в текущем наборе кэшированных записей.</span><span class="sxs-lookup"><span data-stu-id="b7670-129">If the **Recordset** object is forward only, a user can still pass a *NumRecords* argument less than zero, provided the destination is within the current set of cached records.</span></span> <span data-ttu-id="b7670-130">Если при вызове **Move** положение текущей записи перемещается в запись до первой кэшированной записи, возникнет ошибка.</span><span class="sxs-lookup"><span data-stu-id="b7670-130">If the **Move** call would move the current record position to a record before the first cached record, an error will occur.</span></span> <span data-ttu-id="b7670-131">Таким образом, вы можете использовать кэш записей, который поддерживает полную прокрутку для поставщика, поддерживающего только прямую прокрутку.</span><span class="sxs-lookup"><span data-stu-id="b7670-131">Thus, you can use a record cache that supports full scrolling over a provider that supports only forward scrolling.</span></span> <span data-ttu-id="b7670-132">Так как кэшированные записи загружаются в память, не следует кэшировать больше записей, чем требуется.</span><span class="sxs-lookup"><span data-stu-id="b7670-132">Because cached records are loaded into memory, you should avoid caching more records than is necessary.</span></span> <span data-ttu-id="b7670-133">Даже если объект **Recordset** с последовательным использованием поддерживает обратное перемещение таким способом, вызов метода [MovePrevious](movefirst-movelast-movenext-and-moveprevious-methods-ado.md) для любого объекта **Recordset** с последовательной поддержкой будет по-прежнему вызывать ошибку.</span><span class="sxs-lookup"><span data-stu-id="b7670-133">Even if a forward-only **Recordset** object supports backward moves in this way, calling the [MovePrevious](movefirst-movelast-movenext-and-moveprevious-methods-ado.md) method on any forward-only **Recordset** object will still generate an error.</span></span>


> [!NOTE]
> <span data-ttu-id="b7670-134">Поддержка перемещения в обратном направлении в **наборе записей** с последовательным входом не является прогнозируемой в зависимости от поставщика.</span><span class="sxs-lookup"><span data-stu-id="b7670-134">Support for moving backwards in a forward-only **Recordset** is not predictable, depending upon your provider.</span></span> <span data-ttu-id="b7670-135">Если текущая запись была постионед после последней записи в **наборе записей**, **Перемещение** в обратном направлении может не привести к правильному текущему положению.</span><span class="sxs-lookup"><span data-stu-id="b7670-135">If the current record has been postioned after the last record in the **Recordset**, **Move** backwards may not result in the correct current position.</span></span>



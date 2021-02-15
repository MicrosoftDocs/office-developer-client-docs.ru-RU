---
title: Move Method - ActiveX Data Objects (ADO)
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
# <a name="move-method-ado"></a><span data-ttu-id="f88c8-102">Метод Move (ADO)</span><span class="sxs-lookup"><span data-stu-id="f88c8-102">Move method (ADO)</span></span>

<span data-ttu-id="f88c8-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="f88c8-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="f88c8-104">Перемещает положение текущей записи в объекте [Recordset](recordset-object-ado.md).</span><span class="sxs-lookup"><span data-stu-id="f88c8-104">Moves the position of the current record in a [Recordset](recordset-object-ado.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="f88c8-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f88c8-105">Syntax</span></span>

<span data-ttu-id="f88c8-106">*recordset*. Move *NumRecords,* *Start*</span><span class="sxs-lookup"><span data-stu-id="f88c8-106">*recordset*.Move *NumRecords*, *Start*</span></span>

## <a name="parameters"></a><span data-ttu-id="f88c8-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="f88c8-107">Parameters</span></span>

|<span data-ttu-id="f88c8-108">Параметр</span><span class="sxs-lookup"><span data-stu-id="f88c8-108">Parameter</span></span>|<span data-ttu-id="f88c8-109">Описание</span><span class="sxs-lookup"><span data-stu-id="f88c8-109">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="f88c8-110">*NumRecords*</span><span class="sxs-lookup"><span data-stu-id="f88c8-110">*NumRecords*</span></span> |<span data-ttu-id="f88c8-111">Подписанное **длинное** выражение, которое указывает число записей, перемещаемого текущей записью.</span><span class="sxs-lookup"><span data-stu-id="f88c8-111">A signed **Long** expression that specifies the number of records that the current record position moves.</span></span>|
|<span data-ttu-id="f88c8-112">*Начало*</span><span class="sxs-lookup"><span data-stu-id="f88c8-112">*Start*</span></span> |<span data-ttu-id="f88c8-113">Необязательный параметр.</span><span class="sxs-lookup"><span data-stu-id="f88c8-113">Optional.</span></span> <span data-ttu-id="f88c8-114">**Строка** или **вариант,** оцениваемая в закладке.</span><span class="sxs-lookup"><span data-stu-id="f88c8-114">A **String** value or **Variant** that evaluates to a bookmark.</span></span> <span data-ttu-id="f88c8-115">Также можно использовать значение [BookmarkEnum.](bookmarkenum.md)</span><span class="sxs-lookup"><span data-stu-id="f88c8-115">You can also use a [BookmarkEnum](bookmarkenum.md) value.</span></span>|

## <a name="remarks"></a><span data-ttu-id="f88c8-116">Заметки</span><span class="sxs-lookup"><span data-stu-id="f88c8-116">Remarks</span></span>

<span data-ttu-id="f88c8-117">Метод **Move** поддерживается для всех объектов **Recordset.**</span><span class="sxs-lookup"><span data-stu-id="f88c8-117">The **Move** method is supported on all **Recordset** objects.</span></span>

<span data-ttu-id="f88c8-118">Если аргумент *NumRecords* больше нуля, текущая позиция записи перемещается вперед (ближе к концу **recordset).**</span><span class="sxs-lookup"><span data-stu-id="f88c8-118">If the *NumRecords* argument is greater than zero, the current record position moves forward (toward the end of the **Recordset**).</span></span> <span data-ttu-id="f88c8-119">Если *значение NumRecords* меньше нуля, текущая позиция записи перемещается назад (в начало **recordset).**</span><span class="sxs-lookup"><span data-stu-id="f88c8-119">If *NumRecords* is less than zero, the current record position moves backward (toward the beginning of the **Recordset**).</span></span>

<span data-ttu-id="f88c8-120">Если вызов **Move** переместит текущую запись в точку перед первой записью, ADO устанавливает текущую запись в положение перед первой записью в наборе записей ([BOF](bof-eof-properties-ado.md) имеет **true).**</span><span class="sxs-lookup"><span data-stu-id="f88c8-120">If the **Move** call would move the current record position to a point before the first record, ADO sets the current record to the position before the first record in the recordset ([BOF](bof-eof-properties-ado.md) is **True**).</span></span> <span data-ttu-id="f88c8-121">Попытка перейти назад, когда свойство **BOF** уже имеет свойство **True,** вызывает ошибку.</span><span class="sxs-lookup"><span data-stu-id="f88c8-121">An attempt to move backward when the **BOF** property is already **True** generates an error.</span></span>

<span data-ttu-id="f88c8-122">Если вызов **Move** переместит текущую запись в точку после последней записи, ADO устанавливает текущую запись в положение после последней записи в наборе записей ([EOF](bof-eof-properties-ado.md) имеет **true).**</span><span class="sxs-lookup"><span data-stu-id="f88c8-122">If the **Move** call would move the current record position to a point after the last record, ADO sets the current record to the position after the last record in the recordset ([EOF](bof-eof-properties-ado.md) is **True**).</span></span> <span data-ttu-id="f88c8-123">Попытка двигаться вперед, когда свойство **EOF** уже имеет свойство **True,** вызывает ошибку.</span><span class="sxs-lookup"><span data-stu-id="f88c8-123">An attempt to move forward when the **EOF** property is already **True** generates an error.</span></span>

<span data-ttu-id="f88c8-124">Вызов метода **Move** из пустого **объекта Recordset** создает ошибку.</span><span class="sxs-lookup"><span data-stu-id="f88c8-124">Calling the **Move** method from an empty **Recordset** object generates an error.</span></span>

<span data-ttu-id="f88c8-125">Если передать аргумент *Start,* перемещение будет относительно записи с этой закладкой, если объект **Recordset** поддерживает закладки.</span><span class="sxs-lookup"><span data-stu-id="f88c8-125">If you pass the *Start* argument, the move is relative to the record with this bookmark, assuming the **Recordset** object supports bookmarks.</span></span> <span data-ttu-id="f88c8-126">Если не указано, перемещение относительно текущей записи.</span><span class="sxs-lookup"><span data-stu-id="f88c8-126">If not specified, the move is relative to the current record.</span></span>

<span data-ttu-id="f88c8-127">Если вы используете свойство [CacheSize](cachesize-property-ado.md) для локального кэшации записей от поставщика, передав аргумент *NumRecords,* который перемещает текущую запись за пределы текущей группы кэшных записей, ADO будет извлекать новую группу записей, начиная с конечной записи.</span><span class="sxs-lookup"><span data-stu-id="f88c8-127">If you are using the [CacheSize](cachesize-property-ado.md) property to locally cache records from the provider, passing a *NumRecords* argument that moves the current record position outside the current group of cached records forces ADO to retrieve a new group of records, starting from the destination record.</span></span> <span data-ttu-id="f88c8-128">Свойство **CacheSize** определяет размер новой извлекаемой группы, а запись назначения является первой извлеченной записью.</span><span class="sxs-lookup"><span data-stu-id="f88c8-128">The **CacheSize** property determines the size of the newly retrieved group, and the destination record is the first record retrieved.</span></span>

<span data-ttu-id="f88c8-129">Если объект **Recordset** только перенаправлен, пользователь может передать аргумент *NumRecords* меньше нуля, если назначение находится в текущем наборе кэшных записей.</span><span class="sxs-lookup"><span data-stu-id="f88c8-129">If the **Recordset** object is forward only, a user can still pass a *NumRecords* argument less than zero, provided the destination is within the current set of cached records.</span></span> <span data-ttu-id="f88c8-130">Если вызов **Move** переместит текущую запись в запись перед первой кэшной записью, произойдет ошибка.</span><span class="sxs-lookup"><span data-stu-id="f88c8-130">If the **Move** call would move the current record position to a record before the first cached record, an error will occur.</span></span> <span data-ttu-id="f88c8-131">Таким образом, можно использовать кэш записей, поддерживаюющий полную прокрутку поставщика, который поддерживает только прокрутку вперед.</span><span class="sxs-lookup"><span data-stu-id="f88c8-131">Thus, you can use a record cache that supports full scrolling over a provider that supports only forward scrolling.</span></span> <span data-ttu-id="f88c8-132">Так как кэшные записи загружаются в память, не следует кэшировать больше записей, чем необходимо.</span><span class="sxs-lookup"><span data-stu-id="f88c8-132">Because cached records are loaded into memory, you should avoid caching more records than is necessary.</span></span> <span data-ttu-id="f88c8-133">Даже если объект **Recordset** только для переадрешенности поддерживает обратные перемещения таким образом, вызов метода [MovePrevious](movefirst-movelast-movenext-and-moveprevious-methods-ado.md) для любого объекта **Recordset** только для переадреансирования по-прежнему будет создавать ошибку.</span><span class="sxs-lookup"><span data-stu-id="f88c8-133">Even if a forward-only **Recordset** object supports backward moves in this way, calling the [MovePrevious](movefirst-movelast-movenext-and-moveprevious-methods-ado.md) method on any forward-only **Recordset** object will still generate an error.</span></span>


> [!NOTE]
> <span data-ttu-id="f88c8-134">Поддержка перемещения назад в наборе  записей, поддерживающего только вперед, не является предсказуемой в зависимости от поставщика.</span><span class="sxs-lookup"><span data-stu-id="f88c8-134">Support for moving backwards in a forward-only **Recordset** is not predictable, depending upon your provider.</span></span> <span data-ttu-id="f88c8-135">Если текущая запись была опубликована после последней записи в наборе записей, перемещение назад может привести к неправильному текущему положению.  </span><span class="sxs-lookup"><span data-stu-id="f88c8-135">If the current record has been postioned after the last record in the **Recordset**, **Move** backwards may not result in the correct current position.</span></span>



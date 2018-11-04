---
title: Метод - Move ActiveX Data Objects (ADO)
TOCTitle: Move method (ADO)
ms:assetid: 1f858654-5fa3-273d-7cdc-574c5f09a420
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248982(v=office.15)
ms:contentKeyID: 48543645
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 30feb9aabeb84c577b415b2872ce407cf3fc0f44
ms.sourcegitcommit: 980a96cf444882d3d34cecb5faac8f8a7b7c4b57
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/03/2018
ms.locfileid: "25950008"
---
# <a name="move-method-ado"></a><span data-ttu-id="a8843-102">Метод Move (ADO)</span><span class="sxs-lookup"><span data-stu-id="a8843-102">Move method (ADO)</span></span>

<span data-ttu-id="a8843-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="a8843-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="a8843-104">Перемещает положение текущей записи в объекте [набора записей](recordset-object-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="a8843-104">Moves the position of the current record in a [Recordset](recordset-object-ado.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="a8843-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a8843-105">Syntax</span></span>

<span data-ttu-id="a8843-106">*набор записей*. Перемещение *NumRecords*, *запустите*</span><span class="sxs-lookup"><span data-stu-id="a8843-106">*recordset*.Move *NumRecords*, *Start*</span></span>

## <a name="parameters"></a><span data-ttu-id="a8843-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="a8843-107">Parameters</span></span>

|<span data-ttu-id="a8843-108">Параметр</span><span class="sxs-lookup"><span data-stu-id="a8843-108">Parameter</span></span>|<span data-ttu-id="a8843-109">Описание</span><span class="sxs-lookup"><span data-stu-id="a8843-109">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="a8843-110">*NumRecords*</span><span class="sxs-lookup"><span data-stu-id="a8843-110">*NumRecords*</span></span> |<span data-ttu-id="a8843-111">A подписанные **длинный** выражение, которое указывает количество записей, которые перемещает положение текущей записи.</span><span class="sxs-lookup"><span data-stu-id="a8843-111">A signed **Long** expression that specifies the number of records that the current record position moves.</span></span>|
|<span data-ttu-id="a8843-112">*Start*</span><span class="sxs-lookup"><span data-stu-id="a8843-112">*Start*</span></span> |<span data-ttu-id="a8843-113">Необязательно указывать.</span><span class="sxs-lookup"><span data-stu-id="a8843-113">Optional.</span></span> <span data-ttu-id="a8843-114">Значение **String** или **Variant** , которое оценивается как закладку.</span><span class="sxs-lookup"><span data-stu-id="a8843-114">A **String** value or **Variant** that evaluates to a bookmark.</span></span> <span data-ttu-id="a8843-115">Можно также использовать значение [BookmarkEnum](bookmarkenum.md) .</span><span class="sxs-lookup"><span data-stu-id="a8843-115">You can also use a [BookmarkEnum](bookmarkenum.md) value.</span></span>|

## <a name="remarks"></a><span data-ttu-id="a8843-116">Примечания</span><span class="sxs-lookup"><span data-stu-id="a8843-116">Remarks</span></span>

<span data-ttu-id="a8843-117">Метод **Move** поддерживается для всех объектов **набора записей** .</span><span class="sxs-lookup"><span data-stu-id="a8843-117">The **Move** method is supported on all **Recordset** objects.</span></span>

<span data-ttu-id="a8843-118">Если аргумент *NumRecords* больше нуля, в настоящее время записи переход (ближе к концу **набора записей**).</span><span class="sxs-lookup"><span data-stu-id="a8843-118">If the *NumRecords* argument is greater than zero, the current record position moves forward (toward the end of the **Recordset**).</span></span> <span data-ttu-id="a8843-119">Если *NumRecords* меньше нуля, положение текущей записи переход назад (к началу **набора записей**).</span><span class="sxs-lookup"><span data-stu-id="a8843-119">If *NumRecords* is less than zero, the current record position moves backward (toward the beginning of the **Recordset**).</span></span>

<span data-ttu-id="a8843-120">Если звонок **Перемещение** перемещает положение текущей записи в точку перед первой записи, ADO задает текущую запись позицию перед первой записи в наборе записей ([BOF](bof-eof-properties-ado.md) имеет **значение True**).</span><span class="sxs-lookup"><span data-stu-id="a8843-120">If the **Move** call would move the current record position to a point before the first record, ADO sets the current record to the position before the first record in the recordset ([BOF](bof-eof-properties-ado.md) is **True**).</span></span> <span data-ttu-id="a8843-121">При попытке выполнить переход назад, если свойство **BOF** уже имеет **значение True,** приводит к ошибке.</span><span class="sxs-lookup"><span data-stu-id="a8843-121">An attempt to move backward when the **BOF** property is already **True** generates an error.</span></span>

<span data-ttu-id="a8843-122">Если звонок **Перемещение** перемещает положение текущей записи до момента после последней записи, ADO задает текущей позиции после последней записи в наборе записей ([EOF](bof-eof-properties-ado.md) имеет **значение True**).</span><span class="sxs-lookup"><span data-stu-id="a8843-122">If the **Move** call would move the current record position to a point after the last record, ADO sets the current record to the position after the last record in the recordset ([EOF](bof-eof-properties-ado.md) is **True**).</span></span> <span data-ttu-id="a8843-123">При попытке переместить вперед в том случае, если свойство **EOF** уже имеет **значение True** приведет к ошибке.</span><span class="sxs-lookup"><span data-stu-id="a8843-123">An attempt to move forward when the **EOF** property is already **True** generates an error.</span></span>

<span data-ttu-id="a8843-124">Вызов метода **Move** из **пустой Recordset** приводит к ошибке.</span><span class="sxs-lookup"><span data-stu-id="a8843-124">Calling the **Move** method from an empty **Recordset** object generates an error.</span></span>

<span data-ttu-id="a8843-125">Если передать аргумент *Начать* перемещение задается запись с эту закладку, при условии, что объект **набора записей** поддерживает закладки.</span><span class="sxs-lookup"><span data-stu-id="a8843-125">If you pass the *Start* argument, the move is relative to the record with this bookmark, assuming the **Recordset** object supports bookmarks.</span></span> <span data-ttu-id="a8843-126">Если не указан, move — относительно текущей записи.</span><span class="sxs-lookup"><span data-stu-id="a8843-126">If not specified, the move is relative to the current record.</span></span>

<span data-ttu-id="a8843-127">Если вы используете свойство [CacheSize](cachesize-property-ado.md) в локальный кэш записи от поставщика, передав *NumRecords* аргумент, который перемещает текущую позицию записи за пределами текущей группы кэшированной записи принудительно ADO для извлечения новую группу записей, начиная с записи назначения.</span><span class="sxs-lookup"><span data-stu-id="a8843-127">If you are using the [CacheSize](cachesize-property-ado.md) property to locally cache records from the provider, passing a *NumRecords* argument that moves the current record position outside the current group of cached records forces ADO to retrieve a new group of records, starting from the destination record.</span></span> <span data-ttu-id="a8843-128">Свойство **CacheSize** определяет размер группы вновь извлеченных и запись назначения является первой записи извлечен.</span><span class="sxs-lookup"><span data-stu-id="a8843-128">The **CacheSize** property determines the size of the newly retrieved group, and the destination record is the first record retrieved.</span></span>

<span data-ttu-id="a8843-129">Если объект **набора записей** вперед только, пользователь по-прежнему должно пройти *NumRecords* аргумент меньше нуля, условии, что получатель находится в пределах текущего набора кэшированной записи.</span><span class="sxs-lookup"><span data-stu-id="a8843-129">If the **Recordset** object is forward only, a user can still pass a *NumRecords* argument less than zero, provided the destination is within the current set of cached records.</span></span> <span data-ttu-id="a8843-130">Если звонок **Перемещение** переместится в настоящее время записи в записи перед первой кэшированной записи, возникает ошибка.</span><span class="sxs-lookup"><span data-stu-id="a8843-130">If the **Move** call would move the current record position to a record before the first cached record, an error will occur.</span></span> <span data-ttu-id="a8843-131">Таким образом можно использовать в кэш записи, которая поддерживает полный прокрутке поставщика, который поддерживает только перемещение вперед.</span><span class="sxs-lookup"><span data-stu-id="a8843-131">Thus, you can use a record cache that supports full scrolling over a provider that supports only forward scrolling.</span></span> <span data-ttu-id="a8843-132">Так как кэшированной записи, загруженных в память, следует избегать кэширование больше записей, чем это необходимо.</span><span class="sxs-lookup"><span data-stu-id="a8843-132">Because cached records are loaded into memory, you should avoid caching more records than is necessary.</span></span> <span data-ttu-id="a8843-133">Даже в том случае, если только вперед **записей** объект поддерживает обратной перемещается таким образом, вызов метода [MovePrevious](movefirst-movelast-movenext-and-moveprevious-methods-ado.md) для любого объекта **набора записей** только вперед по-прежнему приведет к ошибке.</span><span class="sxs-lookup"><span data-stu-id="a8843-133">Even if a forward-only **Recordset** object supports backward moves in this way, calling the [MovePrevious](movefirst-movelast-movenext-and-moveprevious-methods-ado.md) method on any forward-only **Recordset** object will still generate an error.</span></span>


> [!NOTE]
> <span data-ttu-id="a8843-134">Поддержка обратной перемещения в однонаправленные **записей** не прогнозируемый, в зависимости от вашего поставщика.</span><span class="sxs-lookup"><span data-stu-id="a8843-134">Support for moving backwards in a forward-only **Recordset** is not predictable, depending upon your provider.</span></span> <span data-ttu-id="a8843-135">Если текущая запись была postioned после последней записи в **набор записей**, **Переместите** обратной может появиться не правильный текущей позиции.</span><span class="sxs-lookup"><span data-stu-id="a8843-135">If the current record has been postioned after the last record in the **Recordset**, **Move** backwards may not result in the correct current position.</span></span>



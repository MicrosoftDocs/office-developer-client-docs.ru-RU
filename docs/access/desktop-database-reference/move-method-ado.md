---
title: Метод - Move ActiveX Data Objects (ADO)
TOCTitle: Move method (ADO)
ms:assetid: 1f858654-5fa3-273d-7cdc-574c5f09a420
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248982(v=office.15)
ms:contentKeyID: 48543645
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 55439f14cd2a498ec2592c533dd308f82798b1e8
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/02/2018
ms.locfileid: "25929449"
---
# <a name="move-method-ado"></a><span data-ttu-id="b10c5-102">Метод Move (ADO)</span><span class="sxs-lookup"><span data-stu-id="b10c5-102">Move method (ADO)</span></span>


<span data-ttu-id="b10c5-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="b10c5-103">**Applies to**: Access 2013, Office 2013</span></span>



<span data-ttu-id="b10c5-104">Перемещает положение текущей записи в объекте [набора записей](recordset-object-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="b10c5-104">Moves the position of the current record in a [Recordset](recordset-object-ado.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="b10c5-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b10c5-105">Syntax</span></span>

<span data-ttu-id="b10c5-106">*набор записей*. Перемещение *NumRecords*, *запустите*</span><span class="sxs-lookup"><span data-stu-id="b10c5-106">*recordset*.Move *NumRecords*, *Start*</span></span>

## <a name="parameters"></a><span data-ttu-id="b10c5-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="b10c5-107">Parameters</span></span>

  - <span data-ttu-id="b10c5-108">*NumRecords*</span><span class="sxs-lookup"><span data-stu-id="b10c5-108">*NumRecords*</span></span>

  - <span data-ttu-id="b10c5-109">A подписанные **длинный** выражение, которое указывает количество записей, которые перемещает положение текущей записи.</span><span class="sxs-lookup"><span data-stu-id="b10c5-109">A signed **Long** expression that specifies the number of records that the current record position moves.</span></span>

  - <span data-ttu-id="b10c5-110">*Start*</span><span class="sxs-lookup"><span data-stu-id="b10c5-110">*Start*</span></span>

  - <span data-ttu-id="b10c5-111">Необязательно указывать.</span><span class="sxs-lookup"><span data-stu-id="b10c5-111">Optional.</span></span> <span data-ttu-id="b10c5-112">Значение **String** или **Variant** , которое оценивается как закладку.</span><span class="sxs-lookup"><span data-stu-id="b10c5-112">A **String** value or **Variant** that evaluates to a bookmark.</span></span> <span data-ttu-id="b10c5-113">Можно также использовать значение [BookmarkEnum](bookmarkenum.md) .</span><span class="sxs-lookup"><span data-stu-id="b10c5-113">You can also use a [BookmarkEnum](bookmarkenum.md) value.</span></span>

## <a name="remarks"></a><span data-ttu-id="b10c5-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="b10c5-114">Remarks</span></span>

<span data-ttu-id="b10c5-115">Метод **Move** поддерживается для всех объектов **набора записей** .</span><span class="sxs-lookup"><span data-stu-id="b10c5-115">The **Move** method is supported on all **Recordset** objects.</span></span>

<span data-ttu-id="b10c5-116">Если аргумент *NumRecords* больше нуля, в настоящее время записи переход (ближе к концу **набора записей**).</span><span class="sxs-lookup"><span data-stu-id="b10c5-116">If the *NumRecords* argument is greater than zero, the current record position moves forward (toward the end of the **Recordset**).</span></span> <span data-ttu-id="b10c5-117">Если *NumRecords* меньше нуля, положение текущей записи переход назад (к началу **набора записей**).</span><span class="sxs-lookup"><span data-stu-id="b10c5-117">If *NumRecords* is less than zero, the current record position moves backward (toward the beginning of the **Recordset**).</span></span>

<span data-ttu-id="b10c5-118">Если звонок **Перемещение** перемещает положение текущей записи в точку перед первой записи, ADO задает текущую запись позицию перед первой записи в наборе записей ([BOF](bof-eof-properties-ado.md) имеет **значение True**).</span><span class="sxs-lookup"><span data-stu-id="b10c5-118">If the **Move** call would move the current record position to a point before the first record, ADO sets the current record to the position before the first record in the recordset ([BOF](bof-eof-properties-ado.md) is **True**).</span></span> <span data-ttu-id="b10c5-119">При попытке выполнить переход назад, если свойство **BOF** уже имеет **значение True,** приводит к ошибке.</span><span class="sxs-lookup"><span data-stu-id="b10c5-119">An attempt to move backward when the **BOF** property is already **True** generates an error.</span></span>

<span data-ttu-id="b10c5-120">Если звонок **Перемещение** перемещает положение текущей записи до момента после последней записи, ADO задает текущей позиции после последней записи в наборе записей ([EOF](bof-eof-properties-ado.md) имеет **значение True**).</span><span class="sxs-lookup"><span data-stu-id="b10c5-120">If the **Move** call would move the current record position to a point after the last record, ADO sets the current record to the position after the last record in the recordset ([EOF](bof-eof-properties-ado.md) is **True**).</span></span> <span data-ttu-id="b10c5-121">При попытке переместить вперед в том случае, если свойство **EOF** уже имеет **значение True** приведет к ошибке.</span><span class="sxs-lookup"><span data-stu-id="b10c5-121">An attempt to move forward when the **EOF** property is already **True** generates an error.</span></span>

<span data-ttu-id="b10c5-122">Вызов метода **Move** из **пустой Recordset** приводит к ошибке.</span><span class="sxs-lookup"><span data-stu-id="b10c5-122">Calling the **Move** method from an empty **Recordset** object generates an error.</span></span>

<span data-ttu-id="b10c5-123">Если передать аргумент *Начать* перемещение задается запись с эту закладку, при условии, что объект **набора записей** поддерживает закладки.</span><span class="sxs-lookup"><span data-stu-id="b10c5-123">If you pass the *Start* argument, the move is relative to the record with this bookmark, assuming the **Recordset** object supports bookmarks.</span></span> <span data-ttu-id="b10c5-124">Если не указан, move — относительно текущей записи.</span><span class="sxs-lookup"><span data-stu-id="b10c5-124">If not specified, the move is relative to the current record.</span></span>

<span data-ttu-id="b10c5-125">Если вы используете свойство [CacheSize](cachesize-property-ado.md) в локальный кэш записи от поставщика, передав *NumRecords* аргумент, который перемещает текущую позицию записи за пределами текущей группы кэшированной записи принудительно ADO для извлечения новую группу записей, начиная с записи назначения.</span><span class="sxs-lookup"><span data-stu-id="b10c5-125">If you are using the [CacheSize](cachesize-property-ado.md) property to locally cache records from the provider, passing a *NumRecords* argument that moves the current record position outside the current group of cached records forces ADO to retrieve a new group of records, starting from the destination record.</span></span> <span data-ttu-id="b10c5-126">Свойство **CacheSize** определяет размер группы вновь извлеченных и запись назначения является первой записи извлечен.</span><span class="sxs-lookup"><span data-stu-id="b10c5-126">The **CacheSize** property determines the size of the newly retrieved group, and the destination record is the first record retrieved.</span></span>

<span data-ttu-id="b10c5-127">Если объект **набора записей** вперед только, пользователь по-прежнему должно пройти *NumRecords* аргумент меньше нуля, условии, что получатель находится в пределах текущего набора кэшированной записи.</span><span class="sxs-lookup"><span data-stu-id="b10c5-127">If the **Recordset** object is forward only, a user can still pass a *NumRecords* argument less than zero, provided the destination is within the current set of cached records.</span></span> <span data-ttu-id="b10c5-128">Если звонок **Перемещение** переместится в настоящее время записи в записи перед первой кэшированной записи, возникает ошибка.</span><span class="sxs-lookup"><span data-stu-id="b10c5-128">If the **Move** call would move the current record position to a record before the first cached record, an error will occur.</span></span> <span data-ttu-id="b10c5-129">Таким образом можно использовать в кэш записи, которая поддерживает полный прокрутке поставщика, который поддерживает только перемещение вперед.</span><span class="sxs-lookup"><span data-stu-id="b10c5-129">Thus, you can use a record cache that supports full scrolling over a provider that supports only forward scrolling.</span></span> <span data-ttu-id="b10c5-130">Так как кэшированной записи, загруженных в память, следует избегать кэширование больше записей, чем это необходимо.</span><span class="sxs-lookup"><span data-stu-id="b10c5-130">Because cached records are loaded into memory, you should avoid caching more records than is necessary.</span></span> <span data-ttu-id="b10c5-131">Даже в том случае, если только вперед **записей** объект поддерживает обратной перемещается таким образом, вызов метода [MovePrevious](movefirst-movelast-movenext-and-moveprevious-methods-ado.md) для любого объекта **набора записей** только вперед по-прежнему приведет к ошибке.</span><span class="sxs-lookup"><span data-stu-id="b10c5-131">Even if a forward-only **Recordset** object supports backward moves in this way, calling the [MovePrevious](movefirst-movelast-movenext-and-moveprevious-methods-ado.md) method on any forward-only **Recordset** object will still generate an error.</span></span>


> [!NOTE]
> <span data-ttu-id="b10c5-132">Поддержка обратной перемещения в однонаправленные **записей** не прогнозируемый, в зависимости от вашего поставщика.</span><span class="sxs-lookup"><span data-stu-id="b10c5-132">Support for moving backwards in a forward-only **Recordset** is not predictable, depending upon your provider.</span></span> <span data-ttu-id="b10c5-133">Если текущая запись была postioned после последней записи в **набор записей**, **Переместите** обратной может появиться не правильный текущей позиции.</span><span class="sxs-lookup"><span data-stu-id="b10c5-133">If the current record has been postioned after the last record in the **Recordset**, **Move** backwards may not result in the correct current position.</span></span>



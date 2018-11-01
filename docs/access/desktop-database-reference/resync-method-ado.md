---
title: Выполнить повторную синхронизацию метод (ADO)
TOCTitle: Resync Method (ADO)
ms:assetid: f594a200-56e6-fcf5-9b0a-900c56377f24
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250251(v=office.15)
ms:contentKeyID: 48548717
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 3d8e4a863449d8aea5d95002a6183978d9ca953a
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25884501"
---
# <a name="resync-method-ado"></a><span data-ttu-id="e6702-102">Выполнить повторную синхронизацию метод (ADO)</span><span class="sxs-lookup"><span data-stu-id="e6702-102">Resync Method (ADO)</span></span>


<span data-ttu-id="e6702-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="e6702-103">**Applies to**: Access 2013, Office 2013</span></span>



<span data-ttu-id="e6702-104">Обновляет данные в текущий объект [набора записей](recordset-object-ado.md) или коллекции [полей](fields-collection-ado.md) объекта [записи](record-object-ado.md) из базы данных.</span><span class="sxs-lookup"><span data-stu-id="e6702-104">Refreshes the data in the current [Recordset](recordset-object-ado.md) object, or [Fields](fields-collection-ado.md) collection of a [Record](record-object-ado.md) object, from the underlying database.</span></span>

## <a name="syntax"></a><span data-ttu-id="e6702-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e6702-105">Syntax</span></span>

<span data-ttu-id="e6702-106">*Набор записей*. Выполнить повторную синхронизацию*AffectRecords*, *ResyncValues*</span><span class="sxs-lookup"><span data-stu-id="e6702-106">*Recordset*.Resync*AffectRecords*, *ResyncValues*</span></span>

<span data-ttu-id="e6702-107">*Запись*.</span><span class="sxs-lookup"><span data-stu-id="e6702-107">*Record*.</span></span> <span data-ttu-id="e6702-108">*Поля*. Выполнить повторную синхронизацию*ResyncValues*</span><span class="sxs-lookup"><span data-stu-id="e6702-108">*Fields*.Resync*ResyncValues*</span></span>

## <a name="parameters"></a><span data-ttu-id="e6702-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="e6702-109">Parameters</span></span>

  - <span data-ttu-id="e6702-110">*AffectRecords*</span><span class="sxs-lookup"><span data-stu-id="e6702-110">*AffectRecords*</span></span>

  - <span data-ttu-id="e6702-111">Необязательный параметр.</span><span class="sxs-lookup"><span data-stu-id="e6702-111">Optional.</span></span> <span data-ttu-id="e6702-112">От [AffectEnum](affectenum.md) значение, определяющее число записей влияет на метод **выполнить повторную синхронизацию** .</span><span class="sxs-lookup"><span data-stu-id="e6702-112">An [AffectEnum](affectenum.md) value that determines how many records the **Resync** method will affect.</span></span> <span data-ttu-id="e6702-113">Значение по умолчанию — **adAffectAll**.</span><span class="sxs-lookup"><span data-stu-id="e6702-113">The default value is **adAffectAll**.</span></span> <span data-ttu-id="e6702-114">Это значение с помощью метода **выполнить повторную синхронизацию** коллекции **полей** объекта **записи** недоступен.</span><span class="sxs-lookup"><span data-stu-id="e6702-114">This value is not available with the **Resync** method of the **Fields** collection of a **Record** object.</span></span>

  - <span data-ttu-id="e6702-115">*ResyncValues*</span><span class="sxs-lookup"><span data-stu-id="e6702-115">*ResyncValues*</span></span>

  - <span data-ttu-id="e6702-116">Необязательный параметр.</span><span class="sxs-lookup"><span data-stu-id="e6702-116">Optional.</span></span> <span data-ttu-id="e6702-117">Значение [ResyncEnum](resyncenum.md) , указывает ли базового значения перезаписываются.</span><span class="sxs-lookup"><span data-stu-id="e6702-117">A [ResyncEnum](resyncenum.md) value that specifies whether underlying values are overwritten.</span></span> <span data-ttu-id="e6702-118">Значение по умолчанию — **adResyncAllValues**.</span><span class="sxs-lookup"><span data-stu-id="e6702-118">The default value is **adResyncAllValues**.</span></span>

## <a name="remarks"></a><span data-ttu-id="e6702-119">Замечания</span><span class="sxs-lookup"><span data-stu-id="e6702-119">Remarks</span></span>

<span data-ttu-id="e6702-120">**Набор записей**</span><span class="sxs-lookup"><span data-stu-id="e6702-120">**Recordset**</span></span>

<span data-ttu-id="e6702-121">Используйте метод **выполнить повторную синхронизацию** для повторной синхронизации записей в текущего **набора записей** с основной базы данных.</span><span class="sxs-lookup"><span data-stu-id="e6702-121">Use the **Resync** method to resynchronize records in the current **Recordset** with the underlying database.</span></span> <span data-ttu-id="e6702-122">Это полезно, если вы используете статического или только для прямого текущей позиции, но требуется просмотреть все изменения в базе данных.</span><span class="sxs-lookup"><span data-stu-id="e6702-122">This is useful if you are using either a static or forward-only cursor, but you want to see any changes in the underlying database.</span></span>

<span data-ttu-id="e6702-123">Если значение свойства [CursorLocation](cursorlocation-property-ado.md) **adUseClient**, **выполнить повторную синхронизацию** доступна только для объектов **наборов записей** не только для чтения.</span><span class="sxs-lookup"><span data-stu-id="e6702-123">If you set the [CursorLocation](cursorlocation-property-ado.md) property to **adUseClient**, **Resync** is only available for non-read-only **Recordset** objects.</span></span>

<span data-ttu-id="e6702-124">В отличие от метода [повторный запрос](requery-method-ado.md) метода **выполнить повторную синхронизацию** не повторно выполняется команда базового объекта **набора записей** .</span><span class="sxs-lookup"><span data-stu-id="e6702-124">Unlike the [Requery](requery-method-ado.md) method, the **Resync** method does not re-execute the **Recordset** object's underlying command.</span></span> <span data-ttu-id="e6702-125">Новые записи в базе данных будет недоступен.</span><span class="sxs-lookup"><span data-stu-id="e6702-125">New records in the underlying database will not be visible.</span></span>

<span data-ttu-id="e6702-126">Если происходит сбой попытки повторную синхронизацию из-за конфликта с базовыми данными (например, запись была удалена другим пользователем), поставщик возвращает предупреждения семейство [Errors](errors-collection-ado.md) и возникает ошибка времени выполнения.</span><span class="sxs-lookup"><span data-stu-id="e6702-126">If the attempt to resynchronize fails because of a conflict with the underlying data (for example, a record has been deleted by another user), the provider returns warnings to the [Errors](errors-collection-ado.md) collection and a run-time error occurs.</span></span> <span data-ttu-id="e6702-127">Используйте свойство [фильтра](filter-property-ado.md) (**adFilterConflictingRecords**) и свойство [состояние](status-property-ado-recordset.md) для поиска записей с конфликтами.</span><span class="sxs-lookup"><span data-stu-id="e6702-127">Use the [Filter](filter-property-ado.md) property (**adFilterConflictingRecords**) and the [Status](status-property-ado-recordset.md) property to locate records with conflicts.</span></span>

<span data-ttu-id="e6702-128">Если [Уникальной таблицы](unique-table-unique-schema-unique-catalog-properties-dynamic-ado.md) и [Выполнить повторную синхронизацию команду](resync-command-property-dynamic-ado.md) динамический задано и **записей** представляет собой результат выполнения операции СОЕДИНЕНИЯ на несколько таблиц, затем **выполнить повторную синхронизацию** метода будет выполняться команда в **выполнить повторную синхронизацию Команда** свойство только в таблице с именем в свойстве **Уникальной таблицы** .</span><span class="sxs-lookup"><span data-stu-id="e6702-128">If the [Unique Table](unique-table-unique-schema-unique-catalog-properties-dynamic-ado.md) and [Resync Command](resync-command-property-dynamic-ado.md) dynamic properties are set, and the **Recordset** is the result of executing a JOIN operation on multiple tables, then the **Resync** method will execute the command given in the **Resync Command** property only on the table named in the **Unique Table** property.</span></span>

<span data-ttu-id="e6702-129">**Поля**</span><span class="sxs-lookup"><span data-stu-id="e6702-129">**Fields**</span></span>

<span data-ttu-id="e6702-130">Используйте метод **выполнить повторную синхронизацию** для повторной синхронизации значений коллекции **полей** объекта **записи** с базовым источником данных.</span><span class="sxs-lookup"><span data-stu-id="e6702-130">Use the **Resync** method to resynchronize the values of the **Fields** collection of a **Record** object with the underlying data source.</span></span> <span data-ttu-id="e6702-131">Свойство [Count](count-property-ado.md) не влияют этот метод.</span><span class="sxs-lookup"><span data-stu-id="e6702-131">The [Count](count-property-ado.md) property is not affected by this method.</span></span>

<span data-ttu-id="e6702-132">Если *ResyncValues* **adResyncAllValues** (значение по умолчанию), затем синхронизированы [UnderlyingValue](underlyingvalue-property-ado.md), [значение](value-property-ado.md)и [OriginalValue](originalvalue-property-ado.md) свойства [поля](field-object-ado.md) объектов в коллекции.</span><span class="sxs-lookup"><span data-stu-id="e6702-132">If *ResyncValues* is set to **adResyncAllValues** (the default value), then the [UnderlyingValue](underlyingvalue-property-ado.md), [Value](value-property-ado.md), and [OriginalValue](originalvalue-property-ado.md) properties of [Field](field-object-ado.md) objects in the collection are synchronized.</span></span> <span data-ttu-id="e6702-133">Если *ResyncValues* **adResyncUnderlyingValues**, синхронизируется только свойство **UnderlyingValue** .</span><span class="sxs-lookup"><span data-stu-id="e6702-133">If *ResyncValues* is set to **adResyncUnderlyingValues**, only the **UnderlyingValue** property is synchronized.</span></span>

<span data-ttu-id="e6702-134">Значение свойства **состояние** для каждого объекта **поля** во время вызова также влияет на поведение **выполнить повторную синхронизацию**.</span><span class="sxs-lookup"><span data-stu-id="e6702-134">The value of the **Status** property for each **Field** object at the time of the call also affects the behavior of **Resync**.</span></span> <span data-ttu-id="e6702-135">Для **полей** объектов с помощью значения **состояния** **adFieldPendingUnknown** или **adFieldPendingInsert** **выполнить повторную синхронизацию** не оказывает влияния.</span><span class="sxs-lookup"><span data-stu-id="e6702-135">For **Field** objects with **Status** values of **adFieldPendingUnknown** or **adFieldPendingInsert**, **Resync** has no effect.</span></span> <span data-ttu-id="e6702-136">Для значения **состояния** **adFieldPendingChange** или **adFieldPendingDelete** **выполнить повторную синхронизацию** синхронизирует данные значения для поля, по-прежнему поддерживаются в источнике данных.</span><span class="sxs-lookup"><span data-stu-id="e6702-136">For **Status** values of **adFieldPendingChange** or **adFieldPendingDelete**, **Resync** synchronizes data values for fields that still exist at the data source.</span></span>

<span data-ttu-id="e6702-137">**Выполнить повторную синхронизацию** не изменяйте значения **состояния** объектов **полей** , если не возникает ошибка при вызове **выполнить повторную синхронизацию** .</span><span class="sxs-lookup"><span data-stu-id="e6702-137">**Resync** will not modify **Status** values of **Field** objects unless an error occurs when **Resync** is called.</span></span> <span data-ttu-id="e6702-138">Например если поле больше не существует, поставщик возвращает соответствующее значение **состояния** для объекта **поля** , такие как **adFieldDoesNotExist**.</span><span class="sxs-lookup"><span data-stu-id="e6702-138">For example, if the field no longer exists, the provider will return an appropriate **Status** value for the **Field** object, such as **adFieldDoesNotExist**.</span></span> <span data-ttu-id="e6702-139">Возвращаемые значения **состояния** может быть объединен логически внутри значения свойству **состояние** .</span><span class="sxs-lookup"><span data-stu-id="e6702-139">Returned **Status** values may be logically combined within the value of the **Status** property.</span></span>


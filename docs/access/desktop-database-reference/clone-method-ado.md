---
title: Клонирование метод - ActiveX Data Objects (ADO)
TOCTitle: Clone method (ADO)
ms:assetid: ca9b2b76-90bf-9a60-2611-3cb4977d5591
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249984(v=office.15)
ms:contentKeyID: 48547693
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 095191bbfe55f2c38529cb1c260979c48dd2d5f1
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28702966"
---
# <a name="clone-method-ado"></a><span data-ttu-id="634da-102">Метод Clone (ADO)</span><span class="sxs-lookup"><span data-stu-id="634da-102">Clone method (ADO)</span></span>

<span data-ttu-id="634da-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="634da-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="634da-104">Создает объект повторяющихся [записей](recordset-object-ado.md) из существующего объекта **набора записей** .</span><span class="sxs-lookup"><span data-stu-id="634da-104">Creates a duplicate [Recordset](recordset-object-ado.md) object from an existing **Recordset** object.</span></span> <span data-ttu-id="634da-105">При необходимости указывает копию только для чтения.</span><span class="sxs-lookup"><span data-stu-id="634da-105">Optionally, specifies that the clone be read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="634da-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="634da-106">Syntax</span></span>

<span data-ttu-id="634da-107">**Установка** *rstDuplicate*  =  *rstOriginal*. Копия (*LockType для*)</span><span class="sxs-lookup"><span data-stu-id="634da-107">**Set** *rstDuplicate* = *rstOriginal*.Clone (*LockType*)</span></span>

## <a name="return-value"></a><span data-ttu-id="634da-108">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="634da-108">Return value</span></span>

<span data-ttu-id="634da-109">Возвращает ссылку на объект **набора записей** .</span><span class="sxs-lookup"><span data-stu-id="634da-109">Returns a **Recordset** object reference.</span></span>

## <a name="parameters"></a><span data-ttu-id="634da-110">Parameters</span><span class="sxs-lookup"><span data-stu-id="634da-110">Parameters</span></span>

|<span data-ttu-id="634da-111">Параметр</span><span class="sxs-lookup"><span data-stu-id="634da-111">Parameter</span></span>|<span data-ttu-id="634da-112">Описание</span><span class="sxs-lookup"><span data-stu-id="634da-112">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="634da-113">*rstDuplicate*</span><span class="sxs-lookup"><span data-stu-id="634da-113">*rstDuplicate*</span></span> |<span data-ttu-id="634da-114">Объектная переменная, которая определяет повторяющихся **записей** объект будет создан.</span><span class="sxs-lookup"><span data-stu-id="634da-114">An object variable that identifies the duplicate **Recordset** object to be created.</span></span>|
|<span data-ttu-id="634da-115">*rstOriginal*</span><span class="sxs-lookup"><span data-stu-id="634da-115">*rstOriginal*</span></span> |<span data-ttu-id="634da-116">Объектная переменная, которая определяет объект **набора записей** дублирование.</span><span class="sxs-lookup"><span data-stu-id="634da-116">An object variable that identifies the **Recordset** object to be duplicated.</span></span>|
|<span data-ttu-id="634da-117">*LockType для*</span><span class="sxs-lookup"><span data-stu-id="634da-117">*LockType*</span></span> |<span data-ttu-id="634da-118">Необязательно.</span><span class="sxs-lookup"><span data-stu-id="634da-118">Optional.</span></span> <span data-ttu-id="634da-119">[LockTypeEnum](locktypeenum.md) значение, задающее тип блокировки исходного **набора записей**или только для чтения **набора записей**.</span><span class="sxs-lookup"><span data-stu-id="634da-119">A [LockTypeEnum](locktypeenum.md) value that specifies either the lock type of the original **Recordset**, or a read-only **Recordset**.</span></span> <span data-ttu-id="634da-120">Допустимые значения: **adLockUnspecified** или **adLockReadOnly**.</span><span class="sxs-lookup"><span data-stu-id="634da-120">Valid values are **adLockUnspecified** or **adLockReadOnly**.</span></span>|

## <a name="remarks"></a><span data-ttu-id="634da-121">Замечания</span><span class="sxs-lookup"><span data-stu-id="634da-121">Remarks</span></span>

<span data-ttu-id="634da-122">Используйте метод **клонированной** для создания нескольких дубликатов объектов **набора записей** , особенно в том случае, если вы хотите поддерживать более одного текущей записи в данного набора записей.</span><span class="sxs-lookup"><span data-stu-id="634da-122">Use the **Clone** method to create multiple, duplicate **Recordset** objects, particularly if you want to maintain more than one current record in a given set of records.</span></span> <span data-ttu-id="634da-123">С помощью метода **клонированной** эффективнее, чем создания и открытия нового объекта **набора записей** с тем же определением, что и исходный.</span><span class="sxs-lookup"><span data-stu-id="634da-123">Using the **Clone** method is more efficient than creating and opening a new **Recordset** object with the same definition as the original.</span></span>

<span data-ttu-id="634da-124">Свойства [фильтра](filter-property-ado.md) из исходного **набора записей**при их наличии, не применяются к копии.</span><span class="sxs-lookup"><span data-stu-id="634da-124">The [Filter](filter-property-ado.md) property of the original **Recordset**, if any, will not be applied to the clone.</span></span> <span data-ttu-id="634da-125">Свойства **фильтра** нового **набора записей** для фильтрации результатов.</span><span class="sxs-lookup"><span data-stu-id="634da-125">Set the **Filter** property of the new **Recordset** in order to filter the results.</span></span> <span data-ttu-id="634da-126">Чтобы скопировать все существующие значения **фильтра** проще всего напрямую, назначьте его следующим образом:</span><span class="sxs-lookup"><span data-stu-id="634da-126">The simplest way to copy any existing **Filter** value is to assign it directly, like this:</span></span>

<span data-ttu-id="634da-127">Текущая запись только что созданный клонированной присвоено значение первой записи.</span><span class="sxs-lookup"><span data-stu-id="634da-127">The current record of a newly created clone is set to the first record.</span></span>

<span data-ttu-id="634da-128">Изменения, внесенные на **один Recordset** видны во всех его копирует вне зависимости от типа курсора.</span><span class="sxs-lookup"><span data-stu-id="634da-128">Changes you make to one **Recordset** object are visible in all of its clones regardless of cursor type.</span></span> <span data-ttu-id="634da-129">Тем не менее после выполнения [запроса](requery-method-ado.md) на исходный **набора записей**копирует больше не синхронизируются с исходным.</span><span class="sxs-lookup"><span data-stu-id="634da-129">However, after you execute [Requery](requery-method-ado.md) on the original **Recordset**, the clones will no longer be synchronized to the original.</span></span>

<span data-ttu-id="634da-130">Закрытие исходного **набора записей** не закрывайте его копии, а также закрывая копии закрыть исходной или любых других копий.</span><span class="sxs-lookup"><span data-stu-id="634da-130">Closing the original **Recordset** does not close its copies, nor does closing a copy close the original or any of the other copies.</span></span>

<span data-ttu-id="634da-131">Можно только клонирование объекта **набора записей** , который поддерживает закладки.</span><span class="sxs-lookup"><span data-stu-id="634da-131">You can only clone a **Recordset** object that supports bookmarks.</span></span> <span data-ttu-id="634da-132">Значения закладки являются взаимозаменяемыми; Таким образом закладка ссылку из одного объекта **набора записей** относится к одной и той же записи в любом из его копирует.</span><span class="sxs-lookup"><span data-stu-id="634da-132">Bookmark values are interchangeable; that is, a bookmark reference from one **Recordset** object refers to the same record in any of its clones.</span></span>

<span data-ttu-id="634da-133">Некоторые события **набора записей** , которые запускаются также будет срабатывать в копирует все **набора записей** .</span><span class="sxs-lookup"><span data-stu-id="634da-133">Some **Recordset** events that are triggered will also fire in all **Recordset** clones.</span></span> <span data-ttu-id="634da-134">Тем не менее так как текущей записи может отличаться от клонирования **наборов записей**, события могут быть допустимый для копии.</span><span class="sxs-lookup"><span data-stu-id="634da-134">However, because the current record can differ between cloned **Recordsets**, the events may not be valid for the clone.</span></span>

<span data-ttu-id="634da-135">Например, при изменении значения поля [WillChangeField](willchangefield-and-fieldchangecomplete-events-ado.md) событие происходит в измененных **записей** и копирует все.</span><span class="sxs-lookup"><span data-stu-id="634da-135">For example, if you change a value of a field, a [WillChangeField](willchangefield-and-fieldchangecomplete-events-ado.md) event will occur in the changed **Recordset** and in all clones.</span></span> <span data-ttu-id="634da-136">Параметр *поля* событие **WillChangeField** клонирования **записей** (где не изменения) просто будет ссылаться на поля текущей записи копии, может быть другой записи превышает текущий запись где произошло изменение исходного **набора записей** .</span><span class="sxs-lookup"><span data-stu-id="634da-136">The *Fields* parameter of the **WillChangeField** event of a cloned **Recordset** (where the change was not made) will simply refer to the fields of the current record of the clone, which may be a different record than the current record of the original **Recordset** where the change occurred.</span></span>

<span data-ttu-id="634da-137">В следующей таблице предоставляются полный список всех **записей** событий и указывает, являются ли они действительный и включаемая для любого копирует набора записей, созданных с помощью метода **клонирования** .</span><span class="sxs-lookup"><span data-stu-id="634da-137">The following table provided a full listing of all **Recordset** events and indicates whether they are valid and triggered for any recordset clones generated using the **Clone** method.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="634da-138">Событие</span><span class="sxs-lookup"><span data-stu-id="634da-138">Event</span></span></p></th>
<th><p><span data-ttu-id="634da-139">Запущено копирует?</span><span class="sxs-lookup"><span data-stu-id="634da-139">Triggered in clones?</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="634da-140"><a href="endofrecordset-event-ado.md">EndOfRecordset</a></span><span class="sxs-lookup"><span data-stu-id="634da-140"><a href="endofrecordset-event-ado.md">EndOfRecordset</a></span></span></p></td>
<td><p><span data-ttu-id="634da-141">Нет</span><span class="sxs-lookup"><span data-stu-id="634da-141">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="634da-142"><a href="fetchcomplete-event-ado.md">FetchComplete</a></span><span class="sxs-lookup"><span data-stu-id="634da-142"><a href="fetchcomplete-event-ado.md">FetchComplete</a></span></span></p></td>
<td><p><span data-ttu-id="634da-143">Нет</span><span class="sxs-lookup"><span data-stu-id="634da-143">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="634da-144"><a href="fetchprogress-event-ado.md">FetchProgress</a></span><span class="sxs-lookup"><span data-stu-id="634da-144"><a href="fetchprogress-event-ado.md">FetchProgress</a></span></span></p></td>
<td><p><span data-ttu-id="634da-145">Нет</span><span class="sxs-lookup"><span data-stu-id="634da-145">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="634da-146"><a href="willchangefield-and-fieldchangecomplete-events-ado.md">FieldChangeComplete</a></span><span class="sxs-lookup"><span data-stu-id="634da-146"><a href="willchangefield-and-fieldchangecomplete-events-ado.md">FieldChangeComplete</a></span></span></p></td>
<td><p><span data-ttu-id="634da-147">Да</span><span class="sxs-lookup"><span data-stu-id="634da-147">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="634da-148"><a href="willmove-and-movecomplete-events-ado.md">MoveComplete</a></span><span class="sxs-lookup"><span data-stu-id="634da-148"><a href="willmove-and-movecomplete-events-ado.md">MoveComplete</a></span></span></p></td>
<td><p><span data-ttu-id="634da-149">Нет</span><span class="sxs-lookup"><span data-stu-id="634da-149">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="634da-150"><a href="willchangerecord-and-recordchangecomplete-events-ado.md">RecordChangeComplete</a></span><span class="sxs-lookup"><span data-stu-id="634da-150"><a href="willchangerecord-and-recordchangecomplete-events-ado.md">RecordChangeComplete</a></span></span></p></td>
<td><p><span data-ttu-id="634da-151">Да</span><span class="sxs-lookup"><span data-stu-id="634da-151">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="634da-152"><a href="willchangerecordset-and-recordsetchangecomplete-events-ado.md">RecordsetChangeComplete</a></span><span class="sxs-lookup"><span data-stu-id="634da-152"><a href="willchangerecordset-and-recordsetchangecomplete-events-ado.md">RecordsetChangeComplete</a></span></span></p></td>
<td><p><span data-ttu-id="634da-153">Нет</span><span class="sxs-lookup"><span data-stu-id="634da-153">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="634da-154"><a href="willchangefield-and-fieldchangecomplete-events-ado.md">WillChangeField</a></span><span class="sxs-lookup"><span data-stu-id="634da-154"><a href="willchangefield-and-fieldchangecomplete-events-ado.md">WillChangeField</a></span></span></p></td>
<td><p><span data-ttu-id="634da-155">Да</span><span class="sxs-lookup"><span data-stu-id="634da-155">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="634da-156"><a href="willchangerecord-and-recordchangecomplete-events-ado.md">WillChangeRecord</a></span><span class="sxs-lookup"><span data-stu-id="634da-156"><a href="willchangerecord-and-recordchangecomplete-events-ado.md">WillChangeRecord</a></span></span></p></td>
<td><p><span data-ttu-id="634da-157">Да</span><span class="sxs-lookup"><span data-stu-id="634da-157">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="634da-158"><a href="willchangerecordset-and-recordsetchangecomplete-events-ado.md">WillChangeRecordset</a></span><span class="sxs-lookup"><span data-stu-id="634da-158"><a href="willchangerecordset-and-recordsetchangecomplete-events-ado.md">WillChangeRecordset</a></span></span></p></td>
<td><p><span data-ttu-id="634da-159">Нет</span><span class="sxs-lookup"><span data-stu-id="634da-159">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="634da-160"><a href="willmove-and-movecomplete-events-ado.md">WillMove</a></span><span class="sxs-lookup"><span data-stu-id="634da-160"><a href="willmove-and-movecomplete-events-ado.md">WillMove</a></span></span></p></td>
<td><p><span data-ttu-id="634da-161">Нет</span><span class="sxs-lookup"><span data-stu-id="634da-161">No</span></span></p></td>
</tr>
</tbody>
</table>


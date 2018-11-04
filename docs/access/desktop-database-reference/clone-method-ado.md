---
title: Клонирование метод - ActiveX Data Objects (ADO)
TOCTitle: Clone method (ADO)
ms:assetid: ca9b2b76-90bf-9a60-2611-3cb4977d5591
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249984(v=office.15)
ms:contentKeyID: 48547693
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: c72902c4ed1d1d2657bfa6e2b4c5f84d76dfefa3
ms.sourcegitcommit: 980a96cf444882d3d34cecb5faac8f8a7b7c4b57
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/03/2018
ms.locfileid: "25950260"
---
# <a name="clone-method-ado"></a><span data-ttu-id="b74a3-102">Метод Clone (ADO)</span><span class="sxs-lookup"><span data-stu-id="b74a3-102">Clone method (ADO)</span></span>

<span data-ttu-id="b74a3-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="b74a3-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="b74a3-104">Создает объект повторяющихся [записей](recordset-object-ado.md) из существующего объекта **набора записей** .</span><span class="sxs-lookup"><span data-stu-id="b74a3-104">Creates a duplicate [Recordset](recordset-object-ado.md) object from an existing **Recordset** object.</span></span> <span data-ttu-id="b74a3-105">При необходимости указывает копию только для чтения.</span><span class="sxs-lookup"><span data-stu-id="b74a3-105">Optionally, specifies that the clone be read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="b74a3-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b74a3-106">Syntax</span></span>

<span data-ttu-id="b74a3-107">**Установка** *rstDuplicate*  =  *rstOriginal*. Копия (*LockType для*)</span><span class="sxs-lookup"><span data-stu-id="b74a3-107">**Set** *rstDuplicate* = *rstOriginal*.Clone (*LockType*)</span></span>

## <a name="return-value"></a><span data-ttu-id="b74a3-108">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="b74a3-108">Return value</span></span>

<span data-ttu-id="b74a3-109">Возвращает ссылку на объект **набора записей** .</span><span class="sxs-lookup"><span data-stu-id="b74a3-109">Returns a **Recordset** object reference.</span></span>

## <a name="parameters"></a><span data-ttu-id="b74a3-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="b74a3-110">Parameters</span></span>

|<span data-ttu-id="b74a3-111">Параметр</span><span class="sxs-lookup"><span data-stu-id="b74a3-111">Parameter</span></span>|<span data-ttu-id="b74a3-112">Описание</span><span class="sxs-lookup"><span data-stu-id="b74a3-112">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="b74a3-113">*rstDuplicate*</span><span class="sxs-lookup"><span data-stu-id="b74a3-113">*rstDuplicate*</span></span> |<span data-ttu-id="b74a3-114">Объектная переменная, которая определяет повторяющихся **записей** объект будет создан.</span><span class="sxs-lookup"><span data-stu-id="b74a3-114">An object variable that identifies the duplicate **Recordset** object to be created.</span></span>|
|<span data-ttu-id="b74a3-115">*rstOriginal*</span><span class="sxs-lookup"><span data-stu-id="b74a3-115">*rstOriginal*</span></span> |<span data-ttu-id="b74a3-116">Объектная переменная, которая определяет объект **набора записей** дублирование.</span><span class="sxs-lookup"><span data-stu-id="b74a3-116">An object variable that identifies the **Recordset** object to be duplicated.</span></span>|
|<span data-ttu-id="b74a3-117">*LockType для*</span><span class="sxs-lookup"><span data-stu-id="b74a3-117">*LockType*</span></span> |<span data-ttu-id="b74a3-118">Необязательно указывать.</span><span class="sxs-lookup"><span data-stu-id="b74a3-118">Optional.</span></span> <span data-ttu-id="b74a3-119">[LockTypeEnum](locktypeenum.md) значение, задающее тип блокировки исходного **набора записей**или только для чтения **набора записей**.</span><span class="sxs-lookup"><span data-stu-id="b74a3-119">A [LockTypeEnum](locktypeenum.md) value that specifies either the lock type of the original **Recordset**, or a read-only **Recordset**.</span></span> <span data-ttu-id="b74a3-120">Допустимые значения: **adLockUnspecified** или **adLockReadOnly**.</span><span class="sxs-lookup"><span data-stu-id="b74a3-120">Valid values are **adLockUnspecified** or **adLockReadOnly**.</span></span>|

## <a name="remarks"></a><span data-ttu-id="b74a3-121">Примечания</span><span class="sxs-lookup"><span data-stu-id="b74a3-121">Remarks</span></span>

<span data-ttu-id="b74a3-122">Используйте метод **клонированной** для создания нескольких дубликатов объектов **набора записей** , особенно в том случае, если вы хотите поддерживать более одного текущей записи в данного набора записей.</span><span class="sxs-lookup"><span data-stu-id="b74a3-122">Use the **Clone** method to create multiple, duplicate **Recordset** objects, particularly if you want to maintain more than one current record in a given set of records.</span></span> <span data-ttu-id="b74a3-123">С помощью метода **клонированной** эффективнее, чем создания и открытия нового объекта **набора записей** с тем же определением, что и исходный.</span><span class="sxs-lookup"><span data-stu-id="b74a3-123">Using the **Clone** method is more efficient than creating and opening a new **Recordset** object with the same definition as the original.</span></span>

<span data-ttu-id="b74a3-124">Свойства [фильтра](filter-property-ado.md) из исходного **набора записей**при их наличии, не применяются к копии.</span><span class="sxs-lookup"><span data-stu-id="b74a3-124">The [Filter](filter-property-ado.md) property of the original **Recordset**, if any, will not be applied to the clone.</span></span> <span data-ttu-id="b74a3-125">Свойства **фильтра** нового **набора записей** для фильтрации результатов.</span><span class="sxs-lookup"><span data-stu-id="b74a3-125">Set the **Filter** property of the new **Recordset** in order to filter the results.</span></span> <span data-ttu-id="b74a3-126">Чтобы скопировать все существующие значения **фильтра** проще всего напрямую, назначьте его следующим образом:</span><span class="sxs-lookup"><span data-stu-id="b74a3-126">The simplest way to copy any existing **Filter** value is to assign it directly, like this:</span></span>

<span data-ttu-id="b74a3-127">Текущая запись только что созданный клонированной присвоено значение первой записи.</span><span class="sxs-lookup"><span data-stu-id="b74a3-127">The current record of a newly created clone is set to the first record.</span></span>

<span data-ttu-id="b74a3-128">Изменения, внесенные на **один Recordset** видны во всех его копирует вне зависимости от типа курсора.</span><span class="sxs-lookup"><span data-stu-id="b74a3-128">Changes you make to one **Recordset** object are visible in all of its clones regardless of cursor type.</span></span> <span data-ttu-id="b74a3-129">Тем не менее после выполнения [запроса](requery-method-ado.md) на исходный **набора записей**копирует больше не синхронизируются с исходным.</span><span class="sxs-lookup"><span data-stu-id="b74a3-129">However, after you execute [Requery](requery-method-ado.md) on the original **Recordset**, the clones will no longer be synchronized to the original.</span></span>

<span data-ttu-id="b74a3-130">Закрытие исходного **набора записей** не закрывайте его копии, а также закрывая копии закрыть исходной или любых других копий.</span><span class="sxs-lookup"><span data-stu-id="b74a3-130">Closing the original **Recordset** does not close its copies, nor does closing a copy close the original or any of the other copies.</span></span>

<span data-ttu-id="b74a3-131">Можно только клонирование объекта **набора записей** , который поддерживает закладки.</span><span class="sxs-lookup"><span data-stu-id="b74a3-131">You can only clone a **Recordset** object that supports bookmarks.</span></span> <span data-ttu-id="b74a3-132">Значения закладки являются взаимозаменяемыми; Таким образом закладка ссылку из одного объекта **набора записей** относится к одной и той же записи в любом из его копирует.</span><span class="sxs-lookup"><span data-stu-id="b74a3-132">Bookmark values are interchangeable; that is, a bookmark reference from one **Recordset** object refers to the same record in any of its clones.</span></span>

<span data-ttu-id="b74a3-133">Некоторые события **набора записей** , которые запускаются также будет срабатывать в копирует все **набора записей** .</span><span class="sxs-lookup"><span data-stu-id="b74a3-133">Some **Recordset** events that are triggered will also fire in all **Recordset** clones.</span></span> <span data-ttu-id="b74a3-134">Тем не менее так как текущей записи может отличаться от клонирования **наборов записей**, события могут быть допустимый для копии.</span><span class="sxs-lookup"><span data-stu-id="b74a3-134">However, because the current record can differ between cloned **Recordsets**, the events may not be valid for the clone.</span></span>

<span data-ttu-id="b74a3-135">Например, при изменении значения поля [WillChangeField](willchangefield-and-fieldchangecomplete-events-ado.md) событие происходит в измененных **записей** и копирует все.</span><span class="sxs-lookup"><span data-stu-id="b74a3-135">For example, if you change a value of a field, a [WillChangeField](willchangefield-and-fieldchangecomplete-events-ado.md) event will occur in the changed **Recordset** and in all clones.</span></span> <span data-ttu-id="b74a3-136">Параметр *поля* событие **WillChangeField** клонирования **записей** (где не изменения) просто будет ссылаться на поля текущей записи копии, может быть другой записи превышает текущий запись где произошло изменение исходного **набора записей** .</span><span class="sxs-lookup"><span data-stu-id="b74a3-136">The *Fields* parameter of the **WillChangeField** event of a cloned **Recordset** (where the change was not made) will simply refer to the fields of the current record of the clone, which may be a different record than the current record of the original **Recordset** where the change occurred.</span></span>

<span data-ttu-id="b74a3-137">В следующей таблице предоставляются полный список всех **записей** событий и указывает, являются ли они действительный и включаемая для любого копирует набора записей, созданных с помощью метода **клонирования** .</span><span class="sxs-lookup"><span data-stu-id="b74a3-137">The following table provided a full listing of all **Recordset** events and indicates whether they are valid and triggered for any recordset clones generated using the **Clone** method.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="b74a3-138">Событие</span><span class="sxs-lookup"><span data-stu-id="b74a3-138">Event</span></span></p></th>
<th><p><span data-ttu-id="b74a3-139">Запущено копирует?</span><span class="sxs-lookup"><span data-stu-id="b74a3-139">Triggered in clones?</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b74a3-140"><a href="endofrecordset-event-ado.md">EndOfRecordset</a></span><span class="sxs-lookup"><span data-stu-id="b74a3-140"><a href="endofrecordset-event-ado.md">EndOfRecordset</a></span></span></p></td>
<td><p><span data-ttu-id="b74a3-141">Нет</span><span class="sxs-lookup"><span data-stu-id="b74a3-141">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b74a3-142"><a href="fetchcomplete-event-ado.md">FetchComplete</a></span><span class="sxs-lookup"><span data-stu-id="b74a3-142"><a href="fetchcomplete-event-ado.md">FetchComplete</a></span></span></p></td>
<td><p><span data-ttu-id="b74a3-143">Нет</span><span class="sxs-lookup"><span data-stu-id="b74a3-143">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b74a3-144"><a href="fetchprogress-event-ado.md">FetchProgress</a></span><span class="sxs-lookup"><span data-stu-id="b74a3-144"><a href="fetchprogress-event-ado.md">FetchProgress</a></span></span></p></td>
<td><p><span data-ttu-id="b74a3-145">Нет</span><span class="sxs-lookup"><span data-stu-id="b74a3-145">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b74a3-146"><a href="willchangefield-and-fieldchangecomplete-events-ado.md">FieldChangeComplete</a></span><span class="sxs-lookup"><span data-stu-id="b74a3-146"><a href="willchangefield-and-fieldchangecomplete-events-ado.md">FieldChangeComplete</a></span></span></p></td>
<td><p><span data-ttu-id="b74a3-147">Да</span><span class="sxs-lookup"><span data-stu-id="b74a3-147">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b74a3-148"><a href="willmove-and-movecomplete-events-ado.md">MoveComplete</a></span><span class="sxs-lookup"><span data-stu-id="b74a3-148"><a href="willmove-and-movecomplete-events-ado.md">MoveComplete</a></span></span></p></td>
<td><p><span data-ttu-id="b74a3-149">Нет</span><span class="sxs-lookup"><span data-stu-id="b74a3-149">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b74a3-150"><a href="willchangerecord-and-recordchangecomplete-events-ado.md">RecordChangeComplete</a></span><span class="sxs-lookup"><span data-stu-id="b74a3-150"><a href="willchangerecord-and-recordchangecomplete-events-ado.md">RecordChangeComplete</a></span></span></p></td>
<td><p><span data-ttu-id="b74a3-151">Да</span><span class="sxs-lookup"><span data-stu-id="b74a3-151">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b74a3-152"><a href="willchangerecordset-and-recordsetchangecomplete-events-ado.md">RecordsetChangeComplete</a></span><span class="sxs-lookup"><span data-stu-id="b74a3-152"><a href="willchangerecordset-and-recordsetchangecomplete-events-ado.md">RecordsetChangeComplete</a></span></span></p></td>
<td><p><span data-ttu-id="b74a3-153">Нет</span><span class="sxs-lookup"><span data-stu-id="b74a3-153">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b74a3-154"><a href="willchangefield-and-fieldchangecomplete-events-ado.md">WillChangeField</a></span><span class="sxs-lookup"><span data-stu-id="b74a3-154"><a href="willchangefield-and-fieldchangecomplete-events-ado.md">WillChangeField</a></span></span></p></td>
<td><p><span data-ttu-id="b74a3-155">Да</span><span class="sxs-lookup"><span data-stu-id="b74a3-155">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b74a3-156"><a href="willchangerecord-and-recordchangecomplete-events-ado.md">WillChangeRecord</a></span><span class="sxs-lookup"><span data-stu-id="b74a3-156"><a href="willchangerecord-and-recordchangecomplete-events-ado.md">WillChangeRecord</a></span></span></p></td>
<td><p><span data-ttu-id="b74a3-157">Да</span><span class="sxs-lookup"><span data-stu-id="b74a3-157">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b74a3-158"><a href="willchangerecordset-and-recordsetchangecomplete-events-ado.md">WillChangeRecordset</a></span><span class="sxs-lookup"><span data-stu-id="b74a3-158"><a href="willchangerecordset-and-recordsetchangecomplete-events-ado.md">WillChangeRecordset</a></span></span></p></td>
<td><p><span data-ttu-id="b74a3-159">Нет</span><span class="sxs-lookup"><span data-stu-id="b74a3-159">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b74a3-160"><a href="willmove-and-movecomplete-events-ado.md">WillMove</a></span><span class="sxs-lookup"><span data-stu-id="b74a3-160"><a href="willmove-and-movecomplete-events-ado.md">WillMove</a></span></span></p></td>
<td><p><span data-ttu-id="b74a3-161">Нет</span><span class="sxs-lookup"><span data-stu-id="b74a3-161">No</span></span></p></td>
</tr>
</tbody>
</table>


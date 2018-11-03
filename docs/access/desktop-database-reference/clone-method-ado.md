---
title: Клонирование метод - ActiveX Data Objects (ADO)
TOCTitle: Clone method (ADO)
ms:assetid: ca9b2b76-90bf-9a60-2611-3cb4977d5591
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249984(v=office.15)
ms:contentKeyID: 48547693
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 857a007d1b3bfe2665eea1284bc41cc9c67ccd46
ms.sourcegitcommit: 558d09fad81f8d80b5ad0edd21934fc09c098f2c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/03/2018
ms.locfileid: "25944440"
---
# <a name="clone-method-ado"></a><span data-ttu-id="50008-102">Метод Clone (ADO)</span><span class="sxs-lookup"><span data-stu-id="50008-102">Clone method (ADO)</span></span>


<span data-ttu-id="50008-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="50008-103">**Applies to**: Access 2013, Office 2013</span></span>



<span data-ttu-id="50008-104">Создает объект повторяющихся [записей](recordset-object-ado.md) из существующего объекта **набора записей** .</span><span class="sxs-lookup"><span data-stu-id="50008-104">Creates a duplicate [Recordset](recordset-object-ado.md) object from an existing **Recordset** object.</span></span> <span data-ttu-id="50008-105">При необходимости указывает копию только для чтения.</span><span class="sxs-lookup"><span data-stu-id="50008-105">Optionally, specifies that the clone be read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="50008-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="50008-106">Syntax</span></span>

<span data-ttu-id="50008-107">**Установка** *rstDuplicate*  =  *rstOriginal*. Копия (*LockType для*)</span><span class="sxs-lookup"><span data-stu-id="50008-107">**Set** *rstDuplicate* = *rstOriginal*.Clone (*LockType*)</span></span>

## <a name="return-value"></a><span data-ttu-id="50008-108">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="50008-108">Return value</span></span>

<span data-ttu-id="50008-109">Возвращает ссылку на объект **набора записей** .</span><span class="sxs-lookup"><span data-stu-id="50008-109">Returns a **Recordset** object reference.</span></span>

## <a name="parameters"></a><span data-ttu-id="50008-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="50008-110">Parameters</span></span>

- <span data-ttu-id="50008-111">*rstDuplicate*</span><span class="sxs-lookup"><span data-stu-id="50008-111">*rstDuplicate*</span></span>

  - <span data-ttu-id="50008-112">Объектная переменная, которая определяет повторяющихся **записей** объект будет создан.</span><span class="sxs-lookup"><span data-stu-id="50008-112">An object variable that identifies the duplicate **Recordset** object to be created.</span></span>

- <span data-ttu-id="50008-113">*rstOriginal*</span><span class="sxs-lookup"><span data-stu-id="50008-113">*rstOriginal*</span></span>

  - <span data-ttu-id="50008-114">Объектная переменная, которая определяет объект **набора записей** дублирование.</span><span class="sxs-lookup"><span data-stu-id="50008-114">An object variable that identifies the **Recordset** object to be duplicated.</span></span>

- <span data-ttu-id="50008-115">*LockType для*</span><span class="sxs-lookup"><span data-stu-id="50008-115">*LockType*</span></span>

  - <span data-ttu-id="50008-116">Необязательно указывать.</span><span class="sxs-lookup"><span data-stu-id="50008-116">Optional.</span></span> <span data-ttu-id="50008-117">[LockTypeEnum](locktypeenum.md) значение, задающее тип блокировки исходного **набора записей**или только для чтения **набора записей**.</span><span class="sxs-lookup"><span data-stu-id="50008-117">A [LockTypeEnum](locktypeenum.md) value that specifies either the lock type of the original **Recordset**, or a read-only **Recordset**.</span></span> <span data-ttu-id="50008-118">Допустимые значения: **adLockUnspecified** или **adLockReadOnly**.</span><span class="sxs-lookup"><span data-stu-id="50008-118">Valid values are **adLockUnspecified** or **adLockReadOnly**.</span></span>

## <a name="remarks"></a><span data-ttu-id="50008-119">Примечания</span><span class="sxs-lookup"><span data-stu-id="50008-119">Remarks</span></span>

<span data-ttu-id="50008-120">Используйте метод **клонированной** для создания нескольких дубликатов объектов **набора записей** , особенно в том случае, если вы хотите поддерживать более одного текущей записи в данного набора записей.</span><span class="sxs-lookup"><span data-stu-id="50008-120">Use the **Clone** method to create multiple, duplicate **Recordset** objects, particularly if you want to maintain more than one current record in a given set of records.</span></span> <span data-ttu-id="50008-121">С помощью метода **клонированной** эффективнее, чем создания и открытия нового объекта **набора записей** с тем же определением, что и исходный.</span><span class="sxs-lookup"><span data-stu-id="50008-121">Using the **Clone** method is more efficient than creating and opening a new **Recordset** object with the same definition as the original.</span></span>

<span data-ttu-id="50008-122">Свойства [фильтра](filter-property-ado.md) из исходного **набора записей**при их наличии, не применяются к копии.</span><span class="sxs-lookup"><span data-stu-id="50008-122">The [Filter](filter-property-ado.md) property of the original **Recordset**, if any, will not be applied to the clone.</span></span> <span data-ttu-id="50008-123">Свойства **фильтра** нового **набора записей** для фильтрации результатов.</span><span class="sxs-lookup"><span data-stu-id="50008-123">Set the **Filter** property of the new **Recordset** in order to filter the results.</span></span> <span data-ttu-id="50008-124">Чтобы скопировать все существующие значения **фильтра** проще всего напрямую, назначьте его следующим образом:</span><span class="sxs-lookup"><span data-stu-id="50008-124">The simplest way to copy any existing **Filter** value is to assign it directly, like this:</span></span>

<span data-ttu-id="50008-125">Текущая запись только что созданный клонированной присвоено значение первой записи.</span><span class="sxs-lookup"><span data-stu-id="50008-125">The current record of a newly created clone is set to the first record.</span></span>

<span data-ttu-id="50008-126">Изменения, внесенные на **один Recordset** видны во всех его копирует вне зависимости от типа курсора.</span><span class="sxs-lookup"><span data-stu-id="50008-126">Changes you make to one **Recordset** object are visible in all of its clones regardless of cursor type.</span></span> <span data-ttu-id="50008-127">Тем не менее после выполнения [запроса](requery-method-ado.md) на исходный **набора записей**копирует больше не синхронизируются с исходным.</span><span class="sxs-lookup"><span data-stu-id="50008-127">However, after you execute [Requery](requery-method-ado.md) on the original **Recordset**, the clones will no longer be synchronized to the original.</span></span>

<span data-ttu-id="50008-128">Закрытие исходного **набора записей** не закрывайте его копии, а также закрывая копии закрыть исходной или любых других копий.</span><span class="sxs-lookup"><span data-stu-id="50008-128">Closing the original **Recordset** does not close its copies, nor does closing a copy close the original or any of the other copies.</span></span>

<span data-ttu-id="50008-129">Можно только клонирование объекта **набора записей** , который поддерживает закладки.</span><span class="sxs-lookup"><span data-stu-id="50008-129">You can only clone a **Recordset** object that supports bookmarks.</span></span> <span data-ttu-id="50008-130">Значения закладки являются взаимозаменяемыми; Таким образом закладка ссылку из одного объекта **набора записей** относится к одной и той же записи в любом из его копирует.</span><span class="sxs-lookup"><span data-stu-id="50008-130">Bookmark values are interchangeable; that is, a bookmark reference from one **Recordset** object refers to the same record in any of its clones.</span></span>

<span data-ttu-id="50008-131">Некоторые события **набора записей** , которые запускаются также будет срабатывать в копирует все **набора записей** .</span><span class="sxs-lookup"><span data-stu-id="50008-131">Some **Recordset** events that are triggered will also fire in all **Recordset** clones.</span></span> <span data-ttu-id="50008-132">Тем не менее так как текущей записи может отличаться от клонирования **наборов записей**, события могут быть допустимый для копии.</span><span class="sxs-lookup"><span data-stu-id="50008-132">However, because the current record can differ between cloned **Recordsets**, the events may not be valid for the clone.</span></span>

<span data-ttu-id="50008-133">Например, при изменении значения поля [WillChangeField](willchangefield-and-fieldchangecomplete-events-ado.md) событие происходит в измененных **записей** и копирует все.</span><span class="sxs-lookup"><span data-stu-id="50008-133">For example, if you change a value of a field, a [WillChangeField](willchangefield-and-fieldchangecomplete-events-ado.md) event will occur in the changed **Recordset** and in all clones.</span></span> <span data-ttu-id="50008-134">Параметр *поля* событие **WillChangeField** клонирования **записей** (где не изменения) просто будет ссылаться на поля текущей записи копии, может быть другой записи превышает текущий запись где произошло изменение исходного **набора записей** .</span><span class="sxs-lookup"><span data-stu-id="50008-134">The *Fields* parameter of the **WillChangeField** event of a cloned **Recordset** (where the change was not made) will simply refer to the fields of the current record of the clone, which may be a different record than the current record of the original **Recordset** where the change occurred.</span></span>

<span data-ttu-id="50008-135">В следующей таблице предоставляются полный список всех **записей** событий и указывает, являются ли они действительный и включаемая для любого копирует набора записей, созданных с помощью метода **клонирования** .</span><span class="sxs-lookup"><span data-stu-id="50008-135">The following table provided a full listing of all **Recordset** events and indicates whether they are valid and triggered for any recordset clones generated using the **Clone** method.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="50008-136">Событие</span><span class="sxs-lookup"><span data-stu-id="50008-136">Event</span></span></p></th>
<th><p><span data-ttu-id="50008-137">Запущено копирует?</span><span class="sxs-lookup"><span data-stu-id="50008-137">Triggered in clones?</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="50008-138"><a href="endofrecordset-event-ado.md">EndOfRecordset</a></span><span class="sxs-lookup"><span data-stu-id="50008-138"><a href="endofrecordset-event-ado.md">EndOfRecordset</a></span></span></p></td>
<td><p><span data-ttu-id="50008-139">Нет</span><span class="sxs-lookup"><span data-stu-id="50008-139">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="50008-140"><a href="fetchcomplete-event-ado.md">FetchComplete</a></span><span class="sxs-lookup"><span data-stu-id="50008-140"><a href="fetchcomplete-event-ado.md">FetchComplete</a></span></span></p></td>
<td><p><span data-ttu-id="50008-141">Нет</span><span class="sxs-lookup"><span data-stu-id="50008-141">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="50008-142"><a href="fetchprogress-event-ado.md">FetchProgress</a></span><span class="sxs-lookup"><span data-stu-id="50008-142"><a href="fetchprogress-event-ado.md">FetchProgress</a></span></span></p></td>
<td><p><span data-ttu-id="50008-143">Нет</span><span class="sxs-lookup"><span data-stu-id="50008-143">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="50008-144"><a href="willchangefield-and-fieldchangecomplete-events-ado.md">FieldChangeComplete</a></span><span class="sxs-lookup"><span data-stu-id="50008-144"><a href="willchangefield-and-fieldchangecomplete-events-ado.md">FieldChangeComplete</a></span></span></p></td>
<td><p><span data-ttu-id="50008-145">Да</span><span class="sxs-lookup"><span data-stu-id="50008-145">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="50008-146"><a href="willmove-and-movecomplete-events-ado.md">MoveComplete</a></span><span class="sxs-lookup"><span data-stu-id="50008-146"><a href="willmove-and-movecomplete-events-ado.md">MoveComplete</a></span></span></p></td>
<td><p><span data-ttu-id="50008-147">Нет</span><span class="sxs-lookup"><span data-stu-id="50008-147">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="50008-148"><a href="willchangerecord-and-recordchangecomplete-events-ado.md">RecordChangeComplete</a></span><span class="sxs-lookup"><span data-stu-id="50008-148"><a href="willchangerecord-and-recordchangecomplete-events-ado.md">RecordChangeComplete</a></span></span></p></td>
<td><p><span data-ttu-id="50008-149">Да</span><span class="sxs-lookup"><span data-stu-id="50008-149">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="50008-150"><a href="willchangerecordset-and-recordsetchangecomplete-events-ado.md">RecordsetChangeComplete</a></span><span class="sxs-lookup"><span data-stu-id="50008-150"><a href="willchangerecordset-and-recordsetchangecomplete-events-ado.md">RecordsetChangeComplete</a></span></span></p></td>
<td><p><span data-ttu-id="50008-151">Нет</span><span class="sxs-lookup"><span data-stu-id="50008-151">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="50008-152"><a href="willchangefield-and-fieldchangecomplete-events-ado.md">WillChangeField</a></span><span class="sxs-lookup"><span data-stu-id="50008-152"><a href="willchangefield-and-fieldchangecomplete-events-ado.md">WillChangeField</a></span></span></p></td>
<td><p><span data-ttu-id="50008-153">Да</span><span class="sxs-lookup"><span data-stu-id="50008-153">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="50008-154"><a href="willchangerecord-and-recordchangecomplete-events-ado.md">WillChangeRecord</a></span><span class="sxs-lookup"><span data-stu-id="50008-154"><a href="willchangerecord-and-recordchangecomplete-events-ado.md">WillChangeRecord</a></span></span></p></td>
<td><p><span data-ttu-id="50008-155">Да</span><span class="sxs-lookup"><span data-stu-id="50008-155">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="50008-156"><a href="willchangerecordset-and-recordsetchangecomplete-events-ado.md">WillChangeRecordset</a></span><span class="sxs-lookup"><span data-stu-id="50008-156"><a href="willchangerecordset-and-recordsetchangecomplete-events-ado.md">WillChangeRecordset</a></span></span></p></td>
<td><p><span data-ttu-id="50008-157">Нет</span><span class="sxs-lookup"><span data-stu-id="50008-157">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="50008-158"><a href="willmove-and-movecomplete-events-ado.md">WillMove</a></span><span class="sxs-lookup"><span data-stu-id="50008-158"><a href="willmove-and-movecomplete-events-ado.md">WillMove</a></span></span></p></td>
<td><p><span data-ttu-id="50008-159">Нет</span><span class="sxs-lookup"><span data-stu-id="50008-159">No</span></span></p></td>
</tr>
</tbody>
</table>


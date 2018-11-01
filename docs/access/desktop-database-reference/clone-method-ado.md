---
title: Клонирование метод - ActiveX Data Objects (ADO)
TOCTitle: Clone Method (ADO)
ms:assetid: ca9b2b76-90bf-9a60-2611-3cb4977d5591
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249984(v=office.15)
ms:contentKeyID: 48547693
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: efff94e9f86d1fac7fd8b3716b1df2029bd32eb9
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25876388"
---
# <a name="clone-method-ado"></a><span data-ttu-id="8cab4-102">Клонирование метод (ADO)</span><span class="sxs-lookup"><span data-stu-id="8cab4-102">Clone Method (ADO)</span></span>


<span data-ttu-id="8cab4-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="8cab4-103">**Applies to**: Access 2013, Office 2013</span></span>



<span data-ttu-id="8cab4-104">Создает объект повторяющихся [записей](recordset-object-ado.md) из существующего объекта **набора записей** .</span><span class="sxs-lookup"><span data-stu-id="8cab4-104">Creates a duplicate [Recordset](recordset-object-ado.md) object from an existing **Recordset** object.</span></span> <span data-ttu-id="8cab4-105">При необходимости указывает копию только для чтения.</span><span class="sxs-lookup"><span data-stu-id="8cab4-105">Optionally, specifies that the clone be read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="8cab4-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="8cab4-106">Syntax</span></span>

<span data-ttu-id="8cab4-107">**Установка** *rstDuplicate*  =  *rstOriginal*. Копия (*LockType для*)</span><span class="sxs-lookup"><span data-stu-id="8cab4-107">**Set** *rstDuplicate* = *rstOriginal*.Clone (*LockType*)</span></span>

## <a name="return-value"></a><span data-ttu-id="8cab4-108">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="8cab4-108">Return value</span></span>

<span data-ttu-id="8cab4-109">Возвращает ссылку на объект **набора записей** .</span><span class="sxs-lookup"><span data-stu-id="8cab4-109">Returns a **Recordset** object reference.</span></span>

## <a name="parameters"></a><span data-ttu-id="8cab4-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="8cab4-110">Parameters</span></span>

  - <span data-ttu-id="8cab4-111">*rstDuplicate*</span><span class="sxs-lookup"><span data-stu-id="8cab4-111">*rstDuplicate*</span></span>

  - <span data-ttu-id="8cab4-112">Объектная переменная, которая определяет повторяющихся **записей** объект будет создан.</span><span class="sxs-lookup"><span data-stu-id="8cab4-112">An object variable that identifies the duplicate **Recordset** object to be created.</span></span>

  - <span data-ttu-id="8cab4-113">*rstOriginal*</span><span class="sxs-lookup"><span data-stu-id="8cab4-113">*rstOriginal*</span></span>

  - <span data-ttu-id="8cab4-114">Объектная переменная, которая определяет объект **набора записей** дублирование.</span><span class="sxs-lookup"><span data-stu-id="8cab4-114">An object variable that identifies the **Recordset** object to be duplicated.</span></span>

  - <span data-ttu-id="8cab4-115">*LockType для*</span><span class="sxs-lookup"><span data-stu-id="8cab4-115">*LockType*</span></span>

  - <span data-ttu-id="8cab4-116">Необязательный параметр.</span><span class="sxs-lookup"><span data-stu-id="8cab4-116">Optional.</span></span> <span data-ttu-id="8cab4-117">[LockTypeEnum](locktypeenum.md) значение, задающее тип блокировки исходного **набора записей**или только для чтения **набора записей**.</span><span class="sxs-lookup"><span data-stu-id="8cab4-117">A [LockTypeEnum](locktypeenum.md) value that specifies either the lock type of the original **Recordset**, or a read-only **Recordset**.</span></span> <span data-ttu-id="8cab4-118">Допустимые значения: **adLockUnspecified** или **adLockReadOnly**.</span><span class="sxs-lookup"><span data-stu-id="8cab4-118">Valid values are **adLockUnspecified** or **adLockReadOnly**.</span></span>

## <a name="remarks"></a><span data-ttu-id="8cab4-119">Замечания</span><span class="sxs-lookup"><span data-stu-id="8cab4-119">Remarks</span></span>

<span data-ttu-id="8cab4-120">Используйте метод **клонированной** для создания нескольких дубликатов объектов **набора записей** , особенно в том случае, если вы хотите поддерживать более одного текущей записи в данного набора записей.</span><span class="sxs-lookup"><span data-stu-id="8cab4-120">Use the **Clone** method to create multiple, duplicate **Recordset** objects, particularly if you want to maintain more than one current record in a given set of records.</span></span> <span data-ttu-id="8cab4-121">С помощью метода **клонированной** эффективнее, чем создания и открытия нового объекта **набора записей** с тем же определением, что и исходный.</span><span class="sxs-lookup"><span data-stu-id="8cab4-121">Using the **Clone** method is more efficient than creating and opening a new **Recordset** object with the same definition as the original.</span></span>

<span data-ttu-id="8cab4-122">Свойства [фильтра](filter-property-ado.md) из исходного **набора записей**при их наличии, не применяются к копии.</span><span class="sxs-lookup"><span data-stu-id="8cab4-122">The [Filter](filter-property-ado.md) property of the original **Recordset**, if any, will not be applied to the clone.</span></span> <span data-ttu-id="8cab4-123">Свойства **фильтра** нового **набора записей** для фильтрации результатов.</span><span class="sxs-lookup"><span data-stu-id="8cab4-123">Set the **Filter** property of the new **Recordset** in order to filter the results.</span></span> <span data-ttu-id="8cab4-124">Чтобы скопировать все существующие значения **фильтра** проще всего напрямую, назначьте его следующим образом:</span><span class="sxs-lookup"><span data-stu-id="8cab4-124">The simplest way to copy any existing **Filter** value is to assign it directly, like this:</span></span>

<span data-ttu-id="8cab4-125">Текущая запись только что созданный клонированной присвоено значение первой записи.</span><span class="sxs-lookup"><span data-stu-id="8cab4-125">The current record of a newly created clone is set to the first record.</span></span>

<span data-ttu-id="8cab4-126">Изменения, внесенные на **один Recordset** видны во всех его копирует вне зависимости от типа курсора.</span><span class="sxs-lookup"><span data-stu-id="8cab4-126">Changes you make to one **Recordset** object are visible in all of its clones regardless of cursor type.</span></span> <span data-ttu-id="8cab4-127">Тем не менее после выполнения [запроса](requery-method-ado.md) на исходный **набора записей**копирует больше не синхронизируются с исходным.</span><span class="sxs-lookup"><span data-stu-id="8cab4-127">However, after you execute [Requery](requery-method-ado.md) on the original **Recordset**, the clones will no longer be synchronized to the original.</span></span>

<span data-ttu-id="8cab4-128">Закрытие исходного **набора записей** не закрывайте его копии, а также закрывая копии закрыть исходной или любых других копий.</span><span class="sxs-lookup"><span data-stu-id="8cab4-128">Closing the original **Recordset** does not close its copies, nor does closing a copy close the original or any of the other copies.</span></span>

<span data-ttu-id="8cab4-129">Можно только клонирование объекта **набора записей** , который поддерживает закладки.</span><span class="sxs-lookup"><span data-stu-id="8cab4-129">You can only clone a **Recordset** object that supports bookmarks.</span></span> <span data-ttu-id="8cab4-130">Значения закладки являются взаимозаменяемыми; Таким образом закладка ссылку из одного объекта **набора записей** относится к одной и той же записи в любом из его копирует.</span><span class="sxs-lookup"><span data-stu-id="8cab4-130">Bookmark values are interchangeable; that is, a bookmark reference from one **Recordset** object refers to the same record in any of its clones.</span></span>

<span data-ttu-id="8cab4-131">Некоторые события **набора записей** , которые запускаются также будет срабатывать в копирует все **набора записей** .</span><span class="sxs-lookup"><span data-stu-id="8cab4-131">Some **Recordset** events that are triggered will also fire in all **Recordset** clones.</span></span> <span data-ttu-id="8cab4-132">Тем не менее так как текущей записи может отличаться от клонирования **наборов записей**, события могут быть допустимый для копии.</span><span class="sxs-lookup"><span data-stu-id="8cab4-132">However, because the current record can differ between cloned **Recordsets**, the events may not be valid for the clone.</span></span>

<span data-ttu-id="8cab4-133">Например, при изменении значения поля [WillChangeField](willchangefield-and-fieldchangecomplete-events-ado.md) событие происходит в измененных **записей** и копирует все.</span><span class="sxs-lookup"><span data-stu-id="8cab4-133">For example, if you change a value of a field, a [WillChangeField](willchangefield-and-fieldchangecomplete-events-ado.md) event will occur in the changed **Recordset** and in all clones.</span></span> <span data-ttu-id="8cab4-134">Параметр *поля* событие **WillChangeField** клонирования **записей** (где не изменения) просто будет ссылаться на поля текущей записи копии, может быть другой записи превышает текущий запись где произошло изменение исходного **набора записей** .</span><span class="sxs-lookup"><span data-stu-id="8cab4-134">The *Fields* parameter of the **WillChangeField** event of a cloned **Recordset** (where the change was not made) will simply refer to the fields of the current record of the clone, which may be a different record than the current record of the original **Recordset** where the change occurred.</span></span>

<span data-ttu-id="8cab4-135">В следующей таблице предоставляются полный список всех **записей** событий и указывает, являются ли они действительный и включаемая для любого копирует набора записей, созданных с помощью метода **клонирования** .</span><span class="sxs-lookup"><span data-stu-id="8cab4-135">The following table provided a full listing of all **Recordset** events and indicates whether they are valid and triggered for any recordset clones generated using the **Clone** method.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="8cab4-136">Событие</span><span class="sxs-lookup"><span data-stu-id="8cab4-136">Event</span></span></p></th>
<th><p><span data-ttu-id="8cab4-137">Запущено копирует?</span><span class="sxs-lookup"><span data-stu-id="8cab4-137">Triggered in clones?</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="8cab4-138"><a href="endofrecordset-event-ado.md">EndOfRecordset</a></span><span class="sxs-lookup"><span data-stu-id="8cab4-138"><a href="endofrecordset-event-ado.md">EndOfRecordset</a></span></span></p></td>
<td><p><span data-ttu-id="8cab4-139">Нет</span><span class="sxs-lookup"><span data-stu-id="8cab4-139">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8cab4-140"><a href="fetchcomplete-event-ado.md">FetchComplete</a></span><span class="sxs-lookup"><span data-stu-id="8cab4-140"><a href="fetchcomplete-event-ado.md">FetchComplete</a></span></span></p></td>
<td><p><span data-ttu-id="8cab4-141">Нет</span><span class="sxs-lookup"><span data-stu-id="8cab4-141">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8cab4-142"><a href="fetchprogress-event-ado.md">FetchProgress</a></span><span class="sxs-lookup"><span data-stu-id="8cab4-142"><a href="fetchprogress-event-ado.md">FetchProgress</a></span></span></p></td>
<td><p><span data-ttu-id="8cab4-143">Нет</span><span class="sxs-lookup"><span data-stu-id="8cab4-143">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8cab4-144"><a href="willchangefield-and-fieldchangecomplete-events-ado.md">FieldChangeComplete</a></span><span class="sxs-lookup"><span data-stu-id="8cab4-144"><a href="willchangefield-and-fieldchangecomplete-events-ado.md">FieldChangeComplete</a></span></span></p></td>
<td><p><span data-ttu-id="8cab4-145">Да</span><span class="sxs-lookup"><span data-stu-id="8cab4-145">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8cab4-146"><a href="willmove-and-movecomplete-events-ado.md">MoveComplete</a></span><span class="sxs-lookup"><span data-stu-id="8cab4-146"><a href="willmove-and-movecomplete-events-ado.md">MoveComplete</a></span></span></p></td>
<td><p><span data-ttu-id="8cab4-147">Нет</span><span class="sxs-lookup"><span data-stu-id="8cab4-147">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8cab4-148"><a href="willchangerecord-and-recordchangecomplete-events-ado.md">RecordChangeComplete</a></span><span class="sxs-lookup"><span data-stu-id="8cab4-148"><a href="willchangerecord-and-recordchangecomplete-events-ado.md">RecordChangeComplete</a></span></span></p></td>
<td><p><span data-ttu-id="8cab4-149">Да</span><span class="sxs-lookup"><span data-stu-id="8cab4-149">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8cab4-150"><a href="willchangerecordset-and-recordsetchangecomplete-events-ado.md">RecordsetChangeComplete</a></span><span class="sxs-lookup"><span data-stu-id="8cab4-150"><a href="willchangerecordset-and-recordsetchangecomplete-events-ado.md">RecordsetChangeComplete</a></span></span></p></td>
<td><p><span data-ttu-id="8cab4-151">Нет</span><span class="sxs-lookup"><span data-stu-id="8cab4-151">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8cab4-152"><a href="willchangefield-and-fieldchangecomplete-events-ado.md">WillChangeField</a></span><span class="sxs-lookup"><span data-stu-id="8cab4-152"><a href="willchangefield-and-fieldchangecomplete-events-ado.md">WillChangeField</a></span></span></p></td>
<td><p><span data-ttu-id="8cab4-153">Да</span><span class="sxs-lookup"><span data-stu-id="8cab4-153">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8cab4-154"><a href="willchangerecord-and-recordchangecomplete-events-ado.md">WillChangeRecord</a></span><span class="sxs-lookup"><span data-stu-id="8cab4-154"><a href="willchangerecord-and-recordchangecomplete-events-ado.md">WillChangeRecord</a></span></span></p></td>
<td><p><span data-ttu-id="8cab4-155">Да</span><span class="sxs-lookup"><span data-stu-id="8cab4-155">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8cab4-156"><a href="willchangerecordset-and-recordsetchangecomplete-events-ado.md">WillChangeRecordset</a></span><span class="sxs-lookup"><span data-stu-id="8cab4-156"><a href="willchangerecordset-and-recordsetchangecomplete-events-ado.md">WillChangeRecordset</a></span></span></p></td>
<td><p><span data-ttu-id="8cab4-157">Нет</span><span class="sxs-lookup"><span data-stu-id="8cab4-157">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8cab4-158"><a href="willmove-and-movecomplete-events-ado.md">WillMove</a></span><span class="sxs-lookup"><span data-stu-id="8cab4-158"><a href="willmove-and-movecomplete-events-ado.md">WillMove</a></span></span></p></td>
<td><p><span data-ttu-id="8cab4-159">Нет</span><span class="sxs-lookup"><span data-stu-id="8cab4-159">No</span></span></p></td>
</tr>
</tbody>
</table>


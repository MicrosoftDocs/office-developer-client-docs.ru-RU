---
title: Метод клонирования — ActiveX объектов данных (ADO)
TOCTitle: Clone method (ADO)
ms:assetid: ca9b2b76-90bf-9a60-2611-3cb4977d5591
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249984(v=office.15)
ms:contentKeyID: 48547693
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 095191bbfe55f2c38529cb1c260979c48dd2d5f1
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32296348"
---
# <a name="clone-method-ado"></a><span data-ttu-id="8412a-102">Метод клонирования (ADO)</span><span class="sxs-lookup"><span data-stu-id="8412a-102">Clone method (ADO)</span></span>

<span data-ttu-id="8412a-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="8412a-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="8412a-104">Создает дубликат [объекта Recordset](recordset-object-ado.md) из существующего объекта **Recordset.**</span><span class="sxs-lookup"><span data-stu-id="8412a-104">Creates a duplicate [Recordset](recordset-object-ado.md) object from an existing **Recordset** object.</span></span> <span data-ttu-id="8412a-105">Необязательно указывает, что клон должен быть только для чтения.</span><span class="sxs-lookup"><span data-stu-id="8412a-105">Optionally, specifies that the clone be read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="8412a-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="8412a-106">Syntax</span></span>

<span data-ttu-id="8412a-107">**Установите** *rstDuplicate*  =  *rstOriginal*. Клон *(LockType)*</span><span class="sxs-lookup"><span data-stu-id="8412a-107">**Set** *rstDuplicate* = *rstOriginal*.Clone (*LockType*)</span></span>

## <a name="return-value"></a><span data-ttu-id="8412a-108">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="8412a-108">Return value</span></span>

<span data-ttu-id="8412a-109">Возвращает ссылку **на объект Recordset.**</span><span class="sxs-lookup"><span data-stu-id="8412a-109">Returns a **Recordset** object reference.</span></span>

## <a name="parameters"></a><span data-ttu-id="8412a-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="8412a-110">Parameters</span></span>

|<span data-ttu-id="8412a-111">Параметр</span><span class="sxs-lookup"><span data-stu-id="8412a-111">Parameter</span></span>|<span data-ttu-id="8412a-112">Описание</span><span class="sxs-lookup"><span data-stu-id="8412a-112">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="8412a-113">*rstDuplicate*</span><span class="sxs-lookup"><span data-stu-id="8412a-113">*rstDuplicate*</span></span> |<span data-ttu-id="8412a-114">Переменная объекта, идентифицирует созданный объект **Recordset.**</span><span class="sxs-lookup"><span data-stu-id="8412a-114">An object variable that identifies the duplicate **Recordset** object to be created.</span></span>|
|<span data-ttu-id="8412a-115">*rstOriginal*</span><span class="sxs-lookup"><span data-stu-id="8412a-115">*rstOriginal*</span></span> |<span data-ttu-id="8412a-116">Переменная объекта, идентифицирует объект **Recordset,** который будет дублироваться.</span><span class="sxs-lookup"><span data-stu-id="8412a-116">An object variable that identifies the **Recordset** object to be duplicated.</span></span>|
|<span data-ttu-id="8412a-117">*LockType*</span><span class="sxs-lookup"><span data-stu-id="8412a-117">*LockType*</span></span> |<span data-ttu-id="8412a-118">Необязательный параметр.</span><span class="sxs-lookup"><span data-stu-id="8412a-118">Optional.</span></span> <span data-ttu-id="8412a-119">Значение [LockTypeEnum,](locktypeenum.md) которое указывает тип блокировки исходного **набора записей** или только для **чтения.**</span><span class="sxs-lookup"><span data-stu-id="8412a-119">A [LockTypeEnum](locktypeenum.md) value that specifies either the lock type of the original **Recordset**, or a read-only **Recordset**.</span></span> <span data-ttu-id="8412a-120">Допустимые значения **adLockUnspecified** или **adLockReadOnly.**</span><span class="sxs-lookup"><span data-stu-id="8412a-120">Valid values are **adLockUnspecified** or **adLockReadOnly**.</span></span>|

## <a name="remarks"></a><span data-ttu-id="8412a-121">Примечания</span><span class="sxs-lookup"><span data-stu-id="8412a-121">Remarks</span></span>

<span data-ttu-id="8412a-122">Используйте метод **Клона** для создания нескольких дублирующихся объектов **Recordset,** особенно если вы хотите сохранить несколько текущих записей в определенном наборе записей.</span><span class="sxs-lookup"><span data-stu-id="8412a-122">Use the **Clone** method to create multiple, duplicate **Recordset** objects, particularly if you want to maintain more than one current record in a given set of records.</span></span> <span data-ttu-id="8412a-123">Использование метода **Клона** является более эффективным, чем создание и открытие нового объекта **Recordset** с тем же определением, что и оригинал.</span><span class="sxs-lookup"><span data-stu-id="8412a-123">Using the **Clone** method is more efficient than creating and opening a new **Recordset** object with the same definition as the original.</span></span>

<span data-ttu-id="8412a-124">Свойство [Filter](filter-property-ado.md) исходного **набора записей,** если таково, не будет применено к клону.</span><span class="sxs-lookup"><span data-stu-id="8412a-124">The [Filter](filter-property-ado.md) property of the original **Recordset**, if any, will not be applied to the clone.</span></span> <span data-ttu-id="8412a-125">Установите свойство **Filter** нового **набора записей** для фильтрации результатов.</span><span class="sxs-lookup"><span data-stu-id="8412a-125">Set the **Filter** property of the new **Recordset** in order to filter the results.</span></span> <span data-ttu-id="8412a-126">Самый простой способ скопировать существующее значение **Filter** — назначить его напрямую, например:</span><span class="sxs-lookup"><span data-stu-id="8412a-126">The simplest way to copy any existing **Filter** value is to assign it directly, like this:</span></span>

<span data-ttu-id="8412a-127">Текущая запись только что созданного клона установлена к первой записи.</span><span class="sxs-lookup"><span data-stu-id="8412a-127">The current record of a newly created clone is set to the first record.</span></span>

<span data-ttu-id="8412a-128">Изменения, внесенные в один **объект Recordset,** видны во всех его клонах независимо от типа курсора.</span><span class="sxs-lookup"><span data-stu-id="8412a-128">Changes you make to one **Recordset** object are visible in all of its clones regardless of cursor type.</span></span> <span data-ttu-id="8412a-129">Однако после выполнения [Requery](requery-method-ado.md) в исходном **Наборе записей** клоны больше не будут синхронизированы с оригиналом.</span><span class="sxs-lookup"><span data-stu-id="8412a-129">However, after you execute [Requery](requery-method-ado.md) on the original **Recordset**, the clones will no longer be synchronized to the original.</span></span>

<span data-ttu-id="8412a-130">Закрытие **исходного набора записей** не закрывает его копии и не закрывает копию оригинала или других копий.</span><span class="sxs-lookup"><span data-stu-id="8412a-130">Closing the original **Recordset** does not close its copies, nor does closing a copy close the original or any of the other copies.</span></span>

<span data-ttu-id="8412a-131">Клонировать можно только объект **Recordset,** который поддерживает закладки.</span><span class="sxs-lookup"><span data-stu-id="8412a-131">You can only clone a **Recordset** object that supports bookmarks.</span></span> <span data-ttu-id="8412a-132">Значения закладок взаимозаменяемы; то есть ссылка на закладки с одного объекта **Recordset** относится к одной записи в любом из его клонов.</span><span class="sxs-lookup"><span data-stu-id="8412a-132">Bookmark values are interchangeable; that is, a bookmark reference from one **Recordset** object refers to the same record in any of its clones.</span></span>

<span data-ttu-id="8412a-133">Некоторые  срабатываемые события Recordset также будут запускать во всех **клонах Recordset.**</span><span class="sxs-lookup"><span data-stu-id="8412a-133">Some **Recordset** events that are triggered will also fire in all **Recordset** clones.</span></span> <span data-ttu-id="8412a-134">Однако, поскольку текущая запись может отличаться между клонированными записями, события могут быть не допустимы для клона.</span><span class="sxs-lookup"><span data-stu-id="8412a-134">However, because the current record can differ between cloned **Recordsets**, the events may not be valid for the clone.</span></span>

<span data-ttu-id="8412a-135">Например, при изменении значения поля событие [WillChangeField](willchangefield-and-fieldchangecomplete-events-ado.md) будет происходить  в измененной записи и во всех клонах.</span><span class="sxs-lookup"><span data-stu-id="8412a-135">For example, if you change a value of a field, a [WillChangeField](willchangefield-and-fieldchangecomplete-events-ado.md) event will occur in the changed **Recordset** and in all clones.</span></span> <span data-ttu-id="8412a-136">Параметр *Fields* события **WillChangeField** клонированной записи (где изменение не было сделано) будет просто ссылаться на поля текущей записи клона, которая может быть другой записью, чем текущая запись исходного **recordset,** где произошли изменения. </span><span class="sxs-lookup"><span data-stu-id="8412a-136">The *Fields* parameter of the **WillChangeField** event of a cloned **Recordset** (where the change was not made) will simply refer to the fields of the current record of the clone, which may be a different record than the current record of the original **Recordset** where the change occurred.</span></span>

<span data-ttu-id="8412a-137">В следующей таблице представлен полный список всех событий **Recordset** и указывается, являются ли они допустимы и запускаются для всех клонов наборов записей, созданных с помощью метода **Клона.**</span><span class="sxs-lookup"><span data-stu-id="8412a-137">The following table provided a full listing of all **Recordset** events and indicates whether they are valid and triggered for any recordset clones generated using the **Clone** method.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="8412a-138">Событие</span><span class="sxs-lookup"><span data-stu-id="8412a-138">Event</span></span></p></th>
<th><p><span data-ttu-id="8412a-139">Срабатывает в клонах?</span><span class="sxs-lookup"><span data-stu-id="8412a-139">Triggered in clones?</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="8412a-140"><a href="endofrecordset-event-ado.md">EndOfRecordset</a></span><span class="sxs-lookup"><span data-stu-id="8412a-140"><a href="endofrecordset-event-ado.md">EndOfRecordset</a></span></span></p></td>
<td><p><span data-ttu-id="8412a-141">Нет</span><span class="sxs-lookup"><span data-stu-id="8412a-141">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8412a-142"><a href="fetchcomplete-event-ado.md">FetchComplete</a></span><span class="sxs-lookup"><span data-stu-id="8412a-142"><a href="fetchcomplete-event-ado.md">FetchComplete</a></span></span></p></td>
<td><p><span data-ttu-id="8412a-143">Нет</span><span class="sxs-lookup"><span data-stu-id="8412a-143">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8412a-144"><a href="fetchprogress-event-ado.md">FetchProgress</a></span><span class="sxs-lookup"><span data-stu-id="8412a-144"><a href="fetchprogress-event-ado.md">FetchProgress</a></span></span></p></td>
<td><p><span data-ttu-id="8412a-145">Нет</span><span class="sxs-lookup"><span data-stu-id="8412a-145">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8412a-146"><a href="willchangefield-and-fieldchangecomplete-events-ado.md">FieldChangeComplete</a></span><span class="sxs-lookup"><span data-stu-id="8412a-146"><a href="willchangefield-and-fieldchangecomplete-events-ado.md">FieldChangeComplete</a></span></span></p></td>
<td><p><span data-ttu-id="8412a-147">Да</span><span class="sxs-lookup"><span data-stu-id="8412a-147">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8412a-148"><a href="willmove-and-movecomplete-events-ado.md">MoveComplete</a></span><span class="sxs-lookup"><span data-stu-id="8412a-148"><a href="willmove-and-movecomplete-events-ado.md">MoveComplete</a></span></span></p></td>
<td><p><span data-ttu-id="8412a-149">Нет</span><span class="sxs-lookup"><span data-stu-id="8412a-149">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8412a-150"><a href="willchangerecord-and-recordchangecomplete-events-ado.md">RecordChangeComplete</a></span><span class="sxs-lookup"><span data-stu-id="8412a-150"><a href="willchangerecord-and-recordchangecomplete-events-ado.md">RecordChangeComplete</a></span></span></p></td>
<td><p><span data-ttu-id="8412a-151">Да</span><span class="sxs-lookup"><span data-stu-id="8412a-151">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8412a-152"><a href="willchangerecordset-and-recordsetchangecomplete-events-ado.md">RecordsetChangeComplete</a></span><span class="sxs-lookup"><span data-stu-id="8412a-152"><a href="willchangerecordset-and-recordsetchangecomplete-events-ado.md">RecordsetChangeComplete</a></span></span></p></td>
<td><p><span data-ttu-id="8412a-153">Нет</span><span class="sxs-lookup"><span data-stu-id="8412a-153">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8412a-154"><a href="willchangefield-and-fieldchangecomplete-events-ado.md">WillChangeField</a></span><span class="sxs-lookup"><span data-stu-id="8412a-154"><a href="willchangefield-and-fieldchangecomplete-events-ado.md">WillChangeField</a></span></span></p></td>
<td><p><span data-ttu-id="8412a-155">Да</span><span class="sxs-lookup"><span data-stu-id="8412a-155">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8412a-156"><a href="willchangerecord-and-recordchangecomplete-events-ado.md">WillChangeRecord</a></span><span class="sxs-lookup"><span data-stu-id="8412a-156"><a href="willchangerecord-and-recordchangecomplete-events-ado.md">WillChangeRecord</a></span></span></p></td>
<td><p><span data-ttu-id="8412a-157">Да</span><span class="sxs-lookup"><span data-stu-id="8412a-157">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8412a-158"><a href="willchangerecordset-and-recordsetchangecomplete-events-ado.md">WillChangeRecordset</a></span><span class="sxs-lookup"><span data-stu-id="8412a-158"><a href="willchangerecordset-and-recordsetchangecomplete-events-ado.md">WillChangeRecordset</a></span></span></p></td>
<td><p><span data-ttu-id="8412a-159">Нет</span><span class="sxs-lookup"><span data-stu-id="8412a-159">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8412a-160"><a href="willmove-and-movecomplete-events-ado.md">WillMove</a></span><span class="sxs-lookup"><span data-stu-id="8412a-160"><a href="willmove-and-movecomplete-events-ado.md">WillMove</a></span></span></p></td>
<td><p><span data-ttu-id="8412a-161">Нет</span><span class="sxs-lookup"><span data-stu-id="8412a-161">No</span></span></p></td>
</tr>
</tbody>
</table>


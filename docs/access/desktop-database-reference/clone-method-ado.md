---
title: Метод Clone — объекты данных ActiveX (ADO)
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
# <a name="clone-method-ado"></a><span data-ttu-id="883ce-102">Метод Clone (ADO)</span><span class="sxs-lookup"><span data-stu-id="883ce-102">Clone method (ADO)</span></span>

<span data-ttu-id="883ce-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="883ce-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="883ce-104">Создает дубликат объекта [Recordset](recordset-object-ado.md) из существующего объекта **Recordset** .</span><span class="sxs-lookup"><span data-stu-id="883ce-104">Creates a duplicate [Recordset](recordset-object-ado.md) object from an existing **Recordset** object.</span></span> <span data-ttu-id="883ce-105">При необходимости этот параметр указывает, что клон должен быть доступен только для чтения.</span><span class="sxs-lookup"><span data-stu-id="883ce-105">Optionally, specifies that the clone be read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="883ce-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="883ce-106">Syntax</span></span>

<span data-ttu-id="883ce-107">**Set** *рстдупликате*  =  *рсторигинал*. Clone (*LockType*)</span><span class="sxs-lookup"><span data-stu-id="883ce-107">**Set** *rstDuplicate* = *rstOriginal*.Clone (*LockType*)</span></span>

## <a name="return-value"></a><span data-ttu-id="883ce-108">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="883ce-108">Return value</span></span>

<span data-ttu-id="883ce-109">Возвращает ссылку на объект **Recordset** .</span><span class="sxs-lookup"><span data-stu-id="883ce-109">Returns a **Recordset** object reference.</span></span>

## <a name="parameters"></a><span data-ttu-id="883ce-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="883ce-110">Parameters</span></span>

|<span data-ttu-id="883ce-111">Параметр</span><span class="sxs-lookup"><span data-stu-id="883ce-111">Parameter</span></span>|<span data-ttu-id="883ce-112">Описание</span><span class="sxs-lookup"><span data-stu-id="883ce-112">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="883ce-113">*Рстдупликате*</span><span class="sxs-lookup"><span data-stu-id="883ce-113">*rstDuplicate*</span></span> |<span data-ttu-id="883ce-114">Объектная переменная, определяющая дубликат создаваемого объекта **Recordset** .</span><span class="sxs-lookup"><span data-stu-id="883ce-114">An object variable that identifies the duplicate **Recordset** object to be created.</span></span>|
|<span data-ttu-id="883ce-115">*Рсторигинал*</span><span class="sxs-lookup"><span data-stu-id="883ce-115">*rstOriginal*</span></span> |<span data-ttu-id="883ce-116">Объектная переменная, определяющая объект **Recordset** , который будет дублироваться.</span><span class="sxs-lookup"><span data-stu-id="883ce-116">An object variable that identifies the **Recordset** object to be duplicated.</span></span>|
|<span data-ttu-id="883ce-117">*LockType*</span><span class="sxs-lookup"><span data-stu-id="883ce-117">*LockType*</span></span> |<span data-ttu-id="883ce-118">Необязательный атрибут.</span><span class="sxs-lookup"><span data-stu-id="883ce-118">Optional.</span></span> <span data-ttu-id="883ce-119">Значение [LockTypeEnum](locktypeenum.md) , задающее либо тип блокировки исходного объекта **Recordset**, либо **набор записей**, доступное только для чтения.</span><span class="sxs-lookup"><span data-stu-id="883ce-119">A [LockTypeEnum](locktypeenum.md) value that specifies either the lock type of the original **Recordset**, or a read-only **Recordset**.</span></span> <span data-ttu-id="883ce-120">Допустимые значения: **адлоккунспеЦифиед** и **адлоккреадонли**.</span><span class="sxs-lookup"><span data-stu-id="883ce-120">Valid values are **adLockUnspecified** or **adLockReadOnly**.</span></span>|

## <a name="remarks"></a><span data-ttu-id="883ce-121">Замечания</span><span class="sxs-lookup"><span data-stu-id="883ce-121">Remarks</span></span>

<span data-ttu-id="883ce-122">Используйте метод **clone** для создания нескольких дублирующихся объектов **Recordset** , в частности, если требуется поддерживать несколько текущих записей в заданном наборе записей.</span><span class="sxs-lookup"><span data-stu-id="883ce-122">Use the **Clone** method to create multiple, duplicate **Recordset** objects, particularly if you want to maintain more than one current record in a given set of records.</span></span> <span data-ttu-id="883ce-123">Использование метода **clone** является более эффективным, чем создание и открытие нового объекта **Recordset** с тем же определением, что и исходный.</span><span class="sxs-lookup"><span data-stu-id="883ce-123">Using the **Clone** method is more efficient than creating and opening a new **Recordset** object with the same definition as the original.</span></span>

<span data-ttu-id="883ce-124">Свойство [Filter](filter-property-ado.md) исходного объекта **Recordset**(если таковое имеется) не будет применено к клону.</span><span class="sxs-lookup"><span data-stu-id="883ce-124">The [Filter](filter-property-ado.md) property of the original **Recordset**, if any, will not be applied to the clone.</span></span> <span data-ttu-id="883ce-125">Задайте свойство **Filter** для нового объекта **Recordset** , чтобы отфильтровать результаты.</span><span class="sxs-lookup"><span data-stu-id="883ce-125">Set the **Filter** property of the new **Recordset** in order to filter the results.</span></span> <span data-ttu-id="883ce-126">Самый простой способ скопировать любое существующее значение **фильтра** — назначить его напрямую, как показано ниже:</span><span class="sxs-lookup"><span data-stu-id="883ce-126">The simplest way to copy any existing **Filter** value is to assign it directly, like this:</span></span>

<span data-ttu-id="883ce-127">Для текущей записи созданного клона задается первая запись.</span><span class="sxs-lookup"><span data-stu-id="883ce-127">The current record of a newly created clone is set to the first record.</span></span>

<span data-ttu-id="883ce-128">Изменения, вносимые в один объект **Recordset** , отображаются во всех клонах, независимо от типа курсора.</span><span class="sxs-lookup"><span data-stu-id="883ce-128">Changes you make to one **Recordset** object are visible in all of its clones regardless of cursor type.</span></span> <span data-ttu-id="883ce-129">Однако после выполнения командлета [Requery](requery-method-ado.md) для исходного объекта **Recordset**клоны больше не будут синхронизироваться с исходным.</span><span class="sxs-lookup"><span data-stu-id="883ce-129">However, after you execute [Requery](requery-method-ado.md) on the original **Recordset**, the clones will no longer be synchronized to the original.</span></span>

<span data-ttu-id="883ce-130">Закрытие исходного объекта **Recordset** не приводит к закрытию его копий, а также закрытию копии.</span><span class="sxs-lookup"><span data-stu-id="883ce-130">Closing the original **Recordset** does not close its copies, nor does closing a copy close the original or any of the other copies.</span></span>

<span data-ttu-id="883ce-131">Можно клонировать только объект **Recordset** , который поддерживает закладки.</span><span class="sxs-lookup"><span data-stu-id="883ce-131">You can only clone a **Recordset** object that supports bookmarks.</span></span> <span data-ttu-id="883ce-132">Значения закладок являются взаимозаменяемыми; то есть ссылка на закладку из одного объекта **Recordset** ссылается на одну и ту же запись в любом из его клонов.</span><span class="sxs-lookup"><span data-stu-id="883ce-132">Bookmark values are interchangeable; that is, a bookmark reference from one **Recordset** object refers to the same record in any of its clones.</span></span>

<span data-ttu-id="883ce-133">Некоторые инициированные события **Recordset** также будут срабатывать во всех клонах **набора записей** .</span><span class="sxs-lookup"><span data-stu-id="883ce-133">Some **Recordset** events that are triggered will also fire in all **Recordset** clones.</span></span> <span data-ttu-id="883ce-134">Тем не менее, поскольку текущая запись может различаться с помощью клонированных **наборов записей**, события могут быть недопустимы для клона.</span><span class="sxs-lookup"><span data-stu-id="883ce-134">However, because the current record can differ between cloned **Recordsets**, the events may not be valid for the clone.</span></span>

<span data-ttu-id="883ce-135">Например, если изменить значение поля, событие [события willchangefield](willchangefield-and-fieldchangecomplete-events-ado.md) будет происходить в измененном **наборе записей** и всех клонах.</span><span class="sxs-lookup"><span data-stu-id="883ce-135">For example, if you change a value of a field, a [WillChangeField](willchangefield-and-fieldchangecomplete-events-ado.md) event will occur in the changed **Recordset** and in all clones.</span></span> <span data-ttu-id="883ce-136">Параметр *Fields* для события **события willchangefield** клонированного **набора записей** (если это изменение не был изменен) просто ссылается на поля текущей записи клона, которые могут отличаться от текущей записи исходный объект **Recordset** , в котором произошло изменение.</span><span class="sxs-lookup"><span data-stu-id="883ce-136">The *Fields* parameter of the **WillChangeField** event of a cloned **Recordset** (where the change was not made) will simply refer to the fields of the current record of the clone, which may be a different record than the current record of the original **Recordset** where the change occurred.</span></span>

<span data-ttu-id="883ce-137">В следующей таблице представлен полный список всех событий **Recordset** и указано, являются ли они допустимыми и запущены для всех клонов наборов записей, созданных с помощью метода **clone** .</span><span class="sxs-lookup"><span data-stu-id="883ce-137">The following table provided a full listing of all **Recordset** events and indicates whether they are valid and triggered for any recordset clones generated using the **Clone** method.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="883ce-138">Событие</span><span class="sxs-lookup"><span data-stu-id="883ce-138">Event</span></span></p></th>
<th><p><span data-ttu-id="883ce-139">Активировано в клонах?</span><span class="sxs-lookup"><span data-stu-id="883ce-139">Triggered in clones?</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="883ce-140"><a href="endofrecordset-event-ado.md">Событие endofrecordset</a></span><span class="sxs-lookup"><span data-stu-id="883ce-140"><a href="endofrecordset-event-ado.md">EndOfRecordset</a></span></span></p></td>
<td><p><span data-ttu-id="883ce-141">Нет</span><span class="sxs-lookup"><span data-stu-id="883ce-141">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="883ce-142"><a href="fetchcomplete-event-ado.md">Событие fetchcomplete</a></span><span class="sxs-lookup"><span data-stu-id="883ce-142"><a href="fetchcomplete-event-ado.md">FetchComplete</a></span></span></p></td>
<td><p><span data-ttu-id="883ce-143">Нет</span><span class="sxs-lookup"><span data-stu-id="883ce-143">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="883ce-144"><a href="fetchprogress-event-ado.md">Событие fetchprogress</a></span><span class="sxs-lookup"><span data-stu-id="883ce-144"><a href="fetchprogress-event-ado.md">FetchProgress</a></span></span></p></td>
<td><p><span data-ttu-id="883ce-145">Нет</span><span class="sxs-lookup"><span data-stu-id="883ce-145">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="883ce-146"><a href="willchangefield-and-fieldchangecomplete-events-ado.md">FieldChangeComplete</a></span><span class="sxs-lookup"><span data-stu-id="883ce-146"><a href="willchangefield-and-fieldchangecomplete-events-ado.md">FieldChangeComplete</a></span></span></p></td>
<td><p><span data-ttu-id="883ce-147">Да</span><span class="sxs-lookup"><span data-stu-id="883ce-147">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="883ce-148"><a href="willmove-and-movecomplete-events-ado.md">MoveComplete</a></span><span class="sxs-lookup"><span data-stu-id="883ce-148"><a href="willmove-and-movecomplete-events-ado.md">MoveComplete</a></span></span></p></td>
<td><p><span data-ttu-id="883ce-149">Нет</span><span class="sxs-lookup"><span data-stu-id="883ce-149">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="883ce-150"><a href="willchangerecord-and-recordchangecomplete-events-ado.md">RecordChangeComplete</a></span><span class="sxs-lookup"><span data-stu-id="883ce-150"><a href="willchangerecord-and-recordchangecomplete-events-ado.md">RecordChangeComplete</a></span></span></p></td>
<td><p><span data-ttu-id="883ce-151">Да</span><span class="sxs-lookup"><span data-stu-id="883ce-151">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="883ce-152"><a href="willchangerecordset-and-recordsetchangecomplete-events-ado.md">RecordsetChangeComplete</a></span><span class="sxs-lookup"><span data-stu-id="883ce-152"><a href="willchangerecordset-and-recordsetchangecomplete-events-ado.md">RecordsetChangeComplete</a></span></span></p></td>
<td><p><span data-ttu-id="883ce-153">Нет</span><span class="sxs-lookup"><span data-stu-id="883ce-153">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="883ce-154"><a href="willchangefield-and-fieldchangecomplete-events-ado.md">События willchangefield</a></span><span class="sxs-lookup"><span data-stu-id="883ce-154"><a href="willchangefield-and-fieldchangecomplete-events-ado.md">WillChangeField</a></span></span></p></td>
<td><p><span data-ttu-id="883ce-155">Да</span><span class="sxs-lookup"><span data-stu-id="883ce-155">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="883ce-156"><a href="willchangerecord-and-recordchangecomplete-events-ado.md">События willchangerecord</a></span><span class="sxs-lookup"><span data-stu-id="883ce-156"><a href="willchangerecord-and-recordchangecomplete-events-ado.md">WillChangeRecord</a></span></span></p></td>
<td><p><span data-ttu-id="883ce-157">Да</span><span class="sxs-lookup"><span data-stu-id="883ce-157">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="883ce-158"><a href="willchangerecordset-and-recordsetchangecomplete-events-ado.md">События willchangerecordset</a></span><span class="sxs-lookup"><span data-stu-id="883ce-158"><a href="willchangerecordset-and-recordsetchangecomplete-events-ado.md">WillChangeRecordset</a></span></span></p></td>
<td><p><span data-ttu-id="883ce-159">Нет</span><span class="sxs-lookup"><span data-stu-id="883ce-159">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="883ce-160"><a href="willmove-and-movecomplete-events-ado.md">События WillMove</a></span><span class="sxs-lookup"><span data-stu-id="883ce-160"><a href="willmove-and-movecomplete-events-ado.md">WillMove</a></span></span></p></td>
<td><p><span data-ttu-id="883ce-161">Нет</span><span class="sxs-lookup"><span data-stu-id="883ce-161">No</span></span></p></td>
</tr>
</tbody>
</table>


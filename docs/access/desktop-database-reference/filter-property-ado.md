---
description: Свойство Filter
title: Свойство Filter (ADO)
TOCTitle: Filter property (ADO)
ms:assetid: 5abc528a-a6ee-34de-5d44-a3249194b0a0
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249314(v=office.15)
ms:contentKeyID: 48545053
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 9d3234f1d5f41fd9f07b8d98bf3df395067780ae
ms.sourcegitcommit: 0419850d5c1b3439d9da59070201fb4952ca5d07
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/28/2020
ms.locfileid: "49734198"
---
# <a name="filter-property-ado"></a><span data-ttu-id="c8f57-103">Свойство Filter (ADO)</span><span class="sxs-lookup"><span data-stu-id="c8f57-103">Filter property (ADO)</span></span>


<span data-ttu-id="c8f57-104">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="c8f57-104">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="c8f57-105">Указывает фильтр для данных в [Наборе записей.](recordset-object-ado.md)</span><span class="sxs-lookup"><span data-stu-id="c8f57-105">Indicates a filter for data in a [Recordset](recordset-object-ado.md).</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="c8f57-106">Параметры и значения возврата</span><span class="sxs-lookup"><span data-stu-id="c8f57-106">Settings and return values</span></span>

<span data-ttu-id="c8f57-107">Задает или возвращает значение **Variant,** которое может содержать одно из следующих значений:</span><span class="sxs-lookup"><span data-stu-id="c8f57-107">Sets or returns a **Variant** value, which can contain one of the following:</span></span>

  - <span data-ttu-id="c8f57-108">**Строка** Критериев — строка, выполненная из одного или более отдельных положений, согласуется с **операторами AND** или **OR.**</span><span class="sxs-lookup"><span data-stu-id="c8f57-108">**Criteria string** — a string made up of one or more individual clauses concatenated with **AND** or **OR** operators.</span></span>

  - <span data-ttu-id="c8f57-109">**Массив закладок** — массив уникальных значений закладки, которые указывают на записи в **объекте Recordset.**</span><span class="sxs-lookup"><span data-stu-id="c8f57-109">**Array of bookmarks** — an array of unique bookmark values that point to records in the **Recordset** object.</span></span>

  - <span data-ttu-id="c8f57-110">Значение [FilterGroupEnum.](filtergroupenum.md)</span><span class="sxs-lookup"><span data-stu-id="c8f57-110">A [FilterGroupEnum](filtergroupenum.md) value.</span></span>

## <a name="remarks"></a><span data-ttu-id="c8f57-111">Примечания</span><span class="sxs-lookup"><span data-stu-id="c8f57-111">Remarks</span></span>

<span data-ttu-id="c8f57-112">Используйте свойство **Filter,** чтобы выборочно отсеить записи в **объекте Recordset.**</span><span class="sxs-lookup"><span data-stu-id="c8f57-112">Use the **Filter** property to selectively screen out records in a **Recordset** object.</span></span> <span data-ttu-id="c8f57-113">Фильтрованный **набор записей** становится текущим курсором.</span><span class="sxs-lookup"><span data-stu-id="c8f57-113">The filtered **Recordset** becomes the current cursor.</span></span> <span data-ttu-id="c8f57-114">Другие свойства, возвращающиеся значения на основе текущего курсора, затронуты, например [AbsolutePosition,](absoluteposition-property-ado.md) [AbsolutePage,](absolutepage-property-ado.md) [RecordCount](recordcount-property-ado.md)и [PageCount.](pagecount-property-ado.md)</span><span class="sxs-lookup"><span data-stu-id="c8f57-114">Other properties that return values based on the current cursor are affected, such as [AbsolutePosition](absoluteposition-property-ado.md), [AbsolutePage](absolutepage-property-ado.md), [RecordCount](recordcount-property-ado.md), and [PageCount](pagecount-property-ado.md).</span></span> <span data-ttu-id="c8f57-115">Это потому, что при настройке свойства **Filter** к определенному значению текущая запись будет перемещаться к первой записи, удовлетворяемой новому значению.</span><span class="sxs-lookup"><span data-stu-id="c8f57-115">This is because setting the **Filter** property to a specific value will move the current record to the first record that satisfies the new value.</span></span>

<span data-ttu-id="c8f57-116">Строка критериев состоит из оговорок в форме *FieldName-Operator-Value* (например, "LastName = "Smith").</span><span class="sxs-lookup"><span data-stu-id="c8f57-116">The criteria string is made up of clauses in the form *FieldName-Operator-Value* (for example, "LastName = 'Smith'").</span></span> <span data-ttu-id="c8f57-117">Можно создавать сложные положения, согласовывая отдельные положения с **AND** (например, "LastName = "Smith" и FirstName = "John") или **OR** (например, ").</span><span class="sxs-lookup"><span data-stu-id="c8f57-117">You can create compound clauses by concatenating individual clauses with **AND** (for example, "LastName = 'Smith' AND FirstName = 'John'") or **OR** (for example, ").</span></span> <span data-ttu-id="c8f57-118">Можно создавать сложные положения, согласовывая отдельные положения с **AND** (например, "LastName = "Smith" и FirstName = "John" или **OR** (например, "LastName = "Smith" или LastName = "Jones").</span><span class="sxs-lookup"><span data-stu-id="c8f57-118">You can create compound clauses by concatenating individual clauses with **AND** (for example, "LastName = 'Smith' AND FirstName = 'John'") or **OR** (for example, "LastName = 'Smith' OR LastName = 'Jones'").</span></span> <span data-ttu-id="c8f57-119">Используйте следующие рекомендации для строк критериев:</span><span class="sxs-lookup"><span data-stu-id="c8f57-119">Use the following guidelines for criteria strings:</span></span>

  - <span data-ttu-id="c8f57-120">*Имя fieldName* должно быть допустимым именем поля из **Recordset.**</span><span class="sxs-lookup"><span data-stu-id="c8f57-120">*FieldName* must be a valid field name from the **Recordset**.</span></span> <span data-ttu-id="c8f57-121">Если имя поля содержит пробелы, необходимо включить имя в квадратные скобки.</span><span class="sxs-lookup"><span data-stu-id="c8f57-121">If the field name contains spaces, you must enclose the name in square brackets.</span></span>

  - <span data-ttu-id="c8f57-122">*Оператор* должен быть одним из следующих: \<, \> \<=, \> =, \<\> =, =, или **LIKE**.</span><span class="sxs-lookup"><span data-stu-id="c8f57-122">*Operator* must be one of the following: \<, \>, \<=, \>=, \<\>, =, or **LIKE**.</span></span>

  - <span data-ttu-id="c8f57-123">*Значение* — это значение, с которым вы будете сравнивать значения поля (например, "Smith", \# 8/24/95, \# 12.345 или $50.00).</span><span class="sxs-lookup"><span data-stu-id="c8f57-123">*Value* is the value with which you will compare the field values (for example, 'Smith', \#8/24/95\#, 12.345, or $50.00).</span></span> <span data-ttu-id="c8f57-124">Используйте одиночные кавычка со строками и знаками фунта \# () с датами.</span><span class="sxs-lookup"><span data-stu-id="c8f57-124">Use single quotes with strings and pound signs (\#) with dates.</span></span> <span data-ttu-id="c8f57-125">Для чисел можно использовать десятичных точек, знаки доллара и научные нотации.</span><span class="sxs-lookup"><span data-stu-id="c8f57-125">For numbers, you can use decimal points, dollar signs, and scientific notation.</span></span> <span data-ttu-id="c8f57-126">Если *оператор* **является LIKE,** *значение может* использовать подкарды.</span><span class="sxs-lookup"><span data-stu-id="c8f57-126">If *Operator* is **LIKE**, *Value* can use wildcards.</span></span> <span data-ttu-id="c8f57-127">Только знак звездочки \* () и процентный знак (%) wild cards are allowed, and they must be the last character in the string.</span><span class="sxs-lookup"><span data-stu-id="c8f57-127">Only the asterisk (\*) and percent sign (%) wild cards are allowed, and they must be the last character in the string.</span></span> <span data-ttu-id="c8f57-128">*Значение* не может быть null.</span><span class="sxs-lookup"><span data-stu-id="c8f57-128">*Value* cannot be null.</span></span>

    > [!NOTE]
    > <span data-ttu-id="c8f57-129">Чтобы включить одиночные кавычка (') в значение фильтра, используйте два одиночных кавычка для представления одного.</span><span class="sxs-lookup"><span data-stu-id="c8f57-129">To include single quotation marks (') in the filter Value, use two single quotation marks to represent one.</span></span> <span data-ttu-id="c8f57-130">Например, чтобы фильтровать O'Malley, строка критериев должна быть "col1 = "O'Malley"".</span><span class="sxs-lookup"><span data-stu-id="c8f57-130">For example, to filter on O'Malley, the criteria string should be "col1 = 'O''Malley'".</span></span> <span data-ttu-id="c8f57-131">Чтобы включить одиночные кавычка как в начале, так и в конце значения фильтра, заключив строку с знаками фунта (#).</span><span class="sxs-lookup"><span data-stu-id="c8f57-131">To include single quotation marks at both the beginning and the end of the filter value, enclose the string with pound signs (#).</span></span> <span data-ttu-id="c8f57-132">Например, чтобы отфильтровать строку "1", строка критериев должна быть "col1 = #'1'#".</span><span class="sxs-lookup"><span data-stu-id="c8f57-132">For example, to filter on '1', the criteria string should be "col1 = #'1'#".</span></span>

-   <span data-ttu-id="c8f57-133">Между AND и **OR** нет **приоритета.**</span><span class="sxs-lookup"><span data-stu-id="c8f57-133">There is no precedence between **AND** and **OR**.</span></span> <span data-ttu-id="c8f57-134">Клаузула можно сгруппить в скобки.</span><span class="sxs-lookup"><span data-stu-id="c8f57-134">Clauses can be grouped within parentheses.</span></span> <span data-ttu-id="c8f57-135">Однако нельзя группировать клаузули, к которые присоединяется **or,** а затем присоединяться к группе к другому пункту с **И,** как в следующем фрагменте кода:</span><span class="sxs-lookup"><span data-stu-id="c8f57-135">However, you cannot group clauses joined by an **OR** and then join the group to another clause with an **AND**, as in the following code snippet:</span></span>  
 `(LastName = 'Smith' OR LastName = 'Jones') AND FirstName = 'John'`  
  
-   <span data-ttu-id="c8f57-136">Вместо этого можно создать этот фильтр в качестве</span><span class="sxs-lookup"><span data-stu-id="c8f57-136">Instead, you would construct this filter as</span></span>  
 `(LastName = 'Smith' AND FirstName = 'John') OR (LastName = 'Jones' AND FirstName = 'John')`  

  - <span data-ttu-id="c8f57-137">В пункте **LIKE** можно использовать под диктовку в начале и конце шаблона (например, LastName Like ' mit'), или только в конце шаблона \* \* (например, LastName Like \* 'Smit').</span><span class="sxs-lookup"><span data-stu-id="c8f57-137">In a **LIKE** clause, you can use a wildcard at the beginning and end of the pattern (for example, LastName Like '\*mit\*'), or only at the end of the pattern (for example, LastName Like 'Smit\*').</span></span>

<span data-ttu-id="c8f57-138">Константы фильтра упрощают разрешение отдельных конфликтов записей в режиме пакетного обновления, позволяя просматривать, например, только те записи, которые были затронуты во время последнего вызова метода [UpdateBatch.](updatebatch-method-ado.md)</span><span class="sxs-lookup"><span data-stu-id="c8f57-138">The filter constants make it easier to resolve individual record conflicts during batch update mode by allowing you to view, for example, only those records that were affected during the last [UpdateBatch](updatebatch-method-ado.md) method call.</span></span>

<span data-ttu-id="c8f57-139">Сама настройка **свойства Filter** может привести к сбой из-за конфликта с данными( например, запись уже удалена другим пользователем).</span><span class="sxs-lookup"><span data-stu-id="c8f57-139">Setting the **Filter** property itself may fail because of a conflict with the underlying data (for example, a record has already been deleted by another user).</span></span> <span data-ttu-id="c8f57-140">В этом случае поставщик возвращает предупреждения в коллекцию [Ошибок,](errors-collection-ado.md) но не останавливает выполнение программы.</span><span class="sxs-lookup"><span data-stu-id="c8f57-140">In such a case, the provider returns warnings to the [Errors](errors-collection-ado.md) collection but does not halt program execution.</span></span> <span data-ttu-id="c8f57-141">Ошибка во время запуска возникает только в том случае, если во всех запрашиваемых записях имеются конфликты.</span><span class="sxs-lookup"><span data-stu-id="c8f57-141">A run-time error occurs only if there are conflicts on all the requested records.</span></span> <span data-ttu-id="c8f57-142">Используйте свойство [Status](status-property-ado-recordset.md) для обнаружения записей с конфликтами.</span><span class="sxs-lookup"><span data-stu-id="c8f57-142">Use the [Status](status-property-ado-recordset.md) property to locate records with conflicts.</span></span>

<span data-ttu-id="c8f57-143">Настройка свойства **Filter** для строки нулевой длины ("") имеет тот же эффект, что и использование **константы adFilterNone.**</span><span class="sxs-lookup"><span data-stu-id="c8f57-143">Setting the **Filter** property to a zero-length string ("") has the same effect as using the **adFilterNone** constant.</span></span>

<span data-ttu-id="c8f57-144">При **застановлении** свойства Filter текущая позиция записи перемещается к первой записи в отфильтрованной подмножество записей **в Наборе записей.**</span><span class="sxs-lookup"><span data-stu-id="c8f57-144">Whenever the **Filter** property is set, the current record position moves to the first record in the filtered subset of records in the **Recordset**.</span></span> <span data-ttu-id="c8f57-145">Аналогично, когда свойство **Filter** очищается, текущая позиция записи перемещается к первой записи в **Наборе записей.**</span><span class="sxs-lookup"><span data-stu-id="c8f57-145">Similarly, when the **Filter** property is cleared, the current record position moves to the first record in the **Recordset**.</span></span>

<span data-ttu-id="c8f57-146">Описание значений закладок, из которых можно создать массив для использования с свойством **Filter,** см. в свойстве [Bookmark.](bookmark-property-ado.md)</span><span class="sxs-lookup"><span data-stu-id="c8f57-146">See the [Bookmark](bookmark-property-ado.md) property for an explanation of bookmark values from which you can build an array to use with the **Filter** property.</span></span>

<span data-ttu-id="c8f57-147">Только **фильтры** в виде строк Критериев (например, OrderDate \> '12/31/1999') влияют на содержимое сохраняемого **наборов записей.**</span><span class="sxs-lookup"><span data-stu-id="c8f57-147">Only **Filters** in the form of Criteria Strings (e.g. OrderDate \> '12/31/1999') affect the contents of a persisted **Recordset**.</span></span> <span data-ttu-id="c8f57-148">**Фильтры,** созданные  с помощью массива закладок или с использованием значения **filterGroupEnum,** не влияют на содержимое сохраняемого Набор записей.</span><span class="sxs-lookup"><span data-stu-id="c8f57-148">**Filters** created with an Array of **Bookmarks** or using a value from the **FilterGroupEnum** will not affect the contents of the persisted Recordset.</span></span> <span data-ttu-id="c8f57-149">Эти правила применяются к **записям,** созданным с помощью курсоров на стороне клиента или сервера.</span><span class="sxs-lookup"><span data-stu-id="c8f57-149">These rules apply to **Recordsets** created with either client-side or server-side cursors.</span></span>

> [!NOTE]
> <span data-ttu-id="c8f57-150">При применении **флага adFilterPendingRecords** к фильтрованным и измененным набором записей в режиме пакетного обновления результат **recordset** пуст, если фильтрация была основана на ключевом поле таблицы с одним ключом, а изменение было сделано на значениях ключевого поля. </span><span class="sxs-lookup"><span data-stu-id="c8f57-150">When you apply the **adFilterPendingRecords** flag to a filtered and modified **Recordset** in the batch update mode, the resultant **Recordset** is empty if the filtering was based on the key field of a single-keyed table and the modification was made on the key field values.</span></span> <span data-ttu-id="c8f57-151">Результат **recordset не** будет пустым, если одно из следующих данных является верным:</span><span class="sxs-lookup"><span data-stu-id="c8f57-151">The resultant **Recordset** will be non-empty if one of the following is true:</span></span>
> - <span data-ttu-id="c8f57-152">Фильтрация была основана на неявных полях в таблице с одним ключом.</span><span class="sxs-lookup"><span data-stu-id="c8f57-152">The filtering was based on non-key fields in a single-keyed table.</span></span>
> - <span data-ttu-id="c8f57-153">Фильтрация основана на любых полях в таблице с несколькими ключами.</span><span class="sxs-lookup"><span data-stu-id="c8f57-153">The filtering was based on any fields in a multiple-keyed table.</span></span>
> - <span data-ttu-id="c8f57-154">Изменения были внесены на неключевых полях в таблице с одним ключом.</span><span class="sxs-lookup"><span data-stu-id="c8f57-154">Modifications were made on non-key fields in a single-keyed table.</span></span>
> - <span data-ttu-id="c8f57-155">Изменения были внесены в любые поля в таблице с несколькими ключами.</span><span class="sxs-lookup"><span data-stu-id="c8f57-155">Modifications were made on any fields in a multiple-keyed table.</span></span>

<span data-ttu-id="c8f57-156">В следующей таблице подводятся итоги воздействия **adFilterPendingRecords** в различных сочетаниях фильтрации и изменений.</span><span class="sxs-lookup"><span data-stu-id="c8f57-156">The following table summarizes the effects of **adFilterPendingRecords** in different combinations of filtering and modifications.</span></span> <span data-ttu-id="c8f57-157">В левом столбце показаны возможные изменения; Изменения могут быть внесены в любое из неявных полей, на ключевое поле в таблице с одним ключом или на любом из ключевых полей в таблице с несколькими ключами.</span><span class="sxs-lookup"><span data-stu-id="c8f57-157">The left column shows the possible modifications; modifications can be made on any of the non-keyed fields, on the key field in a single-keyed table, or on any of the key fields in a multiple-keyed table.</span></span> <span data-ttu-id="c8f57-158">В верхней строке показан критерий фильтрации; Фильтрация может быть основана на любом из ненаключевых полей, ключевом поле в таблице с одним ключом или любом из ключевых полей в таблице с несколькими ключами.</span><span class="sxs-lookup"><span data-stu-id="c8f57-158">The top row shows the filtering criterion; filtering can be based on any of the non-keyed fields, the key field in a single-keyed table, or any of the key fields in a multiple-keyed table.</span></span> <span data-ttu-id="c8f57-159">Пересекающиеся ячейки показывают результаты: + означает, что применение **adFilterPendingRecords** приводит к непустой **набору записей;** **-** означает пустой **Набор записей.**</span><span class="sxs-lookup"><span data-stu-id="c8f57-159">The intersecting cells show the results: + means that applying **adFilterPendingRecords** results in a non-empty **Recordset**; **-** means an empty **Recordset**.</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><br />
</p></th>
<th><p><span data-ttu-id="c8f57-160">Не клавиши</span><span class="sxs-lookup"><span data-stu-id="c8f57-160">Non keys</span></span></p></th>
<th><p><span data-ttu-id="c8f57-161">Одиночный ключ</span><span class="sxs-lookup"><span data-stu-id="c8f57-161">Single Key</span></span></p></th>
<th><p><span data-ttu-id="c8f57-162">Несколько ключей</span><span class="sxs-lookup"><span data-stu-id="c8f57-162">Multiple Keys</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c8f57-163">Не клавиши</span><span class="sxs-lookup"><span data-stu-id="c8f57-163">Non keys</span></span></p></td>
<td><p>+</p></td>
<td><p>+</p></td>
<td><p>+</p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c8f57-164">Одиночный ключ</span><span class="sxs-lookup"><span data-stu-id="c8f57-164">Single Key</span></span></p></td>
<td><p>+</p></td>
<td><p>-</p></td>
<td><p><span data-ttu-id="c8f57-165">Н/Д</span><span class="sxs-lookup"><span data-stu-id="c8f57-165">N/A</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c8f57-166">Несколько ключей</span><span class="sxs-lookup"><span data-stu-id="c8f57-166">Multiple Keys</span></span></p></td>
<td><p>+</p></td>
<td><p><span data-ttu-id="c8f57-167">Н/Д</span><span class="sxs-lookup"><span data-stu-id="c8f57-167">N/A</span></span></p></td>
<td><p>+</p></td>
</tr>
</tbody>
</table>


---
title: Свойство Filter (ADO)
TOCTitle: Filter property (ADO)
ms:assetid: 5abc528a-a6ee-34de-5d44-a3249194b0a0
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249314(v=office.15)
ms:contentKeyID: 48545053
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 8cc5153d851a4dc17ef690421d1080ddf91fc3bf
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32292477"
---
# <a name="filter-property-ado"></a><span data-ttu-id="50e84-102">Свойство Filter (ADO)</span><span class="sxs-lookup"><span data-stu-id="50e84-102">Filter property (ADO)</span></span>


<span data-ttu-id="50e84-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="50e84-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="50e84-104">Указывает фильтр для данных в [наборе записей](recordset-object-ado.md).</span><span class="sxs-lookup"><span data-stu-id="50e84-104">Indicates a filter for data in a [Recordset](recordset-object-ado.md).</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="50e84-105">Параметры и возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="50e84-105">Settings and return values</span></span>

<span data-ttu-id="50e84-106">Задает или возвращает значение **типа Variant** , которое может содержать один из следующих элементов:</span><span class="sxs-lookup"><span data-stu-id="50e84-106">Sets or returns a **Variant** value, which can contain one of the following:</span></span>

  - <span data-ttu-id="50e84-107">**Строка условий** — строка, сопоставленная с одним или несколькими отдельными операторами **and** **и or.**</span><span class="sxs-lookup"><span data-stu-id="50e84-107">**Criteria string** — a string made up of one or more individual clauses concatenated with **AND** or **OR** operators.</span></span>

  - <span data-ttu-id="50e84-108">**Массив закладок** — массив уникальных значений закладок, указывающий на записи в объекте **Recordset** .</span><span class="sxs-lookup"><span data-stu-id="50e84-108">**Array of bookmarks** — an array of unique bookmark values that point to records in the **Recordset** object.</span></span>

  - <span data-ttu-id="50e84-109">Значение [филтерграупенум](filtergroupenum.md) .</span><span class="sxs-lookup"><span data-stu-id="50e84-109">A [FilterGroupEnum](filtergroupenum.md) value.</span></span>

## <a name="remarks"></a><span data-ttu-id="50e84-110">Примечания</span><span class="sxs-lookup"><span data-stu-id="50e84-110">Remarks</span></span>

<span data-ttu-id="50e84-111">Используйте свойство **Filter** для выборочного отображения записей в объекте **Recordset** .</span><span class="sxs-lookup"><span data-stu-id="50e84-111">Use the **Filter** property to selectively screen out records in a **Recordset** object.</span></span> <span data-ttu-id="50e84-112">Отфильтрованный **набор записей** становится текущим курсором.</span><span class="sxs-lookup"><span data-stu-id="50e84-112">The filtered **Recordset** becomes the current cursor.</span></span> <span data-ttu-id="50e84-113">Затронуты другие свойства, возвращающие значения на основе текущего курсора, такие как [AbsolutePosition](absoluteposition-property-ado.md), [AbsolutePage](absolutepage-property-ado.md), [RecordCount](recordcount-property-ado.md)и [PageCount](pagecount-property-ado.md).</span><span class="sxs-lookup"><span data-stu-id="50e84-113">Other properties that return values based on the current cursor are affected, such as [AbsolutePosition](absoluteposition-property-ado.md), [AbsolutePage](absolutepage-property-ado.md), [RecordCount](recordcount-property-ado.md), and [PageCount](pagecount-property-ado.md).</span></span> <span data-ttu-id="50e84-114">Это связано с тем, что если задать для свойства **Filter** определенное значение, текущая запись будет перемещена в первую запись, которая соответствует новому значению.</span><span class="sxs-lookup"><span data-stu-id="50e84-114">This is because setting the **Filter** property to a specific value will move the current record to the first record that satisfies the new value.</span></span>

<span data-ttu-id="50e84-115">Строка условия состоит из предложений в виде " *fieldname-operator-value* " (например, "LastName = ' Smith ').</span><span class="sxs-lookup"><span data-stu-id="50e84-115">The criteria string is made up of clauses in the form *FieldName-Operator-Value* (for example, "LastName = 'Smith'").</span></span> <span data-ttu-id="50e84-116">Можно создавать составные предложения, объединяя отдельные предложения с **and** (например, "LastName = ' Smith ' и FirstName = ' John '") или **или** (например,).</span><span class="sxs-lookup"><span data-stu-id="50e84-116">You can create compound clauses by concatenating individual clauses with **AND** (for example, "LastName = 'Smith' AND FirstName = 'John'") or **OR** (for example, ").</span></span> <span data-ttu-id="50e84-117">Можно создавать составные предложения, объединяя отдельные предложения с **and** (например, "LastName = ' Smith ' и FirstName = ' John '") или **или** (например, "LastName = ' Smith ' или LastName = ' Иванов '").</span><span class="sxs-lookup"><span data-stu-id="50e84-117">You can create compound clauses by concatenating individual clauses with **AND** (for example, "LastName = 'Smith' AND FirstName = 'John'") or **OR** (for example, "LastName = 'Smith' OR LastName = 'Jones'").</span></span> <span data-ttu-id="50e84-118">Используйте следующие рекомендации для строк условий:</span><span class="sxs-lookup"><span data-stu-id="50e84-118">Use the following guidelines for criteria strings:</span></span>

  - <span data-ttu-id="50e84-119">Значение *fieldname* должно быть допустимым именем поля из **набора записей**.</span><span class="sxs-lookup"><span data-stu-id="50e84-119">*FieldName* must be a valid field name from the **Recordset**.</span></span> <span data-ttu-id="50e84-120">Если имя поля содержит пробелы, его необходимо заключить в квадратные скобки.</span><span class="sxs-lookup"><span data-stu-id="50e84-120">If the field name contains spaces, you must enclose the name in square brackets.</span></span>

  - <span data-ttu-id="50e84-121">*Оператор* должен быть одним из \<следующих:, \>, \<=, \>=, \< \>, = или **Like**.</span><span class="sxs-lookup"><span data-stu-id="50e84-121">*Operator* must be one of the following: \<, \>, \<=, \>=, \<\>, =, or **LIKE**.</span></span>

  - <span data-ttu-id="50e84-122">*Value* — это значение, с которым сравниваются значения полей (например, ' Smith ', \#8/24/95\#, 12,345 или $50,00).</span><span class="sxs-lookup"><span data-stu-id="50e84-122">*Value* is the value with which you will compare the field values (for example, 'Smith', \#8/24/95\#, 12.345, or $50.00).</span></span> <span data-ttu-id="50e84-123">Используйте одинарные кавычки со строками и\#знаками решетки () с датами.</span><span class="sxs-lookup"><span data-stu-id="50e84-123">Use single quotes with strings and pound signs (\#) with dates.</span></span> <span data-ttu-id="50e84-124">Для чисел можно использовать десятичные точки, знаки доллара и экспоненциальное представление.</span><span class="sxs-lookup"><span data-stu-id="50e84-124">For numbers, you can use decimal points, dollar signs, and scientific notation.</span></span> <span data-ttu-id="50e84-125">*Оператор* If имеет **такой вид**, *значение* может использовать подстановочные знаки.</span><span class="sxs-lookup"><span data-stu-id="50e84-125">If *Operator* is **LIKE**, *Value* can use wildcards.</span></span> <span data-ttu-id="50e84-126">Только звездочка (\*) и знак процента (%) подстановочные знаки разрешены, и они должны быть последними символами в строке.</span><span class="sxs-lookup"><span data-stu-id="50e84-126">Only the asterisk (\*) and percent sign (%) wild cards are allowed, and they must be the last character in the string.</span></span> <span data-ttu-id="50e84-127">*Значение* не может быть равно null.</span><span class="sxs-lookup"><span data-stu-id="50e84-127">*Value* cannot be null.</span></span>

    > [!NOTE]
    > <span data-ttu-id="50e84-128">Чтобы включить в значение фильтра одиночные кавычки ('), используйте два одинарных кавычка для обозначения одного.</span><span class="sxs-lookup"><span data-stu-id="50e84-128">To include single quotation marks (') in the filter Value, use two single quotation marks to represent one.</span></span> <span data-ttu-id="50e84-129">Например, для фильтрации по О'маллэй необходимо указать строку критерия "col1 = ' O ' ' Маллэй '".</span><span class="sxs-lookup"><span data-stu-id="50e84-129">For example, to filter on O'Malley, the criteria string should be "col1 = 'O''Malley'".</span></span> <span data-ttu-id="50e84-130">Чтобы включить одинарные кавычки в начале и конце значения фильтра, заключите строку в знаки фунта (#).</span><span class="sxs-lookup"><span data-stu-id="50e84-130">To include single quotation marks at both the beginning and the end of the filter value, enclose the string with pound signs (#).</span></span> <span data-ttu-id="50e84-131">Например, чтобы выполнить фильтрацию по "1", строка критериев должна иметь значение "col1 = #" 1 "#".</span><span class="sxs-lookup"><span data-stu-id="50e84-131">For example, to filter on '1', the criteria string should be "col1 = #'1'#".</span></span>

  - <span data-ttu-id="50e84-132">Нет приоритета между **and** и **or**.</span><span class="sxs-lookup"><span data-stu-id="50e84-132">There is no precedence between **AND** and **OR**.</span></span> <span data-ttu-id="50e84-133">Предложения можно группировать в круглые скобки.</span><span class="sxs-lookup"><span data-stu-id="50e84-133">Clauses can be grouped within parentheses.</span></span> <span data-ttu-id="50e84-134">Однако вы не можете группировать предложения, Соединенные с помощью оператора **or** , а затем присоединить группу к другому предложению с помощью оператора **and**, как показано ниже.</span><span class="sxs-lookup"><span data-stu-id="50e84-134">However, you cannot group clauses joined by an **OR** and then join the group to another clause with an **AND**, like this:</span></span>

  - <span data-ttu-id="50e84-135">Вместо этого этот фильтр создается как</span><span class="sxs-lookup"><span data-stu-id="50e84-135">Instead, you would construct this filter as</span></span>

  - <span data-ttu-id="50e84-136">В предложении **Like** можно использовать подстановочные знаки в начале и конце шаблона (например, LastName, например, "\*MIT\*") или только в конце шаблона (например, LastName, например, "Смит\*").</span><span class="sxs-lookup"><span data-stu-id="50e84-136">In a **LIKE** clause, you can use a wildcard at the beginning and end of the pattern (for example, LastName Like '\*mit\*'), or only at the end of the pattern (for example, LastName Like 'Smit\*').</span></span>

<span data-ttu-id="50e84-137">Константы фильтра упрощают устранение конфликтов отдельных записей во время пакетного обновления, позволяя просматривать, например, только те записи, которые были затронуты при последнем вызове метода [UpdateBatch](updatebatch-method-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="50e84-137">The filter constants make it easier to resolve individual record conflicts during batch update mode by allowing you to view, for example, only those records that were affected during the last [UpdateBatch](updatebatch-method-ado.md) method call.</span></span>

<span data-ttu-id="50e84-138">Установка свойства **Filter** может закончиться неуспешно из-за конфликта с базовыми данными (например, запись уже была удалена другим пользователем).</span><span class="sxs-lookup"><span data-stu-id="50e84-138">Setting the **Filter** property itself may fail because of a conflict with the underlying data (for example, a record has already been deleted by another user).</span></span> <span data-ttu-id="50e84-139">В этом случае поставщик возвращает предупреждения в коллекцию [Errors](errors-collection-ado.md) , но не прерывает выполнение программы.</span><span class="sxs-lookup"><span data-stu-id="50e84-139">In such a case, the provider returns warnings to the [Errors](errors-collection-ado.md) collection but does not halt program execution.</span></span> <span data-ttu-id="50e84-140">Ошибка во время выполнения возникает только в том случае, если имеются конфликты со всеми запрошенными записями.</span><span class="sxs-lookup"><span data-stu-id="50e84-140">A run-time error occurs only if there are conflicts on all the requested records.</span></span> <span data-ttu-id="50e84-141">Используйте свойство [Status](status-property-ado-recordset.md) для обнаружения записей с конфликтами.</span><span class="sxs-lookup"><span data-stu-id="50e84-141">Use the [Status](status-property-ado-recordset.md) property to locate records with conflicts.</span></span>

<span data-ttu-id="50e84-142">Установка свойства **Filter** для строки нулевой длины ("") имеет тот же последствия, что и использование константы **адфилтерноне** .</span><span class="sxs-lookup"><span data-stu-id="50e84-142">Setting the **Filter** property to a zero-length string ("") has the same effect as using the **adFilterNone** constant.</span></span>

<span data-ttu-id="50e84-143">Если задано свойство **Filter** , текущее положение текущей записи перемещается на первую запись в отфильтрованном подмножестве записей в **наборе**записей.</span><span class="sxs-lookup"><span data-stu-id="50e84-143">Whenever the **Filter** property is set, the current record position moves to the first record in the filtered subset of records in the **Recordset**.</span></span> <span data-ttu-id="50e84-144">Аналогично, когда свойство **Filter** очищается, положение текущей записи перемещается на первую запись в **наборе записей**.</span><span class="sxs-lookup"><span data-stu-id="50e84-144">Similarly, when the **Filter** property is cleared, the current record position moves to the first record in the **Recordset**.</span></span>

<span data-ttu-id="50e84-145">В свойстве [Bookmark](bookmark-property-ado.md) представлено описание значений закладок, из которых можно создать массив для использования со свойством **Filter** .</span><span class="sxs-lookup"><span data-stu-id="50e84-145">See the [Bookmark](bookmark-property-ado.md) property for an explanation of bookmark values from which you can build an array to use with the **Filter** property.</span></span>

<span data-ttu-id="50e84-146">Только **фильтры** в форме строк условий (например, OrderDate \> ' 12/31/1999 ') влияют на Содержимое материализованного **набора записей**.</span><span class="sxs-lookup"><span data-stu-id="50e84-146">Only **Filters** in the form of Criteria Strings (e.g. OrderDate \> '12/31/1999') affect the contents of a persisted **Recordset**.</span></span> <span data-ttu-id="50e84-147">**Фильтры** , созданные с помощью массива **закладок** или значения из **филтерграупенум** , не влияют на Содержимое материализованного набора записей.</span><span class="sxs-lookup"><span data-stu-id="50e84-147">**Filters** created with an Array of **Bookmarks** or using a value from the **FilterGroupEnum** will not affect the contents of the persisted Recordset.</span></span> <span data-ttu-id="50e84-148">Эти правила применяются к **наборам записей** , созданным с помощью клиентских или серверных курсоров.</span><span class="sxs-lookup"><span data-stu-id="50e84-148">These rules apply to **Recordsets** created with either client-side or server-side cursors.</span></span>

> [!NOTE]
> <span data-ttu-id="50e84-149">Когда вы примените флаг **адфилтерпендингрекордс** к отфильтрованному и измененному **набору записей** в режиме пакетного обновления, результирующий **набор записей** будет пустым, если фильтрация основана на ключевом поле таблицы с одним ключом, а для значений ключевых полей было изменено.</span><span class="sxs-lookup"><span data-stu-id="50e84-149">When you apply the **adFilterPendingRecords** flag to a filtered and modified **Recordset** in the batch update mode, the resultant **Recordset** is empty if the filtering was based on the key field of a single-keyed table and the modification was made on the key field values.</span></span> <span data-ttu-id="50e84-150">Результирующий **набор записей** не будет пустым, если выполняется одно из следующих условий:</span><span class="sxs-lookup"><span data-stu-id="50e84-150">The resultant **Recordset** will be non-empty if one of the following is true:</span></span>
> - <span data-ttu-id="50e84-151">Фильтрация основана на не ключевых полях в таблице с одним ключом.</span><span class="sxs-lookup"><span data-stu-id="50e84-151">The filtering was based on non-key fields in a single-keyed table.</span></span>
> - <span data-ttu-id="50e84-152">Фильтрация основана на полях в таблице с несколькими ключами.</span><span class="sxs-lookup"><span data-stu-id="50e84-152">The filtering was based on any fields in a multiple-keyed table.</span></span>
> - <span data-ttu-id="50e84-153">Изменения, внесенные в неключевые поля в таблице с одним ключом.</span><span class="sxs-lookup"><span data-stu-id="50e84-153">Modifications were made on non-key fields in a single-keyed table.</span></span>
> - <span data-ttu-id="50e84-154">Изменения были внесены в любые поля в таблице с несколькими ключами.</span><span class="sxs-lookup"><span data-stu-id="50e84-154">Modifications were made on any fields in a multiple-keyed table.</span></span>

<span data-ttu-id="50e84-155">В приведенной ниже таблице перечислены эффекты **адфилтерпендингрекордс** в различных сочетаниях фильтрации и модификаций.</span><span class="sxs-lookup"><span data-stu-id="50e84-155">The following table summarizes the effects of **adFilterPendingRecords** in different combinations of filtering and modifications.</span></span> <span data-ttu-id="50e84-156">В левом столбце показаны возможные изменения; можно вносить изменения в любые поля без ключей, в поле ключа в таблице с одним ключом или в любом из ключевых полей таблицы с несколькими ключами.</span><span class="sxs-lookup"><span data-stu-id="50e84-156">The left column shows the possible modifications; modifications can be made on any of the non-keyed fields, on the key field in a single-keyed table, or on any of the key fields in a multiple-keyed table.</span></span> <span data-ttu-id="50e84-157">В верхней строке отображается критерий фильтрации; Фильтрация может основываться на любом из полей без ключей, ключевое поле в таблице с одним ключом или любые ключевые поля в таблице с несколькими ключами.</span><span class="sxs-lookup"><span data-stu-id="50e84-157">The top row shows the filtering criterion; filtering can be based on any of the non-keyed fields, the key field in a single-keyed table, or any of the key fields in a multiple-keyed table.</span></span> <span data-ttu-id="50e84-158">В пересекающихся ячейках отображаются результаты: + означает, что результаты **адфилтерпендингрекордс** в непустой **набор записей**; **-** означает пустой **набор записей**.</span><span class="sxs-lookup"><span data-stu-id="50e84-158">The intersecting cells show the results: + means that applying **adFilterPendingRecords** results in a non-empty **Recordset**; **-** means an empty **Recordset**.</span></span>

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
<th><p><span data-ttu-id="50e84-159">Не ключи</span><span class="sxs-lookup"><span data-stu-id="50e84-159">Non keys</span></span></p></th>
<th><p><span data-ttu-id="50e84-160">Один ключ</span><span class="sxs-lookup"><span data-stu-id="50e84-160">Single Key</span></span></p></th>
<th><p><span data-ttu-id="50e84-161">Несколько ключей</span><span class="sxs-lookup"><span data-stu-id="50e84-161">Multiple Keys</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="50e84-162">Не ключи</span><span class="sxs-lookup"><span data-stu-id="50e84-162">Non keys</span></span></p></td>
<td><p>+</p></td>
<td><p>+</p></td>
<td><p>+</p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="50e84-163">Один ключ</span><span class="sxs-lookup"><span data-stu-id="50e84-163">Single Key</span></span></p></td>
<td><p>+</p></td>
<td><p>-</p></td>
<td><p><span data-ttu-id="50e84-164">Н/Д</span><span class="sxs-lookup"><span data-stu-id="50e84-164">N/A</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="50e84-165">Несколько ключей</span><span class="sxs-lookup"><span data-stu-id="50e84-165">Multiple Keys</span></span></p></td>
<td><p>+</p></td>
<td><p><span data-ttu-id="50e84-166">Н/Д</span><span class="sxs-lookup"><span data-stu-id="50e84-166">N/A</span></span></p></td>
<td><p>+</p></td>
</tr>
</tbody>
</table>


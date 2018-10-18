---
<span data-ttu-id="8afb9-101"><<<<<<< Название HEAD: TOCTitle свойство фильтра (ADO): свойство фильтра (ADO) === заголовок: фильтровать свойство (ADO) TOCTitle: фильтрации свойство (ADO)</span><span class="sxs-lookup"><span data-stu-id="8afb9-101"><<<<<<< HEAD title: Filter Property (ADO) TOCTitle: Filter Property (ADO) ======= title: Filter property (ADO) TOCTitle: Filter property (ADO)</span></span>
>>>>>>> <span data-ttu-id="8afb9-102">главные ms:assetid: 5abc528a-a6ee-34de-5d44-a3249194b0a0 ms:mtpsurl: https://msdn.microsoft.com/library/JJ249314(v=office.15) ms:contentKeyID: 48545053 ms.date: 09/18/2015 mtps_version: v=office.15</span><span class="sxs-lookup"><span data-stu-id="8afb9-102">master ms:assetid: 5abc528a-a6ee-34de-5d44-a3249194b0a0 ms:mtpsurl: https://msdn.microsoft.com/library/JJ249314(v=office.15) ms:contentKeyID: 48545053 ms.date: 09/18/2015 mtps_version: v=office.15</span></span>
---

<span data-ttu-id="8afb9-103"><<<<<<< HEAD</span><span class="sxs-lookup"><span data-stu-id="8afb9-103"><<<<<<< HEAD</span></span>
# <a name="filter-property-ado"></a><span data-ttu-id="8afb9-104">Filter Property (ADO)</span><span class="sxs-lookup"><span data-stu-id="8afb9-104">Filter Property (ADO)</span></span>
=======
# <a name="filter-property-ado"></a><span data-ttu-id="8afb9-105">Свойства фильтра (ADO)</span><span class="sxs-lookup"><span data-stu-id="8afb9-105">Filter property (ADO)</span></span>
>>>>>>> <span data-ttu-id="8afb9-106">master</span><span class="sxs-lookup"><span data-stu-id="8afb9-106">master</span></span>


<span data-ttu-id="8afb9-107">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="8afb9-107">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="8afb9-108">Указывает фильтр для данных в [набор записей](recordset-object-ado.md).</span><span class="sxs-lookup"><span data-stu-id="8afb9-108">Indicates a filter for data in a [Recordset](recordset-object-ado.md).</span></span>

<span data-ttu-id="8afb9-109"><<<<<<< HEAD</span><span class="sxs-lookup"><span data-stu-id="8afb9-109"><<<<<<< HEAD</span></span>
## <a name="settings-and-return-values"></a><span data-ttu-id="8afb9-110">Параметры и возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="8afb9-110">Settings and Return Values</span></span>
=======
## <a name="settings-and-return-values"></a><span data-ttu-id="8afb9-111">Параметры и возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="8afb9-111">Settings and return values</span></span>
>>>>>>> <span data-ttu-id="8afb9-112">master</span><span class="sxs-lookup"><span data-stu-id="8afb9-112">master</span></span>

<span data-ttu-id="8afb9-113">Задает или возвращает значение **типа Variant** , который может содержать один из следующих:</span><span class="sxs-lookup"><span data-stu-id="8afb9-113">Sets or returns a **Variant** value, which can contain one of the following:</span></span>

  - <span data-ttu-id="8afb9-114">**Строка условия** — string, состоящую из одного или нескольких отдельных предложений объединяется с операторами **AND** или **OR** .</span><span class="sxs-lookup"><span data-stu-id="8afb9-114">**Criteria string** — a string made up of one or more individual clauses concatenated with **AND** or **OR** operators.</span></span>

  - <span data-ttu-id="8afb9-115">**Массив закладки** — массив уникальный закладку значений текущего момента в записи в объекте **набора записей** .</span><span class="sxs-lookup"><span data-stu-id="8afb9-115">**Array of bookmarks** — an array of unique bookmark values that point to records in the **Recordset** object.</span></span>

  - <span data-ttu-id="8afb9-116">Значение [FilterGroupEnum](filtergroupenum.md) .</span><span class="sxs-lookup"><span data-stu-id="8afb9-116">A [FilterGroupEnum](filtergroupenum.md) value.</span></span>

## <a name="remarks"></a><span data-ttu-id="8afb9-117">Замечания</span><span class="sxs-lookup"><span data-stu-id="8afb9-117">Remarks</span></span>

<span data-ttu-id="8afb9-118">Используйте свойство **фильтра** выборочно пропускать записей в объекте **набора записей** .</span><span class="sxs-lookup"><span data-stu-id="8afb9-118">Use the **Filter** property to selectively screen out records in a **Recordset** object.</span></span> <span data-ttu-id="8afb9-119">Отфильтрованного **набора записей** становится курсора.</span><span class="sxs-lookup"><span data-stu-id="8afb9-119">The filtered **Recordset** becomes the current cursor.</span></span> <span data-ttu-id="8afb9-120">Другие свойства, возвращающие значения на основании текущей курсора влияет на, такие как [AbsolutePosition](absoluteposition-property-ado.md), [AbsolutePage](absolutepage-property-ado.md), [RecordCount](recordcount-property-ado.md)и [PageCount](pagecount-property-ado.md).</span><span class="sxs-lookup"><span data-stu-id="8afb9-120">Other properties that return values based on the current cursor are affected, such as [AbsolutePosition](absoluteposition-property-ado.md), [AbsolutePage](absolutepage-property-ado.md), [RecordCount](recordcount-property-ado.md), and [PageCount](pagecount-property-ado.md).</span></span> <span data-ttu-id="8afb9-121">Это связано с определенным значением свойства **фильтра** для первой записи, которая должна удовлетворять новое значение Перемещение текущей записи.</span><span class="sxs-lookup"><span data-stu-id="8afb9-121">This is because setting the **Filter** property to a specific value will move the current record to the first record that satisfies the new value.</span></span>

<span data-ttu-id="8afb9-122">Строка условия включает в себя предложений в форме *FieldName оператор значение* (например, «LastName = 'Smith»»).</span><span class="sxs-lookup"><span data-stu-id="8afb9-122">The criteria string is made up of clauses in the form *FieldName-Operator-Value* (for example, "LastName = 'Smith'").</span></span> <span data-ttu-id="8afb9-123">Можно создать составные предложения, объединив отдельных предложений с **AND** (, например «LastName = 'Smith» "и" FirstName = «John»») или **OR** (например, «).</span><span class="sxs-lookup"><span data-stu-id="8afb9-123">You can create compound clauses by concatenating individual clauses with **AND** (for example, "LastName = 'Smith' AND FirstName = 'John'") or **OR** (for example, ").</span></span> <span data-ttu-id="8afb9-124">Можно создать составные предложения, объединив отдельных предложений с **AND** (, например «LastName = 'Smith» "и" FirstName = «John»») или **OR** (, например «LastName = 'Smith» или LastName = «Jones»»).</span><span class="sxs-lookup"><span data-stu-id="8afb9-124">You can create compound clauses by concatenating individual clauses with **AND** (for example, "LastName = 'Smith' AND FirstName = 'John'") or **OR** (for example, "LastName = 'Smith' OR LastName = 'Jones'").</span></span> <span data-ttu-id="8afb9-125">Используйте следующие рекомендации для строк с типом условия:</span><span class="sxs-lookup"><span data-stu-id="8afb9-125">Use the following guidelines for criteria strings:</span></span>

  - <span data-ttu-id="8afb9-126">*FieldName* должно быть допустимое имя поля из **набора записей**.</span><span class="sxs-lookup"><span data-stu-id="8afb9-126">*FieldName* must be a valid field name from the **Recordset**.</span></span> <span data-ttu-id="8afb9-127">Если имя поля содержит пробелы, необходимо заключить имя в квадратные скобки.</span><span class="sxs-lookup"><span data-stu-id="8afb9-127">If the field name contains spaces, you must enclose the name in square brackets.</span></span>

  - <span data-ttu-id="8afb9-128">*Оператор* должно быть одно из следующих значений: \<, \>, \<=, \>=, \< \>, =, либо **как**.</span><span class="sxs-lookup"><span data-stu-id="8afb9-128">*Operator* must be one of the following: \<, \>, \<=, \>=, \<\>, =, or **LIKE**.</span></span>

  - <span data-ttu-id="8afb9-129">*Значение* — это значение, с которым будет сравнение значений полей (например, «Smith», \#8/24/95\#, 12.345 или $50,00).</span><span class="sxs-lookup"><span data-stu-id="8afb9-129">*Value* is the value with which you will compare the field values (for example, 'Smith', \#8/24/95\#, 12.345, or $50.00).</span></span> <span data-ttu-id="8afb9-130">Использовать одинарные кавычки, строк и символов (\#) с датами.</span><span class="sxs-lookup"><span data-stu-id="8afb9-130">Use single quotes with strings and pound signs (\#) with dates.</span></span> <span data-ttu-id="8afb9-131">Для номеров можно использовать десятичные, знак доллара и научное обозначение.</span><span class="sxs-lookup"><span data-stu-id="8afb9-131">For numbers, you can use decimal points, dollar signs, and scientific notation.</span></span> <span data-ttu-id="8afb9-132">Если *оператор* **как** *значение* можно использовать подстановочные знаки.</span><span class="sxs-lookup"><span data-stu-id="8afb9-132">If *Operator* is **LIKE**, *Value* can use wildcards.</span></span> <span data-ttu-id="8afb9-133">Только звездочки (\*) и знак процента (%) допускаются подстановочные, и они должны иметь последний символ в строке.</span><span class="sxs-lookup"><span data-stu-id="8afb9-133">Only the asterisk (\*) and percent sign (%) wild cards are allowed, and they must be the last character in the string.</span></span> <span data-ttu-id="8afb9-134">Не может иметь *значение* null.</span><span class="sxs-lookup"><span data-stu-id="8afb9-134">*Value* cannot be null.</span></span>
    

    > [!NOTE]
    > <P><span data-ttu-id="8afb9-135">Чтобы включить в фильтр значение одинарные кавычки ('), используйте одинарные кавычки для представления одного.</span><span class="sxs-lookup"><span data-stu-id="8afb9-135">To include single quotation marks (') in the filter Value, use two single quotation marks to represent one.</span></span> <span data-ttu-id="8afb9-136">Например, чтобы отфильтровать O'Malley, критерии строка должна быть «Столбец1 = "O'' Malley"».</span><span class="sxs-lookup"><span data-stu-id="8afb9-136">For example, to filter on O'Malley, the criteria string should be "col1 = 'O''Malley'".</span></span> <span data-ttu-id="8afb9-137">Для включения одинарные кавычки в начале и конце значение фильтра, заключите строку с знаки решетки (#).</span><span class="sxs-lookup"><span data-stu-id="8afb9-137">To include single quotation marks at both the beginning and the end of the filter value, enclose the string with pound signs (#).</span></span> <span data-ttu-id="8afb9-138">Например, чтобы отфильтровать "1", критерии строка должна быть «Столбец1 = # "1" #».</span><span class="sxs-lookup"><span data-stu-id="8afb9-138">For example, to filter on '1', the criteria string should be "col1 = #'1'#".</span></span></P>



  - <span data-ttu-id="8afb9-139">Нет приоритетах **и** и **или**.</span><span class="sxs-lookup"><span data-stu-id="8afb9-139">There is no precedence between **AND** and **OR**.</span></span> <span data-ttu-id="8afb9-140">Предложения можно разбить в скобки.</span><span class="sxs-lookup"><span data-stu-id="8afb9-140">Clauses can be grouped within parentheses.</span></span> <span data-ttu-id="8afb9-141">Тем не менее невозможно групповой предложений в состав **или** и затем присоединиться к группе на другое предложение с **AND**, следующим образом:</span><span class="sxs-lookup"><span data-stu-id="8afb9-141">However, you cannot group clauses joined by an **OR** and then join the group to another clause with an **AND**, like this:</span></span>

  - <span data-ttu-id="8afb9-142">Вместо этого можно построить этот фильтр как</span><span class="sxs-lookup"><span data-stu-id="8afb9-142">Instead, you would construct this filter as</span></span>

  - <span data-ttu-id="8afb9-143">В предложении **как** можно использовать подстановочный знак в начале и в конце сопоставляться с шаблоном (, например LastName Like '\*mit\*"), или только в конце сопоставляться с шаблоном (, например LastName Like" Smit\*").</span><span class="sxs-lookup"><span data-stu-id="8afb9-143">In a **LIKE** clause, you can use a wildcard at the beginning and end of the pattern (for example, LastName Like '\*mit\*'), or only at the end of the pattern (for example, LastName Like 'Smit\*').</span></span>

<span data-ttu-id="8afb9-144">Константы фильтра упростить конфликтов отдельных записей в режиме пакетного обновления, позволяя просматривать, к примеру, вызвать только записи, измененных во время последнего метода [UpdateBatch](updatebatch-method-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="8afb9-144">The filter constants make it easier to resolve individual record conflicts during batch update mode by allowing you to view, for example, only those records that were affected during the last [UpdateBatch](updatebatch-method-ado.md) method call.</span></span>

<span data-ttu-id="8afb9-145">Свойства **фильтра** самого могут завершиться с ошибкой из-за конфликта с базовыми данными (например, запись уже была удалена другим пользователем).</span><span class="sxs-lookup"><span data-stu-id="8afb9-145">Setting the **Filter** property itself may fail because of a conflict with the underlying data (for example, a record has already been deleted by another user).</span></span> <span data-ttu-id="8afb9-146">В этом случае поставщик возвращает предупреждений в коллекцию [ошибок](errors-collection-ado.md) , но не останавливается выполнение программы.</span><span class="sxs-lookup"><span data-stu-id="8afb9-146">In such a case, the provider returns warnings to the [Errors](errors-collection-ado.md) collection but does not halt program execution.</span></span> <span data-ttu-id="8afb9-147">Только в том случае, если все запрошенные записи конфликтуют возникает ошибка времени выполнения.</span><span class="sxs-lookup"><span data-stu-id="8afb9-147">A run-time error occurs only if there are conflicts on all the requested records.</span></span> <span data-ttu-id="8afb9-148">Используйте свойство [состояние](status-property-ado-recordset.md) для поиска записей с конфликтами.</span><span class="sxs-lookup"><span data-stu-id="8afb9-148">Use the [Status](status-property-ado-recordset.md) property to locate records with conflicts.</span></span>

<span data-ttu-id="8afb9-149">Свойства **фильтра** в строку нулевой длины ("») имеет тот же эффект, что и использование **adFilterNone** константу.</span><span class="sxs-lookup"><span data-stu-id="8afb9-149">Setting the **Filter** property to a zero-length string ("") has the same effect as using the **adFilterNone** constant.</span></span>

<span data-ttu-id="8afb9-150">При использовании свойства **фильтра** , в настоящее время записи перемещает первой записи в отфильтрованное подмножество записей в **набора записей**.</span><span class="sxs-lookup"><span data-stu-id="8afb9-150">Whenever the **Filter** property is set, the current record position moves to the first record in the filtered subset of records in the **Recordset**.</span></span> <span data-ttu-id="8afb9-151">Аналогично Если свойство **Фильтр** установлен, положение текущей записи перемещает первой записи в **набор записей**.</span><span class="sxs-lookup"><span data-stu-id="8afb9-151">Similarly, when the **Filter** property is cleared, the current record position moves to the first record in the **Recordset**.</span></span>

<span data-ttu-id="8afb9-152">В разделе свойства [Bookmark](bookmark-property-ado.md) описание закладку значения, из которых можно создавать массивы для использования с помощью свойства **фильтра** .</span><span class="sxs-lookup"><span data-stu-id="8afb9-152">See the [Bookmark](bookmark-property-ado.md) property for an explanation of bookmark values from which you can build an array to use with the **Filter** property.</span></span>

<span data-ttu-id="8afb9-153">Только **фильтры** в виде строки критерии (например OrderDate \> "12/31/1999") влияет на содержимое постоянных **набора записей**.</span><span class="sxs-lookup"><span data-stu-id="8afb9-153">Only **Filters** in the form of Criteria Strings (e.g. OrderDate \> '12/31/1999') affect the contents of a persisted **Recordset**.</span></span> <span data-ttu-id="8afb9-154">**Фильтры** , созданные с помощью массива **закладки** или с использованием значения из **FilterGroupEnum** не влияет на содержимое постоянных набора записей.</span><span class="sxs-lookup"><span data-stu-id="8afb9-154">**Filters** created with an Array of **Bookmarks** or using a value from the **FilterGroupEnum** will not affect the contents of the persisted Recordset.</span></span> <span data-ttu-id="8afb9-155">Эти правила применяются к **наборов записей** , созданных с помощью курсоры со стороны клиента или на сервере.</span><span class="sxs-lookup"><span data-stu-id="8afb9-155">These rules apply to **Recordsets** created with either client-side or server-side cursors.</span></span>


> [!NOTE]
> <P><span data-ttu-id="8afb9-156">При применении флаг <STRONG>adFilterPendingRecords</STRONG> отфильтрованные и изменения <STRONG>записей</STRONG> в пакетном режиме обновления результирующего <STRONG>набора записей</STRONG> пуст, если фильтрация основана на ключевое поле с ключом одной таблицы, и была изменения внесены значений ключевых полей.</span><span class="sxs-lookup"><span data-stu-id="8afb9-156">When you apply the <STRONG>adFilterPendingRecords</STRONG> flag to a filtered and modified <STRONG>Recordset</STRONG> in the batch update mode, the resultant <STRONG>Recordset</STRONG> is empty if the filtering was based on the key field of a single-keyed table and the modification was made on the key field values.</span></span> <span data-ttu-id="8afb9-157">Результирующий <STRONG>набор записей</STRONG> будет пустым при выполнении одного из следующих:</span><span class="sxs-lookup"><span data-stu-id="8afb9-157">The resultant <STRONG>Recordset</STRONG> will be non-empty if one of the following is true:</span></span></P>



  - <span data-ttu-id="8afb9-158">Фильтрация была основанный на полях не ключи в таблице манипуляции single.</span><span class="sxs-lookup"><span data-stu-id="8afb9-158">The filtering was based on non-key fields in a single-keyed table.</span></span>

  - <span data-ttu-id="8afb9-159">Фильтрация была на основе всех полей в таблице несколько манипуляции.</span><span class="sxs-lookup"><span data-stu-id="8afb9-159">The filtering was based on any fields in a multiple-keyed table.</span></span>

  - <span data-ttu-id="8afb9-160">Изменения были внесены на полях не ключи в таблице манипуляции single.</span><span class="sxs-lookup"><span data-stu-id="8afb9-160">Modifications were made on non-key fields in a single-keyed table.</span></span>

  - <span data-ttu-id="8afb9-161">На всех полей в таблице манипуляции несколькими внесены изменения.</span><span class="sxs-lookup"><span data-stu-id="8afb9-161">Modifications were made on any fields in a multiple-keyed table.</span></span>

<span data-ttu-id="8afb9-162">В следующей таблице перечислены эффекты **adFilterPendingRecords** в разные сочетания фильтрации и изменения.</span><span class="sxs-lookup"><span data-stu-id="8afb9-162">The following table summarizes the effects of **adFilterPendingRecords** in different combinations of filtering and modifications.</span></span> <span data-ttu-id="8afb9-163">В левом столбце отображаются возможные изменения. можно внести изменения на любой из полей не манипуляции, ключевое поле в таблице манипуляции single, либо на любое из ключевых поля в таблице манипуляции несколько.</span><span class="sxs-lookup"><span data-stu-id="8afb9-163">The left column shows the possible modifications; modifications can be made on any of the non-keyed fields, on the key field in a single-keyed table, or on any of the key fields in a multiple-keyed table.</span></span> <span data-ttu-id="8afb9-164">Верхняя строка показывает критерий фильтрации; Фильтрация может быть основана на любой из полей не манипуляции ключевое поле в таблице манипуляции single или любое из ключевых поля в таблице манипуляции несколько.</span><span class="sxs-lookup"><span data-stu-id="8afb9-164">The top row shows the filtering criterion; filtering can be based on any of the non-keyed fields, the key field in a single-keyed table, or any of the key fields in a multiple-keyed table.</span></span> <span data-ttu-id="8afb9-165">Пересекающиеся ячеек показывают результаты: + означает, что применение **adFilterPendingRecords** приводит к непустые **набора записей**; **-** означает, что пустые **набора записей**.</span><span class="sxs-lookup"><span data-stu-id="8afb9-165">The intersecting cells show the results: + means that applying **adFilterPendingRecords** results in a non-empty **Recordset**; **-** means an empty **Recordset**.</span></span>

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
<th><p><span data-ttu-id="8afb9-166">Не ключи</span><span class="sxs-lookup"><span data-stu-id="8afb9-166">Non keys</span></span></p></th>
<th><p><span data-ttu-id="8afb9-167">Один ключ</span><span class="sxs-lookup"><span data-stu-id="8afb9-167">Single Key</span></span></p></th>
<th><p><span data-ttu-id="8afb9-168">Несколько ключей</span><span class="sxs-lookup"><span data-stu-id="8afb9-168">Multiple Keys</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="8afb9-169">Не ключи</span><span class="sxs-lookup"><span data-stu-id="8afb9-169">Non keys</span></span></p></td>
<td><p>+</p></td>
<td><p>+</p></td>
<td><p>+</p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8afb9-170">Один ключ</span><span class="sxs-lookup"><span data-stu-id="8afb9-170">Single Key</span></span></p></td>
<td><p>+</p></td>
<td><p>-</p></td>
<td><p><span data-ttu-id="8afb9-171">Н/Д</span><span class="sxs-lookup"><span data-stu-id="8afb9-171">N/A</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8afb9-172">Несколько ключей</span><span class="sxs-lookup"><span data-stu-id="8afb9-172">Multiple Keys</span></span></p></td>
<td><p>+</p></td>
<td><p><span data-ttu-id="8afb9-173">Н/Д</span><span class="sxs-lookup"><span data-stu-id="8afb9-173">N/A</span></span></p></td>
<td><p>+</p></td>
</tr>
</tbody>
</table>


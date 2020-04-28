---
title: Работа с наборами записей
TOCTitle: Working with Recordsets
ms:assetid: 9cd52866-2738-8150-381c-eee0b8a6cd36
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249711(v=office.15)
ms:contentKeyID: 48546608
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 0d4b877b680c80a10067e19065facd4ce9e4819d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32305975"
---
# <a name="working-with-recordsets"></a><span data-ttu-id="eb950-102">Работа с наборами записей</span><span class="sxs-lookup"><span data-stu-id="eb950-102">Working with Recordsets</span></span>

<span data-ttu-id="eb950-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="eb950-103">**Applies to**: Access 2013, Office 2013</span></span> 

<span data-ttu-id="eb950-104">Объект **Recordset** содержит встроенные функции, позволяющие изменить порядок данных в результирующем наборе, чтобы найти определенную запись на основе предоставленных условий, а также оптимизировать эти операции поиска с помощью индексов.</span><span class="sxs-lookup"><span data-stu-id="eb950-104">The **Recordset** object has built-in features that make it possible for you to rearrange the order of the data in the result set, to search for a specific record based on criteria that you supply, and even to optimize those search operations using indexes.</span></span> <span data-ttu-id="eb950-105">Доступность этих функций зависит от поставщика и в некоторых случаях, таких как свойство [index](index-property-ado.md) — структура самого источника данных.</span><span class="sxs-lookup"><span data-stu-id="eb950-105">Whether these features are available for use depends on the provider and in some cases — such as that of the [Index](index-property-ado.md) property — the structure of the data source itself.</span></span>

## <a name="arranging-data"></a><span data-ttu-id="eb950-106">Упорядочение данных</span><span class="sxs-lookup"><span data-stu-id="eb950-106">Arranging data</span></span>

<span data-ttu-id="eb950-107">Часто наиболее эффективный способ упорядочивания данных в **наборе записей** заключается в указании предложения ORDER BY в команде SQL, используемой для возврата результатов.</span><span class="sxs-lookup"><span data-stu-id="eb950-107">Often, the most efficient way to order the data in your **Recordset** is by specifying an ORDER BY clause in the SQL command used to return results to it.</span></span> <span data-ttu-id="eb950-108">Однако может потребоваться изменить порядок данных в уже созданном **наборе записей** .</span><span class="sxs-lookup"><span data-stu-id="eb950-108">However, you might need to change the order of the data in a **Recordset** that has already been created.</span></span> <span data-ttu-id="eb950-109">С помощью свойства **Sort** можно установить порядок, в котором просматриваются строки **набора записей** .</span><span class="sxs-lookup"><span data-stu-id="eb950-109">You can use the **Sort** property to establish the order in which rows of a **Recordset** are traversed.</span></span> <span data-ttu-id="eb950-110">Кроме того, свойство **Filter** определяет, какие строки доступны при переборе строк.</span><span class="sxs-lookup"><span data-stu-id="eb950-110">Furthermore, the **Filter** property determines which rows are accessible when traversing rows.</span></span>

<span data-ttu-id="eb950-111">Свойство **Sort** задает или возвращает **строковое** значение, которое указывает имена полей в **наборе записей** , по которому выполняется сортировка.</span><span class="sxs-lookup"><span data-stu-id="eb950-111">The **Sort** property sets or returns a **String** value that indicates the field names in the **Recordset** on which to sort.</span></span> <span data-ttu-id="eb950-112">Каждое имя отделяется запятой и при необходимости за ним следует пробел и ключевое слово **ASC** (то есть сортировка поля по возрастанию) или **DESC** (сортировка поля в убывающем порядке).</span><span class="sxs-lookup"><span data-stu-id="eb950-112">Each name is separated by a comma and is optionally followed by a space and the keyword **ASC** (which sorts the field in ascending order) or **DESC** (which sorts the field in descending order).</span></span> <span data-ttu-id="eb950-113">По умолчанию при условии, что ключевое слово не задано, поле сортируется в возрастающем порядке.</span><span class="sxs-lookup"><span data-stu-id="eb950-113">By default, if no keyword is specified, the field is sorted in ascending order.</span></span>

<span data-ttu-id="eb950-114">Операция сортировки эффективна, так как данные не переупорядочиваются физически, но доступ к ним осуществляется только в порядке, указанном индексом.</span><span class="sxs-lookup"><span data-stu-id="eb950-114">The sort operation is efficient because data is not physically rearranged but is simply accessed in the order specified by an index.</span></span>

<span data-ttu-id="eb950-115">Для свойства **Sort** необходимо задать для свойства [CursorLocation](cursorlocation-property-ado.md) значение **адусеклиент**.</span><span class="sxs-lookup"><span data-stu-id="eb950-115">The **Sort** property requires the [CursorLocation](cursorlocation-property-ado.md) property to be set to **adUseClient**.</span></span> <span data-ttu-id="eb950-116">Для каждого поля, указанного в свойстве **Sort** , будет создан временный индекс, если индекс еще не существует.</span><span class="sxs-lookup"><span data-stu-id="eb950-116">A temporary index will be created for each field specified in the **Sort** property if an index does not already exist.</span></span>

<span data-ttu-id="eb950-117">Если задать для свойства **Sort** пустую строку, строки будут сброшены в исходный порядок и удалять временные индексы.</span><span class="sxs-lookup"><span data-stu-id="eb950-117">Setting the **Sort** property to an empty string will reset the rows to their original order and delete temporary indexes.</span></span> <span data-ttu-id="eb950-118">Существующие индексы не будут удалены.</span><span class="sxs-lookup"><span data-stu-id="eb950-118">Existing indexes will not be deleted.</span></span>

<span data-ttu-id="eb950-119">Предположим, что объект **Recordset** содержит три поля с именами *FirstName*, *миддлеинитиал*и *LastName*.</span><span class="sxs-lookup"><span data-stu-id="eb950-119">Suppose a **Recordset** contains three fields named *firstName*, *middleInitial*, and *lastName*.</span></span> <span data-ttu-id="eb950-120">Задайте для свойства **Sort** строку "", которая будет упорядочивать **набор записей** по фамилии в убывающем порядке, а затем по имени по возрастанию.</span><span class="sxs-lookup"><span data-stu-id="eb950-120">Set the **Sort** property to the string "", which will order the **Recordset** by last name in descending order and then by first name in ascending order.</span></span> <span data-ttu-id="eb950-121">Посрединный инициал игнорируется.</span><span class="sxs-lookup"><span data-stu-id="eb950-121">The middle initial is ignored.</span></span>

<span data-ttu-id="eb950-122">Поля, на которые ссылается строка условий сортировки, не могут называться "ASC" или "DESC", так как эти имена конфликтуют с ключевыми словами **ASC** и **DESC**.</span><span class="sxs-lookup"><span data-stu-id="eb950-122">No field referenced in a sort criteria string can be named "ASC" or "DESC" because those names conflict with the keywords **ASC** and **DESC**.</span></span> <span data-ttu-id="eb950-123">Присвойте полю с конфликтующим именем псевдоним, используя ключевое слово **as** в запросе, возвращающем **набор записей**.</span><span class="sxs-lookup"><span data-stu-id="eb950-123">Give a field with a conflicting name an alias by using the **AS** keyword in the query that returns the **Recordset**.</span></span>

<span data-ttu-id="eb950-124">Более подробную информацию об фильтрации **наборов записей** можно узнать в статье фильтрация результатов в этой статье.</span><span class="sxs-lookup"><span data-stu-id="eb950-124">For more details about **Recordset** filtering, see Filtering the Results later in this topic.</span></span>

## <a name="finding-a-specific-record"></a><span data-ttu-id="eb950-125">Поиск определенной записи</span><span class="sxs-lookup"><span data-stu-id="eb950-125">Finding a specific record</span></span>

<span data-ttu-id="eb950-126">ADO предоставляет методы [поиска](find-method-ado.md) и [поиска](seek-method-ado.md) для поиска определенной записи в **наборе записей**.</span><span class="sxs-lookup"><span data-stu-id="eb950-126">ADO provides the [Find](find-method-ado.md) and [Seek](seek-method-ado.md) methods for locating a particular record in a **Recordset**.</span></span> <span data-ttu-id="eb950-127">Метод **Find** поддерживается различными поставщиками, но ограничен одним условием поиска.</span><span class="sxs-lookup"><span data-stu-id="eb950-127">The **Find** method is supported by a variety of providers but is limited to a single search criterion.</span></span> <span data-ttu-id="eb950-128">Метод **Seek** поддерживает поиск по нескольким условиям, но не поддерживается многими поставщиками.</span><span class="sxs-lookup"><span data-stu-id="eb950-128">The **Seek** method supports searching on multiple criteria, but is not supported by many providers.</span></span>

<span data-ttu-id="eb950-129">Индексы для полей могут значительно увеличить производительность метода **Find** объекта **Recordset** , а также свойства **сортировки** и **фильтрации** .</span><span class="sxs-lookup"><span data-stu-id="eb950-129">Indexes on fields can greatly enhance the performance of the **Recordset** object's **Find** method and **Sort** and **Filter** properties.</span></span> <span data-ttu-id="eb950-130">Вы можете создать внутренний индекс для объекта **field** , задав его динамическое свойство [optimize](optimize-property-dynamic-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="eb950-130">You can create an internal index for a **Field** object by setting its dynamic [Optimize](optimize-property-dynamic-ado.md) property.</span></span> <span data-ttu-id="eb950-131">Это динамическое свойство добавляется в коллекцию **свойств** объекта **field** , если для свойства [CursorLocation](cursorlocation-property-ado.md) задано значение **адусеклиент**.</span><span class="sxs-lookup"><span data-stu-id="eb950-131">This dynamic property is added to the **Field** object's **Properties** collection when you set the [CursorLocation](cursorlocation-property-ado.md) property to **adUseClient**.</span></span> <span data-ttu-id="eb950-132">Помните, что этот индекс является внутренним по отношению к ADO, поэтому вы не можете получить к нему доступ или использовать его для других целей.</span><span class="sxs-lookup"><span data-stu-id="eb950-132">Remember that this index is internal to ADO — you cannot gain access to it or use it for any other purpose.</span></span> <span data-ttu-id="eb950-133">Кроме того, этот индекс отличается от свойства [index](index-property-ado.md) объекта **Recordset** .</span><span class="sxs-lookup"><span data-stu-id="eb950-133">Also, this index is distinct from the **Recordset** object's [Index](index-property-ado.md) property.</span></span>

<span data-ttu-id="eb950-134">Метод **Find** быстро находит значение в столбце (поле) объекта **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="eb950-134">The **Find** method quickly locates a value within a column (field) of a **Recordset**.</span></span> <span data-ttu-id="eb950-135">Часто можно улучшить скорость операции метода **Find** для столбца с помощью свойства **optimize** для создания индекса.</span><span class="sxs-lookup"><span data-stu-id="eb950-135">You can often improve the speed of the **Find** method's operation on a column by using the **Optimize** property to create an index on it.</span></span>

<span data-ttu-id="eb950-136">Метод **Find** позволяет ограничить поиск содержимым одного поля.</span><span class="sxs-lookup"><span data-stu-id="eb950-136">The **Find** method limits your search to the contents of one field.</span></span> <span data-ttu-id="eb950-137">Метод **Seek** требует наличия индекса и имеет также и другие ограничения.</span><span class="sxs-lookup"><span data-stu-id="eb950-137">The **Seek** method requires that you have an index and has other limitations as well.</span></span> <span data-ttu-id="eb950-138">Если требуется выполнить поиск по нескольким полям, не являющимся основой для индекса, или если поставщик не поддерживает индексы, вы можете ограничить результаты с помощью свойства **Filter** объекта **Recordset** .</span><span class="sxs-lookup"><span data-stu-id="eb950-138">If you need to search on multiple fields that aren't the basis of an index, or if your provider does not support indexes, you can limit your results using the **Filter** property of the **Recordset** object.</span></span>

### <a name="find"></a><span data-ttu-id="eb950-139">Найти</span><span class="sxs-lookup"><span data-stu-id="eb950-139">Find</span></span>

<span data-ttu-id="eb950-140">Метод **Find** выполняет поиск строки, удовлетворяющей заданному условию, в **наборе записей** .</span><span class="sxs-lookup"><span data-stu-id="eb950-140">The **Find** method searches a **Recordset** for the row that satisfies a specified criterion.</span></span> <span data-ttu-id="eb950-141">При необходимости можно указать направление поиска, начальную строку и смещение из начальной строки.</span><span class="sxs-lookup"><span data-stu-id="eb950-141">Optionally, the direction of the search, starting row, and offset from the starting row may be specified.</span></span> <span data-ttu-id="eb950-142">Если условие выполнено, для найденной записи задается текущая позиция строки; в противном случае в качестве положения задается конец (или начало) **набора записей**в зависимости от направления поиска.</span><span class="sxs-lookup"><span data-stu-id="eb950-142">If the criterion is met, the current row position is set on the found record; otherwise, the position is set to the end (or start) of the **Recordset**, depending on search direction.</span></span>

<span data-ttu-id="eb950-143">Для этого критерия можно указать только одно имя столбца.</span><span class="sxs-lookup"><span data-stu-id="eb950-143">Only a single-column name may be specified for the criterion.</span></span> <span data-ttu-id="eb950-144">Другими словами, этот метод не поддерживает поиск по нескольким столбцам.</span><span class="sxs-lookup"><span data-stu-id="eb950-144">In other words, this method does not support multi-column searches.</span></span>

<span data-ttu-id="eb950-145">Оператор сравнения для критерия может иметь значение "**\>**" (больше),**\<**"" (меньше), "=" (равно), "\>=" (больше или равно), "\<=" (меньше или равно), "\<\>" (не равно) или "Like" (сопоставление по шаблону).</span><span class="sxs-lookup"><span data-stu-id="eb950-145">The comparison operator for the criterion may be "**\>**" (greater than), "**\<**" (less than), "=" (equal), "\>=" (greater than or equal), "\<=" (less than or equal), "\<\>" (not equal), or "LIKE" (pattern matching).</span></span>

<span data-ttu-id="eb950-146">Значение критерия может быть строкой, числом с плавающей запятой или датой.</span><span class="sxs-lookup"><span data-stu-id="eb950-146">The criterion value may be a string, floating-point number, or date.</span></span> <span data-ttu-id="eb950-147">Строковые значения разделяются символами одинарных\#кавычек или "" (знак номера) (например, "State = ' WA '" или "State \#=\#WA").</span><span class="sxs-lookup"><span data-stu-id="eb950-147">String values are delimited with single quotes or "\#" (number sign) marks (for example, "state = 'WA'" or "state = \#WA\#").</span></span> <span data-ttu-id="eb950-148">Значения дат разделяются знаками\#"" (знак номера) (например\_, "Дата \> \#начала 7/22/97\#").</span><span class="sxs-lookup"><span data-stu-id="eb950-148">Date values are delimited with "\#" (number sign) marks (for example, "start\_date \> \#7/22/97\#").</span></span>

<span data-ttu-id="eb950-149">Если оператор сравнения "Like", строковое значение может содержать звездочку (\*), чтобы найти один или несколько вхождений любого знака или подстроки.</span><span class="sxs-lookup"><span data-stu-id="eb950-149">If the comparison operator is "like", the string value may contain an asterisk (\*) to find one or more occurrences of any character or substring.</span></span> <span data-ttu-id="eb950-150">Например, "State Like m\*" соответствует Мэн и Массачусетс.</span><span class="sxs-lookup"><span data-stu-id="eb950-150">For example, "state like 'M\*'" matches Maine and Massachusetts.</span></span> <span data-ttu-id="eb950-151">Кроме того, можно использовать ведущие и замыкающие звездочки, чтобы найти подстроку, содержащуюся в значениях.</span><span class="sxs-lookup"><span data-stu-id="eb950-151">You can also use leading and trailing asterisks to find a substring contained within the values.</span></span> <span data-ttu-id="eb950-152">Например, "состояние, например"\*как\*", соответствует" Аляска "," Арканзас "и Массачусетс.</span><span class="sxs-lookup"><span data-stu-id="eb950-152">For example, "state like '\*as\*'" matches Alaska, Arkansas, and Massachusetts.</span></span>

<span data-ttu-id="eb950-153">Звездочки можно использовать только в конце строки условий, а также в начале и конце строки условий, как показано выше.</span><span class="sxs-lookup"><span data-stu-id="eb950-153">Asterisks can be used only at the end of a criteria string or together at both the beginning and end of a criteria string, as shown above.</span></span> <span data-ttu-id="eb950-154">Вы не можете использовать звездочку в качестве начального подстановочного\*знака ("str") или внедренного подстановочного знака ("\*r").</span><span class="sxs-lookup"><span data-stu-id="eb950-154">You cannot use the asterisk as a leading wildcard ('\*str') or embedded wildcard ('s\*r').</span></span> <span data-ttu-id="eb950-155">Это приведет к ошибке.</span><span class="sxs-lookup"><span data-stu-id="eb950-155">This will cause an error.</span></span>

### <a name="seek-and-index"></a><span data-ttu-id="eb950-156">Поиск и индексирование</span><span class="sxs-lookup"><span data-stu-id="eb950-156">Seek and Index</span></span>

<span data-ttu-id="eb950-157">Используйте метод **Seek** вместе со свойством **index** , если базовый поставщик поддерживает индексы для объекта **Recordset** .</span><span class="sxs-lookup"><span data-stu-id="eb950-157">Use the **Seek** method in conjunction with the **Index** property if the underlying provider supports indexes on the **Recordset** object.</span></span> <span data-ttu-id="eb950-158">Используйте метод Supported **(адсик)** [, чтобы](supports-method-ado.md)определить, поддерживает ли базовый поставщик **Поиск**, и метод **поддержки (адиндекс)** , чтобы определить, поддерживает ли поставщик индексы.</span><span class="sxs-lookup"><span data-stu-id="eb950-158">Use the [Supports](supports-method-ado.md)**(adSeek)** method to determine whether the underlying provider supports **Seek**, and the **Supports(adIndex)** method to determine whether the provider supports indexes.</span></span> <span data-ttu-id="eb950-159">(Например, [поставщик OLE DB для Microsoft Jet](microsoft-ole-db-provider-for-microsoft-jet.md) поддерживает **Поиск** и **индексирование**.)</span><span class="sxs-lookup"><span data-stu-id="eb950-159">(For example, the [OLE DB Provider for Microsoft Jet](microsoft-ole-db-provider-for-microsoft-jet.md) supports **Seek** and **Index**.)</span></span>

<span data-ttu-id="eb950-160">Если **Seek** не находит нужную строку, ошибка не возникает, а строка располагается в конце **набора записей**.</span><span class="sxs-lookup"><span data-stu-id="eb950-160">If **Seek** does not find the desired row, no error occurs, and the row is positioned at the end of the **Recordset**.</span></span> <span data-ttu-id="eb950-161">Перед выполнением этого метода установите для свойства **index** нужный индекс.</span><span class="sxs-lookup"><span data-stu-id="eb950-161">Set the **Index** property to the desired index before executing this method.</span></span>

<span data-ttu-id="eb950-162">Этот метод поддерживается только с курсорами на стороне сервера.</span><span class="sxs-lookup"><span data-stu-id="eb950-162">This method is supported only with server-side cursors.</span></span> <span data-ttu-id="eb950-163">Поиск не поддерживается, если значение свойства [CursorLocation](cursorlocation-property-ado.md) объекта **Recordset** равно **адусеклиент**.</span><span class="sxs-lookup"><span data-stu-id="eb950-163">Seek is not supported when the **Recordset** object's [CursorLocation](cursorlocation-property-ado.md) property value is **adUseClient**.</span></span>

<span data-ttu-id="eb950-164">Этот метод можно использовать только в том случае, если объект **Recordset** открыт со значением [коммандтипинум](commandtypeenum.md) для **адкмдтабледирект**.</span><span class="sxs-lookup"><span data-stu-id="eb950-164">This method can be used only when the **Recordset** object has been opened with a [CommandTypeEnum](commandtypeenum.md) value of **adCmdTableDirect**.</span></span>

## <a name="filtering-the-results"></a><span data-ttu-id="eb950-165">Фильтрация результатов</span><span class="sxs-lookup"><span data-stu-id="eb950-165">Filtering the results</span></span>

<span data-ttu-id="eb950-166">Метод **Find** позволяет ограничить поиск содержимым одного поля.</span><span class="sxs-lookup"><span data-stu-id="eb950-166">The **Find** method limits your search to the contents of one field.</span></span> <span data-ttu-id="eb950-167">Метод **Seek** требует наличия индекса и имеет также и другие ограничения.</span><span class="sxs-lookup"><span data-stu-id="eb950-167">The **Seek** method requires that you have an index and has other limitations as well.</span></span> <span data-ttu-id="eb950-168">Если вам нужно выполнить поиск по нескольким полям, которые не основаны на индексе, или поставщик не поддерживает индексы, вы можете ограничить результаты с помощью свойства **Filter** объекта **Recordset** .</span><span class="sxs-lookup"><span data-stu-id="eb950-168">If you need to search on multiple fields that are not the basis of an index or if your provider does not support indexes, you can limit your results using the **Filter** property of the **Recordset** object.</span></span>

<span data-ttu-id="eb950-169">Используйте свойство **Filter** для выборочного отображения записей в объекте **Recordset** .</span><span class="sxs-lookup"><span data-stu-id="eb950-169">Use the **Filter** property to selectively screen out records in a **Recordset** object.</span></span> <span data-ttu-id="eb950-170">Отфильтрованный **набор записей** становится текущим курсором, что означает, что записи, которые не удовлетворяют условиям **фильтра** , не будут доступны в **наборе записей** до тех пор, пока **Фильтр** не будет удален.</span><span class="sxs-lookup"><span data-stu-id="eb950-170">The filtered **Recordset** becomes the current cursor, which means that records that do not satisfy the **Filter** criteria are not available in the **Recordset** until the **Filter** is removed.</span></span> <span data-ttu-id="eb950-171">Затронуты другие свойства, возвращающие значения на основе текущего курсора, такие как **AbsolutePosition**, **AbsolutePage**, **RecordCount**и **PageCount**.</span><span class="sxs-lookup"><span data-stu-id="eb950-171">Other properties that return values based on the current cursor are affected, such as **AbsolutePosition**, **AbsolutePage**, **RecordCount**, and **PageCount**.</span></span> <span data-ttu-id="eb950-172">Это связано с тем, что если задать для свойства **Filter** определенное значение, текущая запись будет перемещена в первую запись, которая соответствует новому значению.</span><span class="sxs-lookup"><span data-stu-id="eb950-172">This is because setting the **Filter** property to a specific value will move the current record to the first record that satisfies the new value.</span></span>

<span data-ttu-id="eb950-173">Свойство **Filter** принимает аргумент Variant.</span><span class="sxs-lookup"><span data-stu-id="eb950-173">The **Filter** property takes a variant argument.</span></span> <span data-ttu-id="eb950-174">Это значение представляет один из трех методов использования свойства **Filter** : строку условий, константу **филтерграупенум** или массив закладок.</span><span class="sxs-lookup"><span data-stu-id="eb950-174">This value represents one of three methods for using the **Filter** property: a criteria string, a **FilterGroupEnum** constant, or an array of bookmarks.</span></span> <span data-ttu-id="eb950-175">Дополнительные сведения приведены в статье фильтрация с использованием строки условий, фильтрации с использованием констант и фильтрации с помощью закладок далее в этом разделе.</span><span class="sxs-lookup"><span data-stu-id="eb950-175">For more information, see Filtering with a Criteria String, Filtering with a Constant, and Filtering with Bookmarks later in this topic.</span></span>

> [!NOTE]
> <span data-ttu-id="eb950-176">Если вы знаете данные, которые вы хотите выбрать, обычно более эффективно открыть объект **Recordset** с помощью оператора SQL, который эффективно фильтрует набор результатов, а не полагается на свойство **Filter** .</span><span class="sxs-lookup"><span data-stu-id="eb950-176">When you know the data you want to select, it is usually more efficient to open a **Recordset** with a SQL statement that effectively filters the result set, rather than relying on the **Filter** property.</span></span>

<span data-ttu-id="eb950-177">Чтобы удалить фильтр из **набора записей**, используйте константу **адфилтерноне** .</span><span class="sxs-lookup"><span data-stu-id="eb950-177">To remove a filter from a **Recordset**, use the **adFilterNone** constant.</span></span> <span data-ttu-id="eb950-178">Установка свойства **Filter** для строки нулевой длины ("") имеет тот же последствия, что и использование константы **адфилтерноне** .</span><span class="sxs-lookup"><span data-stu-id="eb950-178">Setting the **Filter** property to a zero-length string ("") has the same effect as using the **adFilterNone** constant.</span></span>

### <a name="filtering-with-a-criteria-string"></a><span data-ttu-id="eb950-179">Фильтрация с помощью строки условий</span><span class="sxs-lookup"><span data-stu-id="eb950-179">Filtering with a criteria string</span></span>

<span data-ttu-id="eb950-180">Строка условия состоит из предложений в *значении оператора "FieldName* " формы (например, "LastName = ' Smith ').</span><span class="sxs-lookup"><span data-stu-id="eb950-180">The criteria string is made up of clauses in the form *FieldName Operator Value* (for example, "LastName = 'Smith'").</span></span> <span data-ttu-id="eb950-181">Можно создавать составные предложения, объединяя отдельные предложения с AND (например, "LastName = ' Smith ' и FirstName = ' John '") и или (например,).</span><span class="sxs-lookup"><span data-stu-id="eb950-181">You can create compound clauses by concatenating individual clauses with AND (for example, "LastName = 'Smith' AND FirstName = 'John'") and OR (for example, ).</span></span> <span data-ttu-id="eb950-182">Можно создавать составные предложения, объединяя отдельные предложения с AND (например, "LastName = ' Smith ' и FirstName = ' John '"), а также (например, "LastName = ' Smith ' или LastName = ' Иванов ').</span><span class="sxs-lookup"><span data-stu-id="eb950-182">You can create compound clauses by concatenating individual clauses with AND (for example, "LastName = 'Smith' AND FirstName = 'John'") and OR (for example, "LastName = 'Smith' OR LastName = 'Jones'").</span></span> <span data-ttu-id="eb950-183">Используйте следующие рекомендации для строк условий:</span><span class="sxs-lookup"><span data-stu-id="eb950-183">Use the following guidelines for criteria strings:</span></span>

- <span data-ttu-id="eb950-184">Значение *fieldname* должно быть допустимым именем поля из **набора записей**.</span><span class="sxs-lookup"><span data-stu-id="eb950-184">*FieldName* must be a valid field name from the **Recordset**.</span></span> <span data-ttu-id="eb950-185">Если имя поля содержит пробелы, его необходимо заключить в квадратные скобки.</span><span class="sxs-lookup"><span data-stu-id="eb950-185">If the field name contains spaces, you must enclose the name in square brackets.</span></span>

- <span data-ttu-id="eb950-186">*Оператор* должен быть одним из \<следующих:, \>, \<=, \>=, \< \>, = или LIKE.</span><span class="sxs-lookup"><span data-stu-id="eb950-186">*Operator* must be one of the following: \<, \>, \<=, \>=, \<\>, =, or LIKE.</span></span>

- <span data-ttu-id="eb950-187">*Value* — это значение, с которым сравниваются значения полей (например, ' Smith ', \#8/24/95\#, 12,345 или $50,00).</span><span class="sxs-lookup"><span data-stu-id="eb950-187">*Value* is the value with which you will compare the field values (for example, 'Smith', \#8/24/95\#, 12.345, or $50.00).</span></span> <span data-ttu-id="eb950-188">Используйте одинарные кавычки (') со строками и знаками решетки (\#) с датами.</span><span class="sxs-lookup"><span data-stu-id="eb950-188">Use single quotation marks (') with strings and pound signs (\#) with dates.</span></span> <span data-ttu-id="eb950-189">Для чисел можно использовать десятичные точки, знаки доллара и экспоненциальное представление.</span><span class="sxs-lookup"><span data-stu-id="eb950-189">For numbers, you can use decimal points, dollar signs, and scientific notation.</span></span> <span data-ttu-id="eb950-190">*Оператор* If имеет такой вид, *значение* может использовать подстановочные знаки.</span><span class="sxs-lookup"><span data-stu-id="eb950-190">If *Operator* is LIKE, *Value* can use wildcards.</span></span> <span data-ttu-id="eb950-191">Только звездочка (\*) и знак процента (%) подстановочные знаки разрешены, и они должны быть последними символами в строке.</span><span class="sxs-lookup"><span data-stu-id="eb950-191">Only the asterisk (\*) and percent sign (%) wildcards are allowed, and they must be the last character in the string.</span></span> <span data-ttu-id="eb950-192">*Значение* не может быть равно null.</span><span class="sxs-lookup"><span data-stu-id="eb950-192">*Value* cannot be null.</span></span>
    
  > [!NOTE]
  > <span data-ttu-id="eb950-193">Чтобы включить в *значение*фильтра одиночные кавычки ('), используйте два одинарных кавычка для обозначения одного.</span><span class="sxs-lookup"><span data-stu-id="eb950-193">To include single quotation marks (') in the filter *Value*, use two single quotation marks to represent one.</span></span> <span data-ttu-id="eb950-194">Например, для фильтрации по *о'маллэй*необходимо указать строку критерия "col1 = ' O ' ' маллэй '".</span><span class="sxs-lookup"><span data-stu-id="eb950-194">For example, to filter on *O'Malley*, the criteria string should be "col1 = 'O''Malley'".</span></span> 
  > 
  > <span data-ttu-id="eb950-195">Чтобы включить одинарные кавычки в начале и конце значения фильтра, заключите строку в знаки фунта (#).</span><span class="sxs-lookup"><span data-stu-id="eb950-195">To include single quotation marks at both the beginning and the end of the filter value, enclose the string in pound signs (#).</span></span> <span data-ttu-id="eb950-196">Например, чтобы выполнить фильтрацию по *"1"*, строка критериев должна иметь значение "col1 = #" 1 "#".</span><span class="sxs-lookup"><span data-stu-id="eb950-196">For example, to filter on *'1'*, the criteria string should be "col1 = #'1'#".</span></span>

<span data-ttu-id="eb950-197">Нет приоритета между AND и OR.</span><span class="sxs-lookup"><span data-stu-id="eb950-197">There is no precedence between AND and OR.</span></span> <span data-ttu-id="eb950-198">Предложения можно группировать в круглые скобки.</span><span class="sxs-lookup"><span data-stu-id="eb950-198">Clauses can be grouped within parentheses.</span></span> <span data-ttu-id="eb950-199">Однако вы не можете группировать предложения, Соединенные с помощью оператора OR, а затем присоединить группу к другому предложению с помощью оператора AND, как показано ниже.</span><span class="sxs-lookup"><span data-stu-id="eb950-199">However, you cannot group clauses joined by an OR and then join the group to another clause with an AND, like this:</span></span>

```vb 
 
(LastName = 'Smith' OR LastName = 'Jones') AND FirstName = 'John' 
```

<span data-ttu-id="eb950-200">Вместо этого этот фильтр создается следующим образом:</span><span class="sxs-lookup"><span data-stu-id="eb950-200">Instead, you would construct this filter as:</span></span>

```vb 
 
(LastName = 'Smith' AND FirstName = 'John') OR (LastName = 'Jones' AND FirstName = 'John') 
```

<span data-ttu-id="eb950-201">В выражении LIKE можно использовать подстановочные знаки в начале и конце шаблона (например, LastName, например, "\*MIT\*") или только в конце шаблона (например, "Фамилия") или только в конце шаблона (например, LastName, например "Смит\*").</span><span class="sxs-lookup"><span data-stu-id="eb950-201">In a LIKE clause, you can use a wildcard at the beginning and end of the pattern (for example, LastName Like '\*mit\*') or only at the end of the pattern (for example, ) or only at the end of the pattern (for example, LastName Like 'Smit\*').</span></span>

### <a name="filtering-with-a-constant"></a><span data-ttu-id="eb950-202">Фильтрация с помощью константы</span><span class="sxs-lookup"><span data-stu-id="eb950-202">Filtering with a constant</span></span>

<span data-ttu-id="eb950-203">Для фильтрации **наборов записей**доступны следующие константы.</span><span class="sxs-lookup"><span data-stu-id="eb950-203">The following constants are available for filtering **Recordsets**.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="eb950-204">Константа</span><span class="sxs-lookup"><span data-stu-id="eb950-204">Constant</span></span></p></th>
<th><p><span data-ttu-id="eb950-205">Описание</span><span class="sxs-lookup"><span data-stu-id="eb950-205">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="eb950-206"><strong>адфилтераффектедрекордс</strong></span><span class="sxs-lookup"><span data-stu-id="eb950-206"><strong>adFilterAffectedRecords</strong></span></span></p></td>
<td><p><span data-ttu-id="eb950-207">Фильтры для просмотра записей, которые были применены при вызове последней функции <strong>удаления</strong>, повторной <strong>синхронизации</strong>, <strong>UpdateBatch</strong>или <strong>CancelBatch</strong> .</span><span class="sxs-lookup"><span data-stu-id="eb950-207">Filters for viewing only records effected by the last <strong>Delete</strong>, <strong>Resync</strong>, <strong>UpdateBatch</strong>, or <strong>CancelBatch</strong> call.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="eb950-208"><strong>адфилтерконфликтингрекордс</strong></span><span class="sxs-lookup"><span data-stu-id="eb950-208"><strong>adFilterConflictingRecords</strong></span></span></p></td>
<td><p><span data-ttu-id="eb950-209">Фильтры для просмотра записей, для которых не удалось выполнить Последнее пакетное обновление.</span><span class="sxs-lookup"><span data-stu-id="eb950-209">Filters for viewing the records that failed the last batch update.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="eb950-210"><strong>адфилтерфетчедрекордс</strong></span><span class="sxs-lookup"><span data-stu-id="eb950-210"><strong>adFilterFetchedRecords</strong></span></span></p></td>
<td><p><span data-ttu-id="eb950-211">Фильтры для просмотра записей в текущем кэше (то есть результаты последнего вызова для получения записей из базы данных).</span><span class="sxs-lookup"><span data-stu-id="eb950-211">Filters for viewing the records in the current cache — that is, the results of the last call to retrieve records from the database.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="eb950-212"><strong>адфилтерноне</strong></span><span class="sxs-lookup"><span data-stu-id="eb950-212"><strong>adFilterNone</strong></span></span></p></td>
<td><p><span data-ttu-id="eb950-213">Удаляет текущий фильтр и восстанавливает все записи для просмотра.</span><span class="sxs-lookup"><span data-stu-id="eb950-213">Removes the current filter and restores all records for viewing.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="eb950-214"><strong>адфилтерпендингрекордс</strong></span><span class="sxs-lookup"><span data-stu-id="eb950-214"><strong>adFilterPendingRecords</strong></span></span></p></td>
<td><p><span data-ttu-id="eb950-215">Фильтры для просмотра только тех записей, которые были изменены, но еще не отправлены на сервер.</span><span class="sxs-lookup"><span data-stu-id="eb950-215">Filters for viewing only records that have changed but have not yet been sent to the server.</span></span> <span data-ttu-id="eb950-216">Применяется только для режима пакетного обновления.</span><span class="sxs-lookup"><span data-stu-id="eb950-216">Applicable only for batch update mode.</span></span></p></td>
</tr>
</tbody>
</table>

<br/>

<span data-ttu-id="eb950-217">Константы фильтра упрощают устранение конфликтов отдельных записей во время пакетного обновления, позволяя просматривать, например, только те записи, которые были применены при последнем вызове метода **UpdateBatch** , как показано в следующем примере:</span><span class="sxs-lookup"><span data-stu-id="eb950-217">The filter constants make it easier to resolve individual record conflicts during batch update mode by allowing you to view, for example, only those records that were effected during the last **UpdateBatch** method call, as shown in the following example:</span></span>

```vb 
 
'BeginDeleteGroup 
    'add some bogus records 
    With objRs1 
        For i = 0 To 8 
            .AddNew 
            .Fields("CompanyName") = "Shipper Number " & i + 1 
            .Fields("Phone") = "(425) 555-000" & (i + 1) 
            .Update 
        Next i 
         
    're-connect & update 
        .ActiveConnection = GetNewConnection 
        .UpdateBatch 
         
    'filter on newly added records 
        .Filter = adFilterAffectedRecords 
        Debug.Print "Deleting the " & .RecordCount & _ 
                    " records you just added." 
         
    'delete the newly added bogus records 
        .Delete adAffectGroup 
        .Filter = adFilterNone 
        Debug.Print .RecordCount & " records remain." 
         
        .Close 
    End With 
'EndDeleteGroup 
```

### <a name="filtering-with-bookmarks"></a><span data-ttu-id="eb950-218">Фильтрация с помощью закладок</span><span class="sxs-lookup"><span data-stu-id="eb950-218">Filtering with bookmarks</span></span>

<span data-ttu-id="eb950-219">Наконец, можно передать массив вариантов закладок в свойство **Filter** .</span><span class="sxs-lookup"><span data-stu-id="eb950-219">Finally, you can pass a variant array of bookmarks to the **Filter** property.</span></span> <span data-ttu-id="eb950-220">Полученный курсор будет содержать только те записи, для которых в свойстве была передана закладка.</span><span class="sxs-lookup"><span data-stu-id="eb950-220">The resulting cursor will contain only those records whose bookmark was passed in to the property.</span></span> <span data-ttu-id="eb950-221">В следующем примере кода создается массив закладок из записей в **наборе записей** , где в поле *ProductName* задано значение "B".</span><span class="sxs-lookup"><span data-stu-id="eb950-221">The following code example creates an array of bookmarks from the records in a **Recordset** which have a "B" in the *ProductName* field.</span></span> <span data-ttu-id="eb950-222">Затем массив передается в свойство **Filter** и отображает сведения о итоговом отфильтрованном **наборе записей**.</span><span class="sxs-lookup"><span data-stu-id="eb950-222">It then passes the array to the **Filter** property and displays information about the resulting filtered **Recordset**.</span></span>

```vb 
 
'BeginFilterBkmk 
    Dim vBkmkArray() As Variant 
    Dim i As Integer 
 
    'Recordset created using "SELECT * FROM Products" as command. 
    'So, we will check to see if ProductName has a capital B, and 
    'if so, add to the array. 
    i = 0 
    Do While Not objRs.EOF 
        If InStr(1, objRs("ProductName"), "B") Then 
            ReDim Preserve vBkmkArray(i) 
            vBkmkArray(i) = objRs.Bookmark 
            i = i + 1 
            Debug.Print objRs("ProductName") 
        End If 
        objRs.MoveNext 
    Loop 
     
    'Filter using the array of bookmarks. 
    objRs.Filter = vBkmkArray 
     
    objRs.MoveFirst 
    Do While Not objRs.EOF 
        Debug.Print objRs("ProductName") 
        objRs.MoveNext 
    Loop 
    'EndFilterBkmk 
```

## <a name="creating-a-clone-of-a-recordset"></a><span data-ttu-id="eb950-223">Создание клона объекта Recordset</span><span class="sxs-lookup"><span data-stu-id="eb950-223">Creating a clone of a Recordset</span></span>

<span data-ttu-id="eb950-224">Используйте метод **clone** для создания нескольких дублирующихся объектов **Recordset** , в частности, если требуется поддерживать несколько текущих записей в заданном наборе записей.</span><span class="sxs-lookup"><span data-stu-id="eb950-224">Use the **Clone** method to create multiple, duplicate **Recordset** objects, particularly if you want to maintain more than one current record in a given set of records.</span></span> <span data-ttu-id="eb950-225">Использование метода **clone** является более эффективным, чем создание и открытие нового объекта **Recordset** с тем же определением, что и исходный.</span><span class="sxs-lookup"><span data-stu-id="eb950-225">Using the **Clone** method is more efficient than creating and opening a new **Recordset** object with the same definition as the original.</span></span>

<span data-ttu-id="eb950-226">Для текущей записи созданного клона изначально задается первая запись.</span><span class="sxs-lookup"><span data-stu-id="eb950-226">The current record of a newly created clone is originally set to the first record.</span></span> <span data-ttu-id="eb950-227">Указатель текущей записи в клонированном **наборе записей** не синхронизирован с исходным и наоборот.</span><span class="sxs-lookup"><span data-stu-id="eb950-227">The current record pointer in a cloned **Recordset** is not synchronized with the original or vice versa.</span></span> <span data-ttu-id="eb950-228">В каждом **наборе записей**можно перемещаться независимо друг от друга.</span><span class="sxs-lookup"><span data-stu-id="eb950-228">You can navigate independently in each **Recordset**.</span></span>

<span data-ttu-id="eb950-229">Изменения, вносимые в один объект **Recordset** , отображаются во всех клонах, независимо от типа курсора.</span><span class="sxs-lookup"><span data-stu-id="eb950-229">Changes you make to one **Recordset** object are visible in all of its clones regardless of cursor type.</span></span> <span data-ttu-id="eb950-230">Однако после выполнения командлета [Requery](requery-method-ado.md) для исходного объекта **Recordset**клоны больше не будут синхронизироваться с исходным.</span><span class="sxs-lookup"><span data-stu-id="eb950-230">However, after you execute [Requery](requery-method-ado.md) on the original **Recordset**, the clones will no longer be synchronized to the original.</span></span>

<span data-ttu-id="eb950-231">Закрытие исходного объекта **Recordset** не приводит к закрытию его копий, а также закрытию копии.</span><span class="sxs-lookup"><span data-stu-id="eb950-231">Closing the original **Recordset** does not close its copies, nor does closing a copy close the original or any of the other copies.</span></span>

<span data-ttu-id="eb950-232">Вы можете клонировать объект **Recordset** только в том случае, если он поддерживает закладки.</span><span class="sxs-lookup"><span data-stu-id="eb950-232">You can clone a **Recordset** object only if it supports bookmarks.</span></span> <span data-ttu-id="eb950-233">Значения закладок являются взаимозаменяемыми; то есть ссылка на закладку из одного объекта **Recordset** ссылается на одну и ту же запись в любом из его клонов.</span><span class="sxs-lookup"><span data-stu-id="eb950-233">Bookmark values are interchangeable; that is, a bookmark reference from one **Recordset** object refers to the same record in any of its clones.</span></span>


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
# <a name="working-with-recordsets"></a><span data-ttu-id="d06d5-102">Работа с наборами записей</span><span class="sxs-lookup"><span data-stu-id="d06d5-102">Working with Recordsets</span></span>

<span data-ttu-id="d06d5-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="d06d5-103">**Applies to**: Access 2013, Office 2013</span></span> 

<span data-ttu-id="d06d5-104">Объект **Recordset** имеет встроенные функции, которые делают возможным переупорядочение порядка данных в наборе результатов, поиск определенной записи на основе заставляемого критерия и даже для оптимизации этих операций поиска с помощью индексов.</span><span class="sxs-lookup"><span data-stu-id="d06d5-104">The **Recordset** object has built-in features that make it possible for you to rearrange the order of the data in the result set, to search for a specific record based on criteria that you supply, and even to optimize those search operations using indexes.</span></span> <span data-ttu-id="d06d5-105">То, доступны ли эти функции для использования, зависит от поставщика, а в некоторых случаях — например, от свойства [Index](index-property-ado.md) — от структуры самого источника данных.</span><span class="sxs-lookup"><span data-stu-id="d06d5-105">Whether these features are available for use depends on the provider and in some cases — such as that of the [Index](index-property-ado.md) property — the structure of the data source itself.</span></span>

## <a name="arranging-data"></a><span data-ttu-id="d06d5-106">Организация данных</span><span class="sxs-lookup"><span data-stu-id="d06d5-106">Arranging data</span></span>

<span data-ttu-id="d06d5-107">Часто наиболее эффективным способом упорядочения данных в наборе **записей** является указание предложения ORDER BY в команде SQL, используемой для возврата результатов в него.</span><span class="sxs-lookup"><span data-stu-id="d06d5-107">Often, the most efficient way to order the data in your **Recordset** is by specifying an ORDER BY clause in the SQL command used to return results to it.</span></span> <span data-ttu-id="d06d5-108">Однако может потребоваться изменить порядок данных в наборе **записей,** который уже был создан.</span><span class="sxs-lookup"><span data-stu-id="d06d5-108">However, you might need to change the order of the data in a **Recordset** that has already been created.</span></span> <span data-ttu-id="d06d5-109">Вы можете использовать свойство **Sort,** чтобы установить порядок прохода по строкам **объекта Recordset.**</span><span class="sxs-lookup"><span data-stu-id="d06d5-109">You can use the **Sort** property to establish the order in which rows of a **Recordset** are traversed.</span></span> <span data-ttu-id="d06d5-110">Кроме того, свойство **Filter** определяет, какие строки доступны при проходе по строкам.</span><span class="sxs-lookup"><span data-stu-id="d06d5-110">Furthermore, the **Filter** property determines which rows are accessible when traversing rows.</span></span>

<span data-ttu-id="d06d5-111">Свойство **Sort** задает или возвращает **строку,** которая указывает имена полей в **наборе записей,** по которому необходимо отсортировать.</span><span class="sxs-lookup"><span data-stu-id="d06d5-111">The **Sort** property sets or returns a **String** value that indicates the field names in the **Recordset** on which to sort.</span></span> <span data-ttu-id="d06d5-112">Каждое имя отделяется запятой, за которым при желании следует пробел и ключевое слово **ASC** (сортировать поле в порядке возрастания) или **DESC** (сортировать поле по убыванию).</span><span class="sxs-lookup"><span data-stu-id="d06d5-112">Each name is separated by a comma and is optionally followed by a space and the keyword **ASC** (which sorts the field in ascending order) or **DESC** (which sorts the field in descending order).</span></span> <span data-ttu-id="d06d5-113">По умолчанию, если ключевое слово не указано, поле сортироваться в порядке возрастания.</span><span class="sxs-lookup"><span data-stu-id="d06d5-113">By default, if no keyword is specified, the field is sorted in ascending order.</span></span>

<span data-ttu-id="d06d5-114">Операция сортировки эффективна, так как данные физически не переупорядочены, а просто доступны в порядке, указанном индексом.</span><span class="sxs-lookup"><span data-stu-id="d06d5-114">The sort operation is efficient because data is not physically rearranged but is simply accessed in the order specified by an index.</span></span>

<span data-ttu-id="d06d5-115">Свойство **Sort** требует, чтобы свойство [CursorLocation](cursorlocation-property-ado.md) было установлено в **adUseClient.**</span><span class="sxs-lookup"><span data-stu-id="d06d5-115">The **Sort** property requires the [CursorLocation](cursorlocation-property-ado.md) property to be set to **adUseClient**.</span></span> <span data-ttu-id="d06d5-116">Для каждого поля, указанного в свойстве **Sort,** будет создан временный индекс, если индекс еще не существует.</span><span class="sxs-lookup"><span data-stu-id="d06d5-116">A temporary index will be created for each field specified in the **Sort** property if an index does not already exist.</span></span>

<span data-ttu-id="d06d5-117">При **установке для** свойства Sort пустой строки строки сбрасываются в исходный порядок и удаляются временные индексы.</span><span class="sxs-lookup"><span data-stu-id="d06d5-117">Setting the **Sort** property to an empty string will reset the rows to their original order and delete temporary indexes.</span></span> <span data-ttu-id="d06d5-118">Существующие индексы не будут удалены.</span><span class="sxs-lookup"><span data-stu-id="d06d5-118">Existing indexes will not be deleted.</span></span>

<span data-ttu-id="d06d5-119">**Предположим, что набор записей** содержит три поля с именами *firstName,* *middleInitial* и *lastName.*</span><span class="sxs-lookup"><span data-stu-id="d06d5-119">Suppose a **Recordset** contains three fields named *firstName*, *middleInitial*, and *lastName*.</span></span> <span data-ttu-id="d06d5-120">Установите для **свойства Sort** строку "", которая упорядочение набора **записей** по фамилии по убыванию, а затем по имени в порядке возрастания.</span><span class="sxs-lookup"><span data-stu-id="d06d5-120">Set the **Sort** property to the string "", which will order the **Recordset** by last name in descending order and then by first name in ascending order.</span></span> <span data-ttu-id="d06d5-121">Средний инициал игнорируется.</span><span class="sxs-lookup"><span data-stu-id="d06d5-121">The middle initial is ignored.</span></span>

<span data-ttu-id="d06d5-122">Поля, на которые ссылается строка условий сортировки, не могут называться ASC или DESC, так как эти имена конфликтуют с ключевыми словами **ASC** и **DESC.**</span><span class="sxs-lookup"><span data-stu-id="d06d5-122">No field referenced in a sort criteria string can be named "ASC" or "DESC" because those names conflict with the keywords **ASC** and **DESC**.</span></span> <span data-ttu-id="d06d5-123">Придайте полю с конфликтующий именем псевдоним с помощью ключевого слова **AS** в запросе, возвращаемом **набором записей.**</span><span class="sxs-lookup"><span data-stu-id="d06d5-123">Give a field with a conflicting name an alias by using the **AS** keyword in the query that returns the **Recordset**.</span></span>

<span data-ttu-id="d06d5-124">Дополнительные сведения о **фильтрации наборов** записей см. в разделе "Фильтрация результатов" далее в этом разделе.</span><span class="sxs-lookup"><span data-stu-id="d06d5-124">For more details about **Recordset** filtering, see Filtering the Results later in this topic.</span></span>

## <a name="finding-a-specific-record"></a><span data-ttu-id="d06d5-125">Поиск определенной записи</span><span class="sxs-lookup"><span data-stu-id="d06d5-125">Finding a specific record</span></span>

<span data-ttu-id="d06d5-126">ADO предоставляет методы [Find](find-method-ado.md) и [Seek](seek-method-ado.md) для поиска определенной записи в **наборе записей.**</span><span class="sxs-lookup"><span data-stu-id="d06d5-126">ADO provides the [Find](find-method-ado.md) and [Seek](seek-method-ado.md) methods for locating a particular record in a **Recordset**.</span></span> <span data-ttu-id="d06d5-127">Метод **Find** поддерживается различными поставщиками, но ограничен одним критерием поиска.</span><span class="sxs-lookup"><span data-stu-id="d06d5-127">The **Find** method is supported by a variety of providers but is limited to a single search criterion.</span></span> <span data-ttu-id="d06d5-128">Метод **Seek** поддерживает поиск по нескольким критериям, но не поддерживается многими поставщиками.</span><span class="sxs-lookup"><span data-stu-id="d06d5-128">The **Seek** method supports searching on multiple criteria, but is not supported by many providers.</span></span>

<span data-ttu-id="d06d5-129">Индексы полей могут значительно повысить производительность методов Find объекта **Recordset** и **свойств Sort** и **Filter.** </span><span class="sxs-lookup"><span data-stu-id="d06d5-129">Indexes on fields can greatly enhance the performance of the **Recordset** object's **Find** method and **Sort** and **Filter** properties.</span></span> <span data-ttu-id="d06d5-130">Вы можете создать внутренний индекс для объекта **Field,** установив его динамическое [свойство Optimize.](optimize-property-dynamic-ado.md)</span><span class="sxs-lookup"><span data-stu-id="d06d5-130">You can create an internal index for a **Field** object by setting its dynamic [Optimize](optimize-property-dynamic-ado.md) property.</span></span> <span data-ttu-id="d06d5-131">Это динамическое свойство добавляется в  коллекцию **свойств** объекта Field при задав свойству [CursorLocation](cursorlocation-property-ado.md) свойство **adUseClient.**</span><span class="sxs-lookup"><span data-stu-id="d06d5-131">This dynamic property is added to the **Field** object's **Properties** collection when you set the [CursorLocation](cursorlocation-property-ado.md) property to **adUseClient**.</span></span> <span data-ttu-id="d06d5-132">Помните, что этот индекс является внутренним для ADO— вы не можете получить к нему доступ или использовать его для каких-либо других целей.</span><span class="sxs-lookup"><span data-stu-id="d06d5-132">Remember that this index is internal to ADO — you cannot gain access to it or use it for any other purpose.</span></span> <span data-ttu-id="d06d5-133">Кроме того, этот индекс отличается от свойства [Index](index-property-ado.md) объекта **Recordset.**</span><span class="sxs-lookup"><span data-stu-id="d06d5-133">Also, this index is distinct from the **Recordset** object's [Index](index-property-ado.md) property.</span></span>

<span data-ttu-id="d06d5-134">Метод **Find** быстро находит значение в столбце (поле) **recordset.**</span><span class="sxs-lookup"><span data-stu-id="d06d5-134">The **Find** method quickly locates a value within a column (field) of a **Recordset**.</span></span> <span data-ttu-id="d06d5-135">Часто можно повысить скорость работы метода **Find** со столбцом с помощью свойства **Optimize,** чтобы создать на нем индекс.</span><span class="sxs-lookup"><span data-stu-id="d06d5-135">You can often improve the speed of the **Find** method's operation on a column by using the **Optimize** property to create an index on it.</span></span>

<span data-ttu-id="d06d5-136">Метод **Find** ограничивает поиск содержимым одного поля.</span><span class="sxs-lookup"><span data-stu-id="d06d5-136">The **Find** method limits your search to the contents of one field.</span></span> <span data-ttu-id="d06d5-137">Метод **Seek** требует на то, чтобы у вас был индекс и есть другие ограничения.</span><span class="sxs-lookup"><span data-stu-id="d06d5-137">The **Seek** method requires that you have an index and has other limitations as well.</span></span> <span data-ttu-id="d06d5-138">Если требуется искать по нескольким полям, которые не являются основой индекса, или если поставщик не поддерживает индексы, можно ограничить результаты с помощью свойства **Filter** объекта **Recordset.**</span><span class="sxs-lookup"><span data-stu-id="d06d5-138">If you need to search on multiple fields that aren't the basis of an index, or if your provider does not support indexes, you can limit your results using the **Filter** property of the **Recordset** object.</span></span>

### <a name="find"></a><span data-ttu-id="d06d5-139">Найти</span><span class="sxs-lookup"><span data-stu-id="d06d5-139">Find</span></span>

<span data-ttu-id="d06d5-140">Метод **Find** выполняет поиск **в наборе записей** строки, которая удовлетворяет указанному критерию.</span><span class="sxs-lookup"><span data-stu-id="d06d5-140">The **Find** method searches a **Recordset** for the row that satisfies a specified criterion.</span></span> <span data-ttu-id="d06d5-141">При желании может быть указано направление поиска, начальная строка и смещение от начальной строки.</span><span class="sxs-lookup"><span data-stu-id="d06d5-141">Optionally, the direction of the search, starting row, and offset from the starting row may be specified.</span></span> <span data-ttu-id="d06d5-142">Если критерий установлен, для найденной записи устанавливается текущая позиция строки; в противном случае в зависимости от направления поиска устанавливается конец (или начало) набора записей.</span><span class="sxs-lookup"><span data-stu-id="d06d5-142">If the criterion is met, the current row position is set on the found record; otherwise, the position is set to the end (or start) of the **Recordset**, depending on search direction.</span></span>

<span data-ttu-id="d06d5-143">Для этого критерия может быть указано только имя с одним столбцом.</span><span class="sxs-lookup"><span data-stu-id="d06d5-143">Only a single-column name may be specified for the criterion.</span></span> <span data-ttu-id="d06d5-144">Другими словами, этот метод не поддерживает поиск с несколькими столбцами.</span><span class="sxs-lookup"><span data-stu-id="d06d5-144">In other words, this method does not support multi-column searches.</span></span>

<span data-ttu-id="d06d5-145">Оператор сравнения для критерия может быть " **\>** (больше), \*\*\<** " " (меньше), "=" (равно), " \> =" (больше или равно), " \< =" (меньше или равно), \< \> " " (не равно) или "LIKE" (сопоставление шаблонов).</span><span class="sxs-lookup"><span data-stu-id="d06d5-145">The comparison operator for the criterion may be "**\>**" (greater than), "\*\*\<**" (less than), "=" (equal), "\>=" (greater than or equal), "\<=" (less than or equal), "\<\>" (not equal), or "LIKE" (pattern matching).</span></span>

<span data-ttu-id="d06d5-146">Значением критерия может быть строка, число с плавающей за точкой или дата.</span><span class="sxs-lookup"><span data-stu-id="d06d5-146">The criterion value may be a string, floating-point number, or date.</span></span> <span data-ttu-id="d06d5-147">Строки с замещены одними кавычками или \# знаками "( знак номера) (например, "state = "WA"" или "state = \# \# WA").</span><span class="sxs-lookup"><span data-stu-id="d06d5-147">String values are delimited with single quotes or "\#" (number sign) marks (for example, "state = 'WA'" or "state = \#WA\#").</span></span> <span data-ttu-id="d06d5-148">Значения даты имеют знаки \# "" (знак номера) (например, \_ "дата начала \> \# 7/22/97"). \#</span><span class="sxs-lookup"><span data-stu-id="d06d5-148">Date values are delimited with "\#" (number sign) marks (for example, "start\_date \> \#7/22/97\#").</span></span>

<span data-ttu-id="d06d5-149">Если оператор сравнения имеет значение "like", строка может содержать звездочку ( ), чтобы найти одно или несколько вхождений любого символа \* или подстроки.</span><span class="sxs-lookup"><span data-stu-id="d06d5-149">If the comparison operator is "like", the string value may contain an asterisk (\*) to find one or more occurrences of any character or substring.</span></span> <span data-ttu-id="d06d5-150">Например, "state like 'M \* '" matches Maine andТs.</span><span class="sxs-lookup"><span data-stu-id="d06d5-150">For example, "state like 'M\*'" matches Maine and Massachusetts.</span></span> <span data-ttu-id="d06d5-151">Вы также можете использовать звездочки в конце и в конце, чтобы найти подстроку, содержащееся в значениях.</span><span class="sxs-lookup"><span data-stu-id="d06d5-151">You can also use leading and trailing asterisks to find a substring contained within the values.</span></span> <span data-ttu-id="d06d5-152">Например, "state like' \* as \* "" соответствует "Юрасия", "Арканзас" и "Досье".</span><span class="sxs-lookup"><span data-stu-id="d06d5-152">For example, "state like '\*as\*'" matches Alaska, Arkansas, and Massachusetts.</span></span>

<span data-ttu-id="d06d5-153">Звездочки можно использовать только в конце строки условия или вместе в начале и конце строки условий, как показано выше.</span><span class="sxs-lookup"><span data-stu-id="d06d5-153">Asterisks can be used only at the end of a criteria string or together at both the beginning and end of a criteria string, as shown above.</span></span> <span data-ttu-id="d06d5-154">Звезду нельзя использовать в качестве ведущего подкадрического знака (' str') или внедренного \* подкадрического знака \* (r').</span><span class="sxs-lookup"><span data-stu-id="d06d5-154">You cannot use the asterisk as a leading wildcard ('\*str') or embedded wildcard ('s\*r').</span></span> <span data-ttu-id="d06d5-155">Это приведет к ошибке.</span><span class="sxs-lookup"><span data-stu-id="d06d5-155">This will cause an error.</span></span>

### <a name="seek-and-index"></a><span data-ttu-id="d06d5-156">Поиск и индекс</span><span class="sxs-lookup"><span data-stu-id="d06d5-156">Seek and Index</span></span>

<span data-ttu-id="d06d5-157">Используйте метод **Seek** в сочетании со свойством **Index,** если поставщик поддерживает индексы объекта **Recordset.**</span><span class="sxs-lookup"><span data-stu-id="d06d5-157">Use the **Seek** method in conjunction with the **Index** property if the underlying provider supports indexes on the **Recordset** object.</span></span> <span data-ttu-id="d06d5-158">Используйте метод [Supports](supports-method-ado.md)**(adSeek),** чтобы определить, поддерживает ли поставщик **поиск,** и метод **Supports(adIndex),** чтобы определить, поддерживает ли поставщик индексы.</span><span class="sxs-lookup"><span data-stu-id="d06d5-158">Use the [Supports](supports-method-ado.md)**(adSeek)** method to determine whether the underlying provider supports **Seek**, and the **Supports(adIndex)** method to determine whether the provider supports indexes.</span></span> <span data-ttu-id="d06d5-159">(Например, поставщик [OLE DB для Microsoft Jet](microsoft-ole-db-provider-for-microsoft-jet.md) поддерживает **Seek** и **Index.)**</span><span class="sxs-lookup"><span data-stu-id="d06d5-159">(For example, the [OLE DB Provider for Microsoft Jet](microsoft-ole-db-provider-for-microsoft-jet.md) supports **Seek** and **Index**.)</span></span>

<span data-ttu-id="d06d5-160">Если **Seek** не находит нужную строку, ошибка не возникает, а строка находится в конце **recordset.**</span><span class="sxs-lookup"><span data-stu-id="d06d5-160">If **Seek** does not find the desired row, no error occurs, and the row is positioned at the end of the **Recordset**.</span></span> <span data-ttu-id="d06d5-161">Перед **выполнением** этого метода установите для свойства Index нужный индекс.</span><span class="sxs-lookup"><span data-stu-id="d06d5-161">Set the **Index** property to the desired index before executing this method.</span></span>

<span data-ttu-id="d06d5-162">Этот метод поддерживается только с помощью курсоров на стороне сервера.</span><span class="sxs-lookup"><span data-stu-id="d06d5-162">This method is supported only with server-side cursors.</span></span> <span data-ttu-id="d06d5-163">Seek не поддерживается, если свойство [CursorLocation](cursorlocation-property-ado.md) объекта **Recordset** имеет значение **adUseClient.**</span><span class="sxs-lookup"><span data-stu-id="d06d5-163">Seek is not supported when the **Recordset** object's [CursorLocation](cursorlocation-property-ado.md) property value is **adUseClient**.</span></span>

<span data-ttu-id="d06d5-164">Этот метод можно использовать только в том случае, если объект **Recordset** открыт со значением [CommandTypeEnum](commandtypeenum.md) **adCmdTableDirect.**</span><span class="sxs-lookup"><span data-stu-id="d06d5-164">This method can be used only when the **Recordset** object has been opened with a [CommandTypeEnum](commandtypeenum.md) value of **adCmdTableDirect**.</span></span>

## <a name="filtering-the-results"></a><span data-ttu-id="d06d5-165">Фильтрация результатов</span><span class="sxs-lookup"><span data-stu-id="d06d5-165">Filtering the results</span></span>

<span data-ttu-id="d06d5-166">Метод **Find** ограничивает поиск содержимым одного поля.</span><span class="sxs-lookup"><span data-stu-id="d06d5-166">The **Find** method limits your search to the contents of one field.</span></span> <span data-ttu-id="d06d5-167">Метод **Seek** требует на то, чтобы у вас был индекс и есть другие ограничения.</span><span class="sxs-lookup"><span data-stu-id="d06d5-167">The **Seek** method requires that you have an index and has other limitations as well.</span></span> <span data-ttu-id="d06d5-168">Если требуется искать по нескольким полям, которые не являются основой индекса или поставщик не поддерживает индексы, можно ограничить результаты с помощью свойства **Filter** объекта **Recordset.**</span><span class="sxs-lookup"><span data-stu-id="d06d5-168">If you need to search on multiple fields that are not the basis of an index or if your provider does not support indexes, you can limit your results using the **Filter** property of the **Recordset** object.</span></span>

<span data-ttu-id="d06d5-169">Используйте свойство **Filter,** чтобы выборочно отфильтровать записи в **объекте Recordset.**</span><span class="sxs-lookup"><span data-stu-id="d06d5-169">Use the **Filter** property to selectively screen out records in a **Recordset** object.</span></span> <span data-ttu-id="d06d5-170">Отфильтрованный **набор** записей становится текущим курсором, то есть записи, не  удовлетворяющие  условиям **фильтра,** недоступны в наборе записей, пока фильтр не будет удален.</span><span class="sxs-lookup"><span data-stu-id="d06d5-170">The filtered **Recordset** becomes the current cursor, which means that records that do not satisfy the **Filter** criteria are not available in the **Recordset** until the **Filter** is removed.</span></span> <span data-ttu-id="d06d5-171">Другие свойства, возвращающиеся значения на основе текущего курсора, влияют на такие свойства, как **AbsolutePosition,** **AbsolutePage,** **RecordCount** и **PageCount.**</span><span class="sxs-lookup"><span data-stu-id="d06d5-171">Other properties that return values based on the current cursor are affected, such as **AbsolutePosition**, **AbsolutePage**, **RecordCount**, and **PageCount**.</span></span> <span data-ttu-id="d06d5-172">Это необходимо потому, что при установке для свойства **Filter** определенного значения текущая запись перемещается в первую запись, которая удовлетворяет новому значению.</span><span class="sxs-lookup"><span data-stu-id="d06d5-172">This is because setting the **Filter** property to a specific value will move the current record to the first record that satisfies the new value.</span></span>

<span data-ttu-id="d06d5-173">Свойство **Filter** принимает аргумент variant.</span><span class="sxs-lookup"><span data-stu-id="d06d5-173">The **Filter** property takes a variant argument.</span></span> <span data-ttu-id="d06d5-174">Это значение представляет один из трех методов использования свойства **Filter:** строку условия, константу **FilterGroupEnum** или массив закладок.</span><span class="sxs-lookup"><span data-stu-id="d06d5-174">This value represents one of three methods for using the **Filter** property: a criteria string, a **FilterGroupEnum** constant, or an array of bookmarks.</span></span> <span data-ttu-id="d06d5-175">Дополнительные сведения см. в разделах "Фильтрация со строкой условий", "Фильтрация с константой" и "Фильтрация с закладок" далее в этом разделе.</span><span class="sxs-lookup"><span data-stu-id="d06d5-175">For more information, see Filtering with a Criteria String, Filtering with a Constant, and Filtering with Bookmarks later in this topic.</span></span>

> [!NOTE]
> <span data-ttu-id="d06d5-176">Если вы знаете данные, которые нужно выбрать, обычно  эффективнее открыть набор записей с помощью SQL, который эффективно фильтрует набор результатов, а не полагаться на свойство **Filter.**</span><span class="sxs-lookup"><span data-stu-id="d06d5-176">When you know the data you want to select, it is usually more efficient to open a **Recordset** with a SQL statement that effectively filters the result set, rather than relying on the **Filter** property.</span></span>

<span data-ttu-id="d06d5-177">Чтобы удалить фильтр из **recordset,** используйте константы **adFilterNone.**</span><span class="sxs-lookup"><span data-stu-id="d06d5-177">To remove a filter from a **Recordset**, use the **adFilterNone** constant.</span></span> <span data-ttu-id="d06d5-178">Установка для **свойства Filter** нулевой длины строки ("") имеет тот же эффект, что и использование константы **adFilterNone.**</span><span class="sxs-lookup"><span data-stu-id="d06d5-178">Setting the **Filter** property to a zero-length string ("") has the same effect as using the **adFilterNone** constant.</span></span>

### <a name="filtering-with-a-criteria-string"></a><span data-ttu-id="d06d5-179">Фильтрация со строкой условий</span><span class="sxs-lookup"><span data-stu-id="d06d5-179">Filtering with a criteria string</span></span>

<span data-ttu-id="d06d5-180">Строка условий состоит из предложений в виде Значения оператора *FieldName* (например, "LastName = 'Smith'").</span><span class="sxs-lookup"><span data-stu-id="d06d5-180">The criteria string is made up of clauses in the form *FieldName Operator Value* (for example, "LastName = 'Smith'").</span></span> <span data-ttu-id="d06d5-181">Составные предложения можно создать, соединив отдельные предложения с И (например, "LastName = "Smith' AND FirstName = "John'") и OR (например, ).</span><span class="sxs-lookup"><span data-stu-id="d06d5-181">You can create compound clauses by concatenating individual clauses with AND (for example, "LastName = 'Smith' AND FirstName = 'John'") and OR (for example, ).</span></span> <span data-ttu-id="d06d5-182">Составные предложения можно создать, соединив отдельные предложения с И (например, "LastName = 'Smith' AND FirstName = 'John'") и OR (например, "LastName = 'Smith' OR LastName = 'Jones'").</span><span class="sxs-lookup"><span data-stu-id="d06d5-182">You can create compound clauses by concatenating individual clauses with AND (for example, "LastName = 'Smith' AND FirstName = 'John'") and OR (for example, "LastName = 'Smith' OR LastName = 'Jones'").</span></span> <span data-ttu-id="d06d5-183">Используйте следующие рекомендации для строк условий:</span><span class="sxs-lookup"><span data-stu-id="d06d5-183">Use the following guidelines for criteria strings:</span></span>

- <span data-ttu-id="d06d5-184">*FieldName* должно быть допустимым именем поля из **recordset.**</span><span class="sxs-lookup"><span data-stu-id="d06d5-184">*FieldName* must be a valid field name from the **Recordset**.</span></span> <span data-ttu-id="d06d5-185">Если имя поля содержит пробелы, его необходимо заключить в квадратные скобки.</span><span class="sxs-lookup"><span data-stu-id="d06d5-185">If the field name contains spaces, you must enclose the name in square brackets.</span></span>

- <span data-ttu-id="d06d5-186">*Оператор* должен быть одним из следующих: \< , , \> \< =, \> =, , \< \> =, или LIKE.</span><span class="sxs-lookup"><span data-stu-id="d06d5-186">*Operator* must be one of the following: \<, \>, \<=, \>=, \<\>, =, or LIKE.</span></span>

- <span data-ttu-id="d06d5-187">*Значение* — это значение, с которым будут сравниваться значения полей (например, "Smith", \# 8/24/95, \# 12.345 или $50.00).</span><span class="sxs-lookup"><span data-stu-id="d06d5-187">*Value* is the value with which you will compare the field values (for example, 'Smith', \#8/24/95\#, 12.345, or $50.00).</span></span> <span data-ttu-id="d06d5-188">Используйте одиночные кавычка (') со строками и знаками с знаками с знаками \# () с датами.</span><span class="sxs-lookup"><span data-stu-id="d06d5-188">Use single quotation marks (') with strings and pound signs (\#) with dates.</span></span> <span data-ttu-id="d06d5-189">Для чисел можно использовать десятичных знаков, знаки доллара и научной нотации.</span><span class="sxs-lookup"><span data-stu-id="d06d5-189">For numbers, you can use decimal points, dollar signs, and scientific notation.</span></span> <span data-ttu-id="d06d5-190">Если *оператор* имеет значение LIKE, *value* может использовать под wildcards.</span><span class="sxs-lookup"><span data-stu-id="d06d5-190">If *Operator* is LIKE, *Value* can use wildcards.</span></span> <span data-ttu-id="d06d5-191">Только знак звездочки \* () и знак процента (%) поддиаными знаками разрешено, и они должны быть последними символами в строке.</span><span class="sxs-lookup"><span data-stu-id="d06d5-191">Only the asterisk (\*) and percent sign (%) wildcards are allowed, and they must be the last character in the string.</span></span> <span data-ttu-id="d06d5-192">*Значение* не может быть null.</span><span class="sxs-lookup"><span data-stu-id="d06d5-192">*Value* cannot be null.</span></span>
    
  > [!NOTE]
  > <span data-ttu-id="d06d5-193">Чтобы включить одиночная кавычка (') в значение *фильтра,* используйте два одиночных кавычка для представления одного.</span><span class="sxs-lookup"><span data-stu-id="d06d5-193">To include single quotation marks (') in the filter *Value*, use two single quotation marks to represent one.</span></span> <span data-ttu-id="d06d5-194">Например, для фильтрации *по O'Malley* строка условий должна быть "col1 = "O''Malley'".</span><span class="sxs-lookup"><span data-stu-id="d06d5-194">For example, to filter on *O'Malley*, the criteria string should be "col1 = 'O''Malley'".</span></span> 
  > 
  > <span data-ttu-id="d06d5-195">Чтобы включить одиночная кавычка в начале и конце значения фильтра, заключив строку в знаки с знаками знака (#).</span><span class="sxs-lookup"><span data-stu-id="d06d5-195">To include single quotation marks at both the beginning and the end of the filter value, enclose the string in pound signs (#).</span></span> <span data-ttu-id="d06d5-196">Например, для фильтрации по *"1"* строка условий должна быть "col1 = #'1'#".</span><span class="sxs-lookup"><span data-stu-id="d06d5-196">For example, to filter on *'1'*, the criteria string should be "col1 = #'1'#".</span></span>

<span data-ttu-id="d06d5-197">Между AND и OR нет приоритета.</span><span class="sxs-lookup"><span data-stu-id="d06d5-197">There is no precedence between AND and OR.</span></span> <span data-ttu-id="d06d5-198">Предложения можно сгруппить в скобки.</span><span class="sxs-lookup"><span data-stu-id="d06d5-198">Clauses can be grouped within parentheses.</span></span> <span data-ttu-id="d06d5-199">Однако вы не можете сгруппить предложения, присоединимые к or, а затем присоединить группу к другому предложению с помощью И, например:</span><span class="sxs-lookup"><span data-stu-id="d06d5-199">However, you cannot group clauses joined by an OR and then join the group to another clause with an AND, like this:</span></span>

```vb 
 
(LastName = 'Smith' OR LastName = 'Jones') AND FirstName = 'John' 
```

<span data-ttu-id="d06d5-200">Вместо этого этот фильтр будет создаваться как:</span><span class="sxs-lookup"><span data-stu-id="d06d5-200">Instead, you would construct this filter as:</span></span>

```vb 
 
(LastName = 'Smith' AND FirstName = 'John') OR (LastName = 'Jones' AND FirstName = 'John') 
```

<span data-ttu-id="d06d5-201">В предложении LIKE можно использовать под шаблон в начале и конце шаблона (например, LastName Like ' mit ') или только в конце шаблона (например, ) или только в конце шаблона \* \* (например, LastName Like 'Smit \* ').</span><span class="sxs-lookup"><span data-stu-id="d06d5-201">In a LIKE clause, you can use a wildcard at the beginning and end of the pattern (for example, LastName Like '\*mit\*') or only at the end of the pattern (for example, ) or only at the end of the pattern (for example, LastName Like 'Smit\*').</span></span>

### <a name="filtering-with-a-constant"></a><span data-ttu-id="d06d5-202">Фильтрация с помощью константы</span><span class="sxs-lookup"><span data-stu-id="d06d5-202">Filtering with a constant</span></span>

<span data-ttu-id="d06d5-203">Для фильтрации записей доступны следующие **константы.**</span><span class="sxs-lookup"><span data-stu-id="d06d5-203">The following constants are available for filtering **Recordsets**.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="d06d5-204">Константа</span><span class="sxs-lookup"><span data-stu-id="d06d5-204">Constant</span></span></p></th>
<th><p><span data-ttu-id="d06d5-205">Описание</span><span class="sxs-lookup"><span data-stu-id="d06d5-205">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d06d5-206"><strong>adFilterAffectedRecords</strong></span><span class="sxs-lookup"><span data-stu-id="d06d5-206"><strong>adFilterAffectedRecords</strong></span></span></p></td>
<td><p><span data-ttu-id="d06d5-207">Фильтры для просмотра только записей, на которые влияет последний вызов <strong>Delete,</strong> <strong>Resync,</strong> <strong>UpdateBatch</strong>или <strong>CancelBatch.</strong></span><span class="sxs-lookup"><span data-stu-id="d06d5-207">Filters for viewing only records effected by the last <strong>Delete</strong>, <strong>Resync</strong>, <strong>UpdateBatch</strong>, or <strong>CancelBatch</strong> call.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d06d5-208"><strong>adFilterConflictingRecords</strong></span><span class="sxs-lookup"><span data-stu-id="d06d5-208"><strong>adFilterConflictingRecords</strong></span></span></p></td>
<td><p><span data-ttu-id="d06d5-209">Фильтры для просмотра записей, которые не удалось обновить последним пакетным обновлением.</span><span class="sxs-lookup"><span data-stu-id="d06d5-209">Filters for viewing the records that failed the last batch update.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d06d5-210"><strong>adFilterFetchedRecords</strong></span><span class="sxs-lookup"><span data-stu-id="d06d5-210"><strong>adFilterFetchedRecords</strong></span></span></p></td>
<td><p><span data-ttu-id="d06d5-211">Фильтры для просмотра записей в текущем кэше, то есть результатов последнего вызова для получения записей из базы данных.</span><span class="sxs-lookup"><span data-stu-id="d06d5-211">Filters for viewing the records in the current cache — that is, the results of the last call to retrieve records from the database.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d06d5-212"><strong>adFilterNone</strong></span><span class="sxs-lookup"><span data-stu-id="d06d5-212"><strong>adFilterNone</strong></span></span></p></td>
<td><p><span data-ttu-id="d06d5-213">Удаляет текущий фильтр и восстанавливает все записи для просмотра.</span><span class="sxs-lookup"><span data-stu-id="d06d5-213">Removes the current filter and restores all records for viewing.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d06d5-214"><strong>adFilterPendingRecords</strong></span><span class="sxs-lookup"><span data-stu-id="d06d5-214"><strong>adFilterPendingRecords</strong></span></span></p></td>
<td><p><span data-ttu-id="d06d5-215">Фильтры для просмотра только тех записей, которые были изменены, но еще не отправлены на сервер.</span><span class="sxs-lookup"><span data-stu-id="d06d5-215">Filters for viewing only records that have changed but have not yet been sent to the server.</span></span> <span data-ttu-id="d06d5-216">Применимо только для режима пакетного обновления.</span><span class="sxs-lookup"><span data-stu-id="d06d5-216">Applicable only for batch update mode.</span></span></p></td>
</tr>
</tbody>
</table>

<br/>

<span data-ttu-id="d06d5-217">Константы фильтра упрощают разрешение конфликтов отдельных записей в режиме пакетного обновления, позволяя просматривать, например, только те записи, которые были зарегистрированы во время последнего вызова метода **UpdateBatch,** как показано в следующем примере:</span><span class="sxs-lookup"><span data-stu-id="d06d5-217">The filter constants make it easier to resolve individual record conflicts during batch update mode by allowing you to view, for example, only those records that were effected during the last **UpdateBatch** method call, as shown in the following example:</span></span>

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

### <a name="filtering-with-bookmarks"></a><span data-ttu-id="d06d5-218">Фильтрация с закладок</span><span class="sxs-lookup"><span data-stu-id="d06d5-218">Filtering with bookmarks</span></span>

<span data-ttu-id="d06d5-219">Наконец, можно передать массив вариантов закладок в свойство **Filter.**</span><span class="sxs-lookup"><span data-stu-id="d06d5-219">Finally, you can pass a variant array of bookmarks to the **Filter** property.</span></span> <span data-ttu-id="d06d5-220">В результате курсор будет содержать только те записи, закладка которых была передана свойству.</span><span class="sxs-lookup"><span data-stu-id="d06d5-220">The resulting cursor will contain only those records whose bookmark was passed in to the property.</span></span> <span data-ttu-id="d06d5-221">В следующем примере кода создается массив закладок из записей в **наборе recordset,** у которых в поле *ProductName* есть "B".</span><span class="sxs-lookup"><span data-stu-id="d06d5-221">The following code example creates an array of bookmarks from the records in a **Recordset** which have a "B" in the *ProductName* field.</span></span> <span data-ttu-id="d06d5-222">Затем он передает массив в свойство **Filter** и отображает сведения о итоговом отфильтрованный **набор записей.**</span><span class="sxs-lookup"><span data-stu-id="d06d5-222">It then passes the array to the **Filter** property and displays information about the resulting filtered **Recordset**.</span></span>

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

## <a name="creating-a-clone-of-a-recordset"></a><span data-ttu-id="d06d5-223">Создание клона recordset</span><span class="sxs-lookup"><span data-stu-id="d06d5-223">Creating a clone of a Recordset</span></span>

<span data-ttu-id="d06d5-224">Используйте метод **Clone** для создания нескольких повторяюных объектов **Recordset,** особенно если вы хотите сохранить несколько текущих записей в заданный набор записей.</span><span class="sxs-lookup"><span data-stu-id="d06d5-224">Use the **Clone** method to create multiple, duplicate **Recordset** objects, particularly if you want to maintain more than one current record in a given set of records.</span></span> <span data-ttu-id="d06d5-225">Использование метода **Clone** более эффективно, чем создание и открытие объекта **Recordset** с тем же определением, что и у исходного объекта.</span><span class="sxs-lookup"><span data-stu-id="d06d5-225">Using the **Clone** method is more efficient than creating and opening a new **Recordset** object with the same definition as the original.</span></span>

<span data-ttu-id="d06d5-226">Текущая запись только что созданного клона изначально устанавливается как первая запись.</span><span class="sxs-lookup"><span data-stu-id="d06d5-226">The current record of a newly created clone is originally set to the first record.</span></span> <span data-ttu-id="d06d5-227">Указатель текущей записи в клонированном наборе **записей** не синхронизируется с исходным или наоборот.</span><span class="sxs-lookup"><span data-stu-id="d06d5-227">The current record pointer in a cloned **Recordset** is not synchronized with the original or vice versa.</span></span> <span data-ttu-id="d06d5-228">Вы можете перемещаться независимо в каждом **наборе записей.**</span><span class="sxs-lookup"><span data-stu-id="d06d5-228">You can navigate independently in each **Recordset**.</span></span>

<span data-ttu-id="d06d5-229">Изменения, внесенные в один **объект Recordset,** видны во всех его клонах независимо от типа курсора.</span><span class="sxs-lookup"><span data-stu-id="d06d5-229">Changes you make to one **Recordset** object are visible in all of its clones regardless of cursor type.</span></span> <span data-ttu-id="d06d5-230">Однако после выполнения [Requery](requery-method-ado.md) в исходном наборе **записей** клоны больше не будут синхронизироваться с исходным набором.</span><span class="sxs-lookup"><span data-stu-id="d06d5-230">However, after you execute [Requery](requery-method-ado.md) on the original **Recordset**, the clones will no longer be synchronized to the original.</span></span>

<span data-ttu-id="d06d5-231">Закрытие **исходного наборов записей** не закрывает его копии и не закрывает исходную или любую из других копий.</span><span class="sxs-lookup"><span data-stu-id="d06d5-231">Closing the original **Recordset** does not close its copies, nor does closing a copy close the original or any of the other copies.</span></span>

<span data-ttu-id="d06d5-232">Клонировать объект **Recordset можно** только в том случае, если он поддерживает закладки.</span><span class="sxs-lookup"><span data-stu-id="d06d5-232">You can clone a **Recordset** object only if it supports bookmarks.</span></span> <span data-ttu-id="d06d5-233">Значения закладок являются взаимозаменяемыми; то есть ссылка на закладку из одного объекта **Recordset** ссылается на ту же запись в любом из его клонов.</span><span class="sxs-lookup"><span data-stu-id="d06d5-233">Bookmark values are interchangeable; that is, a bookmark reference from one **Recordset** object refers to the same record in any of its clones.</span></span>


---
title: Работа с наборами записей
TOCTitle: Working with Recordsets
ms:assetid: 9cd52866-2738-8150-381c-eee0b8a6cd36
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249711(v=office.15)
ms:contentKeyID: 48546608
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 241d9470d518893312daaa8101a5517706ea1e50
ms.sourcegitcommit: 1dd744993ecb4bed241ace874ad26edaef1778b8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/06/2018
ms.locfileid: "25998359"
---
# <a name="working-with-recordsets"></a><span data-ttu-id="e8e60-102">Работа с наборами записей</span><span class="sxs-lookup"><span data-stu-id="e8e60-102">Working with Recordsets</span></span>

<span data-ttu-id="e8e60-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="e8e60-103">**Applies to**: Access 2013, Office 2013</span></span> 

<span data-ttu-id="e8e60-104">Объект **набора записей** содержит встроенные функции, которые позволяют изменить порядок данные в результате задать, для поиска конкретных записей по критерии, по которым вы задаете и даже для оптимизации тех поиска операций с помощью индексов.</span><span class="sxs-lookup"><span data-stu-id="e8e60-104">The **Recordset** object has built-in features that make it possible for you to rearrange the order of the data in the result set, to search for a specific record based on criteria that you supply, and even to optimize those search operations using indexes.</span></span> <span data-ttu-id="e8e60-105">Эти возможности доступны для использования зависит от поставщика и в некоторых случаях — например, свойство [Index](index-property-ado.md) — Структура самого источника данных.</span><span class="sxs-lookup"><span data-stu-id="e8e60-105">Whether these features are available for use depends on the provider and in some cases — such as that of the [Index](index-property-ado.md) property — the structure of the data source itself.</span></span>

## <a name="arranging-data"></a><span data-ttu-id="e8e60-106">Упорядочивание данных</span><span class="sxs-lookup"><span data-stu-id="e8e60-106">Arranging data</span></span>

<span data-ttu-id="e8e60-107">Часто самый эффективный способ упорядочивать данные набора **записей** — путем указания предложение ORDER BY в команды SQL, используется для возврата результатов.</span><span class="sxs-lookup"><span data-stu-id="e8e60-107">Often, the most efficient way to order the data in your **Recordset** is by specifying an ORDER BY clause in the SQL command used to return results to it.</span></span> <span data-ttu-id="e8e60-108">Тем не менее может потребоваться изменение порядка данных в **набор записей** , которые уже были созданы.</span><span class="sxs-lookup"><span data-stu-id="e8e60-108">However, you might need to change the order of the data in a **Recordset** that has already been created.</span></span> <span data-ttu-id="e8e60-109">Свойство **сортировки** для установления порядка проверено строк **набора записей** .</span><span class="sxs-lookup"><span data-stu-id="e8e60-109">You can use the **Sort** property to establish the order in which rows of a **Recordset** are traversed.</span></span> <span data-ttu-id="e8e60-110">Кроме того свойство **фильтра** определяет строк, которые доступны при обходе строк.</span><span class="sxs-lookup"><span data-stu-id="e8e60-110">Furthermore, the **Filter** property determines which rows are accessible when traversing rows.</span></span>

<span data-ttu-id="e8e60-111">Свойство **сортировки** задает или возвращает **строковое** значение, указывающее, имена полей в наборе **записей** , по которому выполняется сортировка.</span><span class="sxs-lookup"><span data-stu-id="e8e60-111">The **Sort** property sets or returns a **String** value that indicates the field names in the **Recordset** on which to sort.</span></span> <span data-ttu-id="e8e60-112">Имя каждого разделенных точкой с запятой и при необходимости следуют пробел и ключевое слово **ASC** (который выполняется сортировка поля в порядке возрастания) или **DESC** (который выполняется сортировка поля в порядке убывания).</span><span class="sxs-lookup"><span data-stu-id="e8e60-112">Each name is separated by a comma and is optionally followed by a space and the keyword **ASC** (which sorts the field in ascending order) or **DESC** (which sorts the field in descending order).</span></span> <span data-ttu-id="e8e60-113">По умолчанию если нет ключевых слов не указан, то это поле является сортироваться в восходящем порядке.</span><span class="sxs-lookup"><span data-stu-id="e8e60-113">By default, if no keyword is specified, the field is sorted in ascending order.</span></span>

<span data-ttu-id="e8e60-114">Операция сортировки эффективен, так как данные физически не изменяется, но просто осуществляется в порядке, указанном с помощью индекса.</span><span class="sxs-lookup"><span data-stu-id="e8e60-114">The sort operation is efficient because data is not physically rearranged but is simply accessed in the order specified by an index.</span></span>

<span data-ttu-id="e8e60-115">Свойство **сортировки** требует свойства [CursorLocation](cursorlocation-property-ado.md) должно быть задано для **adUseClient**.</span><span class="sxs-lookup"><span data-stu-id="e8e60-115">The **Sort** property requires the [CursorLocation](cursorlocation-property-ado.md) property to be set to **adUseClient**.</span></span> <span data-ttu-id="e8e60-116">Временный индекс создается для каждого поля, указанных в свойстве **сортировки** , если индекс еще не существует.</span><span class="sxs-lookup"><span data-stu-id="e8e60-116">A temporary index will be created for each field specified in the **Sort** property if an index does not already exist.</span></span>

<span data-ttu-id="e8e60-117">Свойства **сортировки** пустую строку Сброс исходный порядок строк и удалите временные индексы.</span><span class="sxs-lookup"><span data-stu-id="e8e60-117">Setting the **Sort** property to an empty string will reset the rows to their original order and delete temporary indexes.</span></span> <span data-ttu-id="e8e60-118">Существующие индексы не удаляются.</span><span class="sxs-lookup"><span data-stu-id="e8e60-118">Existing indexes will not be deleted.</span></span>

<span data-ttu-id="e8e60-119">Предположим, что **набор записей** содержит три поля с именами *firstName*, *middleInitial*и *Фамилия*.</span><span class="sxs-lookup"><span data-stu-id="e8e60-119">Suppose a **Recordset** contains three fields named *firstName*, *middleInitial*, and *lastName*.</span></span> <span data-ttu-id="e8e60-120">Присвойте свойству **сортировки** в строку «», которое будет порядке **записей** по фамилии в порядке убывания, а затем по имени в порядке возрастания.</span><span class="sxs-lookup"><span data-stu-id="e8e60-120">Set the **Sort** property to the string "", which will order the **Recordset** by last name in descending order and then by first name in ascending order.</span></span> <span data-ttu-id="e8e60-121">Инициалы игнорируется.</span><span class="sxs-lookup"><span data-stu-id="e8e60-121">The middle initial is ignored.</span></span>

<span data-ttu-id="e8e60-122">Поле не указывается в строке условия сортировки может быть с именем «ASC» или «DESC» конфликтовать с ключевыми словами **ASC** и **DESC**их имена.</span><span class="sxs-lookup"><span data-stu-id="e8e60-122">No field referenced in a sort criteria string can be named "ASC" or "DESC" because those names conflict with the keywords **ASC** and **DESC**.</span></span> <span data-ttu-id="e8e60-123">Задайте псевдоним поля с конфликтующими именами с помощью ключевого слова **AS** в запрос, возвращающий **набора записей**.</span><span class="sxs-lookup"><span data-stu-id="e8e60-123">Give a field with a conflicting name an alias by using the **AS** keyword in the query that returns the **Recordset**.</span></span>

<span data-ttu-id="e8e60-124">Для получения дополнительных сведений о фильтрации **записей** видеть фильтрации результатов, полученных данного раздела.</span><span class="sxs-lookup"><span data-stu-id="e8e60-124">For more details about **Recordset** filtering, see Filtering the Results later in this topic.</span></span>

## <a name="finding-a-specific-record"></a><span data-ttu-id="e8e60-125">Поиск определенной записи</span><span class="sxs-lookup"><span data-stu-id="e8e60-125">Finding a specific record</span></span>

<span data-ttu-id="e8e60-126">ADO предоставляет методы [поиска](find-method-ado.md) и [поиска](seek-method-ado.md) для поиска конкретной записи в **набор записей**.</span><span class="sxs-lookup"><span data-stu-id="e8e60-126">ADO provides the [Find](find-method-ado.md) and [Seek](seek-method-ado.md) methods for locating a particular record in a **Recordset**.</span></span> <span data-ttu-id="e8e60-127">Метод **поиска** поддерживается различных поставщиков, но не может превышать одного поиска.</span><span class="sxs-lookup"><span data-stu-id="e8e60-127">The **Find** method is supported by a variety of providers but is limited to a single search criterion.</span></span> <span data-ttu-id="e8e60-128">Метод **Seek** поддерживает поиск по нескольким условиям, но не поддерживает многие поставщики.</span><span class="sxs-lookup"><span data-stu-id="e8e60-128">The **Seek** method supports searching on multiple criteria, but is not supported by many providers.</span></span>

<span data-ttu-id="e8e60-129">Индексов на полях может значительно увеличить производительность **поиска** метода и **Сортировка** и **Фильтрация** свойства объекта **набора записей** .</span><span class="sxs-lookup"><span data-stu-id="e8e60-129">Indexes on fields can greatly enhance the performance of the **Recordset** object's **Find** method and **Sort** and **Filter** properties.</span></span> <span data-ttu-id="e8e60-130">Можно создать внутренний индекс для объекта **поля** путем установки свойства динамического [оптимизировать](optimize-property-dynamic-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="e8e60-130">You can create an internal index for a **Field** object by setting its dynamic [Optimize](optimize-property-dynamic-ado.md) property.</span></span> <span data-ttu-id="e8e60-131">Это свойство динамических добавляется в коллекцию **свойств** объекта **поля** при [CursorLocation](cursorlocation-property-ado.md) свойству присвоено значение **adUseClient**.</span><span class="sxs-lookup"><span data-stu-id="e8e60-131">This dynamic property is added to the **Field** object's **Properties** collection when you set the [CursorLocation](cursorlocation-property-ado.md) property to **adUseClient**.</span></span> <span data-ttu-id="e8e60-132">Имейте в виду, что этот индекс внутренних ADO — не удается получить доступ к нему или использовать в любых других целях.</span><span class="sxs-lookup"><span data-stu-id="e8e60-132">Remember that this index is internal to ADO — you cannot gain access to it or use it for any other purpose.</span></span> <span data-ttu-id="e8e60-133">Кроме того в этом индекса отличается от свойства [Index](index-property-ado.md) объекта **набора записей** .</span><span class="sxs-lookup"><span data-stu-id="e8e60-133">Also, this index is distinct from the **Recordset** object's [Index](index-property-ado.md) property.</span></span>

<span data-ttu-id="e8e60-134">Метод **поиска** быстро находит значение в столбец (поле) набора **записей**.</span><span class="sxs-lookup"><span data-stu-id="e8e60-134">The **Find** method quickly locates a value within a column (field) of a **Recordset**.</span></span> <span data-ttu-id="e8e60-135">Часто может увеличить скорость операции метод **поиска** для столбца с помощью свойства **оптимизировать** для создания индекса.</span><span class="sxs-lookup"><span data-stu-id="e8e60-135">You can often improve the speed of the **Find** method's operation on a column by using the **Optimize** property to create an index on it.</span></span>

<span data-ttu-id="e8e60-136">Метод **Найти** ограничивает поиск значения одного поля.</span><span class="sxs-lookup"><span data-stu-id="e8e60-136">The **Find** method limits your search to the contents of one field.</span></span> <span data-ttu-id="e8e60-137">Метод **Seek** требуется имеет индекса, а также другие ограничения.</span><span class="sxs-lookup"><span data-stu-id="e8e60-137">The **Seek** method requires that you have an index and has other limitations as well.</span></span> <span data-ttu-id="e8e60-138">Если вам требуется выполнять поиск по нескольким полям, которые не отдельных индекса или ваш поставщик поддерживает индексы, можно ограничить результаты с помощью **фильтров** свойств объекта **набора записей** .</span><span class="sxs-lookup"><span data-stu-id="e8e60-138">If you need to search on multiple fields that aren't the basis of an index, or if your provider does not support indexes, you can limit your results using the **Filter** property of the **Recordset** object.</span></span>

### <a name="find"></a><span data-ttu-id="e8e60-139">Найти</span><span class="sxs-lookup"><span data-stu-id="e8e60-139">Find</span></span>

<span data-ttu-id="e8e60-140">Метод **поиска** выполняет поиск **записей** для строки, которая должна удовлетворять указанного критерия.</span><span class="sxs-lookup"><span data-stu-id="e8e60-140">The **Find** method searches a **Recordset** for the row that satisfies a specified criterion.</span></span> <span data-ttu-id="e8e60-141">Кроме того можно указать направление поиска, начальную строку и смещением от начала строки.</span><span class="sxs-lookup"><span data-stu-id="e8e60-141">Optionally, the direction of the search, starting row, and offset from the starting row may be specified.</span></span> <span data-ttu-id="e8e60-142">Если соблюдаются условия, текущей позиции строки имеет значение обнаруженного записи; в противном случае положение задано значение (начала или конца) набора **записей**, в зависимости от направление поиска.</span><span class="sxs-lookup"><span data-stu-id="e8e60-142">If the criterion is met, the current row position is set on the found record; otherwise, the position is set to the end (or start) of the **Recordset**, depending on search direction.</span></span>

<span data-ttu-id="e8e60-143">Может быть указано только имя одного столбца критерия.</span><span class="sxs-lookup"><span data-stu-id="e8e60-143">Only a single-column name may be specified for the criterion.</span></span> <span data-ttu-id="e8e60-144">Другими словами этот метод не поддерживает поиска по нескольким столбцам.</span><span class="sxs-lookup"><span data-stu-id="e8e60-144">In other words, this method does not support multi-column searches.</span></span>

<span data-ttu-id="e8e60-145">Оператор сравнения критерия может быть "**\>**«(больше),»**\<**«(меньше), «=» (равно),»\>=» (больше или равно),"\<=» (меньше или равно), "\<\>" (не равно) или «Как и» (подстановочные знаки).</span><span class="sxs-lookup"><span data-stu-id="e8e60-145">The comparison operator for the criterion may be "**\>**" (greater than), "**\<**" (less than), "=" (equal), "\>=" (greater than or equal), "\<=" (less than or equal), "\<\>" (not equal), or "LIKE" (pattern matching).</span></span>

<span data-ttu-id="e8e60-146">Значение критерия может быть строка, число с плавающей запятой или дата.</span><span class="sxs-lookup"><span data-stu-id="e8e60-146">The criterion value may be a string, floating-point number, or date.</span></span> <span data-ttu-id="e8e60-147">Строковые значения разделяются одинарные кавычки или "\#" (знак) помечает (, например «состояние = «Вашингтон»» или «состояние = \#WA\#«).</span><span class="sxs-lookup"><span data-stu-id="e8e60-147">String values are delimited with single quotes or "\#" (number sign) marks (for example, "state = 'WA'" or "state = \#WA\#").</span></span> <span data-ttu-id="e8e60-148">Значения дат разделяются "\#" помечает (знак) (например, «запустите\_даты \> \#7/22/97\#«).</span><span class="sxs-lookup"><span data-stu-id="e8e60-148">Date values are delimited with "\#" (number sign) marks (for example, "start\_date \> \#7/22/97\#").</span></span>

<span data-ttu-id="e8e60-149">Если оператор сравнения «как», строковое значение может содержать символ звездочки (\*) для поиска одного или нескольких экземпляров любой символ или подстроки.</span><span class="sxs-lookup"><span data-stu-id="e8e60-149">If the comparison operator is "like", the string value may contain an asterisk (\*) to find one or more occurrences of any character or substring.</span></span> <span data-ttu-id="e8e60-150">Например «состояние как am\*"» соответствует Мэн и Массачусетского.</span><span class="sxs-lookup"><span data-stu-id="e8e60-150">For example, "state like 'M\*'" matches Maine and Massachusetts.</span></span> <span data-ttu-id="e8e60-151">Можно также использовать начальные и конечные звездочки поиск подстроки, содержащийся в значениях.</span><span class="sxs-lookup"><span data-stu-id="e8e60-151">You can also use leading and trailing asterisks to find a substring contained within the values.</span></span> <span data-ttu-id="e8e60-152">Например «состояние как "\*как\*"» соответствует Аляска, Arkansas и Массачусетского.</span><span class="sxs-lookup"><span data-stu-id="e8e60-152">For example, "state like '\*as\*'" matches Alaska, Arkansas, and Massachusetts.</span></span>

<span data-ttu-id="e8e60-153">Звездочки можно использовать только в конце строки критерии или друг с другом в начале и в конце строки критерии, как показано выше.</span><span class="sxs-lookup"><span data-stu-id="e8e60-153">Asterisks can be used only at the end of a criteria string or together at both the beginning and end of a criteria string, as shown above.</span></span> <span data-ttu-id="e8e60-154">Нельзя использовать в качестве начальных подстановочный знак звездочка ("\*str") или встраивается подстановочные знаки ('s\*r ").</span><span class="sxs-lookup"><span data-stu-id="e8e60-154">You cannot use the asterisk as a leading wildcard ('\*str') or embedded wildcard ('s\*r').</span></span> <span data-ttu-id="e8e60-155">Это приведет к ошибке.</span><span class="sxs-lookup"><span data-stu-id="e8e60-155">This will cause an error.</span></span>

### <a name="seek-and-index"></a><span data-ttu-id="e8e60-156">Поиск и индексирование</span><span class="sxs-lookup"><span data-stu-id="e8e60-156">Seek and Index</span></span>

<span data-ttu-id="e8e60-157">Используйте метод **Seek** в сочетании со свойством **индекса** , если базовый поставщик поддерживает индексы в объекте **набора записей** .</span><span class="sxs-lookup"><span data-stu-id="e8e60-157">Use the **Seek** method in conjunction with the **Index** property if the underlying provider supports indexes on the **Recordset** object.</span></span> <span data-ttu-id="e8e60-158">Используйте метод [поддерживает](supports-method-ado.md)**(adSeek)** , чтобы определить, поддерживает ли основного поставщика **поиска**и метод **Supports(adIndex)** , чтобы определить, поддерживает ли поставщик индексов.</span><span class="sxs-lookup"><span data-stu-id="e8e60-158">Use the [Supports](supports-method-ado.md)**(adSeek)** method to determine whether the underlying provider supports **Seek**, and the **Supports(adIndex)** method to determine whether the provider supports indexes.</span></span> <span data-ttu-id="e8e60-159">(Например, [Поставщик OLE DB для Microsoft Jet](microsoft-ole-db-provider-for-microsoft-jet.md) поддерживает **поиска** и **индекса**).</span><span class="sxs-lookup"><span data-stu-id="e8e60-159">(For example, the [OLE DB Provider for Microsoft Jet](microsoft-ole-db-provider-for-microsoft-jet.md) supports **Seek** and **Index**.)</span></span>

<span data-ttu-id="e8e60-160">Если **Поиск** не удается найти нужную строку, ошибка не происходит и размещенный строку в конец **набора записей**.</span><span class="sxs-lookup"><span data-stu-id="e8e60-160">If **Seek** does not find the desired row, no error occurs, and the row is positioned at the end of the **Recordset**.</span></span> <span data-ttu-id="e8e60-161">Значение свойства **Index** желаемую индекса перед выполнением этого метода.</span><span class="sxs-lookup"><span data-stu-id="e8e60-161">Set the **Index** property to the desired index before executing this method.</span></span>

<span data-ttu-id="e8e60-162">Этот метод поддерживается только записей на стороне сервера.</span><span class="sxs-lookup"><span data-stu-id="e8e60-162">This method is supported only with server-side cursors.</span></span> <span data-ttu-id="e8e60-163">Поиск не поддерживается, если значение свойства [CursorLocation](cursorlocation-property-ado.md) объекта **набора записей** является **adUseClient**.</span><span class="sxs-lookup"><span data-stu-id="e8e60-163">Seek is not supported when the **Recordset** object's [CursorLocation](cursorlocation-property-ado.md) property value is **adUseClient**.</span></span>

<span data-ttu-id="e8e60-164">Этот метод можно использовать только в том случае, если был открыт со значением [CommandTypeEnum](commandtypeenum.md) **adCmdTableDirect**объекта **набора записей** .</span><span class="sxs-lookup"><span data-stu-id="e8e60-164">This method can be used only when the **Recordset** object has been opened with a [CommandTypeEnum](commandtypeenum.md) value of **adCmdTableDirect**.</span></span>

## <a name="filtering-the-results"></a><span data-ttu-id="e8e60-165">Фильтрация результатов</span><span class="sxs-lookup"><span data-stu-id="e8e60-165">Filtering the results</span></span>

<span data-ttu-id="e8e60-166">Метод **Найти** ограничивает поиск значения одного поля.</span><span class="sxs-lookup"><span data-stu-id="e8e60-166">The **Find** method limits your search to the contents of one field.</span></span> <span data-ttu-id="e8e60-167">Метод **Seek** требуется имеет индекса, а также другие ограничения.</span><span class="sxs-lookup"><span data-stu-id="e8e60-167">The **Seek** method requires that you have an index and has other limitations as well.</span></span> <span data-ttu-id="e8e60-168">Если вам требуется выполнять поиск по нескольким полям, которые не являются основой для индекса или ваш поставщик поддерживает индексы, можно ограничить результаты с помощью **фильтров** свойств объекта **набора записей** .</span><span class="sxs-lookup"><span data-stu-id="e8e60-168">If you need to search on multiple fields that are not the basis of an index or if your provider does not support indexes, you can limit your results using the **Filter** property of the **Recordset** object.</span></span>

<span data-ttu-id="e8e60-169">Используйте свойство **фильтра** выборочно пропускать записей в объекте **набора записей** .</span><span class="sxs-lookup"><span data-stu-id="e8e60-169">Use the **Filter** property to selectively screen out records in a **Recordset** object.</span></span> <span data-ttu-id="e8e60-170">Отфильтрованного **набора записей** становится текущий указатель, что означает, что записи, которые не удовлетворяет условиям **фильтра** , недоступны в **записей** пока не будет снято **фильтра** .</span><span class="sxs-lookup"><span data-stu-id="e8e60-170">The filtered **Recordset** becomes the current cursor, which means that records that do not satisfy the **Filter** criteria are not available in the **Recordset** until the **Filter** is removed.</span></span> <span data-ttu-id="e8e60-171">Другие свойства, возвращающие значения на основании текущей курсора влияет на, такие как **AbsolutePosition**, **AbsolutePage**, **RecordCount**и **PageCount**.</span><span class="sxs-lookup"><span data-stu-id="e8e60-171">Other properties that return values based on the current cursor are affected, such as **AbsolutePosition**, **AbsolutePage**, **RecordCount**, and **PageCount**.</span></span> <span data-ttu-id="e8e60-172">Это связано с определенным значением свойства **фильтра** для первой записи, которая должна удовлетворять новое значение Перемещение текущей записи.</span><span class="sxs-lookup"><span data-stu-id="e8e60-172">This is because setting the **Filter** property to a specific value will move the current record to the first record that satisfies the new value.</span></span>

<span data-ttu-id="e8e60-173">Свойство **фильтра** принимает аргумент типа variant.</span><span class="sxs-lookup"><span data-stu-id="e8e60-173">The **Filter** property takes a variant argument.</span></span> <span data-ttu-id="e8e60-174">Это значение представляет один из трех способов использования свойства **фильтра** : строка критерии, константа **FilterGroupEnum** или массив закладки.</span><span class="sxs-lookup"><span data-stu-id="e8e60-174">This value represents one of three methods for using the **Filter** property: a criteria string, a **FilterGroupEnum** constant, or an array of bookmarks.</span></span> <span data-ttu-id="e8e60-175">Для получения дополнительных сведений см. Далее в этом разделе фильтрация со строкой критерии, фильтрация с константой и фильтрация с помощью закладок.</span><span class="sxs-lookup"><span data-stu-id="e8e60-175">For more information, see Filtering with a Criteria String, Filtering with a Constant, and Filtering with Bookmarks later in this topic.</span></span>

> [!NOTE]
> <span data-ttu-id="e8e60-176">Если вы знаете данных, которые нужно выбрать, обычно более эффективно для открытия **набора записей** с помощью оператора SQL, которая эффективно фильтрует результат установить, а не на свойство **фильтра** .</span><span class="sxs-lookup"><span data-stu-id="e8e60-176">When you know the data you want to select, it is usually more efficient to open a **Recordset** with a SQL statement that effectively filters the result set, rather than relying on the **Filter** property.</span></span>

<span data-ttu-id="e8e60-177">Чтобы удалить фильтр из **набора записей**, используйте константу **adFilterNone** .</span><span class="sxs-lookup"><span data-stu-id="e8e60-177">To remove a filter from a **Recordset**, use the **adFilterNone** constant.</span></span> <span data-ttu-id="e8e60-178">Свойства **фильтра** в строку нулевой длины ("») имеет тот же эффект, что и использование **adFilterNone** константу.</span><span class="sxs-lookup"><span data-stu-id="e8e60-178">Setting the **Filter** property to a zero-length string ("") has the same effect as using the **adFilterNone** constant.</span></span>

### <a name="filtering-with-a-criteria-string"></a><span data-ttu-id="e8e60-179">Фильтрация с использованием строка условий</span><span class="sxs-lookup"><span data-stu-id="e8e60-179">Filtering with a criteria string</span></span>

<span data-ttu-id="e8e60-180">Строка условий включает в себя предложений в форме *FieldName оператор значение* (например, «LastName = «Smith»»).</span><span class="sxs-lookup"><span data-stu-id="e8e60-180">The criteria string is made up of clauses in the form *FieldName Operator Value* (for example, "LastName = 'Smith'").</span></span> <span data-ttu-id="e8e60-181">Можно создать составные предложения, объединив отдельных предложений с AND (например, «LastName = 'Smith» "и" FirstName = «John»») и или (например,).</span><span class="sxs-lookup"><span data-stu-id="e8e60-181">You can create compound clauses by concatenating individual clauses with AND (for example, "LastName = 'Smith' AND FirstName = 'John'") and OR (for example, ).</span></span> <span data-ttu-id="e8e60-182">Можно создать составные предложения, объединив отдельных предложений с AND (, например «LastName = 'Smith» "и" FirstName = «John»») и или (, например «LastName = 'Smith» или LastName = «Jones»»).</span><span class="sxs-lookup"><span data-stu-id="e8e60-182">You can create compound clauses by concatenating individual clauses with AND (for example, "LastName = 'Smith' AND FirstName = 'John'") and OR (for example, "LastName = 'Smith' OR LastName = 'Jones'").</span></span> <span data-ttu-id="e8e60-183">Используйте следующие рекомендации для строк с типом условия:</span><span class="sxs-lookup"><span data-stu-id="e8e60-183">Use the following guidelines for criteria strings:</span></span>

- <span data-ttu-id="e8e60-184">*FieldName* должно быть допустимое имя поля из **набора записей**.</span><span class="sxs-lookup"><span data-stu-id="e8e60-184">*FieldName* must be a valid field name from the **Recordset**.</span></span> <span data-ttu-id="e8e60-185">Если имя поля содержит пробелы, необходимо заключить имя в квадратные скобки.</span><span class="sxs-lookup"><span data-stu-id="e8e60-185">If the field name contains spaces, you must enclose the name in square brackets.</span></span>

- <span data-ttu-id="e8e60-186">*Оператор* должно быть одно из следующих значений: \<, \>, \<=, \>=, \< \>, = или как.</span><span class="sxs-lookup"><span data-stu-id="e8e60-186">*Operator* must be one of the following: \<, \>, \<=, \>=, \<\>, =, or LIKE.</span></span>

- <span data-ttu-id="e8e60-187">*Значение* — это значение, с которым будет сравнение значений полей (например, «Smith», \#8/24/95\#, 12.345 или $50,00).</span><span class="sxs-lookup"><span data-stu-id="e8e60-187">*Value* is the value with which you will compare the field values (for example, 'Smith', \#8/24/95\#, 12.345, or $50.00).</span></span> <span data-ttu-id="e8e60-188">Используйте одинарные кавычки (') со строками и символов (\#) с датами.</span><span class="sxs-lookup"><span data-stu-id="e8e60-188">Use single quotation marks (') with strings and pound signs (\#) with dates.</span></span> <span data-ttu-id="e8e60-189">Для номеров можно использовать десятичные, знак доллара и научное обозначение.</span><span class="sxs-lookup"><span data-stu-id="e8e60-189">For numbers, you can use decimal points, dollar signs, and scientific notation.</span></span> <span data-ttu-id="e8e60-190">Если *оператор* LIKE *значение* можно использовать подстановочные знаки.</span><span class="sxs-lookup"><span data-stu-id="e8e60-190">If *Operator* is LIKE, *Value* can use wildcards.</span></span> <span data-ttu-id="e8e60-191">Только звездочки (\*) и знак процента (%) подстановочные знаки допускаются, и они должны иметь последний символ в строке.</span><span class="sxs-lookup"><span data-stu-id="e8e60-191">Only the asterisk (\*) and percent sign (%) wildcards are allowed, and they must be the last character in the string.</span></span> <span data-ttu-id="e8e60-192">Не может иметь *значение* null.</span><span class="sxs-lookup"><span data-stu-id="e8e60-192">*Value* cannot be null.</span></span>
    
  > [!NOTE]
  > <span data-ttu-id="e8e60-193">Чтобы включить в фильтр *значение*одинарные кавычки ('), используйте одинарные кавычки для представления одного.</span><span class="sxs-lookup"><span data-stu-id="e8e60-193">To include single quotation marks (') in the filter *Value*, use two single quotation marks to represent one.</span></span> <span data-ttu-id="e8e60-194">Например, чтобы отфильтровать *O'Malley*, критерии строка должна быть «Столбец1 = "O'' Malley"».</span><span class="sxs-lookup"><span data-stu-id="e8e60-194">For example, to filter on *O'Malley*, the criteria string should be "col1 = 'O''Malley'".</span></span> 
  > 
  > <span data-ttu-id="e8e60-195">Для включения одинарные кавычки в начале и конце значение фильтра, заключите строку в знаки решетки (#).</span><span class="sxs-lookup"><span data-stu-id="e8e60-195">To include single quotation marks at both the beginning and the end of the filter value, enclose the string in pound signs (#).</span></span> <span data-ttu-id="e8e60-196">Например, чтобы отфильтровать *"1"*, критерии строка должна быть «Столбец1 = # "1" #».</span><span class="sxs-lookup"><span data-stu-id="e8e60-196">For example, to filter on *'1'*, the criteria string should be "col1 = #'1'#".</span></span>

<span data-ttu-id="e8e60-197">Нет нет приоритет между и и или.</span><span class="sxs-lookup"><span data-stu-id="e8e60-197">There is no precedence between AND and OR.</span></span> <span data-ttu-id="e8e60-198">Предложения можно разбить в скобки.</span><span class="sxs-lookup"><span data-stu-id="e8e60-198">Clauses can be grouped within parentheses.</span></span> <span data-ttu-id="e8e60-199">Тем не менее невозможно Группировать предложения, соединенные OR и затем присоединиться к группе на другое предложение с AND, следующим образом:</span><span class="sxs-lookup"><span data-stu-id="e8e60-199">However, you cannot group clauses joined by an OR and then join the group to another clause with an AND, like this:</span></span>

```vb 
 
(LastName = 'Smith' OR LastName = 'Jones') AND FirstName = 'John' 
```

<span data-ttu-id="e8e60-200">Вместо этого построении этот фильтр как:</span><span class="sxs-lookup"><span data-stu-id="e8e60-200">Instead, you would construct this filter as:</span></span>

```vb 
 
(LastName = 'Smith' AND FirstName = 'John') OR (LastName = 'Jones' AND FirstName = 'John') 
```

<span data-ttu-id="e8e60-201">В LIKE, можно использовать подстановочный знак в начале и в конце сопоставляться с шаблоном (, например LastName Like '\*mit\*") или только в конце шаблона (например) или только в конце сопоставляться с шаблоном (, например LastName Like" Smit\*").</span><span class="sxs-lookup"><span data-stu-id="e8e60-201">In a LIKE clause, you can use a wildcard at the beginning and end of the pattern (for example, LastName Like '\*mit\*') or only at the end of the pattern (for example, ) or only at the end of the pattern (for example, LastName Like 'Smit\*').</span></span>

### <a name="filtering-with-a-constant"></a><span data-ttu-id="e8e60-202">Фильтрация с использованием константа</span><span class="sxs-lookup"><span data-stu-id="e8e60-202">Filtering with a constant</span></span>

<span data-ttu-id="e8e60-203">Следующие константы доступны для фильтрации **наборов записей**.</span><span class="sxs-lookup"><span data-stu-id="e8e60-203">The following constants are available for filtering **Recordsets**.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="e8e60-204">Константа</span><span class="sxs-lookup"><span data-stu-id="e8e60-204">Constant</span></span></p></th>
<th><p><span data-ttu-id="e8e60-205">Описание</span><span class="sxs-lookup"><span data-stu-id="e8e60-205">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e8e60-206"><strong>adFilterAffectedRecords</strong></span><span class="sxs-lookup"><span data-stu-id="e8e60-206"><strong>adFilterAffectedRecords</strong></span></span></p></td>
<td><p><span data-ttu-id="e8e60-207">Фильтры для просмотра только записи, относится при последнем вызове <strong>Удаление</strong>, <strong>выполнить повторную синхронизацию</strong>, <strong>UpdateBatch</strong>или <strong>CancelBatch</strong> .</span><span class="sxs-lookup"><span data-stu-id="e8e60-207">Filters for viewing only records effected by the last <strong>Delete</strong>, <strong>Resync</strong>, <strong>UpdateBatch</strong>, or <strong>CancelBatch</strong> call.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e8e60-208"><strong>adFilterConflictingRecords</strong></span><span class="sxs-lookup"><span data-stu-id="e8e60-208"><strong>adFilterConflictingRecords</strong></span></span></p></td>
<td><p><span data-ttu-id="e8e60-209">Фильтры для просмотра записей, которые не удалось последнего обновления пакета.</span><span class="sxs-lookup"><span data-stu-id="e8e60-209">Filters for viewing the records that failed the last batch update.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e8e60-210"><strong>adFilterFetchedRecords</strong></span><span class="sxs-lookup"><span data-stu-id="e8e60-210"><strong>adFilterFetchedRecords</strong></span></span></p></td>
<td><p><span data-ttu-id="e8e60-211">Фильтры для просмотра записей в кэше текущего — то есть, результаты последнего звонка для извлечения записей из базы данных.</span><span class="sxs-lookup"><span data-stu-id="e8e60-211">Filters for viewing the records in the current cache — that is, the results of the last call to retrieve records from the database.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e8e60-212"><strong>adFilterNone</strong></span><span class="sxs-lookup"><span data-stu-id="e8e60-212"><strong>adFilterNone</strong></span></span></p></td>
<td><p><span data-ttu-id="e8e60-213">Удаляет текущий фильтр и восстанавливает все записи для просмотра.</span><span class="sxs-lookup"><span data-stu-id="e8e60-213">Removes the current filter and restores all records for viewing.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e8e60-214"><strong>adFilterPendingRecords</strong></span><span class="sxs-lookup"><span data-stu-id="e8e60-214"><strong>adFilterPendingRecords</strong></span></span></p></td>
<td><p><span data-ttu-id="e8e60-215">Фильтры для просмотра только записей, были изменены, но еще не были отправлены на сервер.</span><span class="sxs-lookup"><span data-stu-id="e8e60-215">Filters for viewing only records that have changed but have not yet been sent to the server.</span></span> <span data-ttu-id="e8e60-216">Применимо только к режим пакетного обновления.</span><span class="sxs-lookup"><span data-stu-id="e8e60-216">Applicable only for batch update mode.</span></span></p></td>
</tr>
</tbody>
</table>

<br/>

<span data-ttu-id="e8e60-217">Константы фильтра упростить конфликтов отдельных записей в режиме пакетного обновления, позволяя просматривать, например позвонить только те записи, которые были относится во время последнего метода **UpdateBatch** , как показано в следующем примере:</span><span class="sxs-lookup"><span data-stu-id="e8e60-217">The filter constants make it easier to resolve individual record conflicts during batch update mode by allowing you to view, for example, only those records that were effected during the last **UpdateBatch** method call, as shown in the following example:</span></span>

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

### <a name="filtering-with-bookmarks"></a><span data-ttu-id="e8e60-218">Фильтрация с помощью закладок</span><span class="sxs-lookup"><span data-stu-id="e8e60-218">Filtering with bookmarks</span></span>

<span data-ttu-id="e8e60-219">И, наконец вы можете передать массив вариантов закладок свойство **фильтра** .</span><span class="sxs-lookup"><span data-stu-id="e8e60-219">Finally, you can pass a variant array of bookmarks to the **Filter** property.</span></span> <span data-ttu-id="e8e60-220">Итоговый курсор будет содержать только записей, чьи закладку был передан в свойство.</span><span class="sxs-lookup"><span data-stu-id="e8e60-220">The resulting cursor will contain only those records whose bookmark was passed in to the property.</span></span> <span data-ttu-id="e8e60-221">В следующем примере кода создается массив закладки из записей в наборе **записей** , которые имеют «Б» в поле *имя продукта* .</span><span class="sxs-lookup"><span data-stu-id="e8e60-221">The following code example creates an array of bookmarks from the records in a **Recordset** which have a "B" in the *ProductName* field.</span></span> <span data-ttu-id="e8e60-222">Затем передает массив в свойство **фильтра** и отображается информация о результирующего **набора записей**.</span><span class="sxs-lookup"><span data-stu-id="e8e60-222">It then passes the array to the **Filter** property and displays information about the resulting filtered **Recordset**.</span></span>

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

## <a name="creating-a-clone-of-a-recordset"></a><span data-ttu-id="e8e60-223">Создание копии набора записей</span><span class="sxs-lookup"><span data-stu-id="e8e60-223">Creating a clone of a Recordset</span></span>

<span data-ttu-id="e8e60-224">Используйте метод **клонированной** для создания нескольких дубликатов объектов **набора записей** , особенно в том случае, если вы хотите поддерживать более одного текущей записи в данного набора записей.</span><span class="sxs-lookup"><span data-stu-id="e8e60-224">Use the **Clone** method to create multiple, duplicate **Recordset** objects, particularly if you want to maintain more than one current record in a given set of records.</span></span> <span data-ttu-id="e8e60-225">С помощью метода **клонированной** эффективнее, чем создания и открытия нового объекта **набора записей** с тем же определением, что и исходный.</span><span class="sxs-lookup"><span data-stu-id="e8e60-225">Using the **Clone** method is more efficient than creating and opening a new **Recordset** object with the same definition as the original.</span></span>

<span data-ttu-id="e8e60-226">Текущая запись только что созданный клонированной изначально присвоено значение первой записи.</span><span class="sxs-lookup"><span data-stu-id="e8e60-226">The current record of a newly created clone is originally set to the first record.</span></span> <span data-ttu-id="e8e60-227">Указатель текущей записи в клонированной **записей** не синхронизируются с исходной или наоборот.</span><span class="sxs-lookup"><span data-stu-id="e8e60-227">The current record pointer in a cloned **Recordset** is not synchronized with the original or vice versa.</span></span> <span data-ttu-id="e8e60-228">Можно перемещаться независимо друг от друга в каждом **набора записей**.</span><span class="sxs-lookup"><span data-stu-id="e8e60-228">You can navigate independently in each **Recordset**.</span></span>

<span data-ttu-id="e8e60-229">Изменения, внесенные на **один Recordset** видны во всех его копирует вне зависимости от типа курсора.</span><span class="sxs-lookup"><span data-stu-id="e8e60-229">Changes you make to one **Recordset** object are visible in all of its clones regardless of cursor type.</span></span> <span data-ttu-id="e8e60-230">Тем не менее после выполнения [запроса](requery-method-ado.md) на исходный **набора записей**копирует больше не синхронизируются с исходным.</span><span class="sxs-lookup"><span data-stu-id="e8e60-230">However, after you execute [Requery](requery-method-ado.md) on the original **Recordset**, the clones will no longer be synchronized to the original.</span></span>

<span data-ttu-id="e8e60-231">Закрытие исходного **набора записей** не закрывайте его копии, а также закрывая копии закрыть исходной или любых других копий.</span><span class="sxs-lookup"><span data-stu-id="e8e60-231">Closing the original **Recordset** does not close its copies, nor does closing a copy close the original or any of the other copies.</span></span>

<span data-ttu-id="e8e60-232">Объект **набора записей** можно скопировать только в том случае, если он поддерживает закладки.</span><span class="sxs-lookup"><span data-stu-id="e8e60-232">You can clone a **Recordset** object only if it supports bookmarks.</span></span> <span data-ttu-id="e8e60-233">Значения закладки являются взаимозаменяемыми; Таким образом закладка ссылку из одного объекта **набора записей** относится к одной и той же записи в любом из его копирует.</span><span class="sxs-lookup"><span data-stu-id="e8e60-233">Bookmark values are interchangeable; that is, a bookmark reference from one **Recordset** object refers to the same record in any of its clones.</span></span>


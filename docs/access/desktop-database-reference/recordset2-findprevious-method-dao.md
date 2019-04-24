---
title: Метод Recordset2. FindPrevious (DAO)
TOCTitle: FindPrevious Method
ms:assetid: ec35faf4-20f2-a83f-54e4-ac1f66c3c2be
ms:mtpsurl: https://msdn.microsoft.com/library/Ff836294(v=office.15)
ms:contentKeyID: 48548509
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 9cf53526f9643737c7236bb2c98589e74f3f2eb5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32307317"
---
# <a name="recordset2findprevious-method-dao"></a><span data-ttu-id="e1238-102">Метод Recordset2. FindPrevious (DAO)</span><span class="sxs-lookup"><span data-stu-id="e1238-102">Recordset2.FindPrevious method (DAO)</span></span>

<span data-ttu-id="e1238-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="e1238-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="e1238-104">Определяет положение предыдущей записи в объекте **[Recordset](recordset-object-dao.md)** типа dynaset или мгновенный снимок, которая отвечает заданным условиям и превращает запись в текущую запись (только для рабочих областей Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="e1238-104">Locates the previous record in a dynaset- or snapshot-type **[Recordset](recordset-object-dao.md)** object that satisfies the specified criteria and makes that record the current record (Microsoft Access workspaces only).</span></span> <span data-ttu-id="e1238-105">.</span><span class="sxs-lookup"><span data-stu-id="e1238-105"></span></span>

## <a name="syntax"></a><span data-ttu-id="e1238-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e1238-106">Syntax</span></span>

<span data-ttu-id="e1238-107">*Expression* . FindPrevious (***критерии***)</span><span class="sxs-lookup"><span data-stu-id="e1238-107">*expression* .FindPrevious(***Criteria***)</span></span>

<span data-ttu-id="e1238-108">*Expression (выражение* ) Переменная, представляющая объект **Recordset2** .</span><span class="sxs-lookup"><span data-stu-id="e1238-108">*expression* A variable that represents a **Recordset2** object.</span></span>

## <a name="parameters"></a><span data-ttu-id="e1238-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="e1238-109">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="e1238-110">Имя</span><span class="sxs-lookup"><span data-stu-id="e1238-110">Name</span></span></p></th>
<th><p><span data-ttu-id="e1238-111">Обязательно/необязательно</span><span class="sxs-lookup"><span data-stu-id="e1238-111">Required/optional</span></span></p></th>
<th><p><span data-ttu-id="e1238-112">Тип данных</span><span class="sxs-lookup"><span data-stu-id="e1238-112">Data type</span></span></p></th>
<th><p><span data-ttu-id="e1238-113">Описание</span><span class="sxs-lookup"><span data-stu-id="e1238-113">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e1238-114"><em>Критерий</em></span><span class="sxs-lookup"><span data-stu-id="e1238-114"><em>Criteria</em></span></span></p></td>
<td><p><span data-ttu-id="e1238-115">Обязательный</span><span class="sxs-lookup"><span data-stu-id="e1238-115">Required</span></span></p></td>
<td><p><span data-ttu-id="e1238-116"><strong>String</strong></span><span class="sxs-lookup"><span data-stu-id="e1238-116"><strong>String</strong></span></span></p></td>
<td><p><span data-ttu-id="e1238-117">Строка, используемая для обнаружения записи.</span><span class="sxs-lookup"><span data-stu-id="e1238-117">A String used to locate the record.</span></span> <span data-ttu-id="e1238-118">Оно аналогично предложению WHERE в операторе SQL, но без слова WHERE.</span><span class="sxs-lookup"><span data-stu-id="e1238-118">It is like the WHERE clause in an SQL statement, but without the word WHERE.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="e1238-119">Замечания</span><span class="sxs-lookup"><span data-stu-id="e1238-119">Remarks</span></span>

<span data-ttu-id="e1238-120">Если вы хотите включить в Поиск все записи, а не только те, которые соответствуют определенному условию, используйте методы **Move** для перемещения записей в записи.</span><span class="sxs-lookup"><span data-stu-id="e1238-120">If you want to include all the records in your search — not just those that meet a specific condition — use the **Move** methods to move from record to record.</span></span> <span data-ttu-id="e1238-121">Чтобы найти запись в **наборе записей**табличного типа, используйте метод **Seek** .</span><span class="sxs-lookup"><span data-stu-id="e1238-121">To locate a record in a table-type **Recordset**, use the **Seek** method.</span></span>

<span data-ttu-id="e1238-122">Если запись, соответствующая критериям, не найдена, то указатель текущей записи неизвестен, \*\*\*\* а для свойства "несовпадение" задано **значение true**.</span><span class="sxs-lookup"><span data-stu-id="e1238-122">If a record matching the criteria isn't located, the current record pointer is unknown, and the **NoMatch** property is set to **True**.</span></span> <span data-ttu-id="e1238-123">Если объект Recordset содержит несколько записей, удовлетворяющих критериям, **FindFirst** ищет первое вхождение, **FindNext** определяет расположение следующего вхождения и т. д.</span><span class="sxs-lookup"><span data-stu-id="e1238-123">If recordset contains more than one record that satisfies the criteria, **FindFirst** locates the first occurrence, **FindNext** locates the next occurrence, and so on.</span></span>

<span data-ttu-id="e1238-124">Каждый из методов **Find** начинает поиск из расположения и в направлении, указанном в приведенной ниже таблице.</span><span class="sxs-lookup"><span data-stu-id="e1238-124">Each of the **Find** methods begins its search from the location and in the direction specified in the following table.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="e1238-125">Метод Find</span><span class="sxs-lookup"><span data-stu-id="e1238-125">Find method</span></span></p></th>
<th><p><span data-ttu-id="e1238-126">Начинает поиск по адресу</span><span class="sxs-lookup"><span data-stu-id="e1238-126">Begins searching at</span></span></p></th>
<th><p><span data-ttu-id="e1238-127">Направление поиска</span><span class="sxs-lookup"><span data-stu-id="e1238-127">Search direction</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e1238-128"><strong>FindFirst</strong></span><span class="sxs-lookup"><span data-stu-id="e1238-128"><strong>FindFirst</strong></span></span></p></td>
<td><p><span data-ttu-id="e1238-129">Начало набора записей</span><span class="sxs-lookup"><span data-stu-id="e1238-129">Beginning of recordset</span></span></p></td>
<td><p><span data-ttu-id="e1238-130">Конец объекта Recordset</span><span class="sxs-lookup"><span data-stu-id="e1238-130">End of recordset</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e1238-131"><strong>FindLast</strong></span><span class="sxs-lookup"><span data-stu-id="e1238-131"><strong>FindLast</strong></span></span></p></td>
<td><p><span data-ttu-id="e1238-132">Конец объекта Recordset</span><span class="sxs-lookup"><span data-stu-id="e1238-132">End of recordset</span></span></p></td>
<td><p><span data-ttu-id="e1238-133">Начало набора записей</span><span class="sxs-lookup"><span data-stu-id="e1238-133">Beginning of recordset</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e1238-134"><strong>FindNext</strong></span><span class="sxs-lookup"><span data-stu-id="e1238-134"><strong>FindNext</strong></span></span></p></td>
<td><p><span data-ttu-id="e1238-135">Текущая запись</span><span class="sxs-lookup"><span data-stu-id="e1238-135">Current record</span></span></p></td>
<td><p><span data-ttu-id="e1238-136">Конец объекта Recordset</span><span class="sxs-lookup"><span data-stu-id="e1238-136">End of recordset</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e1238-137"><strong>FindPrevious</strong></span><span class="sxs-lookup"><span data-stu-id="e1238-137"><strong>FindPrevious</strong></span></span></p></td>
<td><p><span data-ttu-id="e1238-138">Текущая запись</span><span class="sxs-lookup"><span data-stu-id="e1238-138">Current record</span></span></p></td>
<td><p><span data-ttu-id="e1238-139">Начало набора записей</span><span class="sxs-lookup"><span data-stu-id="e1238-139">Beginning of recordset</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="e1238-140">При использовании одного из методов **Find** не то же, что и при использовании метода **Move** , тем не менее, это означает, что первый, последний, следующий или предыдущий записи Current без указания условия.</span><span class="sxs-lookup"><span data-stu-id="e1238-140">Using one of the **Find** methods isn't the same as using a **Move** method, however, which simply makes the first, last, next, or previous record current without specifying a condition.</span></span> <span data-ttu-id="e1238-141">Вы можете выполнить операцию поиска с операцией перемещения.</span><span class="sxs-lookup"><span data-stu-id="e1238-141">You can follow a Find operation with a Move operation.</span></span>

<span data-ttu-id="e1238-142">Всегда проверяйте значение свойства " \*\*\*\* Несопоставленный", чтобы определить, была ли операция поиска выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="e1238-142">Always check the value of the **NoMatch** property to determine whether the Find operation has succeeded.</span></span> <span data-ttu-id="e1238-143">Если поиск выполнен успешно, то \*\*\*\* параметр "несоответствие" имеет **значение "false**".</span><span class="sxs-lookup"><span data-stu-id="e1238-143">If the search succeeds, **NoMatch** is **False**.</span></span> <span data-ttu-id="e1238-144">Если произошел сбой \*\*\*\* , параметр unпоискпоз имеет **значение true** , а текущая запись не определена.</span><span class="sxs-lookup"><span data-stu-id="e1238-144">If it fails, **NoMatch** is **True** and the current record isn't defined.</span></span> <span data-ttu-id="e1238-145">В этом случае необходимо вернуть указатель текущей записи к допустимой записи.</span><span class="sxs-lookup"><span data-stu-id="e1238-145">In this case, you must position the current record pointer back to a valid record.</span></span>

<span data-ttu-id="e1238-146">Использование методов **Find** с ядром СУБД Microsoft Access — это могут быть неэффективными наборы записей, доступ к которым осуществляется с помощью ODBC.</span><span class="sxs-lookup"><span data-stu-id="e1238-146">Using the **Find** methods with Microsoft Access database engine-connected ODBC-accessed recordsets can be inefficient.</span></span> <span data-ttu-id="e1238-147">Возможно, вы обнаружите, что заменяя критерии для поиска определенной записи быстрее, особенно при работе с большими наборами записей.</span><span class="sxs-lookup"><span data-stu-id="e1238-147">You may find that rephrasing your criteria to locate a specific record is faster, especially when working with large recordsets.</span></span>

<span data-ttu-id="e1238-148">При работе с базами данных ODBC, подключенными к ядру СУБД Microsoft Access, и большими объектами **Recordset** типа динамического подмножества данных можно обнаружить, что использование методов **Find** или свойства **Sort** или **Filter** — медленное.</span><span class="sxs-lookup"><span data-stu-id="e1238-148">When working with Microsoft Access database engine-connected ODBC databases and large dynaset-type **Recordset** objects, you might discover that using the **Find** methods or using the **Sort** or **Filter** property is slow.</span></span> <span data-ttu-id="e1238-149">Для повышения производительности используйте SQL запросы с настраиваемыми предложениями ORDER BY или WHERE, запросами с параметрами или объектами **QueryDef** , которые извлекают определенные индексированные записи.</span><span class="sxs-lookup"><span data-stu-id="e1238-149">To improve performance, use SQL queries with customized ORDER BY or WHERE clauses, parameter queries, or **QueryDef** objects that retrieve specific indexed records.</span></span>

<span data-ttu-id="e1238-150">При поиске полей, содержащих даты, следует использовать формат даты США (month-day-year), даже если не используется американский вариант ядра СУБД Microsoft Access. в противном случае данные могут быть не найдены.</span><span class="sxs-lookup"><span data-stu-id="e1238-150">You should use the U.S. date format (month-day-year) when you search for fields containing dates, even if you're not using the U.S. version of the Microsoft Access database engine; otherwise, the data may not be found.</span></span> <span data-ttu-id="e1238-151">Для преобразования даты используйте функцию **Format** в Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="e1238-151">Use the Visual Basic **Format** function to convert the date.</span></span> <span data-ttu-id="e1238-152">Пример:</span><span class="sxs-lookup"><span data-stu-id="e1238-152">For example:</span></span>

```vb
rstEmployees.FindFirst "HireDate > #" _ 
        & Format(mydate, 'm-d-yy' ) & "#" 
```

<span data-ttu-id="e1238-153">Если критерии состоят из строки, сцепленной со значением, не являющимся целым числом, а системные параметры задают символ, отличный от U. S. Decimal (например, Стрскл = "PRICE \> " _амп_ Лнгприце и лнгприце = 125, 50), возникает ошибка при попытке Вызовите метод.</span><span class="sxs-lookup"><span data-stu-id="e1238-153">If criteria is composed of a string concatenated with a non-integer value, and the system parameters specify a non-U.S. decimal character such as a comma (for example, strSQL = "PRICE \> " & lngPrice, and lngPrice = 125,50), an error occurs when you try to call the method.</span></span> <span data-ttu-id="e1238-154">Это вызвано тем, что во время сцепления число преобразуется в строку с использованием десятичного знака системы, а Microsoft Access SQL принимает только десятичные знаки США.</span><span class="sxs-lookup"><span data-stu-id="e1238-154">This is because during concatenation, the number will be converted to a string using your system's default decimal character, and Microsoft Access SQL only accepts U.S. decimal characters.</span></span>

> [!NOTE]
> - <span data-ttu-id="e1238-155">Для достижения оптимальной производительности *критерий*\* должен быть в форме "*значение\*\*поля* = ", где *поле* — это индексированное поле в базовой базовой таблице, или "поле (например,"*поле* *префикс*") \*\* Индексированное поле в базовой базовой таблице, а *префикс* — это строка поиска префикса (например, "Art \*").</span><span class="sxs-lookup"><span data-stu-id="e1238-155">For best performance, the *criteria*\* should be in either the form "*field* = *value*" where *field* is an indexed field in the underlying base table, or "*field* LIKE *prefix*" where *field* is an indexed field in the underlying base table and *prefix* is a prefix search string (for example, "ART\*").</span></span>
> - <span data-ttu-id="e1238-156">Как правило, для эквивалентных типов поиска метод **Seek** обеспечивает лучшую производительность, чем методы **Find** .</span><span class="sxs-lookup"><span data-stu-id="e1238-156">In general, for equivalent types of searches, the **Seek** method provides better performance than the **Find** methods.</span></span> <span data-ttu-id="e1238-157">Предполагается, что только объекты **Recordset** табличного типа могут удовлетворять вашим потребностям.</span><span class="sxs-lookup"><span data-stu-id="e1238-157">This assumes that table-type **Recordset** objects alone can satisfy your needs.</span></span>



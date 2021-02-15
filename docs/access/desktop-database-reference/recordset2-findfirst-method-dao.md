---
title: Метод Recordset2.FindFirst (DAO)
TOCTitle: FindFirst Method
ms:assetid: 2a18e81a-a9e5-cc1a-50b2-40c1f1b7fa06
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192064(v=office.15)
ms:contentKeyID: 48543902
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 823a9b0e095bb726d749021cca99d26f1cc8ceba
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32309410"
---
# <a name="recordset2findfirst-method-dao"></a><span data-ttu-id="30dd5-102">Метод Recordset2.FindFirst (DAO)</span><span class="sxs-lookup"><span data-stu-id="30dd5-102">Recordset2.FindFirst method (DAO)</span></span>

<span data-ttu-id="30dd5-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="30dd5-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="30dd5-104">Определяет положение первой записи в объекте **Recordset** типа "Динамический набор" или "Статический набор", которая отвечает заданным условиям и превращает запись в текущую запись (только для рабочих областей Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="30dd5-104">Locates the first record in a dynaset- or snapshot-type **Recordset** object that satisfies the specified criteria and makes that record the current record (Microsoft Access workspaces only).</span></span>

## <a name="syntax"></a><span data-ttu-id="30dd5-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="30dd5-105">Syntax</span></span>

<span data-ttu-id="30dd5-106">*выражение* .FindFirst(***Criteria***)</span><span class="sxs-lookup"><span data-stu-id="30dd5-106">*expression* .FindFirst(***Criteria***)</span></span>

<span data-ttu-id="30dd5-107">*выражение* Переменная, представляюная объект **Recordset2.**</span><span class="sxs-lookup"><span data-stu-id="30dd5-107">*expression* A variable that represents a **Recordset2** object.</span></span>

## <a name="parameters"></a><span data-ttu-id="30dd5-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="30dd5-108">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="30dd5-109">Имя</span><span class="sxs-lookup"><span data-stu-id="30dd5-109">Name</span></span></p></th>
<th><p><span data-ttu-id="30dd5-110">Обязательный/необязательный</span><span class="sxs-lookup"><span data-stu-id="30dd5-110">Required/optional</span></span></p></th>
<th><p><span data-ttu-id="30dd5-111">Тип данных</span><span class="sxs-lookup"><span data-stu-id="30dd5-111">Data type</span></span></p></th>
<th><p><span data-ttu-id="30dd5-112">Описание</span><span class="sxs-lookup"><span data-stu-id="30dd5-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="30dd5-113"><em>Criteria</em></span><span class="sxs-lookup"><span data-stu-id="30dd5-113"><em>Criteria</em></span></span></p></td>
<td><p><span data-ttu-id="30dd5-114">Обязательный</span><span class="sxs-lookup"><span data-stu-id="30dd5-114">Required</span></span></p></td>
<td><p><span data-ttu-id="30dd5-115"><strong>String</strong></span><span class="sxs-lookup"><span data-stu-id="30dd5-115"><strong>String</strong></span></span></p></td>
<td><p><span data-ttu-id="30dd5-116">Строка, используемая для поиска записи.</span><span class="sxs-lookup"><span data-stu-id="30dd5-116">A String used to locate the record.</span></span> <span data-ttu-id="30dd5-117">Аналогично предложению WHERE в инструкции SQL, но без слова WHERE.</span><span class="sxs-lookup"><span data-stu-id="30dd5-117">It is like the WHERE clause in an SQL statement, but without the word WHERE.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="30dd5-118">Примечания</span><span class="sxs-lookup"><span data-stu-id="30dd5-118">Remarks</span></span>

<span data-ttu-id="30dd5-119">Если в поиск нужно включить все записи, а не только те, которые удовлетворяют заданному условию, используйте методы **Move**, чтобы переходить между записями.</span><span class="sxs-lookup"><span data-stu-id="30dd5-119">If you want to include all the records in your search — not just those that meet a specific condition — use the **Move** methods to move from record to record.</span></span> <span data-ttu-id="30dd5-120">Для поиска записи в объекте **Recordset** табличного типа используется метод **Seek**.</span><span class="sxs-lookup"><span data-stu-id="30dd5-120">To locate a record in a table-type **Recordset**, use the **Seek** method.</span></span>

<span data-ttu-id="30dd5-121">Если соответствующая условиям запись не найдена, то указатель текущей записи неизвестен, а свойству **NoMatch** присваивается значение **True**.</span><span class="sxs-lookup"><span data-stu-id="30dd5-121">If a record matching the criteria isn't located, the current record pointer is unknown, and the **NoMatch** property is set to **True**.</span></span> <span data-ttu-id="30dd5-122">Если набор записей содержит несколько записей, удовлетворяющих условиям, **FindFirst** находит первое вхождение, **FindNext** находит следующее вхождение и т. д.</span><span class="sxs-lookup"><span data-stu-id="30dd5-122">If recordset contains more than one record that satisfies the criteria, **FindFirst** locates the first occurrence, **FindNext** locates the next occurrence, and so on.</span></span>

<span data-ttu-id="30dd5-123">В приведенной ниже таблице показано, с какого расположения и в каком направлении выполняют поиск разные методы **Find**.</span><span class="sxs-lookup"><span data-stu-id="30dd5-123">Each of the **Find** methods begins its search from the location and in the direction specified in the following table.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="30dd5-124">Метод Find</span><span class="sxs-lookup"><span data-stu-id="30dd5-124">Find method</span></span></p></th>
<th><p><span data-ttu-id="30dd5-125">Начало поиска</span><span class="sxs-lookup"><span data-stu-id="30dd5-125">Begins searching at</span></span></p></th>
<th><p><span data-ttu-id="30dd5-126">Направление поиска</span><span class="sxs-lookup"><span data-stu-id="30dd5-126">Search direction</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="30dd5-127"><strong>FindFirst</strong></span><span class="sxs-lookup"><span data-stu-id="30dd5-127"><strong>FindFirst</strong></span></span></p></td>
<td><p><span data-ttu-id="30dd5-128">Начало набора записей</span><span class="sxs-lookup"><span data-stu-id="30dd5-128">Beginning of recordset</span></span></p></td>
<td><p><span data-ttu-id="30dd5-129">Конец набора записей</span><span class="sxs-lookup"><span data-stu-id="30dd5-129">End of recordset</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="30dd5-130"><strong>FindLast</strong></span><span class="sxs-lookup"><span data-stu-id="30dd5-130"><strong>FindLast</strong></span></span></p></td>
<td><p><span data-ttu-id="30dd5-131">Конец набора записей</span><span class="sxs-lookup"><span data-stu-id="30dd5-131">End of recordset</span></span></p></td>
<td><p><span data-ttu-id="30dd5-132">Начало набора записей</span><span class="sxs-lookup"><span data-stu-id="30dd5-132">Beginning of recordset</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="30dd5-133"><strong>FindNext</strong></span><span class="sxs-lookup"><span data-stu-id="30dd5-133"><strong>FindNext</strong></span></span></p></td>
<td><p><span data-ttu-id="30dd5-134">Текущая запись</span><span class="sxs-lookup"><span data-stu-id="30dd5-134">Current record</span></span></p></td>
<td><p><span data-ttu-id="30dd5-135">Конец набора записей</span><span class="sxs-lookup"><span data-stu-id="30dd5-135">End of recordset</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="30dd5-136"><strong>FindPrevious</strong></span><span class="sxs-lookup"><span data-stu-id="30dd5-136"><strong>FindPrevious</strong></span></span></p></td>
<td><p><span data-ttu-id="30dd5-137">Текущая запись</span><span class="sxs-lookup"><span data-stu-id="30dd5-137">Current record</span></span></p></td>
<td><p><span data-ttu-id="30dd5-138">Начало набора записей</span><span class="sxs-lookup"><span data-stu-id="30dd5-138">Beginning of recordset</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="30dd5-139">Однако использование методов **Find** отличается от использования метода **Move**, который просто делает первую, последнюю, следующую или предыдущую запись текущей без указания условия.</span><span class="sxs-lookup"><span data-stu-id="30dd5-139">Using one of the **Find** methods isn't the same as using a **Move** method, however, which simply makes the first, last, next, or previous record current without specifying a condition.</span></span> <span data-ttu-id="30dd5-140">После операции Find можно выполнить операцию Move.</span><span class="sxs-lookup"><span data-stu-id="30dd5-140">You can follow a Find operation with a Move operation.</span></span>

<span data-ttu-id="30dd5-141">Всегда проверяйте значение свойства **NoMatch**, чтобы определить, успешно ли выполнена операция Find.</span><span class="sxs-lookup"><span data-stu-id="30dd5-141">Always check the value of the **NoMatch** property to determine whether the Find operation has succeeded.</span></span> <span data-ttu-id="30dd5-142">Если поиск выполнен успешно, свойство **NoMatch** принимает значение **False**.</span><span class="sxs-lookup"><span data-stu-id="30dd5-142">If the search succeeds, **NoMatch** is **False**.</span></span> <span data-ttu-id="30dd5-143">Если поиск не дал результатов, то свойство **NoMatch** принимает значение **True**, а текущая запись не определяется.</span><span class="sxs-lookup"><span data-stu-id="30dd5-143">If it fails, **NoMatch** is **True** and the current record isn't defined.</span></span> <span data-ttu-id="30dd5-144">В этом случае необходимо вернуть указатель текущей записи к допустимой записи.</span><span class="sxs-lookup"><span data-stu-id="30dd5-144">In this case, you must position the current record pointer back to a valid record.</span></span>

<span data-ttu-id="30dd5-145">Использование методов **Find** с наборами записей, доступ к которым осуществляется через ODBC с подключением к ядру СУБД Microsoft Access, может быть неэффективным.</span><span class="sxs-lookup"><span data-stu-id="30dd5-145">Using the **Find** methods with Microsoft Access database engine-connected ODBC-accessed recordsets can be inefficient.</span></span> <span data-ttu-id="30dd5-146">Может оказаться, что изменение условий поиска определенной записи выполняется быстрее, особенно при работе с большими наборами записей.</span><span class="sxs-lookup"><span data-stu-id="30dd5-146">You may find that rephrasing your criteria to locate a specific record is faster, especially when working with large recordsets.</span></span>

<span data-ttu-id="30dd5-147">При работе с базами данных ODBC, подключенными к ядру СУБД Microsoft Access, и большими объектами **Recordset** типа "Динамический набор" можно обнаружить, что использование методов **Find** или свойств **Sort** и **Filter** выполняется медленно.</span><span class="sxs-lookup"><span data-stu-id="30dd5-147">When working with Microsoft Access database engine-connected ODBC databases and large dynaset-type **Recordset** objects, you might discover that using the **Find** methods or using the **Sort** or **Filter** property is slow.</span></span> <span data-ttu-id="30dd5-148">Чтобы повысить производительность, используйте запросы SQL с настроенными предложениями ORDER BY или WHERE, запросы параметров или объекты **QueryDef**, возвращающие определенные индексированные записи.</span><span class="sxs-lookup"><span data-stu-id="30dd5-148">To improve performance, use SQL queries with customized ORDER BY or WHERE clauses, parameter queries, or **QueryDef** objects that retrieve specific indexed records.</span></span>

<span data-ttu-id="30dd5-149">При поиске полей, содержащих даты, следует использовать формат даты, применяемый в США (месяц, день, год), даже если вы не используете версию ядра СУБД Microsoft Access для США. В противном случае данные могут быть не найдены.</span><span class="sxs-lookup"><span data-stu-id="30dd5-149">You should use the U.S. date format (month-day-year) when you search for fields containing dates, even if you're not using the U.S. version of the Microsoft Access database engine; otherwise, the data may not be found.</span></span> <span data-ttu-id="30dd5-150">Используйте функцию **Format** в Visual Basic для преобразования даты.</span><span class="sxs-lookup"><span data-stu-id="30dd5-150">Use the Visual Basic **Format** function to convert the date.</span></span> <span data-ttu-id="30dd5-151">Например:</span><span class="sxs-lookup"><span data-stu-id="30dd5-151">For example:</span></span>

```vb
rstEmployees.FindFirst "HireDate > #" _ 
        & Format(mydate, 'm-d-yy' ) & "#" 
```

<span data-ttu-id="30dd5-152">Если условие состоит из строки, объединенной с нецелочисленным значением, а параметры системы содержат десятичные символы, не используемые в США, например запятую (примеры: strSQL = "PRICE \> " & lngPrice и lngPrice = 125,50), то при попытке вызова метода возникнет ошибка.</span><span class="sxs-lookup"><span data-stu-id="30dd5-152">If criteria is composed of a string concatenated with a non-integer value, and the system parameters specify a non-U.S. decimal character such as a comma (for example, strSQL = "PRICE \> " & lngPrice, and lngPrice = 125,50), an error occurs when you try to call the method.</span></span> <span data-ttu-id="30dd5-153">Это возникает по причине того, что при объединении число будет преобразовано в строку с помощью используемого по умолчанию в вашей системе десятичного символа, а SQL Microsoft Access поддерживает только десятичные символы, используемые в США.</span><span class="sxs-lookup"><span data-stu-id="30dd5-153">This is because during concatenation, the number will be converted to a string using your system's default decimal character, and Microsoft Access SQL only accepts U.S. decimal characters.</span></span>

> [!NOTE]
> - <span data-ttu-id="30dd5-154">Для лучшей производительности критерий **должен* иметь вид *"значение* поля", где поле является индексным полем в базовой таблице, или "префикс LIKE", где поле является индексным полем в базовой таблице, а префикс — строкой поиска префикса  =  (например, "ART*").     </span><span class="sxs-lookup"><span data-stu-id="30dd5-154">For best performance, the *criteria*\* should be in either the form "*field* = *value*" where *field* is an indexed field in the underlying base table, or "*field* LIKE *prefix*" where *field* is an indexed field in the underlying base table and *prefix* is a prefix search string (for example, "ART\*").</span></span>
> - <span data-ttu-id="30dd5-155">Как правило, для эквивалентных типов поиска метод **Seek** обеспечивает более высокую производительность, чем метод **Find**.</span><span class="sxs-lookup"><span data-stu-id="30dd5-155">In general, for equivalent types of searches, the **Seek** method provides better performance than the **Find** methods.</span></span> <span data-ttu-id="30dd5-156">При этом предполагается, что для ваших потребностей будет достаточно объектов **Recordset** табличного типа.</span><span class="sxs-lookup"><span data-stu-id="30dd5-156">This assumes that table-type **Recordset** objects alone can satisfy your needs.</span></span>



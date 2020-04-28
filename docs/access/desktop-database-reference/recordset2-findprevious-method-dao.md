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
# <a name="recordset2findprevious-method-dao"></a><span data-ttu-id="90714-102">Метод Recordset2. FindPrevious (DAO)</span><span class="sxs-lookup"><span data-stu-id="90714-102">Recordset2.FindPrevious method (DAO)</span></span>

<span data-ttu-id="90714-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="90714-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="90714-104">Определяет положение предыдущей записи в объекте **[Recordset](recordset-object-dao.md)** типа dynaset или мгновенный снимок, которая отвечает заданным условиям и превращает запись в текущую запись (только для рабочих областей Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="90714-104">Locates the previous record in a dynaset- or snapshot-type **[Recordset](recordset-object-dao.md)** object that satisfies the specified criteria and makes that record the current record (Microsoft Access workspaces only).</span></span> <span data-ttu-id="90714-105">.</span><span class="sxs-lookup"><span data-stu-id="90714-105">.</span></span>

## <a name="syntax"></a><span data-ttu-id="90714-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="90714-106">Syntax</span></span>

<span data-ttu-id="90714-107">*Expression* . FindPrevious (***критерии***)</span><span class="sxs-lookup"><span data-stu-id="90714-107">*expression* .FindPrevious(***Criteria***)</span></span>

<span data-ttu-id="90714-108">*Expression (выражение* ) Переменная, представляющая объект **Recordset2** .</span><span class="sxs-lookup"><span data-stu-id="90714-108">*expression* A variable that represents a **Recordset2** object.</span></span>

## <a name="parameters"></a><span data-ttu-id="90714-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="90714-109">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="90714-110">Имя</span><span class="sxs-lookup"><span data-stu-id="90714-110">Name</span></span></p></th>
<th><p><span data-ttu-id="90714-111">Обязательный/необязательный</span><span class="sxs-lookup"><span data-stu-id="90714-111">Required/optional</span></span></p></th>
<th><p><span data-ttu-id="90714-112">Тип данных</span><span class="sxs-lookup"><span data-stu-id="90714-112">Data type</span></span></p></th>
<th><p><span data-ttu-id="90714-113">Описание</span><span class="sxs-lookup"><span data-stu-id="90714-113">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="90714-114"><em>Criteria</em></span><span class="sxs-lookup"><span data-stu-id="90714-114"><em>Criteria</em></span></span></p></td>
<td><p><span data-ttu-id="90714-115">Обязательный</span><span class="sxs-lookup"><span data-stu-id="90714-115">Required</span></span></p></td>
<td><p><span data-ttu-id="90714-116"><strong>String</strong></span><span class="sxs-lookup"><span data-stu-id="90714-116"><strong>String</strong></span></span></p></td>
<td><p><span data-ttu-id="90714-117">Строка, используемая для поиска записи.</span><span class="sxs-lookup"><span data-stu-id="90714-117">A String used to locate the record.</span></span> <span data-ttu-id="90714-118">Аналогично предложению WHERE в инструкции SQL, но без слова WHERE.</span><span class="sxs-lookup"><span data-stu-id="90714-118">It is like the WHERE clause in an SQL statement, but without the word WHERE.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="90714-119">Примечания</span><span class="sxs-lookup"><span data-stu-id="90714-119">Remarks</span></span>

<span data-ttu-id="90714-120">Если в поиск нужно включить все записи, а не только те, которые удовлетворяют заданному условию, используйте методы **Move**, чтобы переходить между записями.</span><span class="sxs-lookup"><span data-stu-id="90714-120">If you want to include all the records in your search — not just those that meet a specific condition — use the **Move** methods to move from record to record.</span></span> <span data-ttu-id="90714-121">Для поиска записи в объекте **Recordset** табличного типа используется метод **Seek**.</span><span class="sxs-lookup"><span data-stu-id="90714-121">To locate a record in a table-type **Recordset**, use the **Seek** method.</span></span>

<span data-ttu-id="90714-122">Если соответствующая условиям запись не найдена, то указатель текущей записи неизвестен, а свойству **NoMatch** присваивается значение **True**.</span><span class="sxs-lookup"><span data-stu-id="90714-122">If a record matching the criteria isn't located, the current record pointer is unknown, and the **NoMatch** property is set to **True**.</span></span> <span data-ttu-id="90714-123">Если набор записей содержит несколько записей, удовлетворяющих условиям, **FindFirst** находит первое вхождение, **FindNext** находит следующее вхождение и т. д.</span><span class="sxs-lookup"><span data-stu-id="90714-123">If recordset contains more than one record that satisfies the criteria, **FindFirst** locates the first occurrence, **FindNext** locates the next occurrence, and so on.</span></span>

<span data-ttu-id="90714-124">В приведенной ниже таблице показано, с какого расположения и в каком направлении выполняют поиск разные методы **Find**.</span><span class="sxs-lookup"><span data-stu-id="90714-124">Each of the **Find** methods begins its search from the location and in the direction specified in the following table.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="90714-125">Метод Find</span><span class="sxs-lookup"><span data-stu-id="90714-125">Find method</span></span></p></th>
<th><p><span data-ttu-id="90714-126">Начало поиска</span><span class="sxs-lookup"><span data-stu-id="90714-126">Begins searching at</span></span></p></th>
<th><p><span data-ttu-id="90714-127">Направление поиска</span><span class="sxs-lookup"><span data-stu-id="90714-127">Search direction</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="90714-128"><strong>FindFirst</strong></span><span class="sxs-lookup"><span data-stu-id="90714-128"><strong>FindFirst</strong></span></span></p></td>
<td><p><span data-ttu-id="90714-129">Начало набора записей</span><span class="sxs-lookup"><span data-stu-id="90714-129">Beginning of recordset</span></span></p></td>
<td><p><span data-ttu-id="90714-130">Конец набора записей</span><span class="sxs-lookup"><span data-stu-id="90714-130">End of recordset</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="90714-131"><strong>FindLast</strong></span><span class="sxs-lookup"><span data-stu-id="90714-131"><strong>FindLast</strong></span></span></p></td>
<td><p><span data-ttu-id="90714-132">Конец набора записей</span><span class="sxs-lookup"><span data-stu-id="90714-132">End of recordset</span></span></p></td>
<td><p><span data-ttu-id="90714-133">Начало набора записей</span><span class="sxs-lookup"><span data-stu-id="90714-133">Beginning of recordset</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="90714-134"><strong>FindNext</strong></span><span class="sxs-lookup"><span data-stu-id="90714-134"><strong>FindNext</strong></span></span></p></td>
<td><p><span data-ttu-id="90714-135">Текущая запись</span><span class="sxs-lookup"><span data-stu-id="90714-135">Current record</span></span></p></td>
<td><p><span data-ttu-id="90714-136">Конец набора записей</span><span class="sxs-lookup"><span data-stu-id="90714-136">End of recordset</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="90714-137"><strong>FindPrevious</strong></span><span class="sxs-lookup"><span data-stu-id="90714-137"><strong>FindPrevious</strong></span></span></p></td>
<td><p><span data-ttu-id="90714-138">Текущая запись</span><span class="sxs-lookup"><span data-stu-id="90714-138">Current record</span></span></p></td>
<td><p><span data-ttu-id="90714-139">Начало набора записей</span><span class="sxs-lookup"><span data-stu-id="90714-139">Beginning of recordset</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="90714-140">Однако использование методов **Find** отличается от использования метода **Move**, который просто делает первую, последнюю, следующую или предыдущую запись текущей без указания условия.</span><span class="sxs-lookup"><span data-stu-id="90714-140">Using one of the **Find** methods isn't the same as using a **Move** method, however, which simply makes the first, last, next, or previous record current without specifying a condition.</span></span> <span data-ttu-id="90714-141">После операции Find можно выполнить операцию Move.</span><span class="sxs-lookup"><span data-stu-id="90714-141">You can follow a Find operation with a Move operation.</span></span>

<span data-ttu-id="90714-142">Всегда проверяйте значение свойства **NoMatch**, чтобы определить, успешно ли выполнена операция Find.</span><span class="sxs-lookup"><span data-stu-id="90714-142">Always check the value of the **NoMatch** property to determine whether the Find operation has succeeded.</span></span> <span data-ttu-id="90714-143">Если поиск выполнен успешно, свойство **NoMatch** принимает значение **False**.</span><span class="sxs-lookup"><span data-stu-id="90714-143">If the search succeeds, **NoMatch** is **False**.</span></span> <span data-ttu-id="90714-144">Если поиск не дал результатов, то свойство **NoMatch** принимает значение **True**, а текущая запись не определяется.</span><span class="sxs-lookup"><span data-stu-id="90714-144">If it fails, **NoMatch** is **True** and the current record isn't defined.</span></span> <span data-ttu-id="90714-145">В этом случае необходимо вернуть указатель текущей записи к допустимой записи.</span><span class="sxs-lookup"><span data-stu-id="90714-145">In this case, you must position the current record pointer back to a valid record.</span></span>

<span data-ttu-id="90714-146">Использование методов **Find** с наборами записей, доступ к которым осуществляется через ODBC с подключением к ядру СУБД Microsoft Access, может быть неэффективным.</span><span class="sxs-lookup"><span data-stu-id="90714-146">Using the **Find** methods with Microsoft Access database engine-connected ODBC-accessed recordsets can be inefficient.</span></span> <span data-ttu-id="90714-147">Может оказаться, что изменение условий поиска определенной записи выполняется быстрее, особенно при работе с большими наборами записей.</span><span class="sxs-lookup"><span data-stu-id="90714-147">You may find that rephrasing your criteria to locate a specific record is faster, especially when working with large recordsets.</span></span>

<span data-ttu-id="90714-148">При работе с базами данных ODBC, подключенными к ядру СУБД Microsoft Access, и большими объектами **Recordset** типа "Динамический набор" можно обнаружить, что использование методов **Find** или свойств **Sort** и **Filter** выполняется медленно.</span><span class="sxs-lookup"><span data-stu-id="90714-148">When working with Microsoft Access database engine-connected ODBC databases and large dynaset-type **Recordset** objects, you might discover that using the **Find** methods or using the **Sort** or **Filter** property is slow.</span></span> <span data-ttu-id="90714-149">Чтобы повысить производительность, используйте запросы SQL с настроенными предложениями ORDER BY или WHERE, запросы параметров или объекты **QueryDef**, возвращающие определенные индексированные записи.</span><span class="sxs-lookup"><span data-stu-id="90714-149">To improve performance, use SQL queries with customized ORDER BY or WHERE clauses, parameter queries, or **QueryDef** objects that retrieve specific indexed records.</span></span>

<span data-ttu-id="90714-150">При поиске полей, содержащих даты, следует использовать формат даты, применяемый в США (месяц, день, год), даже если вы не используете версию ядра СУБД Microsoft Access для США. В противном случае данные могут быть не найдены.</span><span class="sxs-lookup"><span data-stu-id="90714-150">You should use the U.S. date format (month-day-year) when you search for fields containing dates, even if you're not using the U.S. version of the Microsoft Access database engine; otherwise, the data may not be found.</span></span> <span data-ttu-id="90714-151">Используйте функцию **Format** в Visual Basic для преобразования даты.</span><span class="sxs-lookup"><span data-stu-id="90714-151">Use the Visual Basic **Format** function to convert the date.</span></span> <span data-ttu-id="90714-152">Например:</span><span class="sxs-lookup"><span data-stu-id="90714-152">For example:</span></span>

```vb
rstEmployees.FindFirst "HireDate > #" _ 
        & Format(mydate, 'm-d-yy' ) & "#" 
```

<span data-ttu-id="90714-153">Если условие состоит из строки, объединенной с нецелочисленным значением, а параметры системы содержат десятичные символы, не используемые в США, например запятую (примеры: strSQL = "PRICE \> " & lngPrice и lngPrice = 125,50), то при попытке вызова метода возникнет ошибка.</span><span class="sxs-lookup"><span data-stu-id="90714-153">If criteria is composed of a string concatenated with a non-integer value, and the system parameters specify a non-U.S. decimal character such as a comma (for example, strSQL = "PRICE \> " & lngPrice, and lngPrice = 125,50), an error occurs when you try to call the method.</span></span> <span data-ttu-id="90714-154">Это возникает по причине того, что при объединении число будет преобразовано в строку с помощью используемого по умолчанию в вашей системе десятичного символа, а SQL Microsoft Access поддерживает только десятичные символы, используемые в США.</span><span class="sxs-lookup"><span data-stu-id="90714-154">This is because during concatenation, the number will be converted to a string using your system's default decimal character, and Microsoft Access SQL only accepts U.S. decimal characters.</span></span>

> [!NOTE]
> - <span data-ttu-id="90714-155">Для достижения оптимальной производительности *критерий*\* должен быть в форме "значение*поля* = *value*", где *поле* — это индексированное поле в базовой базовой таблице, или "*поле* *со стилем*", где *поле* — это индексируемое поле в базовой базовой таблице, а *префикс* — это строка поиска префикса (например, "Art \*").</span><span class="sxs-lookup"><span data-stu-id="90714-155">For best performance, the *criteria*\* should be in either the form "*field* = *value*" where *field* is an indexed field in the underlying base table, or "*field* LIKE *prefix*" where *field* is an indexed field in the underlying base table and *prefix* is a prefix search string (for example, "ART\*").</span></span>
> - <span data-ttu-id="90714-156">Как правило, для эквивалентных типов поиска метод **Seek** обеспечивает более высокую производительность, чем метод **Find**.</span><span class="sxs-lookup"><span data-stu-id="90714-156">In general, for equivalent types of searches, the **Seek** method provides better performance than the **Find** methods.</span></span> <span data-ttu-id="90714-157">При этом предполагается, что для ваших потребностей будет достаточно объектов **Recordset** табличного типа.</span><span class="sxs-lookup"><span data-stu-id="90714-157">This assumes that table-type **Recordset** objects alone can satisfy your needs.</span></span>



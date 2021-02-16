---
title: Фильтрация и отображение элементов папки "Входящие", измененных в прошлом месяце
TOCTitle: Filter and display Inbox items modified in the last month
ms:assetid: ef6004dc-0b5a-4d1f-8937-1384d1dfc1ca
ms:mtpsurl: https://msdn.microsoft.com/library/Ff424482(v=office.15)
ms:contentKeyID: 55119886
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 77fe6e7df4cf67ed1ca2d62b8cf48f1b2873ccbe
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32320295"
---
# <a name="filter-and-display-inbox-items-modified-in-the-last-month"></a><span data-ttu-id="10ab0-102">Фильтрация и отображение элементов папки "Входящие", измененных в прошлом месяце</span><span class="sxs-lookup"><span data-stu-id="10ab0-102">Filter and display Inbox items modified in the last month</span></span>

<span data-ttu-id="10ab0-103">В этом примере показано, как фильтровать и отображать элементы папки "Входящие", которые были изменены в прошлом месяце.</span><span class="sxs-lookup"><span data-stu-id="10ab0-103">This example shows how to filter and display Inbox items that were modified in the last month.</span></span>

## <a name="example"></a><span data-ttu-id="10ab0-104">Пример</span><span class="sxs-lookup"><span data-stu-id="10ab0-104">Example</span></span>

> [!NOTE] 
> <span data-ttu-id="10ab0-105">Приведенный ниже пример кода представляет собой фрагмент из книги [Программирование приложений для Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).</span><span class="sxs-lookup"><span data-stu-id="10ab0-105">The following code example is an excerpt from [Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).</span></span>

<span data-ttu-id="10ab0-106">Язык запросов DASL основан на реализации DASL Microsoft Exchange в Outlook.</span><span class="sxs-lookup"><span data-stu-id="10ab0-106">DAV Searching and Locating (DASL) query language is based on the Microsoft Exchange implementation of DASL in Outlook.</span></span> <span data-ttu-id="10ab0-107">Его можно использовать для возвращения результатов на основе свойств для поисков на уровне элементов в данных папки, например представленных объектом [Table](https://msdn.microsoft.com/library/bb652856\(v=office.15\)).</span><span class="sxs-lookup"><span data-stu-id="10ab0-107">It can be used to return property-based results for item-level searches in folder data, such as that represented by a [Table](https://msdn.microsoft.com/library/bb652856\(v=office.15\)) object.</span></span> <span data-ttu-id="10ab0-108">Фильтры DASL поддерживают сравнение строк, в том числе сопоставление эквивалентности, префиксов, фраз и подстрок, с помощью оператора равенства (=).</span><span class="sxs-lookup"><span data-stu-id="10ab0-108">DASL filters support string comparisons, including equivalence, prefix, phrase, and substring matching, by using the equal (=) operator.</span></span> <span data-ttu-id="10ab0-109">С помощью запросов DASL можно выполнять сравнение и фильтрацию по дате и времени.</span><span class="sxs-lookup"><span data-stu-id="10ab0-109">You can use DASL queries to perform date-time comparison and filtering.</span></span>

<span data-ttu-id="10ab0-p102">Поскольку в запросах DASL сравнение по значению **DateTime** всегда выполняется по стандартному времени по Гринвичу (UTC), для правильного выполнения запроса необходимо преобразовать время местного часового пояса во время по стандарту UTC. Также необходимо преобразовать значение **DateTime** в строковое представление, поскольку фильтры DASL поддерживают сравнение строк. Преобразование значения **DateTime** можно выполнить двумя способами: с помощью метода [LocalTimeToUTC(Object)](https://msdn.microsoft.com/library/bb645832\(v=office.15\)) объекта [Row](https://msdn.microsoft.com/library/bb610126\(v=office.15\)) или с помощью соответствующего макроса Outlook **DateTime**.</span><span class="sxs-lookup"><span data-stu-id="10ab0-p102">Because DASL queries always perform **DateTime** comparisons in Coordinated Universal Time (UTC), you must convert the local time value to UTC if you want the query to operate correctly. You must also convert the **DateTime** value to a string representation because DASL filters support string comparisons. You can make the **DateTime** conversion in two ways: by using the [LocalTimeToUTC(Object)](https://msdn.microsoft.com/library/bb645832\(v=office.15\)) method of the [Row](https://msdn.microsoft.com/library/bb610126\(v=office.15\)) object, or by using Outlook **DateTime** macros to make the conversion.</span></span>

<span data-ttu-id="10ab0-113">В следующей строке кода показано использование метода **LocalTimeToUTC** для преобразования значения свойства **LastModificationTime** (столбец по умолчанию во всех объектах **Item**) в формат UTC.</span><span class="sxs-lookup"><span data-stu-id="10ab0-113">The following line of code shows how to use the **LocalTimeToUTC** method to convert the value of the **LastModificationTime** property (which is a default column in all **Item** objects) to UTC.</span></span>

```csharp
DateTime modified = nextRow.LocalTimeUTC(“LastModificationTime”);
```

<span data-ttu-id="10ab0-114">В следующей таблице перечислены макросы **DateTime**, обеспечивающие возврат отфильтрованных строк, для которых выполнено сравнение заданного свойства **DateTime** с указанными относительной датой или диапазоном дат в формате UTC.</span><span class="sxs-lookup"><span data-stu-id="10ab0-114">The following table lists the **DateTime** macros you can use to return filtered strings that compare the value of a given **DateTime** property with a specified relative date or date range in UTC.</span></span> <span data-ttu-id="10ab0-115">Свойство SchemaName представляет любое допустимое свойство типа **DateTime**, ссылка на которое указывается в пространстве имен.</span><span class="sxs-lookup"><span data-stu-id="10ab0-115">The SchemaName property value represents any valid **DateTime** property referenced by namespace.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="10ab0-116">Макрос</span><span class="sxs-lookup"><span data-stu-id="10ab0-116">Macro</span></span></p></th>
<th><p><span data-ttu-id="10ab0-117">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="10ab0-117">Syntax</span></span></p></th>
<th><p><span data-ttu-id="10ab0-118">Описание</span><span class="sxs-lookup"><span data-stu-id="10ab0-118">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="10ab0-119">today</span><span class="sxs-lookup"><span data-stu-id="10ab0-119">today</span></span></p></td>
<td><p><span data-ttu-id="10ab0-120">%today(“SchemaName”)%</span><span class="sxs-lookup"><span data-stu-id="10ab0-120">%today(“SchemaName”)%</span></span></p></td>
<td><p><span data-ttu-id="10ab0-121">Ограничение элементами со значением свойства SchemaName, соответствующим сегодняшней дате.</span><span class="sxs-lookup"><span data-stu-id="10ab0-121">Restricts for items with a SchemaName property value equal to today.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="10ab0-122">tomorrow</span><span class="sxs-lookup"><span data-stu-id="10ab0-122">tomorrow</span></span></p></td>
<td><p><span data-ttu-id="10ab0-123">%tomorrow(“SchemaName”)%</span><span class="sxs-lookup"><span data-stu-id="10ab0-123">%tomorrow(“SchemaName”)%</span></span></p></td>
<td><p><span data-ttu-id="10ab0-124">Ограничение элементами со значением свойства SchemaName, соответствующим завтрашней дате.</span><span class="sxs-lookup"><span data-stu-id="10ab0-124">Restricts for items with a SchemaName property value equal to tomorrow.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="10ab0-125">yesterday</span><span class="sxs-lookup"><span data-stu-id="10ab0-125">yesterday</span></span></p></td>
<td><p><span data-ttu-id="10ab0-126">%yesterday(“SchemaName”)%</span><span class="sxs-lookup"><span data-stu-id="10ab0-126">%yesterday(“SchemaName”)%</span></span></p></td>
<td><p><span data-ttu-id="10ab0-127">Ограничение элементами со значением свойства SchemaName, соответствующим вчерашней дате.</span><span class="sxs-lookup"><span data-stu-id="10ab0-127">Restricts for items with a SchemaName property value equal to yesterday.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="10ab0-128">next7days</span><span class="sxs-lookup"><span data-stu-id="10ab0-128">next7days</span></span></p></td>
<td><p><span data-ttu-id="10ab0-129">%next7days(“SchemaName”)%</span><span class="sxs-lookup"><span data-stu-id="10ab0-129">%next7days(“SchemaName”)%</span></span></p></td>
<td><p><span data-ttu-id="10ab0-130">Ограничение элементами, для которых значения свойства SchemaName лежат в диапазоне следующих семи дней.</span><span class="sxs-lookup"><span data-stu-id="10ab0-130">Restricts for items with SchemaName property values in a range equivalent to the next seven days.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="10ab0-131">last7days</span><span class="sxs-lookup"><span data-stu-id="10ab0-131">last7days</span></span></p></td>
<td><p><span data-ttu-id="10ab0-132">%last7days(“SchemaName”)%</span><span class="sxs-lookup"><span data-stu-id="10ab0-132">%last7days(“SchemaName”)%</span></span></p></td>
<td><p><span data-ttu-id="10ab0-133">Ограничение элементами, для которых значения свойства SchemaName лежат в диапазоне прошедших семи дней.</span><span class="sxs-lookup"><span data-stu-id="10ab0-133">Restricts for items with SchemaName property values in a range equivalent to the last seven days.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="10ab0-134">nextweek</span><span class="sxs-lookup"><span data-stu-id="10ab0-134">nextweek</span></span></p></td>
<td><p><span data-ttu-id="10ab0-135">%nextweek(“SchemaName”)%</span><span class="sxs-lookup"><span data-stu-id="10ab0-135">%nextweek(“SchemaName”)%</span></span></p></td>
<td><p><span data-ttu-id="10ab0-136">Ограничение элементами, для которых значения свойства SchemaName лежат в диапазоне следующей недели.</span><span class="sxs-lookup"><span data-stu-id="10ab0-136">Restricts for items with SchemaName property values in a range equivalent to next week.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="10ab0-137">thisweek</span><span class="sxs-lookup"><span data-stu-id="10ab0-137">thisweek</span></span></p></td>
<td><p><span data-ttu-id="10ab0-138">%thisweek(“SchemaName”)%</span><span class="sxs-lookup"><span data-stu-id="10ab0-138">%thisweek(“SchemaName”)%</span></span></p></td>
<td><p><span data-ttu-id="10ab0-139">Ограничение элементами, для которых значения свойства SchemaName лежат в диапазоне текущей недели.</span><span class="sxs-lookup"><span data-stu-id="10ab0-139">Restricts for items with SchemaName property values in a range equivalent to this week.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="10ab0-140">lastweek</span><span class="sxs-lookup"><span data-stu-id="10ab0-140">lastweek</span></span></p></td>
<td><p><span data-ttu-id="10ab0-141">%lastweek(“SchemaName”)%</span><span class="sxs-lookup"><span data-stu-id="10ab0-141">%lastweek(“SchemaName”)%</span></span></p></td>
<td><p><span data-ttu-id="10ab0-142">Ограничение элементами, для которых значения свойства SchemaName лежат в диапазоне прошлой недели.</span><span class="sxs-lookup"><span data-stu-id="10ab0-142">Restricts for items with SchemaName property values in a range equivalent to last week.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="10ab0-143">nextmonth</span><span class="sxs-lookup"><span data-stu-id="10ab0-143">nextmonth</span></span></p></td>
<td><p><span data-ttu-id="10ab0-144">%nextmonth(“SchemaName”)%</span><span class="sxs-lookup"><span data-stu-id="10ab0-144">%nextmonth(“SchemaName”)%</span></span></p></td>
<td><p><span data-ttu-id="10ab0-145">Ограничение элементами, для которых значения свойства SchemaName лежат в диапазоне следующего месяца.</span><span class="sxs-lookup"><span data-stu-id="10ab0-145">Restricts for items with SchemaName property values in a range equivalent to next month.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="10ab0-146">thismonth</span><span class="sxs-lookup"><span data-stu-id="10ab0-146">thismonth</span></span></p></td>
<td><p><span data-ttu-id="10ab0-147">%thismonth(“SchemaName”)%</span><span class="sxs-lookup"><span data-stu-id="10ab0-147">%thismonth(“SchemaName”)%</span></span></p></td>
<td><p><span data-ttu-id="10ab0-148">Ограничение элементами, для которых значения свойства SchemaName лежат в диапазоне текущего месяца.</span><span class="sxs-lookup"><span data-stu-id="10ab0-148">Restricts for items with SchemaName property values in a range equivalent to this month.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="10ab0-149">lastmonth</span><span class="sxs-lookup"><span data-stu-id="10ab0-149">lastmonth</span></span></p></td>
<td><p><span data-ttu-id="10ab0-150">%lastmonth(“SchemaName”)%</span><span class="sxs-lookup"><span data-stu-id="10ab0-150">%lastmonth(“SchemaName”)%</span></span></p></td>
<td><p><span data-ttu-id="10ab0-151">Ограничение элементами, для которых значения свойства SchemaName лежат в диапазоне прошлого месяца.</span><span class="sxs-lookup"><span data-stu-id="10ab0-151">Restricts for items with SchemaName property values in a range equivalent to last month.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="10ab0-152">В следующем примере в процедуре DemoDASLDateMacro создается запрос DASL, в котором используется макрос **lastmonthDateTime** для фильтрации элементов в папке "Входящие" пользователя, измененных в прошлом месяце.</span><span class="sxs-lookup"><span data-stu-id="10ab0-152">In the following example, DemoDASLDateMacro creates a DASL query that uses the **lastmonthDateTime** macro to filter for items in the user’s Inbox that were modified in the last month.</span></span> <span data-ttu-id="10ab0-153">Затем создается объект **Table** с этим фильтром и выполняется перечисление и отображение строк в ограниченном объекте **Table**.</span><span class="sxs-lookup"><span data-stu-id="10ab0-153">It then creates a **Table** object with that filter, and enumerates and displays the rows in the restricted **Table** object.</span></span>

<span data-ttu-id="10ab0-154">Если вы используете Visual Studio для тестирования этого примера кода, сначала добавьте ссылку на компонент Microsoft Outlook 15.0 Object Library и задайте переменную Outlook при импорте пространства имен **Microsoft.Office.Interop.Outlook**.</span><span class="sxs-lookup"><span data-stu-id="10ab0-154">If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the Outlook variable when you import the **Microsoft.Office.Interop.Outlook** namespace.</span></span> <span data-ttu-id="10ab0-155">Инструкция **using** не должна находиться непосредственно перед функциями в примере кода, но ее нужно добавить перед объявлением общедоступного класса.</span><span class="sxs-lookup"><span data-stu-id="10ab0-155">The **using** statement must not occur directly before the functions in the code example but must be added before the public Class declaration.</span></span> <span data-ttu-id="10ab0-156">В приведенной ниже строке кода показано, как выполнить импорт и назначение на языке C\#.</span><span class="sxs-lookup"><span data-stu-id="10ab0-156">The following line of code shows how to do the import and assignment in C\#.</span></span>

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```csharp
private void DemoDASLDateMacro()
{
    string filter = "@SQL=" + "%lastmonth(" + "\"" +
        "DAV:getlastmodified" + "\"" + ")%";
    Outlook.Table table = Application.Session.GetDefaultFolder(
        Outlook.OlDefaultFolders.olFolderInbox).GetTable(
        filter, Outlook.OlTableContents.olUserItems);
    while (!table.EndOfTable)
    {
        Outlook.Row row = table.GetNextRow();
        Debug.WriteLine(row["Subject"]);
    }
}
```

## <a name="see-also"></a><span data-ttu-id="10ab0-157">См. также</span><span class="sxs-lookup"><span data-stu-id="10ab0-157">See also</span></span>

- [<span data-ttu-id="10ab0-158">Поиск и фильтрация</span><span class="sxs-lookup"><span data-stu-id="10ab0-158">Search and filter</span></span>](search-and-filter.md)


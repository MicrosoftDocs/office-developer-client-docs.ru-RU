---
title: Фильтрация и отображение многозначных свойств при перечислении элементов в папке
TOCTitle: Filter and display multivalued properties when enumerating items in a folder
ms:assetid: 62dd2120-5c85-44b3-89ec-c4ca85aa2964
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184613(v=office.15)
ms:contentKeyID: 55119887
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: d6242506bac081ee16d125ea92fbed69939c6abc
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/29/2019
ms.locfileid: "34542627"
---
# <a name="filter-and-display-multivalued-properties-when-enumerating-items-in-a-folder"></a><span data-ttu-id="c1c4e-102">Фильтрация и отображение многозначных свойств при перечислении элементов в папке</span><span class="sxs-lookup"><span data-stu-id="c1c4e-102">Filter and display multivalued properties when enumerating items in a folder</span></span>

<span data-ttu-id="c1c4e-103">В этом примере показан порядок фильтрации и отображения многозначных свойств при перечислении элементов в папке.</span><span class="sxs-lookup"><span data-stu-id="c1c4e-103">This example shows how to filter and display multivalued properties while enumerating items in a folder.</span></span>

## <a name="example"></a><span data-ttu-id="c1c4e-104">Пример</span><span class="sxs-lookup"><span data-stu-id="c1c4e-104">Example</span></span>

> [!NOTE] 
> <span data-ttu-id="c1c4e-105">Приведенный ниже пример кода представляет собой фрагмент из книги [Программирование приложений для Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).</span><span class="sxs-lookup"><span data-stu-id="c1c4e-105">The following code example is an excerpt from [Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).</span></span>

<span data-ttu-id="c1c4e-p101">Объект [Table](https://msdn.microsoft.com/library/bb652856\(v=office.15\)) представляет набор данных элемента из объекта [Folder](https://msdn.microsoft.com/library/bb645774\(v=office.15\)) или [Search](https://msdn.microsoft.com/library/bb612611\(v=office.15\)). При первом добавлении двоичного, многозначного свойства или свойства даты к объекту **Table** способ ссылки на свойство влияет на его тип и формат. Поскольку ссылки на встроенные имена иногда могут возвращать значения столбцов, отличные от ссылок на пространство имен, следует определить, задается ли ссылка на свойство с использованием его явного встроенного имени (если таковое есть) или с помощью пространства имен (независимо от наличия явного встроенного имени). В следующей таблице показаны различия в представлении значения свойства (относительно типа и формата) в зависимости от исходного типа свойства.</span><span class="sxs-lookup"><span data-stu-id="c1c4e-p101">The [Table](https://msdn.microsoft.com/library/bb652856\(v=office.15\)) object represents a set of item data from a [Folder](https://msdn.microsoft.com/library/bb645774\(v=office.15\)) or [Search](https://msdn.microsoft.com/library/bb612611\(v=office.15\)) object. When a binary, date, or multivalued property is first added to a **Table** object, the way the property is referenced affects its type and format. Because built-in name references sometimes return a different column value than a namespace reference, you should determine whether the property is referenced by its explicit built-in name (if it has one), or by namespace (regardless of the existence of an explicit built-in name). The following table shows the difference in the property value representation (in terms of type and format) per original property type.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="c1c4e-110">Тип</span><span class="sxs-lookup"><span data-stu-id="c1c4e-110">Type</span></span></p></th>
<th><p><span data-ttu-id="c1c4e-111">Тип возвращаемого значения, если для указанного свойства используется встроенное имя</span><span class="sxs-lookup"><span data-stu-id="c1c4e-111">Return type if the specified property uses a built-in name</span></span></p></th>
<th><p><span data-ttu-id="c1c4e-112">Тип возвращаемого значения, если для указанного свойства используется пространство имен</span><span class="sxs-lookup"><span data-stu-id="c1c4e-112">Return type if the specified property uses a namespace</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c1c4e-113">Двоичный <b>(PT_BINARY)</b></span><span class="sxs-lookup"><span data-stu-id="c1c4e-113">Binary <b>(PT_BINARY)</b></span></span></p></td>
<td><p><span data-ttu-id="c1c4e-114">Строка</span><span class="sxs-lookup"><span data-stu-id="c1c4e-114">String</span></span></p></td>
<td><p><span data-ttu-id="c1c4e-115">Массив байтов</span><span class="sxs-lookup"><span data-stu-id="c1c4e-115">Byte array</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c1c4e-116">Дата <b>(PT_SYSTIME)</b></span><span class="sxs-lookup"><span data-stu-id="c1c4e-116">Date <b>(PT_SYSTIME)</b></span></span></p></td>
<td><p><span data-ttu-id="c1c4e-117">Местные <b>дата и время</b></span><span class="sxs-lookup"><span data-stu-id="c1c4e-117">Local <b>DateTime</b></span></span></p></td>
<td><p><span data-ttu-id="c1c4e-118"><b>Дата и время</b> в формате UTC</span><span class="sxs-lookup"><span data-stu-id="c1c4e-118">UTC <b>DateTime</b></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c1c4e-119">Многозначное (тип ключевого слова), например свойство <b>Categories</b> <b>(PT_MV_STRING8)</b></span><span class="sxs-lookup"><span data-stu-id="c1c4e-119">Multivalued (also known as keyword type) such as <b>Categories</b> property <b>(PT_MV_STRING8)</b></span></span></p></td>
<td><p><span data-ttu-id="c1c4e-120">Строка с разделителями-запятыми</span><span class="sxs-lookup"><span data-stu-id="c1c4e-120">String that contains comma-separated values</span></span></p></td>
<td><p><span data-ttu-id="c1c4e-121">Одномерный массив, содержащий один элемент для каждого ключевого слова</span><span class="sxs-lookup"><span data-stu-id="c1c4e-121">One-dimensional array that contains one element for each keyword</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="c1c4e-122">В следующем примере кода показаны порядок добавления свойства пространства имен строки MAPI в объект **Table**, а также влияние многозначных свойств на значения, возвращаемые в объект [Column](https://msdn.microsoft.com/library/bb609646\(v=office.15\)).</span><span class="sxs-lookup"><span data-stu-id="c1c4e-122">The following code example illustrates how to add a MAPI string namespace property to the **Table** object and how multivalued properties affect the values returned in a [Column](https://msdn.microsoft.com/library/bb609646\(v=office.15\)) object.</span></span> <span data-ttu-id="c1c4e-123">Процедура TableMultiValuedProperties обеспечивает фильтрацию объекта **Table** в поиске строк, в которых свойство [Categories](https://msdn.microsoft.com/library/bb646607\(v=office.15\)) не является пустой ссылкой.</span><span class="sxs-lookup"><span data-stu-id="c1c4e-123">The TableMultiValuedProperties procedure filters the **Table** object for rows where the [Categories](https://msdn.microsoft.com/library/bb646607\(v=office.15\)) property is not a null reference.</span></span> <span data-ttu-id="c1c4e-124">Свойство **Categories** представлено свойством, использующим пространство имен строки MAPI.</span><span class="sxs-lookup"><span data-stu-id="c1c4e-124">The **Categories** property is represented by a property that uses the MAPI string namespace.</span></span> <span data-ttu-id="c1c4e-125">Фильтр поиска и обнаружения DAV (DASL) создан для элементов, имеющих категории (фактический фильтр возвращает категории, для которых отсутствуют пустые ссылки).</span><span class="sxs-lookup"><span data-stu-id="c1c4e-125">A DAV Searching and Locating (DASL) filter is constructed for items that have categories (the actual filter returns categories that do not have a null reference).</span></span> <span data-ttu-id="c1c4e-126">После этого столбец **Categories** добавляется в объект **Table** посредством объединения спецификатора типа 0000001f с константой categoriesProperty.</span><span class="sxs-lookup"><span data-stu-id="c1c4e-126">A **Categories** column is then added to the **Table** object by concatenating the type specifier, 0000001f, with the categoriesProperty constant.</span></span> <span data-ttu-id="c1c4e-127">Наконец, объект **Column**, представляющий свойство **Categories**, содержит одномерный массив строк, в котором каждый элемент массива представляет категорию, назначенную элементу.</span><span class="sxs-lookup"><span data-stu-id="c1c4e-127">Finally, the **Column** object that represents the **Categories** property contains a one-dimensional string array where each element of the array represents a category assigned to the item.</span></span> <span data-ttu-id="c1c4e-128">Свойства **Categories** и **Subject** записываются в прослушиватели трассировки коллекции [Listeners](https://msdn.microsoft.com/library/system.diagnostics.debug.listeners.aspx).</span><span class="sxs-lookup"><span data-stu-id="c1c4e-128">Both the item’s **Categories** and **Subject** properties are written to the trace listeners of the [Listeners](https://msdn.microsoft.com/library/system.diagnostics.debug.listeners.aspx) collection.</span></span>

<span data-ttu-id="c1c4e-129">Если вы используете Visual Studio для тестирования этого примера кода, сначала добавьте ссылку на компонент Microsoft Outlook 15.0 Object Library и задайте переменную Outlook при импорте пространства имен **Microsoft.Office.Interop.Outlook**.</span><span class="sxs-lookup"><span data-stu-id="c1c4e-129">If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the Outlook variable when you import the **Microsoft.Office.Interop.Outlook** namespace.</span></span> <span data-ttu-id="c1c4e-130">Инструкция **using** не должна находиться непосредственно перед функциями в примере кода, но ее нужно добавить перед объявлением общедоступного класса.</span><span class="sxs-lookup"><span data-stu-id="c1c4e-130">The **using** statement must not occur directly before the functions in the code example but must be added before the public Class declaration.</span></span> <span data-ttu-id="c1c4e-131">В приведенной ниже строке кода показано, как выполнить импорт и назначение на языке C\#.</span><span class="sxs-lookup"><span data-stu-id="c1c4e-131">The following line of code shows how to do the import and assignment in C\#.</span></span>

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```csharp
private void TableMultiValuedProperties()
{
    const string categoriesProperty =
        "http://schemas.microsoft.com/mapi/string/"
        + "{00020329-0000-0000-C000-000000000046}/Keywords";
    // Inbox
    Outlook.Folder folder =
        Application.Session.GetDefaultFolder(
        Outlook.OlDefaultFolders.olFolderInbox)
        as Outlook.Folder;
    // Call GetTable with filter for categories
    string filter = "@SQL="
        + "Not(" + "\"" + categoriesProperty
        + "\"" + " Is Null)";
    Outlook.Table table =
        folder.GetTable(filter,
        Outlook.OlTableContents.olUserItems);
    // Add categories column and append type specifier
    table.Columns.Add(categoriesProperty + "/0000001F");
    while (!table.EndOfTable)
    {
        Outlook.Row nextRow = table.GetNextRow();
        string[] categories =
            (string[])nextRow[categoriesProperty + "/0000001F"];
        Debug.WriteLine("Subject: " + nextRow["Subject"]);
        Debug.Write("Categories: ");
        foreach (string category in categories)
        {
            Debug.Write("\t" + category);
        }
        Debug.WriteLine("\n");
    }
}
```

## <a name="see-also"></a><span data-ttu-id="c1c4e-132">См. также</span><span class="sxs-lookup"><span data-stu-id="c1c4e-132">See also</span></span>

- [<span data-ttu-id="c1c4e-133">Поиск и фильтрация</span><span class="sxs-lookup"><span data-stu-id="c1c4e-133">Search and filter</span></span>](search-and-filter.md)


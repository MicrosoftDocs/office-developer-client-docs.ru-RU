---
title: Фильтрация и отображение многозначных свойств при перечислении элементов в папке
TOCTitle: Filter and display multivalued properties when enumerating items in a folder
ms:assetid: 62dd2120-5c85-44b3-89ec-c4ca85aa2964
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184613(v=office.15)
ms:contentKeyID: 55119887
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: acb6f6807f956ee6d468d3fcefc2cdd27732ab9b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32320323"
---
# <a name="filter-and-display-multivalued-properties-when-enumerating-items-in-a-folder"></a>Фильтрация и отображение многозначных свойств при перечислении элементов в папке

В этом примере показан порядок фильтрации и отображения многозначных свойств при перечислении элементов в папке.

## <a name="example"></a>Пример

> [!NOTE] 
> Приведенный ниже пример кода представляет собой фрагмент из книги [Программирование приложений для Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).

Объект [Table](https://msdn.microsoft.com/library/bb652856\(v=office.15\)) представляет набор данных элемента из объекта [Folder](https://msdn.microsoft.com/library/bb645774\(v=office.15\)) или [Search](https://msdn.microsoft.com/library/bb612611\(v=office.15\)). При первом добавлении двоичного, многозначного свойства или свойства даты к объекту **Table** способ ссылки на свойство влияет на его тип и формат. Поскольку ссылки на встроенные имена иногда могут возвращать значения столбцов, отличные от ссылок на пространство имен, следует определить, задается ли ссылка на свойство с использованием его явного встроенного имени (если таковое есть) или с помощью пространства имен (независимо от наличия явного встроенного имени). В следующей таблице показаны различия в представлении значения свойства (относительно типа и формата) в зависимости от исходного типа свойства.

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Тип</p></th>
<th><p>Тип возвращаемого значения, если для указанного свойства используется встроенное имя</p></th>
<th><p>Тип возвращаемого значения, если для указанного свойства используется пространство имен</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>Двоичный <b>(PT_BINARY)</b></p></td>
<td><p>Строка</p></td>
<td><p>Массив байтов</p></td>
</tr>
<tr class="even">
<td><p>Дата <b>(PT_SYSTIME)</b></p></td>
<td><p>Местные <b>дата и время</b></p></td>
<td><p><b>Дата и время</b> в формате UTC</p></td>
</tr>
<tr class="odd">
<td><p>Многозначное (тип ключевого слова), например свойство <b>Categories</b> <b>(PT_MV_STRING8)</b></p></td>
<td><p>Строка с разделителями-запятыми</p></td>
<td><p>Одномерный массив, содержащий один элемент для каждого ключевого слова</p></td>
</tr>
</tbody>
</table>


В следующем примере кода показаны порядок добавления свойства пространства имен строки MAPI в объект **Table**, а также влияние многозначных свойств на значения, возвращаемые в объект [Column](https://msdn.microsoft.com/library/bb609646\(v=office.15\)). Процедура TableMultiValuedProperties обеспечивает фильтрацию объекта **Table** в поиске строк, в которых свойство [Categories](https://msdn.microsoft.com/library/bb646607\(v=office.15\)) не является пустой ссылкой. Свойство **Categories** представлено свойством, использующим пространство имен строки MAPI. Фильтр поиска и обнаружения DAV (DASL) создан для элементов, имеющих категории (фактический фильтр возвращает категории, для которых отсутствуют пустые ссылки). После этого столбец **Categories** добавляется в объект **Table** посредством объединения спецификатора типа 0000001f с константой categoriesProperty. Наконец, объект **Column**, представляющий свойство **Categories**, содержит одномерный массив строк, в котором каждый элемент массива представляет категорию, назначенную элементу. Свойства **Categories** и **Subject** записываются в прослушиватели трассировки коллекции [Listeners](https://msdn.microsoft.com/library/system.diagnostics.debug.listeners.aspx).

Если вы используете Visual Studio для тестирования этого примера кода, сначала добавьте ссылку на компонент Microsoft Outlook 15.0 Object Library и задайте переменную Outlook при импорте пространства имен **Microsoft.Office.Interop.Outlook**. Инструкция **using** не должна находиться непосредственно перед функциями в примере кода, но ее нужно добавить перед объявлением общедоступного класса. В приведенной ниже строке кода показано, как выполнить импорт и назначение на языке C\#.

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```csharp
private void TableMultiValuedProperties()
{
    const string categoriesProperty =
        "https://schemas.microsoft.com/mapi/string/"
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

## <a name="see-also"></a>См. также

- [Поиск и фильтрация](search-and-filter.md)


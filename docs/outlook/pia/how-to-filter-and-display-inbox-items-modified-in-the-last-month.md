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
# <a name="filter-and-display-inbox-items-modified-in-the-last-month"></a>Фильтрация и отображение элементов папки "Входящие", измененных в прошлом месяце

В этом примере показано, как фильтровать и отображать элементы папки "Входящие", которые были изменены в прошлом месяце.

## <a name="example"></a>Пример

> [!NOTE] 
> Приведенный ниже пример кода представляет собой фрагмент из книги [Программирование приложений для Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).

Язык запросов DASL основан на реализации DASL Microsoft Exchange в Outlook. Его можно использовать для возвращения результатов на основе свойств для поисков на уровне элементов в данных папки, например представленных объектом [Table](https://msdn.microsoft.com/library/bb652856\(v=office.15\)). Фильтры DASL поддерживают сравнение строк, в том числе сопоставление эквивалентности, префиксов, фраз и подстрок, с помощью оператора равенства (=). С помощью запросов DASL можно выполнять сравнение и фильтрацию по дате и времени.

Поскольку в запросах DASL сравнение по значению **DateTime** всегда выполняется по стандартному времени по Гринвичу (UTC), для правильного выполнения запроса необходимо преобразовать время местного часового пояса во время по стандарту UTC. Также необходимо преобразовать значение **DateTime** в строковое представление, поскольку фильтры DASL поддерживают сравнение строк. Преобразование значения **DateTime** можно выполнить двумя способами: с помощью метода [LocalTimeToUTC(Object)](https://msdn.microsoft.com/library/bb645832\(v=office.15\)) объекта [Row](https://msdn.microsoft.com/library/bb610126\(v=office.15\)) или с помощью соответствующего макроса Outlook **DateTime**.

В следующей строке кода показано использование метода **LocalTimeToUTC** для преобразования значения свойства **LastModificationTime** (столбец по умолчанию во всех объектах **Item**) в формат UTC.

```csharp
DateTime modified = nextRow.LocalTimeUTC(“LastModificationTime”);
```

В следующей таблице перечислены макросы **DateTime**, обеспечивающие возврат отфильтрованных строк, для которых выполнено сравнение заданного свойства **DateTime** с указанными относительной датой или диапазоном дат в формате UTC. Свойство SchemaName представляет любое допустимое свойство типа **DateTime**, ссылка на которое указывается в пространстве имен.

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Макрос</p></th>
<th><p>Синтаксис</p></th>
<th><p>Описание</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>today</p></td>
<td><p>%today(“SchemaName”)%</p></td>
<td><p>Ограничение элементами со значением свойства SchemaName, соответствующим сегодняшней дате.</p></td>
</tr>
<tr class="even">
<td><p>tomorrow</p></td>
<td><p>%tomorrow(“SchemaName”)%</p></td>
<td><p>Ограничение элементами со значением свойства SchemaName, соответствующим завтрашней дате.</p></td>
</tr>
<tr class="odd">
<td><p>yesterday</p></td>
<td><p>%yesterday(“SchemaName”)%</p></td>
<td><p>Ограничение элементами со значением свойства SchemaName, соответствующим вчерашней дате.</p></td>
</tr>
<tr class="even">
<td><p>next7days</p></td>
<td><p>%next7days(“SchemaName”)%</p></td>
<td><p>Ограничение элементами, для которых значения свойства SchemaName лежат в диапазоне следующих семи дней.</p></td>
</tr>
<tr class="odd">
<td><p>last7days</p></td>
<td><p>%last7days(“SchemaName”)%</p></td>
<td><p>Ограничение элементами, для которых значения свойства SchemaName лежат в диапазоне прошедших семи дней.</p></td>
</tr>
<tr class="even">
<td><p>nextweek</p></td>
<td><p>%nextweek(“SchemaName”)%</p></td>
<td><p>Ограничение элементами, для которых значения свойства SchemaName лежат в диапазоне следующей недели.</p></td>
</tr>
<tr class="odd">
<td><p>thisweek</p></td>
<td><p>%thisweek(“SchemaName”)%</p></td>
<td><p>Ограничение элементами, для которых значения свойства SchemaName лежат в диапазоне текущей недели.</p></td>
</tr>
<tr class="even">
<td><p>lastweek</p></td>
<td><p>%lastweek(“SchemaName”)%</p></td>
<td><p>Ограничение элементами, для которых значения свойства SchemaName лежат в диапазоне прошлой недели.</p></td>
</tr>
<tr class="odd">
<td><p>nextmonth</p></td>
<td><p>%nextmonth(“SchemaName”)%</p></td>
<td><p>Ограничение элементами, для которых значения свойства SchemaName лежат в диапазоне следующего месяца.</p></td>
</tr>
<tr class="even">
<td><p>thismonth</p></td>
<td><p>%thismonth(“SchemaName”)%</p></td>
<td><p>Ограничение элементами, для которых значения свойства SchemaName лежат в диапазоне текущего месяца.</p></td>
</tr>
<tr class="odd">
<td><p>lastmonth</p></td>
<td><p>%lastmonth(“SchemaName”)%</p></td>
<td><p>Ограничение элементами, для которых значения свойства SchemaName лежат в диапазоне прошлого месяца.</p></td>
</tr>
</tbody>
</table>


В следующем примере в процедуре DemoDASLDateMacro создается запрос DASL, в котором используется макрос **lastmonthDateTime** для фильтрации элементов в папке "Входящие" пользователя, измененных в прошлом месяце. Затем создается объект **Table** с этим фильтром и выполняется перечисление и отображение строк в ограниченном объекте **Table**.

Если вы используете Visual Studio для тестирования этого примера кода, сначала добавьте ссылку на компонент Microsoft Outlook 15.0 Object Library и задайте переменную Outlook при импорте пространства имен **Microsoft.Office.Interop.Outlook**. Инструкция **using** не должна находиться непосредственно перед функциями в примере кода, но ее нужно добавить перед объявлением общедоступного класса. В приведенной ниже строке кода показано, как выполнить импорт и назначение на языке C\#.

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

## <a name="see-also"></a>См. также

- [Поиск и фильтрация](search-and-filter.md)


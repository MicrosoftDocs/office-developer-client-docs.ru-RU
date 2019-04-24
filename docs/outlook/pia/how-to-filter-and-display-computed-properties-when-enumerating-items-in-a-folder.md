---
title: Фильтрация и отображение вычисляемых свойств при перечислении элементов в папке
TOCTitle: Filter and display computed properties when enumerating items in a folder
ms:assetid: b068e625-ff12-444d-a30d-51a3acba3043
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184632(v=office.15)
ms:contentKeyID: 55119922
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 946858221b649cd6189ddf44680b316554cab5de
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32320337"
---
# <a name="filter-and-display-computed-properties-when-enumerating-items-in-a-folder"></a>Фильтрация и отображение вычисляемых свойств при перечислении элементов в папке

В этом примере показан порядок фильтрации и отображения вычисляемых свойств при перечислении элементов в папке.

## <a name="example"></a>Пример

> [!NOTE] 
> Приведенный ниже пример кода взят из книги [Программирование приложений для Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).


Объект [Table](https://msdn.microsoft.com/library/bb652856\(v=office.15\)) представляет набор данных элемента из объекта [Folder](https://msdn.microsoft.com/library/bb645774\(v=office.15\)) или [Search](https://msdn.microsoft.com/library/bb612611\(v=office.15\)) . Объект [Row](https://msdn.microsoft.com/library/bb610126\(v=office.15\)) представляет строку данных в объекте **Table**. Объект [Columns](https://msdn.microsoft.com/library/bb646214\(v=office.15\)) представляет свойства объекта **Table**. Для добавления свойств в объект **Table** можно использовать метод [Add(String)](https://msdn.microsoft.com/library/bb652865\(v=office.15\)) объекта **Columns**. Для фильтрации определенных свойств можно использовать метод [Restrict(String)](https://msdn.microsoft.com/library/bb612178\(v=office.15\)) объекта **Table**. Однако для некоторых свойств не поддерживается ни добавление в объект **Table** с помощью метода **Columns.Add**, ни фильтрация с использованием метода **Restrict**. В следующей таблице приведены сведения о поддержке свойств для объекта **Table** при использовании метода **Columns.Add** или **Restrict**.

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Свойство</p></th>
<th><p>Для метода Columns.Add</p></th>
<th><p>Для метода Restrict</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>Двоичные свойства, например <b>EntryID</b>.</p></td>
<td><p>Поддерживаются через встроенное свойство или свойство пространства имен.</p></td>
<td><p>Не поддерживаются. Outlook сообщает об ошибке.</p></td>
</tr>
<tr class="even">
<td><p>Свойства основного текста, включая <b>Body</b> и <b>HTMLBody</b>, а также представление этих свойств в пространстве имен, включая <b>PR_RTF_COMPRESSED</b>.</p></td>
<td><p>Свойство <b>Body</b> поддерживается при условии, что только первые 255 байт значения хранятся в объекте <b>Table</b>. Другие свойства, которые представляют основное содержимое в формате HTML или RTF не поддерживаются. Так как возвращаются только первые 255 байт свойства <b>Body</b>, поэтому если нужно получить все основное содержимое элемента в формате текста или HTML, используйте свойство элемента <b>EntryID</b> в методе <a href="https://msdn.microsoft.com/library/bb644121(v=office.15)">GetItemFromID(String, Object)</a>, чтобы получить объект элемента. Затем извлеките полное значение <b>Body</b> из объекта элемента.</p></td>
<td><p>В фильтре поддерживается только свойство <b>Body</b>, представленное в тексте. Это означает, что в фильтре поиска и обнаружения DAV (DASL) должна присутствовать ссылка на свойство в формате <em>urn:schemas:http-mail:textdescription</em>, а фильтрация по тегам HTML в тексте сообщения не поддерживается. Чтобы повысить быстродействие, следует использовать в фильтре ключевые слова индексатора контента для сопоставления строк в тексте сообщения.</p></td>
</tr>
<tr class="odd">
<td><p>Свойства вычисления, например <b>AutoResolvedWinner</b> и <b>BodyFormat</b>.</p></td>
<td><p>Не поддерживается.</p></td>
<td><p>Не поддерживается.</p></td>
</tr>
<tr class="even">
<td><p>Многозначные свойства, например <b>Categories</b>, <b>Children</b>, <b>Companies</b> и <b>VotingOptions</b>.</p></td>
<td><p>Поддерживаются.</p></td>
<td><p>Поддерживаются при условии, что можно создать запрос DASL с помощью представления в пространстве имен.</p></td>
</tr>
<tr class="odd">
<td><p>Свойства, возвращающие объект, например <b>Attachments</b>, <b>Parent</b>, <b>Recipients</b>, <b>RecurrencePattern</b> и <b> UserProperties</b>.</p></td>
<td><p>Не поддерживается.</p></td>
<td><p>Не поддерживается.</p></td>
</tr>
</tbody>
</table>


В следующей таблице перечислены известные недопустимые свойства, которые нельзя добавить в объект **Table** с помощью метода **Columns.Add**. При попытке добавить свойство из этого списка возникает ошибка приложения Outlook.

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>AutoResolvedWinner</p></td>
<td><p>BodyFormat</p></td>
<td><p>Класс</p></td>
</tr>
<tr class="even">
<td><p>Компании</p></td>
<td><p>ContactNames</p></td>
<td><p>DLName</p></td>
</tr>
<tr class="odd">
<td><p>DownloadState</p></td>
<td><p>FlagIcon</p></td>
<td><p>HtmlBody</p></td>
</tr>
<tr class="even">
<td><p>InternetCodePage</p></td>
<td><p>IsConflict</p></td>
<td><p>IsMarkedAsTask</p></td>
</tr>
<tr class="odd">
<td><p>MeetingWorkspaceURL</p></td>
<td><p>MemberCount</p></td>
<td><p>Разрешение</p></td>
</tr>
<tr class="even">
<td><p>PermissionService</p></td>
<td><p>RecurrenceState</p></td>
<td><p>ResponseState</p></td>
</tr>
<tr class="odd">
<td><p>Saved</p></td>
<td><p>Sent</p></td>
<td><p>Submitted</p></td>
</tr>
<tr class="even">
<td><p>TaskSubject</p></td>
<td><p>Unread</p></td>
<td><p>VotingOptions</p></td>
</tr>
</tbody>
</table>


Некоторые вычисляемые свойства невозможно добавить в набор столбцов таблицы, но в следующем примере кода выполняется обход этого ограничения. В процедуре GetToDoItems используется запрос DASL для ограничения элементов, отображающихся в объекте **Table**. Если вычисляемое свойство имеет представление в пространстве имен, это представление используется для создания запроса DASL, который ограничивает объект **Table** и возвращает строки для заданного значения вычисляемого свойства. Процедура GetToDoItems получает элементы из папки "Входящие", для которых значение свойства [IsMarkedAsTask](https://msdn.microsoft.com/library/bb623631\(v=office.15\)) равно **true**, а затем присваивает эти значения определенным свойствам задачи, таким как [TaskSubject](https://msdn.microsoft.com/library/bb643880\(v=office.15\)), [TaskDueDate](https://msdn.microsoft.com/library/bb623035\(v=office.15\)), [TaskStartDate](https://msdn.microsoft.com/library/bb610832\(v=office.15\)) и [TaskCompletedDate](https://msdn.microsoft.com/library/bb624055\(v=office.15\)). В завершение эти свойства записываются в прослушиватели трассировки коллекции [Listeners](https://msdn.microsoft.com/library/system.diagnostics.debug.listeners.aspx).

Если для тестирования этого примера кода вы используете Visual Studio, сначала добавьте ссылку на компонент библиотеки объектов Microsoft Outlook 15.0 и укажите переменную Outlook при импорте пространства имен **Microsoft.Office.Interop.Outlook**. Инструкция **using** не должна находиться непосредственно перед функциями в примере кода, но ее нужно добавить перед объявлением общедоступного класса. В приведенной ниже строке кода показано, как выполнить импорт и назначение на языке C\#.

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```csharp
private void GetToDoItems()
{
    // Obtain Inbox
    Outlook.Folder folder =
        Application.Session.GetDefaultFolder(
        Outlook.OlDefaultFolders.olFolderInbox)
        as Outlook.Folder;
    // DASL filter for IsMarkedAsTask
    string filter = "@SQL=" + "\"" +
        "https://schemas.microsoft.com/mapi/proptag/0x0E2B0003"
        + "\"" + " = 1";
    Outlook.Table table =
        folder.GetTable(filter,
        Outlook.OlTableContents.olUserItems);
    table.Columns.Add("TaskStartDate");
    table.Columns.Add("TaskDueDate");
    table.Columns.Add("TaskCompletedDate");
    // Use GUID/ID to represent TaskSubject
    table.Columns.Add(
        "https://schemas.microsoft.com/mapi/id/" +
        "{00062008-0000-0000-C000-000000000046}/85A4001E");
    while (!table.EndOfTable)
    {
        Outlook.Row nextRow = table.GetNextRow();
        StringBuilder sb = new StringBuilder();
        sb.AppendLine("Task Subject: " + nextRow[9]);
        sb.AppendLine("Start Date: "
            + nextRow["TaskStartDate"]);
        sb.AppendLine("Due Date: "
            + nextRow["TaskDueDate"]);
        sb.AppendLine("Completed Date: "
            + nextRow["TaskCompletedDate"]);
        sb.AppendLine();
        Debug.WriteLine(sb.ToString());
    }
}
```

## <a name="see-also"></a>См. также

- [Поиск и фильтрация](search-and-filter.md)


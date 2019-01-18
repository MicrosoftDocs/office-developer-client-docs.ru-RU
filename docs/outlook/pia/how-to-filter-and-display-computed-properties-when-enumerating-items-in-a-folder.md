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
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28723077"
---
# <a name="filter-and-display-computed-properties-when-enumerating-items-in-a-folder"></a><span data-ttu-id="1fdcd-102">Фильтрация и отображение вычисляемых свойств при перечислении элементов в папке</span><span class="sxs-lookup"><span data-stu-id="1fdcd-102">Filter and display computed properties when enumerating items in a folder</span></span>

<span data-ttu-id="1fdcd-103">В этом примере показан порядок фильтрации и отображения вычисляемых свойств при перечислении элементов в папке.</span><span class="sxs-lookup"><span data-stu-id="1fdcd-103">This example shows how to filter and display computed properties when enumerating items in a folder.</span></span>

## <a name="example"></a><span data-ttu-id="1fdcd-104">Пример</span><span class="sxs-lookup"><span data-stu-id="1fdcd-104">Example</span></span>

> [!NOTE] 
> <span data-ttu-id="1fdcd-105">Приведенный ниже пример кода взят из книги [Программирование приложений для Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).</span><span class="sxs-lookup"><span data-stu-id="1fdcd-105">The following code example is an excerpt from [Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).</span></span>


<span data-ttu-id="1fdcd-p101">Объект [Table](https://msdn.microsoft.com/library/bb652856\(v=office.15\)) представляет набор данных элемента из объекта [Folder](https://msdn.microsoft.com/library/bb645774\(v=office.15\)) или [Search](https://msdn.microsoft.com/library/bb612611\(v=office.15\)) . Объект [Row](https://msdn.microsoft.com/library/bb610126\(v=office.15\)) представляет строку данных в объекте **Table**. Объект [Columns](https://msdn.microsoft.com/library/bb646214\(v=office.15\)) представляет свойства объекта **Table**. Для добавления свойств в объект **Table** можно использовать метод [Add(String)](https://msdn.microsoft.com/library/bb652865\(v=office.15\)) объекта **Columns**. Для фильтрации определенных свойств можно использовать метод [Restrict(String)](https://msdn.microsoft.com/library/bb612178\(v=office.15\)) объекта **Table**. Однако для некоторых свойств не поддерживается ни добавление в объект **Table** с помощью метода **Columns.Add**, ни фильтрация с использованием метода **Restrict**. В следующей таблице приведены сведения о поддержке свойств для объекта **Table** при использовании метода **Columns.Add** или **Restrict**.</span><span class="sxs-lookup"><span data-stu-id="1fdcd-p101">The [Table](https://msdn.microsoft.com/library/bb652856\(v=office.15\)) object represents a set of item data from a [Folder](https://msdn.microsoft.com/library/bb645774\(v=office.15\)) or [Search](https://msdn.microsoft.com/library/bb612611\(v=office.15\)) object. The [Row](https://msdn.microsoft.com/library/bb610126\(v=office.15\)) object represents rows of data in a **Table**. The [Columns](https://msdn.microsoft.com/library/bb646214\(v=office.15\)) object represents properties of the **Table**. You can add certain properties to the **Table** object by using the [Add(String)](https://msdn.microsoft.com/library/bb652865\(v=office.15\)) method of the **Columns** object. You can filter certain properties by using the [Restrict(String)](https://msdn.microsoft.com/library/bb612178\(v=office.15\)) method of the **Table** object. However, some properties cannot be added to the **Table** object by using **Columns.Add**, nor can they be filtered by using the **Restrict** method. The following table describes whether properties are supported for the **Table** object when you use the **Columns.Add** or **Restrict** method.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="1fdcd-113">Свойство</span><span class="sxs-lookup"><span data-stu-id="1fdcd-113">Property</span></span></p></th>
<th><p><span data-ttu-id="1fdcd-114">Для метода Columns.Add</span><span class="sxs-lookup"><span data-stu-id="1fdcd-114">For Columns.Add</span></span></p></th>
<th><p><span data-ttu-id="1fdcd-115">Для метода Restrict</span><span class="sxs-lookup"><span data-stu-id="1fdcd-115">For Restrict</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="1fdcd-116">Двоичные свойства, например <b>EntryID</b>.</span><span class="sxs-lookup"><span data-stu-id="1fdcd-116">Binary properties such as <b>EntryID</b>.</span></span></p></td>
<td><p><span data-ttu-id="1fdcd-117">Поддерживаются через встроенное свойство или свойство пространства имен.</span><span class="sxs-lookup"><span data-stu-id="1fdcd-117">Supported via built-in or namespace property.</span></span></p></td>
<td><p><span data-ttu-id="1fdcd-p102">Не поддерживаются. Outlook сообщает об ошибке.</span><span class="sxs-lookup"><span data-stu-id="1fdcd-p102">Not supported. Outlook will raise an error.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1fdcd-120">Свойства основного текста, включая <b>Body</b> и <b>HTMLBody</b>, а также представление этих свойств в пространстве имен, включая <b>PR_RTF_COMPRESSED</b>.</span><span class="sxs-lookup"><span data-stu-id="1fdcd-120">Body properties, including <b>Body</b> and <b>HTMLBody</b>, and namespace representation of those properties, including <b>PR_RTF_COMPRESSED</b>.</span></span></p></td>
<td><p><span data-ttu-id="1fdcd-121">Свойство <b>Body</b> поддерживается при условии, что только первые 255 байт значения хранятся в объекте <b>Table</b>.</span><span class="sxs-lookup"><span data-stu-id="1fdcd-121">The <b>Body</b> property is supported with a condition that only the first 255 bytes of the value are stored in a <b>Table</b> object.</span></span> <span data-ttu-id="1fdcd-122">Другие свойства, которые представляют основное содержимое в формате HTML или RTF не поддерживаются.</span><span class="sxs-lookup"><span data-stu-id="1fdcd-122">Other properties that represent the body content in HTML or RTF are not supported.</span></span> <span data-ttu-id="1fdcd-123">Так как возвращаются только первые 255 байт свойства <b>Body</b>, поэтому если нужно получить все основное содержимое элемента в формате текста или HTML, используйте свойство элемента <b>EntryID</b> в методе <a href="https://msdn.microsoft.com/library/bb644121(v=office.15)">GetItemFromID(String, Object)</a>, чтобы получить объект элемента.</span><span class="sxs-lookup"><span data-stu-id="1fdcd-123">Because only the first 255 bytes of <b>Body</b> are returned, if you want to obtain the full body content of an item in text or HTML, use the item’s <b>EntryID</b> in the <a href="https://msdn.microsoft.com/library/bb644121(v=office.15)">GetItemFromID(String, Object)</a> method to obtain the item object.</span></span> <span data-ttu-id="1fdcd-124">Затем извлеките полное значение <b>Body</b> из объекта элемента.</span><span class="sxs-lookup"><span data-stu-id="1fdcd-124">Then retrieve the full value of <b>Body</b> through the item object.</span></span></p></td>
<td><p><span data-ttu-id="1fdcd-p104">В фильтре поддерживается только свойство <b>Body</b>, представленное в тексте. Это означает, что в фильтре поиска и обнаружения DAV (DASL) должна присутствовать ссылка на свойство в формате <em>urn:schemas:http-mail:textdescription</em>, а фильтрация по тегам HTML в тексте сообщения не поддерживается. Чтобы повысить быстродействие, следует использовать в фильтре ключевые слова индексатора контента для сопоставления строк в тексте сообщения.</span><span class="sxs-lookup"><span data-stu-id="1fdcd-p104">Only the <b>Body</b> property represented in text is supported in a filter. This means that the property must be referenced in a DAV Searching and Locating (DASL) filter as <em>urn:schemas:http-mail:textdescription</em>, and you cannot filter on any HTML tags in the body. To improve performance, use context indexer keywords in the filter to match strings in the body.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1fdcd-128">Свойства вычисления, например <b>AutoResolvedWinner</b> и <b>BodyFormat</b>.</span><span class="sxs-lookup"><span data-stu-id="1fdcd-128">Computer properties, such as <b>AutoResolvedWinner</b> and <b>BodyFormat</b>.</span></span></p></td>
<td><p><span data-ttu-id="1fdcd-129">Не поддерживаются.</span><span class="sxs-lookup"><span data-stu-id="1fdcd-129">Not supported.</span></span></p></td>
<td><p><span data-ttu-id="1fdcd-130">Не поддерживаются.</span><span class="sxs-lookup"><span data-stu-id="1fdcd-130">Not supported.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1fdcd-131">Многозначные свойства, например <b>Categories</b>, <b>Children</b>, <b>Companies</b> и <b>VotingOptions</b>.</span><span class="sxs-lookup"><span data-stu-id="1fdcd-131">Multivalued properties, such as <b>Categories</b>, <b>Children</b>, <b>Companies</b>, and <b>VotingOptions</b>.</span></span></p></td>
<td><p><span data-ttu-id="1fdcd-132">Поддерживаются.</span><span class="sxs-lookup"><span data-stu-id="1fdcd-132">Supported.</span></span></p></td>
<td><p><span data-ttu-id="1fdcd-133">Поддерживаются при условии, что можно создать запрос DASL с помощью представления в пространстве имен.</span><span class="sxs-lookup"><span data-stu-id="1fdcd-133">Supported, provided that you can create a DASL query by using the namespace representation.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1fdcd-134">Свойства, возвращающие объект, например <b>Attachments</b>, <b>Parent</b>, <b>Recipients</b>, <b>RecurrencePattern</b> и <b> UserProperties</b>.</span><span class="sxs-lookup"><span data-stu-id="1fdcd-134">Properties that return an object, such as <b>Attachments</b>, <b>Parent</b>, <b>Recipients</b>, <b>RecurrencePattern</b>, and <b>UserProperties</b>.</span></span></p></td>
<td><p><span data-ttu-id="1fdcd-135">Не поддерживаются.</span><span class="sxs-lookup"><span data-stu-id="1fdcd-135">Not supported.</span></span></p></td>
<td><p><span data-ttu-id="1fdcd-136">Не поддерживаются.</span><span class="sxs-lookup"><span data-stu-id="1fdcd-136">Not supported.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="1fdcd-p105">В следующей таблице перечислены известные недопустимые свойства, которые нельзя добавить в объект **Table** с помощью метода **Columns.Add**. При попытке добавить свойство из этого списка возникает ошибка приложения Outlook.</span><span class="sxs-lookup"><span data-stu-id="1fdcd-p105">The following table lists known invalid properties that cannot be added to the **Table** object by using **Columns.Add**. If you attempt to add a property from this list, Outlook will raise an error.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="1fdcd-139">AutoResolvedWinner</span><span class="sxs-lookup"><span data-stu-id="1fdcd-139">AutoResolvedWinner</span></span></p></td>
<td><p><span data-ttu-id="1fdcd-140">BodyFormat</span><span class="sxs-lookup"><span data-stu-id="1fdcd-140">BodyFormat</span></span></p></td>
<td><p><span data-ttu-id="1fdcd-141">Class</span><span class="sxs-lookup"><span data-stu-id="1fdcd-141">Class</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1fdcd-142">Companies</span><span class="sxs-lookup"><span data-stu-id="1fdcd-142">Companies</span></span></p></td>
<td><p><span data-ttu-id="1fdcd-143">ContactNames</span><span class="sxs-lookup"><span data-stu-id="1fdcd-143">ContactNames</span></span></p></td>
<td><p><span data-ttu-id="1fdcd-144">DLName</span><span class="sxs-lookup"><span data-stu-id="1fdcd-144">DLName</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1fdcd-145">DownloadState</span><span class="sxs-lookup"><span data-stu-id="1fdcd-145">DownloadState</span></span></p></td>
<td><p><span data-ttu-id="1fdcd-146">FlagIcon</span><span class="sxs-lookup"><span data-stu-id="1fdcd-146">FlagIcon</span></span></p></td>
<td><p><span data-ttu-id="1fdcd-147">HtmlBody</span><span class="sxs-lookup"><span data-stu-id="1fdcd-147">HtmlBody</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1fdcd-148">InternetCodePage</span><span class="sxs-lookup"><span data-stu-id="1fdcd-148">InternetCodePage</span></span></p></td>
<td><p><span data-ttu-id="1fdcd-149">IsConflict</span><span class="sxs-lookup"><span data-stu-id="1fdcd-149">IsConflict</span></span></p></td>
<td><p><span data-ttu-id="1fdcd-150">IsMarkedAsTask</span><span class="sxs-lookup"><span data-stu-id="1fdcd-150">IsMarkedAsTask</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1fdcd-151">MeetingWorkspaceURL</span><span class="sxs-lookup"><span data-stu-id="1fdcd-151">MeetingWorkspaceURL</span></span></p></td>
<td><p><span data-ttu-id="1fdcd-152">MemberCount</span><span class="sxs-lookup"><span data-stu-id="1fdcd-152">MemberCount</span></span></p></td>
<td><p><span data-ttu-id="1fdcd-153">Permission</span><span class="sxs-lookup"><span data-stu-id="1fdcd-153">Permission</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1fdcd-154">PermissionService</span><span class="sxs-lookup"><span data-stu-id="1fdcd-154">PermissionService</span></span></p></td>
<td><p><span data-ttu-id="1fdcd-155">RecurrenceState</span><span class="sxs-lookup"><span data-stu-id="1fdcd-155">RecurrenceState</span></span></p></td>
<td><p><span data-ttu-id="1fdcd-156">ResponseState</span><span class="sxs-lookup"><span data-stu-id="1fdcd-156">ResponseState</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1fdcd-157">Saved</span><span class="sxs-lookup"><span data-stu-id="1fdcd-157">Saved</span></span></p></td>
<td><p><span data-ttu-id="1fdcd-158">Sent</span><span class="sxs-lookup"><span data-stu-id="1fdcd-158">Sent</span></span></p></td>
<td><p><span data-ttu-id="1fdcd-159">Submitted</span><span class="sxs-lookup"><span data-stu-id="1fdcd-159">Submitted</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1fdcd-160">TaskSubject</span><span class="sxs-lookup"><span data-stu-id="1fdcd-160">TaskSubject</span></span></p></td>
<td><p><span data-ttu-id="1fdcd-161">Unread</span><span class="sxs-lookup"><span data-stu-id="1fdcd-161">Unread</span></span></p></td>
<td><p><span data-ttu-id="1fdcd-162">VotingOptions</span><span class="sxs-lookup"><span data-stu-id="1fdcd-162">VotingOptions</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="1fdcd-163">Некоторые вычисляемые свойства невозможно добавить в набор столбцов таблицы, но в следующем примере кода выполняется обход этого ограничения.</span><span class="sxs-lookup"><span data-stu-id="1fdcd-163">Although some computed properties cannot be added to the column set for a table, the following code example works around this limitation.</span></span> <span data-ttu-id="1fdcd-164">В процедуре GetToDoItems используется запрос DASL для ограничения элементов, отображающихся в объекте **Table**.</span><span class="sxs-lookup"><span data-stu-id="1fdcd-164">GetToDoItems uses a DASL query to restrict the items that appear in the **Table**.</span></span> <span data-ttu-id="1fdcd-165">Если вычисляемое свойство имеет представление в пространстве имен, это представление используется для создания запроса DASL, который ограничивает объект **Table** и возвращает строки для заданного значения вычисляемого свойства.</span><span class="sxs-lookup"><span data-stu-id="1fdcd-165">If the computed property has a namespace representation, the namespace representation is used to create a DASL query that restricts the **Table** object to return rows for a specified value of the computed property.</span></span> <span data-ttu-id="1fdcd-166">Процедура GetToDoItems получает элементы из папки "Входящие", для которых значение свойства [IsMarkedAsTask](https://msdn.microsoft.com/library/bb623631\(v=office.15\)) равно **true**, а затем присваивает эти значения определенным свойствам задачи, таким как [TaskSubject](https://msdn.microsoft.com/library/bb643880\(v=office.15\)), [TaskDueDate](https://msdn.microsoft.com/library/bb623035\(v=office.15\)), [TaskStartDate](https://msdn.microsoft.com/library/bb610832\(v=office.15\)) и [TaskCompletedDate](https://msdn.microsoft.com/library/bb624055\(v=office.15\)).</span><span class="sxs-lookup"><span data-stu-id="1fdcd-166">GetToDoItems gets items in the Inbox where the value of the [IsMarkedAsTask](https://msdn.microsoft.com/library/bb623631\(v=office.15\)) property is equal to **true**, and then assigns values to certain task properties such as [TaskSubject](https://msdn.microsoft.com/library/bb643880\(v=office.15\)), [TaskDueDate](https://msdn.microsoft.com/library/bb623035\(v=office.15\)), [TaskStartDate](https://msdn.microsoft.com/library/bb610832\(v=office.15\)), and [TaskCompletedDate](https://msdn.microsoft.com/library/bb624055\(v=office.15\)).</span></span> <span data-ttu-id="1fdcd-167">В завершение эти свойства записываются в прослушиватели трассировки коллекции [Listeners](https://msdn.microsoft.com/library/system.diagnostics.debug.listeners.aspx).</span><span class="sxs-lookup"><span data-stu-id="1fdcd-167">Finally, those properties are written to the trace listeners of the [Listeners](https://msdn.microsoft.com/library/system.diagnostics.debug.listeners.aspx) collection.</span></span>

<span data-ttu-id="1fdcd-168">Если для тестирования этого примера кода вы используете Visual Studio, сначала добавьте ссылку на компонент библиотеки объектов Microsoft Outlook 15.0 и укажите переменную Outlook при импорте пространства имен **Microsoft.Office.Interop.Outlook**.</span><span class="sxs-lookup"><span data-stu-id="1fdcd-168">If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the Outlook variable when you import the **Microsoft.Office.Interop.Outlook** namespace.</span></span> <span data-ttu-id="1fdcd-169">Не следует использовать инструкцию **using** непосредственно перед функциями в примере кода, но ее необходимо добавить перед объявлением общедоступного класса.</span><span class="sxs-lookup"><span data-stu-id="1fdcd-169">The **using** statement must not occur directly before the functions in the code example but must be added before the public Class declaration.</span></span> <span data-ttu-id="1fdcd-170">В следующей строке кода показано, как выполнить импорт и назначение в C\#.</span><span class="sxs-lookup"><span data-stu-id="1fdcd-170">The following line of code shows how to do the import and assignment in C\#.</span></span>

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

## <a name="see-also"></a><span data-ttu-id="1fdcd-171">См. также</span><span class="sxs-lookup"><span data-stu-id="1fdcd-171">See also</span></span>

- [<span data-ttu-id="1fdcd-172">Поиск и фильтрация</span><span class="sxs-lookup"><span data-stu-id="1fdcd-172">Search and filter</span></span>](search-and-filter.md)


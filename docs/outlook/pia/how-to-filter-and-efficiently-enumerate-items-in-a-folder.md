---
title: Фильтрация и эффективное перечисление элементов в папке
TOCTitle: Filter and efficiently enumerate items in a folder
ms:assetid: efee7704-b7d9-4586-a72e-4e960ec1ffdb
ms:mtpsurl: https://msdn.microsoft.com/library/Bb612664(v=office.15)
ms:contentKeyID: 55119884
ms.date: 07/24/2014
mtps_version: v=office.15
ms.openlocfilehash: 01f0019d0f038cd1e9ea8fee7c85d0d2f18c4b47
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25405674"
---
# <a name="filter-and-efficiently-enumerate-items-in-a-folder"></a>Фильтрация и эффективное перечисление элементов в папке

В этом примере показано, как использовать объект [Table](https://msdn.microsoft.com/library/bb652856\(v=office.15\)) для фильтрации элементов с вложениями в папке "Входящие", эффективного перечисления таких элементов и показа выбранных свойств для каждого элемента.

## <a name="example"></a>Пример

В примере кода указывается свойство **PR\_HASATTACH** с пространством имен MAPI и используется свойство для создания первоначального фильтра в методе [GetTable](https://msdn.microsoft.com/library/bb612592\(v=office.15\)) в папке "Входящие". В объекте **Table** для типа элемента есть столбцы по умолчанию, представляющие определенные свойства этого типа элемента. Чтобы настроить столбцы, в этом примере сначала вызывается метод [RemoveAll](https://msdn.microsoft.com/library/bb611528\(v=office.15\)) для коллекции [Columns](https://msdn.microsoft.com/library/bb646214\(v=office.15\)) объекта **Table**, а затем вызывается метод [Add](https://msdn.microsoft.com/library/bb652865\(v=office.15\)) для коллекции **Columns**, чтобы добавить свойства **EntryID**, **Subject** и **ReceivedTime** с помощью встроенных имен свойств с сохранением значений даты и времени в локальном представлении в столбце **ReceivedTime**. 

После этого в примере еще раз вызывается **Columns.Add**, чтобы добавить свойство **ReceiveTime**, указывающее пространство имен MAPI, чтобы в этом столбце хранить значения даты и времени в формате UTC. В конце в примере перечисляются все элементы в объекте Table с отображением значения каждого из четырех свойств, указанных в качестве столбцов таблицы.

Если вы используете Visual Studio для тестирования этого примера кода, сначала добавьте ссылку на компонент Microsoft Outlook 15.0 Object Library и задайте переменную Outlook при импорте пространства имен **Microsoft.Office.Interop.Outlook**. Инструкция **Imports** или **using** не должна идти непосредственно перед функциями в примере кода, но ее нужно добавить перед открытым объявлением Class. В следующих строках кода показано, как выполнить импорт и назначение в Visual Basic и C\#.

```vb
Imports Outlook = Microsoft.Office.Interop.Outlook
```


```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```vb
Private Sub DemoTableColumns()
    Const PR_HAS_ATTACH As String = _
        "https://schemas.microsoft.com/mapi/proptag/0x0E1B000B"
    ' Obtain Inbox
    Dim folder As Outlook.Folder = _
        CType(Application.Session.GetDefaultFolder( _
        Outlook.OlDefaultFolders.olFolderInbox), _
        Outlook.Folder)
    ' Create filter
    Dim filter As String = "@SQL=" & Chr(34) _
        & PR_HAS_ATTACH & Chr(34) & " = 1"
    Dim table As Outlook.Table = _
        folder.GetTable(filter, _
        Outlook.OlTableContents.olUserItems)
    ' Remove default columns
    table.Columns.RemoveAll()
    ' Add using built-in name
    table.Columns.Add("EntryID")
    table.Columns.Add("Subject")
    table.Columns.Add("ReceivedTime")
    table.Sort("ReceivedTime", Outlook.OlSortOrder.olDescending)
    ' Add using namespace
    ' Date received
    table.Columns.Add( _
        "urn:schemas:httpmail:datereceived")
    While Not (table.EndOfTable)
        Dim nextRow As Outlook.Row = table.GetNextRow()
        Dim sb As StringBuilder = New StringBuilder()
        sb.AppendLine(nextRow("Subject").ToString())
        ' Reference column by name 
        sb.AppendLine("Received (Local): " _
            & nextRow("ReceivedTime").ToString())
        ' Reference column by index
        sb.AppendLine("Received (UTC): " & nextRow(4).ToString())
        sb.AppendLine()
        Debug.WriteLine(sb.ToString())
    End While
End Sub
```


```csharp
private void DemoTableColumns()
{
    const string PR_HAS_ATTACH =
        "https://schemas.microsoft.com/mapi/proptag/0x0E1B000B";
    // Obtain Inbox
    Outlook.Folder folder =
        Application.Session.GetDefaultFolder(
        Outlook.OlDefaultFolders.olFolderInbox)
        as Outlook.Folder;
    // Create filter
    string filter = "@SQL=" + "\""
        + PR_HAS_ATTACH + "\"" + " = 1";
    Outlook.Table table =
        folder.GetTable(filter,
        Outlook.OlTableContents.olUserItems);
    // Remove default columns
    table.Columns.RemoveAll();
    // Add using built-in name
    table.Columns.Add("EntryID");
    table.Columns.Add("Subject");
    table.Columns.Add("ReceivedTime");
    table.Sort("ReceivedTime", Outlook.OlSortOrder.olDescending);
    // Add using namespace
    // Date received
    table.Columns.Add(
        "urn:schemas:httpmail:datereceived");
    while (!table.EndOfTable)
    {
        Outlook.Row nextRow = table.GetNextRow();
        StringBuilder sb = new StringBuilder();
        sb.AppendLine(nextRow["Subject"].ToString());
        // Reference column by name 
        sb.AppendLine("Received (Local): "
            + nextRow["ReceivedTime"]);
        // Reference column by index
        sb.AppendLine("Received (UTC): " + nextRow[4]);
        sb.AppendLine();
        Debug.WriteLine(sb.ToString());
    }
}
```

## <a name="see-also"></a>См. также

- [Поиск и фильтрация](search-and-filter.md)


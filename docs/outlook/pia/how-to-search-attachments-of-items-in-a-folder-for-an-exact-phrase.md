---
title: Поиск точной фразы во вложениях элементов в папке
TOCTitle: Search attachments of items in a folder for an exact phrase
ms:assetid: 3202c0c7-ee3d-4396-b3a9-d24990b44829
ms:mtpsurl: https://msdn.microsoft.com/library/Bb609825(v=office.15)
ms:contentKeyID: 55119889
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: f237a2268fd287e96959dfc0522103b47e55d37b
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28698297"
---
# <a name="search-attachments-of-items-in-a-folder-for-an-exact-phrase"></a>Поиск точной фразы во вложениях элементов в папке

В этом примере выполняется поиск точной строки поиска "office" во вложениях элементов в папке "Входящие".

## <a name="example"></a>Пример

В этом примере кода используется синтаксис DASL для определения запроса. Для создания фильтра в коде сначала проверяется, включена ли в хранилище по умолчанию функция мгновенного поиска, чтобы определить, использовать ли ключевое слово **ci\_phrasematch** для поиска точного совпадения фразы с "office" во вложении. Затем в примере применяется фильтр к методу [GetTable](https://msdn.microsoft.com/library/bb612592\(v=office.15\)) в папке "Входящие" с получением результатов в объекте [Table](https://msdn.microsoft.com/library/bb652856\(v=office.15\)). После этого в примере кода отображается тема каждого возвращенного элемента в объекте **Table**.

Значение свойства **Attachments** в примере кода задается с помощью представления пространства имен, https://schemas.microsoft.com/mapi/proptag/0x0EA5001E. Для ключевого слова **ci\_phrasematch** используется следующий синтаксис:

`<PropertySchemaName> ci_phrasematch <ComparisonString>`

Если вы используете Visual Studio для тестирования этого примера кода, сначала добавьте ссылку на компонент Microsoft Outlook 15.0 Object Library и задайте переменную Outlook при импорте пространства имен **Microsoft.Office.Interop.Outlook**. Инструкция **Imports** или **using** не должна идти непосредственно перед функциями в примере кода, но ее нужно добавить перед открытым объявлением Class. В следующих строках кода показано, как выполнить импорт и назначение в Visual Basic и C\#.

```vb
Imports Outlook = Microsoft.Office.Interop.Outlook
```


```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```vb
Private Sub DemoSearchAttachments()
    Dim filter As String
    Const PR_SEARCH_ATTACHMENTS As String = _
        "https://schemas.microsoft.com/mapi/proptag/0x0EA5001E"
    If (Application.Session.DefaultStore.IsInstantSearchEnabled) Then
        filter = "@SQL=" & Chr(34) _
            & PR_SEARCH_ATTACHMENTS & Chr(34) _
            & " ci_phrasematch 'office'"
        Dim table As Outlook.Table = _
            Application.Session.GetDefaultFolder( _
            Outlook.OlDefaultFolders.olFolderInbox).GetTable( _
            filter, Outlook.OlTableContents.olUserItems)
        While Not (table.EndOfTable)
            Dim row As Outlook.Row = table.GetNextRow()
            Debug.WriteLine(row("Subject"))
        End While
    End If
End Sub
```


```csharp
private void DemoSearchAttachments()
{
    string filter;
    const string PR_SEARCH_ATTACHMENTS =
        "https://schemas.microsoft.com/mapi/proptag/0x0EA5001E";
    if (Application.Session.DefaultStore.IsInstantSearchEnabled)
    {
        filter = "@SQL=" + "\""
            + PR_SEARCH_ATTACHMENTS + "\""
            + " ci_phrasematch 'office'";
        Outlook.Table table = Application.Session.GetDefaultFolder(
            Outlook.OlDefaultFolders.olFolderInbox).GetTable(
            filter, Outlook.OlTableContents.olUserItems);
        while (!table.EndOfTable)
        {
            Outlook.Row row = table.GetNextRow();
            Debug.WriteLine(row["Subject"]);
        }
    }
}
```

## <a name="see-also"></a>См. также

- [Поиск и фильтрация](search-and-filter.md)


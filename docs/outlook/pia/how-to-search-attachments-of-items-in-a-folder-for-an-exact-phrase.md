---
title: Поиск точной фразы во вложениях элементов в папке
TOCTitle: Search attachments of items in a folder for an exact phrase
ms:assetid: 3202c0c7-ee3d-4396-b3a9-d24990b44829
ms:mtpsurl: https://docs.microsoft.com/office/client-developer/outlook/pia/how-to-search-attachments-of-items-in-a-folder-for-an-exact-phrase?redirectedfrom=MSDN
ms:contentKeyID: 55119889
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 3d14da44731810308d57ba0e70f9651f3105aad0
ms.sourcegitcommit: 31b0a7373ff74fe1d6383c30bc67d7675b73d283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/05/2020
ms.locfileid: "41773717"
---
# <a name="search-attachments-of-items-in-a-folder-for-an-exact-phrase"></a>Поиск точной фразы во вложениях элементов в папке

В этом примере выполняется поиск точной строки поиска "office" во вложениях элементов в папке "Входящие".

## <a name="example"></a>Пример

В этом примере кода используется синтаксис DASL для определения запроса. Для создания фильтра в коде сначала проверяется, включена ли в хранилище по умолчанию функция мгновенного поиска, чтобы определить, использовать ли ключевое слово **ci\_phrasematch** для поиска точного совпадения фразы с "office" во вложении. Затем в примере применяется фильтр к методу [GetTable](https://docs.microsoft.com/dotnet/api/microsoft.office.interop.outlook.mapifolder.gettable?redirectedfrom=MSDN&view=outlook-pia#Microsoft_Office_Interop_Outlook_MAPIFolder_GetTable_System_Object_System_Object_) в папке "Входящие" с получением результатов в объекте [Table](https://docs.microsoft.com/dotnet/api/microsoft.office.interop.outlook.table?redirectedfrom=MSDN&view=outlook-pia). После этого в примере кода отображается тема каждого возвращенного элемента в объекте **Table**.

Значение свойства **Attachments** в примере кода задается с помощью представления пространства имен, https://schemas.microsoft.com/mapi/proptag/0x0EA5001E. Для ключевого слова **ci\_phrasematch** используется следующий синтаксис:

`<PropertySchemaName> ci_phrasematch <ComparisonString>`

Если для тестирования этого примера кода вы используете Visual Studio, сначала добавьте ссылку на компонент библиотеки объектов Microsoft Outlook 15.0 и укажите переменную Outlook при импорте пространства имен **Microsoft.Office.Interop.Outlook**. Инструкция **Imports** или **using** не должна идти непосредственно перед функциями в примере кода, но ее нужно добавить перед объявлением общедоступного класса. В строках кода ниже показано, как выполнить импорт и назначение на Visual Basic и C\#.

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
        "http://schemas.microsoft.com/mapi/proptag/0x0EA5001E"
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
        "http://schemas.microsoft.com/mapi/proptag/0x0EA5001E";
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


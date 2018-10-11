---
title: Поиск фразы в тексте элементов в папке
TOCTitle: Search for a phrase in the body of items in a folder
ms:assetid: 2c9f3b5f-ed91-4a07-b247-8f89f00cbc68
ms:mtpsurl: https://msdn.microsoft.com/library/Bb644806(v=office.15)
ms:contentKeyID: 55119924
ms.date: 07/24/2014
mtps_version: v=office.15
ms.openlocfilehash: 2792e5bd96547975d878f89a7e186c24c4983d8f
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25406934"
---
# <a name="search-for-a-phrase-in-the-body-of-items-in-a-folder"></a>Поиск фразы в тексте элементов в папке

В этом примере выполняется поиск строки "office" в тексте элементов в папке "Входящие".

## <a name="example"></a>Пример

В этом примере кода используется синтаксис DASL для определения запроса. Для создания фильтра в коде примера сначала проверяется, включена ли в хранилище по умолчанию функция мгновенного поиска, чтобы определить, использовать ли ключевое слово **ci\_phrasematch** для точного совпадения фразы в тексте элемента с "office" или ключевое слово **like** для поиска любого вхождения "office" как точной строки или подстроки в тексте элемента. Затем в примере применяется фильтр к методу [GetTable](https://msdn.microsoft.com/library/bb612592\(v=office.15\)) в папке "Входящие" с получением результатов в объекте [Table](https://msdn.microsoft.com/library/bb652856\(v=office.15\)). После этого в примере кода отображается тема каждого возвращенного элемента в объекте **Table**.

Значение свойства **Body** в примере кода задается с помощью представления пространства имен urn:schemas:httpmail:textdescription.

Для ключевого слова **ci\_phrasematch** используется следующий синтаксис:

`<PropertySchemaName> ci_phrasematch <ComparisonString>`

Для ключевого слова **like** при сопоставлении префикса используется следующий синтаксис:

`<PropertySchemaName> like <Token>%`

Для ключевого слова **like** при сопоставлении любой подстроки используется следующий синтаксис:

`<PropertySchemaName> like %<Token>%`

Если вы используете Visual Studio для тестирования этого примера кода, сначала добавьте ссылку на компонент Microsoft Outlook 15.0 Object Library и задайте переменную Outlook при импорте пространства имен **Microsoft.Office.Interop.Outlook**. Инструкция **Imports** или **using** не должна идти непосредственно перед функциями в примере кода, но ее нужно добавить перед открытым объявлением Class. В следующих строках кода показано, как выполнить импорт и назначение в Visual Basic и C\#.

```vb
Imports Outlook = Microsoft.Office.Interop.Outlook
```


```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```vb
Private Sub DemoSearchBody()
    Dim filter As String
    If (Application.Session.DefaultStore.IsInstantSearchEnabled) Then
        filter = "@SQL=" & Chr(34) _
            & "urn:schemas:httpmail:textdescription" & Chr(34) _
            & " ci_phrasematch 'office'"
    Else
        filter = "@SQL=" & Chr(34) _
            & "urn:schemas:httpmail:textdescription" & Chr(34) _
            & " like '%office%'"
    End If
    Dim table As Outlook.Table = _
        Application.Session.GetDefaultFolder( _
        Outlook.OlDefaultFolders.olFolderInbox).GetTable( _
        filter, Outlook.OlTableContents.olUserItems)
    While Not (table.EndOfTable)
        Dim row As Outlook.Row = table.GetNextRow()
        Debug.WriteLine(row("Subject"))
    End While
End Sub
```


```csharp
private void DemoSearchBody()
{
    string filter;
    if (Application.Session.DefaultStore.IsInstantSearchEnabled)
    {
        filter = "@SQL=" + "\""
            + "urn:schemas:httpmail:textdescription" + "\""
            + " ci_phrasematch 'office'";
    }
    else
    {
        filter = "@SQL=" + "\""
            + "urn:schemas:httpmail:textdescription" + "\""
            + " like '%office%'";
    }
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


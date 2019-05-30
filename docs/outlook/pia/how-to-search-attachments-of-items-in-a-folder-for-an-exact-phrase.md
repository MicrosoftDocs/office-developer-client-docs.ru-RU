---
title: Поиск точной фразы во вложениях элементов в папке
TOCTitle: Search attachments of items in a folder for an exact phrase
ms:assetid: 3202c0c7-ee3d-4396-b3a9-d24990b44829
ms:mtpsurl: https://msdn.microsoft.com/library/Bb609825(v=office.15)
ms:contentKeyID: 55119889
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 615b90a8423493a9e202e51993eea1c8127a9939
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/29/2019
ms.locfileid: "34540898"
---
# <a name="search-attachments-of-items-in-a-folder-for-an-exact-phrase"></a><span data-ttu-id="c5075-102">Поиск точной фразы во вложениях элементов в папке</span><span class="sxs-lookup"><span data-stu-id="c5075-102">Search attachments of items in a folder for an exact phrase</span></span>

<span data-ttu-id="c5075-103">В этом примере выполняется поиск точной строки поиска "office" во вложениях элементов в папке "Входящие".</span><span class="sxs-lookup"><span data-stu-id="c5075-103">This example searches for the exact search string "office" in attachments to items in the Inbox.</span></span>

## <a name="example"></a><span data-ttu-id="c5075-104">Пример</span><span class="sxs-lookup"><span data-stu-id="c5075-104">Example</span></span>

<span data-ttu-id="c5075-105">В этом примере кода используется синтаксис DASL для определения запроса.</span><span class="sxs-lookup"><span data-stu-id="c5075-105">This code sample uses a DAV Searching and Locating (DASL) syntax to specify a query.</span></span> <span data-ttu-id="c5075-106">Для создания фильтра в коде сначала проверяется, включена ли в хранилище по умолчанию функция мгновенного поиска, чтобы определить, использовать ли ключевое слово **ci\_phrasematch** для поиска точного совпадения фразы с "office" во вложении.</span><span class="sxs-lookup"><span data-stu-id="c5075-106">To construct the filter, the code sample first checks whether Instant Search is enabled in the default store to determine whether to use the **ci\_phrasematch** keyword for an exact phrase match to "office" in any attachment.</span></span> <span data-ttu-id="c5075-107">Затем в примере применяется фильтр к методу [GetTable](https://msdn.microsoft.com/library/bb612592\(v=office.15\)) в папке "Входящие" с получением результатов в объекте [Table](https://msdn.microsoft.com/library/bb652856\(v=office.15\)).</span><span class="sxs-lookup"><span data-stu-id="c5075-107">The sample then applies the filter to the [GetTable](https://msdn.microsoft.com/library/bb612592\(v=office.15\)) method on the Inbox and obtains the results in a [Table](https://msdn.microsoft.com/library/bb652856\(v=office.15\)) object.</span></span> <span data-ttu-id="c5075-108">После этого в примере кода отображается тема каждого возвращенного элемента в объекте **Table**.</span><span class="sxs-lookup"><span data-stu-id="c5075-108">The code sample then displays the subject of each of the returned items in the **Table**.</span></span>

<span data-ttu-id="c5075-109">Значение свойства **Attachments** в примере кода задается с помощью представления пространства имен, http://schemas.microsoft.com/mapi/proptag/0x0EA5001E.</span><span class="sxs-lookup"><span data-stu-id="c5075-109">The code sample specifies the **Attachments** property of an item using the namespace representation, http://schemas.microsoft.com/mapi/proptag/0x0EA5001E.</span></span> <span data-ttu-id="c5075-110">Для ключевого слова **ci\_phrasematch** используется следующий синтаксис:</span><span class="sxs-lookup"><span data-stu-id="c5075-110">The syntax for using the **ci\_phrasematch** keyword is:</span></span>

`<PropertySchemaName> ci_phrasematch <ComparisonString>`

<span data-ttu-id="c5075-111">Если для тестирования этого примера кода вы используете Visual Studio, сначала добавьте ссылку на компонент библиотеки объектов Microsoft Outlook 15.0 и укажите переменную Outlook при импорте пространства имен **Microsoft.Office.Interop.Outlook**.</span><span class="sxs-lookup"><span data-stu-id="c5075-111">If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the Outlook variable when you import the **Microsoft.Office.Interop.Outlook** namespace.</span></span> <span data-ttu-id="c5075-112">Инструкция **Imports** или **using** не должна идти непосредственно перед функциями в примере кода, но ее нужно добавить перед объявлением общедоступного класса.</span><span class="sxs-lookup"><span data-stu-id="c5075-112">The **Imports** or **using** statement must not occur directly before the functions in the code example but must be added before the public Class declaration.</span></span> <span data-ttu-id="c5075-113">В строках кода ниже показано, как выполнить импорт и назначение на Visual Basic и C\#.</span><span class="sxs-lookup"><span data-stu-id="c5075-113">The following lines of code show how to do the import and assignment in Visual Basic and C\#.</span></span>

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

## <a name="see-also"></a><span data-ttu-id="c5075-114">См. также</span><span class="sxs-lookup"><span data-stu-id="c5075-114">See also</span></span>

- [<span data-ttu-id="c5075-115">Поиск и фильтрация</span><span class="sxs-lookup"><span data-stu-id="c5075-115">Search and filter</span></span>](search-and-filter.md)


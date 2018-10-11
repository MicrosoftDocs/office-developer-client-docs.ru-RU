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
# <a name="search-for-a-phrase-in-the-body-of-items-in-a-folder"></a><span data-ttu-id="cc437-102">Поиск фразы в тексте элементов в папке</span><span class="sxs-lookup"><span data-stu-id="cc437-102">Search for a phrase in the body of items in a folder</span></span>

<span data-ttu-id="cc437-103">В этом примере выполняется поиск строки "office" в тексте элементов в папке "Входящие".</span><span class="sxs-lookup"><span data-stu-id="cc437-103">This example searches for the string "office" in the Body of items in the Inbox.</span></span>

## <a name="example"></a><span data-ttu-id="cc437-104">Пример</span><span class="sxs-lookup"><span data-stu-id="cc437-104">Example</span></span>

<span data-ttu-id="cc437-105">В этом примере кода используется синтаксис DASL для определения запроса.</span><span class="sxs-lookup"><span data-stu-id="cc437-105">This code sample uses a DAV Searching and Locating (DASL) syntax to specify a query.</span></span> <span data-ttu-id="cc437-106">Для создания фильтра в коде примера сначала проверяется, включена ли в хранилище по умолчанию функция мгновенного поиска, чтобы определить, использовать ли ключевое слово **ci\_phrasematch** для точного совпадения фразы в тексте элемента с "office" или ключевое слово **like** для поиска любого вхождения "office" как точной строки или подстроки в тексте элемента.</span><span class="sxs-lookup"><span data-stu-id="cc437-106">To construct the filter, the code sample first checks if Instant Search is enabled in the default store to determine whether to use the ci_phrasematch keyword for an exact phrase match of "office" in the item body, or the like keyword to match any occurrence of "office" as an exact string or a substring in the item body.</span></span> <span data-ttu-id="cc437-107">Затем в примере применяется фильтр к методу [GetTable](https://msdn.microsoft.com/library/bb612592\(v=office.15\)) в папке "Входящие" с получением результатов в объекте [Table](https://msdn.microsoft.com/library/bb652856\(v=office.15\)).</span><span class="sxs-lookup"><span data-stu-id="cc437-107">The sample then applies the filter to the [GetTable](https://msdn.microsoft.com/library/bb612592\(v=office.15\)) method on the Inbox and obtains the results in a [Table](https://msdn.microsoft.com/library/bb652856\(v=office.15\)) object.</span></span> <span data-ttu-id="cc437-108">После этого в примере кода отображается тема каждого возвращенного элемента в объекте **Table**.</span><span class="sxs-lookup"><span data-stu-id="cc437-108">The code sample then displays the subject of each of the returned items in the **Table**.</span></span>

<span data-ttu-id="cc437-109">Значение свойства **Body** в примере кода задается с помощью представления пространства имен urn:schemas:httpmail:textdescription.</span><span class="sxs-lookup"><span data-stu-id="cc437-109">The code sample specifies the Body property by using the namespace representation urn:schemas:httpmail:textdescription.</span></span>

<span data-ttu-id="cc437-110">Для ключевого слова **ci\_phrasematch** используется следующий синтаксис:</span><span class="sxs-lookup"><span data-stu-id="cc437-110">The syntax for using the ci_phrasematch keyword is:</span></span>

`<PropertySchemaName> ci_phrasematch <ComparisonString>`

<span data-ttu-id="cc437-111">Для ключевого слова **like** при сопоставлении префикса используется следующий синтаксис:</span><span class="sxs-lookup"><span data-stu-id="cc437-111">The syntax for using the **like** keyword for prefix matching is:</span></span>

`<PropertySchemaName> like <Token>%`

<span data-ttu-id="cc437-112">Для ключевого слова **like** при сопоставлении любой подстроки используется следующий синтаксис:</span><span class="sxs-lookup"><span data-stu-id="cc437-112">The syntax for using the **like** keyword for any substring matching is:</span></span>

`<PropertySchemaName> like %<Token>%`

<span data-ttu-id="cc437-113">Если вы используете Visual Studio для тестирования этого примера кода, сначала добавьте ссылку на компонент Microsoft Outlook 15.0 Object Library и задайте переменную Outlook при импорте пространства имен **Microsoft.Office.Interop.Outlook**.</span><span class="sxs-lookup"><span data-stu-id="cc437-113">If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the   variable when you import the Microsoft.Office.Interop.Outlook namespace.</span></span> <span data-ttu-id="cc437-114">Инструкция **Imports** или **using** не должна идти непосредственно перед функциями в примере кода, но ее нужно добавить перед открытым объявлением Class.</span><span class="sxs-lookup"><span data-stu-id="cc437-114">The Imports or using statement must not occur directly before the functions in the code example but must be added before the public   declaration.</span></span> <span data-ttu-id="cc437-115">В следующих строках кода показано, как выполнить импорт и назначение в Visual Basic и C\#.</span><span class="sxs-lookup"><span data-stu-id="cc437-115">The following lines of code show how to do the import and assignment in Visual Basic and C#.</span></span>

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

## <a name="see-also"></a><span data-ttu-id="cc437-116">См. также</span><span class="sxs-lookup"><span data-stu-id="cc437-116">See also</span></span>

- [<span data-ttu-id="cc437-117">Поиск и фильтрация</span><span class="sxs-lookup"><span data-stu-id="cc437-117">Search and Filter</span></span>](search-and-filter.md)


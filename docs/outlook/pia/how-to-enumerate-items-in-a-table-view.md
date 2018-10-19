---
title: Перечисление элементов в табличном представлении
TOCTitle: Enumerate items in a table view
ms:assetid: c7d9a667-cfec-49c1-af7a-4c8063991588
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184640(v=office.15)
ms:contentKeyID: 55119900
ms.date: 07/24/2014
mtps_version: v=office.15
ms.openlocfilehash: fbb3b6aa9bed2e08eb11cb58090233d271e5fed3
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25406451"
---
# <a name="enumerate-items-in-a-table-view"></a><span data-ttu-id="f9732-102">Перечисление элементов в табличном представлении</span><span class="sxs-lookup"><span data-stu-id="f9732-102">Enumerate items in a table view</span></span>

<span data-ttu-id="f9732-103">В этом примере показано перечисление элементов в представлении таблицы с помощью метода [GetTable()](https://msdn.microsoft.com/library/ff184699\(v=office.15\)).</span><span class="sxs-lookup"><span data-stu-id="f9732-103">This example enumerates items in a table view by using the [GetTable()](https://msdn.microsoft.com/library/ff184699\(v=office.15\)) method.</span></span>

## <a name="example"></a><span data-ttu-id="f9732-104">Пример</span><span class="sxs-lookup"><span data-stu-id="f9732-104">Example</span></span>

<span data-ttu-id="f9732-p101">В следующем образце кода выполняется получение объекта [Table](https://msdn.microsoft.com/library/bb652856\(v=office.15\)) из текущего представления папки "Входящие". Здесь в качестве текущей папки Проводника задается папка "Входящие". Затем выполняется проверка того, что текущее представление папки "Входящие" является табличным. Если текущее представление выводится в виде таблицы, в примере кода вызывается метод [GetTable()](https://msdn.microsoft.com/library/ff184699\(v=office.15\)) и показывается каждый элемент, которому соответствует строка в возвращенной таблице **Table**.</span><span class="sxs-lookup"><span data-stu-id="f9732-p101">The following code example obtains a [Table](https://msdn.microsoft.com/library/bb652856\(v=office.15\)) object from the current view of the Inbox folder. The code example sets the current folder of the active explorer to the Inbox, and then checks that the current view of the Inbox is a table view. If the current view is a table, the code example calls the [GetTable()](https://msdn.microsoft.com/library/ff184699\(v=office.15\)) method and displays each item represented by each row in the returned **Table**.</span></span>

<span data-ttu-id="f9732-108">Если вы используете Visual Studio для тестирования этого примера кода, сначала добавьте ссылку на компонент библиотеки объектов Microsoft Outlook 15.0 и задайте переменную Outlook при импорте пространства имен **Microsoft.Office.Interop.Outlook**.</span><span class="sxs-lookup"><span data-stu-id="f9732-108">If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the   variable when you import the Microsoft.Office.Interop.Outlook namespace.</span></span> <span data-ttu-id="f9732-109">Инструкция **using** не должна находиться непосредственно перед функциями в примере кода, но ее нужно добавить перед объявлением общедоступного класса.</span><span class="sxs-lookup"><span data-stu-id="f9732-109">The using statement must not occur directly before the functions in the code example but must be added before the public   declaration.</span></span> <span data-ttu-id="f9732-110">В приведенной ниже строке кода показано, как выполнить импорт и назначение на языке C\#.</span><span class="sxs-lookup"><span data-stu-id="f9732-110">The following line of code shows how to do the import and assignment in C#.</span></span>

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```csharp
private void DemoViewGetTable()
{
    // Obtain Inbox.
    Outlook.Folder inbox =
        Application.Session.GetDefaultFolder(
        Outlook.OlDefaultFolders.olFolderInbox)
        as Outlook.Folder;
    // Set ActiveExplorer.CurrentFolder to Inbox.
    // Inbox must be current folder
    // for View.GetTable to work correctly.
    Application.ActiveExplorer().CurrentFolder = inbox;
    // Ensure that current view is TableView.
    if (inbox.CurrentView.ViewType == 
        Outlook.OlViewType.olTableView)
    {
        Outlook.TableView view = 
            inbox.CurrentView as Outlook.TableView;
        // No arguments needed for View.GetTable.
        Outlook.Table table = view.GetTable();
        Debug.WriteLine("View Count=" 
            + table.GetRowCount().ToString());
        while (!table.EndOfTable)
        {
            // First row in Table.
            Outlook.Row nextRow = table.GetNextRow();
            Debug.WriteLine(nextRow["Subject"]
                + " Modified: "
                + nextRow["LastModificationTime"]);
        }
    }
}
```

## <a name="see-also"></a><span data-ttu-id="f9732-111">См. также</span><span class="sxs-lookup"><span data-stu-id="f9732-111">See also</span></span>

- [<span data-ttu-id="f9732-112">Представления</span><span class="sxs-lookup"><span data-stu-id="f9732-112">Views</span></span>](views.md)


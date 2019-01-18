---
title: Отображение элементов запроса выполнения задачи, отправленных получателю
TOCTitle: Display the task request items sent to a recipient
ms:assetid: 167c3d52-67b5-467c-a7b6-e8cc96002b63
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184591(v=office.15)
ms:contentKeyID: 55119930
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 9ab5e830003fbfb64b44fc9e0d813c7a7c5163bf
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/18/2019
ms.locfileid: "28726052"
---
# <a name="display-the-task-request-items-sent-to-a-recipient"></a><span data-ttu-id="afb32-102">Отображение элементов запроса выполнения задачи, отправленных получателю</span><span class="sxs-lookup"><span data-stu-id="afb32-102">Display the task request items sent to a recipient</span></span>

<span data-ttu-id="afb32-103">В этом примере показано, как отобразить все элементы запроса выполнения задачи, которые находятся в папке "Входящие" получателя.</span><span class="sxs-lookup"><span data-stu-id="afb32-103">This example shows how to display all of the task request items that are in a recipient's Inbox.</span></span>

## <a name="example"></a><span data-ttu-id="afb32-104">Пример</span><span class="sxs-lookup"><span data-stu-id="afb32-104">Example</span></span>

> [!NOTE] 
> <span data-ttu-id="afb32-105">Приведенный ниже пример кода представляет собой фрагмент из книги [Программирование приложений для Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).</span><span class="sxs-lookup"><span data-stu-id="afb32-105">The following code example is an excerpt from [Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).</span></span>

<span data-ttu-id="afb32-106">Объект [TaskRequestItem](https://msdn.microsoft.com/library/bb610737\(v=office.15\)) представляет запрос на назначение задачи другому пользователю.</span><span class="sxs-lookup"><span data-stu-id="afb32-106">A [TaskRequestItem](https://msdn.microsoft.com/library/bb610737\(v=office.15\)) object represents a request to assign a task to another user.</span></span> <span data-ttu-id="afb32-107">**TaskRequestItem** создается, когда элемент получен в папке "Входящие" получателя.</span><span class="sxs-lookup"><span data-stu-id="afb32-107">The **TaskRequestItem** is created when the item is received in the recipient's Inbox.</span></span> <span data-ttu-id="afb32-108">В представленном ниже примере кода ShowTaskRequests выполняет фильтрацию папки "Входящие" получателя, создает объект [Table](https://msdn.microsoft.com/library/bb652856\(v=office.15\)) и вставляет строку для каждого элемента, для которого значение свойства [MessageClass](https://msdn.microsoft.com/library/bb610592\(v=office.15\)) равно **IPM.TaskRequest**.</span><span class="sxs-lookup"><span data-stu-id="afb32-108">In the following code example, ShowTaskRequests filters through a recipient’s Inbox, creates a [Table](https://msdn.microsoft.com/library/bb652856\(v=office.15\)) object, and inserts a row for each item for which the value of the [MessageClass](https://msdn.microsoft.com/library/bb610592\(v=office.15\)) property equals **IPM.TaskRequest**.</span></span> <span data-ttu-id="afb32-109">После этого тема каждой задачи в папке "Входящие" записывается в прослушивателях трассировки коллекции [Listeners](https://msdn.microsoft.com/library/system.diagnostics.debug.listeners.aspx).</span><span class="sxs-lookup"><span data-stu-id="afb32-109">The subject of each task in the recipient’s Inbox folder is then written to the trace listeners of the [Listeners](https://msdn.microsoft.com/library/system.diagnostics.debug.listeners.aspx) collection.</span></span>

<span data-ttu-id="afb32-110">Если вы используете Visual Studio для тестирования этого примера кода, сначала добавьте ссылку на компонент Microsoft Outlook 15.0 Object Library и задайте переменную Outlook при импорте пространства имен **Microsoft.Office.Interop.Outlook**.</span><span class="sxs-lookup"><span data-stu-id="afb32-110">If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the Outlook variable when you import the **Microsoft.Office.Interop.Outlook** namespace.</span></span> <span data-ttu-id="afb32-111">Инструкция **using** не должна идти непосредственно перед функциями в примере кода, но ее нужно добавить перед открытым объявлением Class.</span><span class="sxs-lookup"><span data-stu-id="afb32-111">The **using** statement must not occur directly before the functions in the code example but must be added before the public Class declaration.</span></span> <span data-ttu-id="afb32-112">В следующей строке кода показано, как выполнить импорт и назначение в C\#.</span><span class="sxs-lookup"><span data-stu-id="afb32-112">The following line of code shows how to do the import and assignment in C\#.</span></span>

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```csharp
private void ShowTaskRequests()
{
    string filter = "[MessageClass] = 'IPM.TaskRequest'";
    Outlook.Table table =
        Application.Session.GetDefaultFolder
        (Outlook.OlDefaultFolders.olFolderInbox).GetTable
        (filter, Outlook.OlTableContents.olUserItems);
    while (!table.EndOfTable)
    {
        Outlook.Row nextRow = table.GetNextRow();
        Debug.WriteLine(nextRow["Subject"]);
    }
}
```

## <a name="see-also"></a><span data-ttu-id="afb32-113">См. также</span><span class="sxs-lookup"><span data-stu-id="afb32-113">See also</span></span>

- [<span data-ttu-id="afb32-114">Задачи</span><span class="sxs-lookup"><span data-stu-id="afb32-114">Tasks</span></span>](tasks.md)


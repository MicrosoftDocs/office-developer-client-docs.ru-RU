---
title: Назначение задачи получателю
TOCTitle: Assign a task to a recipient
ms:assetid: c6be97a7-de3f-43e5-9111-534d0f04e986
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184639(v=office.15)
ms:contentKeyID: 55119929
ms.date: 07/24/2014
mtps_version: v=office.15
ms.openlocfilehash: 55063cfd6c448fe32a9d4348069266b9e4a8b566
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25406332"
---
# <a name="assign-a-task-to-a-recipient"></a><span data-ttu-id="fe7bb-102">Назначение задачи получателю</span><span class="sxs-lookup"><span data-stu-id="fe7bb-102">Assign a task to a recipient</span></span>

<span data-ttu-id="fe7bb-103">В этом примере показано, как создать задачу и назначить ее получателю.</span><span class="sxs-lookup"><span data-stu-id="fe7bb-103">This example shows how to create a task and assign it to a recipient.</span></span>

## <a name="example"></a><span data-ttu-id="fe7bb-104">Пример</span><span class="sxs-lookup"><span data-stu-id="fe7bb-104">Example</span></span>

> [!NOTE] 
> <span data-ttu-id="fe7bb-105">Приведенный ниже пример кода представляет собой фрагмент из книги [Программирование приложений для Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).</span><span class="sxs-lookup"><span data-stu-id="fe7bb-105">The following code example is an excerpt from  [Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493)  , from Microsoft Press (ISBN 9780735622494, copyright Microsoft Press 2007, all rights reserved).</span></span>


<span data-ttu-id="fe7bb-106">В представленном ниже примере кода AssignTaskExample создает объект [TaskItem](https://msdn.microsoft.com/library/bb624227\(v=office.15\)) и задает значения для свойств [Subject](https://msdn.microsoft.com/library/bb624148\(v=office.15\)), [StartDate](https://msdn.microsoft.com/library/bb643988\(v=office.15\)) и [DueDate](https://msdn.microsoft.com/library/bb612307\(v=office.15\)).</span><span class="sxs-lookup"><span data-stu-id="fe7bb-106">In the following code example, AssignTaskExample creates a [TaskItem](https://msdn.microsoft.com/library/bb624227\(v=office.15\)) object and specifies values for the [Subject](https://msdn.microsoft.com/library/bb624148\(v=office.15\)), [StartDate](https://msdn.microsoft.com/library/bb643988\(v=office.15\)), and [DueDate](https://msdn.microsoft.com/library/bb612307\(v=office.15\)) properties.</span></span> <span data-ttu-id="fe7bb-107">Метод [Assign()](https://msdn.microsoft.com/library/bb644565\(v=office.15\)) указывает, что задача является назначенной.</span><span class="sxs-lookup"><span data-stu-id="fe7bb-107">The [Assign()](https://msdn.microsoft.com/library/bb644565\(v=office.15\)) method specifies that the task is an assigned task.</span></span> <span data-ttu-id="fe7bb-108">После добавления объекта [Recipient](https://msdn.microsoft.com/library/bb624370\(v=office.15\)) в **TaskItem** с помощью метода [Add(String)](https://msdn.microsoft.com/library/bb612668\(v=office.15\)) метод [Send()](https://msdn.microsoft.com/library/bb646608\(v=office.15\)) отправляет задачу получателю.</span><span class="sxs-lookup"><span data-stu-id="fe7bb-108">After a [Recipient](https://msdn.microsoft.com/library/bb624370\(v=office.15\)) object is added to the **TaskItem** by using the [Add(String)](https://msdn.microsoft.com/library/bb612668\(v=office.15\)) method, the [Send()](https://msdn.microsoft.com/library/bb646608\(v=office.15\)) method sends the task to the recipient.</span></span>

<span data-ttu-id="fe7bb-109">Если вы используете Visual Studio для тестирования этого примера кода, сначала добавьте ссылку на компонент Microsoft Outlook 15.0 Object Library и задайте переменную Outlook при импорте пространства имен **Microsoft.Office.Interop.Outlook**.</span><span class="sxs-lookup"><span data-stu-id="fe7bb-109">If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the   variable when you import the Microsoft.Office.Interop.Outlook namespace.</span></span> <span data-ttu-id="fe7bb-110">Инструкция **using** не должна идти непосредственно перед функциями в примере кода, но ее нужно добавить перед открытым объявлением Class.</span><span class="sxs-lookup"><span data-stu-id="fe7bb-110">The using statement must not occur directly before the functions in the code example but must be added before the public   declaration.</span></span> <span data-ttu-id="fe7bb-111">В следующей строке кода показано, как выполнить импорт и назначение в C\#.</span><span class="sxs-lookup"><span data-stu-id="fe7bb-111">The following line of code shows how to do the import and assignment in C#.</span></span>

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```csharp
private void AssignTaskExample()
{
    Outlook.TaskItem task = Application.CreateItem(
        Outlook.OlItemType.olTaskItem) as Outlook.TaskItem;
    task.Subject = "Tax Preparation";
    task.StartDate = DateTime.Parse("4/1/2007 8:00 AM");
    task.DueDate = DateTime.Parse("4/15/2007 8:00 AM");
    Outlook.RecurrencePattern pattern =
        task.GetRecurrencePattern();
    pattern.RecurrenceType = Outlook.OlRecurrenceType.olRecursYearly;
    pattern.PatternStartDate = DateTime.Parse("4/1/2007");
    pattern.NoEndDate = true;
    task.ReminderSet = true;
    task.ReminderTime = DateTime.Parse("4/1/2007 8:00 AM");
    task.Assign();
    task.Recipients.Add("accountant@example.com");
    task.Recipients.ResolveAll();
    task.Send();
}
```

## <a name="see-also"></a><span data-ttu-id="fe7bb-112">См. также</span><span class="sxs-lookup"><span data-stu-id="fe7bb-112">See also</span></span>

- [<span data-ttu-id="fe7bb-113">Задачи</span><span class="sxs-lookup"><span data-stu-id="fe7bb-113">Tasks</span></span>](tasks.md)


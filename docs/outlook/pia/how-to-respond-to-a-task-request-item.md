---
title: Ответ на элемент запроса выполнения задачи
TOCTitle: Respond to a task request item
ms:assetid: 573c98ef-4d15-4fd1-bccd-25a22c9a63f0
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184608(v=office.15)
ms:contentKeyID: 55119896
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 9aa6416680bbf2443506415b5fa871d30fe5f32e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357395"
---
# <a name="respond-to-a-task-request-item"></a><span data-ttu-id="b2296-102">Ответ на элемент запроса выполнения задачи</span><span class="sxs-lookup"><span data-stu-id="b2296-102">Respond to a task request item</span></span>

<span data-ttu-id="b2296-103">В этом примере показано, как получить запрос элемента задачи и ответить на него.</span><span class="sxs-lookup"><span data-stu-id="b2296-103">This example shows how to get and respond to a task request item.</span></span>

## <a name="example"></a><span data-ttu-id="b2296-104">Пример</span><span class="sxs-lookup"><span data-stu-id="b2296-104">Example</span></span>

> [!NOTE] 
> <span data-ttu-id="b2296-105">Приведенный ниже пример кода взят из книги [Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493) ("Программирование приложений для Microsoft Office Outlook 2007").</span><span class="sxs-lookup"><span data-stu-id="b2296-105">The following code example is an excerpt from [Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).</span></span>

<span data-ttu-id="b2296-106">В примере кода ниже метод AcceptTaskRequest использует метод [GetAssociatedTask(Boolean)](https://msdn.microsoft.com/library/bb645779\(v=office.15\)) объекта [TaskRequestItem](https://msdn.microsoft.com/library/bb610737\(v=office.15\)), чтобы получить объект [TaskItem](https://msdn.microsoft.com/library/bb624227\(v=office.15\)).</span><span class="sxs-lookup"><span data-stu-id="b2296-106">In the following code example, AcceptTaskRequest uses the [GetAssociatedTask(Boolean)](https://msdn.microsoft.com/library/bb645779\(v=office.15\)) method of the [TaskRequestItem](https://msdn.microsoft.com/library/bb610737\(v=office.15\)) object to get the [TaskItem](https://msdn.microsoft.com/library/bb624227\(v=office.15\)) object.</span></span> <span data-ttu-id="b2296-107">Затем код в примере вызывает метод [Respond(OlTaskResponse, Object, Object)](https://msdn.microsoft.com/library/bb644188\(v=office.15\)), параметру которого присвоено значение [olTaskAccept](https://msdn.microsoft.com/library/bb624484\(v=office.15\)), чтобы принять запрос выполнения задачи.</span><span class="sxs-lookup"><span data-stu-id="b2296-107">The example then calls the [Respond(OlTaskResponse, Object, Object)](https://msdn.microsoft.com/library/bb644188\(v=office.15\)) method with the parameter set to [olTaskAccept](https://msdn.microsoft.com/library/bb624484\(v=office.15\)) to accept the task request.</span></span>

<span data-ttu-id="b2296-108">Если вы используете Visual Studio для тестирования этого примера кода, сначала добавьте ссылку на компонент Microsoft Outlook 15.0 Object Library и задайте переменную Outlook при импорте пространства имен **Microsoft.Office.Interop.Outlook**.</span><span class="sxs-lookup"><span data-stu-id="b2296-108">If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the Outlook variable when you import the **Microsoft.Office.Interop.Outlook** namespace.</span></span> <span data-ttu-id="b2296-109">Инструкция **using** не должна находиться непосредственно перед функциями в примере кода, но ее нужно добавить перед объявлением общедоступного класса.</span><span class="sxs-lookup"><span data-stu-id="b2296-109">The **using** statement must not occur directly before the functions in the code example but must be added before the public Class declaration.</span></span> <span data-ttu-id="b2296-110">В приведенной ниже строке кода показано, как выполнить импорт и назначение на языке C\#.</span><span class="sxs-lookup"><span data-stu-id="b2296-110">The following line of code shows how to do the import and assignment in C\#.</span></span>

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```csharp
private void AcceptTaskRequest()
{
    string filter = "[MessageClass] = 'IPM.TaskRequest'";
    Outlook.Items items =
        Application.Session.GetDefaultFolder
        (Outlook.OlDefaultFolders.olFolderInbox).
        Items.Restrict(filter);
    if (items.Count > 0)
    {
        Outlook.TaskRequestItem taskRequest =
            (Outlook.TaskRequestItem)items[1];
        Outlook.TaskItem task =
            taskRequest.GetAssociatedTask(false);
        Outlook.TaskItem taskResponse = task.Respond(
            Outlook.OlTaskResponse.olTaskAccept, true, false);
        taskResponse.Send();
    }
}
```

## <a name="see-also"></a><span data-ttu-id="b2296-111">См. также</span><span class="sxs-lookup"><span data-stu-id="b2296-111">See also</span></span>

- [<span data-ttu-id="b2296-112">Задачи</span><span class="sxs-lookup"><span data-stu-id="b2296-112">Tasks</span></span>](tasks.md)


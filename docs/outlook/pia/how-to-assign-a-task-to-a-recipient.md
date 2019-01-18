---
title: Назначение задачи получателю
TOCTitle: Assign a task to a recipient
ms:assetid: c6be97a7-de3f-43e5-9111-534d0f04e986
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184639(v=office.15)
ms:contentKeyID: 55119929
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 54259b00fb3eb67c86985758bb86f5ab7ba120eb
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/18/2019
ms.locfileid: "28726101"
---
# <a name="assign-a-task-to-a-recipient"></a>Назначение задачи получателю

В этом примере показано, как создать задачу и назначить ее получателю.

## <a name="example"></a>Пример

> [!NOTE] 
> Приведенный ниже пример кода представляет собой фрагмент из книги [Программирование приложений для Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).


В представленном ниже примере кода AssignTaskExample создает объект [TaskItem](https://msdn.microsoft.com/library/bb624227\(v=office.15\)) и задает значения для свойств [Subject](https://msdn.microsoft.com/library/bb624148\(v=office.15\)), [StartDate](https://msdn.microsoft.com/library/bb643988\(v=office.15\)) и [DueDate](https://msdn.microsoft.com/library/bb612307\(v=office.15\)). Метод [Assign()](https://msdn.microsoft.com/library/bb644565\(v=office.15\)) указывает, что задача является назначенной. После добавления объекта [Recipient](https://msdn.microsoft.com/library/bb624370\(v=office.15\)) в **TaskItem** с помощью метода [Add(String)](https://msdn.microsoft.com/library/bb612668\(v=office.15\)) метод [Send()](https://msdn.microsoft.com/library/bb646608\(v=office.15\)) отправляет задачу получателю.

Если вы используете Visual Studio для тестирования этого примера кода, сначала добавьте ссылку на компонент Microsoft Outlook 15.0 Object Library и задайте переменную Outlook при импорте пространства имен **Microsoft.Office.Interop.Outlook**. Инструкция **using** не должна идти непосредственно перед функциями в примере кода, но ее нужно добавить перед открытым объявлением Class. В следующей строке кода показано, как выполнить импорт и назначение в C\#.

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

## <a name="see-also"></a>См. также

- [Задачи](tasks.md)


---
title: Создание повторяющейся задачи
TOCTitle: Create a recurring task
ms:assetid: bbca8527-79af-4c00-aae7-a1fd381e707c
ms:mtpsurl: https://msdn.microsoft.com/library/Bb623455(v=office.15)
ms:contentKeyID: 55119932
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 4fd2df68ef866008799a7206e7ae041e5bfd82a3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32349527"
---
# <a name="create-a-recurring-task"></a>Создание повторяющейся задачи

В этом примере показано, как создать повторяющуюся задачу.

## <a name="example"></a>Пример

В этом примере кода показано, как создать объект [TaskItem](https://msdn.microsoft.com/library/bb624227\(v=office.15\)) и с помощью метода [GetRecurrencePattern](https://msdn.microsoft.com/library/bb647080\(v=office.15\)) объекта **TaskItem** превратить обычную задачу в повторяющуюся.

Если для тестирования этого примера кода вы используете Visual Studio, сначала добавьте ссылку на компонент библиотеки объектов Microsoft Outlook 15.0 и укажите переменную Outlook при импорте пространства имен **Microsoft.Office.Interop.Outlook**. Не следует использовать инструкции **Imports** и **using** непосредственно перед функциями в примере кода, но их необходимо добавить перед объявлением общедоступного класса. В строках кода ниже показано, как выполнить импорт и назначение на Visual Basic и C\#.

```vb
Imports Outlook = Microsoft.Office.Interop.Outlook
```


```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```vb
Private Sub CreateRecurringTask()
    Dim task As Outlook.TaskItem = CType(Application.CreateItem( _
        Outlook.OlItemType.olTaskItem), Outlook.TaskItem)
    task.Subject = "Tax Preparation"
    task.StartDate = DateTime.Parse("4/1/2007 8:00 AM")
    task.DueDate = DateTime.Parse("4/15/2007 8:00 AM")
    Dim pattern As Outlook.RecurrencePattern = _
        task.GetRecurrencePattern()
    pattern.RecurrenceType = Outlook.OlRecurrenceType.olRecursYearly
    pattern.PatternStartDate = DateTime.Parse("4/1/2007")
    pattern.NoEndDate = True
    task.ReminderSet = True
    task.ReminderTime = DateTime.Parse("4/1/2007 8:00 AM")
    task.Save()
End Sub
```


```csharp
private void CreateRecurringTask()
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
    task.Save();
}
```

## <a name="see-also"></a>См. также

- [Задачи](tasks.md)


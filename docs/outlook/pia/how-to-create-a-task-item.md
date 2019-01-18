---
title: Создание элемента задачи
TOCTitle: Create a task item
ms:assetid: d458dd31-2771-4a3c-a713-13c7e4e02a74
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184644(v=office.15)
ms:contentKeyID: 55119894
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: c4f9a8f156ec43f446f27c94b2cb061de181b7d4
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28698444"
---
# <a name="create-a-task-item"></a>Создание элемента задачи

В этом примере показано, как создать элемент задачи с помощью метода [MarkAsTask(OlMarkInterval)](https://msdn.microsoft.com/library/bb609068\(v=office.15\)).

## <a name="example"></a>Пример

> [!NOTE] 
> Приведенный ниже пример кода представляет собой фрагмент из книги [Программирование приложений для Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).


В представленном ниже примере кода CreateToDoItemExample создает элемент задачи путем вызова метода **MarkAsTask** для элемента с последующим сохранением элемента. В примере элемент помечается к исполнению завтра и устанавливается напоминание на завтра в 10:00 с помощью свойств [ReminderSet](https://msdn.microsoft.com/library/bb622600\(v=office.15\)) и [ReminderTime](https://msdn.microsoft.com/library/bb622803\(v=office.15\)). Затем в примере используется метод [Save()](https://msdn.microsoft.com/library/bb645518\(v=office.15\)) для сохранения элемента.

Если вы используете Visual Studio для тестирования этого примера кода, сначала добавьте ссылку на компонент Microsoft Outlook 15.0 Object Library и задайте переменную Outlook при импорте пространства имен **Microsoft.Office.Interop.Outlook**. Инструкция **using** не должна идти непосредственно перед функциями в примере кода, но ее нужно добавить перед открытым объявлением Class. В следующей строке кода показано, как выполнить импорт и назначение в C\#.

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```csharp
private void CreateToDoItemExample()
{
    // Date operations
    DateTime today = DateTime.Parse("10:00 AM");
    TimeSpan duration = TimeSpan.FromDays(1);
    DateTime tomorrow = today.Add(duration);
    Outlook.MailItem mail = Application.Session.
        GetDefaultFolder(
        Outlook.OlDefaultFolders.olFolderInbox).Items.Find(
        "[MessageClass]='IPM.Note'") as Outlook.MailItem;
    mail.MarkAsTask(Outlook.OlMarkInterval.olMarkTomorrow);
    mail.TaskStartDate = today;
    mail.ReminderSet = true;
    mail.ReminderTime = tomorrow;
    mail.Save();
}
```

## <a name="see-also"></a>См. также

- [Задачи](tasks.md)


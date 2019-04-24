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
# <a name="respond-to-a-task-request-item"></a>Ответ на элемент запроса выполнения задачи

В этом примере показано, как получить запрос элемента задачи и ответить на него.

## <a name="example"></a>Пример

> [!NOTE] 
> Приведенный ниже пример кода взят из книги [Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493) ("Программирование приложений для Microsoft Office Outlook 2007").

В примере кода ниже метод AcceptTaskRequest использует метод [GetAssociatedTask(Boolean)](https://msdn.microsoft.com/library/bb645779\(v=office.15\)) объекта [TaskRequestItem](https://msdn.microsoft.com/library/bb610737\(v=office.15\)), чтобы получить объект [TaskItem](https://msdn.microsoft.com/library/bb624227\(v=office.15\)). Затем код в примере вызывает метод [Respond(OlTaskResponse, Object, Object)](https://msdn.microsoft.com/library/bb644188\(v=office.15\)), параметру которого присвоено значение [olTaskAccept](https://msdn.microsoft.com/library/bb624484\(v=office.15\)), чтобы принять запрос выполнения задачи.

Если для тестирования этого примера кода вы используете Visual Studio, сначала добавьте ссылку на компонент библиотеки объектов Microsoft Outlook 15.0 и укажите переменную Outlook при импорте пространства имен **Microsoft.Office.Interop.Outlook**. Инструкция **using** не должна находиться непосредственно перед функциями в примере кода, но ее нужно добавить перед объявлением общедоступного класса. В приведенной ниже строке кода показано, как выполнить импорт и назначение на языке C\#.

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

## <a name="see-also"></a>См. также

- [Задачи](tasks.md)


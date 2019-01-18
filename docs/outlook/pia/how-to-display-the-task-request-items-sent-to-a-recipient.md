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
# <a name="display-the-task-request-items-sent-to-a-recipient"></a>Отображение элементов запроса выполнения задачи, отправленных получателю

В этом примере показано, как отобразить все элементы запроса выполнения задачи, которые находятся в папке "Входящие" получателя.

## <a name="example"></a>Пример

> [!NOTE] 
> Приведенный ниже пример кода представляет собой фрагмент из книги [Программирование приложений для Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).

Объект [TaskRequestItem](https://msdn.microsoft.com/library/bb610737\(v=office.15\)) представляет запрос на назначение задачи другому пользователю. **TaskRequestItem** создается, когда элемент получен в папке "Входящие" получателя. В представленном ниже примере кода ShowTaskRequests выполняет фильтрацию папки "Входящие" получателя, создает объект [Table](https://msdn.microsoft.com/library/bb652856\(v=office.15\)) и вставляет строку для каждого элемента, для которого значение свойства [MessageClass](https://msdn.microsoft.com/library/bb610592\(v=office.15\)) равно **IPM.TaskRequest**. После этого тема каждой задачи в папке "Входящие" записывается в прослушивателях трассировки коллекции [Listeners](https://msdn.microsoft.com/library/system.diagnostics.debug.listeners.aspx).

Если вы используете Visual Studio для тестирования этого примера кода, сначала добавьте ссылку на компонент Microsoft Outlook 15.0 Object Library и задайте переменную Outlook при импорте пространства имен **Microsoft.Office.Interop.Outlook**. Инструкция **using** не должна идти непосредственно перед функциями в примере кода, но ее нужно добавить перед открытым объявлением Class. В следующей строке кода показано, как выполнить импорт и назначение в C\#.

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

## <a name="see-also"></a>См. также

- [Задачи](tasks.md)


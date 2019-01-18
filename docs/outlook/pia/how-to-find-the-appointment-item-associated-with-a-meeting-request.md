---
title: Поиск элемента встречи, связанного с приглашением на собрание
TOCTitle: Find the appointment item associated with a meeting request
ms:assetid: ff356fcf-0980-4567-8570-4bbcb14381e7
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184658(v=office.15)
ms:contentKeyID: 55119875
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 43bc64dbbed14dae2e185ea89d15b6061858de42
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28703288"
---
# <a name="find-the-appointment-item-associated-with-a-meeting-request"></a>Поиск элемента встречи, связанного с приглашением на собрание

В этом примере показано, как использовать метод [GetAssociatedAppointment(Boolean)](https://msdn.microsoft.com/library/bb652725\(v=office.15\)) для поиска встречи, которая связана с приглашением на собрание.

## <a name="example"></a>Пример

> [!NOTE] 
> Приведенный ниже пример кода представляет собой фрагмент из книги [Программирование приложений для Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).

Объект [MeetingItem](https://msdn.microsoft.com/library/bb645703\(v=office.15\)) представляет не встречу, а сообщение, содержащее запрос на добавление встречи в календарь получателя. В представленном ниже примере кода MeetingRequestExample использует метод [GetAssociatedAppointment(Boolean)](https://msdn.microsoft.com/library/bb652725\(v=office.15\)) объекта **MeetingItem** для каждого объекта **MeetingItem**, полученного из папки "Входящие" пользователя. После этого возвращаемый объект [AppointmentItem](https://msdn.microsoft.com/library/bb645611\(v=office.15\)) используется для записи темы встречи в прослушивателях трассировки коллекции [Listeners](https://msdn.microsoft.com/library/system.diagnostics.debug.listeners.aspx).


> [!NOTE]
> Учтите, что аргументу **GetAssociatedAppointment** присвоено значение **false**, чтобы встреча не добавлялась в календарь пользователя.

Если вы используете Visual Studio для тестирования этого примера кода, сначала добавьте ссылку на компонент Microsoft Outlook 15.0 Object Library и задайте переменную Outlook при импорте пространства имен **Microsoft.Office.Interop.Outlook**. Инструкция **using** не должна идти непосредственно перед функциями в примере кода, но ее нужно добавить перед открытым объявлением Class. В следующей строке кода показано, как выполнить импорт и назначение в C\#.

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```csharp
private void MeetingRequestsExample()
{
    Outlook.Folder folder = Application.Session.
        GetDefaultFolder(Outlook.OlDefaultFolders.olFolderInbox)
        as Outlook.Folder;
    string filter = "[MessageClass] = " +
        "'IPM.Schedule.Meeting.Request'";
    Outlook.Items items = folder.Items.Restrict(filter);
    foreach (Outlook.MeetingItem request in items)
    {
        Outlook.AppointmentItem appt =
            request.GetAssociatedAppointment(false);
        if (appt != null)
        {
            Debug.WriteLine(appt.Subject);
        }
    }
}
```

## <a name="see-also"></a>См. также

- [Приглашения на собрания](meeting-requests.md)


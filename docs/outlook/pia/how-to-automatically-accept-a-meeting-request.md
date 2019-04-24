---
title: Автоматическое принятие приглашения на собрание
TOCTitle: Automatically accept a meeting request
ms:assetid: 3c729bcf-4c85-4efa-af79-2c94d55c2042
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184604(v=office.15)
ms:contentKeyID: 55119874
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: f546b4e2de2a77034fdfeca4d685d7b7f909f40a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359705"
---
# <a name="automatically-accept-a-meeting-request"></a>Автоматическое принятие приглашения на собрание

В этом примере показано, как автоматически принять приглашение на собрание с помощью метода [Respond(OlMeetingResponse, Object, Object)](https://msdn.microsoft.com/library/bb647086\(v=office.15\)).

## <a name="example"></a>Пример

> [!NOTE] 
> Приведенный ниже пример кода представляет собой фрагмент из книги [Программирование приложений для Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).


Объект [MeetingItem](https://msdn.microsoft.com/library/bb645703\(v=office.15\)) представляет запрос на добавление встречи, представленной объектом [AppointmentItem](https://msdn.microsoft.com/library/bb645611\(v=office.15\)), в календарь получателя. Чтобы ответить на приглашение на собрание, используйте метод [GetAssociatedAppointment(Boolean)](https://msdn.microsoft.com/library/bb652725\(v=office.15\)) для получения объекта **AppointmentItem**, связанного с приглашением на собрание. Затем используйте метод [Respond(OlMeetingResponse, Object, Object)](https://msdn.microsoft.com/library/bb647086\(v=office.15\)) объекта **AppointmentItem**, чтобы уведомить организатора собрания, было ли собрание принято, отклонено или предварительно добавлено в календарь получателя. Метод **Respond** принимает три параметра. 

Параметр *Response* указывает, принят, отклонен или добавлен в календарь ответ. Параметры fNoUI и fAdditionalTextDialog являются значениями **bool**, определяющими соответственно, будет ли ответ отправлен и может ли пользователь изменять ответ. В следующем примере кода AutoAcceptMeetingRequests перечисляет все объекты **MeetingItem**, чтобы получить связанный объект **AppointmentItem**. Затем AutoAcceptMeetingRequests использует метод **Respond** с параметром *fNoUI*, равным **true**, чтобы показать, что ответ будет отправлен автоматически, чтобы принять приглашение на собрание.

Если вы используете Visual Studio для тестирования этого примера кода, сначала добавьте ссылку на компонент Microsoft Outlook 15.0 Object Library и задайте переменную Outlook при импорте пространства имен **Microsoft.Office.Interop.Outlook**. Инструкция **using** не должна находиться непосредственно перед функциями в примере кода, но ее нужно добавить перед объявлением общедоступного класса. В приведенной ниже строке кода показано, как выполнить импорт и назначение на языке C\#.

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```csharp
private void AutoAcceptMeetingRequests()
{
    Outlook.MeetingItem mtgResponse;
    Outlook.Folder folder = Application.Session.
        GetDefaultFolder(Outlook.OlDefaultFolders.olFolderInbox)
        as Outlook.Folder;
    string filter = "[MessageClass] = " +
        "'IPM.Schedule.Meeting.Request'";
    Outlook.Items items = folder.Items.Restrict(filter);
    foreach (Outlook.MeetingItem request in items)
    {
        Outlook.AppointmentItem appt =
            request.GetAssociatedAppointment(true);
        if (appt != null)
        {
            mtgResponse = appt.Respond(
                Outlook.OlMeetingResponse.olMeetingAccepted,
                true, Type.Missing);
            mtgResponse.Send();
        }
    }
}
```

## <a name="see-also"></a>См. также

- [Приглашения на собрания](meeting-requests.md)


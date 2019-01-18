---
title: Запрос ответа у пользователя на приглашение на собрание
TOCTitle: Prompt a user to respond to a meeting request
ms:assetid: a0d69f82-8659-457d-9418-1a897a10882f
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184630(v=office.15)
ms:contentKeyID: 55119877
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 26e59cca7431e9f11f3fea5fa058548b9a5903a4
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28722615"
---
# <a name="prompt-a-user-to-respond-to-a-meeting-request"></a>Запрос ответа у пользователя на приглашение на собрание

В этом примере показано, как пригласить пользователя ответить на приглашение на собрание и дать ему возможность отредактировать свой ответ перед отправкой.

## <a name="example"></a>Пример

> [!NOTE] 
> Приведенный ниже пример кода представляет собой фрагмент из книги [Программирование приложений для Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).

Метод [Respond](https://msdn.microsoft.com/library/bb647086\(v=office.15\)) объекта [AppointmentItem](https://msdn.microsoft.com/library/bb645611\(v=office.15\)) используется, чтобы уведомить организатора собрания о том, что приглашение на встречу принято, отклонено или добавлено в качестве эксперимента в календарь получателя. С помощью метода **Respond** можно указать, требуется ли отправить уведомление автоматически, либо разрешить пользователю изменять ответ перед отправкой. Метод **Respond** принимает три параметра. Параметр *Response* указывает, принят, отклонен или добавлен в календарь ответ. Параметры *fNoUI* и *fAdditionalTextDialog* принимают значения **bool**, которые указывают, будет ли ответ отправлен организатору и сможет ли пользователь изменить текст ответа перед отправкой соответственно. 

В следующем примере кода PromptUserMeetingRequest перечисляет объекты [MeetingItem](https://msdn.microsoft.com/library/bb645703\(v=office.15\)), чтобы получить связанные объекты **AppointmentItem**, а затем вызывает метод **Respond**, где параметру *fNoUI* присвоено значение **false**, а параметру *fAdditionalTextDialog*  значение **true**. Это позволяет пользователю выбрать, отправить ли ответ, или отредактировать основной текст ответа перед отправкой.

Если вы используете Visual Studio для тестирования этого примера кода, сначала добавьте ссылку на компонент Microsoft Outlook 15.0 Object Library и задайте переменную Outlook при импорте пространства имен **Microsoft.Office.Interop.Outlook**. Инструкция **using** не должна идти непосредственно перед функциями в примере кода, но ее нужно добавить перед открытым объявлением Class. В следующей строке кода показано, как выполнить импорт и назначение в C\#.

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```csharp
private void PromptUserMeetingRequest()
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
                false, true);
        }
    }
}
```

## <a name="see-also"></a>См. также

- [Приглашения на собрания](meeting-requests.md)


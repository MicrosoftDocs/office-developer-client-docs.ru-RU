---
title: Проверка всех откликов на приглашение на собрание
TOCTitle: Check all responses to a meeting request
ms:assetid: ebe10e5a-7f04-447a-bfc1-aa8a726cb0b3
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184650(v=office.15)
ms:contentKeyID: 55119881
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 89f3aa7037659bb29346bb70338d535cbbc200b3
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28709245"
---
# <a name="check-all-responses-to-a-meeting-request"></a>Проверка всех откликов на приглашение на собрание

В этом примере показано, как проверить состояние отклика каждого получателя на приглашение на собрание.

## <a name="example"></a>Пример

> [!NOTE] 
> Приведенный ниже пример кода взят из книги [Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493) ("Программирование приложений для Microsoft Office Outlook 2007").

В примере кода ниже метод CheckAttendeeStatus выполняет перечисление коллекции [Recipients](https://msdn.microsoft.com/library/bb646361\(v=office.15\)) для объекта [AppointmentItem](https://msdn.microsoft.com/library/bb645611\(v=office.15\)), который представляет приглашение на собрание и проверяет свойство [MeetingResponseStatus](https://msdn.microsoft.com/library/bb645283\(v=office.15\)) каждого объекта [Recipient](https://msdn.microsoft.com/library/bb624370\(v=office.15\)). Каждый объект **Recipient** представляет получателя приглашения на собрание. Свойство **MeetingResponseStatus** может принимать одно из следующих значений перечисления [OlResponseStatus](https://msdn.microsoft.com/library/bb644655\(v=office.15\)) :

- [olResponseAccepted](https://msdn.microsoft.com/library/bb644655\(v=office.15\))
- [olResponseDeclined](https://msdn.microsoft.com/library/bb644655\(v=office.15\))
- [olResponseNone](https://msdn.microsoft.com/library/bb644655\(v=office.15\))
- [olResponseNotResponded](https://msdn.microsoft.com/library/bb644655\(v=office.15\))
- [olResponseOrganized](https://msdn.microsoft.com/library/bb644655\(v=office.15\))
- [olResponseTentative](https://msdn.microsoft.com/library/bb644655\(v=office.15\))

Если для тестирования этого примера кода вы используете Visual Studio, сначала добавьте ссылку на компонент библиотеки объектов Microsoft Outlook 15.0 и укажите переменную Outlook при импорте пространства имен **Microsoft.Office.Interop.Outlook**. Не следует использовать инструкцию **using** непосредственно перед функциями в примере кода, но ее необходимо добавить перед объявлением общедоступного класса. В строке кода ниже показано, как выполнить импорт и назначение на языке C\#.

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```csharp
private void CheckAttendeeStatus()
{
    Outlook.AppointmentItem appt = Application.Session.
        GetDefaultFolder(Outlook.OlDefaultFolders.olFolderCalendar).
        Items.Find("[Subject]='Sales Strategy FY2007'")
        as Outlook.AppointmentItem;
    if (appt != null)
    {
        foreach (Outlook.Recipient recip in appt.Recipients)
        {
            switch (recip.MeetingResponseStatus)
            {
                case Outlook.OlResponseStatus.olResponseAccepted:
                    Debug.WriteLine("Accepted: " + recip.Name);
                    break;
                case Outlook.OlResponseStatus.olResponseTentative:
                    Debug.WriteLine("Tentative: " + recip.Name);
                    break;
                case Outlook.OlResponseStatus.olResponseDeclined:
                    Debug.WriteLine("Declined: " + recip.Name);
                    break;
                case Outlook.OlResponseStatus.olResponseOrganized:
                    Debug.WriteLine("Organizer: " + recip.Name);
                    break;
                case Outlook.OlResponseStatus.olResponseNone:
                    Debug.WriteLine("None: " + recip.Name);
                    break;
                case Outlook.OlResponseStatus.olResponseNotResponded:
                    Debug.WriteLine("Not responded: " + recip.Name);
                    break;
            }
        }
    }
}
```

## <a name="see-also"></a>См. также

- [Приглашения на собрания](meeting-requests.md)


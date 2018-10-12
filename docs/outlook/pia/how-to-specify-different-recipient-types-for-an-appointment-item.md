---
title: Указание получателей разных типов для элемента встречи
TOCTitle: Specify different recipient types for an appointment item
ms:assetid: 83aedc8f-adc0-453d-8e71-1bb9aacc7993
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184622(v=office.15)
ms:contentKeyID: 55119807
ms.date: 07/24/2014
mtps_version: v=office.15
ms.openlocfilehash: c1f9e1d8e7b4c884853dda9b5c37cd7357d48b6c
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25405688"
---
# <a name="specify-different-recipient-types-for-an-appointment-item"></a>Указание получателей разных типов для элемента встречи

В этом примере показано, как с помощью перечисления [OlMeetingRecipientType](https://msdn.microsoft.com/library/bb623431\(v=office.15\)) указать получателей разных типов для элемента встречи.

## <a name="example"></a>Пример

> [!NOTE] 
> Приведенный ниже пример кода взят из книги [Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493) ("Программирование приложений для Microsoft Office Outlook 2007").

Чтобы добавить получателей для объекта [AppointmentItem](https://msdn.microsoft.com/library/bb645611\(v=office.15\)) , являющегося приглашением на собрание, используйте перечисление OlMeetingRecipientType, чтобы определить, является ли получатель сообщения обязательным или необязательным участником либо ресурсом (таким как помещение или оборудование).

В примере кода ниже метод SetRecipientTypeForAppt создает объект **AppointmentItem** и свойства для этого объекта, а также добавляет обязательных и необязательных участников. Кроме того, он добавляет переговорную для собрания. Обратите внимание на то, что свойство [MeetingStatus](https://msdn.microsoft.com/library/bb611417\(v=office.15\)) имеет значение [olMeeting](https://msdn.microsoft.com/library/bb644590\(v=office.15\)), указывающее, что встреча представляет собой приглашение на собрание.

Если для тестирования этого примера кода вы используете Visual Studio, сначала добавьте ссылку на компонент библиотеки объектов Microsoft Outlook 15.0 и укажите переменную Outlook при импорте пространства имен **Microsoft.Office.Interop.Outlook**. Не следует использовать инструкцию **using** непосредственно перед функциями в примере кода, но ее необходимо добавить перед объявлением общедоступного класса. В строке кода ниже показано, как выполнить импорт и назначение на языке C\#.

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```

```csharp
private void SetRecipientTypeForAppt()
{
    Outlook.AppointmentItem appt =
        Application.CreateItem(
        Outlook.OlItemType.olAppointmentItem)
        as Outlook.AppointmentItem;
    appt.Subject = "Customer Review";
    appt.MeetingStatus = Outlook.OlMeetingStatus.olMeeting;
    appt.Location = "36/2021";
    appt.Start = DateTime.Parse("10/20/2006 10:00 AM");
    appt.End = DateTime.Parse("10/20/2006 11:00 AM");
    Outlook.Recipient recipRequired =
        appt.Recipients.Add("Ryan Gregg");
    recipRequired.Type =
        (int)Outlook.OlMeetingRecipientType.olRequired;
    Outlook.Recipient recipOptional =
        appt.Recipients.Add("Peter Allenspach");
    recipOptional.Type =
        (int)Outlook.OlMeetingRecipientType.olOptional;
    Outlook.Recipient recipConf =
        appt.Recipients.Add("Conf Room 36/2021 (14) AV");
    recipConf.Type =
        (int)Outlook.OlMeetingRecipientType.olResource;
    appt.Recipients.ResolveAll();
    appt.Display(false);
}
```

## <a name="see-also"></a>См. также

- [Встречи](appointments.md)


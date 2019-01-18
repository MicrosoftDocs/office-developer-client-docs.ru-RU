---
title: Указание получателей разных типов для элемента встречи
TOCTitle: Specify different recipient types for an appointment item
ms:assetid: 83aedc8f-adc0-453d-8e71-1bb9aacc7993
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184622(v=office.15)
ms:contentKeyID: 55119807
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: beb29c46d590938d1650dac0c862dd5f898333fc
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28709182"
---
# <a name="specify-different-recipient-types-for-an-appointment-item"></a><span data-ttu-id="4f6f6-102">Указание получателей разных типов для элемента встречи</span><span class="sxs-lookup"><span data-stu-id="4f6f6-102">Specify different recipient types for an appointment item</span></span>

<span data-ttu-id="4f6f6-103">В этом примере показано, как с помощью перечисления [OlMeetingRecipientType](https://msdn.microsoft.com/library/bb623431\(v=office.15\)) указать получателей разных типов для элемента встречи.</span><span class="sxs-lookup"><span data-stu-id="4f6f6-103">This example shows how to use the [OlMeetingRecipientType](https://msdn.microsoft.com/library/bb623431\(v=office.15\)) enumeration to specify different recipient types for an appointment item.</span></span>

## <a name="example"></a><span data-ttu-id="4f6f6-104">Пример</span><span class="sxs-lookup"><span data-stu-id="4f6f6-104">Example</span></span>

> [!NOTE] 
> <span data-ttu-id="4f6f6-105">Приведенный ниже пример кода взят из книги [Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493) ("Программирование приложений для Microsoft Office Outlook 2007").</span><span class="sxs-lookup"><span data-stu-id="4f6f6-105">The following code example is an excerpt from [Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).</span></span>

<span data-ttu-id="4f6f6-106">Чтобы добавить получателей для объекта [AppointmentItem](https://msdn.microsoft.com/library/bb645611\(v=office.15\)) , являющегося приглашением на собрание, используйте перечисление OlMeetingRecipientType, чтобы определить, является ли получатель сообщения обязательным или необязательным участником либо ресурсом (таким как помещение или оборудование).</span><span class="sxs-lookup"><span data-stu-id="4f6f6-106">To add recipients to an [AppointmentItem](https://msdn.microsoft.com/library/bb645611\(v=office.15\)) object that represents a meeting request, use the OlMeetingRecipientType enumeration to specify whether the recipient of the message is a required or optional attendee, or a resource (such as a room or equipment).</span></span>

<span data-ttu-id="4f6f6-107">В примере кода ниже метод SetRecipientTypeForAppt создает объект **AppointmentItem** и свойства для этого объекта, а также добавляет обязательных и необязательных участников.</span><span class="sxs-lookup"><span data-stu-id="4f6f6-107">In the following code example, SetRecipientTypeForAppt creates an **AppointmentItem** object, sets properties for that object, and adds required and optional attendees.</span></span> <span data-ttu-id="4f6f6-108">Кроме того, он добавляет переговорную для собрания.</span><span class="sxs-lookup"><span data-stu-id="4f6f6-108">It also adds a conference room for the meeting.</span></span> <span data-ttu-id="4f6f6-109">Обратите внимание на то, что свойство [MeetingStatus](https://msdn.microsoft.com/library/bb611417\(v=office.15\)) имеет значение [olMeeting](https://msdn.microsoft.com/library/bb644590\(v=office.15\)), указывающее, что встреча представляет собой приглашение на собрание.</span><span class="sxs-lookup"><span data-stu-id="4f6f6-109">Note that the [MeetingStatus](https://msdn.microsoft.com/library/bb611417\(v=office.15\)) property is set to [olMeeting](https://msdn.microsoft.com/library/bb644590\(v=office.15\)), indicating that the appointment is a meeting request.</span></span>

<span data-ttu-id="4f6f6-110">Если для тестирования этого примера кода вы используете Visual Studio, сначала добавьте ссылку на компонент библиотеки объектов Microsoft Outlook 15.0 и укажите переменную Outlook при импорте пространства имен **Microsoft.Office.Interop.Outlook**.</span><span class="sxs-lookup"><span data-stu-id="4f6f6-110">If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the Outlook variable when you import the **Microsoft.Office.Interop.Outlook** namespace.</span></span> <span data-ttu-id="4f6f6-111">Не следует использовать инструкцию **using** непосредственно перед функциями в примере кода, но ее необходимо добавить перед объявлением общедоступного класса.</span><span class="sxs-lookup"><span data-stu-id="4f6f6-111">The **using** statement must not occur directly before the functions in the code example but must be added before the public Class declaration.</span></span> <span data-ttu-id="4f6f6-112">В строке кода ниже показано, как выполнить импорт и назначение на языке C\#.</span><span class="sxs-lookup"><span data-stu-id="4f6f6-112">The following line of code shows how to do the import and assignment in C\#.</span></span>

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

## <a name="see-also"></a><span data-ttu-id="4f6f6-113">См. также</span><span class="sxs-lookup"><span data-stu-id="4f6f6-113">See also</span></span>

- [<span data-ttu-id="4f6f6-114">Встречи</span><span class="sxs-lookup"><span data-stu-id="4f6f6-114">Appointments</span></span>](appointments.md)


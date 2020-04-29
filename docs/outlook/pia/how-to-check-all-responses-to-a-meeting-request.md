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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359719"
---
# <a name="check-all-responses-to-a-meeting-request"></a><span data-ttu-id="a3f0e-102">Проверка всех откликов на приглашение на собрание</span><span class="sxs-lookup"><span data-stu-id="a3f0e-102">Check all responses to a meeting request</span></span>

<span data-ttu-id="a3f0e-103">В этом примере показано, как проверить состояние отклика каждого получателя на приглашение на собрание.</span><span class="sxs-lookup"><span data-stu-id="a3f0e-103">This example shows how to check the status of each recipient’s response to a meeting request.</span></span>

## <a name="example"></a><span data-ttu-id="a3f0e-104">Пример</span><span class="sxs-lookup"><span data-stu-id="a3f0e-104">Example</span></span>

> [!NOTE] 
> <span data-ttu-id="a3f0e-105">Приведенный ниже пример кода взят из книги [Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493) ("Программирование приложений для Microsoft Office Outlook 2007").</span><span class="sxs-lookup"><span data-stu-id="a3f0e-105">The following code example is an excerpt from [Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).</span></span>

<span data-ttu-id="a3f0e-106">В примере кода ниже метод CheckAttendeeStatus выполняет перечисление коллекции [Recipients](https://msdn.microsoft.com/library/bb646361\(v=office.15\)) для объекта [AppointmentItem](https://msdn.microsoft.com/library/bb645611\(v=office.15\)), который представляет приглашение на собрание и проверяет свойство [MeetingResponseStatus](https://msdn.microsoft.com/library/bb645283\(v=office.15\)) каждого объекта [Recipient](https://msdn.microsoft.com/library/bb624370\(v=office.15\)).</span><span class="sxs-lookup"><span data-stu-id="a3f0e-106">In the following code example, CheckAttendeeStatus enumerates the [Recipients](https://msdn.microsoft.com/library/bb646361\(v=office.15\)) collection for the [AppointmentItem](https://msdn.microsoft.com/library/bb645611\(v=office.15\)) object that represents a meeting request and examines the [MeetingResponseStatus](https://msdn.microsoft.com/library/bb645283\(v=office.15\)) property of each [Recipient](https://msdn.microsoft.com/library/bb624370\(v=office.15\)) object.</span></span> <span data-ttu-id="a3f0e-107">Каждый объект **Recipient** представляет получателя приглашения на собрание.</span><span class="sxs-lookup"><span data-stu-id="a3f0e-107">Each **Recipient** object represents a recipient of the meeting request.</span></span> <span data-ttu-id="a3f0e-108">Свойство **MeetingResponseStatus** может принимать одно из следующих значений перечисления [OlResponseStatus](https://msdn.microsoft.com/library/bb644655\(v=office.15\)) :</span><span class="sxs-lookup"><span data-stu-id="a3f0e-108">The value of the **MeetingResponseStatus** property can be one of the following [OlResponseStatus](https://msdn.microsoft.com/library/bb644655\(v=office.15\)) enumeration values:</span></span>

- <span data-ttu-id="a3f0e-109">[olResponseAccepted](https://msdn.microsoft.com/library/bb644655\(v=office.15\))</span><span class="sxs-lookup"><span data-stu-id="a3f0e-109">[olResponseAccepted](https://msdn.microsoft.com/library/bb644655\(v=office.15\))</span></span>
- <span data-ttu-id="a3f0e-110">[olResponseDeclined](https://msdn.microsoft.com/library/bb644655\(v=office.15\))</span><span class="sxs-lookup"><span data-stu-id="a3f0e-110">[olResponseDeclined](https://msdn.microsoft.com/library/bb644655\(v=office.15\))</span></span>
- <span data-ttu-id="a3f0e-111">[olResponseNone](https://msdn.microsoft.com/library/bb644655\(v=office.15\))</span><span class="sxs-lookup"><span data-stu-id="a3f0e-111">[olResponseNone](https://msdn.microsoft.com/library/bb644655\(v=office.15\))</span></span>
- <span data-ttu-id="a3f0e-112">[olResponseNotResponded](https://msdn.microsoft.com/library/bb644655\(v=office.15\))</span><span class="sxs-lookup"><span data-stu-id="a3f0e-112">[olResponseNotResponded](https://msdn.microsoft.com/library/bb644655\(v=office.15\))</span></span>
- <span data-ttu-id="a3f0e-113">[olResponseOrganized](https://msdn.microsoft.com/library/bb644655\(v=office.15\))</span><span class="sxs-lookup"><span data-stu-id="a3f0e-113">[olResponseOrganized](https://msdn.microsoft.com/library/bb644655\(v=office.15\))</span></span>
- <span data-ttu-id="a3f0e-114">[olResponseTentative](https://msdn.microsoft.com/library/bb644655\(v=office.15\))</span><span class="sxs-lookup"><span data-stu-id="a3f0e-114">[olResponseTentative](https://msdn.microsoft.com/library/bb644655\(v=office.15\))</span></span>

<span data-ttu-id="a3f0e-115">Если вы используете Visual Studio для тестирования этого примера кода, сначала добавьте ссылку на компонент Microsoft Outlook 15.0 Object Library и задайте переменную Outlook при импорте пространства имен **Microsoft.Office.Interop.Outlook**.</span><span class="sxs-lookup"><span data-stu-id="a3f0e-115">If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the Outlook variable when you import the **Microsoft.Office.Interop.Outlook** namespace.</span></span> <span data-ttu-id="a3f0e-116">Инструкция **using** не должна находиться непосредственно перед функциями в примере кода, но ее нужно добавить перед объявлением общедоступного класса.</span><span class="sxs-lookup"><span data-stu-id="a3f0e-116">The **using** statement must not occur directly before the functions in the code example but must be added before the public Class declaration.</span></span> <span data-ttu-id="a3f0e-117">В приведенной ниже строке кода показано, как выполнить импорт и назначение на языке C\#.</span><span class="sxs-lookup"><span data-stu-id="a3f0e-117">The following line of code shows how to do the import and assignment in C\#.</span></span>

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

## <a name="see-also"></a><span data-ttu-id="a3f0e-118">См. также</span><span class="sxs-lookup"><span data-stu-id="a3f0e-118">See also</span></span>

- [<span data-ttu-id="a3f0e-119">Приглашения на собрания</span><span class="sxs-lookup"><span data-stu-id="a3f0e-119">Meeting requests</span></span>](meeting-requests.md)


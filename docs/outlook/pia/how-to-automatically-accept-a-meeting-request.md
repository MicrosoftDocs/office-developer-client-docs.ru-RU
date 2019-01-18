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
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28700334"
---
# <a name="automatically-accept-a-meeting-request"></a><span data-ttu-id="5a4d5-102">Автоматическое принятие приглашения на собрание</span><span class="sxs-lookup"><span data-stu-id="5a4d5-102">Automatically accept a meeting request</span></span>

<span data-ttu-id="5a4d5-103">В этом примере показано, как автоматически принять приглашение на собрание с помощью метода [Respond(OlMeetingResponse, Object, Object)](https://msdn.microsoft.com/library/bb647086\(v=office.15\)).</span><span class="sxs-lookup"><span data-stu-id="5a4d5-103">This example shows how to use the [Respond(OlMeetingResponse, Object, Object)](https://msdn.microsoft.com/library/bb647086\(v=office.15\)) method to automatically accept a meeting request.</span></span>

## <a name="example"></a><span data-ttu-id="5a4d5-104">Пример</span><span class="sxs-lookup"><span data-stu-id="5a4d5-104">Example</span></span>

> [!NOTE] 
> <span data-ttu-id="5a4d5-105">Приведенный ниже пример кода представляет собой фрагмент из книги [Программирование приложений для Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).</span><span class="sxs-lookup"><span data-stu-id="5a4d5-105">The following code example is an excerpt from [Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).</span></span>


<span data-ttu-id="5a4d5-106">Объект [MeetingItem](https://msdn.microsoft.com/library/bb645703\(v=office.15\)) представляет запрос на добавление встречи, представленной объектом [AppointmentItem](https://msdn.microsoft.com/library/bb645611\(v=office.15\)), в календарь получателя.</span><span class="sxs-lookup"><span data-stu-id="5a4d5-106">A [MeetingItem](https://msdn.microsoft.com/library/bb645703\(v=office.15\)) object represents a request to add an appointment, represented by an [AppointmentItem](https://msdn.microsoft.com/library/bb645611\(v=office.15\)) object, to a recipient’s calendar.</span></span> <span data-ttu-id="5a4d5-107">Чтобы ответить на приглашение на собрание, используйте метод [GetAssociatedAppointment(Boolean)](https://msdn.microsoft.com/library/bb652725\(v=office.15\)) для получения объекта **AppointmentItem**, связанного с приглашением на собрание.</span><span class="sxs-lookup"><span data-stu-id="5a4d5-107">To respond to a meeting request, use the [GetAssociatedAppointment(Boolean)](https://msdn.microsoft.com/library/bb652725\(v=office.15\)) method to obtain the **AppointmentItem** associated with the meeting request.</span></span> <span data-ttu-id="5a4d5-108">Затем используйте метод [Respond(OlMeetingResponse, Object, Object)](https://msdn.microsoft.com/library/bb647086\(v=office.15\)) объекта **AppointmentItem**, чтобы уведомить организатора собрания, было ли собрание принято, отклонено или предварительно добавлено в календарь получателя.</span><span class="sxs-lookup"><span data-stu-id="5a4d5-108">Then use the [Respond(OlMeetingResponse, Object, Object)](https://msdn.microsoft.com/library/bb647086\(v=office.15\)) method of the **AppointmentItem** to notify the meeting organizer whether the meeting has been accepted, declined, or tentatively added to the recipient’s calendar.</span></span> <span data-ttu-id="5a4d5-109">Метод **Respond** принимает три параметра.</span><span class="sxs-lookup"><span data-stu-id="5a4d5-109">The **Respond** method accepts three parameters.</span></span> 

<span data-ttu-id="5a4d5-110">Параметр *Response* указывает, принят, отклонен или добавлен в календарь ответ.</span><span class="sxs-lookup"><span data-stu-id="5a4d5-110">The *Response* parameter indicates whether the response is accept, decline, or tentative.</span></span> <span data-ttu-id="5a4d5-111">Параметры fNoUI и fAdditionalTextDialog являются значениями **bool**, определяющими соответственно, будет ли ответ отправлен и может ли пользователь изменять ответ.</span><span class="sxs-lookup"><span data-stu-id="5a4d5-111">The fNoUI and fAdditionalTextDialog parameters are **bool** values that determine whether a response will be sent, and whether the user may or may not edit the response, respectively.</span></span> <span data-ttu-id="5a4d5-112">В следующем примере кода AutoAcceptMeetingRequests перечисляет все объекты **MeetingItem**, чтобы получить связанный объект **AppointmentItem**.</span><span class="sxs-lookup"><span data-stu-id="5a4d5-112">In the following code example, AutoAcceptMeetingRequests enumerates through every **MeetingItem** object to get the associated **AppointmentItem**.</span></span> <span data-ttu-id="5a4d5-113">Затем AutoAcceptMeetingRequests использует метод **Respond** с параметром *fNoUI*, равным **true**, чтобы показать, что ответ будет отправлен автоматически, чтобы принять приглашение на собрание.</span><span class="sxs-lookup"><span data-stu-id="5a4d5-113">AutoAcceptMeetingRequests then uses the **Respond** method with the *fNoUI* parameter set to **true** to indicate that a response will be sent automatically to accept the meeting request.</span></span>

<span data-ttu-id="5a4d5-114">Если вы используете Visual Studio для тестирования этого примера кода, сначала добавьте ссылку на компонент Microsoft Outlook 15.0 Object Library и задайте переменную Outlook при импорте пространства имен **Microsoft.Office.Interop.Outlook**.</span><span class="sxs-lookup"><span data-stu-id="5a4d5-114">If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the Outlook variable when you import the **Microsoft.Office.Interop.Outlook** namespace.</span></span> <span data-ttu-id="5a4d5-115">Инструкция **using** не должна идти непосредственно перед функциями в примере кода, но ее нужно добавить перед открытым объявлением Class.</span><span class="sxs-lookup"><span data-stu-id="5a4d5-115">The **using** statement must not occur directly before the functions in the code example but must be added before the public Class declaration.</span></span> <span data-ttu-id="5a4d5-116">В следующей строке кода показано, как выполнить импорт и назначение в C\#.</span><span class="sxs-lookup"><span data-stu-id="5a4d5-116">The following line of code shows how to do the import and assignment in C\#.</span></span>

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

## <a name="see-also"></a><span data-ttu-id="5a4d5-117">См. также</span><span class="sxs-lookup"><span data-stu-id="5a4d5-117">See also</span></span>

- [<span data-ttu-id="5a4d5-118">Приглашения на собрания</span><span class="sxs-lookup"><span data-stu-id="5a4d5-118">Meeting requests</span></span>](meeting-requests.md)


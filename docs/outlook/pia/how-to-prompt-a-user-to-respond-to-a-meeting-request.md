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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32320050"
---
# <a name="prompt-a-user-to-respond-to-a-meeting-request"></a><span data-ttu-id="15455-102">Запрос ответа у пользователя на приглашение на собрание</span><span class="sxs-lookup"><span data-stu-id="15455-102">Prompt a user to respond to a meeting request</span></span>

<span data-ttu-id="15455-103">В этом примере показано, как пригласить пользователя ответить на приглашение на собрание и дать ему возможность отредактировать свой ответ перед отправкой.</span><span class="sxs-lookup"><span data-stu-id="15455-103">This example shows how to prompt the user for a response to a meeting request, and to enable the user to edit the response before sending it.</span></span>

## <a name="example"></a><span data-ttu-id="15455-104">Пример</span><span class="sxs-lookup"><span data-stu-id="15455-104">Example</span></span>

> [!NOTE] 
> <span data-ttu-id="15455-105">Приведенный ниже пример кода представляет собой фрагмент из книги [Программирование приложений для Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).</span><span class="sxs-lookup"><span data-stu-id="15455-105">The following code example is an excerpt from [Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).</span></span>

<span data-ttu-id="15455-106">Метод [Respond](https://msdn.microsoft.com/library/bb647086\(v=office.15\)) объекта [AppointmentItem](https://msdn.microsoft.com/library/bb645611\(v=office.15\)) используется, чтобы уведомить организатора собрания о том, что приглашение на встречу принято, отклонено или добавлено в качестве эксперимента в календарь получателя.</span><span class="sxs-lookup"><span data-stu-id="15455-106">The [Respond](https://msdn.microsoft.com/library/bb647086\(v=office.15\)) method of the [AppointmentItem](https://msdn.microsoft.com/library/bb645611\(v=office.15\)) object is used to notify the meeting organizer whether the meeting has been accepted, declined, or tentatively added to the recipient’s calendar.</span></span> <span data-ttu-id="15455-107">С помощью метода **Respond** можно указать, требуется ли отправить уведомление автоматически, либо разрешить пользователю изменять ответ перед отправкой.</span><span class="sxs-lookup"><span data-stu-id="15455-107">By using the **Respond** method, you can indicate whether you want to send the notification automatically, or whether you want to allow the user to edit the response before sending it.</span></span> <span data-ttu-id="15455-108">Метод **Respond** принимает три параметра.</span><span class="sxs-lookup"><span data-stu-id="15455-108">The **Respond** method accepts three parameters.</span></span> <span data-ttu-id="15455-109">Параметр *Response* указывает, принят, отклонен или добавлен в календарь ответ.</span><span class="sxs-lookup"><span data-stu-id="15455-109">The *Response* parameter indicates whether the response is accept, decline, or tentative.</span></span> <span data-ttu-id="15455-110">Параметры *fNoUI* и *fAdditionalTextDialog* принимают значения **bool**, которые указывают, будет ли ответ отправлен организатору и сможет ли пользователь изменить текст ответа перед отправкой соответственно.</span><span class="sxs-lookup"><span data-stu-id="15455-110">The *fNoUI* and *fAdditionalTextDialog* parameters are **bool** values that indicate whether the response will be sent to the organizer, and whether the user can edit the body of the response before sending it, respectively.</span></span> 

<span data-ttu-id="15455-111">В следующем примере кода PromptUserMeetingRequest перечисляет объекты [MeetingItem](https://msdn.microsoft.com/library/bb645703\(v=office.15\)), чтобы получить связанные объекты **AppointmentItem**, а затем вызывает метод **Respond**, где параметру *fNoUI* присвоено значение **false**, а параметру *fAdditionalTextDialog*  значение **true**.</span><span class="sxs-lookup"><span data-stu-id="15455-111">In the following code example, PromptUserMeetingRequest enumerates through the [MeetingItem](https://msdn.microsoft.com/library/bb645703\(v=office.15\)) objects to get the associated **AppointmentItem** objects, and then calls the **Respond** method with the *fNoUI* parameter set to **false** and the *fAdditionalTextDialog* parameter set to **true**.</span></span> <span data-ttu-id="15455-112">Это позволяет пользователю выбрать, отправить ли ответ, или отредактировать основной текст ответа перед отправкой.</span><span class="sxs-lookup"><span data-stu-id="15455-112">This allows the user to choose whether to send a response, and whether to edit the body of the response before sending it.</span></span>

<span data-ttu-id="15455-113">Если вы используете Visual Studio для тестирования этого примера кода, сначала добавьте ссылку на компонент Microsoft Outlook 15.0 Object Library и задайте переменную Outlook при импорте пространства имен **Microsoft.Office.Interop.Outlook**.</span><span class="sxs-lookup"><span data-stu-id="15455-113">If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the Outlook variable when you import the **Microsoft.Office.Interop.Outlook** namespace.</span></span> <span data-ttu-id="15455-114">Инструкция **using** не должна находиться непосредственно перед функциями в примере кода, но ее нужно добавить перед объявлением общедоступного класса.</span><span class="sxs-lookup"><span data-stu-id="15455-114">The **using** statement must not occur directly before the functions in the code example but must be added before the public Class declaration.</span></span> <span data-ttu-id="15455-115">В приведенной ниже строке кода показано, как выполнить импорт и назначение на языке C\#.</span><span class="sxs-lookup"><span data-stu-id="15455-115">The following line of code shows how to do the import and assignment in C\#.</span></span>

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

## <a name="see-also"></a><span data-ttu-id="15455-116">См. также</span><span class="sxs-lookup"><span data-stu-id="15455-116">See also</span></span>

- [<span data-ttu-id="15455-117">Приглашения на собрания</span><span class="sxs-lookup"><span data-stu-id="15455-117">Meeting requests</span></span>](meeting-requests.md)


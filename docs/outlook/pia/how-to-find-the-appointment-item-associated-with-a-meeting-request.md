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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32320302"
---
# <a name="find-the-appointment-item-associated-with-a-meeting-request"></a><span data-ttu-id="77437-102">Поиск элемента встречи, связанного с приглашением на собрание</span><span class="sxs-lookup"><span data-stu-id="77437-102">Find the appointment item associated with a meeting request</span></span>

<span data-ttu-id="77437-103">В этом примере показано, как использовать метод [GetAssociatedAppointment(Boolean)](https://msdn.microsoft.com/library/bb652725\(v=office.15\)) для поиска встречи, которая связана с приглашением на собрание.</span><span class="sxs-lookup"><span data-stu-id="77437-103">This example shows how to use the [GetAssociatedAppointment(Boolean)](https://msdn.microsoft.com/library/bb652725\(v=office.15\)) method to find the appointment that is associated with a meeting request.</span></span>

## <a name="example"></a><span data-ttu-id="77437-104">Пример</span><span class="sxs-lookup"><span data-stu-id="77437-104">Example</span></span>

> [!NOTE] 
> <span data-ttu-id="77437-105">Приведенный ниже пример кода представляет собой фрагмент из книги [Программирование приложений для Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).</span><span class="sxs-lookup"><span data-stu-id="77437-105">The following code example is an excerpt from [Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).</span></span>

<span data-ttu-id="77437-106">Объект [MeetingItem](https://msdn.microsoft.com/library/bb645703\(v=office.15\)) представляет не встречу, а сообщение, содержащее запрос на добавление встречи в календарь получателя.</span><span class="sxs-lookup"><span data-stu-id="77437-106">A [MeetingItem](https://msdn.microsoft.com/library/bb645703\(v=office.15\)) object does not represent an appointment, but a message that contains a request to add an appointment to the recipient’s calendar.</span></span> <span data-ttu-id="77437-107">В представленном ниже примере кода MeetingRequestExample использует метод [GetAssociatedAppointment(Boolean)](https://msdn.microsoft.com/library/bb652725\(v=office.15\)) объекта **MeetingItem** для каждого объекта **MeetingItem**, полученного из папки "Входящие" пользователя.</span><span class="sxs-lookup"><span data-stu-id="77437-107">In the following code example, MeetingRequestExample uses the [GetAssociatedAppointment(Boolean)](https://msdn.microsoft.com/library/bb652725\(v=office.15\)) method of the **MeetingItem** object on each **MeetingItem** retrieved from the user’s Inbox.</span></span> <span data-ttu-id="77437-108">После этого возвращаемый объект [AppointmentItem](https://msdn.microsoft.com/library/bb645611\(v=office.15\)) используется для записи темы встречи в прослушивателях трассировки коллекции [Listeners](https://msdn.microsoft.com/library/system.diagnostics.debug.listeners.aspx).</span><span class="sxs-lookup"><span data-stu-id="77437-108">The returned [AppointmentItem](https://msdn.microsoft.com/library/bb645611\(v=office.15\)) object is then used to write the subject of the appointment to the trace listeners of the [Listeners](https://msdn.microsoft.com/library/system.diagnostics.debug.listeners.aspx) collection.</span></span>


> [!NOTE]
> <span data-ttu-id="77437-109">Учтите, что аргументу **GetAssociatedAppointment** присвоено значение **false**, чтобы встреча не добавлялась в календарь пользователя.</span><span class="sxs-lookup"><span data-stu-id="77437-109">Note that **GetAssociatedAppointment** argument is set to **false** so that the appointment is not added to the user’s calendar.</span></span>

<span data-ttu-id="77437-110">Если вы используете Visual Studio для тестирования этого примера кода, сначала добавьте ссылку на компонент Microsoft Outlook 15.0 Object Library и задайте переменную Outlook при импорте пространства имен **Microsoft.Office.Interop.Outlook**.</span><span class="sxs-lookup"><span data-stu-id="77437-110">If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the Outlook variable when you import the **Microsoft.Office.Interop.Outlook** namespace.</span></span> <span data-ttu-id="77437-111">Инструкция **using** не должна находиться непосредственно перед функциями в примере кода, но ее нужно добавить перед объявлением общедоступного класса.</span><span class="sxs-lookup"><span data-stu-id="77437-111">The **using** statement must not occur directly before the functions in the code example but must be added before the public Class declaration.</span></span> <span data-ttu-id="77437-112">В приведенной ниже строке кода показано, как выполнить импорт и назначение на языке C\#.</span><span class="sxs-lookup"><span data-stu-id="77437-112">The following line of code shows how to do the import and assignment in C\#.</span></span>

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

## <a name="see-also"></a><span data-ttu-id="77437-113">См. также</span><span class="sxs-lookup"><span data-stu-id="77437-113">See also</span></span>

- [<span data-ttu-id="77437-114">Приглашения на собрания</span><span class="sxs-lookup"><span data-stu-id="77437-114">Meeting requests</span></span>](meeting-requests.md)


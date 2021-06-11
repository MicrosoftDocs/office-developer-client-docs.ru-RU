---
title: Получение организатора собрания
TOCTitle: Get the organizer of a meeting
ms:assetid: 6a33db84-573b-4d1b-a91a-903f30630ec9
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184615(v=office.15)
ms:contentKeyID: 55119872
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: e19b293b581984e9dbb1fe27c9564cb78a73caa1
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/29/2019
ms.locfileid: "34542538"
---
# <a name="get-the-organizer-of-a-meeting"></a><span data-ttu-id="41786-102">Получение организатора собрания</span><span class="sxs-lookup"><span data-stu-id="41786-102">Get the organizer of a meeting</span></span>

<span data-ttu-id="41786-103">В этом примере показано, как программным способом вернуть организатора собрания.</span><span class="sxs-lookup"><span data-stu-id="41786-103">This example shows how to programmatically return the organizer of a meeting.</span></span>

## <a name="example"></a><span data-ttu-id="41786-104">Пример</span><span class="sxs-lookup"><span data-stu-id="41786-104">Example</span></span>

> [!NOTE] 
> <span data-ttu-id="41786-105">Приведенный ниже пример кода представляет собой фрагмент из книги [Программирование приложений для Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).</span><span class="sxs-lookup"><span data-stu-id="41786-105">The following code example is an excerpt from [Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).</span></span>

<span data-ttu-id="41786-106">В следующем примере кода метод GetMeetingOrganizer принимает параметр типа [AppointmentItem](https://msdn.microsoft.com/library/bb645611\(v=office.15\)), который представляет собрание, и использует объект [PropertyAccessor](https://msdn.microsoft.com/library/bb646034\(v=office.15\)) и метод [GetProperty(String)](https://msdn.microsoft.com/library/bb645726\(v=office.15\)) для получения элемента [EntryID](https://msdn.microsoft.com/library/bb645980\(v=office.15\)) для объекта **AppointmentItem**.</span><span class="sxs-lookup"><span data-stu-id="41786-106">In the following code example, GetMeetingOrganizer takes a parameter of type [AppointmentItem](https://msdn.microsoft.com/library/bb645611\(v=office.15\)) that represents a meeting, and uses the [PropertyAccessor](https://msdn.microsoft.com/library/bb646034\(v=office.15\)) object and the [GetProperty(String)](https://msdn.microsoft.com/library/bb645726\(v=office.15\)) method to obtain the [EntryID](https://msdn.microsoft.com/library/bb645980\(v=office.15\)) for the **AppointmentItem** object.</span></span> <span data-ttu-id="41786-107">После получения элемента **EntryID** в примере используется метод [GetAddressEntryFromID(String)](https://msdn.microsoft.com/library/ff185034\(v=office.15\)), чтобы вернуть объект [AddressEntry](https://msdn.microsoft.com/library/bb609728\(v=office.15\)), представляющий организатора собрания.</span><span class="sxs-lookup"><span data-stu-id="41786-107">Once the **EntryID** is obtained, the example uses the [GetAddressEntryFromID(String)](https://msdn.microsoft.com/library/ff185034\(v=office.15\)) method to return the [AddressEntry](https://msdn.microsoft.com/library/bb609728\(v=office.15\)) object that represents the organizer of the meeting.</span></span>

<span data-ttu-id="41786-108">Если вы используете Visual Studio для тестирования этого примера кода, сначала добавьте ссылку на компонент Microsoft Outlook 15.0 Object Library и задайте переменную Outlook при импорте пространства имен **Microsoft.Office.Interop.Outlook**.</span><span class="sxs-lookup"><span data-stu-id="41786-108">If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the Outlook variable when you import the **Microsoft.Office.Interop.Outlook** namespace.</span></span> <span data-ttu-id="41786-109">Инструкция **using** не должна находиться непосредственно перед функциями в примере кода, но ее нужно добавить перед объявлением общедоступного класса.</span><span class="sxs-lookup"><span data-stu-id="41786-109">The **using** statement must not occur directly before the functions in the code example but must be added before the public Class declaration.</span></span> <span data-ttu-id="41786-110">В приведенной ниже строке кода показано, как выполнить импорт и назначение на языке C\#.</span><span class="sxs-lookup"><span data-stu-id="41786-110">The following line of code shows how to do the import and assignment in C\#.</span></span>

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```csharp
private Outlook.AddressEntry GetMeetingOrganizer(Outlook.AppointmentItem appt)
{
    if (appt == null)
    {
        throw new ArgumentNullException();
    }
    string PR_SENT_REPRESENTING_ENTRYID =
        @"http://schemas.microsoft.com/mapi/proptag/0x00410102";
    string organizerEntryID =
        appt.PropertyAccessor.BinaryToString(
            appt.PropertyAccessor.GetProperty(
            PR_SENT_REPRESENTING_ENTRYID));
    Outlook.AddressEntry organizer =
        Application.Session.
        GetAddressEntryFromID(organizerEntryID);
    if (organizer != null)
    {
        return organizer; 
    }
    else
    {
        return null;
    }
}
```

## <a name="see-also"></a><span data-ttu-id="41786-111">См. также</span><span class="sxs-lookup"><span data-stu-id="41786-111">See also</span></span>

- [<span data-ttu-id="41786-112">Приглашения на собрания</span><span class="sxs-lookup"><span data-stu-id="41786-112">Meeting requests</span></span>](meeting-requests.md)


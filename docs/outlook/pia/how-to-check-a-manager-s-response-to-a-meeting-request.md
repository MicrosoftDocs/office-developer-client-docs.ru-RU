---
title: Проверка ответа руководителя на приглашение на собрание
TOCTitle: Check a manager's response to a meeting request
ms:assetid: 7bdb2163-17e3-47b4-95e5-e051b90506c6
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184618(v=office.15)
ms:contentKeyID: 55119847
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: ba54ba740182eaffc92a0e1932a6fbed1d3804c8
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359712"
---
# <a name="check-a-managers-response-to-a-meeting-request"></a><span data-ttu-id="51415-102">Проверка ответа руководителя на приглашение на собрание</span><span class="sxs-lookup"><span data-stu-id="51415-102">Check a manager's response to a meeting request</span></span>

<span data-ttu-id="51415-103">В этом примере показано использование методов [GetExchangeUser()](https://msdn.microsoft.com/library/bb611808\(v=office.15\)) и [GetExchangeUserManager()](https://msdn.microsoft.com/library/bb646656\(v=office.15\)) для проверки состояния ответа руководителя текущего пользователя на приглашение на собрание.</span><span class="sxs-lookup"><span data-stu-id="51415-103">This example illustrates how to use the [GetExchangeUser()](https://msdn.microsoft.com/library/bb611808\(v=office.15\)) and [GetExchangeUserManager()](https://msdn.microsoft.com/library/bb646656\(v=office.15\)) methods to check the status of the response of the current user's manager to a meeting request.</span></span>

## <a name="example"></a><span data-ttu-id="51415-104">Пример</span><span class="sxs-lookup"><span data-stu-id="51415-104">Example</span></span>

> [!NOTE] 
> <span data-ttu-id="51415-105">Приведенный ниже пример кода представляет собой фрагмент из книги [Программирование приложений для Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).</span><span class="sxs-lookup"><span data-stu-id="51415-105">The following code example is an excerpt from [Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).</span></span>

<span data-ttu-id="51415-106">Чтобы определить, принято или отклонено приглашение на собрание соответствующим получателем, используйте свойство [MeetingResponseStatus](https://msdn.microsoft.com/library/bb645283\(v=office.15\)) объекта [Recipient](https://msdn.microsoft.com/library/bb624370\(v=office.15\)) из коллекции [Recipients](https://msdn.microsoft.com/library/bb646361\(v=office.15\)), связанной с объектом [AppointmentItem](https://msdn.microsoft.com/library/bb645611\(v=office.15\)) .</span><span class="sxs-lookup"><span data-stu-id="51415-106">To determine whether a given recipient has accepted or declined a requested meeting, use the [MeetingResponseStatus](https://msdn.microsoft.com/library/bb645283\(v=office.15\)) property of the [Recipient](https://msdn.microsoft.com/library/bb624370\(v=office.15\)) object from the [Recipients](https://msdn.microsoft.com/library/bb646361\(v=office.15\)) collection associated with the [AppointmentItem](https://msdn.microsoft.com/library/bb645611\(v=office.15\)) object.</span></span>

<span data-ttu-id="51415-107">В следующем примере кода метод CheckManagerResponseStatus принимает в качестве параметра объект **AppointmentItem**.</span><span class="sxs-lookup"><span data-stu-id="51415-107">In the following code example, CheckManagerResponseStatus takes in an **AppointmentItem** object as a parameter.</span></span> <span data-ttu-id="51415-108">Метод CheckManagerResponseStatus получает объект [ExchangeUser](https://msdn.microsoft.com/library/bb609574\(v=office.15\)) путем вызова метода **GetExchangeUser** для текущего пользователя.</span><span class="sxs-lookup"><span data-stu-id="51415-108">CheckManagerResponseStatus gets the [ExchangeUser](https://msdn.microsoft.com/library/bb609574\(v=office.15\)) object by calling the **GetExchangeUser** method on the current user.</span></span> <span data-ttu-id="51415-109">После этого метод CheckManagerResponseStatus получает объект **ExchangeUser**, связанный с руководителем текущего пользователя, посредством вызова метода **GetExchangeUserManager**.</span><span class="sxs-lookup"><span data-stu-id="51415-109">CheckManagerResponseStatus then gets the **ExchangeUser** object that is associated with the current user’s manager by calling the **GetExchangeUserManager** method.</span></span> <span data-ttu-id="51415-110">С помощью метода [CompareEntryIDs(String, String)](https://msdn.microsoft.com/library/bb646919\(v=office.15\)) объекта [NameSpace](https://msdn.microsoft.com/library/bb645857\(v=office.15\)) в этом примере проверяется, соответствует ли объект **Recipient**, связанный с объектом **AppointmentItem**, объекту **ExchangeUser**, который представляет руководителя пользователя.</span><span class="sxs-lookup"><span data-stu-id="51415-110">By using the [CompareEntryIDs(String, String)](https://msdn.microsoft.com/library/bb646919\(v=office.15\)) method of the [NameSpace](https://msdn.microsoft.com/library/bb645857\(v=office.15\)) object, the example then checks whether the **Recipient** object associated with the **AppointmentItem** object is the same as the **ExchangeUser** object that represents the user’s manager.</span></span> <span data-ttu-id="51415-111">Если метод **CompareEntryIDs** возвращает значение **true**, это значит, что руководитель пользователя присутствует в коллекции **Recipients**, и метод CheckManagerResponseStatus возвращает значение свойства **MeetingResponseStatus** для руководителя.</span><span class="sxs-lookup"><span data-stu-id="51415-111">If **CompareEntryIDs** returns **true**, the user’s manager is found in the **Recipients** collection, and CheckManagerResponseStatus returns the manager’s **MeetingResponseStatus**.</span></span> <span data-ttu-id="51415-112">Если метод **CompareEntryIDs** возвращает значение **false**, метод CheckManagerResponseStatus возвращает пустую ссылку.</span><span class="sxs-lookup"><span data-stu-id="51415-112">If **CompareEntryIDs** returns **false**, CheckManagerResponseStatus returns a null reference.</span></span>

<span data-ttu-id="51415-113">Если вы используете Visual Studio для тестирования этого примера кода, сначала добавьте ссылку на компонент Microsoft Outlook 15.0 Object Library и задайте переменную Outlook при импорте пространства имен **Microsoft.Office.Interop.Outlook**.</span><span class="sxs-lookup"><span data-stu-id="51415-113">If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the Outlook variable when you import the **Microsoft.Office.Interop.Outlook** namespace.</span></span> <span data-ttu-id="51415-114">Инструкция **using** не должна находиться непосредственно перед функциями в примере кода, но ее нужно добавить перед объявлением общедоступного класса.</span><span class="sxs-lookup"><span data-stu-id="51415-114">The **using** statement must not occur directly before the functions in the code example but must be added before the public Class declaration.</span></span> <span data-ttu-id="51415-115">В приведенной ниже строке кода показано, как выполнить импорт и назначение на языке C\#.</span><span class="sxs-lookup"><span data-stu-id="51415-115">The following line of code shows how to do the import and assignment in C\#.</span></span>

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```csharp
private Object CheckManagerResponseStatus(Outlook.AppointmentItem appt)
{
    try
    {
        if (appt == null)
        {
            throw new ArgumentNullException();
        }
        Outlook.AddressEntry user =
            Application.Session.CurrentUser.AddressEntry;
        Outlook.ExchangeUser userEx = user.GetExchangeUser();
        if (userEx == null)
        {
            return null;
        }
        Outlook.ExchangeUser manager =
            userEx.GetExchangeUserManager();
        if (manager == null)
        {
            return null;
        }
        foreach (Outlook.Recipient recip in appt.Recipients)
        {
            if (Application.Session.CompareEntryIDs(
                recip.AddressEntry.ID, manager.ID))
            {
                return recip.MeetingResponseStatus;
            }
        }
        return null;
    }
    catch (Exception ex)
    {
        Debug.WriteLine(ex.Message);
        return null;
    }
}
```

## <a name="see-also"></a><span data-ttu-id="51415-116">См. также</span><span class="sxs-lookup"><span data-stu-id="51415-116">See also</span></span>

- [<span data-ttu-id="51415-117">Пользователи Exchange</span><span class="sxs-lookup"><span data-stu-id="51415-117">Exchange users</span></span>](exchange-users.md)


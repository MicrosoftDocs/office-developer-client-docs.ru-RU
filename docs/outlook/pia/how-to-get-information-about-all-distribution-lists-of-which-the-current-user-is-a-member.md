---
title: Получение сведений обо всех списках рассылки, участником которых является текущий пользователь
TOCTitle: Get information about all distribution lists of which the current user is a member
ms:assetid: c5be6aa8-8d85-463e-a377-2a4d57e2106b
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184638(v=office.15)
ms:contentKeyID: 55119836
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 2bbc87250ab77f662e0fc5a71f9857e734637dd2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32349429"
---
# <a name="get-information-about-all-distribution-lists-of-which-the-current-user-is-a-member"></a><span data-ttu-id="67cb2-102">Получение сведений обо всех списках рассылки, участником которых является текущий пользователь</span><span class="sxs-lookup"><span data-stu-id="67cb2-102">Get information about all distribution lists of which the current user is a member</span></span>

<span data-ttu-id="67cb2-103">В этом примере используется метод [GetMemberOfList()](https://msdn.microsoft.com/library/bb623397\(v=office.15\)) для получения сведений обо всех списках рассылки, участником которых является текущий пользователь.</span><span class="sxs-lookup"><span data-stu-id="67cb2-103">This example uses the [GetMemberOfList()](https://msdn.microsoft.com/library/bb623397\(v=office.15\)) method to get information about all distribution lists of which the current user is a member.</span></span>

## <a name="example"></a><span data-ttu-id="67cb2-104">Пример</span><span class="sxs-lookup"><span data-stu-id="67cb2-104">Example</span></span>

> [!NOTE] 
> <span data-ttu-id="67cb2-105">Приведенный ниже пример кода взят из книги [Программирование приложений для Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).</span><span class="sxs-lookup"><span data-stu-id="67cb2-105">The following code example is an excerpt from [Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).</span></span>

<span data-ttu-id="67cb2-106">В приведенном ниже примере GetCurrentUserMembership вызывает метод **GetMemberOfList**, чтобы получить коллекцию [AddressEntries](https://msdn.microsoft.com/library/bb647650\(v=office.15\)) для всех списков рассылки, в которые входит пользователь Exchange.</span><span class="sxs-lookup"><span data-stu-id="67cb2-106">In the following example, GetCurrentUserMembership calls the **GetMemberOfList** method to get an [AddressEntries](https://msdn.microsoft.com/library/bb647650\(v=office.15\)) collection for all distribution lists of which the Exchange user is a member.</span></span> <span data-ttu-id="67cb2-107">Если пользователь не является участником списков рассылки, **GetMemberOfList** возвращает коллекцию **AddressEntries** с количеством, равным нулю.</span><span class="sxs-lookup"><span data-stu-id="67cb2-107">If the user is not a member of any distribution lists, **GetMemberOfList** returns an **AddressEntries** collection that has a count of zero.</span></span> <span data-ttu-id="67cb2-108">Чтобы метод **GetMemberOfList** вернул коллекцию **AddressEntries**, вошедший в систему пользователь должен присутствовать, в противном случае **GetMemberOfList** возвращает пустую ссылку (NULL).</span><span class="sxs-lookup"><span data-stu-id="67cb2-108">The user must be online for **GetMemberOfList** to return an **AddressEntries** collection; otherwise, **GetMemberOfList** returns a null reference.</span></span> <span data-ttu-id="67cb2-109">GetCurrentUserMembership использует метод [GetExchangeUser()](https://msdn.microsoft.com/library/bb645260\(v=office.15\)), который возвращает текущий объект [ExchangeUser](https://msdn.microsoft.com/library/bb609574\(v=office.15\)), чтобы определить, присутствует ли пользователь.</span><span class="sxs-lookup"><span data-stu-id="67cb2-109">GetCurrentUserMembership uses the [GetExchangeUser()](https://msdn.microsoft.com/library/bb645260\(v=office.15\)) method, which returns the current [ExchangeUser](https://msdn.microsoft.com/library/bb609574\(v=office.15\)) object, to test whether the user is online.</span></span> <span data-ttu-id="67cb2-110">Если записи адресов получены, в примере записываются сведения о каждом списке рассылки пользователя в прослушиватели трассировки коллекции [Listeners](https://msdn.microsoft.com/library/system.diagnostics.debug.listeners.aspx).</span><span class="sxs-lookup"><span data-stu-id="67cb2-110">Once the address entries are obtained, the example writes information about each of the user’s distribution lists to the trace listeners of the [Listeners](https://msdn.microsoft.com/library/system.diagnostics.debug.listeners.aspx) collection.</span></span>

<span data-ttu-id="67cb2-111">Если вы используете Visual Studio для тестирования этого примера кода, сначала добавьте ссылку на компонент Microsoft Outlook 15.0 Object Library и задайте переменную Outlook при импорте пространства имен **Microsoft.Office.Interop.Outlook**.</span><span class="sxs-lookup"><span data-stu-id="67cb2-111">If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the Outlook variable when you import the **Microsoft.Office.Interop.Outlook** namespace.</span></span> <span data-ttu-id="67cb2-112">Инструкция **using** не должна находиться непосредственно перед функциями в примере кода, но ее нужно добавить перед объявлением общедоступного класса.</span><span class="sxs-lookup"><span data-stu-id="67cb2-112">The **using** statement must not occur directly before the functions in the code example but must be added before the public Class declaration.</span></span> <span data-ttu-id="67cb2-113">В приведенной ниже строке кода показано, как выполнить импорт и назначение на языке C\#.</span><span class="sxs-lookup"><span data-stu-id="67cb2-113">The following line of code shows how to do the import and assignment in C\#.</span></span>

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```csharp
private void GetCurrentUserMembership()
{
    Outlook.AddressEntry currentUser =
        Application.Session.CurrentUser.AddressEntry;
    if (currentUser.Type == "EX")
    {
        Outlook.ExchangeUser exchUser =
            currentUser.GetExchangeUser();
        if (exchUser != null)
        {
            Outlook.AddressEntries addrEntries =
                exchUser.GetMemberOfList();
            if (addrEntries != null)
            {
                foreach (Outlook.AddressEntry addrEntry
                    in addrEntries)
                {
                    Debug.WriteLine(addrEntry.Name);
                }
            }
        }
    }
}
```

## <a name="see-also"></a><span data-ttu-id="67cb2-114">См. также</span><span class="sxs-lookup"><span data-stu-id="67cb2-114">See also</span></span>

- [<span data-ttu-id="67cb2-115">Пользователи Exchange</span><span class="sxs-lookup"><span data-stu-id="67cb2-115">Exchange users</span></span>](exchange-users.md)


---
title: Получение сведений о подчиненных руководителя текущего пользователя
TOCTitle: Get information about direct reports of the current user's manager
ms:assetid: 768bf573-1b10-4776-8947-a7f8dc3ebde0
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184617(v=office.15)
ms:contentKeyID: 55119842
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: d49e96138d8cd2d857c49cc293258e1493afc747
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32349436"
---
# <a name="get-information-about-direct-reports-of-the-current-users-manager"></a><span data-ttu-id="e6ee5-102">Получение сведений о подчиненных руководителя текущего пользователя</span><span class="sxs-lookup"><span data-stu-id="e6ee5-102">Get information about direct reports of the current user's manager</span></span>

<span data-ttu-id="e6ee5-103">В этом примере получаются, при их наличии, подчиненные руководителя текущего пользователя, а затем отображаются сведения о каждом из подчиненных руководителя.</span><span class="sxs-lookup"><span data-stu-id="e6ee5-103">This example gets the direct reports of the current user’s manager, if any, and then displays information about each of the manager’s direct reports.</span></span>

## <a name="example"></a><span data-ttu-id="e6ee5-104">Пример</span><span class="sxs-lookup"><span data-stu-id="e6ee5-104">Example</span></span>

> [!NOTE] 
> <span data-ttu-id="e6ee5-105">Приведенный ниже пример кода представляет собой фрагмент из книги [Программирование приложений для Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).</span><span class="sxs-lookup"><span data-stu-id="e6ee5-105">The following code example is an excerpt from [Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).</span></span>

<span data-ttu-id="e6ee5-106">В следующем примере процедура GetManagerDirectReports вызывает метод [GetExchangeUserManager()](https://msdn.microsoft.com/library/bb646656\(v=office.15\)), чтобы получить руководителя пользователя, представленного объектом [ExchangeUser](https://msdn.microsoft.com/library/bb609574\(v=office.15\)).</span><span class="sxs-lookup"><span data-stu-id="e6ee5-106">In the following example, the GetManagerDirectReports procedure calls the [GetExchangeUserManager()](https://msdn.microsoft.com/library/bb646656\(v=office.15\)) method to get the user’s manager, represented by an [ExchangeUser](https://msdn.microsoft.com/library/bb609574\(v=office.15\)) object.</span></span> <span data-ttu-id="e6ee5-107">Если у текущего пользователя есть руководитель, вызывается [GetDirectReports()](https://msdn.microsoft.com/library/bb647204\(v=office.15\)), чтобы возвратить коллекцию [AddressEntries](https://msdn.microsoft.com/library/bb647650\(v=office.15\)), представляющую собой записи адресов для всех подчиненных руководителя пользователя.</span><span class="sxs-lookup"><span data-stu-id="e6ee5-107">If the current user has a manager, [GetDirectReports()](https://msdn.microsoft.com/library/bb647204\(v=office.15\)) is called to return an [AddressEntries](https://msdn.microsoft.com/library/bb647650\(v=office.15\)) collection that represents the address entries for all the direct reports of user’s manager.</span></span> <span data-ttu-id="e6ee5-108">Если у руководителя нет подчиненных, **GetDirectReports** возвращает коллекцию **AddressEntries** с количеством, равным нулю.</span><span class="sxs-lookup"><span data-stu-id="e6ee5-108">If the manager has no direct reports, **GetDirectReports** returns an **AddressEntries** collection that has a count of zero.</span></span> <span data-ttu-id="e6ee5-109">Если подчиненные руководителя получены, GetManagerDirectReports записывает сведения о каждом из подчиненных руководителя в прослушиватели трассировки коллекции [Listeners](https://msdn.microsoft.com/library/system.diagnostics.debug.listeners.aspx).</span><span class="sxs-lookup"><span data-stu-id="e6ee5-109">Once the manager’s direct reports are obtained, GetManagerDirectReports writes information about each of the manager’s direct reports to the trace listeners of the [Listeners](https://msdn.microsoft.com/library/system.diagnostics.debug.listeners.aspx) collection.</span></span>


> [!NOTE]
> <span data-ttu-id="e6ee5-110">Чтобы этот метод вернул коллекцию **AddressEntries**, вошедший в систему пользователь должен присутствовать, в противном случае **GetDirectReports** возвращает пустую ссылку (NULL).</span><span class="sxs-lookup"><span data-stu-id="e6ee5-110">The signed-in user must be online for this method to return an **AddressEntries** collection; otherwise, **GetDirectReports** returns a null reference.</span></span> <span data-ttu-id="e6ee5-111">Для кода, используемого в производственной среде, необходимо проверить возможное отсутствие пользователя, используя свойство [\_NameSpace.ExchangeConnectionMode](https://msdn.microsoft.com/library/bb647638(v=office.15)) или свойство [\_Account.ExchangeConnectionMode](https://msdn.microsoft.com/library/ff185249(v=office.15)) для нескольких сценариев Exchange.</span><span class="sxs-lookup"><span data-stu-id="e6ee5-111">For production code, you must test for the user being offline by using the [\_NameSpace.ExchangeConnectionMode](https://msdn.microsoft.com/library/bb647638(v=office.15)) property, or the [\_Account.ExchangeConnectionMode](https://msdn.microsoft.com/library/ff185249(v=office.15)) property for multiple Exchange scenarios.</span></span>

<span data-ttu-id="e6ee5-112">Если вы используете Visual Studio для тестирования этого примера кода, сначала добавьте ссылку на компонент Microsoft Outlook 15.0 Object Library и задайте переменную Outlook при импорте пространства имен **Microsoft.Office.Interop.Outlook**.</span><span class="sxs-lookup"><span data-stu-id="e6ee5-112">If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the Outlook variable when you import the **Microsoft.Office.Interop.Outlook** namespace.</span></span> <span data-ttu-id="e6ee5-113">Инструкция **using** не должна находиться непосредственно перед функциями в примере кода, но ее нужно добавить перед объявлением общедоступного класса.</span><span class="sxs-lookup"><span data-stu-id="e6ee5-113">The **using** statement must not occur directly before the functions in the code example but must be added before the public Class declaration.</span></span> <span data-ttu-id="e6ee5-114">В приведенной ниже строке кода показано, как выполнить импорт и назначение на языке C\#.</span><span class="sxs-lookup"><span data-stu-id="e6ee5-114">The following line of code shows how to do the import and assignment in C\#.</span></span>

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```csharp
private void GetManagerDirectReports()
{
    Outlook.AddressEntry currentUser =
        Application.Session.CurrentUser.AddressEntry;
    if (currentUser.Type == "EX")
    {
        Outlook.ExchangeUser manager =
            currentUser.GetExchangeUser().GetExchangeUserManager();
        if (manager != null)
        {
            Outlook.AddressEntries addrEntries =
                manager.GetDirectReports();
            if (addrEntries != null)
            {
                foreach (Outlook.AddressEntry addrEntry
                    in addrEntries)
                {
                    Outlook.ExchangeUser exchUser =
                        addrEntry.GetExchangeUser();
                    StringBuilder sb = new StringBuilder();
                    sb.AppendLine("Name: "
                        + exchUser.Name);
                    sb.AppendLine("Title: "
                        + exchUser.JobTitle);
                    sb.AppendLine("Department: "
                        + exchUser.Department);
                    sb.AppendLine("Location: "
                        + exchUser.OfficeLocation);
                    Debug.WriteLine(sb.ToString());
                }
            }
        }
    }
}
```

## <a name="see-also"></a><span data-ttu-id="e6ee5-115">См. также</span><span class="sxs-lookup"><span data-stu-id="e6ee5-115">See also</span></span>

- [<span data-ttu-id="e6ee5-116">Пользователи Exchange</span><span class="sxs-lookup"><span data-stu-id="e6ee5-116">Exchange users</span></span>](exchange-users.md)


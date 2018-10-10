---
title: Получение сведений о руководителе текущего пользователя
TOCTitle: Get information about the current user's manager
ms:assetid: 3a77fa51-e2e3-4544-849f-4267b1762270
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184603(v=office.15)
ms:contentKeyID: 55119846
ms.date: 07/24/2014
mtps_version: v=office.15
ms.openlocfilehash: 89da7df4aac29b7d308dd0b0f432d8652c5f0127
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25407312"
---
# <a name="get-information-about-the-current-users-manager"></a><span data-ttu-id="90582-102">Получение сведений о руководителе текущего пользователя</span><span class="sxs-lookup"><span data-stu-id="90582-102">Get information about the current user's manager</span></span>

<span data-ttu-id="90582-103">В этом примере показано, как получить сведения (например, имя, должность и номера телефонов) о руководителе текущего пользователя.</span><span class="sxs-lookup"><span data-stu-id="90582-103">This example shows how to get information (such as name, job title, and phone numbers) about the current user’s manager.</span></span>

## <a name="example"></a><span data-ttu-id="90582-104">Пример</span><span class="sxs-lookup"><span data-stu-id="90582-104">Example</span></span>

> [!NOTE] 
> <span data-ttu-id="90582-105">Приведенный ниже пример кода представляет собой фрагмент из книги [Программирование приложений для Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).</span><span class="sxs-lookup"><span data-stu-id="90582-105">The following code example is an excerpt from  [Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493)  , from Microsoft Press (ISBN 9780735622494, copyright Microsoft Press 2007, all rights reserved).</span></span>

<span data-ttu-id="90582-106">В следующей процедуре GetManagerInfo вызывает метод [GetExchangeUserManager()](https://msdn.microsoft.com/library/bb646656\(v=office.15\)), чтобы получить объект [ExchangeUser](https://msdn.microsoft.com/library/bb609574\(v=office.15\)), представляющий руководителя пользователя **ExchangeUser** в структуре организации.</span><span class="sxs-lookup"><span data-stu-id="90582-106">In the following procedure,   calls the GetExchangeUserManager() method to obtain an ExchangeUser object that represents the manager of an ExchangeUser in the organizational hierarchy.</span></span> <span data-ttu-id="90582-107">Процедура проверяет, находится ли вошедший пользователь в сети для подтверждения того, что метод **GetExchangeUserManager** может вернуть объект **ExchangeUser**.</span><span class="sxs-lookup"><span data-stu-id="90582-107">The procedure tests whether the logged-on user is online to ensure that **GetExchangeUserManager** can return an **ExchangeUser** object.</span></span> <span data-ttu-id="90582-108">Если пользователь не находится в сети, метод **GetExchangeUserManager** вернет пустую ссылку.</span><span class="sxs-lookup"><span data-stu-id="90582-108">If the user is not online, **GetExchangeUserManager** will return a null reference.</span></span> <span data-ttu-id="90582-109">GetManagerInfo затем записывает сведения о руководителе в прослушиватели трассировки коллекции [Listeners](https://msdn.microsoft.com/library/system.diagnostics.debug.listeners.aspx).</span><span class="sxs-lookup"><span data-stu-id="90582-109"> then writes manager information to the trace listeners of the Listeners collection.</span></span>

<span data-ttu-id="90582-110">Если вы используете Visual Studio для тестирования этого примера кода, сначала добавьте ссылку на компонент Microsoft Outlook 15.0 Object Library и задайте переменную Outlook при импорте пространства имен **Microsoft.Office.Interop.Outlook**.</span><span class="sxs-lookup"><span data-stu-id="90582-110">If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the   variable when you import the Microsoft.Office.Interop.Outlook namespace.</span></span> <span data-ttu-id="90582-111">Инструкция **using** не должна идти непосредственно перед функциями в примере кода, но ее нужно добавить перед открытым объявлением Class.</span><span class="sxs-lookup"><span data-stu-id="90582-111">The using statement must not occur directly before the functions in the code example but must be added before the public   declaration.</span></span> <span data-ttu-id="90582-112">В следующей строке кода показано, как выполнить импорт и назначение в C\#.</span><span class="sxs-lookup"><span data-stu-id="90582-112">The following line of code shows how to do the import and assignment in C#.</span></span>

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```csharp
private void GetManagerInfo()
{
    Outlook.AddressEntry currentUser =
        Application.Session.CurrentUser.AddressEntry;
    if (currentUser.Type == "EX")
    {
        Outlook.ExchangeUser manager =
            currentUser.GetExchangeUser().GetExchangeUserManager();
        if (manager != null)
        {
            StringBuilder sb = new StringBuilder();
            sb.AppendLine("Name: "
                + manager.Name);
            sb.AppendLine("STMP address: "
                + manager.PrimarySmtpAddress);
            sb.AppendLine("Title: "
                + manager.JobTitle);
            sb.AppendLine("Department: "
                + manager.Department);
            sb.AppendLine("Location: "
                + manager.OfficeLocation);
            sb.AppendLine("Business phone: "
                + manager.BusinessTelephoneNumber);
            sb.AppendLine("Mobile phone: "
                + manager.MobileTelephoneNumber);
            Debug.WriteLine(sb.ToString());
        }
    }
}
```

## <a name="see-also"></a><span data-ttu-id="90582-113">См. также</span><span class="sxs-lookup"><span data-stu-id="90582-113">See also</span></span>

- [<span data-ttu-id="90582-114">Пользователи Exchange</span><span class="sxs-lookup"><span data-stu-id="90582-114">Exchange Users</span></span>](exchange-users.md)


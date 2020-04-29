---
title: Выполнение перечисления записей в глобальном списке адресов
TOCTitle: Enumerate the entries in the Global Address List
ms:assetid: f3dfe312-fe91-475d-8435-1c7a0bb2b725
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184654(v=office.15)
ms:contentKeyID: 55119801
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 98256ce539172b69c2ae94d495c4aab12e3b8cc4
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32320365"
---
# <a name="enumerate-the-entries-in-the-global-address-list"></a><span data-ttu-id="46a36-102">Выполнение перечисления записей в глобальном списке адресов</span><span class="sxs-lookup"><span data-stu-id="46a36-102">Enumerate the entries in the Global Address List</span></span>

<span data-ttu-id="46a36-103">В этом примере показано, как выполнить перечисление первых 100 основных SMTP-адресов в глобальном списке адресов.</span><span class="sxs-lookup"><span data-stu-id="46a36-103">This example enumerates the first 100 primary Simple Mail Transfer Protocol (SMTP) addresses in the Global Address List (GAL).</span></span>

## <a name="example"></a><span data-ttu-id="46a36-104">Пример</span><span class="sxs-lookup"><span data-stu-id="46a36-104">Example</span></span>

> [!NOTE] 
> <span data-ttu-id="46a36-105">Приведенный ниже пример кода взят из книги [Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493) ("Программирование приложений для Microsoft Office Outlook 2007").</span><span class="sxs-lookup"><span data-stu-id="46a36-105">The following code example is an excerpt from [Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).</span></span>

<span data-ttu-id="46a36-106">В следующем примере получение кода адреса SMTP для объекта [AddressEntry](https://msdn.microsoft.com/library/bb609728\(v=office.15\)) выполняется путем приведения его к объекту [ExchangeUser](https://msdn.microsoft.com/library/bb609574\(v=office.15\)) или [ExchangeDistributionList](https://msdn.microsoft.com/library/bb624320\(v=office.15\)) при вызове метода [GetExchangeUser()](https://msdn.microsoft.com/library/bb645260\(v=office.15\)) или [GetExchangeDistributionList()](https://msdn.microsoft.com/library/bb611805\(v=office.15\)) .</span><span class="sxs-lookup"><span data-stu-id="46a36-106">In the following code example, the SMTP address for an [AddressEntry](https://msdn.microsoft.com/library/bb609728\(v=office.15\)) object is obtained by casting it to an [ExchangeUser](https://msdn.microsoft.com/library/bb609574\(v=office.15\)) or [ExchangeDistributionList](https://msdn.microsoft.com/library/bb624320\(v=office.15\)) object in a call to the [GetExchangeUser()](https://msdn.microsoft.com/library/bb645260\(v=office.15\)) or [GetExchangeDistributionList()](https://msdn.microsoft.com/library/bb611805\(v=office.15\)) methods.</span></span> <span data-ttu-id="46a36-107">Если объект **AddressEntry** представляет пользователя Exchange, метод EnumerateGAL возвращает объект **ExchangeUser**, через который можно получить доступ к свойствам объекта **AddressEntry**.</span><span class="sxs-lookup"><span data-stu-id="46a36-107">If the **AddressEntry** object represents an Exchange user, EnumerateGAL returns an **ExchangeUser** object that exposes properties of the **AddressEntry** object.</span></span> <span data-ttu-id="46a36-108">Для доступа к этим свойствам используйте свойства объекта ExchangeUser, например [JobTitle](https://msdn.microsoft.com/library/bb645451\(v=office.15\)), [Department](https://msdn.microsoft.com/library/bb623789\(v=office.15\)), [Alias](https://msdn.microsoft.com/library/bb610682\(v=office.15\)), [BusinessTelephoneNumber](https://msdn.microsoft.com/library/bb612294\(v=office.15\)) или [PrimarySmtpAddress](https://msdn.microsoft.com/library/bb645506\(v=office.15\)).</span><span class="sxs-lookup"><span data-stu-id="46a36-108">Use ExchangeUser properties such as [JobTitle](https://msdn.microsoft.com/library/bb645451\(v=office.15\)), [Department](https://msdn.microsoft.com/library/bb623789\(v=office.15\)), [Alias](https://msdn.microsoft.com/library/bb610682\(v=office.15\)), [BusinessTelephoneNumber](https://msdn.microsoft.com/library/bb612294\(v=office.15\)), or [PrimarySmtpAddress](https://msdn.microsoft.com/library/bb645506\(v=office.15\)) to expose them.</span></span>

<span data-ttu-id="46a36-109">Если вы используете Visual Studio для тестирования этого примера кода, сначала добавьте ссылку на компонент Microsoft Outlook 15.0 Object Library и задайте переменную Outlook при импорте пространства имен **Microsoft.Office.Interop.Outlook**.</span><span class="sxs-lookup"><span data-stu-id="46a36-109">If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the Outlook variable when you import the **Microsoft.Office.Interop.Outlook** namespace.</span></span> <span data-ttu-id="46a36-110">Инструкция **using** не должна находиться непосредственно перед функциями в примере кода, но ее нужно добавить перед объявлением общедоступного класса.</span><span class="sxs-lookup"><span data-stu-id="46a36-110">The **using** statement must not occur directly before the functions in the code example but must be added before the public Class declaration.</span></span> <span data-ttu-id="46a36-111">В приведенной ниже строке кода показано, как выполнить импорт и назначение на языке C\#.</span><span class="sxs-lookup"><span data-stu-id="46a36-111">The following line of code shows how to do the import and assignment in C\#.</span></span>

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```

```csharp
private void EnumerateGAL()
{
    Outlook.AddressList gal =
        Application.Session.GetGlobalAddressList();
    if (gal != null)
    {
        for (int i = 1; 
            i <= Math.Min(100, gal.AddressEntries.Count - 1); i++)
        {
            Outlook.AddressEntry addrEntry =
                gal.AddressEntries[i];
            if (addrEntry.AddressEntryUserType ==
                Outlook.OlAddressEntryUserType.
                olExchangeUserAddressEntry
                || addrEntry.AddressEntryUserType ==
                Outlook.OlAddressEntryUserType.
                olExchangeRemoteUserAddressEntry)
            {
                Outlook.ExchangeUser exchUser =
                    addrEntry.GetExchangeUser();
                Debug.WriteLine(exchUser.Name + " "
                    + exchUser.PrimarySmtpAddress);
            }
            if (addrEntry.AddressEntryUserType ==
                Outlook.OlAddressEntryUserType.
                olExchangeDistributionListAddressEntry)
            {
                Outlook.ExchangeDistributionList exchDL =
                    addrEntry.GetExchangeDistributionList();
                Debug.WriteLine(exchDL.Name + " "
                    + exchDL.PrimarySmtpAddress);
            }
        }
    }
}
```

## <a name="see-also"></a><span data-ttu-id="46a36-112">См. также</span><span class="sxs-lookup"><span data-stu-id="46a36-112">See also</span></span>

[<span data-ttu-id="46a36-113">Адресная книга</span><span class="sxs-lookup"><span data-stu-id="46a36-113">Address book</span></span>](address-book.md)


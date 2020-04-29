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
# <a name="get-information-about-all-distribution-lists-of-which-the-current-user-is-a-member"></a>Получение сведений обо всех списках рассылки, участником которых является текущий пользователь

В этом примере используется метод [GetMemberOfList()](https://msdn.microsoft.com/library/bb623397\(v=office.15\)) для получения сведений обо всех списках рассылки, участником которых является текущий пользователь.

## <a name="example"></a>Пример

> [!NOTE] 
> Приведенный ниже пример кода взят из книги [Программирование приложений для Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).

В приведенном ниже примере GetCurrentUserMembership вызывает метод **GetMemberOfList**, чтобы получить коллекцию [AddressEntries](https://msdn.microsoft.com/library/bb647650\(v=office.15\)) для всех списков рассылки, в которые входит пользователь Exchange. Если пользователь не является участником списков рассылки, **GetMemberOfList** возвращает коллекцию **AddressEntries** с количеством, равным нулю. Чтобы метод **GetMemberOfList** вернул коллекцию **AddressEntries**, вошедший в систему пользователь должен присутствовать, в противном случае **GetMemberOfList** возвращает пустую ссылку (NULL). GetCurrentUserMembership использует метод [GetExchangeUser()](https://msdn.microsoft.com/library/bb645260\(v=office.15\)), который возвращает текущий объект [ExchangeUser](https://msdn.microsoft.com/library/bb609574\(v=office.15\)), чтобы определить, присутствует ли пользователь. Если записи адресов получены, в примере записываются сведения о каждом списке рассылки пользователя в прослушиватели трассировки коллекции [Listeners](https://msdn.microsoft.com/library/system.diagnostics.debug.listeners.aspx).

Если вы используете Visual Studio для тестирования этого примера кода, сначала добавьте ссылку на компонент Microsoft Outlook 15.0 Object Library и задайте переменную Outlook при импорте пространства имен **Microsoft.Office.Interop.Outlook**. Инструкция **using** не должна находиться непосредственно перед функциями в примере кода, но ее нужно добавить перед объявлением общедоступного класса. В приведенной ниже строке кода показано, как выполнить импорт и назначение на языке C\#.

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

## <a name="see-also"></a>См. также

- [Пользователи Exchange](exchange-users.md)


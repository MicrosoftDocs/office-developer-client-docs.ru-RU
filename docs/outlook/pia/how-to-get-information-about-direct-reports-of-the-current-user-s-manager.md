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
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28705577"
---
# <a name="get-information-about-direct-reports-of-the-current-users-manager"></a>Получение сведений о подчиненных руководителя текущего пользователя

В этом примере получаются, при их наличии, подчиненные руководителя текущего пользователя, а затем отображаются сведения о каждом из подчиненных руководителя.

## <a name="example"></a>Пример

> [!NOTE] 
> Приведенный ниже пример кода представляет собой фрагмент из книги [Программирование приложений для Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).

В следующем примере процедура GetManagerDirectReports вызывает метод [GetExchangeUserManager()](https://msdn.microsoft.com/library/bb646656\(v=office.15\)), чтобы получить руководителя пользователя, представленного объектом [ExchangeUser](https://msdn.microsoft.com/library/bb609574\(v=office.15\)). Если у текущего пользователя есть руководитель, вызывается [GetDirectReports()](https://msdn.microsoft.com/library/bb647204\(v=office.15\)), чтобы возвратить коллекцию [AddressEntries](https://msdn.microsoft.com/library/bb647650\(v=office.15\)), представляющую собой записи адресов для всех подчиненных руководителя пользователя. Если у руководителя нет подчиненных, **GetDirectReports** возвращает коллекцию **AddressEntries** с количеством, равным нулю. Если подчиненные руководителя получены, GetManagerDirectReports записывает сведения о каждом из подчиненных руководителя в прослушиватели трассировки коллекции [Listeners](https://msdn.microsoft.com/library/system.diagnostics.debug.listeners.aspx).


> [!NOTE]
> Чтобы этот метод вернул коллекцию **AddressEntries**, вошедший в систему пользователь должен присутствовать, в противном случае **GetDirectReports** возвращает пустую ссылку (NULL). Для кода, используемого в производственной среде, необходимо проверить возможное отсутствие пользователя, используя свойство [\_NameSpace.ExchangeConnectionMode](https://msdn.microsoft.com/library/bb647638(v=office.15)) или свойство [\_Account.ExchangeConnectionMode](https://msdn.microsoft.com/library/ff185249(v=office.15)) для нескольких сценариев Exchange.

Если вы используете Visual Studio для тестирования этого примера кода, сначала добавьте ссылку на компонент Microsoft Outlook 15.0 Object Library и задайте переменную Outlook при импорте пространства имен **Microsoft.Office.Interop.Outlook**. Инструкция **using** не должна идти непосредственно перед функциями в примере кода, но ее нужно добавить перед открытым объявлением Class. В следующей строке кода показано, как выполнить импорт и назначение в C\#.

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

## <a name="see-also"></a>См. также

- [Пользователи Exchange](exchange-users.md)


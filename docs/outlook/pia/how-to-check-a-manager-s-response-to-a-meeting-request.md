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
# <a name="check-a-managers-response-to-a-meeting-request"></a>Проверка ответа руководителя на приглашение на собрание

В этом примере показано использование методов [GetExchangeUser()](https://msdn.microsoft.com/library/bb611808\(v=office.15\)) и [GetExchangeUserManager()](https://msdn.microsoft.com/library/bb646656\(v=office.15\)) для проверки состояния ответа руководителя текущего пользователя на приглашение на собрание.

## <a name="example"></a>Пример

> [!NOTE] 
> Приведенный ниже пример кода представляет собой фрагмент из книги [Программирование приложений для Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).

Чтобы определить, принято или отклонено приглашение на собрание соответствующим получателем, используйте свойство [MeetingResponseStatus](https://msdn.microsoft.com/library/bb645283\(v=office.15\)) объекта [Recipient](https://msdn.microsoft.com/library/bb624370\(v=office.15\)) из коллекции [Recipients](https://msdn.microsoft.com/library/bb646361\(v=office.15\)), связанной с объектом [AppointmentItem](https://msdn.microsoft.com/library/bb645611\(v=office.15\)) .

В следующем примере кода метод CheckManagerResponseStatus принимает в качестве параметра объект **AppointmentItem**. Метод CheckManagerResponseStatus получает объект [ExchangeUser](https://msdn.microsoft.com/library/bb609574\(v=office.15\)) путем вызова метода **GetExchangeUser** для текущего пользователя. После этого метод CheckManagerResponseStatus получает объект **ExchangeUser**, связанный с руководителем текущего пользователя, посредством вызова метода **GetExchangeUserManager**. С помощью метода [CompareEntryIDs(String, String)](https://msdn.microsoft.com/library/bb646919\(v=office.15\)) объекта [NameSpace](https://msdn.microsoft.com/library/bb645857\(v=office.15\)) в этом примере проверяется, соответствует ли объект **Recipient**, связанный с объектом **AppointmentItem**, объекту **ExchangeUser**, который представляет руководителя пользователя. Если метод **CompareEntryIDs** возвращает значение **true**, это значит, что руководитель пользователя присутствует в коллекции **Recipients**, и метод CheckManagerResponseStatus возвращает значение свойства **MeetingResponseStatus** для руководителя. Если метод **CompareEntryIDs** возвращает значение **false**, метод CheckManagerResponseStatus возвращает пустую ссылку.

Если вы используете Visual Studio для тестирования этого примера кода, сначала добавьте ссылку на компонент Microsoft Outlook 15.0 Object Library и задайте переменную Outlook при импорте пространства имен **Microsoft.Office.Interop.Outlook**. Инструкция **using** не должна находиться непосредственно перед функциями в примере кода, но ее нужно добавить перед объявлением общедоступного класса. В приведенной ниже строке кода показано, как выполнить импорт и назначение на языке C\#.

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

## <a name="see-also"></a>См. также

- [Пользователи Exchange](exchange-users.md)


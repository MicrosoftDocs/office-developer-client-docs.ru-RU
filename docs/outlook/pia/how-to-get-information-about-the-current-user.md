---
title: Получение сведений о текущем пользователе
TOCTitle: Get information about the current user
ms:assetid: 3802523a-3ccf-4cca-a348-abe2645a0d9c
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184601(v=office.15)
ms:contentKeyID: 55119840
ms.date: 07/24/2014
mtps_version: v=office.15
ms.openlocfilehash: 7ac10c01d205f4f4590183bcef8006e8f1344cbd
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25406976"
---
# <a name="get-information-about-the-current-user"></a>Получение сведений о текущем пользователе

В этом примере показано, как получить сведения о текущем пользователе, например имя, должность и номер телефона.

## <a name="example"></a>Пример

> [!NOTE] 
> Приведенный ниже пример кода представляет собой фрагмент из книги [Программирование приложений для Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).

Чтобы получить объект [ExchangeUser](https://msdn.microsoft.com/library/bb609574\(v=office.15\)) из объекта [AddressEntry](https://msdn.microsoft.com/library/bb609728\(v=office.15\)), вызовите метод [GetExchangeUser()](https://msdn.microsoft.com/library/bb611808\(v=office.15\)) для объекта **AddressEntry**. В следующей процедуре GetCurrentUserInfo получает свойство [AddressEntry](https://msdn.microsoft.com/library/bb644359\(v=office.15\)) для объекта [Recipient](https://msdn.microsoft.com/library/bb624370\(v=office.15\)), используя свойство [CurrentUser](https://msdn.microsoft.com/library/bb622574\(v=office.15\)). Если объект **AddressEntry** представляет пользователя почтового ящика Exchange, GetCurrentUserInfo вызывает метод **GetExchangeUser**, и возвращается объект **ExchangeUser**. Свойства [Name](https://msdn.microsoft.com/library/bb622941\(v=office.15\)), [PrimarySmtpAddress](https://msdn.microsoft.com/library/bb645506\(v=office.15\)), [JobTitle](https://msdn.microsoft.com/library/bb645451\(v=office.15\)), [Department](https://msdn.microsoft.com/library/bb623789\(v=office.15\)), [OfficeLocation](https://msdn.microsoft.com/library/bb611429\(v=office.15\)), [BusinessTelephoneNumber](https://msdn.microsoft.com/library/bb612294\(v=office.15\)) и [MobileTelephoneNumber](https://msdn.microsoft.com/library/bb609292\(v=office.15\)) записываются в прослушиватели трассировки коллекции [Listeners](https://msdn.microsoft.com/library/system.diagnostics.debug.listeners.aspx).

Если вы используете Visual Studio для тестирования этого примера кода, сначала добавьте ссылку на компонент Microsoft Outlook 15.0 Object Library и задайте переменную Outlook при импорте пространства имен **Microsoft.Office.Interop.Outlook**. Инструкция **using** не должна идти непосредственно перед функциями в примере кода, но ее нужно добавить перед открытым объявлением Class. В следующей строке кода показано, как выполнить импорт и назначение в C\#.

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```csharp
private void GetCurrentUserInfo()
{
    Outlook.AddressEntry addrEntry =
        Application.Session.CurrentUser.AddressEntry;
    if (addrEntry.Type == "EX")
    {
        Outlook.ExchangeUser currentUser =
            Application.Session.CurrentUser.
            AddressEntry.GetExchangeUser();
        if (currentUser != null)
        {
            StringBuilder sb = new StringBuilder();
            sb.AppendLine("Name: "
                + currentUser.Name);
            sb.AppendLine("STMP address: "
                + currentUser.PrimarySmtpAddress);
            sb.AppendLine("Title: "
                + currentUser.JobTitle);
            sb.AppendLine("Department: "
                + currentUser.Department);
            sb.AppendLine("Location: "
                + currentUser.OfficeLocation);
            sb.AppendLine("Business phone: "
                + currentUser.BusinessTelephoneNumber);
            sb.AppendLine("Mobile phone: "
                + currentUser.MobileTelephoneNumber);
            Debug.WriteLine(sb.ToString());
        }
    }
}
```

## <a name="see-also"></a>См. также

- [Пользователи Exchange](exchange-users.md)


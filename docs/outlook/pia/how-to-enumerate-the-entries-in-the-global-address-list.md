---
title: Выполнение перечисления записей в глобальном списке адресов
TOCTitle: Enumerate the entries in the Global Address List
ms:assetid: f3dfe312-fe91-475d-8435-1c7a0bb2b725
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184654(v=office.15)
ms:contentKeyID: 55119801
ms.date: 07/24/2014
mtps_version: v=office.15
ms.openlocfilehash: f9e392710940a63f5d7723d303d5cf48569ad92f
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25407550"
---
# <a name="enumerate-the-entries-in-the-global-address-list"></a>Выполнение перечисления записей в глобальном списке адресов

В этом примере показано, как выполнить перечисление первых 100 основных SMTP-адресов в глобальном списке адресов.

## <a name="example"></a>Пример

> [!NOTE] 
> Приведенный ниже пример кода взят из книги [Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493) ("Программирование приложений для Microsoft Office Outlook 2007").

В следующем примере получение кода адреса SMTP для объекта [AddressEntry](https://msdn.microsoft.com/library/bb609728\(v=office.15\)) выполняется путем приведения его к объекту [ExchangeUser](https://msdn.microsoft.com/library/bb609574\(v=office.15\)) или [ExchangeDistributionList](https://msdn.microsoft.com/library/bb624320\(v=office.15\)) при вызове метода [GetExchangeUser()](https://msdn.microsoft.com/library/bb645260\(v=office.15\)) или [GetExchangeDistributionList()](https://msdn.microsoft.com/library/bb611805\(v=office.15\)) . Если объект **AddressEntry** представляет пользователя Exchange, метод EnumerateGAL возвращает объект **ExchangeUser**, через который можно получить доступ к свойствам объекта **AddressEntry**. Для доступа к этим свойствам используйте свойства объекта ExchangeUser, например [JobTitle](https://msdn.microsoft.com/library/bb645451\(v=office.15\)), [Department](https://msdn.microsoft.com/library/bb623789\(v=office.15\)), [Alias](https://msdn.microsoft.com/library/bb610682\(v=office.15\)), [BusinessTelephoneNumber](https://msdn.microsoft.com/library/bb612294\(v=office.15\)) или [PrimarySmtpAddress](https://msdn.microsoft.com/library/bb645506\(v=office.15\)).

Если для тестирования этого примера кода вы используете Visual Studio, сначала добавьте ссылку на компонент библиотеки объектов Microsoft Outlook 15.0 и укажите переменную Outlook при импорте пространства имен **Microsoft.Office.Interop.Outlook**. Не следует использовать инструкцию **using** непосредственно перед функциями в примере кода, но ее необходимо добавить перед объявлением общедоступного класса. В строке кода ниже показано, как выполнить импорт и назначение на языке C\#.

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

## <a name="see-also"></a>См. также

[Адресная книга](address-book.md)


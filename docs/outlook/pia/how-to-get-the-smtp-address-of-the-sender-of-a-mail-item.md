---
title: Получение SMTP-адреса отправителя почтового элемента
TOCTitle: Get the SMTP address of the sender of a mail item
ms:assetid: 86e0c0aa-1696-4415-b25f-f9c1c29d88a9
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184624(v=office.15)
ms:contentKeyID: 55119869
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Priority
ms.openlocfilehash: 05d52f24262f08a6326d464a2dc0d57d6d0510d7
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/29/2019
ms.locfileid: "34542550"
---
# <a name="get-the-smtp-address-of-the-sender-of-a-mail-item"></a>Получение SMTP-адреса отправителя почтового элемента

В этом примере выполняется получение SMTP-адреса отправителя для почтового элемента.

## <a name="example"></a>Пример

Чтобы определить SMTP-адрес полученного почтового элемента, используйте свойство [SenderEmailAddress](https://msdn.microsoft.com/library/bb622746\(v=office.15\)) объекта [MailItem](https://msdn.microsoft.com/library/bb643865\(v=office.15\)). Однако если отправитель сообщения находится внутри организации, свойство **SenderEmailAddress** не возвращает SMTP-адрес. В этом случае необходимо использовать объект [PropertyAccessor](https://msdn.microsoft.com/library/bb646034\(v=office.15\)).

В следующем примере кода метод GetSenderSMTPAddress использует объект **PropertyAccessor** для получения значений, которые не предоставляются явно в объектной модели приложения Outlook. Метод GetSenderSMTPAddress получает объект **MailItem**. Если свойство [SenderEmailType](https://msdn.microsoft.com/library/bb624136\(v=office.15\)) полученного объекта **MailItem** имеет значение "EX", отправитель сообщения размещается на сервере Exchange в организации. Метод GetSenderSMTPAddress использует свойство [Sender](https://msdn.microsoft.com/library/ff184720\(v=office.15\)) объекта **MailItem** для получения отправителя, представленного объектом [AddressEntry](https://msdn.microsoft.com/library/bb609728\(v=office.15\)). Если объект **AddressEntry** представляет пользователя Exchange, в этом примере вызывается метод [GetExchangeUser()](https://msdn.microsoft.com/library/bb611808\(v=office.15\)), который возвращает объект [ExchangeUser](https://msdn.microsoft.com/library/bb609574\(v=office.15\)) объекта **AddressEntry**. После этого метод GetSenderSMTPAddress использует свойство [PrimarySmtpAddress](https://msdn.microsoft.com/library/bb645506\(v=office.15\)) объекта **ExchangeUser**, которое возвращает SMTP-адрес отправителя. Если объект **AddressEntry** для отправителя не представляет объект **ExchangeUser**, для получения SMTP-адреса отправителя используется метод [GetProperty(String)](https://msdn.microsoft.com/library/bb645726\(v=office.15\)) объекта **PropertyAccessor** с аргументом **PR\_SMTP\_ADDRESS** ([PidTagSmtpAddress](https://msdn.microsoft.com/library/cc842421\(v=office.15\))).

Если вы используете Visual Studio для тестирования этого примера кода, сначала добавьте ссылку на компонент Microsoft Outlook 15.0 Object Library и задайте переменную Outlook при импорте пространства имен **Microsoft.Office.Interop.Outlook**. Инструкция **using** не должна находиться непосредственно перед функциями в примере кода, но ее нужно добавить перед объявлением общедоступного класса. В приведенной ниже строке кода показано, как выполнить импорт и назначение на языке C\#.

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```csharp
private string GetSenderSMTPAddress(Outlook.MailItem mail)
{
    string PR_SMTP_ADDRESS =
        @"http://schemas.microsoft.com/mapi/proptag/0x39FE001E";
    if (mail == null)
    {
        throw new ArgumentNullException();
    }
    if (mail.SenderEmailType == "EX")
    {
        Outlook.AddressEntry sender =
            mail.Sender;
        if (sender != null)
        {
            //Now we have an AddressEntry representing the Sender
            if (sender.AddressEntryUserType ==
                Outlook.OlAddressEntryUserType.
                olExchangeUserAddressEntry
                || sender.AddressEntryUserType ==
                Outlook.OlAddressEntryUserType.
                olExchangeRemoteUserAddressEntry)
            {
                //Use the ExchangeUser object PrimarySMTPAddress
                Outlook.ExchangeUser exchUser =
                    sender.GetExchangeUser();
                if (exchUser != null)
                {
                    return exchUser.PrimarySmtpAddress;
                }
                else
                {
                    return null;
                }
            }
            else
            {
                return sender.PropertyAccessor.GetProperty(
                    PR_SMTP_ADDRESS) as string;
            }
        }
        else
        {
            return null;
        }
    }
    else
    {
        return mail.SenderEmailAddress;
    }
}
```

## <a name="see-also"></a>См. также

- [Почта](mail.md)


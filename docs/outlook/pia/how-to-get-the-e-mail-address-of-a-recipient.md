---
title: Получение адреса электронной почты получателя
TOCTitle: Get the email address of a recipient
ms:assetid: e585811b-a298-496f-ba79-df7d46526169
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184647(v=office.15)
ms:contentKeyID: 55119879
ms.date: 07/24/2014
mtps_version: v=office.15
ms.openlocfilehash: 15e2450e6ab51ea2b34822443914b0f18f3d7c9a
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25407522"
---
# <a name="get-the-email-address-of-a-recipient"></a>Получение адреса электронной почты получателя

В этом примере показан способ получения SMTP-адреса получателя.

## <a name="example"></a>Пример

В следующем примере кода метод GetSMTPAddressForRecipients принимает в качестве аргумента ввода объект [MailItem](https://msdn.microsoft.com/library/bb643865\(v=office.15\)), а затем показывает SMTP-адрес каждого получателя этого почтового элемента. Метод сначала извлекает коллекцию [Recipients](https://msdn.microsoft.com/library/bb646361\(v=office.15\)), которая представляет набор получателей, указанный для почтового элемента. После этого для каждого объекта [Recipient](https://msdn.microsoft.com/library/bb624370\(v=office.15\)) в этой коллекции **Recipients** метод получает объект [PropertyAccessor](https://msdn.microsoft.com/library/bb646034\(v=office.15\)), который соответствует этому объекту **Recipient**. Наконец, метод использует свойство [PropertyAccessor](https://msdn.microsoft.com/library/bb623797\(v=office.15\)) для получения свойства MAPI https://schemas.microsoft.com/mapi/proptag/0x39FE001E, которое сопоставляется со свойством **PR\_SMTP\_ADDRESS** ([PidTagSmtpAddress](https://msdn.microsoft.com/library/cc842421\(v=office.15\))) получателя.

Если вы используете Visual Studio для тестирования этого примера кода, сначала добавьте ссылку на компонент Microsoft Outlook 15.0 Object Library и задайте переменную Outlook при импорте пространства имен **Microsoft.Office.Interop.Outlook**. Инструкция **using** не должна идти непосредственно перед функциями в примере кода, но ее нужно добавить перед открытым объявлением Class. В следующей строке кода показано, как выполнить импорт и назначение в C\#.

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```csharp
private void GetSMTPAddressForRecipients(Outlook.MailItem mail)
{
    const string PR_SMTP_ADDRESS =
        "https://schemas.microsoft.com/mapi/proptag/0x39FE001E";
    Outlook.Recipients recips = mail.Recipients;
    foreach (Outlook.Recipient recip in recips)
    {
        Outlook.PropertyAccessor pa = recip.PropertyAccessor;
        string smtpAddress =
            pa.GetProperty(PR_SMTP_ADDRESS).ToString();
        Debug.WriteLine(recip.Name + " SMTP=" + smtpAddress);
    }
}
```

## <a name="see-also"></a>См. также

- [Получатели](recipients.md)


---
title: Получение электронного адреса получателя
TOCTitle: Get the email address of a recipient
ms:assetid: e585811b-a298-496f-ba79-df7d46526169
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184647(v=office.15)
ms:contentKeyID: 55119879
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 5d145dadd974b6608da29cdf85a4624d6c452eb8
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/29/2019
ms.locfileid: "34542578"
---
# <a name="get-the-email-address-of-a-recipient"></a><span data-ttu-id="9dae3-102">Получение адреса электронной почты получателя</span><span class="sxs-lookup"><span data-stu-id="9dae3-102">Get the email address of a recipient</span></span>

<span data-ttu-id="9dae3-103">В этом примере показан способ получения SMTP-адреса получателя.</span><span class="sxs-lookup"><span data-stu-id="9dae3-103">This example shows how to get the Simple Mail Transfer Protocol (SMTP) address of a recipient.</span></span>

## <a name="example"></a><span data-ttu-id="9dae3-104">Пример</span><span class="sxs-lookup"><span data-stu-id="9dae3-104">Example</span></span>

<span data-ttu-id="9dae3-105">В следующем примере кода метод GetSMTPAddressForRecipients принимает в качестве аргумента ввода объект [MailItem](https://msdn.microsoft.com/library/bb643865\(v=office.15\)), а затем показывает SMTP-адрес каждого получателя этого почтового элемента.</span><span class="sxs-lookup"><span data-stu-id="9dae3-105">In the following the code example, the GetSMTPAddressForRecipients method takes a [MailItem](https://msdn.microsoft.com/library/bb643865\(v=office.15\)) object as an input argument and then displays the SMTP address of each recipient for that mail item.</span></span> <span data-ttu-id="9dae3-106">Метод сначала извлекает коллекцию [Recipients](https://msdn.microsoft.com/library/bb646361\(v=office.15\)), которая представляет набор получателей, указанный для почтового элемента.</span><span class="sxs-lookup"><span data-stu-id="9dae3-106">The method first retrieves the [Recipients](https://msdn.microsoft.com/library/bb646361\(v=office.15\)) collection that represents the set of recipients specified for the mail item.</span></span> <span data-ttu-id="9dae3-107">Затем метод получает для каждого [Recipient](https://msdn.microsoft.com/library/bb624370\(v=office.15\)) в коллекции **Recipients** объект [PropertyAccessor](https://msdn.microsoft.com/library/bb646034\(v=office.15\)) , который соответствует объекту **Recipient**.</span><span class="sxs-lookup"><span data-stu-id="9dae3-107">For each [Recipient](https://msdn.microsoft.com/library/bb624370\(v=office.15\)) in that **Recipients** collection, the method then obtains the [PropertyAccessor](https://msdn.microsoft.com/library/bb646034\(v=office.15\)) object that corresponds to that **Recipient** object.</span></span> <span data-ttu-id="9dae3-108">Наконец, метод использует свойство [PropertyAccessor](https://msdn.microsoft.com/library/bb623797\(v=office.15\)) , чтобы получить значение свойства http://schemas.microsoft.com/mapi/proptag/0x39FE001EMAPI, которое сопоставляется с **\_SMTP-\_адресом**([PidTagSmtpAddress](https://msdn.microsoft.com/library/cc842421\(v=office.15\))) для получателя (URL-адрес ) получателя.</span><span class="sxs-lookup"><span data-stu-id="9dae3-108">Finally, the method uses the [PropertyAccessor](https://msdn.microsoft.com/library/bb623797\(v=office.15\)) property to get the value of the MAPI property http://schemas.microsoft.com/mapi/proptag/0x39FE001E, which maps to the **PR\_SMTP\_ADDRESS** ([PidTagSmtpAddress](https://msdn.microsoft.com/library/cc842421\(v=office.15\))) property of the recipient.</span></span>

<span data-ttu-id="9dae3-109">Если вы используете Visual Studio для тестирования этого примера кода, сначала добавьте ссылку на компонент Microsoft Outlook 15.0 Object Library и задайте переменную Outlook при импорте пространства имен **Microsoft.Office.Interop.Outlook**.</span><span class="sxs-lookup"><span data-stu-id="9dae3-109">If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the Outlook variable when you import the **Microsoft.Office.Interop.Outlook** namespace.</span></span> <span data-ttu-id="9dae3-110">Инструкция **using** не должна находиться непосредственно перед функциями в примере кода, но ее нужно добавить перед объявлением общедоступного класса.</span><span class="sxs-lookup"><span data-stu-id="9dae3-110">The **using** statement must not occur directly before the functions in the code example but must be added before the public Class declaration.</span></span> <span data-ttu-id="9dae3-111">В приведенной ниже строке кода показано, как выполнить импорт и назначение на языке C\#.</span><span class="sxs-lookup"><span data-stu-id="9dae3-111">The following line of code shows how to do the import and assignment in C\#.</span></span>

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```csharp
private void GetSMTPAddressForRecipients(Outlook.MailItem mail)
{
    const string PR_SMTP_ADDRESS =
        "http://schemas.microsoft.com/mapi/proptag/0x39FE001E";
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

## <a name="see-also"></a><span data-ttu-id="9dae3-112">См. также</span><span class="sxs-lookup"><span data-stu-id="9dae3-112">See also</span></span>

- [<span data-ttu-id="9dae3-113">Получатели</span><span class="sxs-lookup"><span data-stu-id="9dae3-113">Recipients</span></span>](recipients.md)


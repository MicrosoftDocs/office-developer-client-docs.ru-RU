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
# <a name="get-the-email-address-of-a-recipient"></a><span data-ttu-id="e8065-102">Получение адреса электронной почты получателя</span><span class="sxs-lookup"><span data-stu-id="e8065-102">Gets the email address type of a recipient.</span></span>

<span data-ttu-id="e8065-103">В этом примере показан способ получения SMTP-адреса получателя.</span><span class="sxs-lookup"><span data-stu-id="e8065-103">This example shows how to get the Simple Mail Transfer Protocol (SMTP) address of a recipient.</span></span>

## <a name="example"></a><span data-ttu-id="e8065-104">Пример</span><span class="sxs-lookup"><span data-stu-id="e8065-104">Example</span></span>

<span data-ttu-id="e8065-105">В следующем примере кода метод GetSMTPAddressForRecipients принимает в качестве аргумента ввода объект [MailItem](https://msdn.microsoft.com/library/bb643865\(v=office.15\)), а затем показывает SMTP-адрес каждого получателя этого почтового элемента.</span><span class="sxs-lookup"><span data-stu-id="e8065-105">In the following the code example, the   method takes a MailItem object as an input argument and then displays the SMTP address of each recipient for that mail item.</span></span> <span data-ttu-id="e8065-106">Метод сначала извлекает коллекцию [Recipients](https://msdn.microsoft.com/library/bb646361\(v=office.15\)), которая представляет набор получателей, указанный для почтового элемента.</span><span class="sxs-lookup"><span data-stu-id="e8065-106">The method first retrieves the [Recipients](https://msdn.microsoft.com/library/bb646361\(v=office.15\)) collection that represents the set of recipients specified for the mail item.</span></span> <span data-ttu-id="e8065-107">После этого для каждого объекта [Recipient](https://msdn.microsoft.com/library/bb624370\(v=office.15\)) в этой коллекции **Recipients** метод получает объект [PropertyAccessor](https://msdn.microsoft.com/library/bb646034\(v=office.15\)), который соответствует этому объекту **Recipient**.</span><span class="sxs-lookup"><span data-stu-id="e8065-107">For each [Recipient](https://msdn.microsoft.com/library/bb624370\(v=office.15\)) in that **Recipients** collection, the method then obtains the [PropertyAccessor](https://msdn.microsoft.com/library/bb646034\(v=office.15\)) object that corresponds to that **Recipient** object.</span></span> <span data-ttu-id="e8065-108">Наконец, метод использует свойство [PropertyAccessor](https://msdn.microsoft.com/library/bb623797\(v=office.15\)) для получения свойства MAPI https://schemas.microsoft.com/mapi/proptag/0x39FE001E, которое сопоставляется со свойством **PR\_SMTP\_ADDRESS** ([PidTagSmtpAddress](https://msdn.microsoft.com/library/cc842421\(v=office.15\))) получателя.</span><span class="sxs-lookup"><span data-stu-id="e8065-108">Finally, the method uses the PropertyAccessor property to get the value of the MAPI property  , which maps to the PR_SMTP_ADDRESS ( PidTagSmtpAddress) property of the recipient.</span></span>

<span data-ttu-id="e8065-109">Если вы используете Visual Studio для тестирования этого примера кода, сначала добавьте ссылку на компонент Microsoft Outlook 15.0 Object Library и задайте переменную Outlook при импорте пространства имен **Microsoft.Office.Interop.Outlook**.</span><span class="sxs-lookup"><span data-stu-id="e8065-109">If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the   variable when you import the Microsoft.Office.Interop.Outlook namespace.</span></span> <span data-ttu-id="e8065-110">Инструкция **using** не должна идти непосредственно перед функциями в примере кода, но ее нужно добавить перед открытым объявлением Class.</span><span class="sxs-lookup"><span data-stu-id="e8065-110">The using statement must not occur directly before the functions in the code example but must be added before the public   declaration.</span></span> <span data-ttu-id="e8065-111">В следующей строке кода показано, как выполнить импорт и назначение в C\#.</span><span class="sxs-lookup"><span data-stu-id="e8065-111">The following line of code shows how to do the import and assignment in C#.</span></span>

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

## <a name="see-also"></a><span data-ttu-id="e8065-112">См. также</span><span class="sxs-lookup"><span data-stu-id="e8065-112">See also</span></span>

- [<span data-ttu-id="e8065-113">Получатели</span><span class="sxs-lookup"><span data-stu-id="e8065-113">Recipients</span></span>](recipients.md)


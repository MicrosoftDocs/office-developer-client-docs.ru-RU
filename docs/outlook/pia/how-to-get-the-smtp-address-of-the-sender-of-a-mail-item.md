---
title: Получение SMTP-адреса отправителя почтового элемента
TOCTitle: Get the SMTP address of the sender of a mail item
ms:assetid: 86e0c0aa-1696-4415-b25f-f9c1c29d88a9
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184624(v=office.15)
ms:contentKeyID: 55119869
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Priority
ms.openlocfilehash: 74adbf02180e0e993b22e35481f51d304b14e7d6
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28712486"
---
# <a name="get-the-smtp-address-of-the-sender-of-a-mail-item"></a><span data-ttu-id="3650e-102">Получение SMTP-адреса отправителя почтового элемента</span><span class="sxs-lookup"><span data-stu-id="3650e-102">Get the SMTP address of the sender of a mail item</span></span>

<span data-ttu-id="3650e-103">В этом примере выполняется получение SMTP-адреса отправителя для почтового элемента.</span><span class="sxs-lookup"><span data-stu-id="3650e-103">This example gets the sender’s Simple Mail Transfer Protocol (SMTP) address for a mail item.</span></span>

## <a name="example"></a><span data-ttu-id="3650e-104">Пример</span><span class="sxs-lookup"><span data-stu-id="3650e-104">Example</span></span>

<span data-ttu-id="3650e-105">Чтобы определить SMTP-адрес полученного почтового элемента, используйте свойство [SenderEmailAddress](https://msdn.microsoft.com/library/bb622746\(v=office.15\)) объекта [MailItem](https://msdn.microsoft.com/library/bb643865\(v=office.15\)).</span><span class="sxs-lookup"><span data-stu-id="3650e-105">To determine the SMTP address for a received mail item, use the [SenderEmailAddress](https://msdn.microsoft.com/library/bb622746\(v=office.15\)) property of the [MailItem](https://msdn.microsoft.com/library/bb643865\(v=office.15\)) object.</span></span> <span data-ttu-id="3650e-106">Однако если отправитель сообщения находится внутри организации, свойство **SenderEmailAddress** не возвращает SMTP-адрес. В этом случае необходимо использовать объект [PropertyAccessor](https://msdn.microsoft.com/library/bb646034\(v=office.15\)).</span><span class="sxs-lookup"><span data-stu-id="3650e-106">However, if the sender is internal to your organization, **SenderEmailAddress** does not return an SMTP address, and you must use the [PropertyAccessor](https://msdn.microsoft.com/library/bb646034\(v=office.15\)) object to return the sender’s SMTP address.</span></span>

<span data-ttu-id="3650e-107">В следующем примере кода метод GetSenderSMTPAddress использует объект **PropertyAccessor** для получения значений, которые не предоставляются явно в объектной модели приложения Outlook.</span><span class="sxs-lookup"><span data-stu-id="3650e-107">In the following code example, GetSenderSMTPAddress uses the **PropertyAccessor** object to obtain values that are not exposed directly in the Outlook object model.</span></span> <span data-ttu-id="3650e-108">Метод GetSenderSMTPAddress получает объект **MailItem**.</span><span class="sxs-lookup"><span data-stu-id="3650e-108">GetSenderSMTPAddress takes in a **MailItem**.</span></span> <span data-ttu-id="3650e-109">Если свойство [SenderEmailType](https://msdn.microsoft.com/library/bb624136\(v=office.15\)) полученного объекта **MailItem** имеет значение "EX", отправитель сообщения размещается на сервере Exchange в организации.</span><span class="sxs-lookup"><span data-stu-id="3650e-109">If the value of the [SenderEmailType](https://msdn.microsoft.com/library/bb624136\(v=office.15\)) property of the received **MailItem** is "EX", the sender of the message resides on an Exchange server in your organization.</span></span> <span data-ttu-id="3650e-110">Метод GetSenderSMTPAddress использует свойство [Sender](https://msdn.microsoft.com/library/ff184720\(v=office.15\)) объекта **MailItem** для получения отправителя, представленного объектом [AddressEntry](https://msdn.microsoft.com/library/bb609728\(v=office.15\)).</span><span class="sxs-lookup"><span data-stu-id="3650e-110">GetSenderSMTPAddress uses the [Sender](https://msdn.microsoft.com/library/ff184720\(v=office.15\)) property of the **MailItem** object to get the sender, represented by the [AddressEntry](https://msdn.microsoft.com/library/bb609728\(v=office.15\)) object.</span></span> <span data-ttu-id="3650e-111">Если объект **AddressEntry** представляет пользователя Exchange, в этом примере вызывается метод [GetExchangeUser()](https://msdn.microsoft.com/library/bb611808\(v=office.15\)), который возвращает объект [ExchangeUser](https://msdn.microsoft.com/library/bb609574\(v=office.15\)) объекта **AddressEntry**.</span><span class="sxs-lookup"><span data-stu-id="3650e-111">If the **AddressEntry** object represents an Exchange user, the example calls the [GetExchangeUser()](https://msdn.microsoft.com/library/bb611808\(v=office.15\)) method to return the [ExchangeUser](https://msdn.microsoft.com/library/bb609574\(v=office.15\)) object of the **AddressEntry** object.</span></span> <span data-ttu-id="3650e-112">После этого метод GetSenderSMTPAddress использует свойство [PrimarySmtpAddress](https://msdn.microsoft.com/library/bb645506\(v=office.15\)) объекта **ExchangeUser**, которое возвращает SMTP-адрес отправителя.</span><span class="sxs-lookup"><span data-stu-id="3650e-112">GetSenderSMTPAddress then uses the [PrimarySmtpAddress](https://msdn.microsoft.com/library/bb645506\(v=office.15\)) property of the **ExchangeUser** object to return the SMTP address of the sender.</span></span> <span data-ttu-id="3650e-113">Если объект **AddressEntry** для отправителя не представляет объект **ExchangeUser**, для получения SMTP-адреса отправителя используется метод [GetProperty(String)](https://msdn.microsoft.com/library/bb645726\(v=office.15\)) объекта **PropertyAccessor** с аргументом **PR\_SMTP\_ADDRESS** ([PidTagSmtpAddress](https://msdn.microsoft.com/library/cc842421\(v=office.15\))).</span><span class="sxs-lookup"><span data-stu-id="3650e-113">If the **AddressEntry** object for the sender does not represent an **ExchangeUser** object, the [GetProperty(String)](https://msdn.microsoft.com/library/bb645726\(v=office.15\)) method of the **PropertyAccessor** object is used, with **PR\_SMTP\_ADDRESS** ([PidTagSmtpAddress](https://msdn.microsoft.com/library/cc842421\(v=office.15\))) as the argument, to return the sender’s SMTP address.</span></span>

<span data-ttu-id="3650e-114">Если вы используете Visual Studio для тестирования этого примера кода, сначала добавьте ссылку на компонент Microsoft Outlook 15.0 Object Library и задайте переменную Outlook при импорте пространства имен **Microsoft.Office.Interop.Outlook**.</span><span class="sxs-lookup"><span data-stu-id="3650e-114">If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the Outlook variable when you import the **Microsoft.Office.Interop.Outlook** namespace.</span></span> <span data-ttu-id="3650e-115">Инструкция **using** не должна идти непосредственно перед функциями в примере кода, но ее нужно добавить перед открытым объявлением Class.</span><span class="sxs-lookup"><span data-stu-id="3650e-115">The **using** statement must not occur directly before the functions in the code example but must be added before the public Class declaration.</span></span> <span data-ttu-id="3650e-116">В следующей строке кода показано, как выполнить импорт и назначение в C\#.</span><span class="sxs-lookup"><span data-stu-id="3650e-116">The following line of code shows how to do the import and assignment in C\#.</span></span>

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```csharp
private string GetSenderSMTPAddress(Outlook.MailItem mail)
{
    string PR_SMTP_ADDRESS =
        @"https://schemas.microsoft.com/mapi/proptag/0x39FE001E";
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

## <a name="see-also"></a><span data-ttu-id="3650e-117">См. также</span><span class="sxs-lookup"><span data-stu-id="3650e-117">See also</span></span>

- [<span data-ttu-id="3650e-118">Почта</span><span class="sxs-lookup"><span data-stu-id="3650e-118">Mail</span></span>](mail.md)


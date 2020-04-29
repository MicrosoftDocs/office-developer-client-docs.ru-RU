---
title: Отправка почтового элемента с помощью учетной записи Hotmail
TOCTitle: Send a mail item by using a Hotmail account
ms:assetid: f25853a7-67c0-46a3-a298-5cdf72ebc53f
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184652(v=office.15)
ms:contentKeyID: 55119797
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 008f66ff1a43f90e756900c467ba6c086829b769
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32331166"
---
# <a name="send-a-mail-item-by-using-a-hotmail-account"></a><span data-ttu-id="fec94-102">Отправка почтового элемента с помощью учетной записи Hotmail</span><span class="sxs-lookup"><span data-stu-id="fec94-102">Send a mail item by using a Hotmail account</span></span>

<span data-ttu-id="fec94-103">В этом примере используется свойство [SendUsingAccount](https://msdn.microsoft.com/library/bb623679\(v=office.15\)) для отправки почтового элемента с помощью учетной записи Windows Live Hotmail.</span><span class="sxs-lookup"><span data-stu-id="fec94-103">This example uses the [SendUsingAccount](https://msdn.microsoft.com/library/bb623679\(v=office.15\)) property to send a mail item by using a Windows Live Hotmail account.</span></span>

## <a name="example"></a><span data-ttu-id="fec94-104">Пример</span><span class="sxs-lookup"><span data-stu-id="fec94-104">Example</span></span>

> [!NOTE] 
> <span data-ttu-id="fec94-105">Приведенный ниже пример кода взят из книги [Программирование приложений для Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).</span><span class="sxs-lookup"><span data-stu-id="fec94-105">The following code example is an excerpt from [Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).</span></span>

<span data-ttu-id="fec94-106">Профиль определяет одну или несколько учетных записей электронной почты, а каждая такая учетная запись связана с сервером определенного типа (например, с сервером Microsoft Exchange Server или сервером POP3).</span><span class="sxs-lookup"><span data-stu-id="fec94-106">A profile defines one or more email accounts, and each email account is associated with a server of a specific type, such as Microsoft Exchange Server or Post Office Protocol 3 (POP3).</span></span> <span data-ttu-id="fec94-107">Поскольку в вашем профиле может находиться несколько учетных записей, необходимо указать используемую для отправки элемента учетную запись электронной почты, а затем получить представляющий ее объект [Account](https://msdn.microsoft.com/library/bb645103\(v=office.15\)).</span><span class="sxs-lookup"><span data-stu-id="fec94-107">Because you may have multiple accounts in your profile, you must specify which email account you want to use to send the item, and then obtain an [Account](https://msdn.microsoft.com/library/bb645103\(v=office.15\)) object to represent it.</span></span>

<span data-ttu-id="fec94-108">В представленном ниже примере кода сообщение создается с вложенным маршрутом и затем отправляется с помощью учетной записи Windows Live Hotmail.</span><span class="sxs-lookup"><span data-stu-id="fec94-108">In the following code example, a message is created with an attached itinerary and then sent by using a Windows Live Hotmail account.</span></span> <span data-ttu-id="fec94-109">Учетная запись Hotmail применяется в качестве объекта **Account** в профиле пользователя.</span><span class="sxs-lookup"><span data-stu-id="fec94-109">The Hotmail email account is used as the **Account** object in the user’s profile.</span></span> <span data-ttu-id="fec94-110">Затем в примере кода для свойства SendUsingAccount задается этот объект Account и вызывается метод [Send()](https://msdn.microsoft.com/library/bb644139\(v=office.15\)) из объекта [MailItem](https://msdn.microsoft.com/library/bb643865\(v=office.15\)).</span><span class="sxs-lookup"><span data-stu-id="fec94-110">The code example then sets the SendUsingAccount property to that Account and calls the [Send()](https://msdn.microsoft.com/library/bb644139\(v=office.15\)) method from the [MailItem](https://msdn.microsoft.com/library/bb643865\(v=office.15\)) object.</span></span>

<span data-ttu-id="fec94-111">Если вы используете Visual Studio для тестирования этого примера кода, сначала добавьте ссылку на компонент Microsoft Outlook 15.0 Object Library и задайте переменную Outlook при импорте пространства имен **Microsoft.Office.Interop.Outlook**.</span><span class="sxs-lookup"><span data-stu-id="fec94-111">If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the Outlook variable when you import the **Microsoft.Office.Interop.Outlook** namespace.</span></span> <span data-ttu-id="fec94-112">Инструкция **using** не должна находиться непосредственно перед функциями в примере кода, но ее нужно добавить перед объявлением общедоступного класса.</span><span class="sxs-lookup"><span data-stu-id="fec94-112">The **using** statement must not occur directly before the functions in the code example but must be added before the public Class declaration.</span></span> <span data-ttu-id="fec94-113">В приведенной ниже строке кода показано, как выполнить импорт и назначение на языке C\#.</span><span class="sxs-lookup"><span data-stu-id="fec94-113">The following line of code shows how to do the import and assignment in C\#.</span></span>

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```

```csharp
private void SendUsingAccountExample()
{
    Outlook.MailItem mail = Application.CreateItem(
        Outlook.OlItemType.olMailItem) as Outlook.MailItem;
    mail.Subject = "Our itinerary";
    mail.Attachments.Add(@"c:\travel\itinerary.doc",
        Outlook.OlAttachmentType.olByValue,
        Type.Missing, Type.Missing);
    Outlook.Account account =
        Application.Session.Accounts["Hotmail"];
    mail.SendUsingAccount = account;
    mail.Send();
}
```

## <a name="see-also"></a><span data-ttu-id="fec94-114">См. также</span><span class="sxs-lookup"><span data-stu-id="fec94-114">See also</span></span>

- [<span data-ttu-id="fec94-115">Учетные записи</span><span class="sxs-lookup"><span data-stu-id="fec94-115">Accounts</span></span>](accounts.md)


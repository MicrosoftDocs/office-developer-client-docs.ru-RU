---
title: Задание разных типов получателей для почтового элемента
TOCTitle: Specify different recipient types for a mail item
ms:assetid: 2a3ace9f-627c-4fdd-b182-afc1b53af85b
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184598(v=office.15)
ms:contentKeyID: 55119871
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: bf61a7fbb470291eae448a93c80866112c41407a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32335513"
---
# <a name="specify-different-recipient-types-for-a-mail-item"></a><span data-ttu-id="63983-102">Задание разных типов получателей для почтового элемента</span><span class="sxs-lookup"><span data-stu-id="63983-102">Specify different recipient types for a mail item</span></span>

<span data-ttu-id="63983-103">В этом примере показано, как программно задать разные типы получателей ("Кому", "Копия" или "СК") для почтового элемента.</span><span class="sxs-lookup"><span data-stu-id="63983-103">This example shows how to programmatically set different recipient types (To, Cc, or Bcc) for a mail item.</span></span>

## <a name="example"></a><span data-ttu-id="63983-104">Пример</span><span class="sxs-lookup"><span data-stu-id="63983-104">Example</span></span>

> [!NOTE] 
> <span data-ttu-id="63983-105">Приведенный ниже пример кода представляет собой фрагмент из книги [Программирование приложений для Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).</span><span class="sxs-lookup"><span data-stu-id="63983-105">The following code example is an excerpt from [Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).</span></span>

<span data-ttu-id="63983-106">В примере кода ниже показано, как указать, к какому типу ("Кому", "Копия" или "СК") относится получатель объекта [MailItem](https://msdn.microsoft.com/library/bb643865\(v=office.15\)).</span><span class="sxs-lookup"><span data-stu-id="63983-106">The following code example illustrates how to specify whether a recipient of a [MailItem](https://msdn.microsoft.com/library/bb643865\(v=office.15\)) object is a To, Cc, or Bcc recipient.</span></span> <span data-ttu-id="63983-107">SetRecipientTypeForMail создает объект **MailItem**, добавляет три объекта [Recipient](https://msdn.microsoft.com/library/bb624370\(v=office.15\)) в коллекцию [Recipients](https://msdn.microsoft.com/library/bb646361\(v=office.15\)) элемента **MailItem**, а затем для свойства [Type](https://msdn.microsoft.com/library/bb611841\(v=office.15\)) каждого объекта **Recipient** задает значение из перечисления [OlMailRecipientType](https://msdn.microsoft.com/library/bb647641\(v=office.15\)).</span><span class="sxs-lookup"><span data-stu-id="63983-107">SetRecipientTypeForMail creates a **MailItem** object, adds three [Recipient](https://msdn.microsoft.com/library/bb624370\(v=office.15\)) objects to the [Recipients](https://msdn.microsoft.com/library/bb646361\(v=office.15\)) collection of the **MailItem**, and then sets the [Type](https://msdn.microsoft.com/library/bb611841\(v=office.15\)) property of each **Recipient** object to a value from the [OlMailRecipientType](https://msdn.microsoft.com/library/bb647641\(v=office.15\)) enumeration.</span></span>


> [!NOTE]
> <span data-ttu-id="63983-108">Свойство **Type** объекта **Recipient** относится к типу int и не соответствует конкретному перечислению типов получателей.</span><span class="sxs-lookup"><span data-stu-id="63983-108">The **Type** property of the **Recipient** object is an int type and does not correlate to a specific recipient type enumeration.</span></span>

<span data-ttu-id="63983-109">Если вы используете Visual Studio для тестирования этого примера кода, сначала добавьте ссылку на компонент Microsoft Outlook 15.0 Object Library и задайте переменную Outlook при импорте пространства имен **Microsoft.Office.Interop.Outlook**.</span><span class="sxs-lookup"><span data-stu-id="63983-109">If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the Outlook variable when you import the **Microsoft.Office.Interop.Outlook** namespace.</span></span> <span data-ttu-id="63983-110">Инструкция **using** не должна находиться непосредственно перед функциями в примере кода, но ее нужно добавить перед объявлением общедоступного класса.</span><span class="sxs-lookup"><span data-stu-id="63983-110">The **using** statement must not occur directly before the functions in the code example but must be added before the public Class declaration.</span></span> <span data-ttu-id="63983-111">В приведенной ниже строке кода показано, как выполнить импорт и назначение на языке C\#.</span><span class="sxs-lookup"><span data-stu-id="63983-111">The following line of code shows how to do the import and assignment in C\#.</span></span>

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```csharp
private void SetRecipientTypeForMail()
{
    Outlook.MailItem mail = Application.CreateItem(
        Outlook.OlItemType.olMailItem) as Outlook.MailItem;
    mail.Subject = "Sample Message";
    Outlook.Recipient recipTo =
        mail.Recipients.Add("someone@example.com");
    recipTo.Type = (int)Outlook.OlMailRecipientType.olTo;
    Outlook.Recipient recipCc =
        mail.Recipients.Add("someonecc@example.com");
    recipCc.Type = (int)Outlook.OlMailRecipientType.olCC;
    Outlook.Recipient recipBcc =
        mail.Recipients.Add("someonebcc@example.com");
    recipBcc.Type = (int)Outlook.OlMailRecipientType.olBCC;
    mail.Recipients.ResolveAll();
    mail.Display(false);
}
```

## <a name="see-also"></a><span data-ttu-id="63983-112">См. также</span><span class="sxs-lookup"><span data-stu-id="63983-112">See also</span></span>

- [<span data-ttu-id="63983-113">Почта</span><span class="sxs-lookup"><span data-stu-id="63983-113">Mail</span></span>](mail.md)


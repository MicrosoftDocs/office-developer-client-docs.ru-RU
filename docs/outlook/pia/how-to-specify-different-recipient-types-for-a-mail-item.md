---
title: Задание разных типов получателей для почтового элемента
TOCTitle: Specify different recipient types for a mail item
ms:assetid: 2a3ace9f-627c-4fdd-b182-afc1b53af85b
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184598(v=office.15)
ms:contentKeyID: 55119871
ms.date: 07/24/2014
mtps_version: v=office.15
ms.openlocfilehash: 9eca70f9c1b77e8430625fb49e3ae9787d337ba7
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25405534"
---
# <a name="specify-different-recipient-types-for-a-mail-item"></a><span data-ttu-id="621cd-102">Задание разных типов получателей для почтового элемента</span><span class="sxs-lookup"><span data-stu-id="621cd-102">Specify different recipient types for a mail item</span></span>

<span data-ttu-id="621cd-103">В этом примере показано, как программно задать разные типы получателей ("Кому", "Копия" или "СК") для почтового элемента.</span><span class="sxs-lookup"><span data-stu-id="621cd-103">This example shows how to programmatically set different recipient types (To, Cc, or Bcc) for a mail item.</span></span>

## <a name="example"></a><span data-ttu-id="621cd-104">Пример</span><span class="sxs-lookup"><span data-stu-id="621cd-104">Example</span></span>

> [!NOTE] 
> <span data-ttu-id="621cd-105">Приведенный ниже пример кода представляет собой фрагмент из книги [Программирование приложений для Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).</span><span class="sxs-lookup"><span data-stu-id="621cd-105">The following code example is an excerpt from  [Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493)  , from Microsoft Press (ISBN 9780735622494, copyright Microsoft Press 2007, all rights reserved).</span></span>

<span data-ttu-id="621cd-106">В примере кода ниже показано, как указать, к какому типу ("Кому", "Копия" или "СК") относится получатель объекта [MailItem](https://msdn.microsoft.com/library/bb643865\(v=office.15\)).</span><span class="sxs-lookup"><span data-stu-id="621cd-106">The following code example illustrates how to specify whether a recipient of a [MailItem](https://msdn.microsoft.com/library/bb643865\(v=office.15\)) object is a To, Cc, or Bcc recipient.</span></span> <span data-ttu-id="621cd-107">SetRecipientTypeForMail создает объект **MailItem**, добавляет три объекта [Recipient](https://msdn.microsoft.com/library/bb624370\(v=office.15\)) в коллекцию [Recipients](https://msdn.microsoft.com/library/bb646361\(v=office.15\)) элемента **MailItem**, а затем для свойства [Type](https://msdn.microsoft.com/library/bb611841\(v=office.15\)) каждого объекта **Recipient** задает значение из перечисления [OlMailRecipientType](https://msdn.microsoft.com/library/bb647641\(v=office.15\)).</span><span class="sxs-lookup"><span data-stu-id="621cd-107"> creates a MailItem object, adds three Recipient objects to the Recipients collection of the MailItem, and then sets the Type property of each Recipient object to a value from the OlMailRecipientType enumeration.</span></span>


> [!NOTE]
> <span data-ttu-id="621cd-108">Свойство **Type** объекта **Recipient** относится к типу int и не соответствует конкретному перечислению типов получателей.</span><span class="sxs-lookup"><span data-stu-id="621cd-108">The **Type** property of the **Recipient** object is an int type and does not correlate to a specific recipient type enumeration.</span></span>

<span data-ttu-id="621cd-109">Если вы используете Visual Studio для тестирования этого примера кода, сначала добавьте ссылку на компонент Microsoft Outlook 15.0 Object Library и задайте переменную Outlook при импорте пространства имен **Microsoft.Office.Interop.Outlook**.</span><span class="sxs-lookup"><span data-stu-id="621cd-109">If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the   variable when you import the Microsoft.Office.Interop.Outlook namespace.</span></span> <span data-ttu-id="621cd-110">Инструкция **using** не должна идти непосредственно перед функциями в примере кода, но ее нужно добавить перед открытым объявлением Class.</span><span class="sxs-lookup"><span data-stu-id="621cd-110">The using statement must not occur directly before the functions in the code example but must be added before the public   declaration.</span></span> <span data-ttu-id="621cd-111">В следующей строке кода показано, как выполнить импорт и назначение в C\#.</span><span class="sxs-lookup"><span data-stu-id="621cd-111">The following line of code shows how to do the import and assignment in C#.</span></span>

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

## <a name="see-also"></a><span data-ttu-id="621cd-112">См. также</span><span class="sxs-lookup"><span data-stu-id="621cd-112">See also</span></span>

- [<span data-ttu-id="621cd-113">Почта</span><span class="sxs-lookup"><span data-stu-id="621cd-113">Mail</span></span>](mail.md)


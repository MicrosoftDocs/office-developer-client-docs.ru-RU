---
title: Добавление параметров голосования в почтовый элемент
TOCTitle: Add voting options to a mail item
ms:assetid: 0fb209a8-178d-411e-9551-0a72e041fd65
ms:mtpsurl: https://msdn.microsoft.com/library/Ff424466(v=office.15)
ms:contentKeyID: 55119867
ms.date: 07/24/2014
mtps_version: v=office.15
ms.openlocfilehash: 6a65bdd5086a10b2d6e9803047555a8b052ff38e
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25407172"
---
# <a name="add-voting-options-to-a-mail-item"></a><span data-ttu-id="d7d76-102">Добавление параметров голосования в почтовый элемент</span><span class="sxs-lookup"><span data-stu-id="d7d76-102">Add voting options to a mail item</span></span>

<span data-ttu-id="d7d76-103">В этом примере показано, как использовать свойство [VotingOptions](https://msdn.microsoft.com/library/bb652695\(v=office.15\)) объекта [MailItem](https://msdn.microsoft.com/library/bb643865\(v=office.15\)), чтобы добавить параметры голосования в сообщение электронной почты.</span><span class="sxs-lookup"><span data-stu-id="d7d76-103">This example shows how to use the [P:Microsoft.Office.Interop.Outlook._MailItem.VotingOptions](https://msdn.microsoft.com/library/bb652695\(v=office.15\)) property of the [T:Microsoft.Office.Interop.Outlook.MailItem](https://msdn.microsoft.com/library/bb643865\(v=office.15\)) object to add voting options to an e-mail message.</span></span>

## <a name="example"></a><span data-ttu-id="d7d76-104">Пример</span><span class="sxs-lookup"><span data-stu-id="d7d76-104">Example</span></span>

> [!NOTE] 
> <span data-ttu-id="d7d76-105">Приведенный ниже пример кода представляет собой фрагмент из книги [Программирование приложений для Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).</span><span class="sxs-lookup"><span data-stu-id="d7d76-105">The following code example is an excerpt from  [Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493)  , from Microsoft Press (ISBN 9780735622494, copyright Microsoft Press 2007, all rights reserved).</span></span>


<span data-ttu-id="d7d76-p101">Параметры голосования в сообщениях используются для предоставления получателям сообщения списка вариантов ответа и отслеживания ответов. Чтобы программно создать параметры голосования, следует задать для свойства **VotingOptions** объекта **MailItem** строковое значение, содержащее разделенный точками с запятыми список значений. Значения для свойства **VotingOptions** будут появляться под командой **Голосование** в группе **Ответить** ленты полученных сообщений. </span><span class="sxs-lookup"><span data-stu-id="d7d76-p101">Voting options on messages are used to give message recipients a list of choices and to track their responses. To create voting options programmatically, set a string that is a semicolon-delimited list of values for the **VotingOptions** property of a **MailItem** object. The values for the **VotingOptions** property will appear under the **Vote** command in the **Respond** group in the ribbon of the received message.</span></span>

<span data-ttu-id="d7d76-109">В приведенном ниже примере OrderPizza создает параметры голосования в новом сообщении электронной почты.</span><span class="sxs-lookup"><span data-stu-id="d7d76-109">In the following example, OrderPizza creates voting options in a new mail message.</span></span> <span data-ttu-id="d7d76-110">OrderPizza сначала создает объект **MailItem**, затем устанавливает свойство **VotingOptions** равным "Cheese; Mushroom; Sausage; Combo; Veg Combo", а свойство [Subject](https://msdn.microsoft.com/library/bb611353\(v=office.15\)) равным "Pizza Order".</span><span class="sxs-lookup"><span data-stu-id="d7d76-110">OrderPizza first creates a **MailItem**, and then sets the **VotingOptions** property to “Cheese; Mushroom; Sausage; Combo; Veg Combo”, and the [Subject](https://msdn.microsoft.com/library/bb611353\(v=office.15\)) property to “Pizza Order”.</span></span> <span data-ttu-id="d7d76-111">При отправке сообщения "Pizza Order" параметры голосования отображаются для получателей.</span><span class="sxs-lookup"><span data-stu-id="d7d76-111">When the “Pizza Order” message is sent, the voting options appear to recipients.</span></span> <span data-ttu-id="d7d76-112">Выбор получателя в каждом полученном ответе регистрируется на странице **Отслеживание** сообщения в папке отправителя "Отправленные".</span><span class="sxs-lookup"><span data-stu-id="d7d76-112">For each response received, the recipient’s choice will be tallied on the **Tracking** page of the message in the sender’s Sent Items folder.</span></span>

<span data-ttu-id="d7d76-113">Если вы используете Visual Studio для тестирования этого примера кода, сначала добавьте ссылку на компонент Microsoft Outlook 15.0 Object Library и задайте переменную Outlook при импорте пространства имен **Microsoft.Office.Interop.Outlook**.</span><span class="sxs-lookup"><span data-stu-id="d7d76-113">If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the   variable when you import the Microsoft.Office.Interop.Outlook namespace.</span></span> <span data-ttu-id="d7d76-114">Инструкция **using** не должна идти непосредственно перед функциями в примере кода, но ее нужно добавить перед открытым объявлением Class.</span><span class="sxs-lookup"><span data-stu-id="d7d76-114">The using statement must not occur directly before the functions in the code example but must be added before the public   declaration.</span></span> <span data-ttu-id="d7d76-115">В следующей строке кода показано, как выполнить импорт и назначение в C\#.</span><span class="sxs-lookup"><span data-stu-id="d7d76-115">The following line of code shows how to do the import and assignment in C#.</span></span>

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;

    private void OrderPizza()
    {
        Outlook.MailItem mail = (Outlook.MailItem)Application.CreateItem(
            Outlook.OlItemType.olMailItem);
        mail.VotingOptions = “Cheese; Mushroom; Sausage; Combo; Veg Combo;”
        mail.Subject = “Pizza Order”;
        mail.Display(false);
    }
```

## <a name="see-also"></a><span data-ttu-id="d7d76-116">См. также</span><span class="sxs-lookup"><span data-stu-id="d7d76-116">See also</span></span>

- [<span data-ttu-id="d7d76-117">Почта</span><span class="sxs-lookup"><span data-stu-id="d7d76-117">Mail</span></span>](mail.md)


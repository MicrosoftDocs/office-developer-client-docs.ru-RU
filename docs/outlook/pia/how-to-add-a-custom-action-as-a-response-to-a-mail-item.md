---
title: Добавление настраиваемого действия в качестве ответа на почтовый элемент
TOCTitle: Add a custom action as a response to a mail item
ms:assetid: 99e8ba6b-9c47-4b10-968b-436b08d199ec
ms:mtpsurl: https://msdn.microsoft.com/library/Ff424474(v=office.15)
ms:contentKeyID: 55119870
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: a6a82b02d357f86ca37d3ec4987ea6323d6d59cb
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359754"
---
# <a name="add-a-custom-action-as-a-response-to-a-mail-item"></a><span data-ttu-id="9c2b0-102">Добавление настраиваемого действия в качестве ответа на почтовый элемент</span><span class="sxs-lookup"><span data-stu-id="9c2b0-102">Add a custom action as a response to a mail item</span></span>

<span data-ttu-id="9c2b0-103">В этом примере показано добавление настраиваемых действий в виде ответа на сообщение электронной почты с помощью метода [Add()](https://msdn.microsoft.com/library/bb612077\(v=office.15\)) коллекции [Actions](https://msdn.microsoft.com/library/bb611963\(v=office.15\)).</span><span class="sxs-lookup"><span data-stu-id="9c2b0-103">This example shows how to add custom actions as a response to an email item by using the [Add()](https://msdn.microsoft.com/library/bb612077\(v=office.15\)) method of the [Actions](https://msdn.microsoft.com/library/bb611963\(v=office.15\)) collection.</span></span>

## <a name="example"></a><span data-ttu-id="9c2b0-104">Пример</span><span class="sxs-lookup"><span data-stu-id="9c2b0-104">Example</span></span>

> [!NOTE] 
> <span data-ttu-id="9c2b0-105">Приведенный ниже пример кода представляет собой фрагмент из книги [Программирование приложений для Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).</span><span class="sxs-lookup"><span data-stu-id="9c2b0-105">The following code example is an excerpt from [Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).</span></span>


<span data-ttu-id="9c2b0-106">Можно программным способом создать настраиваемые действия, которые будут отображаться на ленте в группе **Действия** вкладки **Сообщение** в ответе на сообщение электронной почты.</span><span class="sxs-lookup"><span data-stu-id="9c2b0-106">You can create custom actions programmatically to appear on the ribbon in the **Actions** group on the **Message** tab in an email response.</span></span> <span data-ttu-id="9c2b0-107">В следующем примере кода в процедуре ReplyWithVoiceMail создается настраиваемое действие "Reply with Voice Mail" (Ответить по голосовой почте), которое добавляется в панель команд инспектора.</span><span class="sxs-lookup"><span data-stu-id="9c2b0-107">In the following code example, ReplyWithVoiceMail creates and adds a custom action named “Reply with Voice Mail” to the inspector command bar.</span></span> <span data-ttu-id="9c2b0-108">В процедуре ReplyWithVoiceMail сначала получается объект [\_MailItem](https://msdn.microsoft.com/library/bb610623\(v=office.15\)), а затем создается объект [Action](https://msdn.microsoft.com/library/bb646971\(v=office.15\)) с помощью метода **Add** коллекции **Actions**, связанной с элементом **MailItem**.</span><span class="sxs-lookup"><span data-stu-id="9c2b0-108">ReplyWithVoiceMail first gets a [\_MailItem](https://msdn.microsoft.com/library/bb610623\(v=office.15\)) object and then creates an [Action](https://msdn.microsoft.com/library/bb646971\(v=office.15\)) object by calling the **Add** method of the **Actions** collection that is associated with the **MailItem**.</span></span> <span data-ttu-id="9c2b0-109">После этого свойству [Name](https://msdn.microsoft.com/library/bb624053\(v=office.15\)) объекта **Action** присваивается значение "Reply with Voice Mail".</span><span class="sxs-lookup"><span data-stu-id="9c2b0-109">It then sets the [Name](https://msdn.microsoft.com/library/bb624053\(v=office.15\)) property of the **Action** object to “Reply with Voice Mail”.</span></span> <span data-ttu-id="9c2b0-110">Также задаются свойства [ReplyStyle](https://msdn.microsoft.com/library/bb624278\(v=office.15\)), [ResponseStyle](https://msdn.microsoft.com/library/bb622491\(v=office.15\)), [CopyLike](https://msdn.microsoft.com/library/bb624213\(v=office.15\)) и [MessageClass](https://msdn.microsoft.com/library/bb624391\(v=office.15\)).</span><span class="sxs-lookup"><span data-stu-id="9c2b0-110">The [ReplyStyle](https://msdn.microsoft.com/library/bb624278\(v=office.15\)), [ResponseStyle](https://msdn.microsoft.com/library/bb622491\(v=office.15\)), [CopyLike](https://msdn.microsoft.com/library/bb624213\(v=office.15\)), and [MessageClass](https://msdn.microsoft.com/library/bb624391\(v=office.15\)) properties are also set.</span></span> <span data-ttu-id="9c2b0-111">В конце элемент **MailItem** сохраняется.</span><span class="sxs-lookup"><span data-stu-id="9c2b0-111">Finally, the **MailItem** is saved.</span></span>


> [!NOTE]
> <span data-ttu-id="9c2b0-112">Вы также можете добавить настраиваемые действия во время разработки с помощью конструктора форм Outlook.</span><span class="sxs-lookup"><span data-stu-id="9c2b0-112">You can also add custom actions at design time by using the Outlook Forms Designer.</span></span>


<span data-ttu-id="9c2b0-113">Если вы используете Visual Studio для тестирования этого примера кода, сначала добавьте ссылку на компонент Microsoft Outlook 15.0 Object Library и задайте переменную Outlook при импорте пространства имен **Microsoft.Office.Interop.Outlook**.</span><span class="sxs-lookup"><span data-stu-id="9c2b0-113">If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the Outlook variable when you import the **Microsoft.Office.Interop.Outlook** namespace.</span></span> <span data-ttu-id="9c2b0-114">Инструкция **using** не должна находиться непосредственно перед функциями в примере кода, но ее нужно добавить перед объявлением общедоступного класса.</span><span class="sxs-lookup"><span data-stu-id="9c2b0-114">The **using** statement must not occur directly before the functions in the code example but must be added before the public Class declaration.</span></span> <span data-ttu-id="9c2b0-115">В приведенной ниже строке кода показано, как выполнить импорт и назначение на языке C\#.</span><span class="sxs-lookup"><span data-stu-id="9c2b0-115">The following line of code shows how to do the import and assignment in C\#.</span></span>

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;

    private void ReplyWithVoiceMail()
    {
        Outlook.MailItem mail = (Outlook.MailItem)Application.ActiveInspector().CurrentItem;
        Outlook.Action action = mail.Actions.Add();
        action.Name = “Reply with Voice Mail”;
        action.ReplyStyle = Outlook.OlActionReplyStyle.olUserPreference;
        action.ResponseStyle = Outlook.OlActionResponseStyle.olOpen;
        action.CopyLike = Outlook.OlActionCopyLike.olReply;
        action.MessageClass = “IPM.Post.Voice Message”;
        mail.Save();
    }
```

## <a name="see-also"></a><span data-ttu-id="9c2b0-116">См. также</span><span class="sxs-lookup"><span data-stu-id="9c2b0-116">See also</span></span>

- [<span data-ttu-id="9c2b0-117">Почта</span><span class="sxs-lookup"><span data-stu-id="9c2b0-117">Mail</span></span>](mail.md)


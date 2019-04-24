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
# <a name="add-a-custom-action-as-a-response-to-a-mail-item"></a>Добавление настраиваемого действия в качестве ответа на почтовый элемент

В этом примере показано добавление настраиваемых действий в виде ответа на сообщение электронной почты с помощью метода [Add()](https://msdn.microsoft.com/library/bb612077\(v=office.15\)) коллекции [Actions](https://msdn.microsoft.com/library/bb611963\(v=office.15\)).

## <a name="example"></a>Пример

> [!NOTE] 
> Приведенный ниже пример кода представляет собой фрагмент из книги [Программирование приложений для Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).


Можно программным способом создать настраиваемые действия, которые будут отображаться на ленте в группе **Действия** вкладки **Сообщение** в ответе на сообщение электронной почты. В следующем примере кода в процедуре ReplyWithVoiceMail создается настраиваемое действие "Reply with Voice Mail" (Ответить по голосовой почте), которое добавляется в панель команд инспектора. В процедуре ReplyWithVoiceMail сначала получается объект [\_MailItem](https://msdn.microsoft.com/library/bb610623\(v=office.15\)), а затем создается объект [Action](https://msdn.microsoft.com/library/bb646971\(v=office.15\)) с помощью метода **Add** коллекции **Actions**, связанной с элементом **MailItem**. После этого свойству [Name](https://msdn.microsoft.com/library/bb624053\(v=office.15\)) объекта **Action** присваивается значение "Reply with Voice Mail". Также задаются свойства [ReplyStyle](https://msdn.microsoft.com/library/bb624278\(v=office.15\)), [ResponseStyle](https://msdn.microsoft.com/library/bb622491\(v=office.15\)), [CopyLike](https://msdn.microsoft.com/library/bb624213\(v=office.15\)) и [MessageClass](https://msdn.microsoft.com/library/bb624391\(v=office.15\)). В конце элемент **MailItem** сохраняется.


> [!NOTE]
> Вы также можете добавить настраиваемые действия во время разработки с помощью конструктора форм Outlook.


Если вы используете Visual Studio для тестирования этого примера кода, сначала добавьте ссылку на компонент Microsoft Outlook 15.0 Object Library и задайте переменную Outlook при импорте пространства имен **Microsoft.Office.Interop.Outlook**. Инструкция **using** не должна находиться непосредственно перед функциями в примере кода, но ее нужно добавить перед объявлением общедоступного класса. В приведенной ниже строке кода показано, как выполнить импорт и назначение на языке C\#.

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

## <a name="see-also"></a>См. также

- [Почта](mail.md)


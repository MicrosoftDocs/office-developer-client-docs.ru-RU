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
# <a name="add-voting-options-to-a-mail-item"></a>Добавление параметров голосования в почтовый элемент

В этом примере показано, как использовать свойство [VotingOptions](https://msdn.microsoft.com/library/bb652695\(v=office.15\)) объекта [MailItem](https://msdn.microsoft.com/library/bb643865\(v=office.15\)), чтобы добавить параметры голосования в сообщение электронной почты.

## <a name="example"></a>Пример

> [!NOTE] 
> Приведенный ниже пример кода представляет собой фрагмент из книги [Программирование приложений для Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).


Параметры голосования в сообщениях используются для предоставления получателям сообщения списка вариантов ответа и отслеживания ответов. Чтобы программно создать параметры голосования, следует задать для свойства **VotingOptions** объекта **MailItem** строковое значение, содержащее разделенный точками с запятыми список значений. Значения для свойства **VotingOptions** будут появляться под командой **Голосование** в группе **Ответить** ленты полученных сообщений. 

В приведенном ниже примере OrderPizza создает параметры голосования в новом сообщении электронной почты. OrderPizza сначала создает объект **MailItem**, затем устанавливает свойство **VotingOptions** равным "Cheese; Mushroom; Sausage; Combo; Veg Combo", а свойство [Subject](https://msdn.microsoft.com/library/bb611353\(v=office.15\)) равным "Pizza Order". При отправке сообщения "Pizza Order" параметры голосования отображаются для получателей. Выбор получателя в каждом полученном ответе регистрируется на странице **Отслеживание** сообщения в папке отправителя "Отправленные".

Если вы используете Visual Studio для тестирования этого примера кода, сначала добавьте ссылку на компонент Microsoft Outlook 15.0 Object Library и задайте переменную Outlook при импорте пространства имен **Microsoft.Office.Interop.Outlook**. Инструкция **using** не должна идти непосредственно перед функциями в примере кода, но ее нужно добавить перед открытым объявлением Class. В следующей строке кода показано, как выполнить импорт и назначение в C\#.

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

## <a name="see-also"></a>См. также

- [Почта](mail.md)


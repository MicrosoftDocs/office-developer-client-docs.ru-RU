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
# <a name="specify-different-recipient-types-for-a-mail-item"></a>Задание разных типов получателей для почтового элемента

В этом примере показано, как программно задать разные типы получателей ("Кому", "Копия" или "СК") для почтового элемента.

## <a name="example"></a>Пример

> [!NOTE] 
> Приведенный ниже пример кода представляет собой фрагмент из книги [Программирование приложений для Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).

В примере кода ниже показано, как указать, к какому типу ("Кому", "Копия" или "СК") относится получатель объекта [MailItem](https://msdn.microsoft.com/library/bb643865\(v=office.15\)). SetRecipientTypeForMail создает объект **MailItem**, добавляет три объекта [Recipient](https://msdn.microsoft.com/library/bb624370\(v=office.15\)) в коллекцию [Recipients](https://msdn.microsoft.com/library/bb646361\(v=office.15\)) элемента **MailItem**, а затем для свойства [Type](https://msdn.microsoft.com/library/bb611841\(v=office.15\)) каждого объекта **Recipient** задает значение из перечисления [OlMailRecipientType](https://msdn.microsoft.com/library/bb647641\(v=office.15\)).


> [!NOTE]
> Свойство **Type** объекта **Recipient** относится к типу int и не соответствует конкретному перечислению типов получателей.

Если вы используете Visual Studio для тестирования этого примера кода, сначала добавьте ссылку на компонент Microsoft Outlook 15.0 Object Library и задайте переменную Outlook при импорте пространства имен **Microsoft.Office.Interop.Outlook**. Инструкция **using** не должна находиться непосредственно перед функциями в примере кода, но ее нужно добавить перед объявлением общедоступного класса. В приведенной ниже строке кода показано, как выполнить импорт и назначение на языке C\#.

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

## <a name="see-also"></a>См. также

- [Почта](mail.md)


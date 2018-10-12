---
title: Отправка почтового элемента с помощью учетной записи Hotmail
TOCTitle: Send a mail item by using a Hotmail account
ms:assetid: f25853a7-67c0-46a3-a298-5cdf72ebc53f
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184652(v=office.15)
ms:contentKeyID: 55119797
ms.date: 07/24/2014
mtps_version: v=office.15
ms.openlocfilehash: f95d5202f17c21e1c4be4545687f2eee96a00da3
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25407305"
---
# <a name="send-a-mail-item-by-using-a-hotmail-account"></a>Отправка почтового элемента с помощью учетной записи Hotmail

В этом примере используется свойство [SendUsingAccount](https://msdn.microsoft.com/library/bb623679\(v=office.15\)) для отправки почтового элемента с помощью учетной записи Windows Live Hotmail.

## <a name="example"></a>Пример

> [!NOTE] 
> Приведенный ниже пример кода взят из книги [Программирование приложений для Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).

Профиль определяет одну или несколько учетных записей электронной почты, а каждая такая учетная запись связана с сервером определенного типа (например, с сервером Microsoft Exchange Server или сервером POP3). Поскольку в вашем профиле может находиться несколько учетных записей, необходимо указать используемую для отправки элемента учетную запись электронной почты, а затем получить представляющий ее объект [Account](https://msdn.microsoft.com/library/bb645103\(v=office.15\)).

В представленном ниже примере кода сообщение создается с вложенным маршрутом и затем отправляется с помощью учетной записи Windows Live Hotmail. Учетная запись Hotmail применяется в качестве объекта **Account** в профиле пользователя. Затем в примере кода для свойства SendUsingAccount задается этот объект Account и вызывается метод [Send()](https://msdn.microsoft.com/library/bb644139\(v=office.15\)) из объекта [MailItem](https://msdn.microsoft.com/library/bb643865\(v=office.15\)).

Если для тестирования этого примера кода вы используете Visual Studio, сначала добавьте ссылку на компонент библиотеки объектов Microsoft Outlook 15.0 и укажите переменную Outlook при импорте пространства имен **Microsoft.Office.Interop.Outlook**. Не следует использовать инструкцию **using** непосредственно перед функциями в примере кода, но ее необходимо добавить перед объявлением общедоступного класса. В следующей строке кода показано, как выполнить импорт и назначение в C\#.

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

## <a name="see-also"></a>См. также

- [Учетные записи](accounts.md)


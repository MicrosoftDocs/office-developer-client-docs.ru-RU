---
title: Создание отправляемого элемента для определенной учетной записи на основе текущей папки
TOCTitle: Create a sendable item for a specific account based on the current folder
ms:assetid: 665ebdc5-2912-4d85-ac40-835c9ef9a439
ms:contentKeyID: 55119796
ms.date: 07/24/2014
mtps_version: v=office.15
ms.openlocfilehash: 076677ed2eeedb269ddddc3bee201a162196db0c
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25405765"
---
# <a name="create-a-sendable-item-for-a-specific-account-based-on-the-current-folder"></a>Создание отправляемого элемента для определенной учетной записи на основе текущей папки

Этот раздел содержит два примера кода, показывающих, как создавать отправляемый элемент электронной почты и приглашение на собрание и как потом отправить эти элементы, используя конкретную учетную запись, основанную на текущей папке.

## <a name="example"></a>Пример

При использовании метода [CreateItem(OlItemType)](https://msdn.microsoft.com/library/bb610587\(v=office.15\)) объекта [Application](https://msdn.microsoft.com/library/bb646615\(v=office.15\)) для создания элемента Outlook этот элемент создается для основной учетной записи данного сеанса. В сеансе, в профиле которого определено несколько учетных записей, можно создать элемент для конкретной учетной записи IMAP, POP или Exchange. 

Если в текущем профиле есть несколько учетных записей и в интерфейсе пользователя создается отправляемый элемент, например с помощью кнопки **Создать сообщение** или **Создать собрание**, инспектор отображает новый почтовый элемент или приглашение на собрание в режиме создания, а затем можно выбрать учетную запись, от имени которой будет отправлен элемент. 

В этом разделе показано, как программно создать отправляемый элемент и отправить его с помощью определенной учетной записи. Раздел содержит два примера кода, показывающих, как создать элементы [MailItem](https://msdn.microsoft.com/library/bb643865\(v=office.15\)) и [AppointmentItem](https://msdn.microsoft.com/library/bb645611\(v=office.15\)) для конкретной учетной записи, определенной текущей папкой в активном проводнике.

Если вы используете Visual Studio для тестирования этого примера кода, сначала добавьте ссылку на компонент Microsoft Outlook 15.0 Object Library и задайте переменную Outlook при импорте пространства имен **Microsoft.Office.Interop.Outlook**. Инструкция **using** не должна идти непосредственно перед функциями в примере кода, но ее нужно добавить перед открытым объявлением Class. В следующей строке кода показано, как выполнить импорт и назначение в C\#.

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```

В первом методе CreateMailItemFromAccount сначала определяет соответствующую учетную запись, сопоставляя хранилище текущей папки (полученное из свойства [Store](https://msdn.microsoft.com/library/bb612742\(v=office.15\))) с хранилищем доставки по умолчанию каждой учетной записи (полученной с помощью свойства [DeliveryStore](https://msdn.microsoft.com/library/ff185090\(v=office.15\))), определенной в коллекции [Accounts](https://msdn.microsoft.com/library/bb646328\(v=office.15\)) для сеанса. Затем CreateMailItemFromAccount создает элемент **MailItem**. 

Чтобы связать этот элемент с учетной записью, CreateMailItemFromAccount назначает пользователя учетной записи отправителем элемента, устанавливая свойство account.CurrentUser.AddressEntry равным свойству [Sender](https://msdn.microsoft.com/library/ff184720\(v=office.15\)) элемента **MailItem**. Назначение свойства Sender является важным шагом  если отправитель не задан, элемент **MailItem** по умолчанию создается для основной учетной записи. В конце метода CreateMailItemFromAccount отображает элемент **MailItem**. Обратите внимание, что если текущая папка находится не в хранилище доставки, то CreateMailItemFromAccount создает элемент **MailItem** для основной учетной записи сеанса.

```csharp
private void CreateMailItemFromAccount()
{
    Outlook.AddressEntry addrEntry = null;
    // Get the Store for CurrentFolder.
    Outlook.Folder folder =
        Application.ActiveExplorer().CurrentFolder 
        as Outlook.Folder;
    Outlook.Store store = folder.Store;
    Outlook.Accounts accounts =
        Application.Session.Accounts;
    // Enumerate accounts to find
    // account.DeliveryStore for store.
    foreach (Outlook.Account account in accounts)
    {
        if (account.DeliveryStore.StoreID == 
            store.StoreID)
        {
            addrEntry =
                account.CurrentUser.AddressEntry;
            break;
        }
    }
    // Create MailItem.
    Outlook.MailItem mail =
        Application.CreateItem(
        Outlook.OlItemType.olMailItem)
        as Outlook.MailItem;
    if (addrEntry != null)
    {
        // Set Sender property.
        mail.Sender = addrEntry;
        mail.Display(false);
    }
}
```

Следующий метод CreateMeetingRequestFromAccount похож на CreateMailItemFromAccount, только вместо MailItem создается элемент AppointmentItem. CreateMeetingRequestFromAccount сначала определяет соответствующую учетную запись, сопоставляя хранилище текущей папки (полученное из свойства [Store](https://msdn.microsoft.com/library/bb612742\(v=office.15\))) с хранилищем доставки по умолчанию каждой учетной записи (полученным из свойства [DeliveryStore](https://msdn.microsoft.com/library/ff185090\(v=office.15\))), определенной в коллекции Accounts для сеанса. Затем CreateMeetingRequestFromAccount создает элемент AppointmentItem. 

Чтобы связать этот элемент с учетной записью, CreateMeetingRequestFromAccount назначает эту учетную запись в качестве учетной записи, отправляющей элемент, устанавливая объект [Account](https://msdn.microsoft.com/library/bb645103\(v=office.15\)) в качестве значения свойству [SendUsingAccount](https://msdn.microsoft.com/library/bb610680\(v=office.15\)) элемента AppointmentItem. Назначение свойства SendUsingAccount является важным шагом  если учетная запись не задана, элемент AppointmentItem по умолчанию создается для основной учетной записи. В конце метода CreateMeetingRequestFromAccount отображает элемент AppointmentItem. Обратите внимание, что если текущая папка не находится в хранилище доставки, то CreateMeetingRequestFromAccount создает элемент AppointmentItem для основной учетной записи сеанса.

```csharp
private void CreateMeetingRequestFromAccount()
{
    Outlook.Account acct = null;
    Outlook.Folder folder =
        Application.ActiveExplorer().CurrentFolder
        as Outlook.Folder;
    Outlook.Store store = folder.Store;
    Outlook.Accounts accounts =
        Application.Session.Accounts;
    foreach (Outlook.Account account in accounts)
    {
        if (account.DeliveryStore.StoreID ==
            store.StoreID)
        {
            acct = account;
            break;
        }
    }
    Outlook.AppointmentItem appt =
        Application.CreateItem(
        Outlook.OlItemType.olAppointmentItem)
        as Outlook.AppointmentItem;
    appt.MeetingStatus = 
        Outlook.OlMeetingStatus.olMeeting;
    if (acct != null)
    {
        // Set SendUsingAccount property.
        appt.SendUsingAccount=acct;
        appt.Display(false);
    }
}
```

## <a name="see-also"></a>См. также

- [Учетные записи](accounts.md)


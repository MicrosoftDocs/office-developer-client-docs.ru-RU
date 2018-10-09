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
# <a name="create-a-sendable-item-for-a-specific-account-based-on-the-current-folder"></a><span data-ttu-id="442cd-102">Создание отправляемого элемента для определенной учетной записи на основе текущей папки</span><span class="sxs-lookup"><span data-stu-id="442cd-102">Create a Sendable Item for a Specific Account Based on the Current Folder</span></span>

<span data-ttu-id="442cd-103">Этот раздел содержит два примера кода, показывающих, как создавать отправляемый элемент электронной почты и приглашение на собрание и как потом отправить эти элементы, используя конкретную учетную запись, основанную на текущей папке.</span><span class="sxs-lookup"><span data-stu-id="442cd-103">This topic contains two code examples that show how to create a sendable e-mail item and meeting request, and then how to send them by using a specific account that is based on the current folder.</span></span>

## <a name="example"></a><span data-ttu-id="442cd-104">Пример</span><span class="sxs-lookup"><span data-stu-id="442cd-104">Example</span></span>

<span data-ttu-id="442cd-105">При использовании метода [CreateItem(OlItemType)](https://msdn.microsoft.com/library/bb610587\(v=office.15\)) объекта [Application](https://msdn.microsoft.com/library/bb646615\(v=office.15\)) для создания элемента Outlook этот элемент создается для основной учетной записи данного сеанса.</span><span class="sxs-lookup"><span data-stu-id="442cd-105">When you use the [CreateItem(OlItemType)](https://msdn.microsoft.com/library/bb610587\(v=office.15\)) method of the [Application](https://msdn.microsoft.com/library/bb646615\(v=office.15\)) object to create a Microsoft Outlook item, the item is created for the primary account for that session.</span></span> <span data-ttu-id="442cd-106">В сеансе, в профиле которого определено несколько учетных записей, можно создать элемент для конкретной учетной записи IMAP, POP или Exchange.</span><span class="sxs-lookup"><span data-stu-id="442cd-106">In a session where multiple accounts are defined in the profile, you can create an item for a specific IMAP, POP, or Microsoft Exchange account.</span></span> 

<span data-ttu-id="442cd-107">Если в текущем профиле есть несколько учетных записей и в интерфейсе пользователя создается отправляемый элемент, например с помощью кнопки **Создать сообщение** или **Создать собрание**, инспектор отображает новый почтовый элемент или приглашение на собрание в режиме создания, а затем можно выбрать учетную запись, от имени которой будет отправлен элемент.</span><span class="sxs-lookup"><span data-stu-id="442cd-107">If there are multiple accounts in the current profile and you create a sendable item in the user interface, for example, by clicking **New E-mail** or **New Meeting**, an inspector displays a new mail item or meeting request in compose mode, and then you can select the account from which to send the item.</span></span> 

<span data-ttu-id="442cd-108">В этом разделе показано, как программно создать отправляемый элемент и отправить его с помощью определенной учетной записи.</span><span class="sxs-lookup"><span data-stu-id="442cd-108">This topic shows how to programmatically create a sendable item and send it by using a specific sending account.</span></span> <span data-ttu-id="442cd-109">Раздел содержит два примера кода, показывающих, как создать элементы [MailItem](https://msdn.microsoft.com/library/bb643865\(v=office.15\)) и [AppointmentItem](https://msdn.microsoft.com/library/bb645611\(v=office.15\)) для конкретной учетной записи, определенной текущей папкой в активном проводнике.</span><span class="sxs-lookup"><span data-stu-id="442cd-109">The topic has two code examples that show how to create a [MailItem](https://msdn.microsoft.com/library/bb643865\(v=office.15\)) and an [AppointmentItem](https://msdn.microsoft.com/library/bb645611\(v=office.15\)) for a specific account that is determined by the current folder in the active explorer.</span></span>

<span data-ttu-id="442cd-110">Если вы используете Visual Studio для тестирования этого примера кода, сначала добавьте ссылку на компонент Microsoft Outlook 15.0 Object Library и задайте переменную Outlook при импорте пространства имен **Microsoft.Office.Interop.Outlook**.</span><span class="sxs-lookup"><span data-stu-id="442cd-110">If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the   variable when you import the Microsoft.Office.Interop.Outlook namespace.</span></span> <span data-ttu-id="442cd-111">Инструкция **using** не должна идти непосредственно перед функциями в примере кода, но ее нужно добавить перед открытым объявлением Class.</span><span class="sxs-lookup"><span data-stu-id="442cd-111">The using statement must not occur directly before the functions in the code example but must be added before the public   declaration.</span></span> <span data-ttu-id="442cd-112">В следующей строке кода показано, как выполнить импорт и назначение в C\#.</span><span class="sxs-lookup"><span data-stu-id="442cd-112">The following line of code shows how to do the import and assignment in C#.</span></span>

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```

<span data-ttu-id="442cd-113">В первом методе CreateMailItemFromAccount сначала определяет соответствующую учетную запись, сопоставляя хранилище текущей папки (полученное из свойства [Store](https://msdn.microsoft.com/library/bb612742\(v=office.15\))) с хранилищем доставки по умолчанию каждой учетной записи (полученной с помощью свойства [DeliveryStore](https://msdn.microsoft.com/library/ff185090\(v=office.15\))), определенной в коллекции [Accounts](https://msdn.microsoft.com/library/bb646328\(v=office.15\)) для сеанса.</span><span class="sxs-lookup"><span data-stu-id="442cd-113">In the first method below,   first identifies the appropriate account by matching the store of the current folder (obtained from the Store property) with the default delivery store of each account (obtained with the DeliveryStore property) that is defined in the Accounts collection for the session.</span></span> <span data-ttu-id="442cd-114">Затем CreateMailItemFromAccount создает элемент **MailItem**.</span><span class="sxs-lookup"><span data-stu-id="442cd-114"> then creates the MailItem.</span></span> 

<span data-ttu-id="442cd-115">Чтобы связать этот элемент с учетной записью, CreateMailItemFromAccount назначает пользователя учетной записи отправителем элемента, устанавливая свойство account.CurrentUser.AddressEntry равным свойству [Sender](https://msdn.microsoft.com/library/ff184720\(v=office.15\)) элемента **MailItem**.</span><span class="sxs-lookup"><span data-stu-id="442cd-115">To associate the item with the account,   assigns the user of the account as the sender of the item by setting the   property to the Sender property of the MailItem.</span></span> <span data-ttu-id="442cd-116">Назначение свойства Sender является важным шагом  если отправитель не задан, элемент **MailItem** по умолчанию создается для основной учетной записи.</span><span class="sxs-lookup"><span data-stu-id="442cd-116">Assigning the Sender property is the important step; if you do not specify the sender, the **MailItem** is created for the primary account by default.</span></span> <span data-ttu-id="442cd-117">В конце метода CreateMailItemFromAccount отображает элемент **MailItem**.</span><span class="sxs-lookup"><span data-stu-id="442cd-117">At the end of the method,   displays the MailItem.</span></span> <span data-ttu-id="442cd-118">Обратите внимание, что если текущая папка находится не в хранилище доставки, то CreateMailItemFromAccount создает элемент **MailItem** для основной учетной записи сеанса.</span><span class="sxs-lookup"><span data-stu-id="442cd-118">Note that if the current folder is not on a delivery store,   creates the MailItem for the primary account for the session.</span></span>

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

<span data-ttu-id="442cd-119">Следующий метод CreateMeetingRequestFromAccount похож на CreateMailItemFromAccount, только вместо MailItem создается элемент AppointmentItem.</span><span class="sxs-lookup"><span data-stu-id="442cd-119">The next method,  , is similar to   except that it creates an AppointmentItem instead of a MailItem.</span></span> <span data-ttu-id="442cd-120">CreateMeetingRequestFromAccount сначала определяет соответствующую учетную запись, сопоставляя хранилище текущей папки (полученное из свойства [Store](https://msdn.microsoft.com/library/bb612742\(v=office.15\))) с хранилищем доставки по умолчанию каждой учетной записи (полученным из свойства [DeliveryStore](https://msdn.microsoft.com/library/ff185090\(v=office.15\))), определенной в коллекции Accounts для сеанса.</span><span class="sxs-lookup"><span data-stu-id="442cd-120"> first identifies the appropriate account by matching the store of the current folder (obtained from the Store property) with the default delivery store of each account (obtained from the DeliveryStore property) that is defined in the Accounts collection for the session.</span></span> <span data-ttu-id="442cd-121">Затем CreateMeetingRequestFromAccount создает элемент AppointmentItem.</span><span class="sxs-lookup"><span data-stu-id="442cd-121"> then creates the AppointmentItem.</span></span> 

<span data-ttu-id="442cd-122">Чтобы связать этот элемент с учетной записью, CreateMeetingRequestFromAccount назначает эту учетную запись в качестве учетной записи, отправляющей элемент, устанавливая объект [Account](https://msdn.microsoft.com/library/bb645103\(v=office.15\)) в качестве значения свойству [SendUsingAccount](https://msdn.microsoft.com/library/bb610680\(v=office.15\)) элемента AppointmentItem.</span><span class="sxs-lookup"><span data-stu-id="442cd-122">To associate the item with the account,   assigns that account as the item's sending account by setting the Account object to the SendUsingAccount property of the AppointmentItem.</span></span> <span data-ttu-id="442cd-123">Назначение свойства SendUsingAccount является важным шагом  если учетная запись не задана, элемент AppointmentItem по умолчанию создается для основной учетной записи.</span><span class="sxs-lookup"><span data-stu-id="442cd-123">Assigning the SendUsingAccount property is the important step; if you do not specify the account, the AppointmentItem is created for the primary account by default.</span></span> <span data-ttu-id="442cd-124">В конце метода CreateMeetingRequestFromAccount отображает элемент AppointmentItem.</span><span class="sxs-lookup"><span data-stu-id="442cd-124">At the end of the method,   displays the AppointmentItem.</span></span> <span data-ttu-id="442cd-125">Обратите внимание, что если текущая папка не находится в хранилище доставки, то CreateMeetingRequestFromAccount создает элемент AppointmentItem для основной учетной записи сеанса.</span><span class="sxs-lookup"><span data-stu-id="442cd-125">Note that if the current folder is not on a delivery store,   creates the AppointmentItem for the primary account for the session.</span></span>

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

## <a name="see-also"></a><span data-ttu-id="442cd-126">См. также</span><span class="sxs-lookup"><span data-stu-id="442cd-126">See also</span></span>

- [<span data-ttu-id="442cd-127">Учетные записи</span><span class="sxs-lookup"><span data-stu-id="442cd-127">Accounts</span></span>](accounts.md)


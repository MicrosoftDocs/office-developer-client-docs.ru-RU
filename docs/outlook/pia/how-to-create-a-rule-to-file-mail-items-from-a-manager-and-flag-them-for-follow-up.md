---
title: Создание правила для передачи почтовых элементов от руководителя и их пометки к исполнению
TOCTitle: Create a rule to file mail items from a manager and flag them for follow-up
ms:assetid: c50578c2-15de-4d5f-87d9-d6162034f083
ms:mtpsurl: https://msdn.microsoft.com/library/Ff424477(v=office.15)
ms:contentKeyID: 55119880
ms.date: 07/24/2014
mtps_version: v=office.15
ms.openlocfilehash: 2fc6f5fe60b2f643590e8f7545804cf6d8a4c11c
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25405989"
---
# <a name="create-a-rule-to-file-mail-items-from-a-manager-and-flag-them-for-follow-up"></a><span data-ttu-id="f6513-102">Создание правила для передачи почтовых элементов от руководителя и их пометки к исполнению</span><span class="sxs-lookup"><span data-stu-id="f6513-102">Create a rule to file mail items from a manager and flag them for follow-up</span></span>

<span data-ttu-id="f6513-103">В этом примере показано, как задать правило для передачи почтовых элементов от руководителя пользователя и пометить их к исполнению.</span><span class="sxs-lookup"><span data-stu-id="f6513-103">This example shows how to set up a rule to file mail items from the user’s manager and flag them for follow up.</span></span>

## <a name="example"></a><span data-ttu-id="f6513-104">Пример</span><span class="sxs-lookup"><span data-stu-id="f6513-104">Example</span></span>

> [!NOTE] 
> <span data-ttu-id="f6513-105">Приведенный ниже пример кода представляет собой фрагмент из книги [Программирование приложений для Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).</span><span class="sxs-lookup"><span data-stu-id="f6513-105">The following code example is an excerpt from  [Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493)  , from Microsoft Press (ISBN 9780735622494, copyright Microsoft Press 2007, all rights reserved).</span></span>

<span data-ttu-id="f6513-p101">Правила Outlook могут выполняться как на стороне сервера, так и на стороне клиента, в зависимости от типа учетной записи и правила. Существует несколько способов реализации правил в соответствии с принятой в организации схемой хранения элементов в почтовых ящиках. Например, можно создать иерархию вложенных папок, в которых будут храниться прочитанные и непрочитанные сообщения по теме. Также можно создать иерархию вложенных папок, упорядоченную по отправителю сообщения. Кроме того, можно назначать сообщениям категории и использовать папки поиска для сбора сообщений по категориям.</span><span class="sxs-lookup"><span data-stu-id="f6513-p101">Outlook rules can operate either server-side or client-side, depending on the type of account and rule. There are many ways you can implement rules to enforce your own organizational schemes when you organize items in your mailbox. For example, you can create a subfolder hierarchy that organizes unread mail and read mail by subject area. Or, you can create a subfolder hierarchy that corresponds to the sender of the message. You can also categorize your mail and then use search folders to aggregate the mail by category.</span></span>

<span data-ttu-id="f6513-111">Объектная модель **Rules** содержит объект [Rule](https://msdn.microsoft.com/library/bb647152\(v=office.15\)) , представляющий правило в приложении Outlook, что позволяет создавать программным способом правила, реализующие принятую в организации схему, создавать уникальные правила для решений, а также обеспечивать развертывание определенных правил для групп пользователей.</span><span class="sxs-lookup"><span data-stu-id="f6513-111">The **Rules** object model, which includes a [Rule](https://msdn.microsoft.com/library/bb647152\(v=office.15\)) object that represents a rule in Outlook, allows you to create rules programmatically to enforce a certain organizational scheme, create a specific rule that is unique to your solution, or ensure that certain rules are deployed to a group of users.</span></span> <span data-ttu-id="f6513-112">С помощью объектной модели **Rules** можно программным способом добавлять, изменять и удалять правила.</span><span class="sxs-lookup"><span data-stu-id="f6513-112">By using the **Rules** object model, you can programmatically add, edit, and delete rules.</span></span> <span data-ttu-id="f6513-113">С помощью коллекции [Rules](https://msdn.microsoft.com/library/bb622788\(v=office.15\)) и объекта **Rule** также можно получать доступ к правилам, определенным для сеанса, добавлять и удалять их.</span><span class="sxs-lookup"><span data-stu-id="f6513-113">By using the [Rules](https://msdn.microsoft.com/library/bb622788\(v=office.15\)) collection and the **Rule** object, you can also access, add, and delete rules defined for a session.</span></span> 

<span data-ttu-id="f6513-114">Объект **Rule** содержит свойство [RuleType](https://msdn.microsoft.com/library/bb645613\(v=office.15\)) , которое определяет тип правила (отправка или получение).</span><span class="sxs-lookup"><span data-stu-id="f6513-114">A **Rule** object has a [RuleType](https://msdn.microsoft.com/library/bb645613\(v=office.15\)) property that indicates whether the rule is a send or receive rule.</span></span> <span data-ttu-id="f6513-115">Свойство **RuleType** устанавливается при создании правила и может быть изменено только посредством удаления правила или его повторного создания с другим значением свойства **RuleType**.</span><span class="sxs-lookup"><span data-stu-id="f6513-115">When a rule is created, the **RuleType** property is specified, and cannot be changed without deleting and re-creating the rule with a different **RuleType** property.</span></span> <span data-ttu-id="f6513-116">Объекты [RuleAction](https://msdn.microsoft.com/library/bb644297\(v=office.15\)) и [RuleCondition](https://msdn.microsoft.com/library/bb612469\(v=office.15\)) , соответствующие объекты коллекций, производные действия и объекты условий обеспечивают дополнительные возможности по изменению действий и условий правил.</span><span class="sxs-lookup"><span data-stu-id="f6513-116">The [RuleAction](https://msdn.microsoft.com/library/bb644297\(v=office.15\)) and [RuleCondition](https://msdn.microsoft.com/library/bb612469\(v=office.15\)) objects, their collection objects, and derived action and condition objects are also used to further support editing rule actions and rule conditions.</span></span>

<span data-ttu-id="f6513-p104">В объектной модели **Rules** поддерживаются не все правила, которые можно создать с помощью мастера правил и оповещений в интерфейсе пользователя Outlook, однако при этом обеспечивается поддержка наиболее распространенных действий и условий. Правила, создаваемые с помощью мастера правил и оповещений, которые применяются к сообщениям, в том числе к почтовым элементам, приглашениям на собрания, запросам на задачи, документам, уведомлениям о доставке, уведомлениям о прочтении, результатам голосования и уведомлениям об отсутствии на работе, также можно создавать программным способом.</span><span class="sxs-lookup"><span data-stu-id="f6513-p104">The **Rules** object model does not support all rules that you can create by using the Rules and Alert Wizard in the Outlook user interface, but it supports the most commonly used rule actions and conditions. Any rules created by using the Rules and Alerts Wizard that are applied to messages, which include mail items, meeting requests, task requests, documents, delivery receipts, read receipts, voting responses, and out-of-office notices, can also be created programmatically.</span></span>

<span data-ttu-id="f6513-119">Правило может выполняться на сервере Exchange или в клиенте Outlook при условии, что почтовый ящик текущего пользователя размещается на сервере Exchange.</span><span class="sxs-lookup"><span data-stu-id="f6513-119">A rule can execute on the Exchange server or on the Outlook client, provided that the current user's mailbox is hosted on an Exchange server.</span></span> <span data-ttu-id="f6513-120">Свойство [IsLocalRule](https://msdn.microsoft.com/library/bb647386\(v=office.15\)) объекта **Rule** возвращает значение **true**, свидетельствующее о выполнении правила в клиенте и необходимости запуска приложения Outlook для выполнения правила.</span><span class="sxs-lookup"><span data-stu-id="f6513-120">The [IsLocalRule](https://msdn.microsoft.com/library/bb647386\(v=office.15\)) property of the **Rule** object returns **true** to indicate that the rule executes on a client, and Outlook must be running for the rule to execute.</span></span> <span data-ttu-id="f6513-121">Если правило выполняется на сервере, для оценки условий и выполнения действий правила запускать приложение Outlook не требуется.</span><span class="sxs-lookup"><span data-stu-id="f6513-121">If the rule executes on the server, Outlook does not have to be running for the rule conditions to be evaluated and the rule actions to be completed.</span></span>

> [!NOTE]
> <span data-ttu-id="f6513-p106">Отдельная коллекция, представляющая условия исключений из правила, не предусмотрена. Следует использовать свойство [Exceptions](https://docs.microsoft.com/dotnet/api/microsoft.office.interop.outlook._rule.exceptions?view=outlook-pia) объекта **Rule** для получение коллекции [RuleConditions](https://docs.microsoft.com/dotnet/api/microsoft.office.interop.outlook.ruleconditions?view=outlook-pia) , которая представляет условия исключений из правила.</span><span class="sxs-lookup"><span data-stu-id="f6513-p106">There is no separate collection that represents rule exception conditions. Use the [Exceptions](https://docs.microsoft.com/dotnet/api/microsoft.office.interop.outlook._rule.exceptions?view=outlook-pia) property of the **Rule** object to get a [RuleConditions](https://docs.microsoft.com/dotnet/api/microsoft.office.interop.outlook.ruleconditions?view=outlook-pia) collection that represents rule exception conditions.</span></span>

<span data-ttu-id="f6513-124">Для создания правил с помощью объектной модели Outlook выполните следующие действия:</span><span class="sxs-lookup"><span data-stu-id="f6513-124">To create rules through the Outlook object model, follow these steps:</span></span>

1.  <span data-ttu-id="f6513-p107">Получите коллекцию **Rules** из свойства [DefaultStore](https://msdn.microsoft.com/library/bb623164\(v=office.15\)) объекта [NameSpace](https://msdn.microsoft.com/library/bb645857\(v=office.15\)) . Для этого вызовите метод [GetRules()](https://msdn.microsoft.com/library/bb609979\(v=office.15\)) для установленного по умолчанию объекта [Store](https://msdn.microsoft.com/library/bb609139\(v=office.15\)) . Используйте блок **try…catch** для учетной записи пользователя, находящегося в автономном режиме или отключенного от сервера Exchange. Это позволит исключить возникновение ошибки приложения Outlook.</span><span class="sxs-lookup"><span data-stu-id="f6513-p107">Get the **Rules** collection from the [DefaultStore](https://msdn.microsoft.com/library/bb623164\(v=office.15\)) property of the [NameSpace](https://msdn.microsoft.com/library/bb645857\(v=office.15\)) object by calling the [GetRules()](https://msdn.microsoft.com/library/bb609979\(v=office.15\)) method on the default [Store](https://msdn.microsoft.com/library/bb609139\(v=office.15\)) object. Use a **try…catch** block to account for the user being offline or disconnected from the Exchange server. This prevents Outlook from raising an error.</span></span>

2.  <span data-ttu-id="f6513-128">Вызовите метод [Create(String, OlRuleType)](https://msdn.microsoft.com/library/bb643857\(v=office.15\)) для объекта **Rules**, чтобы создать переменную экземпляра объекта **Rule**. Для этого укажите параметры Name и [OlRuleType](https://msdn.microsoft.com/library/bb645776\(v=office.15\)).</span><span class="sxs-lookup"><span data-stu-id="f6513-128">Call the [Create(String, OlRuleType)](https://msdn.microsoft.com/library/bb643857\(v=office.15\)) method on the **Rules** object to create an instance variable or a **Rule** object, specifying a  Name and a [OlRuleType](https://msdn.microsoft.com/library/bb645776\(v=office.15\)) parameter.</span></span>

3.  <span data-ttu-id="f6513-p108">С помощью коллекций [RuleActions](https://msdn.microsoft.com/library/bb610113\(v=office.15\)) и [RuleConditions](https://msdn.microsoft.com/library/bb610965\(v=office.15\)) включите действия, условия и исключения для объекта **Rule**. Обратите внимание, что условия, включенные в коллекции **RuleConditions**, возвращаемой свойством [Exceptions](https://msdn.microsoft.com/library/bb609880\(v=office.15\)) , обрабатываются как условия исключений из правила и добавление встроенных настраиваемых действий и условий в эту коллекцию не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="f6513-p108">Use the [RuleActions](https://msdn.microsoft.com/library/bb610113\(v=office.15\)) and [RuleConditions](https://msdn.microsoft.com/library/bb610965\(v=office.15\)) collections to enable actions, conditions, and exceptions on the **Rule** object. Note that any condition enabled in the **RuleConditions** collection, returned by the [Exceptions](https://msdn.microsoft.com/library/bb609880\(v=office.15\)) property, is treated as a rule exception condition, and additional built-in custom actions or conditions cannot be added to the collection.</span></span>

4.  <span data-ttu-id="f6513-p109">Присвойте свойству [Enabled](https://msdn.microsoft.com/library/bb609147\(v=office.15\)) значение **true** для любого подлежащего исполнению действия, условия или исключения. Для некоторых действий и свойств, например для свойства [Folder](https://msdn.microsoft.com/library/bb646755\(v=office.15\)) , требуется настройка дополнительных свойств, позволяющих сохранять объект **Rule** без ошибок.</span><span class="sxs-lookup"><span data-stu-id="f6513-p109">Set the [Enabled](https://msdn.microsoft.com/library/bb609147\(v=office.15\)) property to **true** for any given rule action, condition, or exception to be operational. Some actions or conditions, such as the [Folder](https://msdn.microsoft.com/library/bb646755\(v=office.15\)) property, require that you set additional properties on the action or condition to save the **Rule** object without an error.</span></span>

5.  <span data-ttu-id="f6513-p110">В завершение вызовите метод [Save(Object)](https://msdn.microsoft.com/library/bb610738\(v=office.15\)) для коллекции **Rules**, чтобы сохранить созданные или измененные правила. Для обработки исключений метод **Save** следует заключить в блок **try…catch**.</span><span class="sxs-lookup"><span data-stu-id="f6513-p110">Finally, call the [Save(Object)](https://msdn.microsoft.com/library/bb610738\(v=office.15\)) method on the **Rules** collection to save the created or modified rules. Enclose the **Save** method in a **try…catch** block to handle exceptions.</span></span>

<span data-ttu-id="f6513-135">В следующем примере кода в процедуре CreateManagerRule реализованы описанные выше действия.</span><span class="sxs-lookup"><span data-stu-id="f6513-135">In the following code example,   implements the steps previously described.</span></span> <span data-ttu-id="f6513-136">В процедуре CreateManagerRule сначала проверяется, представляет ли свойство [CurrentUser](https://msdn.microsoft.com/library/bb622574\(v=office.15\)) объект [ExchangeUser](https://msdn.microsoft.com/library/bb609574\(v=office.15\)), который определяет, является ли текущий пользователь пользователем Exchange.</span><span class="sxs-lookup"><span data-stu-id="f6513-136"> first verifies whether the CurrentUser property represents an ExchangeUser object, indicating that the current user is an Exchange user.</span></span> <span data-ttu-id="f6513-137">Если текущий пользователь является пользователем Exchange, процедура CreateManagerRule получает руководителя текущего пользователя путем вызова метода [GetExchangeUserManager()](https://msdn.microsoft.com/library/bb646656\(v=office.15\)) для объекта **ExchangeUser** свойства **CurrentUser** объекта **NameSpace**.</span><span class="sxs-lookup"><span data-stu-id="f6513-137">If the current user is an Exchange user,   gets the current user's manager by calling the GetExchangeUserManager() method on the ExchangeUser object of the CurrentUser property of the NameSpace object.</span></span> <span data-ttu-id="f6513-138">После этого создается правило получения для перемещения полученных сообщений во вложенную папку папки "Входящие" для следующих условий:</span><span class="sxs-lookup"><span data-stu-id="f6513-138">A receive rule is then created to move received messages to a subfolder of the Inbox for the following conditions:</span></span>

- <span data-ttu-id="f6513-139">сообщение получено от руководителя пользователя;</span><span class="sxs-lookup"><span data-stu-id="f6513-139">The message is from the user’s manager.</span></span>

- <span data-ttu-id="f6513-140">получатель указан в строке **Кому:** сообщения;</span><span class="sxs-lookup"><span data-stu-id="f6513-140">The recipient is on the **To:** line of the message.</span></span>

- <span data-ttu-id="f6513-141">сообщение не является приглашением на собрание или обновлением.</span><span class="sxs-lookup"><span data-stu-id="f6513-141">The message is not a meeting request or update.</span></span>

<span data-ttu-id="f6513-p112">В завершение сообщение помечается к исполнению за сегодняшний день. В процедуре CreateManagerRule также реализован правильный порядок обработки ошибок при условиях, которые могут привести к возникновению исключений, например в случае перехода пользователя в автономный режим или отключения в режиме Exchange с кэшированием. </span><span class="sxs-lookup"><span data-stu-id="f6513-p112">Finally, the message is flagged for follow-up today. CreateManagerRule also illustrates appropriate error handling for conditions that could raise an exception such as the user being offline or disconnected in cached Exchange mode.</span></span>

<span data-ttu-id="f6513-144">Если вы используете Visual Studio для тестирования этого примера кода, сначала добавьте ссылку на компонент Microsoft Outlook 15.0 Object Library и задайте переменную Outlook при импорте пространства имен **Microsoft.Office.Interop.Outlook**.</span><span class="sxs-lookup"><span data-stu-id="f6513-144">If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the   variable when you import the Microsoft.Office.Interop.Outlook namespace.</span></span> <span data-ttu-id="f6513-145">Инструкция **using** не должна идти непосредственно перед функциями в примере кода, но ее нужно добавить перед открытым объявлением Class.</span><span class="sxs-lookup"><span data-stu-id="f6513-145">The using statement must not occur directly before the functions in the code example but must be added before the public   declaration.</span></span> <span data-ttu-id="f6513-146">В следующей строке кода показано, как выполнить импорт и назначение в C\#.</span><span class="sxs-lookup"><span data-stu-id="f6513-146">The following line of code shows how to do the import and assignment in C#.</span></span>

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```csharp
private void CreateManagerRule()
{
    Outlook.ExchangeUser manager;
    Outlook.Folder managerFolder;
    Outlook.AddressEntry currentUser =
        Application.Session.CurrentUser.AddressEntry;
    if (currentUser.Type == "EX")
    {
        try
        {
            manager = currentUser.
                GetExchangeUser().GetExchangeUserManager();
        }
        catch
        {
            Debug.WriteLine("Could not obtain user's manager.");
            return;
        }
        Outlook.Rules rules;
        try
        {
            rules = Application.Session.DefaultStore.GetRules();
        }
        catch
        {
            Debug.WriteLine("Could not obtain rules collection.");
            return;
        }
        if (manager != null)
        {
            string displayName = manager.Name;
            Outlook.Folders folders =
                Application.Session.GetDefaultFolder(
                Outlook.OlDefaultFolders.olFolderInbox).Folders;
            try
            {
                managerFolder =
                    folders[displayName] as Outlook.Folder;
            }
            catch
            {
                managerFolder =
                    folders.Add(displayName, Type.Missing)
                    as Outlook.Folder;
            }
            Outlook.Rule rule = rules.Create(displayName,
                Outlook.OlRuleType.olRuleReceive);

            // Rule conditions
            // From condition
            rule.Conditions.From.Recipients.Add(
                manager.PrimarySmtpAddress);
            rule.Conditions.From.Recipients.ResolveAll();
            rule.Conditions.From.Enabled = true;

            // Sent only to me
            rule.Conditions.ToMe.Enabled = true;

            // Rule exceptions
            // Meeting invite or update
            rule.Exceptions.MeetingInviteOrUpdate.Enabled = true;

            // Rule actions
            // MarkAsTask action
            rule.Actions.MarkAsTask.MarkInterval =
                Outlook.OlMarkInterval.olMarkToday;
            rule.Actions.MarkAsTask.FlagTo = "Follow-up";
            rule.Actions.MarkAsTask.Enabled = true;

            // MoveToFolder action
            rule.Actions.MoveToFolder.Folder = managerFolder;
            rule.Actions.MoveToFolder.Enabled = true;
            try
            {
                rules.Save(true);
            }
            catch (Exception ex)
            {
                Debug.WriteLine(ex.Message);
            }
        }
    }
}
```

## <a name="see-also"></a><span data-ttu-id="f6513-147">См. также</span><span class="sxs-lookup"><span data-stu-id="f6513-147">See also</span></span>

- [<span data-ttu-id="f6513-148">Правила</span><span class="sxs-lookup"><span data-stu-id="f6513-148">Rules</span></span>](rules.md)


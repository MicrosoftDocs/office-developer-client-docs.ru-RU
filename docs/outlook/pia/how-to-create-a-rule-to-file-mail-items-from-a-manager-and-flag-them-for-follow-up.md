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
# <a name="create-a-rule-to-file-mail-items-from-a-manager-and-flag-them-for-follow-up"></a>Создание правила для передачи почтовых элементов от руководителя и их пометки к исполнению

В этом примере показано, как задать правило для передачи почтовых элементов от руководителя пользователя и пометить их к исполнению.

## <a name="example"></a>Пример

> [!NOTE] 
> Приведенный ниже пример кода представляет собой фрагмент из книги [Программирование приложений для Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).

Правила Outlook могут выполняться как на стороне сервера, так и на стороне клиента, в зависимости от типа учетной записи и правила. Существует несколько способов реализации правил в соответствии с принятой в организации схемой хранения элементов в почтовых ящиках. Например, можно создать иерархию вложенных папок, в которых будут храниться прочитанные и непрочитанные сообщения по теме. Также можно создать иерархию вложенных папок, упорядоченную по отправителю сообщения. Кроме того, можно назначать сообщениям категории и использовать папки поиска для сбора сообщений по категориям.

Объектная модель **Rules** содержит объект [Rule](https://msdn.microsoft.com/library/bb647152\(v=office.15\)) , представляющий правило в приложении Outlook, что позволяет создавать программным способом правила, реализующие принятую в организации схему, создавать уникальные правила для решений, а также обеспечивать развертывание определенных правил для групп пользователей. С помощью объектной модели **Rules** можно программным способом добавлять, изменять и удалять правила. С помощью коллекции [Rules](https://msdn.microsoft.com/library/bb622788\(v=office.15\)) и объекта **Rule** также можно получать доступ к правилам, определенным для сеанса, добавлять и удалять их. 

Объект **Rule** содержит свойство [RuleType](https://msdn.microsoft.com/library/bb645613\(v=office.15\)) , которое определяет тип правила (отправка или получение). Свойство **RuleType** устанавливается при создании правила и может быть изменено только посредством удаления правила или его повторного создания с другим значением свойства **RuleType**. Объекты [RuleAction](https://msdn.microsoft.com/library/bb644297\(v=office.15\)) и [RuleCondition](https://msdn.microsoft.com/library/bb612469\(v=office.15\)) , соответствующие объекты коллекций, производные действия и объекты условий обеспечивают дополнительные возможности по изменению действий и условий правил.

В объектной модели **Rules** поддерживаются не все правила, которые можно создать с помощью мастера правил и оповещений в интерфейсе пользователя Outlook, однако при этом обеспечивается поддержка наиболее распространенных действий и условий. Правила, создаваемые с помощью мастера правил и оповещений, которые применяются к сообщениям, в том числе к почтовым элементам, приглашениям на собрания, запросам на задачи, документам, уведомлениям о доставке, уведомлениям о прочтении, результатам голосования и уведомлениям об отсутствии на работе, также можно создавать программным способом.

Правило может выполняться на сервере Exchange или в клиенте Outlook при условии, что почтовый ящик текущего пользователя размещается на сервере Exchange. Свойство [IsLocalRule](https://msdn.microsoft.com/library/bb647386\(v=office.15\)) объекта **Rule** возвращает значение **true**, свидетельствующее о выполнении правила в клиенте и необходимости запуска приложения Outlook для выполнения правила. Если правило выполняется на сервере, для оценки условий и выполнения действий правила запускать приложение Outlook не требуется.

> [!NOTE]
> Отдельная коллекция, представляющая условия исключений из правила, не предусмотрена. Следует использовать свойство [Exceptions](https://docs.microsoft.com/dotnet/api/microsoft.office.interop.outlook._rule.exceptions?view=outlook-pia) объекта **Rule** для получение коллекции [RuleConditions](https://docs.microsoft.com/dotnet/api/microsoft.office.interop.outlook.ruleconditions?view=outlook-pia) , которая представляет условия исключений из правила.

Для создания правил с помощью объектной модели Outlook выполните следующие действия:

1.  Получите коллекцию **Rules** из свойства [DefaultStore](https://msdn.microsoft.com/library/bb623164\(v=office.15\)) объекта [NameSpace](https://msdn.microsoft.com/library/bb645857\(v=office.15\)) . Для этого вызовите метод [GetRules()](https://msdn.microsoft.com/library/bb609979\(v=office.15\)) для установленного по умолчанию объекта [Store](https://msdn.microsoft.com/library/bb609139\(v=office.15\)) . Используйте блок **try…catch** для учетной записи пользователя, находящегося в автономном режиме или отключенного от сервера Exchange. Это позволит исключить возникновение ошибки приложения Outlook.

2.  Вызовите метод [Create(String, OlRuleType)](https://msdn.microsoft.com/library/bb643857\(v=office.15\)) для объекта **Rules**, чтобы создать переменную экземпляра объекта **Rule**. Для этого укажите параметры Name и [OlRuleType](https://msdn.microsoft.com/library/bb645776\(v=office.15\)).

3.  С помощью коллекций [RuleActions](https://msdn.microsoft.com/library/bb610113\(v=office.15\)) и [RuleConditions](https://msdn.microsoft.com/library/bb610965\(v=office.15\)) включите действия, условия и исключения для объекта **Rule**. Обратите внимание, что условия, включенные в коллекции **RuleConditions**, возвращаемой свойством [Exceptions](https://msdn.microsoft.com/library/bb609880\(v=office.15\)) , обрабатываются как условия исключений из правила и добавление встроенных настраиваемых действий и условий в эту коллекцию не поддерживается.

4.  Присвойте свойству [Enabled](https://msdn.microsoft.com/library/bb609147\(v=office.15\)) значение **true** для любого подлежащего исполнению действия, условия или исключения. Для некоторых действий и свойств, например для свойства [Folder](https://msdn.microsoft.com/library/bb646755\(v=office.15\)) , требуется настройка дополнительных свойств, позволяющих сохранять объект **Rule** без ошибок.

5.  В завершение вызовите метод [Save(Object)](https://msdn.microsoft.com/library/bb610738\(v=office.15\)) для коллекции **Rules**, чтобы сохранить созданные или измененные правила. Для обработки исключений метод **Save** следует заключить в блок **try…catch**.

В следующем примере кода в процедуре CreateManagerRule реализованы описанные выше действия. В процедуре CreateManagerRule сначала проверяется, представляет ли свойство [CurrentUser](https://msdn.microsoft.com/library/bb622574\(v=office.15\)) объект [ExchangeUser](https://msdn.microsoft.com/library/bb609574\(v=office.15\)), который определяет, является ли текущий пользователь пользователем Exchange. Если текущий пользователь является пользователем Exchange, процедура CreateManagerRule получает руководителя текущего пользователя путем вызова метода [GetExchangeUserManager()](https://msdn.microsoft.com/library/bb646656\(v=office.15\)) для объекта **ExchangeUser** свойства **CurrentUser** объекта **NameSpace**. После этого создается правило получения для перемещения полученных сообщений во вложенную папку папки "Входящие" для следующих условий:

- сообщение получено от руководителя пользователя;

- получатель указан в строке **Кому:** сообщения;

- сообщение не является приглашением на собрание или обновлением.

В завершение сообщение помечается к исполнению за сегодняшний день. В процедуре CreateManagerRule также реализован правильный порядок обработки ошибок при условиях, которые могут привести к возникновению исключений, например в случае перехода пользователя в автономный режим или отключения в режиме Exchange с кэшированием. 

Если вы используете Visual Studio для тестирования этого примера кода, сначала добавьте ссылку на компонент Microsoft Outlook 15.0 Object Library и задайте переменную Outlook при импорте пространства имен **Microsoft.Office.Interop.Outlook**. Инструкция **using** не должна идти непосредственно перед функциями в примере кода, но ее нужно добавить перед открытым объявлением Class. В следующей строке кода показано, как выполнить импорт и назначение в C\#.

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

## <a name="see-also"></a>См. также

- [Правила](rules.md)


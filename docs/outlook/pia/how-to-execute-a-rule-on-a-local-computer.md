---
title: Выполнение правила на локальном компьютере
TOCTitle: Execute a rule on a local computer
ms:assetid: 65e91010-3e4c-4921-a0fb-ad90a7b841b2
ms:mtpsurl: https://msdn.microsoft.com/library/Ff424471(v=office.15)
ms:contentKeyID: 55119883
ms.date: 07/24/2014
mtps_version: v=office.15
ms.openlocfilehash: 76587a72d9c77a5484d9aa9788173f9f40f57614
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25405842"
---
# <a name="execute-a-rule-on-a-local-computer"></a><span data-ttu-id="6cb22-102">Выполнение правила на локальном компьютере</span><span class="sxs-lookup"><span data-stu-id="6cb22-102">Execute a rule on a local computer</span></span>

<span data-ttu-id="6cb22-103">В этом примере показано, как выполнять правило на локальном компьютере с помощью свойства [OnLocalMachine](https://msdn.microsoft.com/library/bb612005\(v=office.15\)) объекта [RuleConditions](https://msdn.microsoft.com/library/bb610965\(v=office.15\)).</span><span class="sxs-lookup"><span data-stu-id="6cb22-103">This example shows how to execute a rule on a local computer by using the [OnLocalMachine](https://msdn.microsoft.com/library/bb612005\(v=office.15\)) property of the [RuleConditions](https://msdn.microsoft.com/library/bb610965\(v=office.15\)) object.</span></span>

## <a name="example"></a><span data-ttu-id="6cb22-104">Пример</span><span class="sxs-lookup"><span data-stu-id="6cb22-104">Example</span></span>

> [!NOTE] 
> <span data-ttu-id="6cb22-105">Приведенный ниже пример кода представляет собой фрагмент из книги [Программирование приложений для Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).</span><span class="sxs-lookup"><span data-stu-id="6cb22-105">The following code example is an excerpt from  [Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493)  , from Microsoft Press (ISBN 9780735622494, copyright Microsoft Press 2007, all rights reserved).</span></span>

<span data-ttu-id="6cb22-p101">Если почтовый ящик размещается на сервере Exchange, правило может выполняться на сервере Exchange или в клиенте Outlook. Если правило выполняется на сервере, для оценки условий правила и выполнения действий правила не требуется запускать Outlook. Для выполнения правила в клиенте требуется запускать приложение Outlook. Если свойство [IsLocalRule](https://msdn.microsoft.com/library/bb647386\(v=office.15\)) объекта [Rule](https://msdn.microsoft.com/library/bb647152\(v=office.15\)) возвращает значение **true**, правило выполняется в клиенте.</span><span class="sxs-lookup"><span data-stu-id="6cb22-p101">If your mailbox is hosted on an Exchange server, a rule can be executed on the Exchange server or on the Outlook client. If the rule is executed on the server, Outlook does not have to be running for the rule conditions to be evaluated and the rule actions to be completed. If the rule is executed on the client, Outlook must be running for the rule to execute. If the [IsLocalRule](https://msdn.microsoft.com/library/bb647386\(v=office.15\)) property of the [Rule](https://msdn.microsoft.com/library/bb647152\(v=office.15\)) object returns **true**, the rule is executed on the client.</span></span>

<span data-ttu-id="6cb22-110">Для действий правила, по умолчанию выполняемых в клиенте (например, отображение оповещений о новых сообщениях), условие **OnLocalMachine** включается автоматически, а свойству [Enabled](https://msdn.microsoft.com/library/bb611875\(v=office.15\)) присваивается значение **true** только для объекта [RuleAction](https://msdn.microsoft.com/library/bb644297\(v=office.15\)), расположенного на стороне клиента.</span><span class="sxs-lookup"><span data-stu-id="6cb22-110">For rule actions that execute on the client by default (such as displaying a new mail alert), the **OnLocalMachine** condition will automatically be enabled, and the [Enabled](https://msdn.microsoft.com/library/bb611875\(v=office.15\)) property is set to **true** for a client-side-only [RuleAction](https://msdn.microsoft.com/library/bb644297\(v=office.15\)) object.</span></span> <span data-ttu-id="6cb22-111">Для действий правила, обычно выполняемых на сервере, задайте свойство **Enabled** только для объекта **RuleAction**, расположенного на стороне клиента, чтобы включить условие **OnLocalMachine**.</span><span class="sxs-lookup"><span data-stu-id="6cb22-111">For rule actions that generally execute on the server, set the **Enabled** property of the client-side-only **RuleAction** object to enable the **OnLocalMachine** condition.</span></span> <span data-ttu-id="6cb22-112">В этом случае правило будет принудительно выполняться локально в клиенте.</span><span class="sxs-lookup"><span data-stu-id="6cb22-112">This will force the rule to execute locally on the client.</span></span> 

<span data-ttu-id="6cb22-113">Если условие **OnLocalMachine** для правила включено, условие [OnOtherMachine](https://msdn.microsoft.com/library/bb624486\(v=office.15\)) также будет включено при выполнении этого правила на другом компьютере.</span><span class="sxs-lookup"><span data-stu-id="6cb22-113">When the **OnLocalMachine** condition for a rule is enabled, the [OnOtherMachine](https://msdn.microsoft.com/library/bb624486\(v=office.15\)) condition will also be enabled when the same rule is examined from another machine.</span></span> <span data-ttu-id="6cb22-114">Условие правила типа [olConditionOtherMachine](https://msdn.microsoft.com/library/bb645741\(v=office.15\)) означает, что правило может выполняться только на заданном компьютере, отличном от текущего, и не может включаться и отключаться программным способом.</span><span class="sxs-lookup"><span data-stu-id="6cb22-114">A rule condition of type [olConditionOtherMachine](https://msdn.microsoft.com/library/bb645741\(v=office.15\)) indicates that the rule can execute only on a specific computer other than the current one, and cannot be programmatically enabled or disabled.</span></span> <span data-ttu-id="6cb22-115">Например, если правило создано на текущем компьютере и включено условие правила **OnLocalMachine**, правило может выполняться только на локальном компьютере.</span><span class="sxs-lookup"><span data-stu-id="6cb22-115">For example, if a rule is created on the current computer and the **OnLocalMachine** rule condition is enabled, the rule can execute only on that computer.</span></span> <span data-ttu-id="6cb22-116">Если это же правило выполняется на другом компьютере, правило будет показывать, что включено условие правила **OnOtherMachine**.</span><span class="sxs-lookup"><span data-stu-id="6cb22-116">If the same rule is executed on another computer, the rule will show that the **OnOtherMachine** rule condition is enabled.</span></span>

<span data-ttu-id="6cb22-117">В представленном ниже примере кода DemoOnMachineOnly создает правило и включает условие [OnlyToMe](https://msdn.microsoft.com/library/bb609250\(v=office.15\)) и действие [Forward](https://msdn.microsoft.com/library/bb652908\(v=office.15\)) путем присвоения для свойств **Enabled** значения **true**.</span><span class="sxs-lookup"><span data-stu-id="6cb22-117">In the following code example, DemoOnMachineOnly creates a rule and enables the [OnlyToMe](https://msdn.microsoft.com/library/bb609250\(v=office.15\)) condition and [Forward](https://msdn.microsoft.com/library/bb652908\(v=office.15\)) action by setting the **Enabled** properties to **true**.</span></span> <span data-ttu-id="6cb22-118">Затем включается условие **OnLocalMachine**, приводящее к локальному выполнению серверного правила, и правила сохраняются.</span><span class="sxs-lookup"><span data-stu-id="6cb22-118">The **OnLocalMachine** condition is then enabled, forcing a server-side rule to execute locally, and the rules are saved.</span></span> <span data-ttu-id="6cb22-119">По умолчанию действие **Forward** и условие **OnlyToMe** выполняются на сервере.</span><span class="sxs-lookup"><span data-stu-id="6cb22-119">By default, a **Forward** action and **OnlyToMe** condition will operate on the server.</span></span> <span data-ttu-id="6cb22-120">После включения условия **OnLocalMachine** они выполняются в качестве клиентского правила.</span><span class="sxs-lookup"><span data-stu-id="6cb22-120">Once the **OnLocalMachine** condition has been enabled, they will operate as a client-side rule.</span></span>

<span data-ttu-id="6cb22-121">Если вы используете Visual Studio для тестирования этого примера кода, сначала добавьте ссылку на компонент Microsoft Outlook 15.0 Object Library и задайте переменную Outlook при импорте пространства имен **Microsoft.Office.Interop.Outlook**.</span><span class="sxs-lookup"><span data-stu-id="6cb22-121">If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the   variable when you import the Microsoft.Office.Interop.Outlook namespace.</span></span> <span data-ttu-id="6cb22-122">Инструкция **using** не должна идти непосредственно перед функциями в примере кода, но ее нужно добавить перед открытым объявлением Class.</span><span class="sxs-lookup"><span data-stu-id="6cb22-122">The using statement must not occur directly before the functions in the code example but must be added before the public   declaration.</span></span> <span data-ttu-id="6cb22-123">В следующей строке кода показано, как выполнить импорт и назначение в C\#.</span><span class="sxs-lookup"><span data-stu-id="6cb22-123">The following line of code shows how to do the import and assignment in C#.</span></span>

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```csharp
private void DemoOnMachineOnly()
{
    Outlook.Rules rules =
        Application.Session.DefaultStore.GetRules();
    Outlook.Rule rule =
        rules.Create("Demo Machine Only Rule",
        Outlook.OlRuleType.olRuleReceive);
    rule.Conditions.OnlyToMe.Enabled = true;
    rule.Actions.Forward.Enabled = true;
    rule.Actions.Forward.Recipients.Add("someone@example.com");
    rule.Actions.Forward.Recipients.ResolveAll();

    // Force the rule to execute locally
    rule.Conditions.OnLocalMachine.Enabled = true;
    rules.Save(true);
}
```

## <a name="see-also"></a><span data-ttu-id="6cb22-124">См. также</span><span class="sxs-lookup"><span data-stu-id="6cb22-124">See also</span></span>

- [<span data-ttu-id="6cb22-125">Правила</span><span class="sxs-lookup"><span data-stu-id="6cb22-125">Rules</span></span>](rules.md)


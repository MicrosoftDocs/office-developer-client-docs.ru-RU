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
# <a name="execute-a-rule-on-a-local-computer"></a>Выполнение правила на локальном компьютере

В этом примере показано, как выполнять правило на локальном компьютере с помощью свойства [OnLocalMachine](https://msdn.microsoft.com/library/bb612005\(v=office.15\)) объекта [RuleConditions](https://msdn.microsoft.com/library/bb610965\(v=office.15\)).

## <a name="example"></a>Пример

> [!NOTE] 
> Приведенный ниже пример кода представляет собой фрагмент из книги [Программирование приложений для Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).

Если почтовый ящик размещается на сервере Exchange, правило может выполняться на сервере Exchange или в клиенте Outlook. Если правило выполняется на сервере, для оценки условий правила и выполнения действий правила не требуется запускать Outlook. Для выполнения правила в клиенте требуется запускать приложение Outlook. Если свойство [IsLocalRule](https://msdn.microsoft.com/library/bb647386\(v=office.15\)) объекта [Rule](https://msdn.microsoft.com/library/bb647152\(v=office.15\)) возвращает значение **true**, правило выполняется в клиенте.

Для действий правила, по умолчанию выполняемых в клиенте (например, отображение оповещений о новых сообщениях), условие **OnLocalMachine** включается автоматически, а свойству [Enabled](https://msdn.microsoft.com/library/bb611875\(v=office.15\)) присваивается значение **true** только для объекта [RuleAction](https://msdn.microsoft.com/library/bb644297\(v=office.15\)), расположенного на стороне клиента. Для действий правила, обычно выполняемых на сервере, задайте свойство **Enabled** только для объекта **RuleAction**, расположенного на стороне клиента, чтобы включить условие **OnLocalMachine**. В этом случае правило будет принудительно выполняться локально в клиенте. 

Если условие **OnLocalMachine** для правила включено, условие [OnOtherMachine](https://msdn.microsoft.com/library/bb624486\(v=office.15\)) также будет включено при выполнении этого правила на другом компьютере. Условие правила типа [olConditionOtherMachine](https://msdn.microsoft.com/library/bb645741\(v=office.15\)) означает, что правило может выполняться только на заданном компьютере, отличном от текущего, и не может включаться и отключаться программным способом. Например, если правило создано на текущем компьютере и включено условие правила **OnLocalMachine**, правило может выполняться только на локальном компьютере. Если это же правило выполняется на другом компьютере, правило будет показывать, что включено условие правила **OnOtherMachine**.

В представленном ниже примере кода DemoOnMachineOnly создает правило и включает условие [OnlyToMe](https://msdn.microsoft.com/library/bb609250\(v=office.15\)) и действие [Forward](https://msdn.microsoft.com/library/bb652908\(v=office.15\)) путем присвоения для свойств **Enabled** значения **true**. Затем включается условие **OnLocalMachine**, приводящее к локальному выполнению серверного правила, и правила сохраняются. По умолчанию действие **Forward** и условие **OnlyToMe** выполняются на сервере. После включения условия **OnLocalMachine** они выполняются в качестве клиентского правила.

Если вы используете Visual Studio для тестирования этого примера кода, сначала добавьте ссылку на компонент Microsoft Outlook 15.0 Object Library и задайте переменную Outlook при импорте пространства имен **Microsoft.Office.Interop.Outlook**. Инструкция **using** не должна идти непосредственно перед функциями в примере кода, но ее нужно добавить перед открытым объявлением Class. В следующей строке кода показано, как выполнить импорт и назначение в C\#.

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

## <a name="see-also"></a>См. также

- [Правила](rules.md)


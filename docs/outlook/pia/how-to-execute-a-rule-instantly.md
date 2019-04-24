---
title: Мгновенное выполнение правила
TOCTitle: Execute a rule instantly
ms:assetid: b41031d5-aa81-40e2-ae78-b45a2f79eb5d
ms:mtpsurl: https://msdn.microsoft.com/library/Ff424476(v=office.15)
ms:contentKeyID: 55119919
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: a6bb6ac5422b9785660cb3ec0020c01244002c6b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32320372"
---
# <a name="execute-a-rule-instantly"></a>Мгновенное выполнение правила

В этом примере показано мгновенное выполнение правила с помощью метода [Execute(Object, Object, Object, Object)](https://msdn.microsoft.com/library/bb645769\(v=office.15\)) объекта [Rule](https://msdn.microsoft.com/library/bb647152\(v=office.15\)).

## <a name="example"></a>Пример

> [!NOTE] 
> Приведенный ниже пример кода представляет собой фрагмент из книги [Программирование приложений для Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).

Для немедленного выполнения правила следует вызвать метод **Execute** объекта **Rule**. Параметры метода **Execute** являются необязательными. Если параметры метода не заданы, правило применяется ко всем сообщениям в папке "Входящие", однако не затрагивает ее вложенные папки. При этом используются значения параметров по умолчанию. В следующей таблице перечислены значения по умолчанию для необязательных параметров метода **Execute**.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Параметр</p></th>
<th><p>Значение по умолчанию</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>ShowProgress</p></td>
<td><p>False</p></td>
</tr>
<tr class="even">
<td><p>Folder</p></td>
<td><p>Inbox</p></td>
</tr>
<tr class="odd">
<td><p>IncludeSubfolders</p></td>
<td><p>False</p></td>
</tr>
<tr class="even">
<td><p>RuleExecuteOption</p></td>
<td><p>OlRuleExecuteOption.olRuleExecuteAllMessages</p></td>
</tr>
</tbody>
</table>


Выполнение правила можно отменить с помощью мастера правил и оповещений. Также можно отменить выполнение правила, присвоив параметру *ShowProgress* значение **true**, а затем выбрав команду отмены в диалоговом окне хода выполнения процесса. После отмены в диалоговом окне хода выполнения процесса метод **Execute** вернет ошибку.

В следующем примере кода процедура ExecuteManagerRule получает правило, созданное в процедуре CreateManagerRule раздела [Создание правила для передачи почтовых элементов от руководителя и их пометки к исполнению](how-to-create-a-rule-to-file-mail-items-from-a-manager-and-flag-them-for-follow-up.md). После этого в процедуре ExecuteManagerRule проверяется, является ли правило пустой ссылкой. Если правило не является пустой ссылкой, в процедуре ExecuteManagerRule вызывается метод **Execute** правила с параметрами по умолчанию, в результате чего правило немедленно выполняется.

> [!NOTE]
> Чтобы выполнить правило однократно независимо от того, возвращает ли свойство [Enabled](https://msdn.microsoft.com/library/bb609147(v=office.15)) значение **true**, используйте метод **Rule.Execute**. Чтобы применить правило к текущему и последующим сеансам, используйте свойство **Rule.Enabled** и метод [Save(Object)](https://msdn.microsoft.com/library/bb610738(v=office.15)) .

Если вы используете Visual Studio для тестирования этого примера кода, сначала добавьте ссылку на компонент Microsoft Outlook 15.0 Object Library и задайте переменную Outlook при импорте пространства имен **Microsoft.Office.Interop.Outlook**. Инструкция **using** не должна находиться непосредственно перед функциями в примере кода, но ее нужно добавить перед объявлением общедоступного класса. В приведенной ниже строке кода показано, как выполнить импорт и назначение на языке C\#.

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```csharp
private void ExecuteManagerRule()
{
    Outlook.AddressEntry currentUser =
        Application.Session.CurrentUser.AddressEntry;
    if (currentUser.Type == "EX")
    {
        try
        {
            string managerName = currentUser.
                GetExchangeUser().GetExchangeUserManager().Name;
            Outlook.Rule managerRule =
                Application.Session.DefaultStore.GetRules()[managerName];
            if (managerRule != null)
            {
                managerRule.Execute(false, Type.Missing,
                    Type.Missing, Type.Missing);
            }
        }
        catch (Exception ex)
        {
            Debug.WriteLine(ex.Message);
        }
    }
}
```

## <a name="see-also"></a>См. также

- [Правила](rules.md)


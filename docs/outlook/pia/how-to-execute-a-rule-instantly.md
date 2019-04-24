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
# <a name="execute-a-rule-instantly"></a><span data-ttu-id="aebd0-102">Мгновенное выполнение правила</span><span class="sxs-lookup"><span data-stu-id="aebd0-102">Execute a rule instantly</span></span>

<span data-ttu-id="aebd0-103">В этом примере показано мгновенное выполнение правила с помощью метода [Execute(Object, Object, Object, Object)](https://msdn.microsoft.com/library/bb645769\(v=office.15\)) объекта [Rule](https://msdn.microsoft.com/library/bb647152\(v=office.15\)).</span><span class="sxs-lookup"><span data-stu-id="aebd0-103">This example shows how to execute a rule instantly by using the [Execute(Object, Object, Object, Object)](https://msdn.microsoft.com/library/bb645769\(v=office.15\)) method of the [Rule](https://msdn.microsoft.com/library/bb647152\(v=office.15\)) object.</span></span>

## <a name="example"></a><span data-ttu-id="aebd0-104">Пример</span><span class="sxs-lookup"><span data-stu-id="aebd0-104">Example</span></span>

> [!NOTE] 
> <span data-ttu-id="aebd0-105">Приведенный ниже пример кода представляет собой фрагмент из книги [Программирование приложений для Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).</span><span class="sxs-lookup"><span data-stu-id="aebd0-105">The following code example is an excerpt from [Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).</span></span>

<span data-ttu-id="aebd0-p101">Для немедленного выполнения правила следует вызвать метод **Execute** объекта **Rule**. Параметры метода **Execute** являются необязательными. Если параметры метода не заданы, правило применяется ко всем сообщениям в папке "Входящие", однако не затрагивает ее вложенные папки. При этом используются значения параметров по умолчанию. В следующей таблице перечислены значения по умолчанию для необязательных параметров метода **Execute**.</span><span class="sxs-lookup"><span data-stu-id="aebd0-p101">You can cause a rule to execute immediately by calling the **Execute** method on the **Rule** object. The parameters to the **Execute** method are optional; if they are not specified, the rule will be applied to all messages in the Inbox but not to the subfolders of the Inbox, and default values for the parameters will be used. The following table lists the default values for the optional parameters of the **Execute** method.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="aebd0-109">Параметр</span><span class="sxs-lookup"><span data-stu-id="aebd0-109">Parameter</span></span></p></th>
<th><p><span data-ttu-id="aebd0-110">Значение по умолчанию</span><span class="sxs-lookup"><span data-stu-id="aebd0-110">Default value</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="aebd0-111">ShowProgress</span><span class="sxs-lookup"><span data-stu-id="aebd0-111">ShowProgress</span></span></p></td>
<td><p><span data-ttu-id="aebd0-112">False</span><span class="sxs-lookup"><span data-stu-id="aebd0-112">False</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="aebd0-113">Folder</span><span class="sxs-lookup"><span data-stu-id="aebd0-113">Folder</span></span></p></td>
<td><p><span data-ttu-id="aebd0-114">Inbox</span><span class="sxs-lookup"><span data-stu-id="aebd0-114">Inbox</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="aebd0-115">IncludeSubfolders</span><span class="sxs-lookup"><span data-stu-id="aebd0-115">IncludeSubfolders</span></span></p></td>
<td><p><span data-ttu-id="aebd0-116">False</span><span class="sxs-lookup"><span data-stu-id="aebd0-116">False</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="aebd0-117">RuleExecuteOption</span><span class="sxs-lookup"><span data-stu-id="aebd0-117">RuleExecuteOption</span></span></p></td>
<td><p><span data-ttu-id="aebd0-118">OlRuleExecuteOption.olRuleExecuteAllMessages</span><span class="sxs-lookup"><span data-stu-id="aebd0-118">OlRuleExecuteOption.olRuleExecuteAllMessages</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="aebd0-119">Выполнение правила можно отменить с помощью мастера правил и оповещений.</span><span class="sxs-lookup"><span data-stu-id="aebd0-119">You can cancel a rule execution by using the Rules and Alerts Wizard.</span></span> <span data-ttu-id="aebd0-120">Также можно отменить выполнение правила, присвоив параметру *ShowProgress* значение **true**, а затем выбрав команду отмены в диалоговом окне хода выполнения процесса.</span><span class="sxs-lookup"><span data-stu-id="aebd0-120">You can also cancel a rule execution by setting the *ShowProgress* parameter to **true** and then canceling the progress dialog box.</span></span> <span data-ttu-id="aebd0-121">После отмены в диалоговом окне хода выполнения процесса метод **Execute** вернет ошибку.</span><span class="sxs-lookup"><span data-stu-id="aebd0-121">Once you cancel the progress dialog box, **Execute** will return an error.</span></span>

<span data-ttu-id="aebd0-122">В следующем примере кода процедура ExecuteManagerRule получает правило, созданное в процедуре CreateManagerRule раздела [Создание правила для передачи почтовых элементов от руководителя и их пометки к исполнению](how-to-create-a-rule-to-file-mail-items-from-a-manager-and-flag-them-for-follow-up.md).</span><span class="sxs-lookup"><span data-stu-id="aebd0-122">In the following code example, ExecuteManagerRule gets the rule that was created in the procedure CreateManagerRule from the topic [Create a Rule to File Mail Items from a Manager and Flag Them for Follow-Up](how-to-create-a-rule-to-file-mail-items-from-a-manager-and-flag-them-for-follow-up.md).</span></span> <span data-ttu-id="aebd0-123">После этого в процедуре ExecuteManagerRule проверяется, является ли правило пустой ссылкой.</span><span class="sxs-lookup"><span data-stu-id="aebd0-123">ExecuteManagerRule then checks whether the rule is not a null reference.</span></span> <span data-ttu-id="aebd0-124">Если правило не является пустой ссылкой, в процедуре ExecuteManagerRule вызывается метод **Execute** правила с параметрами по умолчанию, в результате чего правило немедленно выполняется.</span><span class="sxs-lookup"><span data-stu-id="aebd0-124">If the rule is not a null reference, ExecuteManagerRule calls the **Execute** method on the rule with default parameters, instantly executing the rule.</span></span>

> [!NOTE]
> <span data-ttu-id="aebd0-p104">Чтобы выполнить правило однократно независимо от того, возвращает ли свойство [Enabled](https://msdn.microsoft.com/library/bb609147(v=office.15)) значение **true**, используйте метод **Rule.Execute**. Чтобы применить правило к текущему и последующим сеансам, используйте свойство **Rule.Enabled** и метод [Save(Object)](https://msdn.microsoft.com/library/bb610738(v=office.15)) .</span><span class="sxs-lookup"><span data-stu-id="aebd0-p104">To apply a rule once, regardless of whether the [Enabled](https://msdn.microsoft.com/library/bb609147(v=office.15)) property returns **true**, use the **Rule.Execute** method. To apply the rule for the current session and beyond the current session, use both the **Rule.Enabled** property and the [Save(Object)](https://msdn.microsoft.com/library/bb610738(v=office.15)) method.</span></span>

<span data-ttu-id="aebd0-127">Если вы используете Visual Studio для тестирования этого примера кода, сначала добавьте ссылку на компонент Microsoft Outlook 15.0 Object Library и задайте переменную Outlook при импорте пространства имен **Microsoft.Office.Interop.Outlook**.</span><span class="sxs-lookup"><span data-stu-id="aebd0-127">If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the Outlook variable when you import the **Microsoft.Office.Interop.Outlook** namespace.</span></span> <span data-ttu-id="aebd0-128">Инструкция **using** не должна находиться непосредственно перед функциями в примере кода, но ее нужно добавить перед объявлением общедоступного класса.</span><span class="sxs-lookup"><span data-stu-id="aebd0-128">The **using** statement must not occur directly before the functions in the code example but must be added before the public Class declaration.</span></span> <span data-ttu-id="aebd0-129">В приведенной ниже строке кода показано, как выполнить импорт и назначение на языке C\#.</span><span class="sxs-lookup"><span data-stu-id="aebd0-129">The following line of code shows how to do the import and assignment in C\#.</span></span>

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

## <a name="see-also"></a><span data-ttu-id="aebd0-130">См. также</span><span class="sxs-lookup"><span data-stu-id="aebd0-130">See also</span></span>

- [<span data-ttu-id="aebd0-131">Правила</span><span class="sxs-lookup"><span data-stu-id="aebd0-131">Rules</span></span>](rules.md)


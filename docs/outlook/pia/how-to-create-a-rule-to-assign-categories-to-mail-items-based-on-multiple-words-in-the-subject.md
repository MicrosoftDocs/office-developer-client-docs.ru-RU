---
title: Создание правила для назначения категорий почтовым элементам с учетом нескольких слов в теме
TOCTitle: Create a rule to assign categories to mail items based on multiple words in the subject
ms:assetid: 6e1fa40c-edf3-407c-9e90-99f634fa8e24
ms:mtpsurl: https://msdn.microsoft.com/library/Ff424472(v=office.15)
ms:contentKeyID: 55119918
ms.date: 07/24/2014
mtps_version: v=office.15
ms.openlocfilehash: 1ff096454aa15a0a45c423913140eb50e6de9678
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25406325"
---
# <a name="create-a-rule-to-assign-categories-to-mail-items-based-on-multiple-words-in-the-subject"></a><span data-ttu-id="f6c31-102">Создание правила для назначения категорий почтовым элементам с учетом нескольких слов в теме</span><span class="sxs-lookup"><span data-stu-id="f6c31-102">Create a rule to assign categories to mail items based on multiple words in the subject</span></span>

<span data-ttu-id="f6c31-103">В этом примере показано, как задать правило, которое назначает категории почтовым элементам с учетом нескольких слов в теме.</span><span class="sxs-lookup"><span data-stu-id="f6c31-103">This example shows how to set up a rule that assigns categories to mail items based on multiple words in the subject.</span></span>

## <a name="example"></a><span data-ttu-id="f6c31-104">Пример</span><span class="sxs-lookup"><span data-stu-id="f6c31-104">Example</span></span>

> [!NOTE] 
> <span data-ttu-id="f6c31-105">Приведенный ниже пример кода взят из книги [Программирование приложений для Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).</span><span class="sxs-lookup"><span data-stu-id="f6c31-105">The following code example is an excerpt from  [Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493)  , from Microsoft Press (ISBN 9780735622494, copyright Microsoft Press 2007, all rights reserved).</span></span>

<span data-ttu-id="f6c31-106">Элементы в Outlook можно классифицировать для упрощения организации и отображения.</span><span class="sxs-lookup"><span data-stu-id="f6c31-106">In Outlook, items can be categorized for easier organization and display.</span></span> <span data-ttu-id="f6c31-107">Объектная модель Outlook предоставляет объект [Category](https://msdn.microsoft.com/library/bb623480\(v=office.15\)) и коллекцию [Categories](https://msdn.microsoft.com/library/bb623535\(v=office.15\)) для представления категорий.</span><span class="sxs-lookup"><span data-stu-id="f6c31-107">The Outlook object model provides the [Category](https://msdn.microsoft.com/library/bb623480\(v=office.15\)) object and the [Categories](https://msdn.microsoft.com/library/bb623535\(v=office.15\)) collection to represent categories.</span></span> <span data-ttu-id="f6c31-108">Дополнительные сведения об объекте **Category** и коллекции **Categories** элемента Outlook см. в статье [Перечисление и добавление категорий](how-to-enumerate-and-add-categories.md).</span><span class="sxs-lookup"><span data-stu-id="f6c31-108">In Outlook, items can be categorized for easier organization and display. The Outlook object model provides the Category object and the Categories collection to represent categories. For more information about the Category object and the Categories collection for an Outlook item, see How to: Enumerate and Add Categories.</span></span>

<span data-ttu-id="f6c31-109">Правило, представленное объектом [Rule](https://msdn.microsoft.com/library/bb647152\(v=office.15\)), можно назначить с несколькими условиями.</span><span class="sxs-lookup"><span data-stu-id="f6c31-109">A rule, represented by a [Rule](https://msdn.microsoft.com/library/bb647152\(v=office.15\)) object, can be assigned with multiple conditions.</span></span> <span data-ttu-id="f6c31-110">Можно получить или задать массив, представляющий условия для оценки или действия для выполнения.</span><span class="sxs-lookup"><span data-stu-id="f6c31-110">You can get or set an array that represents conditions to be evaluated or actions to be completed.</span></span> <span data-ttu-id="f6c31-111">Например, свойство [Text](https://msdn.microsoft.com/library/bb611271\(v=office.15\)) объекта [TextRuleCondition](https://msdn.microsoft.com/library/bb644796\(v=office.15\)) возвращает или задает массив элементов строки, представляющий текст для оценки условиями правила.</span><span class="sxs-lookup"><span data-stu-id="f6c31-111">For example, the [Text](https://msdn.microsoft.com/library/bb611271\(v=office.15\)) property of the [TextRuleCondition](https://msdn.microsoft.com/library/bb644796\(v=office.15\)) object returns or sets an array of string elements that represents the text to be evaluated by the rule condition.</span></span> <span data-ttu-id="f6c31-112">Необходимо назначить массив с одной или несколькими строками для оценки.</span><span class="sxs-lookup"><span data-stu-id="f6c31-112">You must assign an array with one string or multiple strings for evaluation.</span></span> <span data-ttu-id="f6c31-113">Чтобы оценить несколько текстовых строк, назначенных в массиве, используйте логическую операцию OR.</span><span class="sxs-lookup"><span data-stu-id="f6c31-113">To evaluate multiple text strings that are assigned in an array, use the logical OR operation.</span></span> 

<span data-ttu-id="f6c31-114">Для получения или задания массива можно использовать следующие свойства: [Address](https://msdn.microsoft.com/library/bb647045\(v=office.15\)), [Categories](https://msdn.microsoft.com/library/bb611021\(v=office.15\)), [Categories](https://msdn.microsoft.com/library/bb612345\(v=office.15\)), [FormName](https://msdn.microsoft.com/library/bb647042\(v=office.15\)) и **TextRuleCondition.Text**.</span><span class="sxs-lookup"><span data-stu-id="f6c31-114">The properties that you can use to get or set an array are as follows: [Address](https://msdn.microsoft.com/library/bb647045\(v=office.15\)), [Categories](https://msdn.microsoft.com/library/bb611021\(v=office.15\)), [Categories](https://msdn.microsoft.com/library/bb612345\(v=office.15\)), [FormName](https://msdn.microsoft.com/library/bb647042\(v=office.15\)), and **TextRuleCondition.Text**.</span></span> <span data-ttu-id="f6c31-115">Дополнительные сведения о правилах см. в статье [Создание правила для передачи почтовых элементов от руководителя и их пометки к исполнению](how-to-create-a-rule-to-file-mail-items-from-a-manager-and-flag-them-for-follow-up.md).</span><span class="sxs-lookup"><span data-stu-id="f6c31-115">[How to: Create a Rule to File Mail Items from a Manager and Flag Them for Follow-Up](how-to-create-a-rule-to-file-mail-items-from-a-manager-and-flag-them-for-follow-up.md)</span></span>

<span data-ttu-id="f6c31-116">В следующем примере в процедуре CreateTextAndCategoryRule используется метод CategoryExists для проверки почтовых элементов пользователя на наличие категорий, содержащих названия "Office" или "Outlook" в коллекции **Categories**.</span><span class="sxs-lookup"><span data-stu-id="f6c31-116">In the following example,   uses the   method to check the user's mail items for any categories by the name "Office" or "Outlook" in the Categories collection.</span></span> <span data-ttu-id="f6c31-117">Если категории не найдены, они будут добавлены.</span><span class="sxs-lookup"><span data-stu-id="f6c31-117">If no categories are found, they are added.</span></span> <span data-ttu-id="f6c31-118">Затем в этом примере создается массив строк, содержащий строки "Office", "Outlook" и "2007".</span><span class="sxs-lookup"><span data-stu-id="f6c31-118">The example then creates an array of strings that include "Office, "Outlook", and "2007".</span></span> <span data-ttu-id="f6c31-119">Этот массив представляет условия для оценки.</span><span class="sxs-lookup"><span data-stu-id="f6c31-119">This array will represent the conditions to be evaluated.</span></span> <span data-ttu-id="f6c31-120">После этого в процедуре CreateTextAndCategoryRule создается правило назначения категорий, в котором проверяется соответствие темы любому из заданных в массиве условий с использованием свойства **Text** объекта **TextRuleCondition** и свойства [BodyOrSubject](https://msdn.microsoft.com/library/bb612744\(v=office.15\)) коллекции [RuleConditions](https://msdn.microsoft.com/library/bb610965\(v=office.15\)).</span><span class="sxs-lookup"><span data-stu-id="f6c31-120"> then creates a rule that assigns categories by examining the subject for any of the conditions in the array by using the Text property of the TextRuleCondition object and the BodyOrSubject property of the RuleConditions collection.</span></span> <span data-ttu-id="f6c31-121">Если условие соблюдается, категории Office и Outlook назначаются элементу с помощью метода [AssignToCategory](https://msdn.microsoft.com/library/bb623146\(v=office.15\)) объекта [RuleActions](https://msdn.microsoft.com/library/bb610113\(v=office.15\)) .</span><span class="sxs-lookup"><span data-stu-id="f6c31-121">If the condition is satisfied, the categories of Office and Outlook are assigned to the item by using the [AssignToCategory](https://msdn.microsoft.com/library/bb623146\(v=office.15\)) method of the [RuleActions](https://msdn.microsoft.com/library/bb610113\(v=office.15\)) object.</span></span>

<span data-ttu-id="f6c31-122">Если для тестирования этого примера кода вы используете Visual Studio, сначала добавьте ссылку на компонент библиотеки объектов Microsoft Outlook 15.0 и укажите переменную Outlook при импорте пространства имен **Microsoft.Office.Interop.Outlook**.</span><span class="sxs-lookup"><span data-stu-id="f6c31-122">If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the   variable when you import the Microsoft.Office.Interop.Outlook namespace.</span></span> <span data-ttu-id="f6c31-123">Не следует использовать инструкцию **using** непосредственно перед функциями в примере кода, но ее необходимо добавить перед объявлением общедоступного класса.</span><span class="sxs-lookup"><span data-stu-id="f6c31-123">The using statement must not occur directly before the functions in the code example but must be added before the public   declaration.</span></span> <span data-ttu-id="f6c31-124">В следующей строке кода показано, как выполнить импорт и назначение в C\#.</span><span class="sxs-lookup"><span data-stu-id="f6c31-124">The following line of code shows how to do the import and assignment in C#.</span></span>

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```csharp
private void CreateTextAndCategoryRule()
{
    if (!CategoryExists("Office"))
    {
        Application.Session.Categories.Add(
            "Office", Type.Missing, Type.Missing);
    }
    if (!CategoryExists("Outlook"))
    {
        Application.Session.Categories.Add(
            "Outlook", Type.Missing, Type.Missing);
    }
    Outlook.Rules rules =
        Application.Session.DefaultStore.GetRules();
    Outlook.Rule textRule =
        rules.Create("Demo Text and Category Rule",
        Outlook.OlRuleType.olRuleReceive);
    Object[] textCondition = 
        { "Office", "Outlook", "2007" };
    Object[] categoryAction = 
        { "Office", "Outlook" };
    textRule.Conditions.BodyOrSubject.Text =
        textCondition;
    textRule.Conditions.BodyOrSubject.Enabled = true;
    textRule.Actions.AssignToCategory.Categories =
        categoryAction;
    textRule.Actions.AssignToCategory.Enabled = true;
    rules.Save(true);
}

// Determines if categoryName exists in Categories collection
private bool CategoryExists(string categoryName)
{
    try
    {
        Outlook.Category category =
            Application.Session.Categories[categoryName];
        if (category != null)
        {
            return true;
        }
        else
        {
            return false;
        }
    }
    catch { return false; }
}
```

## <a name="see-also"></a><span data-ttu-id="f6c31-125">См. также</span><span class="sxs-lookup"><span data-stu-id="f6c31-125">See also</span></span>

- [<span data-ttu-id="f6c31-126">Правила</span><span class="sxs-lookup"><span data-stu-id="f6c31-126">Rules</span></span>](rules.md)


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
# <a name="create-a-rule-to-assign-categories-to-mail-items-based-on-multiple-words-in-the-subject"></a>Создание правила для назначения категорий почтовым элементам с учетом нескольких слов в теме

В этом примере показано, как задать правило, которое назначает категории почтовым элементам с учетом нескольких слов в теме.

## <a name="example"></a>Пример

> [!NOTE] 
> Приведенный ниже пример кода взят из книги [Программирование приложений для Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).

Элементы в Outlook можно классифицировать для упрощения организации и отображения. Объектная модель Outlook предоставляет объект [Category](https://msdn.microsoft.com/library/bb623480\(v=office.15\)) и коллекцию [Categories](https://msdn.microsoft.com/library/bb623535\(v=office.15\)) для представления категорий. Дополнительные сведения об объекте **Category** и коллекции **Categories** элемента Outlook см. в статье [Перечисление и добавление категорий](how-to-enumerate-and-add-categories.md).

Правило, представленное объектом [Rule](https://msdn.microsoft.com/library/bb647152\(v=office.15\)), можно назначить с несколькими условиями. Можно получить или задать массив, представляющий условия для оценки или действия для выполнения. Например, свойство [Text](https://msdn.microsoft.com/library/bb611271\(v=office.15\)) объекта [TextRuleCondition](https://msdn.microsoft.com/library/bb644796\(v=office.15\)) возвращает или задает массив элементов строки, представляющий текст для оценки условиями правила. Необходимо назначить массив с одной или несколькими строками для оценки. Чтобы оценить несколько текстовых строк, назначенных в массиве, используйте логическую операцию OR. 

Для получения или задания массива можно использовать следующие свойства: [Address](https://msdn.microsoft.com/library/bb647045\(v=office.15\)), [Categories](https://msdn.microsoft.com/library/bb611021\(v=office.15\)), [Categories](https://msdn.microsoft.com/library/bb612345\(v=office.15\)), [FormName](https://msdn.microsoft.com/library/bb647042\(v=office.15\)) и **TextRuleCondition.Text**. Дополнительные сведения о правилах см. в статье [Создание правила для передачи почтовых элементов от руководителя и их пометки к исполнению](how-to-create-a-rule-to-file-mail-items-from-a-manager-and-flag-them-for-follow-up.md).

В следующем примере в процедуре CreateTextAndCategoryRule используется метод CategoryExists для проверки почтовых элементов пользователя на наличие категорий, содержащих названия "Office" или "Outlook" в коллекции **Categories**. Если категории не найдены, они будут добавлены. Затем в этом примере создается массив строк, содержащий строки "Office", "Outlook" и "2007". Этот массив представляет условия для оценки. После этого в процедуре CreateTextAndCategoryRule создается правило назначения категорий, в котором проверяется соответствие темы любому из заданных в массиве условий с использованием свойства **Text** объекта **TextRuleCondition** и свойства [BodyOrSubject](https://msdn.microsoft.com/library/bb612744\(v=office.15\)) коллекции [RuleConditions](https://msdn.microsoft.com/library/bb610965\(v=office.15\)). Если условие соблюдается, категории Office и Outlook назначаются элементу с помощью метода [AssignToCategory](https://msdn.microsoft.com/library/bb623146\(v=office.15\)) объекта [RuleActions](https://msdn.microsoft.com/library/bb610113\(v=office.15\)) .

Если для тестирования этого примера кода вы используете Visual Studio, сначала добавьте ссылку на компонент библиотеки объектов Microsoft Outlook 15.0 и укажите переменную Outlook при импорте пространства имен **Microsoft.Office.Interop.Outlook**. Не следует использовать инструкцию **using** непосредственно перед функциями в примере кода, но ее необходимо добавить перед объявлением общедоступного класса. В следующей строке кода показано, как выполнить импорт и назначение в C\#.

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

## <a name="see-also"></a>См. также

- [Правила](rules.md)


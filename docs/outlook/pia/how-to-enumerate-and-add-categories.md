---
title: Перечисление и добавление категорий
TOCTitle: Enumerate and add categories
ms:assetid: 17a94a01-c463-4332-851e-7d280c66d8c2
ms:mtpsurl: https://msdn.microsoft.com/library/Ff424467(v=office.15)
ms:contentKeyID: 55119829
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 488e00971adb1f2fa38555039478ac830d3c9f7a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32320414"
---
# <a name="enumerate-and-add-categories"></a>Перечисление и добавление категорий

В этом примере показано, как перечислять категории и добавлять их в основной список категорий.

## <a name="example"></a>Пример

> [!NOTE] 
> Приведенный ниже пример кода представляет собой фрагмент из книги [Программирование приложений для Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).

Объектная модель Outlook поддерживает категории, которые помогают упорядочивать элементы в папке "Входящие" пользователя. Чтобы поддерживать более высокий уровень организации, можно выполнять указанные ниже действия.

- классифицировать элементы Outlook и отображать их по категориям;
- добавлять несколько цветовых категорий для одного элемента Outlook;
- группировать и упорядочивать элементы Outlook по цветовым категориям;
- назначать сочетания клавиш для каждой цветовой категории, облегчая пользователям процесс распределения элементов по категориям;
- создавать, удалять или изменять цветовые категории программным путем или с помощью действий пользователя в интерфейсе Outlook.

Чтобы выделить функции категорий, объектная модель Outlook содержит объект [Category](https://msdn.microsoft.com/library/bb623480\(v=office.15\)), который представляет одну пользовательскую цветовую категорию в основном списке категорий. Основной список категорий содержит цветовые категории, которые представлены в пользовательском интерфейсе Outlook. Список представлен коллекцией [Categories](https://msdn.microsoft.com/library/bb623535\(v=office.15\)) объекта [NameSpace](https://msdn.microsoft.com/library/bb645857\(v=office.15\)). Чтобы создать объект **Category**, используйте метод [Add(String, Object, Object)](https://msdn.microsoft.com/library/bb623093\(v=office.15\)) коллекции **Categories**. При создании объекта **Category** создается глобальный уникальный идентификатор (GUID), который нельзя изменить. Он представлен свойством [CategoryID](https://msdn.microsoft.com/library/bb647100\(v=office.15\)). Однако можно изменить имя, цвет и сочетание клавиш, связанные с цветовой категорией, задав свойства [Name](https://msdn.microsoft.com/library/bb645577\(v=office.15\)), [Color](https://msdn.microsoft.com/library/bb612316\(v=office.15\)) и [ShortcutKey](https://msdn.microsoft.com/library/bb644944\(v=office.15\)) соответственно для объекта **Category**. Можно изменить свойство **Color**, установив или получив его константу [OlCategoryColor](https://msdn.microsoft.com/library/bb608974\(v=office.15\)). Чтобы воспроизвести цвет в пользовательском элементе управления, используйте следующие нередактируемые свойства объекта **Category**:

  - [CategoryBorderColor](https://msdn.microsoft.com/library/bb610083\(v=office.15\))

  - [CategoryGradientBottomColor](https://msdn.microsoft.com/library/bb647357\(v=office.15\))

  - [CategoryGradientTopColor](https://msdn.microsoft.com/library/bb623975\(v=office.15\))

Эти свойства возвращают значение **OLE\_COLOR**, которое зависит от свойства **Color** объекта **Category**.

Элементы Outlook отображаются на основе имени категории. Каждый объект элемента имеет свойство **Categories**, в котором хранится строка с разделителями запятыми, представляющая названия категорий. (Например, для объекта [MailItem](https://msdn.microsoft.com/library/bb643865\(v=office.15\)) можно использовать свойство **MailItem** [Categories).](https://msdn.microsoft.com/library/bb646442\(v=office.15\)) Это позволяет добавлять категорию для элемента, даже если этой категории нет в основном списке категорий.


> [!NOTE]
> Если свойство **Categories** элемента содержит имя категории, не входящей в коллекцию **Categories** объекта **NameSpace**, то имя этой категории, связанной с элементом Outlook, отображается, но без соответствующего цвета. Свойство **Categories** объекта **Item** не возвращает коллекцию **Categories**.

В представленном ниже примере кода первая процедура EnumerateCategories получает основной список категорий текущего пользователя, представленный коллекцией **Categories**. Затем перечисляются объекты **Category** в этой коллекции и записываются свойства **Name** и **CategoryID** для отслеживания прослушивателей коллекции [Listeners](https://msdn.microsoft.com/library/system.diagnostics.debug.listeners.aspx). Вторая процедура AddACategory получает основной список категорий текущего пользователя и использует метод CategoryExists для проверки существования категории "ISV" в коллекции. Если категория с именем "ISV" не существует, процедура AddACategory добавляет категорию "ISV" в основной список категорий и назначает ей темно-синий цвет с помощью метода **Add** коллекции **Categories**. Для категории также назначается сочетание клавиш CTRL + F11.

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```csharp
private void EnumerateCategories()
{
    Outlook.Categories categories =
        Application.Session.Categories;
    foreach (Outlook.Category category in categories)
    {
        Debug.WriteLine(category.Name);
        Debug.WriteLine(category.CategoryID);
    }
}

private void AddACategory()
{
    Outlook.Categories categories =
        Application.Session.Categories;
    if (!CategoryExists("ISV"))
    {
        Outlook.Category category = categories.Add("ISV",
            Outlook.OlCategoryColor.olCategoryColorDarkBlue,
            Outlook.OlCategoryShortcutKey.olCategoryShortcutKeyCtrlF11);
    }
}

private bool CategoryExists(string categoryName)
{
    try
    {
        Outlook.Category category = 
            Application.Session.Categories[categoryName];
        if(category != null)
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

- [Цветовые категории](color-categories.md)


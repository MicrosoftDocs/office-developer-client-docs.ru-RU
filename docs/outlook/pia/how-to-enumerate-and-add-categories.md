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
# <a name="enumerate-and-add-categories"></a><span data-ttu-id="5d0f8-102">Перечисление и добавление категорий</span><span class="sxs-lookup"><span data-stu-id="5d0f8-102">Enumerate and add categories</span></span>

<span data-ttu-id="5d0f8-103">В этом примере показано, как перечислять категории и добавлять их в основной список категорий.</span><span class="sxs-lookup"><span data-stu-id="5d0f8-103">This example shows how to enumerate categories and add a category to the main category list.</span></span>

## <a name="example"></a><span data-ttu-id="5d0f8-104">Пример</span><span class="sxs-lookup"><span data-stu-id="5d0f8-104">Example</span></span>

> [!NOTE] 
> <span data-ttu-id="5d0f8-105">Приведенный ниже пример кода представляет собой фрагмент из книги [Программирование приложений для Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).</span><span class="sxs-lookup"><span data-stu-id="5d0f8-105">The following code example is an excerpt from [Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).</span></span>

<span data-ttu-id="5d0f8-106">Объектная модель Outlook поддерживает категории, которые помогают упорядочивать элементы в папке "Входящие" пользователя.</span><span class="sxs-lookup"><span data-stu-id="5d0f8-106">The Outlook object model supports categories that help organize items in a user’s Inbox.</span></span> <span data-ttu-id="5d0f8-107">Чтобы поддерживать более высокий уровень организации, можно выполнять указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="5d0f8-107">To maintain a higher level of organization, you can do the following:</span></span>

- <span data-ttu-id="5d0f8-108">классифицировать элементы Outlook и отображать их по категориям;</span><span class="sxs-lookup"><span data-stu-id="5d0f8-108">Categorize Outlook items and display them by category.</span></span>
- <span data-ttu-id="5d0f8-109">добавлять несколько цветовых категорий для одного элемента Outlook;</span><span class="sxs-lookup"><span data-stu-id="5d0f8-109">Apply multiple color categories to a single Outlook item.</span></span>
- <span data-ttu-id="5d0f8-110">группировать и упорядочивать элементы Outlook по цветовым категориям;</span><span class="sxs-lookup"><span data-stu-id="5d0f8-110">Group and sort Outlook items by color category.</span></span>
- <span data-ttu-id="5d0f8-111">назначать сочетания клавиш для каждой цветовой категории, облегчая пользователям процесс распределения элементов по категориям;</span><span class="sxs-lookup"><span data-stu-id="5d0f8-111">Assign shortcut keys to each color category, enabling users to more easily categorize items.</span></span>
- <span data-ttu-id="5d0f8-112">создавать, удалять или изменять цветовые категории программным путем или с помощью действий пользователя в интерфейсе Outlook.</span><span class="sxs-lookup"><span data-stu-id="5d0f8-112">Create, delete, and change color categories either programmatically, or by user action within the Outlook user interface.</span></span>

<span data-ttu-id="5d0f8-113">Чтобы выделить функции категорий, объектная модель Outlook содержит объект [Category](https://msdn.microsoft.com/library/bb623480\(v=office.15\)), который представляет одну пользовательскую цветовую категорию в основном списке категорий.</span><span class="sxs-lookup"><span data-stu-id="5d0f8-113">To expose the functionality of categories, the Outlook object model provides a [Category](https://msdn.microsoft.com/library/bb623480\(v=office.15\)) object that represents a single user-defined color category in the main category list.</span></span> <span data-ttu-id="5d0f8-114">Основной список категорий содержит цветовые категории, которые представлены в пользовательском интерфейсе Outlook.</span><span class="sxs-lookup"><span data-stu-id="5d0f8-114">The main category list contains color categories that are presented in the Outlook user interface.</span></span> <span data-ttu-id="5d0f8-115">Список представлен коллекцией [Categories](https://msdn.microsoft.com/library/bb623535\(v=office.15\)) объекта [NameSpace](https://msdn.microsoft.com/library/bb645857\(v=office.15\)).</span><span class="sxs-lookup"><span data-stu-id="5d0f8-115">The list is represented by the [Categories](https://msdn.microsoft.com/library/bb623535\(v=office.15\)) collection of the [NameSpace](https://msdn.microsoft.com/library/bb645857\(v=office.15\)) object.</span></span> <span data-ttu-id="5d0f8-116">Чтобы создать объект **Category**, используйте метод [Add(String, Object, Object)](https://msdn.microsoft.com/library/bb623093\(v=office.15\)) коллекции **Categories**.</span><span class="sxs-lookup"><span data-stu-id="5d0f8-116">To create a **Category** object, use the [Add(String, Object, Object)](https://msdn.microsoft.com/library/bb623093\(v=office.15\)) method of the **Categories** collection.</span></span> <span data-ttu-id="5d0f8-117">При создании объекта **Category** создается глобальный уникальный идентификатор (GUID), который нельзя изменить.</span><span class="sxs-lookup"><span data-stu-id="5d0f8-117">When you create a **Category** object, a globally unique identifier (GUID) is created, and this identifier cannot be changed.</span></span> <span data-ttu-id="5d0f8-118">Он представлен свойством [CategoryID](https://msdn.microsoft.com/library/bb647100\(v=office.15\)).</span><span class="sxs-lookup"><span data-stu-id="5d0f8-118">It is represented by the [CategoryID](https://msdn.microsoft.com/library/bb647100\(v=office.15\)) property.</span></span> <span data-ttu-id="5d0f8-119">Однако можно изменить имя, цвет и сочетание клавиш, связанные с цветовой категорией, задав свойства [Name](https://msdn.microsoft.com/library/bb645577\(v=office.15\)), [Color](https://msdn.microsoft.com/library/bb612316\(v=office.15\)) и [ShortcutKey](https://msdn.microsoft.com/library/bb644944\(v=office.15\)) соответственно для объекта **Category**.</span><span class="sxs-lookup"><span data-stu-id="5d0f8-119">You can, however, change the name, color, and shortcut key associated with a color category by setting the [Name](https://msdn.microsoft.com/library/bb645577\(v=office.15\)), [Color](https://msdn.microsoft.com/library/bb612316\(v=office.15\)), and [ShortcutKey](https://msdn.microsoft.com/library/bb644944\(v=office.15\)) properties, respectively, of the **Category** object.</span></span> <span data-ttu-id="5d0f8-120">Можно изменить свойство **Color**, установив или получив его константу [OlCategoryColor](https://msdn.microsoft.com/library/bb608974\(v=office.15\)).</span><span class="sxs-lookup"><span data-stu-id="5d0f8-120">You can change the **Color** property by setting or getting its [OlCategoryColor](https://msdn.microsoft.com/library/bb608974\(v=office.15\)) constant.</span></span> <span data-ttu-id="5d0f8-121">Чтобы воспроизвести цвет в пользовательском элементе управления, используйте следующие нередактируемые свойства объекта **Category**:</span><span class="sxs-lookup"><span data-stu-id="5d0f8-121">To reproduce the color in a custom control, use the following read-only properties of the **Category** object:</span></span>

  - <span data-ttu-id="5d0f8-122">[CategoryBorderColor](https://msdn.microsoft.com/library/bb610083\(v=office.15\))</span><span class="sxs-lookup"><span data-stu-id="5d0f8-122">[CategoryBorderColor](https://msdn.microsoft.com/library/bb610083\(v=office.15\))</span></span>

  - <span data-ttu-id="5d0f8-123">[CategoryGradientBottomColor](https://msdn.microsoft.com/library/bb647357\(v=office.15\))</span><span class="sxs-lookup"><span data-stu-id="5d0f8-123">[CategoryGradientBottomColor](https://msdn.microsoft.com/library/bb647357\(v=office.15\))</span></span>

  - <span data-ttu-id="5d0f8-124">[CategoryGradientTopColor](https://msdn.microsoft.com/library/bb623975\(v=office.15\))</span><span class="sxs-lookup"><span data-stu-id="5d0f8-124">[CategoryGradientTopColor](https://msdn.microsoft.com/library/bb623975\(v=office.15\))</span></span>

<span data-ttu-id="5d0f8-125">Эти свойства возвращают значение **OLE\_COLOR**, которое зависит от свойства **Color** объекта **Category**.</span><span class="sxs-lookup"><span data-stu-id="5d0f8-125">These properties return an **OLE\_COLOR** value, which is dependent on the **Color** property of the **Category** object.</span></span>

<span data-ttu-id="5d0f8-126">Элементы Outlook отображаются на основе имени категории.</span><span class="sxs-lookup"><span data-stu-id="5d0f8-126">Outlook items are displayed based on the category name.</span></span> <span data-ttu-id="5d0f8-127">Каждый объект элемента имеет свойство **Categories**, в котором хранится строка с разделителями запятыми, представляющая названия категорий.</span><span class="sxs-lookup"><span data-stu-id="5d0f8-127">Each item object has a **Categories** property that stores a comma-delimited string that represents category names.</span></span> <span data-ttu-id="5d0f8-128">(Например, для объекта [MailItem](https://msdn.microsoft.com/library/bb643865\(v=office.15\)) используется свойство **MailItem** [Categories](https://msdn.microsoft.com/library/bb646442\(v=office.15\)) ).</span><span class="sxs-lookup"><span data-stu-id="5d0f8-128">(For example, for the [MailItem](https://msdn.microsoft.com/library/bb643865\(v=office.15\)) object, you would use the **MailItem** [Categories](https://msdn.microsoft.com/library/bb646442\(v=office.15\)) property).</span></span> <span data-ttu-id="5d0f8-129">Это позволяет добавлять категорию для элемента, даже если этой категории нет в основном списке категорий.</span><span class="sxs-lookup"><span data-stu-id="5d0f8-129">This enables you to add a category to the item, even if the category is not present in the main category list.</span></span>


> [!NOTE]
> <span data-ttu-id="5d0f8-p104">Если свойство **Categories** элемента содержит имя категории, не входящей в коллекцию **Categories** объекта **NameSpace**, то имя этой категории, связанной с элементом Outlook, отображается, но без соответствующего цвета. Свойство **Categories** объекта **Item** не возвращает коллекцию **Categories**.</span><span class="sxs-lookup"><span data-stu-id="5d0f8-p104">If the **Categories** property of an item contains a category name that is not in the **Categories** collection of the **NameSpace** object, the category name associated with that Outlook item is displayed, but without an associated color. The **Categories** property on an **Item** object does not return a **Categories** collection.</span></span>

<span data-ttu-id="5d0f8-132">В представленном ниже примере кода первая процедура EnumerateCategories получает основной список категорий текущего пользователя, представленный коллекцией **Categories**.</span><span class="sxs-lookup"><span data-stu-id="5d0f8-132">In the following code example, the first procedure, EnumerateCategories, gets the current user’s main list of categories, represented by the **Categories** collection.</span></span> <span data-ttu-id="5d0f8-133">Затем перечисляются объекты **Category** в этой коллекции и записываются свойства **Name** и **CategoryID** для отслеживания прослушивателей коллекции [Listeners](https://msdn.microsoft.com/library/system.diagnostics.debug.listeners.aspx).</span><span class="sxs-lookup"><span data-stu-id="5d0f8-133">It then enumerates the **Category** objects in that collection, and writes the **Name** and **CategoryID** properties to the trace listeners of the [Listeners](https://msdn.microsoft.com/library/system.diagnostics.debug.listeners.aspx) collection.</span></span> <span data-ttu-id="5d0f8-134">Вторая процедура AddACategory получает основной список категорий текущего пользователя и использует метод CategoryExists для проверки существования категории "ISV" в коллекции.</span><span class="sxs-lookup"><span data-stu-id="5d0f8-134">The second procedure, AddACategory, gets the current user’s main list of categories and uses the CategoryExists method to check whether a category named “ISV” exists in the collection.</span></span> <span data-ttu-id="5d0f8-135">Если категория с именем "ISV" не существует, процедура AddACategory добавляет категорию "ISV" в основной список категорий и назначает ей темно-синий цвет с помощью метода **Add** коллекции **Categories**.</span><span class="sxs-lookup"><span data-stu-id="5d0f8-135">If no category with the name “ISV” exists, AddACategory adds a category named “ISV” to the main category list and assigns it a dark blue color by using the **Add** method of the **Categories** collection.</span></span> <span data-ttu-id="5d0f8-136">Для категории также назначается сочетание клавиш CTRL + F11.</span><span class="sxs-lookup"><span data-stu-id="5d0f8-136">It also assigns CTRL+F11 as the shortcut key for the category.</span></span>

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

## <a name="see-also"></a><span data-ttu-id="5d0f8-137">См. также</span><span class="sxs-lookup"><span data-stu-id="5d0f8-137">See also</span></span>

- [<span data-ttu-id="5d0f8-138">Цветовые категории</span><span class="sxs-lookup"><span data-stu-id="5d0f8-138">Color categories</span></span>](color-categories.md)


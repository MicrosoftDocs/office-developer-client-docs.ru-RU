---
title: Назначение категорий элементу
TOCTitle: Assign categories to an item
ms:assetid: 4070801b-994a-46df-91fe-4efca834886e
ms:mtpsurl: https://msdn.microsoft.com/library/Ff424469(v=office.15)
ms:contentKeyID: 55119828
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: f8b94d03a1aea447c4dba859659f044d8ec11994
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359735"
---
# <a name="assign-categories-to-an-item"></a><span data-ttu-id="8a6fa-102">Назначение категорий элементу</span><span class="sxs-lookup"><span data-stu-id="8a6fa-102">Assign categories to an item</span></span>

<span data-ttu-id="8a6fa-103">В этом примере показано, как назначить категории элементу с помощью его свойства **Categories**.</span><span class="sxs-lookup"><span data-stu-id="8a6fa-103">This example shows how to assign categories to an item by using its **Categories** property.</span></span>

## <a name="example"></a><span data-ttu-id="8a6fa-104">Пример</span><span class="sxs-lookup"><span data-stu-id="8a6fa-104">Example</span></span>

> [!NOTE] 
> <span data-ttu-id="8a6fa-105">Приведенный ниже пример кода взят из книги [Программирование приложений для Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).</span><span class="sxs-lookup"><span data-stu-id="8a6fa-105">The following code example is an excerpt from [Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).</span></span>


<span data-ttu-id="8a6fa-106">Чтобы назначить категории элементу, используйте специальное свойство **Categories** элемента.</span><span class="sxs-lookup"><span data-stu-id="8a6fa-106">To assign categories to an item, use the particular item's **Categories** property.</span></span> <span data-ttu-id="8a6fa-107">В этом примере кода используется вспомогательный класс OutlookItem, определенный в статье [Создание вспомогательного класса для доступа к общим элементам Outlook](how-to-create-a-helper-class-to-access-common-outlook-item-members.md), с помощью которого можно удобно вызвать свойство OutlookItem.**Categories** без необходимости сначала выполнять приведение элемента.</span><span class="sxs-lookup"><span data-stu-id="8a6fa-107">This code sample makes use of the OutlookItem helper class, defined in [Create a Helper Class to Access Common Outlook Item Members](how-to-create-a-helper-class-to-access-common-outlook-item-members.md), to conveniently call the OutlookItem.**Categories** property without having to first cast the item.</span></span> <span data-ttu-id="8a6fa-108">Свойство **Categories** получает или задает категории, представленные в виде строки с разделителями-запятыми, которая может содержать не более 255 знаков.</span><span class="sxs-lookup"><span data-stu-id="8a6fa-108">The **Categories** property gets or sets categories that are represented by a comma-delimited string that can contain a maximum of 255 characters.</span></span> <span data-ttu-id="8a6fa-109">Запятые и пробелы используются для разделения значений категории.</span><span class="sxs-lookup"><span data-stu-id="8a6fa-109">The commas and spaces are used to separate the category values.</span></span> <span data-ttu-id="8a6fa-110">Назначение категории, не входящей в коллекцию [Categories](https://msdn.microsoft.com/library/bb646607\(v=office.15\)) объекта [NameSpace](https://msdn.microsoft.com/library/bb645857\(v=office.15\)), приведет к тому, что категория не будет отображать цвет.</span><span class="sxs-lookup"><span data-stu-id="8a6fa-110">Assigning a category that is not in the [Categories](https://msdn.microsoft.com/library/bb646607\(v=office.15\)) collection of the [NameSpace](https://msdn.microsoft.com/library/bb645857\(v=office.15\)) object will result in the category not displaying a color.</span></span>

<span data-ttu-id="8a6fa-p102">В следующем примере кода процедура AssignCategories создает ограничение для элементов с символами "ISV" в теме, сначала с помощью запроса DASL отфильтровывая в папке "Входящие" такие элементы. Затем AssignCategories проходит по отфильтрованным элементам с помощью класса **OutlookItem** и в том случае, если строка, возвращенная **item.Categories**, не является пустой ссылкой или не была назначена категории ISV, назначает категорию ISV этому элементу.</span><span class="sxs-lookup"><span data-stu-id="8a6fa-p102">In the following code example, AssignCategories creates a restriction for items that contain “ISV” in the subject by first using a DAV Searching and Locating (DASL) query to filter items in the Inbox that contain “ISV” in the subject. AssignCategories then iterates through the filtered items by using the **OutlookItem** class and, if the string returned by **item.Categories** is not a null reference or was already assigned to the ISV, the ISV category is assigned to the item.</span></span>

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```

```csharp
private void AssignCategories()
{
    string filter = "@SQL=" + "\"" + "urn:schemas:httpmail:subject"
        + "\"" + " ci_phrasematch 'ISV'";
    Outlook.Items items =
        Application.Session.GetDefaultFolder(
        Outlook.OlDefaultFolders.olFolderInbox).Items.Restrict(filter);
    for (int i = 1; i <= items.Count; i++)
    {
        OutlookItem item = new OutlookItem(items[i]);
        string existingCategories = item.Categories;
        if (String.IsNullOrEmpty(existingCategories))
        {
            item.Categories = "ISV";
        }
        else
        {
            if (item.Categories.Contains("ISV") == false)
            {
                item.Categories = existingCategories + ", ISV";
            }
        }
        item.Save();
    }
}
```

## <a name="see-also"></a><span data-ttu-id="8a6fa-113">См. также</span><span class="sxs-lookup"><span data-stu-id="8a6fa-113">See also</span></span>

- [<span data-ttu-id="8a6fa-114">Цветовые категории</span><span class="sxs-lookup"><span data-stu-id="8a6fa-114">Color categories</span></span>](color-categories.md)


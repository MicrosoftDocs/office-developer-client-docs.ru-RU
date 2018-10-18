---
title: Отображение выбранных элементов в активном окне проводника
TOCTitle: Display selected items in the active Explorer
ms:assetid: 31bb217b-8b45-4b50-942e-b6c2a7f13c83
ms:mtpsurl: https://msdn.microsoft.com/library/Dn292517(v=office.15)
ms:contentKeyID: 55119844
ms.date: 07/24/2014
mtps_version: v=office.15
ms.openlocfilehash: d2599aff01afc7cc02797210a260befdfb72be33
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25405506"
---
# <a name="display-selected-items-in-the-active-explorer"></a><span data-ttu-id="71574-102">Отображение выбранных элементов в активном окне проводника</span><span class="sxs-lookup"><span data-stu-id="71574-102">Display selected items in the active Explorer</span></span>

<span data-ttu-id="71574-103">В этом примере показано, как использовать вспомогательный класс OutlookItem для удобного отображения всех выбранных элементов в активном окне проводника.</span><span class="sxs-lookup"><span data-stu-id="71574-103">This example shows how to use the OutlookItem helper class to conveniently display all the items selected in the active Explorer window.</span></span>

## <a name="example"></a><span data-ttu-id="71574-104">Пример</span><span class="sxs-lookup"><span data-stu-id="71574-104">Example</span></span>

> [!NOTE] 
> <span data-ttu-id="71574-105">Приведенный ниже пример кода представляет собой фрагмент из книги [Программирование приложений для Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).</span><span class="sxs-lookup"><span data-stu-id="71574-105">The following code example is an excerpt from  [Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493)  , from Microsoft Press (ISBN 9780735622494, copyright Microsoft Press 2007, all rights reserved).</span></span>

<span data-ttu-id="71574-106">Объект [Selection](https://msdn.microsoft.com/library/bb612099\(v=office.15\)) содержит набор элементов Outlook, которые в настоящее время выбраны в активном окне проводника Outlook.</span><span class="sxs-lookup"><span data-stu-id="71574-106">The [Selection](https://msdn.microsoft.com/library/bb612099\(v=office.15\)) object contains the set of Outlook items currently selected in the active Outlook explorer.</span></span> <span data-ttu-id="71574-107">Ни активное окно проводника, представленное как [ActiveExplorer()](https://msdn.microsoft.com/library/bb647410\(v=office.15\)), ни набор выбранных элементов не указывают на тип элементов, которые выбраны.</span><span class="sxs-lookup"><span data-stu-id="71574-107">Neither the active explorer, represented by [ActiveExplorer()](https://msdn.microsoft.com/library/bb647410\(v=office.15\)), nor the set of selected items indicates the type of the items that are selected.</span></span> <span data-ttu-id="71574-108">Как правило, сначала необходимо определить тип элемента, а затем вызвать конкретный метод **Display** для этого типа.</span><span class="sxs-lookup"><span data-stu-id="71574-108">Normally, you would have to first identify the item type and then call the specific **Display** method for that type.</span></span> <span data-ttu-id="71574-109">Так как метод **Display** является общим для всех элементов Outlook, а вспомогательный класс OutlookItem содержит этот метод, можно воспользоваться вспомогательным классом путем объявления экземпляра объекта OutlookItem myItem и использования myItem.Display для отображения всех выбранных элементов.</span><span class="sxs-lookup"><span data-stu-id="71574-109">Because the **Display** method is common to all Outlook items objects and the OutlookItem helper class includes this method, you can take advantage of the helper class, by declaring an instance of the OutlookItem object, myItem, and using myItem.Display to display each item in the selection.</span></span> <span data-ttu-id="71574-110">Ознакомиться с реализацией вспомогательного класса OutlookItem можно в статье [Создание вспомогательного класса для доступа к общим элементам Outlook](how-to-create-a-helper-class-to-access-common-outlook-item-members.md)</span><span class="sxs-lookup"><span data-stu-id="71574-110">You can see the implementation of the OutlookItem helper class in [Create a Helper Class to Access Common Outlook Item Members](how-to-create-a-helper-class-to-access-common-outlook-item-members.md)</span></span>

<span data-ttu-id="71574-111">Если вы используете Visual Studio для тестирования этого примера кода, сначала добавьте ссылку на компонент Microsoft Outlook 15.0 Object Library и задайте переменную Outlook при импорте пространства имен **Microsoft.Office.Interop.Outlook**.</span><span class="sxs-lookup"><span data-stu-id="71574-111">If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the   variable when you import the Microsoft.Office.Interop.Outlook namespace.</span></span> <span data-ttu-id="71574-112">Инструкция **using** не должна идти непосредственно перед функциями в примере кода, но ее нужно добавить перед объявлением public Class.</span><span class="sxs-lookup"><span data-stu-id="71574-112">The using statement must not occur directly before the functions in the code example but must be added before the public   declaration.</span></span> <span data-ttu-id="71574-113">В следующей строке кода показано, как выполнить импорт и назначение в C\#.</span><span class="sxs-lookup"><span data-stu-id="71574-113">The following line of code shows how to do the import and assignment in C#.</span></span>

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```csharp
private void DisplaySelectedItems()
{
    Outlook.Selection selection =
        Application.ActiveExplorer().Selection;
    for (int i = 1; i <= selection.Count; i++)
    {
        OutlookItem myItem = new OutlookItem(selection[i]);
        myItem.Display();
    }
}
```

## <a name="see-also"></a><span data-ttu-id="71574-114">См. также</span><span class="sxs-lookup"><span data-stu-id="71574-114">See also</span></span>

- [<span data-ttu-id="71574-115">Создание вспомогательного класса для доступа к общим элементам Outlook</span><span class="sxs-lookup"><span data-stu-id="71574-115">Create a Helper class to access common Outlook item members</span></span>](how-to-create-a-helper-class-to-access-common-outlook-item-members.md)
- [<span data-ttu-id="71574-116">Общие элементы Outlook</span><span class="sxs-lookup"><span data-stu-id="71574-116">General Outlook items</span></span>](general-outlook-items.md)


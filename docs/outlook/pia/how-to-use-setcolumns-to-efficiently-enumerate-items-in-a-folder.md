---
title: Эффективное перечисление элементов в папке с помощью метода SetColumns
TOCTitle: Use SetColumns to efficiently enumerate items in a folder
ms:assetid: cd7c7758-8a9c-4f1c-a49c-9305d75be341
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184641(v=office.15)
ms:contentKeyID: 55119921
ms.date: 07/24/2014
mtps_version: v=office.15
ms.openlocfilehash: 2e75a0cb06420f5072805cdf03ad8f7925670e67
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25407473"
---
# <a name="use-setcolumns-to-efficiently-enumerate-items-in-a-folder"></a><span data-ttu-id="eb783-102">Эффективное перечисление элементов в папке с помощью метода SetColumns</span><span class="sxs-lookup"><span data-stu-id="eb783-102">Use SetColumns to efficiently enumerate items in a folder</span></span>

<span data-ttu-id="eb783-103">В этом примере показан порядок повышения быстродействия при перечислении коллекции [Items](https://msdn.microsoft.com/library/bb645287\(v=office.15\)) за счет кэширования определенных свойств каждого элемента коллекции с помощью метода [SetColumns(String)](https://msdn.microsoft.com/library/bb610268\(v=office.15\)).</span><span class="sxs-lookup"><span data-stu-id="eb783-103">This example shows how to improve the performance of enumerating the [Items](https://msdn.microsoft.com/library/bb645287\(v=office.15\)) collection by using the [SetColumns(String)](https://msdn.microsoft.com/library/bb610268\(v=office.15\)) method to cache certain properties of each item in the collection.</span></span>

## <a name="example"></a><span data-ttu-id="eb783-104">Пример</span><span class="sxs-lookup"><span data-stu-id="eb783-104">Example</span></span>

> [!NOTE] 
> <span data-ttu-id="eb783-105">Приведенный ниже пример кода представляет собой фрагмент из книги [Программирование приложений для Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).</span><span class="sxs-lookup"><span data-stu-id="eb783-105">The following code example is an excerpt from  [Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493)  , from Microsoft Press (ISBN 9780735622494, copyright Microsoft Press 2007, all rights reserved).</span></span>

<span data-ttu-id="eb783-p101">При перечислении коллекции следует использовать метод **SetColumns** для кэширования свойств коллекции **Items**. Метод **SetColumns** принимает аргумент, который представляет собой строку, содержащую разделенные запятыми имена свойств. После перечисления всех элементов коллекции вызовите метод [ResetColumns()](https://msdn.microsoft.com/library/bb624355\(v=office.15\)) для очистки кэша свойств.</span><span class="sxs-lookup"><span data-stu-id="eb783-p101">To enumerate items in a collection, use the **SetColumns** method to cache properties on the **Items** collection. **SetColumns** takes an argument that is a comma-delimited string that represents property names. Once all items in the collection have been enumerated, call the [ResetColumns()](https://msdn.microsoft.com/library/bb624355\(v=office.15\)) method to clear the property cache.</span></span>

<span data-ttu-id="eb783-109">В следующем примере кода в процедуре EnumerateContactsWithSetColumns используется метод **SetColumns** для кэширования свойств [FileAs](https://msdn.microsoft.com/library/bb647792\(v=office.15\)), [CompanyName](https://msdn.microsoft.com/library/bb610212\(v=office.15\)) и [JobTitle](https://msdn.microsoft.com/library/bb609294\(v=office.15\)) для элементов папки "Контакты".</span><span class="sxs-lookup"><span data-stu-id="eb783-109">In the following code example,   uses the SetColumns method to cache the FileAs , CompanyName , and JobTitle properties of items in the Contacts folder.</span></span> <span data-ttu-id="eb783-110">Обратите внимание, что необходимо проверить наличие пустых строк или пустой ссылки в ограничении.</span><span class="sxs-lookup"><span data-stu-id="eb783-110">Note that you must test for empty strings or a null reference in the restriction.</span></span>

<span data-ttu-id="eb783-111">Обратите внимание, что папка Outlook может содержать элементы разных типов.</span><span class="sxs-lookup"><span data-stu-id="eb783-111">Note that an Outlook folder can possibly contain items of different types.</span></span> <span data-ttu-id="eb783-112">В этом примере кода используется вспомогательный класс OutlookItem, определенный в статье [Создание вспомогательного класса для доступа к общим элементам Outlook](how-to-create-a-helper-class-to-access-common-outlook-item-members.md), чтобы легко вызывать свойство OutlookItem.Class для проверки класса сообщений каждого элемента в отфильтрованном подмножестве элементов в папке до предположения, что элемент является элементом контактов.</span><span class="sxs-lookup"><span data-stu-id="eb783-112">This code sample makes use of the OutlookItem helper class, defined in [Create a Helper Class to Access Common Outlook Item Members](how-to-create-a-helper-class-to-access-common-outlook-item-members.md), to conveniently call the OutlookItem.Class property to verify the message class of each item in the filtered subset of items in the folder, before assuming the item is a contact item.</span></span>

<span data-ttu-id="eb783-113">Если вы используете Visual Studio для тестирования этого примера кода, сначала добавьте ссылку на компонент Microsoft Outlook 15.0 Object Library и задайте переменную Outlook при импорте пространства имен **Microsoft.Office.Interop.Outlook**.</span><span class="sxs-lookup"><span data-stu-id="eb783-113">If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the   variable when you import the Microsoft.Office.Interop.Outlook namespace.</span></span> <span data-ttu-id="eb783-114">Инструкция **using** не должна идти непосредственно перед функциями в примере кода, но ее нужно добавить перед открытым объявлением Class.</span><span class="sxs-lookup"><span data-stu-id="eb783-114">The using statement must not occur directly before the functions in the code example but must be added before the public   declaration.</span></span> <span data-ttu-id="eb783-115">В следующей строке кода показано, как выполнить импорт и назначение в C\#.</span><span class="sxs-lookup"><span data-stu-id="eb783-115">The following line of code shows how to do the import and assignment in C#.</span></span>

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```csharp
private void EnumerateContactsWithSetColumns()
{
    // Obtain Contacts folder
    Outlook.Folder folder =
        Application.Session.GetDefaultFolder(
        Outlook.OlDefaultFolders.olFolderContacts)
        as Outlook.Folder;
    string filter = "Not([CompanyName] Is Null)" +
        " AND Not([JobTitle] Is Null)";
    Outlook.Items items = folder.Items.Restrict(filter);
    items.SetColumns("FileAs, CompanyName, JobTitle");
    for (int i = 1; i <= items.Count; i++)
    {
        // Create an instance of OutlookItem
        OutlookItem myItem = new OutlookItem(items[i]);
        if (myItem.Class == Outlook.OlObjectClass.olContact)
        {
            // Use InnerObject to return ContactItem
            Outlook.ContactItem contact =
                myItem.InnerObject as Outlook.ContactItem;
            StringBuilder sb = new StringBuilder();
            sb.AppendLine(contact.FileAs);
            sb.AppendLine(contact.CompanyName);
            sb.AppendLine(contact.JobTitle);
            sb.AppendLine();
            Debug.WriteLine(sb.ToString());
        }
    }
    items.ResetColumns();
}
```

## <a name="see-also"></a><span data-ttu-id="eb783-116">См. также</span><span class="sxs-lookup"><span data-stu-id="eb783-116">See also</span></span>

- [<span data-ttu-id="eb783-117">Поиск и фильтрация</span><span class="sxs-lookup"><span data-stu-id="eb783-117">Search and Filter</span></span>](search-and-filter.md)


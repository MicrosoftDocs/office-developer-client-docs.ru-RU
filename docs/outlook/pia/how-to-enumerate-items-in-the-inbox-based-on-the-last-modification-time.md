---
title: Перечисление элементов в папке "Входящие" с учетом времени последнего изменения
TOCTitle: Enumerate items in the Inbox based on the last modification time
ms:assetid: 93a25143-def6-4832-bac2-3744558c2736
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184626(v=office.15)
ms:contentKeyID: 55119920
ms.date: 07/24/2014
mtps_version: v=office.15
ms.openlocfilehash: ecc4ed8f2fb207b8952fef41481738dd8be0ee02
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25406045"
---
# <a name="enumerate-items-in-the-inbox-based-on-the-last-modification-time"></a><span data-ttu-id="f1f75-102">Перечисление элементов в папке "Входящие" с учетом времени последнего изменения</span><span class="sxs-lookup"><span data-stu-id="f1f75-102">Enumerate items in the Inbox based on the last modification time</span></span>

<span data-ttu-id="f1f75-103">В этом примере показано, как перечислять элементы в папке "Входящие" с учетом времени последнего изменения.</span><span class="sxs-lookup"><span data-stu-id="f1f75-103">This example shows how to enumerate items in the Inbox folder based on the last modification time.</span></span>

## <a name="example"></a><span data-ttu-id="f1f75-104">Пример</span><span class="sxs-lookup"><span data-stu-id="f1f75-104">Example</span></span>

> [!NOTE] 
> <span data-ttu-id="f1f75-105">Приведенный ниже пример кода взят из книги [Программирование приложений для Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).</span><span class="sxs-lookup"><span data-stu-id="f1f75-105">The following code example is an excerpt from  [Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493)  , from Microsoft Press (ISBN 9780735622494, copyright Microsoft Press 2007, all rights reserved).</span></span>

<span data-ttu-id="f1f75-106">Объект [Table](https://msdn.microsoft.com/library/bb652856\(v=office.15\)) представляет набор элементов из объекта [Folder](https://msdn.microsoft.com/library/bb645774\(v=office.15\)) или [Search](https://msdn.microsoft.com/library/bb612611\(v=office.15\)).</span><span class="sxs-lookup"><span data-stu-id="f1f75-106">The [Table](https://msdn.microsoft.com/library/bb652856\(v=office.15\)) object represents a set of items from a [Folder](https://msdn.microsoft.com/library/bb645774\(v=office.15\)) or [Search](https://msdn.microsoft.com/library/bb612611\(v=office.15\)) object.</span></span> <span data-ttu-id="f1f75-107">Для получения объекта **Table** вызовите метод [GetTable(Object, Object)](https://msdn.microsoft.com/library/bb612592\(v=office.15\)) для объекта **Folder** или **Search**.</span><span class="sxs-lookup"><span data-stu-id="f1f75-107">To obtain a **Table**, call the [GetTable(Object, Object)](https://msdn.microsoft.com/library/bb612592\(v=office.15\)) method on a **Folder** or **Search** object.</span></span> <span data-ttu-id="f1f75-108">Каждый элемент возвращаемого объекта **Table** содержит только заданный по умолчанию поднабор свойств элемента.</span><span class="sxs-lookup"><span data-stu-id="f1f75-108">Each item in the returned **Table** contains only a default subset of the item's properties.</span></span> <span data-ttu-id="f1f75-109">Каждый объект [Row](https://msdn.microsoft.com/library/bb610126\(v=office.15\)) может считаться элементом в папке, а каждый объект [Column](https://msdn.microsoft.com/library/bb609646\(v=office.15\)) — свойством элемента.</span><span class="sxs-lookup"><span data-stu-id="f1f75-109">Each [Row](https://msdn.microsoft.com/library/bb610126\(v=office.15\)) object can be regarded as an item in the folder, and each [Column](https://msdn.microsoft.com/library/bb609646\(v=office.15\)) object as a property of an item.</span></span> <span data-ttu-id="f1f75-110">Удаление, добавление или изменение строк в объекте **Table** не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="f1f75-110">Removing, adding, or changing rows is not supported in the **Table**.</span></span> <span data-ttu-id="f1f75-111">Для перечисления элементов в объекте **Table** сначала следует использовать свойство [EndOfTable](https://msdn.microsoft.com/library/bb647715\(v=office.15\)), чтобы определить, находится ли текущая позиция в конце таблицы.</span><span class="sxs-lookup"><span data-stu-id="f1f75-111">To enumerate items in a **Table**, first use the [EndOfTable](https://msdn.microsoft.com/library/bb647715\(v=office.15\)) property to see whether your current position is at the end of the table.</span></span> <span data-ttu-id="f1f75-112">Если свойство **EndOfTable** возвращает значение **false**, используйте метод [GetNextRow()](https://msdn.microsoft.com/library/bb609740\(v=office.15\)) для возврата объекта **Row**, который содержит заданное по умолчанию число объектов **Column**.</span><span class="sxs-lookup"><span data-stu-id="f1f75-112">If **EndOfTable** returns **false**, use the [GetNextRow()](https://msdn.microsoft.com/library/bb609740\(v=office.15\)) method to return a **Row**, which contains a default number of **Column** objects.</span></span> <span data-ttu-id="f1f75-113">Продолжайте итерацию в прямом направлении в объекте **Table** путем вызова метода **GetNextRow**, пока свойство **EndOfTable** не вернет значение **true**.</span><span class="sxs-lookup"><span data-stu-id="f1f75-113">You continue iterating in a forward manner through the **Table** by calling **GetNextRow** until **EndOfTable** returns **true**.</span></span>

<span data-ttu-id="f1f75-114">В следующем примере кода процедура DemoTableForInbox получает объект **Table** в папке "Входящие", сортирует объект **Table** с помощью свойства **LastModificationTime** и метода [Sort(String, Object)](https://msdn.microsoft.com/library/bb652667\(v=office.15\)), после чего выполняет итерацию по таблице для записи темы каждого элемента в прослушиватели трассировки в коллекции [Listeners](https://msdn.microsoft.com/library/system.diagnostics.debug.listeners.aspx).</span><span class="sxs-lookup"><span data-stu-id="f1f75-114">In the following code example,   obtains a Table object for the Inbox folder, sorts the Table object by using the LastModificationTime property and Sort(String, Object) method, and iterates through the table to write the subject of each item to the trace listeners of the Listeners collection.</span></span>

<span data-ttu-id="f1f75-115">Если для тестирования этого примера кода вы используете Visual Studio, сначала добавьте ссылку на компонент библиотеки объектов Microsoft Outlook 15.0 и укажите переменную Outlook при импорте пространства имен **Microsoft.Office.Interop.Outlook**.</span><span class="sxs-lookup"><span data-stu-id="f1f75-115">If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the   variable when you import the Microsoft.Office.Interop.Outlook namespace.</span></span> <span data-ttu-id="f1f75-116">Не следует использовать инструкцию **using** непосредственно перед функциями в примере кода, но ее необходимо добавить перед объявлением общедоступного класса.</span><span class="sxs-lookup"><span data-stu-id="f1f75-116">The using statement must not occur directly before the functions in the code example but must be added before the public   declaration.</span></span> <span data-ttu-id="f1f75-117">В следующей строке кода показано, как выполнить импорт и назначение в C\#.</span><span class="sxs-lookup"><span data-stu-id="f1f75-117">The following line of code shows how to do the import and assignment in C#.</span></span>

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```csharp
private void DemoTableForInbox()
{
    //Obtain Inbox
    Outlook.Folder folder =
        Application.Session.GetDefaultFolder(
        Outlook.OlDefaultFolders.olFolderInbox)
        as Outlook.Folder;
    //Obtain Table using defaults
    Outlook.Table table =
        folder.GetTable(Type.Missing, Type.Missing);
    table.Sort("LastModificationTime",
        Outlook.OlSortOrder.olDescending);
    while (!table.EndOfTable)
    {
        Outlook.Row nextRow = table.GetNextRow();
        Debug.WriteLine(nextRow["Subject"]);
    }
}
```

## <a name="see-also"></a><span data-ttu-id="f1f75-118">См. также</span><span class="sxs-lookup"><span data-stu-id="f1f75-118">See also</span></span>

- [<span data-ttu-id="f1f75-119">Поиск и фильтрация</span><span class="sxs-lookup"><span data-stu-id="f1f75-119">Search and Filter</span></span>](search-and-filter.md)


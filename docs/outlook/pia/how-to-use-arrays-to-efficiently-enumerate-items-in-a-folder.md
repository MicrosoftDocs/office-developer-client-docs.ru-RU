---
title: Эффективное перечисление элементов в папке с помощью массивов
TOCTitle: Use arrays to efficiently enumerate items in a folder
ms:assetid: 05a73225-ad0d-4d52-90b6-448d220348df
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184588(v=office.15)
ms:contentKeyID: 55119885
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: be65e2818f22e6da289ef8b8da483c2747f941a5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32335387"
---
# <a name="use-arrays-to-efficiently-enumerate-items-in-a-folder"></a><span data-ttu-id="147be-102">Эффективное перечисление элементов в папке с помощью массивов</span><span class="sxs-lookup"><span data-stu-id="147be-102">Use arrays to efficiently enumerate items in a folder</span></span>

<span data-ttu-id="147be-103">В этом примере показано, как эффективно перечислять элементы в объекте [Folder](https://msdn.microsoft.com/library/bb645774\(v=office.15\)) с помощью метода [GetArray(Int32)](https://msdn.microsoft.com/library/bb608928\(v=office.15\)).</span><span class="sxs-lookup"><span data-stu-id="147be-103">This example shows how to efficiently enumerate items in a [Folder](https://msdn.microsoft.com/library/bb645774\(v=office.15\)) object by using the [GetArray(Int32)](https://msdn.microsoft.com/library/bb608928\(v=office.15\)) method.</span></span>

## <a name="example"></a><span data-ttu-id="147be-104">Пример</span><span class="sxs-lookup"><span data-stu-id="147be-104">Example</span></span>

> [!NOTE] 
> <span data-ttu-id="147be-105">Приведенный ниже пример кода взят из книги [Программирование приложений для Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).</span><span class="sxs-lookup"><span data-stu-id="147be-105">The following code example is an excerpt from [Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).</span></span>

<span data-ttu-id="147be-106">В следующем примере кода DemoGetArrayForTable получает объект [Table](https://msdn.microsoft.com/library/bb652856\(v=office.15\)) из объекта **Folder** с помощью метода [GetTable(Object, Object)](https://msdn.microsoft.com/library/bb612592\(v=office.15\)).</span><span class="sxs-lookup"><span data-stu-id="147be-106">In the following code example, DemoGetArrayForTable gets a [Table](https://msdn.microsoft.com/library/bb652856\(v=office.15\)) object from a **Folder** object by using the [GetTable(Object, Object)](https://msdn.microsoft.com/library/bb612592\(v=office.15\)) method.</span></span> <span data-ttu-id="147be-107">Затем DemoGetArrayForTable использует метод **GetArray**, чтобы вернуть объект [Array](https://msdn.microsoft.com/library/system.array.aspx), содержащий элементы для каждой строки в таблице.</span><span class="sxs-lookup"><span data-stu-id="147be-107">DemoGetArrayForTable then uses the **GetArray** method to return an [Array](https://msdn.microsoft.com/library/system.array.aspx) object that contains elements for every row in the table.</span></span> <span data-ttu-id="147be-108">Возвращаемый объект **Array** является двумерным массивом, представляющим набор значений строк и столбцов из объекта **Table**.</span><span class="sxs-lookup"><span data-stu-id="147be-108">The returned **Array** object is a two-dimensional array that represents a set of row and column values from the **Table**.</span></span> <span data-ttu-id="147be-109">Массив отсчитывается с нуля, а не с единицы, как для коллекций Outlook.</span><span class="sxs-lookup"><span data-stu-id="147be-109">The array is zero-based, instead of one-based as is the case with Outlook collections.</span></span> <span data-ttu-id="147be-110">После получения объекта **Array** в коде используется цикл for для перечисления в таблице.</span><span class="sxs-lookup"><span data-stu-id="147be-110">Once the **Array** object is obtained, the code uses a for loop to enumerate through the table.</span></span>

<span data-ttu-id="147be-111">Если для тестирования этого примера кода вы используете Visual Studio, сначала добавьте ссылку на компонент библиотеки объектов Microsoft Outlook 15.0 и укажите переменную Outlook при импорте пространства имен **Microsoft.Office.Interop.Outlook**.</span><span class="sxs-lookup"><span data-stu-id="147be-111">If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the Outlook variable when you import the **Microsoft.Office.Interop.Outlook** namespace.</span></span> <span data-ttu-id="147be-112">Инструкция **using** не должна находиться непосредственно перед функциями в примере кода, но ее нужно добавить перед объявлением общедоступного класса.</span><span class="sxs-lookup"><span data-stu-id="147be-112">The **using** statement must not occur directly before the functions in the code example but must be added before the public Class declaration.</span></span> <span data-ttu-id="147be-113">В приведенной ниже строке кода показано, как выполнить импорт и назначение на языке C\#.</span><span class="sxs-lookup"><span data-stu-id="147be-113">The following line of code shows how to do the import and assignment in C\#.</span></span>

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```csharp
private void DemoGetArrayForTable()
{
    // Obtain Inbox
    Outlook.Folder folder =
        Application.Session.GetDefaultFolder(
        Outlook.OlDefaultFolders.olFolderInbox)
        as Outlook.Folder;
    Outlook.Table table =
        folder.GetTable("", Outlook.OlTableContents.olUserItems);
    Array tableArray = table.GetArray(table.GetRowCount()) as Array;
    for (int i = 0; i <= tableArray.GetUpperBound(0); i++)
    {
        for (int j = 0; j <= tableArray.GetUpperBound(1); j++)
        {
            Debug.WriteLine(tableArray.GetValue(i, j));
        }
    }
}
```

## <a name="see-also"></a><span data-ttu-id="147be-114">См. также</span><span class="sxs-lookup"><span data-stu-id="147be-114">See also</span></span>

- [<span data-ttu-id="147be-115">Поиск и фильтрация</span><span class="sxs-lookup"><span data-stu-id="147be-115">Search and filter</span></span>](search-and-filter.md)


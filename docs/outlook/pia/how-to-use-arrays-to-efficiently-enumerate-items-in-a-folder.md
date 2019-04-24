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
# <a name="use-arrays-to-efficiently-enumerate-items-in-a-folder"></a>Эффективное перечисление элементов в папке с помощью массивов

В этом примере показано, как эффективно перечислять элементы в объекте [Folder](https://msdn.microsoft.com/library/bb645774\(v=office.15\)) с помощью метода [GetArray(Int32)](https://msdn.microsoft.com/library/bb608928\(v=office.15\)).

## <a name="example"></a>Пример

> [!NOTE] 
> Приведенный ниже пример кода взят из книги [Программирование приложений для Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).

В следующем примере кода DemoGetArrayForTable получает объект [Table](https://msdn.microsoft.com/library/bb652856\(v=office.15\)) из объекта **Folder** с помощью метода [GetTable(Object, Object)](https://msdn.microsoft.com/library/bb612592\(v=office.15\)). Затем DemoGetArrayForTable использует метод **GetArray**, чтобы вернуть объект [Array](https://msdn.microsoft.com/library/system.array.aspx), содержащий элементы для каждой строки в таблице. Возвращаемый объект **Array** является двумерным массивом, представляющим набор значений строк и столбцов из объекта **Table**. Массив отсчитывается с нуля, а не с единицы, как для коллекций Outlook. После получения объекта **Array** в коде используется цикл for для перечисления в таблице.

Если для тестирования этого примера кода вы используете Visual Studio, сначала добавьте ссылку на компонент библиотеки объектов Microsoft Outlook 15.0 и укажите переменную Outlook при импорте пространства имен **Microsoft.Office.Interop.Outlook**. Инструкция **using** не должна находиться непосредственно перед функциями в примере кода, но ее нужно добавить перед объявлением общедоступного класса. В приведенной ниже строке кода показано, как выполнить импорт и назначение на языке C\#.

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

## <a name="see-also"></a>См. также

- [Поиск и фильтрация](search-and-filter.md)


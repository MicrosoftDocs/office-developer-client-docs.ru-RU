---
title: Перечисление скрытых элементов в папке
TOCTitle: Enumerate hidden items in a folder
ms:assetid: dafad1fb-94ce-4584-b5d1-2de5fad2f72a
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184645(v=office.15)
ms:contentKeyID: 55119888
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 6508ea955ad74b49b5fef73352b4a1706d8e338c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357409"
---
# <a name="enumerate-hidden-items-in-a-folder"></a>Перечисление скрытых элементов в папке

В этом примере показано, как находить и перечислять скрытые элементы в папке.

## <a name="example"></a>Пример

> [!NOTE] 
> Приведенный ниже пример кода представляет собой фрагмент из книги [Программирование приложений для Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).

Одна из функций объекта [Table](https://msdn.microsoft.com/library/bb652856\(v=office.15\)), который представляет набор элементов в папке, заключается в том, что он может содержать скрытые элементы. Для возврата скрытых элементов в папке присвойте параметру *TableContents* метода [GetTable(Object, Object)](https://msdn.microsoft.com/library/bb612592\(v=office.15\)) объекта [MAPIFolder](https://msdn.microsoft.com/library/bb624369\(v=office.15\)) значение [olHiddenItems](https://msdn.microsoft.com/library/bb622801\(v=office.15\)). В следующем примере кода процедура TableForInboxHiddenItems получает скрытые элементы в папке "Входящие" и записывает значения свойств [Subject](https://msdn.microsoft.com/library/bb611353\(v=office.15\)) и [MessageClass](https://msdn.microsoft.com/library/bb645845\(v=office.15\)) для каждого скрытого элемента в прослушиватели трассировки в коллекции [Listeners](https://msdn.microsoft.com/library/system.diagnostics.debug.listeners.aspx).

Если вы используете Visual Studio для тестирования этого примера кода, сначала добавьте ссылку на компонент Microsoft Outlook 15.0 Object Library и задайте переменную Outlook при импорте пространства имен **Microsoft.Office.Interop.Outlook**. Инструкция **using** не должна находиться непосредственно перед функциями в примере кода, но ее нужно добавить перед объявлением общедоступного класса. В приведенной ниже строке кода показано, как выполнить импорт и назначение на языке C\#.

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```csharp
private void TableForInboxHiddenItems()
{
    // Inbox
    Outlook.Folder folder =
        Application.Session.GetDefaultFolder(
        Outlook.OlDefaultFolders.olFolderInbox)
        as Outlook.Folder;
    // Call GetTable with OlTableContents.olHiddenItems
    Outlook.Table table =
        folder.GetTable("",
        Outlook.OlTableContents.olHiddenItems);
    while (!table.EndOfTable)
    {
        Outlook.Row nextRow = table.GetNextRow();
        // Test for null subject
        if (nextRow["Subject"] == null)
        {
            Debug.WriteLine(nextRow["MessageClass"]);
        }
        else
        {
            Debug.WriteLine(nextRow["Subject"] + " "
                + nextRow["MessageClass"]);
        }
    }
}
```

## <a name="see-also"></a>См. также

-[Поиск и фильтрация](search-and-filter.md)


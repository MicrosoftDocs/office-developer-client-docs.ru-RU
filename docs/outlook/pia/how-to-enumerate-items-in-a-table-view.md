---
title: Перечисление элементов в табличном представлении
TOCTitle: Enumerate items in a table view
ms:assetid: c7d9a667-cfec-49c1-af7a-4c8063991588
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184640(v=office.15)
ms:contentKeyID: 55119900
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: b3bde66fd07a39aa8a63219876b9bdbcf72e00f7
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32320386"
---
# <a name="enumerate-items-in-a-table-view"></a>Перечисление элементов в табличном представлении

В этом примере показано перечисление элементов в представлении таблицы с помощью метода [GetTable()](https://msdn.microsoft.com/library/ff184699\(v=office.15\)).

## <a name="example"></a>Пример

В следующем образце кода выполняется получение объекта [Table](https://msdn.microsoft.com/library/bb652856\(v=office.15\)) из текущего представления папки "Входящие". Здесь в качестве текущей папки Проводника задается папка "Входящие". Затем выполняется проверка того, что текущее представление папки "Входящие" является табличным. Если текущее представление выводится в виде таблицы, в примере кода вызывается метод [GetTable()](https://msdn.microsoft.com/library/ff184699\(v=office.15\)) и показывается каждый элемент, которому соответствует строка в возвращенной таблице **Table**.

Если вы используете Visual Studio для тестирования этого примера кода, сначала добавьте ссылку на компонент Microsoft Outlook 15.0 Object Library и задайте переменную Outlook при импорте пространства имен **Microsoft.Office.Interop.Outlook**. Инструкция **using** не должна находиться непосредственно перед функциями в примере кода, но ее нужно добавить перед объявлением общедоступного класса. В приведенной ниже строке кода показано, как выполнить импорт и назначение на языке C\#.

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```csharp
private void DemoViewGetTable()
{
    // Obtain Inbox.
    Outlook.Folder inbox =
        Application.Session.GetDefaultFolder(
        Outlook.OlDefaultFolders.olFolderInbox)
        as Outlook.Folder;
    // Set ActiveExplorer.CurrentFolder to Inbox.
    // Inbox must be current folder
    // for View.GetTable to work correctly.
    Application.ActiveExplorer().CurrentFolder = inbox;
    // Ensure that current view is TableView.
    if (inbox.CurrentView.ViewType == 
        Outlook.OlViewType.olTableView)
    {
        Outlook.TableView view = 
            inbox.CurrentView as Outlook.TableView;
        // No arguments needed for View.GetTable.
        Outlook.Table table = view.GetTable();
        Debug.WriteLine("View Count=" 
            + table.GetRowCount().ToString());
        while (!table.EndOfTable)
        {
            // First row in Table.
            Outlook.Row nextRow = table.GetNextRow();
            Debug.WriteLine(nextRow["Subject"]
                + " Modified: "
                + nextRow["LastModificationTime"]);
        }
    }
}
```

## <a name="see-also"></a>См. также

- [Представления](views.md)


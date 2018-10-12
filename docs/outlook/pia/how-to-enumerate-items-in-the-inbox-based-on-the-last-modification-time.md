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
# <a name="enumerate-items-in-the-inbox-based-on-the-last-modification-time"></a>Перечисление элементов в папке "Входящие" с учетом времени последнего изменения

В этом примере показано, как перечислять элементы в папке "Входящие" с учетом времени последнего изменения.

## <a name="example"></a>Пример

> [!NOTE] 
> Приведенный ниже пример кода взят из книги [Программирование приложений для Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).

Объект [Table](https://msdn.microsoft.com/library/bb652856\(v=office.15\)) представляет набор элементов из объекта [Folder](https://msdn.microsoft.com/library/bb645774\(v=office.15\)) или [Search](https://msdn.microsoft.com/library/bb612611\(v=office.15\)). Для получения объекта **Table** вызовите метод [GetTable(Object, Object)](https://msdn.microsoft.com/library/bb612592\(v=office.15\)) для объекта **Folder** или **Search**. Каждый элемент возвращаемого объекта **Table** содержит только заданный по умолчанию поднабор свойств элемента. Каждый объект [Row](https://msdn.microsoft.com/library/bb610126\(v=office.15\)) может считаться элементом в папке, а каждый объект [Column](https://msdn.microsoft.com/library/bb609646\(v=office.15\)) — свойством элемента. Удаление, добавление или изменение строк в объекте **Table** не поддерживается. Для перечисления элементов в объекте **Table** сначала следует использовать свойство [EndOfTable](https://msdn.microsoft.com/library/bb647715\(v=office.15\)), чтобы определить, находится ли текущая позиция в конце таблицы. Если свойство **EndOfTable** возвращает значение **false**, используйте метод [GetNextRow()](https://msdn.microsoft.com/library/bb609740\(v=office.15\)) для возврата объекта **Row**, который содержит заданное по умолчанию число объектов **Column**. Продолжайте итерацию в прямом направлении в объекте **Table** путем вызова метода **GetNextRow**, пока свойство **EndOfTable** не вернет значение **true**.

В следующем примере кода процедура DemoTableForInbox получает объект **Table** в папке "Входящие", сортирует объект **Table** с помощью свойства **LastModificationTime** и метода [Sort(String, Object)](https://msdn.microsoft.com/library/bb652667\(v=office.15\)), после чего выполняет итерацию по таблице для записи темы каждого элемента в прослушиватели трассировки в коллекции [Listeners](https://msdn.microsoft.com/library/system.diagnostics.debug.listeners.aspx).

Если для тестирования этого примера кода вы используете Visual Studio, сначала добавьте ссылку на компонент библиотеки объектов Microsoft Outlook 15.0 и укажите переменную Outlook при импорте пространства имен **Microsoft.Office.Interop.Outlook**. Не следует использовать инструкцию **using** непосредственно перед функциями в примере кода, но ее необходимо добавить перед объявлением общедоступного класса. В следующей строке кода показано, как выполнить импорт и назначение в C\#.

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

## <a name="see-also"></a>См. также

- [Поиск и фильтрация](search-and-filter.md)


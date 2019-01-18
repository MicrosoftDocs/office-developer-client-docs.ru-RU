---
title: Отображение выбранных элементов в активном окне проводника
TOCTitle: Display selected items in the active Explorer
ms:assetid: 31bb217b-8b45-4b50-942e-b6c2a7f13c83
ms:mtpsurl: https://msdn.microsoft.com/library/Dn292517(v=office.15)
ms:contentKeyID: 55119844
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: b722bcb404f987a6f07a9fe305046ea6673dc231
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28698710"
---
# <a name="display-selected-items-in-the-active-explorer"></a>Отображение выбранных элементов в активном окне проводника

В этом примере показано, как использовать вспомогательный класс OutlookItem для удобного отображения всех выбранных элементов в активном окне проводника.

## <a name="example"></a>Пример

> [!NOTE] 
> Приведенный ниже пример кода представляет собой фрагмент из книги [Программирование приложений для Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).

Объект [Selection](https://msdn.microsoft.com/library/bb612099\(v=office.15\)) содержит набор элементов Outlook, которые в настоящее время выбраны в активном окне проводника Outlook. Ни активное окно проводника, представленное как [ActiveExplorer()](https://msdn.microsoft.com/library/bb647410\(v=office.15\)), ни набор выбранных элементов не указывают на тип элементов, которые выбраны. Как правило, сначала необходимо определить тип элемента, а затем вызвать конкретный метод **Display** для этого типа. Так как метод **Display** является общим для всех элементов Outlook, а вспомогательный класс OutlookItem содержит этот метод, можно воспользоваться вспомогательным классом путем объявления экземпляра объекта OutlookItem myItem и использования myItem.Display для отображения всех выбранных элементов. Ознакомиться с реализацией вспомогательного класса OutlookItem можно в статье [Создание вспомогательного класса для доступа к общим элементам Outlook](how-to-create-a-helper-class-to-access-common-outlook-item-members.md)

Если вы используете Visual Studio для тестирования этого примера кода, сначала добавьте ссылку на компонент Microsoft Outlook 15.0 Object Library и задайте переменную Outlook при импорте пространства имен **Microsoft.Office.Interop.Outlook**. Инструкция **using** не должна идти непосредственно перед функциями в примере кода, но ее нужно добавить перед объявлением public Class. В следующей строке кода показано, как выполнить импорт и назначение в C\#.

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

## <a name="see-also"></a>См. также

- [Создание вспомогательного класса для доступа к общим элементам Outlook](how-to-create-a-helper-class-to-access-common-outlook-item-members.md)
- [Общие элементы Outlook](general-outlook-items.md)


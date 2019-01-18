---
title: Отображение списков адресов для профиля
TOCTitle: Display the address lists for a profile
ms:assetid: ced8230b-110b-4ccb-a699-588798144154
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184643(v=office.15)
ms:contentKeyID: 55119802
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: b69ed930241dc058b22b75c6ccc9121f8856d28f
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28703722"
---
# <a name="display-the-address-lists-for-a-profile"></a>Отображение списков адресов для профиля

В этом примере показано, как отобразить список адресов для текущего профиля.

## <a name="example"></a>Пример

> [!NOTE] 
> Приведенный ниже пример кода представляет собой фрагмент из книги [Программирование приложений для Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).

Текущий профиль содержит списки адресов, представленные коллекцией [AddressLists](https://msdn.microsoft.com/library/bb611894\(v=office.15\)). Чтобы получить экземпляр коллекции AddressLists, необходимо использовать свойство [AddressLists](https://msdn.microsoft.com/library/bb624048\(v=office.15\)) объекта [NameSpace](https://msdn.microsoft.com/library/bb645857\(v=office.15\)).

В следующем примере кода в процедуре EnumerateAddressLists сначала перечисляется каждый объект [AddressList](https://msdn.microsoft.com/library/bb623538\(v=office.15\)) в коллекции AddressLists с помощью оператора foreach. Затем в этом примере создается строка, содержащая значения свойств [Name](https://msdn.microsoft.com/library/bb609849\(v=office.15\)), [ResolutionOrder](https://msdn.microsoft.com/library/bb646853\(v=office.15\)), [IsReadOnly](https://msdn.microsoft.com/library/bb612676\(v=office.15\)) и [IsInitialAddressList](https://msdn.microsoft.com/library/bb646646\(v=office.15\)). В завершение процедура EnumerateAddressLists записывает строку в прослушиватели трассировки в коллекции [Listeners](https://msdn.microsoft.com/library/system.diagnostics.debug.listeners.aspx). В результате отображается каждый список адресов для текущего профиля.

Если вы используете Visual Studio для тестирования этого примера кода, сначала добавьте ссылку на компонент Microsoft Outlook 15.0 Object Library и задайте переменную Outlook при импорте пространства имен **Microsoft.Office.Interop.Outlook**. Инструкция **using** не должна идти непосредственно перед функциями в примере кода, но ее нужно добавить перед открытым объявлением Class. В следующей строке кода показано, как выполнить импорт и назначение в C\#.

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```

```csharp
private void EnumerateAddressLists()
{
    Outlook.AddressLists addrLists =
         Application.Session.AddressLists;
    foreach (Outlook.AddressList addrList in addrLists)
    {
        StringBuilder sb = new StringBuilder();
        sb.AppendLine("Display Name: " + addrList.Name);
        sb.AppendLine("Resolution Order: "
            + addrList.ResolutionOrder.ToString());
        sb.AppendLine("Read-only : "
            + addrList.IsReadOnly.ToString());
        sb.AppendLine("Initial Address List: "
            + addrList.IsInitialAddressList.ToString());
        sb.AppendLine("");
        Debug.WriteLine(sb.ToString());
    }
}
```

## <a name="see-also"></a>См. также

- [Адресная книга](address-book.md)


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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32356373"
---
# <a name="display-the-address-lists-for-a-profile"></a><span data-ttu-id="a475e-102">Отображение списков адресов для профиля</span><span class="sxs-lookup"><span data-stu-id="a475e-102">Display the address lists for a profile</span></span>

<span data-ttu-id="a475e-103">В этом примере показано, как отобразить список адресов для текущего профиля.</span><span class="sxs-lookup"><span data-stu-id="a475e-103">This example shows how to display the address lists for the current profile.</span></span>

## <a name="example"></a><span data-ttu-id="a475e-104">Пример</span><span class="sxs-lookup"><span data-stu-id="a475e-104">Example</span></span>

> [!NOTE] 
> <span data-ttu-id="a475e-105">Приведенный ниже пример кода представляет собой фрагмент из книги [Программирование приложений для Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).</span><span class="sxs-lookup"><span data-stu-id="a475e-105">The following code example is an excerpt from [Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).</span></span>

<span data-ttu-id="a475e-p101">Текущий профиль содержит списки адресов, представленные коллекцией [AddressLists](https://msdn.microsoft.com/library/bb611894\(v=office.15\)). Чтобы получить экземпляр коллекции AddressLists, необходимо использовать свойство [AddressLists](https://msdn.microsoft.com/library/bb624048\(v=office.15\)) объекта [NameSpace](https://msdn.microsoft.com/library/bb645857\(v=office.15\)).</span><span class="sxs-lookup"><span data-stu-id="a475e-p101">The current profile contains address lists that are represented by the [AddressLists](https://msdn.microsoft.com/library/bb611894\(v=office.15\)) collection. To get an instance of the AddressLists collection, you must use the [AddressLists](https://msdn.microsoft.com/library/bb624048\(v=office.15\)) property of the [NameSpace](https://msdn.microsoft.com/library/bb645857\(v=office.15\)) object.</span></span>

<span data-ttu-id="a475e-108">В следующем примере кода в процедуре EnumerateAddressLists сначала перечисляется каждый объект [AddressList](https://msdn.microsoft.com/library/bb623538\(v=office.15\)) в коллекции AddressLists с помощью оператора foreach.</span><span class="sxs-lookup"><span data-stu-id="a475e-108">In the following code example, EnumerateAddressLists first enumerates each [AddressList](https://msdn.microsoft.com/library/bb623538\(v=office.15\)) object in the AddressLists collection by using a foreach statement.</span></span> <span data-ttu-id="a475e-109">Затем в этом примере создается строка, содержащая значения свойств [Name](https://msdn.microsoft.com/library/bb609849\(v=office.15\)), [ResolutionOrder](https://msdn.microsoft.com/library/bb646853\(v=office.15\)), [IsReadOnly](https://msdn.microsoft.com/library/bb612676\(v=office.15\)) и [IsInitialAddressList](https://msdn.microsoft.com/library/bb646646\(v=office.15\)).</span><span class="sxs-lookup"><span data-stu-id="a475e-109">The example then creates a string that contains the values of the [Name](https://msdn.microsoft.com/library/bb609849\(v=office.15\)), [ResolutionOrder](https://msdn.microsoft.com/library/bb646853\(v=office.15\)), [IsReadOnly](https://msdn.microsoft.com/library/bb612676\(v=office.15\)), and [IsInitialAddressList](https://msdn.microsoft.com/library/bb646646\(v=office.15\)) properties.</span></span> <span data-ttu-id="a475e-110">В завершение процедура EnumerateAddressLists записывает строку в прослушиватели трассировки в коллекции [Listeners](https://msdn.microsoft.com/library/system.diagnostics.debug.listeners.aspx).</span><span class="sxs-lookup"><span data-stu-id="a475e-110">Finally, EnumerateAddressLists writes the string to the trace listeners of the [Listeners](https://msdn.microsoft.com/library/system.diagnostics.debug.listeners.aspx) collection.</span></span> <span data-ttu-id="a475e-111">В результате отображается каждый список адресов для текущего профиля.</span><span class="sxs-lookup"><span data-stu-id="a475e-111">This displays each address list for the current profile.</span></span>

<span data-ttu-id="a475e-112">Если вы используете Visual Studio для тестирования этого примера кода, сначала добавьте ссылку на компонент Microsoft Outlook 15.0 Object Library и задайте переменную Outlook при импорте пространства имен **Microsoft.Office.Interop.Outlook**.</span><span class="sxs-lookup"><span data-stu-id="a475e-112">If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the Outlook variable when you import the **Microsoft.Office.Interop.Outlook** namespace.</span></span> <span data-ttu-id="a475e-113">Инструкция **using** не должна находиться непосредственно перед функциями в примере кода, но ее нужно добавить перед объявлением общедоступного класса.</span><span class="sxs-lookup"><span data-stu-id="a475e-113">The **using** statement must not occur directly before the functions in the code example but must be added before the public Class declaration.</span></span> <span data-ttu-id="a475e-114">В приведенной ниже строке кода показано, как выполнить импорт и назначение на языке C\#.</span><span class="sxs-lookup"><span data-stu-id="a475e-114">The following line of code shows how to do the import and assignment in C\#.</span></span>

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

## <a name="see-also"></a><span data-ttu-id="a475e-115">См. также</span><span class="sxs-lookup"><span data-stu-id="a475e-115">See also</span></span>

- [<span data-ttu-id="a475e-116">Адресная книга</span><span class="sxs-lookup"><span data-stu-id="a475e-116">Address book</span></span>](address-book.md)


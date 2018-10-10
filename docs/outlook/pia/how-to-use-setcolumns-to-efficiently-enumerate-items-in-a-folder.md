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
# <a name="use-setcolumns-to-efficiently-enumerate-items-in-a-folder"></a>Эффективное перечисление элементов в папке с помощью метода SetColumns

В этом примере показан порядок повышения быстродействия при перечислении коллекции [Items](https://msdn.microsoft.com/library/bb645287\(v=office.15\)) за счет кэширования определенных свойств каждого элемента коллекции с помощью метода [SetColumns(String)](https://msdn.microsoft.com/library/bb610268\(v=office.15\)).

## <a name="example"></a>Пример

> [!NOTE] 
> Приведенный ниже пример кода представляет собой фрагмент из книги [Программирование приложений для Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).

При перечислении коллекции следует использовать метод **SetColumns** для кэширования свойств коллекции **Items**. Метод **SetColumns** принимает аргумент, который представляет собой строку, содержащую разделенные запятыми имена свойств. После перечисления всех элементов коллекции вызовите метод [ResetColumns()](https://msdn.microsoft.com/library/bb624355\(v=office.15\)) для очистки кэша свойств.

В следующем примере кода в процедуре EnumerateContactsWithSetColumns используется метод **SetColumns** для кэширования свойств [FileAs](https://msdn.microsoft.com/library/bb647792\(v=office.15\)), [CompanyName](https://msdn.microsoft.com/library/bb610212\(v=office.15\)) и [JobTitle](https://msdn.microsoft.com/library/bb609294\(v=office.15\)) для элементов папки "Контакты". Обратите внимание, что необходимо проверить наличие пустых строк или пустой ссылки в ограничении.

Обратите внимание, что папка Outlook может содержать элементы разных типов. В этом примере кода используется вспомогательный класс OutlookItem, определенный в статье [Создание вспомогательного класса для доступа к общим элементам Outlook](how-to-create-a-helper-class-to-access-common-outlook-item-members.md), чтобы легко вызывать свойство OutlookItem.Class для проверки класса сообщений каждого элемента в отфильтрованном подмножестве элементов в папке до предположения, что элемент является элементом контактов.

Если вы используете Visual Studio для тестирования этого примера кода, сначала добавьте ссылку на компонент Microsoft Outlook 15.0 Object Library и задайте переменную Outlook при импорте пространства имен **Microsoft.Office.Interop.Outlook**. Инструкция **using** не должна идти непосредственно перед функциями в примере кода, но ее нужно добавить перед открытым объявлением Class. В следующей строке кода показано, как выполнить импорт и назначение в C\#.

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

## <a name="see-also"></a>См. также

- [Поиск и фильтрация](search-and-filter.md)


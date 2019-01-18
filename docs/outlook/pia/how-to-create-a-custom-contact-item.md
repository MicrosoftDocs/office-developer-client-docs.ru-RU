---
title: Создание настраиваемого элемента контакта
TOCTitle: Create a custom Contact item
ms:assetid: 24b2a104-a0a7-469b-9676-a07cab613f59
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184596(v=office.15)
ms:contentKeyID: 55119831
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 4261fffef0934e01cbfbcc7068377cc392af178c
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28716428"
---
# <a name="create-a-custom-contact-item"></a>Создание настраиваемого элемента контакта

В этом примере показано, как создать настраиваемый элемент контакта и настроить предопределенные и пользовательские свойства.

## <a name="example"></a>Пример

> [!NOTE] 
> Приведенный ниже пример кода представляет собой фрагмент из книги [Программирование приложений для Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).

Объект [ContactItem](https://msdn.microsoft.com/library/bb644956\(v=office.15\)) представляет контакт в папке контактов и имеет более 100 встроенных свойств, таких как [FirstName](https://msdn.microsoft.com/library/bb652965\(v=office.15\)) и [LastName](https://msdn.microsoft.com/library/bb609750\(v=office.15\)). Иногда встроенных свойств недостаточно и нужно добавить настраиваемые свойства, что можно сделать с помощью коллекции [UserProperties](https://msdn.microsoft.com/library/bb611428\(v=office.15\)).

В представленном ниже примере кода CreateCustomItem создает настраиваемый объект **ContactItem**, называет его "Shoe Store" и вызывает метод [Add(String, Object)](https://msdn.microsoft.com/library/bb645065\(v=office.15\)), чтобы добавить его в папку с именем "Shoe Store". CreateCustomItem сначала получает папку "Shoe Store" с помощью метода [GetDefaultFolder(OlDefaultFolders)](https://msdn.microsoft.com/library/bb646473\(v=office.15\)). Папка "Shoe Store" вложена в папку контактов по умолчанию. Затем CreateCustomItem устанавливает свойства **FirstName** и **LastName** и создает пользовательское свойство ("Shoe Size") с помощью коллекции **UserProperties**.

Если вы используете Visual Studio для тестирования этого примера кода, сначала добавьте ссылку на компонент Microsoft Outlook 15.0 Object Library и задайте переменную Outlook при импорте пространства имен **Microsoft.Office.Interop.Outlook**. Инструкция **using** не должна идти непосредственно перед функциями в примере кода, но ее нужно добавить перед открытым объявлением Class. В следующей строке кода показано, как выполнить импорт и назначение в C\#.

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```csharp
private void CreateCustomItem()
{
    Outlook.Folder folder =
        Application.Session.GetDefaultFolder(
        Outlook.OlDefaultFolders.olFolderContacts).Folders[
        "Shoe Store"] as Outlook.Folder;
    Outlook.ContactItem contact =
        folder.Items.Add(
        "IPM.Contact.Shoe Store") as Outlook.ContactItem;
    contact.FirstName = "Michael";
    contact.LastName = "Affronti";
    contact.UserProperties["Shoe Size"].Value = "9";
    contact.Save();
}
```

## <a name="see-also"></a>См. также

- [Контакты](contacts.md)


---
title: Назначение категорий элементу
TOCTitle: Assign categories to an item
ms:assetid: 4070801b-994a-46df-91fe-4efca834886e
ms:mtpsurl: https://msdn.microsoft.com/library/Ff424469(v=office.15)
ms:contentKeyID: 55119828
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: f8b94d03a1aea447c4dba859659f044d8ec11994
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359735"
---
# <a name="assign-categories-to-an-item"></a>Назначение категорий элементу

В этом примере показано, как назначить категории элементу с помощью его свойства **Categories**.

## <a name="example"></a>Пример

> [!NOTE] 
> Приведенный ниже пример кода взят из книги [Программирование приложений для Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).


Чтобы назначить категории элементу, используйте специальное свойство **Categories** элемента. В этом примере кода используется вспомогательный класс OutlookItem, определенный в статье [Создание вспомогательного класса для доступа к общим элементам Outlook](how-to-create-a-helper-class-to-access-common-outlook-item-members.md), с помощью которого можно удобно вызвать свойство OutlookItem.**Categories** без необходимости сначала выполнять приведение элемента. Свойство **Categories** получает или задает категории, представленные в виде строки с разделителями-запятыми, которая может содержать не более 255 знаков. Запятые и пробелы используются для разделения значений категории. Назначение категории, не входящей в коллекцию [Categories](https://msdn.microsoft.com/library/bb646607\(v=office.15\)) объекта [NameSpace](https://msdn.microsoft.com/library/bb645857\(v=office.15\)), приведет к тому, что категория не будет отображать цвет.

В следующем примере кода процедура AssignCategories создает ограничение для элементов с символами "ISV" в теме, сначала с помощью запроса DASL отфильтровывая в папке "Входящие" такие элементы. Затем AssignCategories проходит по отфильтрованным элементам с помощью класса **OutlookItem** и в том случае, если строка, возвращенная **item.Categories**, не является пустой ссылкой или не была назначена категории ISV, назначает категорию ISV этому элементу.

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```

```csharp
private void AssignCategories()
{
    string filter = "@SQL=" + "\"" + "urn:schemas:httpmail:subject"
        + "\"" + " ci_phrasematch 'ISV'";
    Outlook.Items items =
        Application.Session.GetDefaultFolder(
        Outlook.OlDefaultFolders.olFolderInbox).Items.Restrict(filter);
    for (int i = 1; i <= items.Count; i++)
    {
        OutlookItem item = new OutlookItem(items[i]);
        string existingCategories = item.Categories;
        if (String.IsNullOrEmpty(existingCategories))
        {
            item.Categories = "ISV";
        }
        else
        {
            if (item.Categories.Contains("ISV") == false)
            {
                item.Categories = existingCategories + ", ISV";
            }
        }
        item.Save();
    }
}
```

## <a name="see-also"></a>См. также

- [Цветовые категории](color-categories.md)


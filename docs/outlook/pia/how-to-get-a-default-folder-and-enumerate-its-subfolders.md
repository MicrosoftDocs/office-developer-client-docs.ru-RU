---
title: Получение папки, используемой по умолчанию, и выполнение перечисления вложенных в нее папок
TOCTitle: Get a default folder and enumerate its subfolders
ms:assetid: 587e8392-cb03-442c-9058-1282f36dabdb
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184610(v=office.15)
ms:contentKeyID: 55119857
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 6151b564957f9574f3a65502584716f5bab0c17e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32320239"
---
# <a name="get-a-default-folder-and-enumerate-its-subfolders"></a>Получение папки, используемой по умолчанию, и выполнение перечисления вложенных в нее папок

В этом примере показано, как получить папку, используемую по умолчанию, в хранилище пользователя, используемом по умолчанию, и выполнить перечисление вложенных в нее папок.

## <a name="example"></a>Пример

> [!NOTE] 
> Приведенный ниже пример кода взят из книги [Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493) ("Программирование приложений для Microsoft Office Outlook 2007").

В примере кода ниже показано, как GetRSSFeeds с помощью метода [GetDefaultFolder(OlDefaultFolders)](https://msdn.microsoft.com/library/bb646473\(v=office.15\)) объекта [NameSpace](https://msdn.microsoft.com/library/bb645857\(v=office.15\)) получает корневую папку "RSS Feeds" ("RSS-каналы") пользователя. Затем метод GetRSSFeeds отображает окно сообщения с именами папок для всех RSS-каналов в папке "RSS Feeds" ("RSS-каналы").

Если вы используете Visual Studio для тестирования этого примера кода, сначала добавьте ссылку на компонент Microsoft Outlook 15.0 Object Library и задайте переменную Outlook при импорте пространства имен **Microsoft.Office.Interop.Outlook**. Инструкция **using** не должна находиться непосредственно перед функциями в примере кода, но ее нужно добавить перед объявлением общедоступного класса. В приведенной ниже строке кода показано, как выполнить импорт и назначение на языке C\#.

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```csharp
private void GetRSSFeeds()
{
    Outlook.Folder folder =
        Application.Session.GetDefaultFolder(
        Outlook.OlDefaultFolders.olFolderRssFeeds)
        as Outlook.Folder;
    if (folder != null)
    {
        if (folder.Folders.Count > 0)
        {
            StringBuilder sb = new StringBuilder();
            foreach (Outlook.Folder subfolder
                in folder.Folders)
            {
                sb.AppendLine(subfolder.Name);
            }
            MessageBox.Show(sb.ToString(),
                "RSS Feeds",
                MessageBoxButtons.OK,
                MessageBoxIcon.Information);
        }
    }
}
```

## <a name="see-also"></a>См. также

- [Folders](folders.md)


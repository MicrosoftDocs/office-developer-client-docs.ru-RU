---
title: Перечисление папок
TOCTitle: Enumerate folders
ms:assetid: 564730f9-3da3-4eff-b207-64ac4fec632d
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184607(v=office.15)
ms:contentKeyID: 55119855
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 0fe79f78ba1aab1e54df0b0bc88fa0c55c73e187
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357402"
---
# <a name="enumerate-folders"></a>Перечисление папок

В этом примере показано, как перечислять папки путем итерации по коллекциям папок.

## <a name="example"></a>Пример

> [!NOTE] 
> Приведенный ниже пример кода представляет собой фрагмент из книги [Программирование приложений для Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).

В следующем примере кода метод EnumerateFoldersInDefaultStore сначала получает корневую папку хранилища по умолчанию, используя метод [GetRootFolder()](https://msdn.microsoft.com/library/bb645807\(v=office.15\)). Затем для корневой папки вызывается метод EnumerateFolders. EnumerateFolders берет корневую папку и перебирает папки хранилища по умолчанию, представленного корневой папкой. EnumerateFolders сначала использует свойство [Folders](https://msdn.microsoft.com/library/bb646854\(v=office.15\)), чтобы получить вложенные папки объекта [Folder](https://msdn.microsoft.com/library/bb645774\(v=office.15\)) корневой папки. Затем рекурсивно вызывается EnumerateFolders, чтобы перечислить все папки в иерархии. Наконец, EnumerateFolders записывает свойство [FolderPath](https://msdn.microsoft.com/library/bb647409\(v=office.15\)) каждой папки **Folder** в прослушиватели трассировки коллекции [Listeners](https://msdn.microsoft.com/library/system.diagnostics.debug.listeners.aspx).

Если вы используете Visual Studio для тестирования этого примера кода, сначала добавьте ссылку на компонент Microsoft Outlook 15.0 Object Library и задайте переменную Outlook при импорте пространства имен **Microsoft.Office.Interop.Outlook**. Инструкция **using** не должна находиться непосредственно перед функциями в примере кода, но ее нужно добавить перед объявлением общедоступного класса. В приведенной ниже строке кода показано, как выполнить импорт и назначение на языке C\#.

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```csharp
private void EnumerateFoldersInDefaultStore()
{
    Outlook.Folder root =
        Application.Session.
        DefaultStore.GetRootFolder() as Outlook.Folder;
    EnumerateFolders(root);
}

// Uses recursion to enumerate Outlook subfolders.
private void EnumerateFolders(Outlook.Folder folder)
{
    Outlook.Folders childFolders =
        folder.Folders;
    if (childFolders.Count > 0)
    {
        foreach (Outlook.Folder childFolder in childFolders)
        {
            // Write the folder path.
            Debug.WriteLine(childFolder.FolderPath);
            // Call EnumerateFolders using childFolder.
            EnumerateFolders(childFolder);
        }
    }
}               
```

## <a name="see-also"></a>См. также

- [Folders](folders.md)


---
title: Перечисление папок
TOCTitle: Enumerate folders
ms:assetid: 564730f9-3da3-4eff-b207-64ac4fec632d
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184607(v=office.15)
ms:contentKeyID: 55119855
ms.date: 07/24/2014
mtps_version: v=office.15
ms.openlocfilehash: 91165754ccd86ebff07ec99e60f0ad1a167dea05
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25406255"
---
# <a name="enumerate-folders"></a>Перечисление папок

В этом примере показано, как перечислять папки путем итерации по коллекциям папок.

## <a name="example"></a>Пример

> [!NOTE] 
> Приведенный ниже пример кода представляет собой фрагмент из книги [Программирование приложений для Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).

В следующем примере кода метод EnumerateFoldersInDefaultStore сначала получает корневую папку хранилища по умолчанию, используя метод [GetRootFolder()](https://msdn.microsoft.com/library/bb645807\(v=office.15\)). Затем для корневой папки вызывается метод EnumerateFolders. EnumerateFolders берет корневую папку и перебирает папки хранилища по умолчанию, представленного корневой папкой. EnumerateFolders сначала использует свойство [Folders](https://msdn.microsoft.com/library/bb646854\(v=office.15\)), чтобы получить вложенные папки объекта [Folder](https://msdn.microsoft.com/library/bb645774\(v=office.15\)) корневой папки. Затем рекурсивно вызывается EnumerateFolders, чтобы перечислить все папки в иерархии. Наконец, EnumerateFolders записывает свойство [FolderPath](https://msdn.microsoft.com/library/bb647409\(v=office.15\)) каждой папки **Folder** в прослушиватели трассировки коллекции [Listeners](https://msdn.microsoft.com/library/system.diagnostics.debug.listeners.aspx).

Если вы используете Visual Studio для тестирования этого примера кода, сначала добавьте ссылку на компонент Microsoft Outlook 15.0 Object Library и задайте переменную Outlook при импорте пространства имен **Microsoft.Office.Interop.Outlook**. Инструкция **using** не должна идти непосредственно перед функциями в примере кода, но ее нужно добавить перед открытым объявлением Class. В следующей строке кода показано, как выполнить импорт и назначение в C\#.

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

- [Папки](folders.md)


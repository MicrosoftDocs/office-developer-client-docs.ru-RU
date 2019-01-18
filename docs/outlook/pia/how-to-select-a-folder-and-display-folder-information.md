---
title: Выбор папки и отображение сведений о папке
TOCTitle: Select a folder and display folder information
ms:assetid: 737b19bc-1efd-4ddb-86d0-72b3ab8eaf8c
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184616(v=office.15)
ms:contentKeyID: 55119859
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 41dc96f26e7e0040467096731cb16ae7c0c08f74
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28721942"
---
# <a name="select-a-folder-and-display-folder-information"></a>Выбор папки и отображение сведений о папке

В этом примере показан способ программного отображения сведений о папке, выбранной пользователем из определенного списка папок.

## <a name="example"></a>Пример

> [!NOTE] 
> Приведенный ниже пример кода представляет собой фрагмент из книги [Программирование приложений для Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).

В следующем примере кода ShowFolderInfo использует метод [PickFolder()](https://msdn.microsoft.com/library/bb623484\(v=office.15\)) объекта [NameSpace](https://msdn.microsoft.com/library/bb645857\(v=office.15\)), чтобы вывести для пользователя диалоговое окно **Выбор папки** и дождаться, пока пользователь выберет папку. После того как пользователь выберет папку, отображаются свойства [EntryID](https://msdn.microsoft.com/library/bb646192\(v=office.15\)), [StoreID](https://msdn.microsoft.com/library/bb612609\(v=office.15\)), [UnReadItemCount](https://msdn.microsoft.com/library/bb610138\(v=office.15\)), [DefaultMessageClass](https://msdn.microsoft.com/library/bb646541\(v=office.15\)), [CurrentView](https://msdn.microsoft.com/library/bb612411\(v=office.15\)), [Name](https://msdn.microsoft.com/library/bb623727\(v=office.15\)) и [FolderPath](https://msdn.microsoft.com/library/bb647409\(v=office.15\)) этой папки. Затем в примере вызывается метод [GetFolderFromID](https://msdn.microsoft.com/library/bb647784\(v=office.15\)), чтобы создать новый объект [Folder](https://msdn.microsoft.com/library/bb645774\(v=office.15\)) и отобразить папку.

Если вы используете Visual Studio для тестирования этого примера кода, сначала добавьте ссылку на компонент Microsoft Outlook 15.0 Object Library и задайте переменную Outlook при импорте пространства имен **Microsoft.Office.Interop.Outlook**. Инструкция **using** не должна идти непосредственно перед функциями в примере кода, но ее нужно добавить перед открытым объявлением Class. В следующей строке кода показано, как выполнить импорт и назначение в C\#.

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```csharp
private void ShowFolderInfo()
{
    Outlook.Folder folder =
        Application.Session.PickFolder()
        as Outlook.Folder;
    if (folder != null)
    {
        StringBuilder sb = new StringBuilder();
        sb.AppendLine("Folder EntryID:");
        sb.AppendLine(folder.EntryID);
        sb.AppendLine();
        sb.AppendLine("Folder StoreID:");
        sb.AppendLine(folder.StoreID);
        sb.AppendLine();
        sb.AppendLine("Unread Item Count: "
            + folder.UnReadItemCount);
        sb.AppendLine("Default MessageClass: "
            + folder.DefaultMessageClass);
        sb.AppendLine("Current View: "
            + folder.CurrentView.Name);
        sb.AppendLine("Folder Path: "
            + folder.FolderPath);
        MessageBox.Show(sb.ToString(),
            "Folder Information",
            MessageBoxButtons.OK,
            MessageBoxIcon.Information);
        Outlook.Folder folderFromID =
            Application.Session.GetFolderFromID(
            folder.EntryID, folder.StoreID)
            as Outlook.Folder;
        folderFromID.Display();
    }
}
```

## <a name="see-also"></a>См. также

- [Папки](folders.md)


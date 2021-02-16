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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316039"
---
# <a name="select-a-folder-and-display-folder-information"></a><span data-ttu-id="a6db1-102">Выбор папки и отображение сведений о папке</span><span class="sxs-lookup"><span data-stu-id="a6db1-102">Select a folder and display folder information</span></span>

<span data-ttu-id="a6db1-103">В этом примере показан способ программного отображения сведений о папке, выбранной пользователем из определенного списка папок.</span><span class="sxs-lookup"><span data-stu-id="a6db1-103">This example shows how to programmatically display information about a folder that a user selects from a specified folder list.</span></span>

## <a name="example"></a><span data-ttu-id="a6db1-104">Пример</span><span class="sxs-lookup"><span data-stu-id="a6db1-104">Example</span></span>

> [!NOTE] 
> <span data-ttu-id="a6db1-105">Приведенный ниже пример кода представляет собой фрагмент из книги [Программирование приложений для Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).</span><span class="sxs-lookup"><span data-stu-id="a6db1-105">The following code example is an excerpt from [Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).</span></span>

<span data-ttu-id="a6db1-106">В следующем примере кода ShowFolderInfo использует метод [PickFolder()](https://msdn.microsoft.com/library/bb623484\(v=office.15\)) объекта [NameSpace](https://msdn.microsoft.com/library/bb645857\(v=office.15\)), чтобы вывести для пользователя диалоговое окно **Выбор папки** и дождаться, пока пользователь выберет папку.</span><span class="sxs-lookup"><span data-stu-id="a6db1-106">In the following code example, ShowFolderInfo uses the [PickFolder()](https://msdn.microsoft.com/library/bb623484\(v=office.15\)) method of the [NameSpace](https://msdn.microsoft.com/library/bb645857\(v=office.15\)) object to display a **Select Folder** dialog box to the user, and waits for the user to select a folder.</span></span> <span data-ttu-id="a6db1-107">После того как пользователь выберет папку, отображаются свойства [EntryID](https://msdn.microsoft.com/library/bb646192\(v=office.15\)), [StoreID](https://msdn.microsoft.com/library/bb612609\(v=office.15\)), [UnReadItemCount](https://msdn.microsoft.com/library/bb610138\(v=office.15\)), [DefaultMessageClass](https://msdn.microsoft.com/library/bb646541\(v=office.15\)), [CurrentView](https://msdn.microsoft.com/library/bb612411\(v=office.15\)), [Name](https://msdn.microsoft.com/library/bb623727\(v=office.15\)) и [FolderPath](https://msdn.microsoft.com/library/bb647409\(v=office.15\)) этой папки.</span><span class="sxs-lookup"><span data-stu-id="a6db1-107">Once the user selects a folder, its [EntryID](https://msdn.microsoft.com/library/bb646192\(v=office.15\)), [StoreID](https://msdn.microsoft.com/library/bb612609\(v=office.15\)), [UnReadItemCount](https://msdn.microsoft.com/library/bb610138\(v=office.15\)), [DefaultMessageClass](https://msdn.microsoft.com/library/bb646541\(v=office.15\)), [CurrentView](https://msdn.microsoft.com/library/bb612411\(v=office.15\)), [Name](https://msdn.microsoft.com/library/bb623727\(v=office.15\)), and [FolderPath](https://msdn.microsoft.com/library/bb647409\(v=office.15\)) properties are displayed.</span></span> <span data-ttu-id="a6db1-108">Затем в примере вызывается метод [GetFolderFromID](https://msdn.microsoft.com/library/bb647784\(v=office.15\)), чтобы создать новый объект [Folder](https://msdn.microsoft.com/library/bb645774\(v=office.15\)) и отобразить папку.</span><span class="sxs-lookup"><span data-stu-id="a6db1-108">The example then calls the [GetFolderFromID](https://msdn.microsoft.com/library/bb647784\(v=office.15\)) method to create a new [Folder](https://msdn.microsoft.com/library/bb645774\(v=office.15\)) object and display the folder.</span></span>

<span data-ttu-id="a6db1-109">Если вы используете Visual Studio для тестирования этого примера кода, сначала добавьте ссылку на компонент Microsoft Outlook 15.0 Object Library и задайте переменную Outlook при импорте пространства имен **Microsoft.Office.Interop.Outlook**.</span><span class="sxs-lookup"><span data-stu-id="a6db1-109">If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the Outlook variable when you import the **Microsoft.Office.Interop.Outlook** namespace.</span></span> <span data-ttu-id="a6db1-110">Инструкция **using** не должна находиться непосредственно перед функциями в примере кода, но ее нужно добавить перед объявлением общедоступного класса.</span><span class="sxs-lookup"><span data-stu-id="a6db1-110">The **using** statement must not occur directly before the functions in the code example but must be added before the public Class declaration.</span></span> <span data-ttu-id="a6db1-111">В приведенной ниже строке кода показано, как выполнить импорт и назначение на языке C\#.</span><span class="sxs-lookup"><span data-stu-id="a6db1-111">The following line of code shows how to do the import and assignment in C\#.</span></span>

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

## <a name="see-also"></a><span data-ttu-id="a6db1-112">См. также</span><span class="sxs-lookup"><span data-stu-id="a6db1-112">See also</span></span>

- [<span data-ttu-id="a6db1-113">Folders</span><span class="sxs-lookup"><span data-stu-id="a6db1-113">Folders</span></span>](folders.md)


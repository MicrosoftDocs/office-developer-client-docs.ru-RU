---
title: Добавление папки в список папок
TOCTitle: Add a folder to the folder list
ms:assetid: f636a190-d966-4421-9977-0ead2bff5eee
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184655(v=office.15)
ms:contentKeyID: 55119850
ms.date: 07/24/2014
mtps_version: v=office.15
ms.openlocfilehash: dc8ead207261cfd4835e230981d923211771de7b
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25405527"
---
# <a name="add-a-folder-to-the-folder-list"></a><span data-ttu-id="fad42-102">Добавление папки в список папок</span><span class="sxs-lookup"><span data-stu-id="fad42-102">Add a folder to the folder list</span></span>

<span data-ttu-id="fad42-103">В этом примере показано, как использовать метод [Add(String, Object)](https://msdn.microsoft.com/library/bb645065\(v=office.15\)) для добавления папки в список папок Outlook.</span><span class="sxs-lookup"><span data-stu-id="fad42-103">This example shows how to use the [Add(String, Object)](https://msdn.microsoft.com/library/bb645065\(v=office.15\)) method to add a folder to the Outlook folder list.</span></span>

## <a name="example"></a><span data-ttu-id="fad42-104">Пример</span><span class="sxs-lookup"><span data-stu-id="fad42-104">Example</span></span>

> [!NOTE] 
> <span data-ttu-id="fad42-105">Приведенный ниже пример кода представляет собой фрагмент из книги [Программирование приложений для Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).</span><span class="sxs-lookup"><span data-stu-id="fad42-105">The following code example is an excerpt from  [Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493)  , from Microsoft Press (ISBN 9780735622494, copyright Microsoft Press 2007, all rights reserved).</span></span>


<span data-ttu-id="fad42-106">В следующем примере кода в процедуре **AddMyNewFolder** вызывается метод **Add** коллекции [Folders](https://msdn.microsoft.com/library/bb612071\(v=office.15\)) для добавления объекта [Folder](https://msdn.microsoft.com/library/bb645774\(v=office.15\)), представляющего папку "My New Folder" в папке **Входящие** из списка папок Outlook.</span><span class="sxs-lookup"><span data-stu-id="fad42-106">In the following code example,  \*\*\*\* calls the **Add** method of the [Folders](https://msdn.microsoft.com/library/bb612071\(v=office.15\)) collection to add a [Folder](https://msdn.microsoft.com/library/bb645774\(v=office.15\)) object that represents a folder called "My New Folder" to the **Inbox** in the Outlook folder list.</span></span> <span data-ttu-id="fad42-107">После этого отображается папка "My New Folder".</span><span class="sxs-lookup"><span data-stu-id="fad42-107">"My New Folder" is then displayed.</span></span>

<span data-ttu-id="fad42-108">Если вы используете Visual Studio для тестирования этого примера кода, сначала добавьте ссылку на компонент Microsoft Outlook 15.0 Object Library и задайте переменную Outlook при импорте пространства имен **Microsoft.Office.Interop.Outlook**.</span><span class="sxs-lookup"><span data-stu-id="fad42-108">If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the   variable when you import the Microsoft.Office.Interop.Outlook namespace.</span></span> <span data-ttu-id="fad42-109">Инструкция **using** не должна идти непосредственно перед функциями в примере кода, но ее нужно добавить перед открытым объявлением Class.</span><span class="sxs-lookup"><span data-stu-id="fad42-109">The using statement must not occur directly before the functions in the code example but must be added before the public   declaration.</span></span> <span data-ttu-id="fad42-110">В следующей строке кода показано, как выполнить импорт и назначение в C\#.</span><span class="sxs-lookup"><span data-stu-id="fad42-110">The following line of code shows how to do the import and assignment in C#.</span></span>

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```csharp
private void AddMyNewFolder()
{
    Outlook.Folder folder =
        Application.Session.GetDefaultFolder(
        Outlook.OlDefaultFolders.olFolderInbox)
        as Outlook.Folder;
    Outlook.Folders folders = folder.Folders;
    try
    {
        Outlook.Folder newFolder = folders.Add(
            "My New Folder", Type.Missing)
            as Outlook.Folder;
        newFolder.Display();
    }
    catch
    {
        MessageBox.Show(
            "Could not add 'My New Folder'",
            "Add Folder",
            MessageBoxButtons.OK,
            MessageBoxIcon.Error);
    }
}
```

## <a name="see-also"></a><span data-ttu-id="fad42-111">См. также</span><span class="sxs-lookup"><span data-stu-id="fad42-111">See also</span></span>

- [<span data-ttu-id="fad42-112">Папки</span><span class="sxs-lookup"><span data-stu-id="fad42-112">Folders</span></span>](folders.md)


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
# <a name="enumerate-folders"></a><span data-ttu-id="629d0-102">Перечисление папок</span><span class="sxs-lookup"><span data-stu-id="629d0-102">Enumerate folders</span></span>

<span data-ttu-id="629d0-103">В этом примере показано, как перечислять папки путем итерации по коллекциям папок.</span><span class="sxs-lookup"><span data-stu-id="629d0-103">This example shows how to enumerate folders by iterating through a collection of folders.</span></span>

## <a name="example"></a><span data-ttu-id="629d0-104">Пример</span><span class="sxs-lookup"><span data-stu-id="629d0-104">Example</span></span>

> [!NOTE] 
> <span data-ttu-id="629d0-105">Приведенный ниже пример кода представляет собой фрагмент из книги [Программирование приложений для Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).</span><span class="sxs-lookup"><span data-stu-id="629d0-105">The following code example is an excerpt from  [Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493)  , from Microsoft Press (ISBN 9780735622494, copyright Microsoft Press 2007, all rights reserved).</span></span>

<span data-ttu-id="629d0-106">В следующем примере кода метод EnumerateFoldersInDefaultStore сначала получает корневую папку хранилища по умолчанию, используя метод [GetRootFolder()](https://msdn.microsoft.com/library/bb645807\(v=office.15\)).</span><span class="sxs-lookup"><span data-stu-id="629d0-106">In the following code example, the   method first obtains the root folder for the default store by using the GetRootFolder() method.</span></span> <span data-ttu-id="629d0-107">Затем для корневой папки вызывается метод EnumerateFolders.</span><span class="sxs-lookup"><span data-stu-id="629d0-107">It then calls the   method on the root folder.</span></span> <span data-ttu-id="629d0-108">EnumerateFolders берет корневую папку и перебирает папки хранилища по умолчанию, представленного корневой папкой.</span><span class="sxs-lookup"><span data-stu-id="629d0-108"> takes in a root folder and walks through the folders of the default store that the root folder represents.</span></span> <span data-ttu-id="629d0-109">EnumerateFolders сначала использует свойство [Folders](https://msdn.microsoft.com/library/bb646854\(v=office.15\)), чтобы получить вложенные папки объекта [Folder](https://msdn.microsoft.com/library/bb645774\(v=office.15\)) корневой папки.</span><span class="sxs-lookup"><span data-stu-id="629d0-109"> first uses the Folders property to obtain the subfolders of the root Folder object.</span></span> <span data-ttu-id="629d0-110">Затем рекурсивно вызывается EnumerateFolders, чтобы перечислить все папки в иерархии.</span><span class="sxs-lookup"><span data-stu-id="629d0-110"> is then called recursively to enumerate all the folders in a hierarchy.</span></span> <span data-ttu-id="629d0-111">Наконец, EnumerateFolders записывает свойство [FolderPath](https://msdn.microsoft.com/library/bb647409\(v=office.15\)) каждой папки **Folder** в прослушиватели трассировки коллекции [Listeners](https://msdn.microsoft.com/library/system.diagnostics.debug.listeners.aspx).</span><span class="sxs-lookup"><span data-stu-id="629d0-111">Finally,   writes the FolderPath property of each Folder to the trace listeners in the Listeners collection.</span></span>

<span data-ttu-id="629d0-112">Если вы используете Visual Studio для тестирования этого примера кода, сначала добавьте ссылку на компонент Microsoft Outlook 15.0 Object Library и задайте переменную Outlook при импорте пространства имен **Microsoft.Office.Interop.Outlook**.</span><span class="sxs-lookup"><span data-stu-id="629d0-112">If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the   variable when you import the Microsoft.Office.Interop.Outlook namespace.</span></span> <span data-ttu-id="629d0-113">Инструкция **using** не должна идти непосредственно перед функциями в примере кода, но ее нужно добавить перед открытым объявлением Class.</span><span class="sxs-lookup"><span data-stu-id="629d0-113">The using statement must not occur directly before the functions in the code example but must be added before the public   declaration.</span></span> <span data-ttu-id="629d0-114">В следующей строке кода показано, как выполнить импорт и назначение в C\#.</span><span class="sxs-lookup"><span data-stu-id="629d0-114">The following line of code shows how to do the import and assignment in C#.</span></span>

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

## <a name="see-also"></a><span data-ttu-id="629d0-115">См. также</span><span class="sxs-lookup"><span data-stu-id="629d0-115">See also</span></span>

- [<span data-ttu-id="629d0-116">Папки</span><span class="sxs-lookup"><span data-stu-id="629d0-116">Folders</span></span>](folders.md)


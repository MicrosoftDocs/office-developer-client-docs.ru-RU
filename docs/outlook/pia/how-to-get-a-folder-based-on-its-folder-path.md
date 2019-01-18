---
title: Получение папки на основе пути к ней
TOCTitle: Get a folder based on its folder path
ms:assetid: 613f2209-667c-48f0-82cf-86e3c9a24cb4
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184612(v=office.15)
ms:contentKeyID: 55119858
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: fed1e7eb39f31ddd4340fc82a16e31ec67523a9d
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28708132"
---
# <a name="get-a-folder-based-on-its-folder-path"></a><span data-ttu-id="b5721-102">Получение папки на основе пути к ней</span><span class="sxs-lookup"><span data-stu-id="b5721-102">Get a folder based on its folder path</span></span>

<span data-ttu-id="b5721-103">В этом примере используется путь к папке для получения связанной папки.</span><span class="sxs-lookup"><span data-stu-id="b5721-103">This example takes a folder path and obtains the associated folder.</span></span>

## <a name="example"></a><span data-ttu-id="b5721-104">Пример</span><span class="sxs-lookup"><span data-stu-id="b5721-104">Example</span></span>

> [!NOTE] 
> <span data-ttu-id="b5721-105">Приведенный ниже пример кода представляет собой фрагмент из книги [Программирование приложений для Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).</span><span class="sxs-lookup"><span data-stu-id="b5721-105">The following code example is an excerpt from [Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).</span></span>

<span data-ttu-id="b5721-106">В следующем примере кода метод GetKeyContacts использует свойство [GetRootFolder()](https://msdn.microsoft.com/library/bb645807\(v=office.15\)), чтобы получить путь для папки Contacts\\Key Contacts.</span><span class="sxs-lookup"><span data-stu-id="b5721-106">In the following code example, the GetKeyContacts method uses the [GetRootFolder()](https://msdn.microsoft.com/library/bb645807\(v=office.15\)) property to obtain the folder path of the Contacts\\Key Contacts folder.</span></span> <span data-ttu-id="b5721-107">Затем вызывается метод GetFolder с использованием свойства [FolderPath](https://msdn.microsoft.com/library/bb647409\(v=office.15\)) в качестве аргумента.</span><span class="sxs-lookup"><span data-stu-id="b5721-107">The GetFolder method is then called by using the [FolderPath](https://msdn.microsoft.com/library/bb647409\(v=office.15\)) property as the argument.</span></span> <span data-ttu-id="b5721-108">Если GetFolder возвращает папку, появляется сообщение о том, что папка Key Contacts найдена.</span><span class="sxs-lookup"><span data-stu-id="b5721-108">If GetFolder returns a folder, a message will appear saying the Key Contacts are found.</span></span> <span data-ttu-id="b5721-109">Метод GetFolder получает путь к папке и возвращает правильный объект [Folder](https://msdn.microsoft.com/library/bb645774\(v=office.15\)).</span><span class="sxs-lookup"><span data-stu-id="b5721-109">The GetFolder method takes in a path to a folder and returns the correct [Folder](https://msdn.microsoft.com/library/bb645774\(v=office.15\)) object.</span></span> <span data-ttu-id="b5721-110">Для этого свойство **FolderPath** сначала разбивается на массив из элементов string, который затем используется для поиска правильного объекта **Folder**, начиная с верхнего компонента свойства **FolderPath**.</span><span class="sxs-lookup"><span data-stu-id="b5721-110">This is done by first splitting the **FolderPath** property into a string array and then using the array to find the correct **Folder** object starting from the top of the **FolderPath** property.</span></span> <span data-ttu-id="b5721-111">Если заданная папка не найдена, GetFolder возвращает пустую ссылку (NULL).</span><span class="sxs-lookup"><span data-stu-id="b5721-111">If the specified folder is not found, GetFolder returns a null reference.</span></span>

<span data-ttu-id="b5721-112">Если вы используете Visual Studio для тестирования этого примера кода, сначала добавьте ссылку на компонент Microsoft Outlook 15.0 Object Library и задайте переменную Outlook при импорте пространства имен **Microsoft.Office.Interop.Outlook**.</span><span class="sxs-lookup"><span data-stu-id="b5721-112">If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the Outlook variable when you import the **Microsoft.Office.Interop.Outlook** namespace.</span></span> <span data-ttu-id="b5721-113">Инструкция **using** не должна идти непосредственно перед функциями в примере кода, но ее нужно добавить перед открытым объявлением Class.</span><span class="sxs-lookup"><span data-stu-id="b5721-113">The **using** statement must not occur directly before the functions in the code example but must be added before the public Class declaration.</span></span> <span data-ttu-id="b5721-114">В следующей строке кода показано, как выполнить импорт и назначение в C\#.</span><span class="sxs-lookup"><span data-stu-id="b5721-114">The following line of code shows how to do the import and assignment in C\#.</span></span>

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```csharp
private void GetKeyContacts()
{
    string folderPath =
        Application.Session.
        DefaultStore.GetRootFolder().FolderPath
        + @"\Contacts\Key Contacts";
    Outlook.Folder folder = GetFolder(folderPath);
    if (folder != null)
    {
        //Work with folder here
        Debug.WriteLine("Found Key Contacts");
    }
}

// Returns Folder object based on folder path
private Outlook.Folder GetFolder(string folderPath)
{
    Outlook.Folder folder;
    string backslash = @"\";
    try
    {
        if (folderPath.StartsWith(@"\\"))
        {
            folderPath = folderPath.Remove(0, 2);
        }
        String[] folders =
            folderPath.Split(backslash.ToCharArray());
        folder =
            Application.Session.Folders[folders[0]]
            as Outlook.Folder;
        if (folder != null)
        {
            for (int i = 1; i <= folders.GetUpperBound(0); i++)
            {
                Outlook.Folders subFolders = folder.Folders;
                folder = subFolders[folders[i]]
                    as Outlook.Folder;
                if (folder == null)
                {
                    return null;
                }
            }
        }
        return folder;
    }
    catch { return null; }
}        
```

## <a name="see-also"></a><span data-ttu-id="b5721-115">См. также</span><span class="sxs-lookup"><span data-stu-id="b5721-115">See also</span></span>

- [<span data-ttu-id="b5721-116">Папки</span><span class="sxs-lookup"><span data-stu-id="b5721-116">Folders</span></span>](folders.md)


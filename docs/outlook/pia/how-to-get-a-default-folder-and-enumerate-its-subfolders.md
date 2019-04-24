---
title: Получение папки, используемой по умолчанию, и перечисление вложенных в нее папок
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
# <a name="get-a-default-folder-and-enumerate-its-subfolders"></a><span data-ttu-id="6ce3d-102">Получение папки, используемой по умолчанию, и выполнение перечисления вложенных в нее папок</span><span class="sxs-lookup"><span data-stu-id="6ce3d-102">Get a default folder and enumerate its subfolders</span></span>

<span data-ttu-id="6ce3d-103">В этом примере показано, как получить папку, используемую по умолчанию, в хранилище пользователя, используемом по умолчанию, и выполнить перечисление вложенных в нее папок.</span><span class="sxs-lookup"><span data-stu-id="6ce3d-103">This example shows how to obtain a default folder in the user’s default store and enumerate its subfolders.</span></span>

## <a name="example"></a><span data-ttu-id="6ce3d-104">Пример</span><span class="sxs-lookup"><span data-stu-id="6ce3d-104">Example</span></span>

> [!NOTE] 
> <span data-ttu-id="6ce3d-105">Приведенный ниже пример кода взят из книги [Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493) ("Программирование приложений для Microsoft Office Outlook 2007").</span><span class="sxs-lookup"><span data-stu-id="6ce3d-105">The following code example is an excerpt from [Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).</span></span>

<span data-ttu-id="6ce3d-106">В примере кода ниже показано, как GetRSSFeeds с помощью метода [GetDefaultFolder(OlDefaultFolders)](https://msdn.microsoft.com/library/bb646473\(v=office.15\)) объекта [NameSpace](https://msdn.microsoft.com/library/bb645857\(v=office.15\)) получает корневую папку "RSS Feeds" ("RSS-каналы") пользователя.</span><span class="sxs-lookup"><span data-stu-id="6ce3d-106">In the following code example, GetRSSFeeds uses the [GetDefaultFolder(OlDefaultFolders)](https://msdn.microsoft.com/library/bb646473\(v=office.15\)) method of the [NameSpace](https://msdn.microsoft.com/library/bb645857\(v=office.15\)) object to obtain the user’s RSS Feeds root folder.</span></span> <span data-ttu-id="6ce3d-107">Затем метод GetRSSFeeds отображает окно сообщения с именами папок для всех RSS-каналов в папке "RSS Feeds" ("RSS-каналы").</span><span class="sxs-lookup"><span data-stu-id="6ce3d-107">GetRSSFeeds then displays a message box that contains the folder names for all RSS feeds in the RSS Feeds folder.</span></span>

<span data-ttu-id="6ce3d-108">Если для тестирования этого примера кода вы используете Visual Studio, сначала добавьте ссылку на компонент библиотеки объектов Microsoft Outlook 15.0 и укажите переменную Outlook при импорте пространства имен **Microsoft.Office.Interop.Outlook**.</span><span class="sxs-lookup"><span data-stu-id="6ce3d-108">If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the Outlook variable when you import the **Microsoft.Office.Interop.Outlook** namespace.</span></span> <span data-ttu-id="6ce3d-109">Инструкция **using** не должна находиться непосредственно перед функциями в примере кода, но ее нужно добавить перед объявлением общедоступного класса.</span><span class="sxs-lookup"><span data-stu-id="6ce3d-109">The **using** statement must not occur directly before the functions in the code example but must be added before the public Class declaration.</span></span> <span data-ttu-id="6ce3d-110">В приведенной ниже строке кода показано, как выполнить импорт и назначение на языке C\#.</span><span class="sxs-lookup"><span data-stu-id="6ce3d-110">The following line of code shows how to do the import and assignment in C\#.</span></span>

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

## <a name="see-also"></a><span data-ttu-id="6ce3d-111">См. также</span><span class="sxs-lookup"><span data-stu-id="6ce3d-111">See also</span></span>

- [<span data-ttu-id="6ce3d-112">Folders</span><span class="sxs-lookup"><span data-stu-id="6ce3d-112">Folders</span></span>](folders.md)


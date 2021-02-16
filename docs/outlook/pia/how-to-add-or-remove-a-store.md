---
title: Добавление и удаление хранилища
TOCTitle: Add or remove a store
ms:assetid: db2930ec-ef99-4e31-86c5-820e8368e05f
ms:mtpsurl: https://msdn.microsoft.com/library/Bb612380(v=office.15)
ms:contentKeyID: 55119895
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 4346f3bf1b7bba1f26a34e1562997b4d043c8d49
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359747"
---
# <a name="add-or-remove-a-store"></a><span data-ttu-id="328ae-102">Добавление и удаление хранилища</span><span class="sxs-lookup"><span data-stu-id="328ae-102">Add or remove a store</span></span>

<span data-ttu-id="328ae-103">В этом примере показано, как добавлять и удалять хранилище в заданном профиле.</span><span class="sxs-lookup"><span data-stu-id="328ae-103">This example shows how to add and remove a store in a given profile.</span></span>

## <a name="example"></a><span data-ttu-id="328ae-104">Пример</span><span class="sxs-lookup"><span data-stu-id="328ae-104">Example</span></span>

<span data-ttu-id="328ae-105">В этом образце кода показан метод добавления и удаления хранилища в указанном профиле путем вызова метода [AddStoreEx](https://msdn.microsoft.com/library/bb623442\(v=office.15\)) и метода [RemoveStore](https://msdn.microsoft.com/library/bb610524\(v=office.15\)) соответственно по отношению к объекту [NameSpace](https://msdn.microsoft.com/library/bb645857\(v=office.15\)) .</span><span class="sxs-lookup"><span data-stu-id="328ae-105">This code sample shows how to add and remove a store in a specified profile, by calling the [AddStoreEx](https://msdn.microsoft.com/library/bb623442\(v=office.15\)) method and the [RemoveStore](https://msdn.microsoft.com/library/bb610524\(v=office.15\)) method respectively on the [NameSpace](https://msdn.microsoft.com/library/bb645857\(v=office.15\)) object.</span></span>

<span data-ttu-id="328ae-106">В Outlook можно добавить или удалить PST-хранилище только программным путем.</span><span class="sxs-lookup"><span data-stu-id="328ae-106">In Outlook, you can add or remove a PST store only programmatically.</span></span> <span data-ttu-id="328ae-107">Следующий образец кода служит для добавления хранилища Юникода и размещения PST-файла в местоположении, выбранном по умолчанию для пользовательских PST-файлов: Documents and Settings\\\<Имя_пользователя\>\\Local Settings\\Application Data\\Microsoft\\Outlook.</span><span class="sxs-lookup"><span data-stu-id="328ae-107">The following code sample adds a Unicode store and places the .pst file in the default location for user .pst files: Documents and Settings\\\<UserName\>\\Local Settings\\Application Data\\Microsoft\\Outlook.</span></span> <span data-ttu-id="328ae-108">В этом образце кода применяется Environment.SpecialFolder.LocalApplicationData для извлечения пути к папке Application Data в папке Local Settings.</span><span class="sxs-lookup"><span data-stu-id="328ae-108">The code sample uses Environment.SpecialFolder.LocalApplicationData to retrieve the path to the Application Data folder under the Local Settings folder.</span></span> <span data-ttu-id="328ae-109">После добавления хранилища образец кода удаляет хранилище.</span><span class="sxs-lookup"><span data-stu-id="328ae-109">Once the store has been added, the code sample removes the store.</span></span> <span data-ttu-id="328ae-110">Так как метод **RemoveStore** требует наличия объекта [Folder](https://msdn.microsoft.com/library/bb645774\(v=office.15\)) для удаления [Store](https://msdn.microsoft.com/library/bb609139\(v=office.15\)) , он перечисляет коллекцию [Stores](https://msdn.microsoft.com/library/bb622944\(v=office.15\)) для поиска только что добавленного объекта **Store**, исходя из свойства [FilePath](https://msdn.microsoft.com/library/bb646113\(v=office.15\)) объекта **Store**.</span><span class="sxs-lookup"><span data-stu-id="328ae-110">Because the **RemoveStore** method requires a [Folder](https://msdn.microsoft.com/library/bb645774\(v=office.15\)) object to remove the [Store](https://msdn.microsoft.com/library/bb609139\(v=office.15\)) object, it enumerates the [Stores](https://msdn.microsoft.com/library/bb622944\(v=office.15\)) collection to find the **Store** object that has just been added based on the [FilePath](https://msdn.microsoft.com/library/bb646113\(v=office.15\)) property of the **Store** object.</span></span>

<span data-ttu-id="328ae-p102">Метод **RemoveStore** удаляет только хранилище из текущего профиля. Он не удаляет PST-файл из файловой системы.</span><span class="sxs-lookup"><span data-stu-id="328ae-p102">**RemoveStore** only removes the store from the current profile. It does not delete the .pst file from the file system.</span></span>

<span data-ttu-id="328ae-113">Если для тестирования этого примера кода вы используете Visual Studio, сначала добавьте ссылку на компонент библиотеки объектов Microsoft Outlook 15.0 и укажите переменную Outlook при импорте пространства имен **Microsoft.Office.Interop.Outlook**.</span><span class="sxs-lookup"><span data-stu-id="328ae-113">If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the Outlook variable when you import the **Microsoft.Office.Interop.Outlook** namespace.</span></span> <span data-ttu-id="328ae-114">Инструкция **Imports** или **using** не должна идти непосредственно перед функциями в примере кода, но ее нужно добавить перед объявлением общедоступного класса.</span><span class="sxs-lookup"><span data-stu-id="328ae-114">The **Imports** or **using** statement must not occur directly before the functions in the code example but must be added before the public Class declaration.</span></span> <span data-ttu-id="328ae-115">В строках кода ниже показано, как выполнить импорт и назначение на Visual Basic и C\#.</span><span class="sxs-lookup"><span data-stu-id="328ae-115">The following lines of code show how to do the import and assignment in Visual Basic and C\#.</span></span>

```vb
Imports Outlook = Microsoft.Office.Interop.Outlook
```


```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```vb
Private Sub CreateUnicodePST()
    Dim path As String = Environment.GetFolderPath( _
        Environment.SpecialFolder.LocalApplicationData) _
        & "\Microsoft\Outlook\MyUnicodeStore.pst"
    Try
        Application.Session.AddStoreEx( _
            path, Outlook.OlStoreType.olStoreUnicode)
        Dim stores As Outlook.Stores = Application.Session.Stores
        For Each store As Outlook.Store In stores
            If store.FilePath = path Then
                Dim folder As Outlook.Folder = _
                    CType(store.GetRootFolder(), Outlook.Folder)
                ' Remove the store
                Application.Session.RemoveStore(folder)
            End If
        Next
    Catch ex As Exception
        Debug.WriteLine(ex.Message)
    End Try
End Sub
```


```csharp
private void CreateUnicodePST()
{
    string path = Environment.GetFolderPath(
        Environment.SpecialFolder.LocalApplicationData)
        + @"\Microsoft\Outlook\MyUnicodeStore.pst";
    try
    {
        Application.Session.AddStoreEx(
            path, Outlook.OlStoreType.olStoreUnicode);
        Outlook.Stores stores = Application.Session.Stores;
        foreach (Outlook.Store store in stores)
        {
            if (store.FilePath == path)
            {
               Outlook.Folder folder =
                    store.GetRootFolder() as Outlook.Folder;
               // Remove the store
               Application.Session.RemoveStore(folder);
            }
        }
    }
    catch (Exception ex)
    {
        Debug.WriteLine(ex.Message);
    }
}
```

## <a name="see-also"></a><span data-ttu-id="328ae-116">См. также</span><span class="sxs-lookup"><span data-stu-id="328ae-116">See also</span></span>

- [<span data-ttu-id="328ae-117">Stores</span><span class="sxs-lookup"><span data-stu-id="328ae-117">Stores</span></span>](stores.md)


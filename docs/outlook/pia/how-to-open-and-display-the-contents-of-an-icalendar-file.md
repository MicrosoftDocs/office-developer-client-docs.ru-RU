---
title: Открытие и отображение содержимого файла iCalendar
TOCTitle: Open and display the contents of an iCalendar file
ms:assetid: 2066e404-7aaf-4fd2-bf5c-9604e3fc2681
ms:mtpsurl: https://msdn.microsoft.com/library/Bb644609(v=office.15)
ms:contentKeyID: 55119818
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: fad55b4e9b98a2157d1efdab83d5495cd2169429
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32320022"
---
# <a name="open-and-display-the-contents-of-an-icalendar-file"></a><span data-ttu-id="a084d-102">Открытие и отображение содержимого файла iCalendar</span><span class="sxs-lookup"><span data-stu-id="a084d-102">Open and display the contents of an iCalendar file</span></span>

<span data-ttu-id="a084d-103">В этом примере показано, как открывать и отображать содержимое файла iCalendar в зависимости от того, содержит ли этот файл единственную или повторяющуюся встречу, либо он содержит группу встреч.</span><span class="sxs-lookup"><span data-stu-id="a084d-103">This example shows how to open and display the contents of an iCalendar file, depending on whether the file contains a single or recurrent appointment, or the file contains a group of appointments.</span></span>

## <a name="example"></a><span data-ttu-id="a084d-104">Пример</span><span class="sxs-lookup"><span data-stu-id="a084d-104">Example</span></span>

<span data-ttu-id="a084d-p101">В этом примере кода сначала предпринимается попытка использовать метод [OpenSharedItem](https://msdn.microsoft.com/library/bb645399\(v=office.15\)) объекта [NameSpace](https://msdn.microsoft.com/library/bb645857\(v=office.15\)) , чтобы открыть файл iCalendar как файл iCalendar одной встречи. Если эта попытка оказывается успешной, в окне инспектора выводятся данные элемента встречи. Но этот элемент не будет скопирован в хранилище по умолчанию. Если примеру не удается открыть файл как файл iCalendar одной встречи, будет использован метод [OpenSharedFolder](https://msdn.microsoft.com/library/bb610157\(v=office.15\)) объекта **NameSpace** для попытки импортировать содержимое в хранилище по умолчанию как новый календарь. Если импорт оказывается успешным, календарь появляется в окне проводника.</span><span class="sxs-lookup"><span data-stu-id="a084d-p101">This code sample first tries to use the [OpenSharedItem](https://msdn.microsoft.com/library/bb645399\(v=office.15\)) method of the [NameSpace](https://msdn.microsoft.com/library/bb645857\(v=office.15\)) object to open the iCalendar file as a single-appointment iCalendar file. If it succeeds, it will display the appointment item details in an inspector window. However, it will not copy the item to the default store. If the sample cannot open the file as a single-appointment iCalendar file, then it will use the [OpenSharedFolder](https://msdn.microsoft.com/library/bb610157\(v=office.15\)) method of the **NameSpace** object to attempt to import the contents as a new calendar in the default store. If it succeeds in importing, then it will display the calendar in an explorer window.</span></span>

<span data-ttu-id="a084d-110">В этом примере кода используется вспомогательный класс OutlookItem, определенный в статье [Создание вспомогательного класса для доступа к стандартным членам элемента Outlook](how-to-create-a-helper-class-to-access-common-outlook-item-members.md), с помощью которого можно удобно вызвать метод **OutlookItem.Display** для отображения элемента встречи без необходимости выполнять приведение элемента.</span><span class="sxs-lookup"><span data-stu-id="a084d-110">This code sample makes use of the OutlookItem helper class, defined in [Create a Helper Class to Access Common Outlook Item Members](how-to-create-a-helper-class-to-access-common-outlook-item-members.md), to conveniently call the **OutlookItem.Display** method to display the appointment item without having to first cast the item.</span></span>

<span data-ttu-id="a084d-111">Если для тестирования этого примера кода вы используете Visual Studio, сначала добавьте ссылку на компонент библиотеки объектов Microsoft Outlook 15.0 и укажите переменную Outlook при импорте пространства имен **Microsoft.Office.Interop.Outlook**.</span><span class="sxs-lookup"><span data-stu-id="a084d-111">If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the Outlook variable when you import the **Microsoft.Office.Interop.Outlook** namespace.</span></span> <span data-ttu-id="a084d-112">Инструкция **Imports** или **using** не должна идти непосредственно перед функциями в примере кода, но ее нужно добавить перед объявлением общедоступного класса.</span><span class="sxs-lookup"><span data-stu-id="a084d-112">The **Imports** or **using** statement must not occur directly before the functions in the code example but must be added before the public Class declaration.</span></span> <span data-ttu-id="a084d-113">В строках кода ниже показано, как выполнить импорт и назначение на Visual Basic и C\#.</span><span class="sxs-lookup"><span data-stu-id="a084d-113">The following lines of code show how to do the import and assignment in Visual Basic and C\#.</span></span>

```vb
Imports Outlook = Microsoft.Office.Interop.Outlook
```


```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```vb
Private Sub OpenICalendarFile(ByVal fileName As String)
    If String.IsNullOrEmpty(fileName) Then
        Throw New ArgumentException(_
        "Parameter must contain a value.", "exportFileName")
    End If
    If Not File.Exists(fileName) Then
        Throw New FileNotFoundException(fileName)
    End If

    '' First try to open the icalendar file as an appointment 
    '' (not a calendar folder).
    Dim item As Object = Nothing
    Try
         item = Application.Session.OpenSharedItem(fileName)
    Catch
    End Try

    If Not item Is Nothing Then
        '' Display the item
        Dim olItem As OutlookItem = New OutlookItem(item)
        olItem.Display()
        Return
    End If

    '' If unsucessful in opening it as an item, 
    '' try opening it as a folder
    Dim importedFolder As Outlook.Folder = Nothing
    Try
        importedFolder = TryCast( _
            Application.Session.OpenSharedFolder(fileName), _
            Outlook.Folder)
    Catch
    End Try

    '' If sucessful, open the folder in a new explorer window
    If Not importedFolder Is Nothing Then
        Dim explorer As Outlook.Explorer = _
            Application.Explorers.Add( _
            importedFolder, _
            Outlook.OlFolderDisplayMode.olFolderDisplayNormal)
        explorer.Display()
    End If
End Sub
```


```csharp
private void OpenICalendarFile(string fileName)
{
    if (string.IsNullOrEmpty(fileName))
        throw new ArgumentException("exportFileName", 
        "Parameter must contain a value.");
    if (!File.Exists(fileName))
        throw new FileNotFoundException(fileName);

    // First try to open the icalendar file as an appointment 
    // (not a calendar folder).
    object item = null;
    try
    {
        item = Application.Session.OpenSharedItem(fileName);
    }
    catch
    { }

    if (item != null)
    {
         // Display the item
         OutlookItem olItem = new OutlookItem(item);
         olItem.Display();
         return;
    }

    // If unsucessful in opening it as an item, 
    // try opening it as a folder
    Outlook.Folder importedFolder = null;
    try
    {
        importedFolder = Application.Session.OpenSharedFolder(
            fileName, Type.Missing, Type.Missing, Type.Missing) 
            as Outlook.Folder;
    }
    catch
    { }

    // If sucessful, open the folder in a new explorer window
    if (importedFolder != null)
    {
        Outlook.Explorer explorer =
            Application.Explorers.Add(importedFolder, 
            Outlook.OlFolderDisplayMode.olFolderDisplayNormal);
        explorer.Display();
    }
}
```

## <a name="see-also"></a><span data-ttu-id="a084d-114">См. также</span><span class="sxs-lookup"><span data-stu-id="a084d-114">See also</span></span>

- [<span data-ttu-id="a084d-115">Calendar</span><span class="sxs-lookup"><span data-stu-id="a084d-115">Calendar</span></span>](calendar.md)


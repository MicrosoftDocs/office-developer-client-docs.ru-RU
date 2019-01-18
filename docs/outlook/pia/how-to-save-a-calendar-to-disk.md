---
title: Сохранение календаря на диск
TOCTitle: Save a calendar to disk
ms:assetid: f1b57bd0-c972-4b86-8870-f26290f28050
ms:mtpsurl: https://msdn.microsoft.com/library/Bb647583(v=office.15)
ms:contentKeyID: 55119827
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: b07df7458f80b751077358ac3c53ad41032d1080
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28712507"
---
# <a name="save-a-calendar-to-disk"></a><span data-ttu-id="4bc23-102">Сохранение календаря на диск</span><span class="sxs-lookup"><span data-stu-id="4bc23-102">Save a calendar to disk</span></span>

<span data-ttu-id="4bc23-103">В этом примере показано, как сохранить весь календарь на диск в файле формата iCalendar (ICS-файле).</span><span class="sxs-lookup"><span data-stu-id="4bc23-103">This example shows how to save an entire calendar to disk in the iCalendar (.ics) file format.</span></span>

## <a name="example"></a><span data-ttu-id="4bc23-104">Пример</span><span class="sxs-lookup"><span data-stu-id="4bc23-104">Example</span></span>

<span data-ttu-id="4bc23-p101">В данном образце кода задействован объект [CalendarSharing](https://msdn.microsoft.com/library/bb624344\(v=office.15\)) , поддерживающий сохранение на диск всего календаря или ряда встреч из него. ICS-файл автоматически оптимизируется в Outlook, чтобы повторяющиеся события не сохранялись в качестве отдельных встреч в ICS-файле. В зависимости от размера сохраняемого календаря его запись на диск может потребовать значительного времени. Во время сохранения календаря окно Outlook не реагирует на действия пользователя.</span><span class="sxs-lookup"><span data-stu-id="4bc23-p101">This code sample uses the [CalendarSharing](https://msdn.microsoft.com/library/bb624344\(v=office.15\)) object that supports saving a whole calendar or a range of appointments from the calendar to disk. Outlook automatically optimizes an .ics file so that recurring appointments are not saved as individual appointments in the .ics file. Depending on the size of the calendar being saved, saving a calendar to disk can take a significant amount of time. While saving the calendar, the Outlook window appears unresponsive to the user.</span></span>

<span data-ttu-id="4bc23-p102">В этом образце кода сначала вызывается [GetCalendarExporter](https://msdn.microsoft.com/library/bb610021\(v=office.15\)) по отношению к папке "Календарь" по умолчанию для получения объекта **CalendarSharing**. Затем задаются свойства объекта **CalendarSharing**, указывающие критерии для экспорта (например, нужно ли сохранять календарь целиком, включая сведения о встречах с отметкой "частная").</span><span class="sxs-lookup"><span data-stu-id="4bc23-p102">The code sample first calls [GetCalendarExporter](https://msdn.microsoft.com/library/bb610021\(v=office.15\)) on the default Calendar folder to obtain a **CalendarSharing** object. Then it sets properties of the **CalendarSharing** object to specify criteria for the export, such as whether to save the entire calendar and include details of appointments that are marked "private".</span></span>

<span data-ttu-id="4bc23-111">Чтобы сохранить данные календаря в ICS-файле, пример кода вызывает метод [SaveAsICal](https://msdn.microsoft.com/library/bb644844\(v=office.15\)) объекта **CalendarSharing**.</span><span class="sxs-lookup"><span data-stu-id="4bc23-111">To save the calendar information in .ics file format, the code sample calls the [SaveAsICal](https://msdn.microsoft.com/library/bb644844\(v=office.15\)) method of the **CalendarSharing** object.</span></span>

<span data-ttu-id="4bc23-112">Если вы используете Visual Studio для тестирования этого примера кода, сначала добавьте ссылку на компонент библиотеки объектов Microsoft Outlook 15.0 и задайте переменную Outlook при импорте пространства имен **Microsoft.Office.Interop.Outlook**.</span><span class="sxs-lookup"><span data-stu-id="4bc23-112">If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the Outlook variable when you import the **Microsoft.Office.Interop.Outlook** namespace.</span></span> <span data-ttu-id="4bc23-113">Инструкция **Imports** или **using** не должна идти непосредственно перед функциями в примере кода, но ее нужно добавить перед объявлением общедоступного класса.</span><span class="sxs-lookup"><span data-stu-id="4bc23-113">The **Imports** or **using** statement must not occur directly before the functions in the code example but must be added before the public Class declaration.</span></span> <span data-ttu-id="4bc23-114">В строках кода ниже показано, как выполнить импорт и назначение на Visual Basic и C\#.</span><span class="sxs-lookup"><span data-stu-id="4bc23-114">The following lines of code show how to do the import and assignment in Visual Basic and C\#.</span></span>

```vb
Imports Outlook = Microsoft.Office.Interop.Outlook
```


```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```vb
Private Sub SaveCalendarToDisk(ByVal calendarFileName As String)
    If String.IsNullOrEmpty(calendarFileName) Then
        Throw New ArgumentException( _
        "Parameter must contain a value.", "calendarFileName")
    End If

    Dim calendar As Outlook.Folder = TryCast( _
        Application.Session.GetDefaultFolder(_
        Outlook.OlDefaultFolders.olFolderCalendar), Outlook.Folder)
    Dim exporter As Outlook.CalendarSharing = _
        calendar.GetCalendarExporter()

    '' Set the properties for the export
    exporter.CalendarDetail = Outlook.OlCalendarDetail.olFullDetails
    exporter.IncludeAttachments = True
    exporter.IncludePrivateDetails = True
    exporter.RestrictToWorkingHours = False
    exporter.IncludeWholeCalendar = True

    '' Save the calendar to disk
    exporter.SaveAsICal(calendarFileName)
End Sub
```


```csharp
private void SaveCalendarToDisk(string calendarFileName)
{
    if (string.IsNullOrEmpty(calendarFileName))
        throw new ArgumentException("calendarFileName", 
        "Parameter must contain a value.");

    Outlook.Folder calendar = Application.Session.GetDefaultFolder(
        Outlook.OlDefaultFolders.olFolderCalendar) as Outlook.Folder;
    Outlook.CalendarSharing exporter = calendar.GetCalendarExporter();

    // Set the properties for the export
    exporter.CalendarDetail = Outlook.OlCalendarDetail.olFullDetails;
    exporter.IncludeAttachments = true;
    exporter.IncludePrivateDetails = true;
    exporter.RestrictToWorkingHours = false;
    exporter.IncludeWholeCalendar = true;

    // Save the calendar to disk
    exporter.SaveAsICal(calendarFileName);
}
```

## <a name="see-also"></a><span data-ttu-id="4bc23-115">См. также</span><span class="sxs-lookup"><span data-stu-id="4bc23-115">See also</span></span>

- [<span data-ttu-id="4bc23-116">Календарь</span><span class="sxs-lookup"><span data-stu-id="4bc23-116">Calendar</span></span>](calendar.md)


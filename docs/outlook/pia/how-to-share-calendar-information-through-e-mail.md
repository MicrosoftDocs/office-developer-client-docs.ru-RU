---
title: Отправка сведений календаря по электронной почте
TOCTitle: Share calendar information through email
ms:assetid: 3382010c-0a16-4dca-a99e-669e9178354e
ms:mtpsurl: https://msdn.microsoft.com/library/Bb609881(v=office.15)
ms:contentKeyID: 55119817
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 48b299ad4d3afe5c0c9aaa05f5d8af3b92bf655d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32332083"
---
# <a name="share-calendar-information-through-email"></a><span data-ttu-id="43b54-102">Отправка сведений календаря по электронной почте</span><span class="sxs-lookup"><span data-stu-id="43b54-102">Share calendar information through email</span></span>

<span data-ttu-id="43b54-103">В этом примере показывается, как обмениваться сведениями из календаря по электронной почте в формате iCalendar.</span><span class="sxs-lookup"><span data-stu-id="43b54-103">This example shows how to share information from a calendar by email in the iCalendar format.</span></span>

## <a name="example"></a><span data-ttu-id="43b54-104">Пример</span><span class="sxs-lookup"><span data-stu-id="43b54-104">Example</span></span>

<span data-ttu-id="43b54-p101">Формат iCalendar позволяет отправлять элементы другим клиентам Outlook или других почтовых программ, используя стандартные форматы и протоколы почты Интернета. В примере кода используется объект [CalendarSharing](https://msdn.microsoft.com/library/bb624344\(v=office.15\)) , поддерживающий экспорт данных из папки календаря в формат iCalendar.</span><span class="sxs-lookup"><span data-stu-id="43b54-p101">The iCalendar format allows you to send items to other Outlook or non-Outlook clients via standard Internet mail formats and protocols. The code sample uses the [CalendarSharing](https://msdn.microsoft.com/library/bb624344\(v=office.15\)) object that supports exporting information from a calendar folder to the iCalendar format.</span></span>

<span data-ttu-id="43b54-p102">Сначала в коде для папки календаря по умолчанию вызывается метод [GetCalendarExporter](https://msdn.microsoft.com/library/bb610021\(v=office.15\)) , чтобы получить объект **CalendarSharing**. Затем задаются свойства объекта **CalendarSharing**, чтобы определить условия экспорта, например диапазон дат для данных календаря, необходимость включения вложений и данных встреч, помеченных как "закрытые".</span><span class="sxs-lookup"><span data-stu-id="43b54-p102">The code sample first calls [GetCalendarExporter](https://msdn.microsoft.com/library/bb610021\(v=office.15\)) on the default Calendar folder to obtain a **CalendarSharing** object. Then it sets properties of the **CalendarSharing** object to specify criteria for the export, such as the date range of calendar information, whether to include attachments, and details of appointments that are marked "private."</span></span>

<span data-ttu-id="43b54-109">Чтобы отправить сведения из календаря по электронной почте, в коде примера вызывается метод [ForwardAsICal](https://msdn.microsoft.com/library/bb652866\(v=office.15\)) объекта **CalendarSharing**.</span><span class="sxs-lookup"><span data-stu-id="43b54-109">To send the calendar information by email, the code sample calls the [ForwardAsICal](https://msdn.microsoft.com/library/bb652866\(v=office.15\)) method of the **CalendarSharing** object.</span></span>

<span data-ttu-id="43b54-110">Если для тестирования этого примера кода вы используете Visual Studio, сначала добавьте ссылку на компонент библиотеки объектов Microsoft Outlook 15.0 и укажите переменную Outlook при импорте пространства имен **Microsoft.Office.Interop.Outlook**.</span><span class="sxs-lookup"><span data-stu-id="43b54-110">If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the Outlook variable when you import the **Microsoft.Office.Interop.Outlook** namespace.</span></span> <span data-ttu-id="43b54-111">Инструкция **Imports** или **using** не должна идти непосредственно перед функциями в примере кода, но ее нужно добавить перед объявлением общедоступного класса.</span><span class="sxs-lookup"><span data-stu-id="43b54-111">The **Imports** or **using** statement must not occur directly before the functions in the code example but must be added before the public Class declaration.</span></span> <span data-ttu-id="43b54-112">В строках кода ниже показано, как выполнить импорт и назначение на Visual Basic и C\#.</span><span class="sxs-lookup"><span data-stu-id="43b54-112">The following lines of code show how to do the import and assignment in Visual Basic and C\#.</span></span>

```vb
Imports Outlook = Microsoft.Office.Interop.Outlook
```

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```

```vb
Private Sub SendNextWeekToAddress(ByVal sendToAddresses As String)
    If String.IsNullOrEmpty(sendToAddresses) Then
        Throw New ArgumentException( _
            "Parameter must contain a value.", "sendToAddress")
    End If

    Dim calendar As Outlook.Folder = TryCast( _
        Application.Session.GetDefaultFolder( _
        Outlook.OlDefaultFolders.olFolderCalendar), Outlook.Folder)
    Dim exporter As Outlook.CalendarSharing = calendar.GetCalendarExporter()

    '' Set the properties for the export
    exporter.CalendarDetail = Outlook.OlCalendarDetail.olFullDetails
    exporter.IncludeAttachments = True
    exporter.IncludePrivateDetails = False
    exporter.RestrictToWorkingHours = False
    exporter.StartDate = DateTime.Today.Date
    exporter.EndDate = DateTime.Today.Date.AddDays(7)

    '' Create a new mail item
    Dim calendarMail As Outlook.MailItem = exporter.ForwardAsICal _
        (Outlook.OlCalendarMailFormat. _
        olCalendarMailFormatDailySchedule)
    calendarMail.To = sendToAddresses
    calendarMail.Send()
    calendarMail.Display()
End Sub
```

```csharp
private void SendNextWeekToAddress(string sendToAddresses)
{
    if (string.IsNullOrEmpty(sendToAddresses))
        throw new ArgumentException(
        "sendToAddress","Parameter must contain a value.");
    Outlook.Folder calendar = 
        Application.Session.GetDefaultFolder(
        Outlook.OlDefaultFolders.olFolderCalendar)
        as Outlook.Folder;
    Outlook.CalendarSharing exporter = calendar.GetCalendarExporter();

    // Set the properties for the export
    exporter.CalendarDetail = Outlook.OlCalendarDetail.olFullDetails;
    exporter.IncludeAttachments = true;
    exporter.IncludePrivateDetails = false;
    exporter.RestrictToWorkingHours = false;
    exporter.StartDate = DateTime.Today.Date;
    exporter.EndDate = DateTime.Today.Date.AddDays(7);

    // Create a new mail item
    Outlook.MailItem calendarMail = 
        exporter.ForwardAsICal(Outlook.OlCalendarMailFormat.
        olCalendarMailFormatDailySchedule);
    calendarMail.To = sendToAddresses;
    ((Outlook.MailItemClass)calendarMail).Send();
    ((Outlook.MailItemClass)calendarMail).Display(Type.Missing);
}
```

## <a name="see-also"></a><span data-ttu-id="43b54-113">См. также</span><span class="sxs-lookup"><span data-stu-id="43b54-113">See also</span></span>

- [<span data-ttu-id="43b54-114">Calendar</span><span class="sxs-lookup"><span data-stu-id="43b54-114">Calendar</span></span>](calendar.md)


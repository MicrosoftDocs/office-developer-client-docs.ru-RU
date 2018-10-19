---
title: Сохранение календаря на диск
TOCTitle: Save a calendar to disk
ms:assetid: f1b57bd0-c972-4b86-8870-f26290f28050
ms:mtpsurl: https://msdn.microsoft.com/library/Bb647583(v=office.15)
ms:contentKeyID: 55119827
ms.date: 07/24/2014
mtps_version: v=office.15
ms.openlocfilehash: 2f9a71d2743896ca6257e30efc7260ed11086ca5
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25405646"
---
# <a name="save-a-calendar-to-disk"></a>Сохранение календаря на диск

В этом примере показано, как сохранить весь календарь на диск в файле формата iCalendar (ICS-файле).

## <a name="example"></a>Пример

В данном образце кода задействован объект [CalendarSharing](https://msdn.microsoft.com/library/bb624344\(v=office.15\)) , поддерживающий сохранение на диск всего календаря или ряда встреч из него. ICS-файл автоматически оптимизируется в Outlook, чтобы повторяющиеся события не сохранялись в качестве отдельных встреч в ICS-файле. В зависимости от размера сохраняемого календаря его запись на диск может потребовать значительного времени. Во время сохранения календаря окно Outlook не реагирует на действия пользователя.

В этом образце кода сначала вызывается [GetCalendarExporter](https://msdn.microsoft.com/library/bb610021\(v=office.15\)) по отношению к папке "Календарь" по умолчанию для получения объекта **CalendarSharing**. Затем задаются свойства объекта **CalendarSharing**, указывающие критерии для экспорта (например, нужно ли сохранять календарь целиком, включая сведения о встречах с отметкой "частная").

Чтобы сохранить данные календаря в ICS-файле, пример кода вызывает метод [SaveAsICal](https://msdn.microsoft.com/library/bb644844\(v=office.15\)) объекта **CalendarSharing**.

Если вы используете Visual Studio для тестирования этого примера кода, сначала добавьте ссылку на компонент библиотеки объектов Microsoft Outlook 15.0 и задайте переменную Outlook при импорте пространства имен **Microsoft.Office.Interop.Outlook**. Инструкция **Imports** или **using** не должна идти непосредственно перед функциями в примере кода, но ее нужно добавить перед объявлением общедоступного класса. В строках кода ниже показано, как выполнить импорт и назначение на Visual Basic и C\#.

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

## <a name="see-also"></a>См. также

- [Календарь](calendar.md)


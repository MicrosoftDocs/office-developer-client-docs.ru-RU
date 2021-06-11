---
title: Поиск и получение встреч в диапазоне времени
TOCTitle: Search and obtain appointments in a time range
ms:assetid: ce5205ad-6967-4f21-8a9d-503b731dbd40
ms:mtpsurl: https://msdn.microsoft.com/library/Gg619398(v=office.15)
ms:contentKeyID: 55119927
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 9088da5f2deb4b3d4ccb1c2bc5409e0ff280ed24
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316094"
---
# <a name="search-and-obtain-appointments-in-a-time-range"></a>Поиск и получение встреч в диапазоне времени

Этот пример возвращает встречи в определенном диапазоне времени в календаре по умолчанию Microsoft Outlook.

## <a name="example"></a>Пример

Этот пример кода содержит два метода: DemoAppointmentsInRange и GetAppointmentsInRange. DemoAppointmentsInRange получает календарь по умолчанию для текущего профиля Outlook, вошедшего в систему, устанавливает диапазон дат на 5 дней с 12:00 сегодняшнего дня, вызывает GetAppointmentsInRange для получения встреч, которые находятся в этом диапазоне времени, и отображает тему и время начала для каждой из возвращенных встреч.

GetAppointmentsInRange принимает папку Outlook и значения **DateTime** начала и окончания диапазона времени в качестве входных параметров. В этом методе используется метод [Restrict(String)](https://msdn.microsoft.com/library/bb612531\(v=office.15\)) и фильтр строк в формате Jet, который возвращает встречи, начинающиеся и оканчивающиеся в указанном диапазоне времени. Принимая \[Start\] и \[End\] в качестве времени начала и окончания встречи, а startTime и endTime в качестве начала и окончания указанного диапазона времени, метод GetAppointmentsInRange настраивает фильтр для поиска встреч с параметрами `[Start]>=startTime` и `[End]<=endTime`. Ниже показан фильтр Jet в C\#.

```csharp
string filter = "[Start] >= '"
    + startTime.ToString("g")
    + "' AND [End] <= '"
    + endTime.ToString("g") + "'";
```

До вызова метода **Items.Restrict** для поиска встреч GetAppointmentsInRange выполняет другие два действия, чтобы включить повторяющиеся встречи, которые происходят в указанном диапазоне времени:

- Задание свойства [IncludeRecurrences](https://msdn.microsoft.com/library/bb646522\(v=office.15\)) коллекции [Items](https://msdn.microsoft.com/library/bb645287\(v=office.15\)).

- Сортировка элементов встреч в заданной папке календаря с помощью свойства [Start](https://msdn.microsoft.com/library/bb647263\(v=office.15\)).

Либо, если вас также интересуют встречи, частично или полностью перекрывающие указанный диапазон времени, можно задать разные фильтры, чтобы получить дополнительные типы встреч (как показано на рисунке 1):

- Встречи, начинающиеся и оканчивающиеся в указанном диапазоне времени (например, встреча A):<br/><br/>`[Start]>=startTime and [End]<=endTime`

- Встречи, начинающиеся до указанного диапазона времени, но заканчивающиеся в нем (например, встреча B):<br/><br/>`[Start]<startTime and [End]<=endTime`

- Встречи, начинающиеся в указанном диапазоне времени, но заканчивающиеся после него (например, встреча C):<br/><br/>`[Start]>=startTime and [End]>endTime`

- Встречи, начинающиеся до указанного диапазона времени и заканчивающиеся после него (например, встреча D):<br/><br/>`[Start]<startTime and [End]>endTime`

**Рис. 1. Типы встреч, которые происходят в определенном диапазоне времени или перекрывают его**

![Типы встреч, которые происходят в определенном диапазоне времени или перекрывают его](media/pia-appointment-starttime-endtime.gif)
 

Поскольку в любом диапазоне времени `startTime<=endTime`, в фильтр с параметрами `[Start]<=endTime` и `[End]>=startTime` попадут указанные выше типы встреч из этого диапазона времени.

В C\# фильтр Jet можно представить следующим образом.

```csharp
string filter = "[Start] <= '&quot;
    + endTime.ToString(&quot;g")
    + "' AND [End] >= '"
    + startTime.ToString("g") + "'";
```

Ниже показан полный пример. Если для тестирования этого примера кода вы используете Visual Studio, сначала добавьте ссылку на компонент библиотеки объектов Microsoft Outlook 15.0 и укажите переменную Outlook при импорте пространства имен **Microsoft.Office.Interop.Outlook**. Инструкция **Imports** или **using** не должна идти непосредственно перед функциями в примере кода, но ее нужно добавить перед объявлением общедоступного класса. В строках кода ниже показано, как выполнить импорт и назначение на Visual Basic и C\#.

```vb
Imports Outlook = Microsoft.Office.Interop.Outlook
```


```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```csharp
private void DemoAppointmentsInRange()
{
    Outlook.Folder calFolder =
        Application.Session.GetDefaultFolder(
        Outlook.OlDefaultFolders.olFolderCalendar)
        as Outlook.Folder;
    DateTime start = DateTime.Now;
    DateTime end = start.AddDays(5);
    Outlook.Items rangeAppts = GetAppointmentsInRange(calFolder, start, end);
    if (rangeAppts != null)
    {
        foreach (Outlook.AppointmentItem appt in rangeAppts)
        {
            Debug.WriteLine("Subject: " + appt.Subject 
                + " Start: " + appt.Start.ToString("g"));
        }
    }
}

/// <summary>
/// Get recurring appointments in date range.
/// </summary>
/// <param name="folder"></param>
/// <param name="startTime"></param>
/// <param name="endTime"></param>
/// <returns>Outlook.Items</returns>
private Outlook.Items GetAppointmentsInRange(
    Outlook.Folder folder, DateTime startTime, DateTime endTime)
{
    string filter = "[Start] >= '"
        + startTime.ToString("g")
        + "' AND [End] <= '"
        + endTime.ToString("g") + "'";
    Debug.WriteLine(filter);
    try
    {
        Outlook.Items calItems = folder.Items;
        calItems.IncludeRecurrences = true;
        calItems.Sort("[Start]", Type.Missing);
        Outlook.Items restrictItems = calItems.Restrict(filter);
        if (restrictItems.Count > 0)
        {
            return restrictItems;
        }
        else
        {
            return null;
        }
    }
    catch { return null; }
}
```

## <a name="see-also"></a>См. также

- [Поиск и фильтрация](search-and-filter.md)


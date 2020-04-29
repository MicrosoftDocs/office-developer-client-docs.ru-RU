---
title: Создание встречи, начинающейся по тихоокеанскому времени и заканчивающейся по восточному поясному времени
TOCTitle: Create an appointment that starts in the Pacific Time Zone and ends in the Eastern Time Zone
ms:assetid: ba19532b-df31-4384-8816-e64e6eecbe53
ms:mtpsurl: https://msdn.microsoft.com/library/Bb623388(v=office.15)
ms:contentKeyID: 55119808
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: e9a1b9d5f65d8683c08821d4cf0851f599f32030
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32349457"
---
# <a name="create-an-appointment-that-starts-in-the-pacific-time-zone-and-ends-in-the-eastern-time-zone"></a>Создание встречи, начинающейся по тихоокеанскому времени и заканчивающейся по восточному поясному времени

Иногда встреча может растянуться на такой срок, в течение которого пользователь может сменить часовой пояс, уехав из часового пояса, выбранного в начале встречи. В этом примере создается встреча, которая начинается по тихоокеанскому времени (UTC-8) и заканчивается по восточному поясному времени (UTC-5).

## <a name="example"></a>Пример

В этом примере кода используется объект [timezones](https://msdn.microsoft.com/library/bb611081\(v=office.15\)) , который представляет все часовые пояса, распознаваемые в Microsoft Windows. Он также использует объект [TimeZone](https://msdn.microsoft.com/library/bb646259\(v=office.15\)) для задания или получения свойства [StartTimeZone](https://msdn.microsoft.com/library/bb623657\(v=office.15\)) и свойства [EndTimeZone](https://msdn.microsoft.com/library/bb612198\(v=office.15\)) объекта [AppointmentItem](https://msdn.microsoft.com/library/bb645611\(v=office.15\)) .

Все даты в Outlook отображаются с использованием местного времени, которое выражено в текущем часовом поясе пользователя, контролируемом параметрами пользователя в панели управления Windows. Outlook также задает или получает свойства, такие как [Start](https://msdn.microsoft.com/library/bb647263\(v=office.15\)) и [End](https://msdn.microsoft.com/library/bb623715\(v=office.15\)), по местному времени. Однако значения даты и времени сохраняются в Outlook в формате UTC, а не в формате местного времени. Если вы изучите внутреннее значение встречи. Начните с использования объекта [PropertyAccessor](https://msdn.microsoft.com/library/bb646034\(v=office.15\)) , вы обнаружите внутреннее значение даты и времени, равное локальному значению даты и времени, преобразованному в эквивалентное значение даты и времени в формате UTC.

Outlook использует сведения о часовом поясе, чтобы сопоставить встречу с правильным временем в формате UTC, когда он сохраняет встречу, и в правильное местное время при отображении элемента в календаре. Изменение StartTimeZone влияет на значение свойства встреча. Start, которое всегда выражается в местном часовом поясе, представленном свойством [CurrentTimeZone](https://msdn.microsoft.com/library/bb612024\(v=office.15\)) объекта, возвращаемого с помощью [часовых поясов](https://msdn.microsoft.com/library/bb645170\(v=office.15\)). Аналогично, изменение EndTimeZone влияет на значение свойства встреча. end, которое всегда выражается в местном часовом поясе, представленном свойством CurrentTimeZone объекта, возвращаемого приложением. TimeZones.

Конкретное значение TimeZone можно извлечь из объекта TimeZones с помощью независимого от региональных стандартов ключа TimeZone в реестре Windows. Независимые от региональных стандартов ключи TimeZone перечислены в следующем разделе: `HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Windows NT\CurrentVersion\TimeZones`.

Если для тестирования этого примера кода вы используете Visual Studio, сначала добавьте ссылку на компонент библиотеки объектов Microsoft Outlook 15.0 и укажите переменную Outlook при импорте пространства имен **Microsoft.Office.Interop.Outlook**. Инструкция **Imports** или **using** не должна идти непосредственно перед функциями в примере кода, но ее нужно добавить перед объявлением общедоступного класса. В строках кода ниже показано, как выполнить импорт и назначение на Visual Basic и C\#.


```vb
Imports Outlook = Microsoft.Office.Interop.Outlook
```



```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```



```vb
Private Sub TimeZoneExample()
    Dim appt As Outlook.AppointmentItem = _
        CType(Application.CreateItem( _
        Outlook.OlItemType.olAppointmentItem), Outlook.AppointmentItem)
    Dim tzs As Outlook.TimeZones = Application.TimeZones
    ' Obtain timezone using indexer and locale-independent key
    Dim tzEastern As Outlook.TimeZone = tzs("Eastern Standard Time")
    Dim tzPacific As Outlook.TimeZone = tzs("Pacific Standard Time")
    appt.Subject = "SEA - JFK Flight"
    appt.Start = DateTime.Parse("8/9/2006 8:00 AM")
    appt.StartTimeZone = tzPacific
    appt.End = DateTime.Parse("8/9/2006 5:30 PM")
    appt.EndTimeZone = tzEastern
    appt.Display(False)
End Sub
```



```csharp
private void TimeZoneExample()
{
    Outlook.AppointmentItem appt = Application.CreateItem(
        Outlook.OlItemType.olAppointmentItem)
        as Outlook.AppointmentItem;
    Outlook.TimeZones tzs = Application.TimeZones;
    // Obtain timezone using indexer and locale-independent key
    Outlook.TimeZone tzEastern = tzs["Eastern Standard Time"];
    Outlook.TimeZone tzPacific = tzs["Pacific Standard Time"];
    appt.Subject = "SEA - JFK Flight";
    appt.Start = DateTime.Parse("8/9/2006 8:00 AM");
    appt.StartTimeZone = tzPacific;
    appt.End = DateTime.Parse("8/9/2006 5:30 PM");
    appt.EndTimeZone = tzEastern; 
    appt.Display(false);
}
```

## <a name="see-also"></a>См. также

- [Встречи](appointments.md)


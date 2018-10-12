---
title: Создание встречи, начинающейся по тихоокеанскому времени и заканчивающейся по восточному поясному времени
TOCTitle: Create an appointment that starts in the Pacific Time Zone and ends in the Eastern Time Zone
ms:assetid: ba19532b-df31-4384-8816-e64e6eecbe53
ms:mtpsurl: https://msdn.microsoft.com/library/Bb623388(v=office.15)
ms:contentKeyID: 55119808
ms.date: 07/24/2014
mtps_version: v=office.15
ms.openlocfilehash: 9cb21bddb425adb54082dbe21b32653e1fe3ca75
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25406080"
---
# <a name="create-an-appointment-that-starts-in-the-pacific-time-zone-and-ends-in-the-eastern-time-zone"></a>Создание встречи, начинающейся по тихоокеанскому времени и заканчивающейся по восточному поясному времени

Иногда встреча может растянуться на такой срок, в течение которого пользователь может сменить часовой пояс, уехав из часового пояса, выбранного в начале встречи. В этом примере создается встреча, которая начинается по тихоокеанскому времени (UTC-8) и заканчивается по восточному поясному времени (UTC-5).

## <a name="example"></a>Пример

В этом примере кода применяется объект [TimeZones](https://msdn.microsoft.com/library/bb611081\(v=office.15\)), который представляет собой все часовые пояса, распознаваемые в Microsoft Windows. Здесь также применяется объект [TimeZone](https://msdn.microsoft.com/library/bb646259\(v=office.15\)) , используемый для задания или получения свойства [StartTimeZone](https://msdn.microsoft.com/library/bb623657\(v=office.15\)) и свойства [EndTimeZone](https://msdn.microsoft.com/library/bb612198\(v=office.15\)) объекта [AppointmentItem](https://msdn.microsoft.com/library/bb645611\(v=office.15\)) .

Все даты в Outlook отображаются с использованием местного времени, которое выражено в текущем часовом поясе пользователя, контролируемом параметрами пользователя в панели управления Windows. При задании или получении свойств в Outlook (например, [Start](https://msdn.microsoft.com/library/bb647263\(v=office.15\)) и [End](https://msdn.microsoft.com/library/bb623715\(v=office.15\))) они также выражаются в формате местного времени. Однако Outlook сохраняет значения даты и времени в формате UTC, а не в формате местного времени. При изучении внутреннего значения Appointment.Start при помощи объекта [PropertyAccessor](https://msdn.microsoft.com/library/bb646034\(v=office.15\)) выясняется, что внутреннее значение даты и времени равняется значению местной даты и времени, преобразованному в равноценное значение в формате UTC.

При сохранении встречи Outlook использует сведения о часовом поясе, чтобы сопоставить встречу с соответствующим временем в формате UTC, а при отображении элемента в календаре — с соответствующим местным временем. Изменение элемента StartTimeZone влияет на значение Appointment.Start, которое всегда выражается в местном часовом поясе, представленном свойством [CurrentTimeZone](https://msdn.microsoft.com/library/bb612024\(v=office.15\)) объекта, возвращенного с помощью [TimeZones](https://msdn.microsoft.com/library/bb645170\(v=office.15\)). Аналогичным образом изменение элемента EndTimeZone влияет на значение Appointment.End, которое всегда выражается в местном часовом поясе, представленном свойством CurrentTimeZone объекта, возвращенного с помощью Application.TimeZones.

Вы можете получить определенный объект TimeZone из объекта TimeZones с помощью независимого от региональных стандартов ключа для TimeZone в реестре Windows. Независимые от региональных стандартов ключи TimeZone перечислены в следующем разделе: `HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Windows NT\CurrentVersion\TimeZones`.

Если для тестирования этого примера кода вы используете Visual Studio, сначала добавьте ссылку на компонент библиотеки объектов Microsoft Outlook 15.0 и укажите переменную Outlook при импорте пространства имен **Microsoft.Office.Interop.Outlook**. Не следует использовать инструкции **Imports** и **using** непосредственно перед функциями в примере кода, но их необходимо добавить перед объявлением общедоступного класса. В следующих строках кода показано, как выполнить импорт и назначение в Visual Basic и C\#.


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


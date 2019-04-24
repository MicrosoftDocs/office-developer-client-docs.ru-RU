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
# <a name="create-an-appointment-that-starts-in-the-pacific-time-zone-and-ends-in-the-eastern-time-zone"></a><span data-ttu-id="cee64-102">Создание встречи, начинающейся по тихоокеанскому времени и заканчивающейся по восточному поясному времени</span><span class="sxs-lookup"><span data-stu-id="cee64-102">Create an appointment that starts in the Pacific Time Zone and ends in the Eastern Time Zone</span></span>

<span data-ttu-id="cee64-p101">Иногда встреча может растянуться на такой срок, в течение которого пользователь может сменить часовой пояс, уехав из часового пояса, выбранного в начале встречи. В этом примере создается встреча, которая начинается по тихоокеанскому времени (UTC-8) и заканчивается по восточному поясному времени (UTC-5).</span><span class="sxs-lookup"><span data-stu-id="cee64-p101">Occasionally, an appointment may span over a period of time during which the user may have traveled to a different time zone than when the appointment starts. This example creates an appointment that begins in the Pacific Time Zone (UTC-8) and ends in the Eastern Time Zone (UTC-5).</span></span>

## <a name="example"></a><span data-ttu-id="cee64-105">Пример</span><span class="sxs-lookup"><span data-stu-id="cee64-105">Example</span></span>

<span data-ttu-id="cee64-106">В этом примере кода используется [](https://msdn.microsoft.com/library/bb611081\(v=office.15\)) объект timezones, который представляет все часовые пояса, распознаваемые в Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="cee64-106">This code sample uses the [TimeZones](https://msdn.microsoft.com/library/bb611081\(v=office.15\)) object that represents all the time zones recognized in Microsoft Windows.</span></span> <span data-ttu-id="cee64-107">Он также использует объект [TimeZone](https://msdn.microsoft.com/library/bb646259\(v=office.15\)) для задания или получения свойства [StartTimeZone](https://msdn.microsoft.com/library/bb623657\(v=office.15\)) и свойства [EndTimeZone](https://msdn.microsoft.com/library/bb612198\(v=office.15\)) объекта [AppointmentItem](https://msdn.microsoft.com/library/bb645611\(v=office.15\)) .</span><span class="sxs-lookup"><span data-stu-id="cee64-107">It also uses the [TimeZone](https://msdn.microsoft.com/library/bb646259\(v=office.15\)) object to set or get the [StartTimeZone](https://msdn.microsoft.com/library/bb623657\(v=office.15\)) property and the [EndTimeZone](https://msdn.microsoft.com/library/bb612198\(v=office.15\)) property on the [AppointmentItem](https://msdn.microsoft.com/library/bb645611\(v=office.15\)) object.</span></span>

<span data-ttu-id="cee64-108">Все даты в Outlook отображаются с использованием местного времени, которое выражено в текущем часовом поясе пользователя, контролируемом параметрами пользователя в панели управления Windows.</span><span class="sxs-lookup"><span data-stu-id="cee64-108">Outlook displays all dates in local time, which is expressed in the user's current time zone, controlled by the user's settings in the Windows Control Panel.</span></span> <span data-ttu-id="cee64-109">Outlook также задает или получает свойства, такие как [Start](https://msdn.microsoft.com/library/bb647263\(v=office.15\)) и [End](https://msdn.microsoft.com/library/bb623715\(v=office.15\)), по местному времени.</span><span class="sxs-lookup"><span data-stu-id="cee64-109">Outlook also sets or gets properties, such as [Start](https://msdn.microsoft.com/library/bb647263\(v=office.15\)) and [End](https://msdn.microsoft.com/library/bb623715\(v=office.15\)), in local time.</span></span> <span data-ttu-id="cee64-110">Однако значения даты и времени сохраняются в Outlook в формате UTC, а не в формате местного времени.</span><span class="sxs-lookup"><span data-stu-id="cee64-110">However, Outlook stores date and time values as Coordinated Universal Time (UTC) rather than local time.</span></span> <span data-ttu-id="cee64-111">Если вы изучите внутреннее значение встречи. Начните с использования объекта [PropertyAccessor](https://msdn.microsoft.com/library/bb646034\(v=office.15\)) , вы обнаружите внутреннее значение даты и времени, равное локальному значению даты и времени, преобразованному в эквивалентное значение даты и времени в формате UTC.</span><span class="sxs-lookup"><span data-stu-id="cee64-111">If you examine the internal value of Appointment.Start by using the [PropertyAccessor](https://msdn.microsoft.com/library/bb646034\(v=office.15\)) object, you would find the internal date and time value is equal to the local date and time value converted to the equivalent UTC date and time value.</span></span>

<span data-ttu-id="cee64-112">Outlook использует сведения о часовом поясе, чтобы сопоставить встречу с правильным временем в формате UTC, когда он сохраняет встречу, и в правильное местное время при отображении элемента в календаре.</span><span class="sxs-lookup"><span data-stu-id="cee64-112">Outlook uses the time zone information to map the appointment to the correct UTC time when it saves an appointment, and into the correct local time when it displays the item in the calendar.</span></span> <span data-ttu-id="cee64-113">Изменение StartTimeZone влияет на значение свойства встреча. Start, которое всегда выражается в местном часовом поясе, представленном свойством [CurrentTimeZone](https://msdn.microsoft.com/library/bb612024\(v=office.15\)) объекта, возвращаемого с помощью [часовых поясов](https://msdn.microsoft.com/library/bb645170\(v=office.15\)).</span><span class="sxs-lookup"><span data-stu-id="cee64-113">Changing StartTimeZone affects the value of Appointment.Start, which is always expressed in the local time zone, represented by the [CurrentTimeZone](https://msdn.microsoft.com/library/bb612024\(v=office.15\)) property of the object returned by [TimeZones](https://msdn.microsoft.com/library/bb645170\(v=office.15\)).</span></span> <span data-ttu-id="cee64-114">Аналогично, изменение EndTimeZone влияет на значение свойства встреча. end, которое всегда выражается в местном часовом поясе, представленном свойством CurrentTimeZone объекта, возвращаемого приложением. TimeZones.</span><span class="sxs-lookup"><span data-stu-id="cee64-114">Similarly, changing EndTimeZone affects the value of Appointment.End, which is always expressed in the local time zone, represented by the CurrentTimeZone property of the object returned by Application.TimeZones.</span></span>

<span data-ttu-id="cee64-115">Конкретное значение TimeZone можно извлечь из объекта TimeZones с помощью независимого от региональных стандартов ключа TimeZone в реестре Windows.</span><span class="sxs-lookup"><span data-stu-id="cee64-115">You can retrieve a specific TimeZone from the TimeZones object by using the locale-independent key for the TimeZone in the Windows registry.</span></span> <span data-ttu-id="cee64-116">Независимые от региональных стандартов ключи TimeZone перечислены в следующем разделе: `HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Windows NT\CurrentVersion\TimeZones`.</span><span class="sxs-lookup"><span data-stu-id="cee64-116">Locale-independent TimeZone keys are listed under the following key: `HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Windows NT\CurrentVersion\TimeZones`.</span></span>

<span data-ttu-id="cee64-117">Если вы используете Visual Studio для тестирования этого примера кода, сначала добавьте ссылку на компонент библиотеки объектов Microsoft Outlook 15.0 и задайте переменную Outlook при импорте пространства имен **Microsoft.Office.Interop.Outlook**.</span><span class="sxs-lookup"><span data-stu-id="cee64-117">If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the Outlook variable when you import the **Microsoft.Office.Interop.Outlook** namespace.</span></span> <span data-ttu-id="cee64-118">Не следует использовать инструкции **Imports** и **using** непосредственно перед функциями в примере кода, но их необходимо добавить перед объявлением общедоступного класса.</span><span class="sxs-lookup"><span data-stu-id="cee64-118">The **Imports** or **using** statement must not occur directly before the functions in the code example but must be added before the public Class declaration.</span></span> <span data-ttu-id="cee64-119">В строках кода ниже показано, как выполнить импорт и назначение на Visual Basic и C\#.</span><span class="sxs-lookup"><span data-stu-id="cee64-119">The following lines of code show how to do the import and assignment in Visual Basic and C\#.</span></span>


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

## <a name="see-also"></a><span data-ttu-id="cee64-120">См. также</span><span class="sxs-lookup"><span data-stu-id="cee64-120">See also</span></span>

- [<span data-ttu-id="cee64-121">Встречи</span><span class="sxs-lookup"><span data-stu-id="cee64-121">Appointments</span></span>](appointments.md)


---
title: Создание встречи, которая повторяется по недельному расписанию
TOCTitle: Create a recurring appointment that has a weekly pattern
ms:assetid: 20b46b26-e278-451b-9e35-36683205d164
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184595(v=office.15)
ms:contentKeyID: 55119810
ms.date: 07/24/2014
mtps_version: v=office.15
ms.openlocfilehash: bc764fd1be5fb419a0bd4586e7ccba39c6a34dc9
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25405562"
---
# <a name="create-a-recurring-appointment-that-has-a-weekly-pattern"></a>Создание встречи, которая повторяется по недельному расписанию

В этом примере показывается создание повторяющейся встречи, которая имеет недельное расписание (например, встречи, которая происходит каждые понедельник, среду и пятницу).

## <a name="example"></a>Пример

> [!NOTE] 
> Приведенный ниже пример кода представляет собой фрагмент из книги [Программирование приложений для Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).


При создании повторяющейся встречи основой расписания повторения является время, которое задается при создании встречи. Например, при создании встречи, повторяющейся каждый день в 13:00, она будет ежедневно повторяться только в 13:00. Чтобы изменить расписание повторения встречи, задайте свойства объекта [RecurrencePattern](https://msdn.microsoft.com/library/bb608903\(v=office.15\)) для встречи. Задайте свойство [RecurrenceType](https://msdn.microsoft.com/library/bb623463\(v=office.15\)) объекта RecurrencePattern до назначения других свойств RecurrencePattern. В следующей таблице показаны допустимые свойства RecurrencePattern для заданного RecurrenceType (определяется перечислением [OlRecurrenceType](https://msdn.microsoft.com/library/bb647129\(v=office.15\))).

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Значение OlRecurrenceType</p></th>
<th><p>Допустимые свойства RecurrencePattern</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>olRecursDaily</p></td>
<td><p><a href="https://msdn.microsoft.com/library/bb644889(v=office.15)">Duration</a>, <a href="https://msdn.microsoft.com/library/bb644544(v=office.15)">EndTime</a>, <a href="https://msdn.microsoft.com/library/bb624287(v=office.15)">Interval</a>, <a href="https://msdn.microsoft.com/library/bb646849(v=office.15)">NoEndDate</a>, <a href="https://msdn.microsoft.com/library/bb611303(v=office.15)">Occurrences</a>, <a href="https://msdn.microsoft.com/library/bb624492(v=office.15)">PatternStartDate</a>, <a href="https://msdn.microsoft.com/library/bb609279(v=office.15)">PatternEndDate</a>, <a href="https://msdn.microsoft.com/library/bb646324(v=office.15)">StartTime</a></p></td>
</tr>
<tr class="even">
<td><p>olRecursWeekly</p></td>
<td><p><a href="https://msdn.microsoft.com/library/bb609163(v=office.15)">DayOfWeekMask</a>, Duration, EndTime, Interval, NoEndDate, Occurrences, PatternStartDate, PatternEndDate, StartTime</p></td>
</tr>
<tr class="odd">
<td><p>olRecursMonthly</p></td>
<td><p><a href="https://msdn.microsoft.com/library/bb622604(v=office.15)">DayOfMonth</a>, Duration, EndTime, Interval, NoEndDate, Occurrences, PatternStartDate, PatternEndDate, StartTime</p></td>
</tr>
<tr class="even">
<td><p>olRecursMonthNth</p></td>
<td><p>DayOfWeekMask, Duration, EndTime, Interval, <a href="https://msdn.microsoft.com/library/bb645269(v=office.15)">Instance</a>, NoEndDate, Occurrences, PatternStartDate, PatternEndDate, StartTime</p></td>
</tr>
<tr class="odd">
<td><p>olRecursYearly</p></td>
<td><p>DayOfMonth, Duration, EndTime, Interval, <a href="https://msdn.microsoft.com/library/bb610515(v=office.15)">MonthOfYear</a>, NoEndDate, Occurrences, PatternStartDate, PatternEndDate, StartTime</p></td>
</tr>
<tr class="even">
<td><p>olRecursYearNth</p></td>
<td><p>DayOfWeekMask, Duration, EndTime, Interval, Instance, NoEndDate, Occurrences, PatternStartDate, PatternEndDate, StartTime</p></td>
</tr>
</tbody>
</table>


При работе с элементами повторяющейся встречи следует удалить все предыдущие ссылки, получить новые ссылки на элемент повторяющейся встречи перед обращением к элементу или его изменением и удалить эти ссылки сразу после завершения работы и сохранения изменений. Такой подход применяется к повторяющемуся объекту **AppointmentItem** и любому объекту [Exception](https://msdn.microsoft.com/library/bb610440\(v=office.15\)) или [RecurrencePattern](https://msdn.microsoft.com/library/bb608903\(v=office.15\)). Чтобы удалить ссылку в Visual Basic, установите для существующего объекта значение Nothing. В C\# явным образом удалите память для этого объекта.

Следует отметить, что даже после удаления ссылок при попытке получения новой ссылки, когда имеется активная ссылка (удерживаемая другой надстройкой в Outlook) на один из вышеупомянутых объектов, новая ссылка будет продолжать указывать на устаревшую копию объекта. Поэтому важно удалять ссылки сразу же по окончании работы с повторяющейся встречей.

В представленном ниже примере кода RecurringAppointmentEveryMondayWednesdayFriday создает объект [AppointmentItem](https://msdn.microsoft.com/library/bb645611\(v=office.15\)), а затем вызывает [GetRecurrencePattern()](https://msdn.microsoft.com/library/bb652582\(v=office.15\)), чтобы получить вновь созданный объект RecurrencePattern для встречи. Затем RecurringAppointmentEveryMondayWednesdayFriday задает свойства RecurrenceType, DayOfWeekMask, PatternStartDate, PatternEndDate, Duration, StartTime, EndTime и Subject, сохраняет встречу и отображает ее с расписанием "Происходит каждый понедельник, среду и пятницу, начиная с 7.10.2006 по 8.25.2006 с 14:00 до 15:00".

Если вы используете Visual Studio для тестирования этого примера кода, сначала добавьте ссылку на компонент Microsoft Outlook 15.0 Object Library и задайте переменную Outlook при импорте пространства имен **Microsoft.Office.Interop.Outlook**. Инструкция **using** не должна идти непосредственно перед функциями в примере кода, но ее нужно добавить перед открытым объявлением Class. В следующей строке кода показано, как выполнить импорт и назначение в C\#.

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```

```csharp
private void RecurringAppointmentEveryMondayWednesdayFriday()
{
    Outlook.AppointmentItem appt = Application.CreateItem(
        Outlook.OlItemType.olAppointmentItem)
        as Outlook.AppointmentItem;
    appt.Subject = "Recurring Appointment DaysOfWeekMask Example";
    Outlook.RecurrencePattern pattern = appt.GetRecurrencePattern();
    pattern.RecurrenceType = Outlook.OlRecurrenceType.olRecursWeekly;
    // Logical OR for DayOfWeekMask creates pattern
    pattern.DayOfWeekMask = Outlook.OlDaysOfWeek.olMonday |
        Outlook.OlDaysOfWeek.olWednesday |
        Outlook.OlDaysOfWeek.olFriday;
    pattern.PatternStartDate = DateTime.Parse("7/10/2006");
    pattern.PatternEndDate = DateTime.Parse("8/25/2006");
    pattern.Duration = 60;
    pattern.StartTime = DateTime.Parse("2:00:00 PM");
    pattern.EndTime = DateTime.Parse("3:00:00 PM");
    appt.Save();
    appt.Display(false);
}
```

## <a name="see-also"></a>См. также

- [Встречи](appointments.md)


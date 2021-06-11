---
title: Создание встречи, которая повторяется по недельному расписанию
TOCTitle: Create a recurring appointment that has a weekly pattern
ms:assetid: 20b46b26-e278-451b-9e35-36683205d164
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184595(v=office.15)
ms:contentKeyID: 55119810
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: b326ad23f8cbe47e5141775eacdd2bc9302db3cd
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359173"
---
# <a name="create-a-recurring-appointment-that-has-a-weekly-pattern"></a><span data-ttu-id="ce7f4-102">Создание встречи, которая повторяется по недельному расписанию</span><span class="sxs-lookup"><span data-stu-id="ce7f4-102">Create a recurring appointment that has a weekly pattern</span></span>

<span data-ttu-id="ce7f4-103">В этом примере показывается создание повторяющейся встречи, которая имеет недельное расписание (например, встречи, которая происходит каждые понедельник, среду и пятницу).</span><span class="sxs-lookup"><span data-stu-id="ce7f4-103">This example shows how to create a recurring appointment that has a weekly pattern (for example, an appointment that occurs every Monday, Wednesday, and Friday).</span></span>

## <a name="example"></a><span data-ttu-id="ce7f4-104">Пример</span><span class="sxs-lookup"><span data-stu-id="ce7f4-104">Example</span></span>

> [!NOTE] 
> <span data-ttu-id="ce7f4-105">Приведенный ниже пример кода представляет собой фрагмент из книги [Программирование приложений для Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).</span><span class="sxs-lookup"><span data-stu-id="ce7f4-105">The following code example is an excerpt from [Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).</span></span>


<span data-ttu-id="ce7f4-106">При создании повторяющейся встречи основой расписания повторения является время, которое задается при создании встречи.</span><span class="sxs-lookup"><span data-stu-id="ce7f4-106">When you create a new recurring appointment, the recurrence pattern is based on the time you specify when you create the appointment.</span></span> <span data-ttu-id="ce7f4-107">Например, при создании встречи, повторяющейся каждый день в 13:00, она будет ежедневно повторяться только в 13:00.</span><span class="sxs-lookup"><span data-stu-id="ce7f4-107">For example, if you create an appointment that recurs daily at 1:00 PM, the appointment will recur only at 1:00 PM on a daily basis.</span></span> <span data-ttu-id="ce7f4-108">Чтобы изменить расписание повторения встречи, задайте свойства объекта [RecurrencePattern](https://msdn.microsoft.com/library/bb608903\(v=office.15\)) для встречи.</span><span class="sxs-lookup"><span data-stu-id="ce7f4-108">To change the recurrence pattern of an appointment, set the properties of the appointment’s [RecurrencePattern](https://msdn.microsoft.com/library/bb608903\(v=office.15\)) object.</span></span> <span data-ttu-id="ce7f4-109">Задайте свойство [RecurrenceType](https://msdn.microsoft.com/library/bb623463\(v=office.15\)) объекта RecurrencePattern до назначения других свойств RecurrencePattern.</span><span class="sxs-lookup"><span data-stu-id="ce7f4-109">Set the [RecurrenceType](https://msdn.microsoft.com/library/bb623463\(v=office.15\)) property of the RecurrencePattern object before setting other RecurrencePattern properties.</span></span> <span data-ttu-id="ce7f4-110">В следующей таблице показаны допустимые свойства RecurrencePattern для заданного RecurrenceType (определяется перечислением [OlRecurrenceType](https://msdn.microsoft.com/library/bb647129\(v=office.15\))).</span><span class="sxs-lookup"><span data-stu-id="ce7f4-110">The following table shows valid RecurrencePattern properties for a given RecurrenceType (specified by the [OlRecurrenceType](https://msdn.microsoft.com/library/bb647129\(v=office.15\)) enumeration).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="ce7f4-111">Значение OlRecurrenceType</span><span class="sxs-lookup"><span data-stu-id="ce7f4-111">OlRecurrenceType value</span></span></p></th>
<th><p><span data-ttu-id="ce7f4-112">Допустимые свойства RecurrencePattern</span><span class="sxs-lookup"><span data-stu-id="ce7f4-112">Valid RecurrencePattern properties</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ce7f4-113">olRecursDaily</span><span class="sxs-lookup"><span data-stu-id="ce7f4-113">olRecursDaily</span></span></p></td>
<td><p><span data-ttu-id="ce7f4-114"><a href="https://msdn.microsoft.com/library/bb644889(v=office.15)">Duration</a>, <a href="https://msdn.microsoft.com/library/bb644544(v=office.15)">EndTime</a>, <a href="https://msdn.microsoft.com/library/bb624287(v=office.15)">Interval</a>, <a href="https://msdn.microsoft.com/library/bb646849(v=office.15)">NoEndDate</a>, <a href="https://msdn.microsoft.com/library/bb611303(v=office.15)">Occurrences</a>, <a href="https://msdn.microsoft.com/library/bb624492(v=office.15)">PatternStartDate</a>, <a href="https://msdn.microsoft.com/library/bb609279(v=office.15)">PatternEndDate</a>, <a href="https://msdn.microsoft.com/library/bb646324(v=office.15)">StartTime</a></span><span class="sxs-lookup"><span data-stu-id="ce7f4-114"><a href="https://msdn.microsoft.com/library/bb644889(v=office.15)">Duration</a>, <a href="https://msdn.microsoft.com/library/bb644544(v=office.15)">EndTime</a>, <a href="https://msdn.microsoft.com/library/bb624287(v=office.15)">Interval</a>, <a href="https://msdn.microsoft.com/library/bb646849(v=office.15)">NoEndDate</a>, <a href="https://msdn.microsoft.com/library/bb611303(v=office.15)">Occurrences</a>, <a href="https://msdn.microsoft.com/library/bb624492(v=office.15)">PatternStartDate</a>, <a href="https://msdn.microsoft.com/library/bb609279(v=office.15)">PatternEndDate</a>, <a href="https://msdn.microsoft.com/library/bb646324(v=office.15)">StartTime</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ce7f4-115">olRecursWeekly</span><span class="sxs-lookup"><span data-stu-id="ce7f4-115">olRecursWeekly</span></span></p></td>
<td><p><span data-ttu-id="ce7f4-116"><a href="https://msdn.microsoft.com/library/bb609163(v=office.15)">DayOfWeekMask</a>, Duration, EndTime, Interval, NoEndDate, Occurrences, PatternStartDate, PatternEndDate, StartTime</span><span class="sxs-lookup"><span data-stu-id="ce7f4-116"><a href="https://msdn.microsoft.com/library/bb609163(v=office.15)">DayOfWeekMask</a>, Duration, EndTime, Interval, NoEndDate, Occurrences, PatternStartDate, PatternEndDate, StartTime</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ce7f4-117">olRecursMonthly</span><span class="sxs-lookup"><span data-stu-id="ce7f4-117">olRecursMonthly</span></span></p></td>
<td><p><span data-ttu-id="ce7f4-118"><a href="https://msdn.microsoft.com/library/bb622604(v=office.15)">DayOfMonth</a>, Duration, EndTime, Interval, NoEndDate, Occurrences, PatternStartDate, PatternEndDate, StartTime</span><span class="sxs-lookup"><span data-stu-id="ce7f4-118"><a href="https://msdn.microsoft.com/library/bb622604(v=office.15)">DayOfMonth</a>, Duration, EndTime, Interval, NoEndDate, Occurrences, PatternStartDate, PatternEndDate, StartTime</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ce7f4-119">olRecursMonthNth</span><span class="sxs-lookup"><span data-stu-id="ce7f4-119">olRecursMonthNth</span></span></p></td>
<td><p><span data-ttu-id="ce7f4-120">DayOfWeekMask, Duration, EndTime, Interval, <a href="https://msdn.microsoft.com/library/bb645269(v=office.15)">Instance</a>, NoEndDate, Occurrences, PatternStartDate, PatternEndDate, StartTime</span><span class="sxs-lookup"><span data-stu-id="ce7f4-120">DayOfWeekMask, Duration, EndTime, Interval, <a href="https://msdn.microsoft.com/library/bb645269(v=office.15)">Instance</a>, NoEndDate, Occurrences, PatternStartDate, PatternEndDate, StartTime</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ce7f4-121">olRecursYearly</span><span class="sxs-lookup"><span data-stu-id="ce7f4-121">olRecursYearly</span></span></p></td>
<td><p><span data-ttu-id="ce7f4-122">DayOfMonth, Duration, EndTime, Interval, <a href="https://msdn.microsoft.com/library/bb610515(v=office.15)">MonthOfYear</a>, NoEndDate, Occurrences, PatternStartDate, PatternEndDate, StartTime</span><span class="sxs-lookup"><span data-stu-id="ce7f4-122">DayOfMonth, Duration, EndTime, Interval, <a href="https://msdn.microsoft.com/library/bb610515(v=office.15)">MonthOfYear</a>, NoEndDate, Occurrences, PatternStartDate, PatternEndDate, StartTime</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ce7f4-123">olRecursYearNth</span><span class="sxs-lookup"><span data-stu-id="ce7f4-123">olRecursYearNth</span></span></p></td>
<td><p><span data-ttu-id="ce7f4-124">DayOfWeekMask, Duration, EndTime, Interval, Instance, NoEndDate, Occurrences, PatternStartDate, PatternEndDate, StartTime</span><span class="sxs-lookup"><span data-stu-id="ce7f4-124">DayOfWeekMask, Duration, EndTime, Interval, Instance, NoEndDate, Occurrences, PatternStartDate, PatternEndDate, StartTime</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="ce7f4-125">При работе с элементами повторяющейся встречи следует удалить все предыдущие ссылки, получить новые ссылки на элемент повторяющейся встречи перед обращением к элементу или его изменением и удалить эти ссылки сразу после завершения работы и сохранения изменений.</span><span class="sxs-lookup"><span data-stu-id="ce7f4-125">When you work with recurring appointment items, you should release any prior references, obtain new references to the recurring appointment item before you access or modify the item, and release these references as soon as you are finished and have saved the changes.</span></span> <span data-ttu-id="ce7f4-126">Такой подход применяется к повторяющемуся объекту **AppointmentItem** и любому объекту [Exception](https://msdn.microsoft.com/library/bb610440\(v=office.15\)) или [RecurrencePattern](https://msdn.microsoft.com/library/bb608903\(v=office.15\)).</span><span class="sxs-lookup"><span data-stu-id="ce7f4-126">This practice applies to the recurring **AppointmentItem** object, and any [Exception](https://msdn.microsoft.com/library/bb610440\(v=office.15\)) or [RecurrencePattern](https://msdn.microsoft.com/library/bb608903\(v=office.15\)) object.</span></span> <span data-ttu-id="ce7f4-127">Чтобы удалить ссылку в Visual Basic, установите для существующего объекта значение Nothing.</span><span class="sxs-lookup"><span data-stu-id="ce7f4-127">To release a reference in Visual Basic, set that existing object to Nothing.</span></span> <span data-ttu-id="ce7f4-128">В C\# явным образом освободите память для этого объекта.</span><span class="sxs-lookup"><span data-stu-id="ce7f4-128">In C\#, explicitly release the memory for that object.</span></span>

<span data-ttu-id="ce7f4-p103">Следует отметить, что даже после удаления ссылок при попытке получения новой ссылки, когда имеется активная ссылка (удерживаемая другой надстройкой в Outlook) на один из вышеупомянутых объектов, новая ссылка будет продолжать указывать на устаревшую копию объекта. Поэтому важно удалять ссылки сразу же по окончании работы с повторяющейся встречей.</span><span class="sxs-lookup"><span data-stu-id="ce7f4-p103">Note that even after you release your reference and attempt to obtain a new reference, if there is still an active reference (held by another add-in or Outlook) to one of the above objects, your new reference will still point to an out-of-date copy of the object. Therefore, it is important that you release your references as soon as you are finished with the recurring appointment.</span></span>

<span data-ttu-id="ce7f4-131">В представленном ниже примере кода RecurringAppointmentEveryMondayWednesdayFriday создает объект [AppointmentItem](https://msdn.microsoft.com/library/bb645611\(v=office.15\)), а затем вызывает [GetRecurrencePattern()](https://msdn.microsoft.com/library/bb652582\(v=office.15\)), чтобы получить вновь созданный объект RecurrencePattern для встречи.</span><span class="sxs-lookup"><span data-stu-id="ce7f4-131">In the following code example, RecurringAppointmentEveryMondayWednesdayFriday creates an [AppointmentItem](https://msdn.microsoft.com/library/bb645611\(v=office.15\)) object, and then calls [GetRecurrencePattern()](https://msdn.microsoft.com/library/bb652582\(v=office.15\)) to get the newly created appointment’s RecurrencePattern object.</span></span> <span data-ttu-id="ce7f4-132">Затем RecurringAppointmentEveryMondayWednesdayFriday задает свойства RecurrenceType, DayOfWeekMask, PatternStartDate, PatternEndDate, Duration, StartTime, EndTime и Subject, сохраняет встречу и отображает ее с расписанием "Происходит каждый понедельник, среду и пятницу, начиная с 7.10.2006 по 8.25.2006 с 14:00 до 15:00".</span><span class="sxs-lookup"><span data-stu-id="ce7f4-132">RecurringAppointmentEveryMondayWednesdayFriday then sets the RecurrenceType, DayOfWeekMask, PatternStartDate, PatternEndDate, Duration, StartTime, EndTime, and Subject properties, saves the appointment, and finally displays the appointment with the pattern "Occurs every Monday, Wednesday, and Friday effective 7/10/2006 until 8/25/2006 from 2:00 PM to 3:00 PM."</span></span>

<span data-ttu-id="ce7f4-133">Если вы используете Visual Studio для тестирования этого примера кода, сначала добавьте ссылку на компонент Microsoft Outlook 15.0 Object Library и задайте переменную Outlook при импорте пространства имен **Microsoft.Office.Interop.Outlook**.</span><span class="sxs-lookup"><span data-stu-id="ce7f4-133">If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the Outlook variable when you import the **Microsoft.Office.Interop.Outlook** namespace.</span></span> <span data-ttu-id="ce7f4-134">Инструкция **using** не должна находиться непосредственно перед функциями в примере кода, но ее нужно добавить перед объявлением общедоступного класса.</span><span class="sxs-lookup"><span data-stu-id="ce7f4-134">The **using** statement must not occur directly before the functions in the code example but must be added before the public Class declaration.</span></span> <span data-ttu-id="ce7f4-135">В приведенной ниже строке кода показано, как выполнить импорт и назначение на языке C\#.</span><span class="sxs-lookup"><span data-stu-id="ce7f4-135">The following line of code shows how to do the import and assignment in C\#.</span></span>

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

## <a name="see-also"></a><span data-ttu-id="ce7f4-136">См. также</span><span class="sxs-lookup"><span data-stu-id="ce7f4-136">See also</span></span>

- [<span data-ttu-id="ce7f4-137">Встречи</span><span class="sxs-lookup"><span data-stu-id="ce7f4-137">Appointments</span></span>](appointments.md)


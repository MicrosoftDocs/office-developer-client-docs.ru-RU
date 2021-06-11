---
title: Создание ежегодно повторяющейся встречи, в которой используется шаблон YearNth
TOCTitle: Create an annual recurring appointment that uses a YearNth pattern
ms:assetid: 5fb2ad0b-248c-417d-8868-52e0550d970f
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184611(v=office.15)
ms:contentKeyID: 55119811
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 9fc50166674ee7b9699ef8e29c5ff1e54db705ad
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32349506"
---
# <a name="create-an-annual-recurring-appointment-that-uses-a-yearnth-pattern"></a><span data-ttu-id="74a45-102">Создание ежегодно повторяющейся встречи, в которой используется шаблон YearNth</span><span class="sxs-lookup"><span data-stu-id="74a45-102">Create an annual recurring appointment that uses a YearNth pattern</span></span>

<span data-ttu-id="74a45-103">В этом примере показывается создание встречи с годовым шаблоном повторяемости, таким как первый понедельник июня.</span><span class="sxs-lookup"><span data-stu-id="74a45-103">This example shows how to create an appointment for which the annual recurrence pattern is a specific day such as the first Monday in June.</span></span>

## <a name="example"></a><span data-ttu-id="74a45-104">Пример</span><span class="sxs-lookup"><span data-stu-id="74a45-104">Example</span></span>

> [!NOTE] 
> <span data-ttu-id="74a45-105">Приведенный ниже пример кода представляет собой фрагмент из книги [Программирование приложений для Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).</span><span class="sxs-lookup"><span data-stu-id="74a45-105">The following code example is an excerpt from [Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).</span></span>

<span data-ttu-id="74a45-106">Если вы хотите создать ежегодную встречу, которая повторяется в определенный день недели определенного месяца (например, в первый понедельник июня), необходимо использовать повторения YearNth.</span><span class="sxs-lookup"><span data-stu-id="74a45-106">If you want to create an annual appointment that recurs on a specific day of the week during a specific month (for example, the first Monday in June), you must use YearNth recurrences.</span></span> <span data-ttu-id="74a45-107">Чтобы настроить повторение YearNth, требуется сначала установить значение olRecursYearNth для свойства [RecurrenceType](https://msdn.microsoft.com/library/bb623463\(v=office.15\)) объекта [RecurrencePattern](https://msdn.microsoft.com/library/bb608903\(v=office.15\)).</span><span class="sxs-lookup"><span data-stu-id="74a45-107">To set a YearNth recurrence, you must first set the [RecurrenceType](https://msdn.microsoft.com/library/bb623463\(v=office.15\)) property of the [RecurrencePattern](https://msdn.microsoft.com/library/bb608903\(v=office.15\)) object to olRecursYearNth.</span></span> <span data-ttu-id="74a45-108">Затем задайте свойство [DayOfWeekMask](https://msdn.microsoft.com/library/bb609163\(v=office.15\)), чтобы указать, в какой день недели должна повторяться встреча, и свойство [Instance](https://msdn.microsoft.com/library/bb645269\(v=office.15\)), чтобы указать порядковый номер вхождения этого дня недели (например, третий вторник) в выбранном месяце для годового шаблона.</span><span class="sxs-lookup"><span data-stu-id="74a45-108">Then set the [DayOfWeekMask](https://msdn.microsoft.com/library/bb609163\(v=office.15\)) property to specify on which day of the week the appointment should recur, and the [Instance](https://msdn.microsoft.com/library/bb645269\(v=office.15\)) property to specify the Nth occurrence of the specified day of the week (for example, the third Tuesday) during a specified month for the yearly pattern.</span></span>

<span data-ttu-id="74a45-109">При работе с элементами повторяющейся встречи следует удалить все предыдущие ссылки, получить новые ссылки на элемент повторяющейся встречи перед обращением к элементу или его изменением и удалить эти ссылки сразу после завершения работы и сохранения изменений.</span><span class="sxs-lookup"><span data-stu-id="74a45-109">When you work with recurring appointment items, you should release any prior references, obtain new references to the recurring appointment item before you access or modify the item, and release these references as soon as you are finished and have saved the changes.</span></span> <span data-ttu-id="74a45-110">Такой подход применяется к повторяющемуся объекту **AppointmentItem** и любому объекту [Exception](https://msdn.microsoft.com/library/bb610440\(v=office.15\)) или [RecurrencePattern](https://msdn.microsoft.com/library/bb608903\(v=office.15\)).</span><span class="sxs-lookup"><span data-stu-id="74a45-110">This practice applies to the recurring **AppointmentItem** object, and any [Exception](https://msdn.microsoft.com/library/bb610440\(v=office.15\)) or [RecurrencePattern](https://msdn.microsoft.com/library/bb608903\(v=office.15\)) object.</span></span> <span data-ttu-id="74a45-111">Чтобы удалить ссылку в Visual Basic, установите для существующего объекта значение Nothing.</span><span class="sxs-lookup"><span data-stu-id="74a45-111">To release a reference in Visual Basic, set that existing object to Nothing.</span></span> <span data-ttu-id="74a45-112">В C\# явным образом освободите память для этого объекта.</span><span class="sxs-lookup"><span data-stu-id="74a45-112">In C\#, explicitly release the memory for that object.</span></span>

<span data-ttu-id="74a45-p103">Следует отметить, что даже после удаления ссылок при попытке получения новой ссылки, когда имеется активная ссылка (удерживаемая другой надстройкой в Outlook) на один из вышеупомянутых объектов, новая ссылка будет продолжать указывать на устаревшую копию объекта. Поэтому важно удалять ссылки сразу же по окончании работы с повторяющейся встречей.</span><span class="sxs-lookup"><span data-stu-id="74a45-p103">Note that even after you release your reference and attempt to obtain a new reference, if there is still an active reference (held by another add-in or Outlook) to one of the above objects, your new reference will still point to an out-of-date copy of the object. Therefore, it is important that you release your references as soon as you are finished with the recurring appointment.</span></span>

<span data-ttu-id="74a45-115">В представленном ниже примере кода процедура RecurringYearNthAppointment создает встречу с шаблоном повторения YearNth.</span><span class="sxs-lookup"><span data-stu-id="74a45-115">In the following code example, RecurringYearNthAppointment creates an appointment that has a YearNth recurrence pattern.</span></span> <span data-ttu-id="74a45-116">Процедура RecurringYearNthAppointment сначала создает повторяющуюся встречу путем создания объекта [AppointmentItem](https://msdn.microsoft.com/library/bb645611\(v=office.15\)).</span><span class="sxs-lookup"><span data-stu-id="74a45-116">RecurringYearNthAppointment first creates a recurring appointment by creating an [AppointmentItem](https://msdn.microsoft.com/library/bb645611\(v=office.15\)) object.</span></span> <span data-ttu-id="74a45-117">После этого она получает расписание повторения с помощью метода [GetRecurrencePattern()](https://msdn.microsoft.com/library/bb652582\(v=office.15\)).</span><span class="sxs-lookup"><span data-stu-id="74a45-117">Next, it gets the appointment’s recurrence pattern by using the [GetRecurrencePattern()](https://msdn.microsoft.com/library/bb652582\(v=office.15\)) method.</span></span> <span data-ttu-id="74a45-118">Затем задаются следующие свойства RecurrencePattern: RecurrenceType, DayOfWeekMask, [MonthOfYear](https://msdn.microsoft.com/library/bb610515\(v=office.15\)), [Instance](https://msdn.microsoft.com/library/bb645269\(v=office.15\)), [Occurrences](https://msdn.microsoft.com/library/bb611303\(v=office.15\)), [Duration](https://msdn.microsoft.com/library/bb644889\(v=office.15\)), [PatternStartDate](https://msdn.microsoft.com/library/bb624492\(v=office.15\)), [StartTime](https://msdn.microsoft.com/library/bb646324\(v=office.15\)) и [EndTime](https://msdn.microsoft.com/library/bb644544\(v=office.15\)).</span><span class="sxs-lookup"><span data-stu-id="74a45-118">It then sets the following RecurrencePattern properties: RecurrenceType, DayOfWeekMask, [MonthOfYear](https://msdn.microsoft.com/library/bb610515\(v=office.15\)), [Instance](https://msdn.microsoft.com/library/bb645269\(v=office.15\)), [Occurrences](https://msdn.microsoft.com/library/bb611303\(v=office.15\)), [Duration](https://msdn.microsoft.com/library/bb644889\(v=office.15\)), [PatternStartDate](https://msdn.microsoft.com/library/bb624492\(v=office.15\)), [StartTime](https://msdn.microsoft.com/library/bb646324\(v=office.15\)), and [EndTime](https://msdn.microsoft.com/library/bb644544\(v=office.15\)).</span></span> <span data-ttu-id="74a45-119">Свойство MonthOfYear может принимать числовые значения от 1 до 12, где каждое число представляет соответствующий месяц.</span><span class="sxs-lookup"><span data-stu-id="74a45-119">The MonthOfYear property can take a numerical value of 1 through 12, where each number represents the corresponding month.</span></span> <span data-ttu-id="74a45-120">После задания свойств процедура RecurringYearNthAppointment сохраняет встречу и отображает ее с расписанием "Происходит в первый понедельник июня с 06.01.2007 по 06.06.2016 с 14:00 до 17:00".</span><span class="sxs-lookup"><span data-stu-id="74a45-120">Once the properties are set, RecurringYearNthAppointment saves the appointment, and then displays it with the pattern "Occurs the first Monday of June effective 6/1/2007 until 6/6/2016 from 2:00 PM to 5:00 PM."</span></span>

<span data-ttu-id="74a45-121">Если вы используете Visual Studio для тестирования этого примера кода, сначала добавьте ссылку на компонент Microsoft Outlook 15.0 Object Library и задайте переменную Outlook при импорте пространства имен **Microsoft.Office.Interop.Outlook**.</span><span class="sxs-lookup"><span data-stu-id="74a45-121">If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the Outlook variable when you import the **Microsoft.Office.Interop.Outlook** namespace.</span></span> <span data-ttu-id="74a45-122">Инструкция **using** не должна находиться непосредственно перед функциями в примере кода, но ее нужно добавить перед объявлением общедоступного класса.</span><span class="sxs-lookup"><span data-stu-id="74a45-122">The **using** statement must not occur directly before the functions in the code example but must be added before the public Class declaration.</span></span> <span data-ttu-id="74a45-123">В приведенной ниже строке кода показано, как выполнить импорт и назначение на языке C\#.</span><span class="sxs-lookup"><span data-stu-id="74a45-123">The following line of code shows how to do the import and assignment in C\#.</span></span>

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```

```csharp
private void RecurringYearNthAppointment()
{
    Outlook.AppointmentItem appt = Application.CreateItem(
        Outlook.OlItemType.olAppointmentItem)
        as Outlook.AppointmentItem;
    appt.Subject = "Recurring YearNth Appointment";
    Outlook.RecurrencePattern pattern = appt.GetRecurrencePattern();
    pattern.RecurrenceType = Outlook.OlRecurrenceType.olRecursYearNth;
    pattern.DayOfWeekMask = Outlook.OlDaysOfWeek.olMonday;
    pattern.MonthOfYear = 6;
    pattern.Instance = 1;
    pattern.Occurrences = 10;
    pattern.Duration = 180;
    pattern.PatternStartDate = DateTime.Parse("6/1/2007");
    pattern.StartTime = DateTime.Parse("2:00:00 PM");
    pattern.EndTime = DateTime.Parse("5:00:00 PM");
    appt.Save();
    appt.Display(false);
}
```

## <a name="see-also"></a><span data-ttu-id="74a45-124">См. также</span><span class="sxs-lookup"><span data-stu-id="74a45-124">See also</span></span>

- [<span data-ttu-id="74a45-125">Встречи</span><span class="sxs-lookup"><span data-stu-id="74a45-125">Appointments</span></span>](appointments.md)


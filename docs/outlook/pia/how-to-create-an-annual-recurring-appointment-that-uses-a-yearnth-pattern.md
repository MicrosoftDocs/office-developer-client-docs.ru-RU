---
title: Создание ежегодно повторяющейся встречи, в которой используется шаблон YearNth
TOCTitle: Create an annual recurring appointment that uses a YearNth pattern
ms:assetid: 5fb2ad0b-248c-417d-8868-52e0550d970f
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184611(v=office.15)
ms:contentKeyID: 55119811
ms.date: 07/24/2014
mtps_version: v=office.15
ms.openlocfilehash: 9aa18f0e2f875e86acf6cacbf222577e0f9c93e2
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25407081"
---
# <a name="create-an-annual-recurring-appointment-that-uses-a-yearnth-pattern"></a>Создание ежегодно повторяющейся встречи, в которой используется шаблон YearNth

В этом примере показывается создание встречи с годовым шаблоном повторяемости, таким как первый понедельник июня.

## <a name="example"></a>Пример

> [!NOTE] 
> Приведенный ниже пример кода представляет собой фрагмент из книги [Программирование приложений для Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).

Если вы хотите создать ежегодную встречу, которая повторяется в определенный день недели определенного месяца (например, в первый понедельник июня), необходимо использовать повторения YearNth. Чтобы задать повторение YearNth, необходимо сначала установить значение olRecursYearNth для свойства [RecurrenceType](https://msdn.microsoft.com/library/bb623463\(v=office.15\)) объекта [RecurrencePattern](https://msdn.microsoft.com/library/bb608903\(v=office.15\)). Затем задайте свойство [DayOfWeekMask](https://msdn.microsoft.com/library/bb609163\(v=office.15\)), чтобы указать, в какой день недели должна повторяться встреча, и свойство [Instance](https://msdn.microsoft.com/library/bb645269\(v=office.15\)), чтобы указать порядковый номер вхождения указанного дня недели (например, третий вторник) в указанном месяце для годового шаблона.

При работе с элементами повторяющейся встречи следует удалить все предыдущие ссылки, получить новые ссылки на элемент повторяющейся встречи перед обращением к элементу или его изменением и удалить эти ссылки сразу после завершения работы и сохранения изменений. Такой подход применяется к повторяющемуся объекту **AppointmentItem** и любому объекту [Exception](https://msdn.microsoft.com/library/bb610440\(v=office.15\)) или [RecurrencePattern](https://msdn.microsoft.com/library/bb608903\(v=office.15\)). Чтобы удалить ссылку в Visual Basic, установите для существующего объекта значение Nothing. В C\# явным образом удалите память для этого объекта.

Следует отметить, что даже после удаления ссылок при попытке получения новой ссылки, когда имеется активная ссылка (удерживаемая другой надстройкой в Outlook) на один из вышеупомянутых объектов, новая ссылка будет продолжать указывать на устаревшую копию объекта. Поэтому важно удалять ссылки сразу же по окончании работы с повторяющейся встречей.

В представленном ниже примере кода процедура RecurringYearNthAppointment создает встречу с шаблоном повторения YearNth. Процедура RecurringYearNthAppointment сначала создает повторяющуюся встречу путем создания объекта [AppointmentItem](https://msdn.microsoft.com/library/bb645611\(v=office.15\)). После этого она получает расписание повторения с помощью метода [GetRecurrencePattern()](https://msdn.microsoft.com/library/bb652582\(v=office.15\)). Затем задаются следующие свойства RecurrencePattern: RecurrenceType, DayOfWeekMask, [MonthOfYear](https://msdn.microsoft.com/library/bb610515\(v=office.15\)), [Instance](https://msdn.microsoft.com/library/bb645269\(v=office.15\)), [Occurrences](https://msdn.microsoft.com/library/bb611303\(v=office.15\)), [Duration](https://msdn.microsoft.com/library/bb644889\(v=office.15\)), [PatternStartDate](https://msdn.microsoft.com/library/bb624492\(v=office.15\)), [StartTime](https://msdn.microsoft.com/library/bb646324\(v=office.15\)) и [EndTime](https://msdn.microsoft.com/library/bb644544\(v=office.15\)). Свойство MonthOfYear может принимать числовые значения от 1 до 12, где каждое число представляет соответствующий месяц. После задания свойств процедура RecurringYearNthAppointment сохраняет встречу и отображает ее с расписанием "Происходит в первый понедельник июня, начиная с 06.01.2007 по 06.06.2016 с 14:00 до 17:00".

Если вы используете Visual Studio для тестирования этого примера кода, сначала добавьте ссылку на компонент Microsoft Outlook 15.0 Object Library и задайте переменную Outlook при импорте пространства имен **Microsoft.Office.Interop.Outlook**. Инструкция **using** не должна идти непосредственно перед функциями в примере кода, но ее нужно добавить перед открытым объявлением Class. В следующей строке кода показано, как выполнить импорт и назначение в C\#.

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

## <a name="see-also"></a>См. также

- [Встречи](appointments.md)


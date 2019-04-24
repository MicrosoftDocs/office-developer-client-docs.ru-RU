---
title: Создание повторяющейся встречи с использованием установленного по умолчанию шаблона повтора
TOCTitle: Create a recurring appointment by using the default recurrence pattern
ms:assetid: 157bf1ae-2efe-4783-99ea-606722dde204
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184589(v=office.15)
ms:contentKeyID: 55119809
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: de58523e663349c43cc358f5b76896987a0f23b3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32332118"
---
# <a name="create-a-recurring-appointment-by-using-the-default-recurrence-pattern"></a>Создание повторяющейся встречи с использованием установленного по умолчанию шаблона повтора

В этом примере показывается создание повторяющейся встречи с помощью шаблона повторения по умолчанию.

## <a name="example"></a>Пример

> [!NOTE] 
> Приведенный ниже пример кода взят из книги [Программирование приложений для Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).


При создании встречи в Outlook создается объект [AppointmentItem](https://msdn.microsoft.com/library/bb645611\(v=office.15\)). Встреча является повторяющейся, если свойству [IsRecurring](https://msdn.microsoft.com/library/bb609491\(v=office.15\)) объекта AppointmentItem присвоено значение true. Значение IsRecurring нельзя задать напрямую. 

Но можно создать повторяющуюся встречу с помощью объекта [RecurrencePattern](https://msdn.microsoft.com/library/bb608903\(v=office.15\)). Чтобы программно создать повторяющуюся встречу, создайте объект **AppointmentItem**, вызовите метод [GetRecurrencePattern()](https://msdn.microsoft.com/library/bb652582\(v=office.15\)) объекта **AppointmentItem** и сохраните объект **AppointmentItem**. Это создает встречу, использующую шаблон повторения по умолчанию, которая происходит еженедельно (в день недели, для которого она создана) и не имеет даты окончания. Объект RecurrencePattern позволяет создавать повторяющиеся встречи с указанными интервалами: ежедневные, еженедельные, ежемесячные или ежегодные. Если не указать интервалы для объекта RecurrencePattern, Outlook будет использовать шаблон повторения по умолчанию.

При работе с элементами повторяющейся встречи следует удалить все предыдущие ссылки, получить новые ссылки на элемент повторяющейся встречи перед обращением к элементу или его изменением и удалить эти ссылки сразу после завершения работы и сохранения изменений. Такой подход применяется к повторяющемуся объекту **AppointmentItem** и любому объекту [Exception](https://msdn.microsoft.com/library/bb610440\(v=office.15\)) или [RecurrencePattern](https://msdn.microsoft.com/library/bb608903\(v=office.15\)). Чтобы удалить ссылку в Visual Basic, установите для существующего объекта значение Nothing. В C\# явным образом освободите память для этого объекта.

Следует отметить, что даже после удаления ссылок при попытке получения новой ссылки, когда имеется активная ссылка (удерживаемая другой надстройкой в Outlook) на один из вышеупомянутых объектов, новая ссылка будет продолжать указывать на устаревшую копию объекта. Поэтому важно удалять ссылки сразу же по окончании работы с повторяющейся встречей.

В приведенном ниже примере метод CreateRecurringAppointment создает объект **AppointmentItem**. Затем вызывается метод GetRecurrencePattern. Метод GetRecurrencePattern возвращает объект RecurrencePattern, и сохраняется объект AppointmentItem. При этом создается повторяющаяся встреча с использованием установленного по умолчанию шаблона повтора.

Если для тестирования этого примера кода вы используете Visual Studio, сначала добавьте ссылку на компонент библиотеки объектов Microsoft Outlook 15.0 и укажите переменную Outlook при импорте пространства имен **Microsoft.Office.Interop.Outlook**. Инструкция **using** не должна находиться непосредственно перед функциями в примере кода, но ее нужно добавить перед объявлением общедоступного класса. В приведенной ниже строке кода показано, как выполнить импорт и назначение на языке C\#.

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```

```csharp
private void CreateRecurringAppointment()
{
    Outlook.AppointmentItem appt = Application.CreateItem(
        Outlook.OlItemType.olAppointmentItem)
        as Outlook.AppointmentItem;
    appt.Subject = "Weekly Extensibility Team Meeting";
    Outlook.RecurrencePattern pattern = appt.GetRecurrencePattern();
    appt.Save();
}
```

## <a name="see-also"></a>См. также

- [Встречи](appointments.md)


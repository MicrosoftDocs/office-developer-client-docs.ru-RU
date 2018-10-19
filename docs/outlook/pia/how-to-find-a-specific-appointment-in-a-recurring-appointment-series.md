---
title: Поиск определенной встречи в серии повторяющихся встреч
TOCTitle: Find a specific appointment in a recurring appointment series
ms:assetid: 01f55f04-7245-4325-a354-50a6eb270a31
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184586(v=office.15)
ms:contentKeyID: 55119812
ms.date: 07/24/2014
mtps_version: v=office.15
ms.openlocfilehash: ab245fc0ff9b60862cebe57fbb2d996735442b89
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25405870"
---
# <a name="find-a-specific-appointment-in-a-recurring-appointment-series"></a>Поиск определенной встречи в серии повторяющихся встреч

В этом примере показывается способ получения объекта [AppointmentItem](https://msdn.microsoft.com/library/bb645611\(v=office.15\)), который представляет конкретную встречу в серии повторяющихся встреч.

## <a name="example"></a>Пример

> [!NOTE] 
> Приведенный ниже пример кода представляет собой фрагмент из книги [Программирование приложений для Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).

Чтобы найти экземпляр повторяющейся встречи, которая происходит в определенную дату и в определенное время, следует использовать метод [GetOccurrence(DateTime)](https://msdn.microsoft.com/library/bb622806\(v=office.15\)) объекта [RecurrencePattern](https://msdn.microsoft.com/library/bb608903\(v=office.15\)) для получения объекта **AppointmentItem**. 

При работе с элементами повторяющейся встречи следует удалить все предыдущие ссылки, получить новые ссылки на элемент повторяющейся встречи перед обращением к элементу или его изменением и удалить эти ссылки сразу после завершения работы и сохранения изменений. Такой подход применяется к повторяющемуся объекту **AppointmentItem** и любому объекту [Exception](https://msdn.microsoft.com/library/bb610440\(v=office.15\)) или [RecurrencePattern](https://msdn.microsoft.com/library/bb608903\(v=office.15\)). Чтобы удалить ссылку в Visual Basic, установите для существующего объекта значение Nothing. В C\# явным образом освободите память для этого объекта.

Следует отметить, что даже после удаления ссылок при попытке получения новой ссылки, когда имеется активная ссылка (удерживаемая другой надстройкой в Outlook) на один из вышеупомянутых объектов, новая ссылка будет продолжать указывать на устаревшую копию объекта. Поэтому важно удалять ссылки сразу же по окончании работы с повторяющейся встречей.

В представленном ниже примере кода CheckOccurrenceExample использует повторяющуюся встречу, созданную в примере кода в статье [Создание встречи, которая повторяется по недельному расписанию](how-to-create-a-recurring-appointment-that-has-a-weekly-pattern.md). Затем вызывается метод GetOccurrence, чтобы определить, начинается ли повторяющаяся встреча в определенную дату и время. Чтобы гарантировать продолжение выполнения процедуры, даже если предоставленные сведения не соответствуют дате начала и времени вхождения повторяющейся встречи, в примере используется блок try…catch. После вызова метода GetOccurrence для каждой встречи в серии процедура CheckOccurrenceExample проверяет переменную singleAppt, чтобы определить, является ли она пустой ссылкой (это указывает на сбой метода и на то, что объект **AppointmentItem** не был получен).

Если вы используете Visual Studio для тестирования этого примера кода, сначала добавьте ссылку на компонент Microsoft Outlook 15.0 Object Library и задайте переменную Outlook при импорте пространства имен **Microsoft.Office.Interop.Outlook**. Инструкция **using** не должна идти непосредственно перед функциями в примере кода, но ее нужно добавить перед объявлением public Class. В следующей строке кода показано, как выполнить импорт и назначение в C\#.

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```

```csharp
private void CheckOccurrenceExample()
{
    Outlook.AppointmentItem appt = Application.Session.
        GetDefaultFolder(Outlook.OlDefaultFolders.olFolderCalendar).
        Items.Find(
        "[Subject]='Recurring Appointment DaysOfWeekMask Example'")
        as Outlook.AppointmentItem;
    if (appt != null)
    {
        try
        {
            Outlook.RecurrencePattern pattern =
                appt.GetRecurrencePattern();
            Outlook.AppointmentItem singleAppt =
                pattern.GetOccurrence(DateTime.Parse(
                "7/21/2006 2:00 PM"))
                as Outlook.AppointmentItem;
            if (singleAppt != null)
            {
                Debug.WriteLine("7/21/2006 2:00 PM occurrence found.");
            }
        }
        catch (Exception ex)
        {
            Debug.WriteLine(ex.Message);
        }
    }
}
```

## <a name="see-also"></a>См. также

- [Встречи](appointments.md)


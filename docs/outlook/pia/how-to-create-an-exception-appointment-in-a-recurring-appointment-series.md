---
title: Создание встречи-исключения в серии повторяющихся встреч
TOCTitle: Create an exception appointment in a recurring appointment series
ms:assetid: b7cd0975-4f44-453a-b878-ec55feeedc4e
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184635(v=office.15)
ms:contentKeyID: 55119813
ms.date: 07/24/2014
mtps_version: v=office.15
ms.openlocfilehash: 1344188ad8947245ec0a6d54efff603b9e7755e7
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25405982"
---
# <a name="create-an-exception-appointment-in-a-recurring-appointment-series"></a>Создание встречи-исключения в серии повторяющихся встреч

В этом примере создается исключение из стандартного шаблона повтора встреч с помощью объекта [Exception](https://msdn.microsoft.com/library/bb610440\(v=office.15\)).

## <a name="example"></a>Пример

> [!NOTE] 
> Приведенный ниже пример кода представляет собой фрагмент из книги [Программирование приложений для Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).

После удаления или изменения одного экземпляра повторяющейся встречи Outlook создает объект [Exception](https://msdn.microsoft.com/library/bb610440\(v=office.15\)). Объект Exception позволяет создавать исключение из стандартного шаблона повторения. Свойства объекта содержат изменения, внесенные в экземпляр встречи. Коллекция [Exceptions](https://msdn.microsoft.com/library/bb647601\(v=office.15\)) содержит все объекты Exception повторяющейся встречи и связана с объектом [RecurrencePattern](https://msdn.microsoft.com/library/bb608903\(v=office.15\)) встречи.

Чтобы получить объект [AppointmentItem](https://msdn.microsoft.com/library/bb645611\(v=office.15\)), представляющий исключение из исходного шаблона повторения повторяющейся встречи, используйте свойство [AppointmentItem](https://msdn.microsoft.com/library/bb645648\(v=office.15\)) объекта Exception. С помощью методов и свойств возвращенного объекта AppointmentItem можно задать свойства для исключения из встреч.

При работе с элементами повторяющейся встречи следует удалить все предыдущие ссылки, получить новые ссылки на элемент повторяющейся встречи перед обращением к элементу или его изменением и удалить эти ссылки сразу после завершения работы и сохранения изменений. Такой подход применяется к повторяющемуся объекту **AppointmentItem** и любому объекту [Exception](https://msdn.microsoft.com/library/bb610440\(v=office.15\)) или [RecurrencePattern](https://msdn.microsoft.com/library/bb608903\(v=office.15\)). Чтобы удалить ссылку в Visual Basic, установите для существующего объекта значение Nothing. В C\# явным образом удалите память для этого объекта.

Обратите внимание, что даже после высвобождения ссылки и попытки получения новой ссылки, если по-прежнему существует активная ссылка на любой из вышеупомянутых объектов, удерживаемая другой надстройкой или приложением Outlook, новая ссылка будет указывать на устаревшую копию объекта. В связи с этим важно высвобождать ссылки немедленно после завершения текущей встречи.

В следующем примере кода CreateExceptionExample изменяет тему повторяющейся встречи, которая создана в разделе [Поиск определенной встречи в серии повторяющихся встреч](how-to-find-a-specific-appointment-in-a-recurring-appointment-series.md), а затем использует свойство AppointmentItem полученного в результате объекта Exception, чтобы получить AppointmentItem, соответствующее исключению из встреч. Затем CreateExceptionExample изменяет время начала и окончания для исключения из встреч.

Если вы используете Visual Studio для тестирования этого примера кода, сначала добавьте ссылку на компонент Microsoft Outlook 15.0 Object Library и задайте переменную Outlook при импорте пространства имен **Microsoft.Office.Interop.Outlook**. Инструкция **using** не должна идти непосредственно перед функциями в примере кода, но ее нужно добавить перед открытым объявлением Class. В следующей строке кода показано, как выполнить импорт и назначение в C\#.

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```

```csharp
private void CreateExceptionExample()
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
            Outlook.AppointmentItem myInstance =
                pattern.GetOccurrence(DateTime.Parse(
                "7/21/2006 2:00 PM"))
                as Outlook.AppointmentItem;
            if (myInstance != null)
            {
                myInstance.Subject = "My Exception";
                myInstance.Save();
                Outlook.RecurrencePattern newPattern =
                    appt.GetRecurrencePattern();
                Outlook.Exception myException =
                    newPattern.Exceptions[1];
                if (myException != null)
                {
                    Outlook.AppointmentItem myNewInstance =
                        myException.AppointmentItem;
                    myNewInstance.Start =
                        DateTime.Parse("7/21/2006 1:00 PM");
                    myNewInstance.End =
                        DateTime.Parse("7/21/2006 2:00 PM");
                    myNewInstance.Save();
                }
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


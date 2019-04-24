---
title: Создание напоминания для элемента встречи
TOCTitle: Create a reminder for an appointment item
ms:assetid: 85e772f0-65ac-4abc-8286-9099882a2400
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184623(v=office.15)
ms:contentKeyID: 55119814
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 1f5f31c480f31b01e53fec9651c8154765b581a3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32349499"
---
# <a name="create-a-reminder-for-an-appointment-item"></a>Создание напоминания для элемента встречи

В этом примере показано, как использовать свойство [ReminderSet](https://msdn.microsoft.com/library/bb624262\(v=office.15\)), чтобы создать напоминание для элемента встречи.

## <a name="example"></a>Пример

> [!NOTE] 
> Приведенный ниже пример кода представляет собой фрагмент из книги [Программирование приложений для Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).


Outlook предоставляет способ создать напоминание о встрече, используя свойство [ReminderSet](https://msdn.microsoft.com/library/bb624262\(v=office.15\)) объекта [AppointmentItem](https://msdn.microsoft.com/library/bb645611\(v=office.15\)). Это свойство указывает, создано ли напоминание о встрече. Задание для свойства ReminderSet значения true создает напоминание, а задание значения false удаляет напоминание.

В следующем примере кода ReminderExample создает напоминание о закрытой встрече для дегустации вина в Напе (Калифорния) и определяет, что напоминание должно появиться за два часа до начала мероприятия. Сначала ReminderExample создает объект Outlook **AppointmentItem**. Затем свойство [Sensitivity](https://msdn.microsoft.com/library/bb623503\(v=office.15\)) для элемента устанавливается равным [olPrivate](https://msdn.microsoft.com/library/bb645125\(v=office.15\)). Это означает, что это личная встреча. После задания других свойств встречи, таких как времена [Start](https://msdn.microsoft.com/library/bb647263\(v=office.15\)) и [End](https://msdn.microsoft.com/library/bb623715\(v=office.15\)), ReminderExample устанавливает свойство [ReminderMinutesBeforeStart](https://msdn.microsoft.com/library/bb644528\(v=office.15\)), чтобы показать число минут, определяющих, за какое время до начала встречи будет появляться напоминание. В этом случае для свойства ReminderMinutesBeforeStart установлено значение 120 минут (два часа).

Если вы используете Visual Studio для тестирования этого примера кода, сначала добавьте ссылку на компонент Microsoft Outlook 15.0 Object Library и задайте переменную Outlook при импорте пространства имен **Microsoft.Office.Interop.Outlook**. Инструкция **using** не должна находиться непосредственно перед функциями в примере кода, но ее нужно добавить перед объявлением общедоступного класса. В приведенной ниже строке кода показано, как выполнить импорт и назначение на языке C\#.

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```

```csharp
private void ReminderExample()
{
    Outlook.AppointmentItem appt = Application.CreateItem(
        Outlook.OlItemType.olAppointmentItem)
        as Outlook.AppointmentItem;
    appt.Subject = "Wine Tasting";
    appt.Location = "Napa CA";
    appt.Sensitivity = Outlook.OlSensitivity.olPrivate;
    appt.Start = DateTime.Parse("10/21/2006 10:00 AM");
    appt.End = DateTime.Parse("10/21/2006 3:00 PM");
    appt.ReminderSet = true;
    appt.ReminderMinutesBeforeStart = 120;
    appt.Save();
}
```

## <a name="see-also"></a>См. также

- [Встречи](appointments.md)


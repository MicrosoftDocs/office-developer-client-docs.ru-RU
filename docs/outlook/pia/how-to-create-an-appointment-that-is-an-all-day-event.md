---
title: Создание встречи как события на целый день
TOCTitle: Create an appointment that is an all-day event
ms:assetid: a0d3baeb-6ed5-41b6-bef5-d6c1bb56fee3
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184629(v=office.15)
ms:contentKeyID: 55119806
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: b5065395afe39247f8113bc5223b0e3e403a02fa
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28710827"
---
# <a name="create-an-appointment-that-is-an-all-day-event"></a>Создание встречи как события на целый день

В этом примере показано создание встречи длительностью в целый день с помощью свойства [AllDayEvent](https://msdn.microsoft.com/library/bb610279\(v=office.15\)).

## <a name="example"></a>Пример

> [!NOTE] 
> Приведенный ниже пример кода взят из книги [Программирование приложений для Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).

Событие отличается от обычной встречи, поскольку это действие продолжается 24 часа и более. В качестве примеров событий можно назвать ярмарки, семинары или каникулы. События и ежегодные события не вызывают появление занятых временных блоков в календаре пользователя. Вместо этого они появляются в виде баннеров. Баннеры отображаются над просматриваемым днем или неделей в календаре. Если событие продолжается весь день, то время пользователя по умолчанию выглядит занятым при просмотре другими людьми. Однако если речь идет о событии или ежегодном событии, время пользователя отображается свободным.

Чтобы создать событие на весь день программным методом, присвойте свойству [AllDayEvent](https://msdn.microsoft.com/library/bb610279\(v=office.15\)) объекта [AppointmentItem](https://msdn.microsoft.com/library/bb645611\(v=office.15\)) значение true. Затем задайте свойства [Start](https://msdn.microsoft.com/library/bb647263\(v=office.15\)) и [End](https://msdn.microsoft.com/library/bb623715\(v=office.15\)) для AppointmentItem. Если свойству AllDayEvent присвоено значение true, а свойства Start и End не заданы, событие произойдет сегодня и оно будет выглядеть как мероприятие, отмеченное в вашем календаре статусом "занято". Необходимо задать свойства Start и End, если нужно, чтобы событие происходило в будущем.

> [!NOTE]
> Чтобы сделать встречу событием на целый день, необходимо присвоить свойству Start значение 00:00 (полночь) для дня начала события, а свойству End — значение 00:00 для следующего дня после завершения события. Если значение Start или End не установлено на 00:00, встреча станет многодневной вместо события на целый день. 
>
> Например, если продолжительность события только один день, присвойте свойству Start значение 00:00 для дня начала события, а свойству End — значение 00:00 для следующего дня. Свойству End всегда следует присваивать значение 00:00 на дату, превосходящую дату начала на один день.

В следующем примере кода свойство AllDayEventExample создает событие на весь день, которое начинается 11 июня 2007 г. и заканчивается 15 июня 2007 г. Обратите внимание, что свойству End этой встречи присвоено значение 00:00 16 июня 2007 г.

Если вы используете Visual Studio для тестирования этого примера кода, сначала добавьте ссылку на компонент Microsoft Outlook 15.0 Object Library и задайте переменную Outlook при импорте пространства имен **Microsoft.Office.Interop.Outlook**. Не следует использовать инструкцию **using** непосредственно перед функциями в примере кода, но ее необходимо добавить перед объявлением общедоступного класса. В следующей строке кода показано, как выполнить импорт и назначение в C\#.

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```

```csharp
private void AllDayEventExample()
{
    Outlook.AppointmentItem appt = Application.CreateItem(
        Outlook.OlItemType.olAppointmentItem)
        as Outlook.AppointmentItem;
    appt.Subject = "Developer's Conference";
    appt.AllDayEvent = true;
    appt.Start = DateTime.Parse("6/11/2007 12:00 AM");
    appt.End = DateTime.Parse("6/16/2007 12:00 AM");
    appt.Display(false);
}
```

## <a name="see-also"></a>См. также

- [Встречи](appointments.md)


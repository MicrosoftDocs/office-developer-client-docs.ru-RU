---
title: Создание встречи как события на целый день
TOCTitle: Create an appointment that is an all-day event
ms:assetid: a0d3baeb-6ed5-41b6-bef5-d6c1bb56fee3
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184629(v=office.15)
ms:contentKeyID: 55119806
ms.date: 07/24/2014
mtps_version: v=office.15
ms.openlocfilehash: 79bffb9185db43395df7254bc353ac24b65d717a
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25405940"
---
# <a name="create-an-appointment-that-is-an-all-day-event"></a><span data-ttu-id="62918-102">Создание встречи как события на целый день</span><span class="sxs-lookup"><span data-stu-id="62918-102">Uses the AllDayEvent property to create an appointment that is an all-day event.</span></span>

<span data-ttu-id="62918-103">В этом примере показано создание встречи длительностью в целый день с помощью свойства [AllDayEvent](https://msdn.microsoft.com/library/bb610279\(v=office.15\)).</span><span class="sxs-lookup"><span data-stu-id="62918-103">This example shows how use the [AllDayEvent](https://msdn.microsoft.com/library/bb610279\(v=office.15\)) property to create an appointment that is an all-day event.</span></span>

## <a name="example"></a><span data-ttu-id="62918-104">Пример</span><span class="sxs-lookup"><span data-stu-id="62918-104">Example</span></span>

> [!NOTE] 
> <span data-ttu-id="62918-105">Приведенный ниже пример кода взят из книги [Программирование приложений для Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).</span><span class="sxs-lookup"><span data-stu-id="62918-105">The following code example is an excerpt from  [Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493)  , from Microsoft Press (ISBN 9780735622494, copyright Microsoft Press 2007, all rights reserved).</span></span>

<span data-ttu-id="62918-p101">Событие отличается от обычной встречи, поскольку это действие продолжается 24 часа и более. В качестве примеров событий можно назвать ярмарки, семинары или каникулы. События и ежегодные события не вызывают появление занятых временных блоков в календаре пользователя. Вместо этого они появляются в виде баннеров. Баннеры отображаются над просматриваемым днем или неделей в календаре. Если событие продолжается весь день, то время пользователя по умолчанию выглядит занятым при просмотре другими людьми. Однако если речь идет о событии или ежегодном событии, время пользователя отображается свободным.</span><span class="sxs-lookup"><span data-stu-id="62918-p101">An event is different from a regular appointment because it is an activity that lasts 24 hours or longer. Examples of events include trade shows, seminars, or vacations. Events and annual events do not appear as occupied blocks of time in the user’s calendar. Instead, they appear as banners. You can see the banners at the top of a calendar day or week view. For an all-day appointment, by default, the user’s time is displayed as busy when viewed by other people, but the user’s time is displayed as free for an event or annual event.</span></span>

<span data-ttu-id="62918-112">Чтобы создать событие на весь день программным методом, присвойте свойству [AllDayEvent](https://msdn.microsoft.com/library/bb610279\(v=office.15\)) объекта [AppointmentItem](https://msdn.microsoft.com/library/bb645611\(v=office.15\)) значение true.</span><span class="sxs-lookup"><span data-stu-id="62918-112">To create an all-day event programmatically, set the AllDayEvent property of the AppointmentItem object to true.</span></span> <span data-ttu-id="62918-113">Затем задайте свойства [Start](https://msdn.microsoft.com/library/bb647263\(v=office.15\)) и [End](https://msdn.microsoft.com/library/bb623715\(v=office.15\)) для AppointmentItem.</span><span class="sxs-lookup"><span data-stu-id="62918-113">Then set the Start and End properties of the AppointmentItem.</span></span> <span data-ttu-id="62918-114">Если свойству AllDayEvent присвоено значение true, а свойства Start и End не заданы, событие произойдет сегодня и оно будет выглядеть как мероприятие, отмеченное в вашем календаре статусом "занято".</span><span class="sxs-lookup"><span data-stu-id="62918-114">If you set the AllDayEvent property to true and do not set the Start and End properties, the event will occur today, and it will be an appointment, showing a busy status on your calendar.</span></span> <span data-ttu-id="62918-115">Необходимо задать свойства Start и End, если нужно, чтобы событие происходило в будущем.</span><span class="sxs-lookup"><span data-stu-id="62918-115">You must set the Start and End properties if you want the event to occur on a future date.</span></span>

> [!NOTE]
> <span data-ttu-id="62918-116">Чтобы сделать встречу событием на целый день, необходимо присвоить свойству Start значение 00:00</span><span class="sxs-lookup"><span data-stu-id="62918-116">To make the appointment an all-day event, you must set the Start property to 12:00 A.M.</span></span> <span data-ttu-id="62918-117">(полночь) для дня начала события, а свойству End — значение 00:00</span><span class="sxs-lookup"><span data-stu-id="62918-117">(midnight) on the day you want the event to begin, and set End property to 12:00 A.M.</span></span> <span data-ttu-id="62918-118">для следующего дня после завершения события.</span><span class="sxs-lookup"><span data-stu-id="62918-118">on the day after you want the event to end.</span></span> <span data-ttu-id="62918-119">Если значение Start или End не установлено на 00:00, встреча станет многодневной вместо события на целый день.</span><span class="sxs-lookup"><span data-stu-id="62918-119">If you set the Start or End time to a date and time value other than 12:00 A.M., the appointment will become a multiday appointment instead of an all-day event.</span></span> 
>
> <span data-ttu-id="62918-120">Например, если продолжительность события только один день, присвойте свойству Start значение 00:00</span><span class="sxs-lookup"><span data-stu-id="62918-120">For example, if your event duration is only one day, set the Start property to 12:00 A.M.</span></span> <span data-ttu-id="62918-121">для дня начала события, а свойству End — значение 00:00</span><span class="sxs-lookup"><span data-stu-id="62918-121">on the day you want the event to begin, and set the End property to 12:00 A.M.</span></span> <span data-ttu-id="62918-122">для следующего дня.</span><span class="sxs-lookup"><span data-stu-id="62918-122">on the following day.</span></span> <span data-ttu-id="62918-123">Свойству End всегда следует присваивать значение 00:00</span><span class="sxs-lookup"><span data-stu-id="62918-123">You should always set the End property to 12:00 A.M.</span></span> <span data-ttu-id="62918-124">на дату, превосходящую дату начала на один день.</span><span class="sxs-lookup"><span data-stu-id="62918-124">on a date that is more than one day after the start date.</span></span>

<span data-ttu-id="62918-p105">В следующем примере кода свойство AllDayEventExample создает событие на весь день, которое начинается 11 июня 2007 г. и заканчивается 15 июня 2007 г. Обратите внимание, что свойству End этой встречи присвоено значение 00:00 16 июня 2007 г.</span><span class="sxs-lookup"><span data-stu-id="62918-p105">In the following code example, AllDayEventExample creates an all-day event that begins on June 11, 2007, and ends on June 15, 2007. Note that the End property for the appointment is set to 12:00 A.M. on June 16, 2007.</span></span>

<span data-ttu-id="62918-128">Если вы используете Visual Studio для тестирования этого примера кода, сначала добавьте ссылку на компонент Microsoft Outlook 15.0 Object Library и задайте переменную Outlook при импорте пространства имен **Microsoft.Office.Interop.Outlook**.</span><span class="sxs-lookup"><span data-stu-id="62918-128">If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the   variable when you import the Microsoft.Office.Interop.Outlook namespace.</span></span> <span data-ttu-id="62918-129">Не следует использовать инструкцию **using** непосредственно перед функциями в примере кода, но ее необходимо добавить перед объявлением общедоступного класса.</span><span class="sxs-lookup"><span data-stu-id="62918-129">The using statement must not occur directly before the functions in the code example but must be added before the public   declaration.</span></span> <span data-ttu-id="62918-130">В следующей строке кода показано, как выполнить импорт и назначение в C\#.</span><span class="sxs-lookup"><span data-stu-id="62918-130">The following line of code shows how to do the import and assignment in C#.</span></span>

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

## <a name="see-also"></a><span data-ttu-id="62918-131">См. также</span><span class="sxs-lookup"><span data-stu-id="62918-131">See also</span></span>

- [<span data-ttu-id="62918-132">Встречи</span><span class="sxs-lookup"><span data-stu-id="62918-132">Appointments</span></span>](appointments.md)


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
# <a name="create-a-recurring-appointment-by-using-the-default-recurrence-pattern"></a><span data-ttu-id="cdbec-102">Создание повторяющейся встречи с использованием установленного по умолчанию шаблона повтора</span><span class="sxs-lookup"><span data-stu-id="cdbec-102">Create a recurring appointment by using the default recurrence pattern</span></span>

<span data-ttu-id="cdbec-103">В этом примере показывается создание повторяющейся встречи с помощью шаблона повторения по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="cdbec-103">This example shows how to create a recurring appointment by using the default recurrence pattern.</span></span>

## <a name="example"></a><span data-ttu-id="cdbec-104">Пример</span><span class="sxs-lookup"><span data-stu-id="cdbec-104">Example</span></span>

> [!NOTE] 
> <span data-ttu-id="cdbec-105">Приведенный ниже пример кода взят из книги [Программирование приложений для Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).</span><span class="sxs-lookup"><span data-stu-id="cdbec-105">The following code example is an excerpt from [Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).</span></span>


<span data-ttu-id="cdbec-106">При создании встречи в Outlook создается объект [AppointmentItem](https://msdn.microsoft.com/library/bb645611\(v=office.15\)).</span><span class="sxs-lookup"><span data-stu-id="cdbec-106">When you create an appointment in Outlook, you are creating an [AppointmentItem](https://msdn.microsoft.com/library/bb645611\(v=office.15\)) object.</span></span> <span data-ttu-id="cdbec-107">Встреча является повторяющейся, если свойству [IsRecurring](https://msdn.microsoft.com/library/bb609491\(v=office.15\)) объекта AppointmentItem присвоено значение true.</span><span class="sxs-lookup"><span data-stu-id="cdbec-107">Your appointment is a recurring appointment if the [IsRecurring](https://msdn.microsoft.com/library/bb609491\(v=office.15\)) property of the AppointmentItem is set to true.</span></span> <span data-ttu-id="cdbec-108">Значение IsRecurring нельзя задать напрямую.</span><span class="sxs-lookup"><span data-stu-id="cdbec-108">IsRecurring cannot be set directly.</span></span> 

<span data-ttu-id="cdbec-109">Но можно создать повторяющуюся встречу с помощью объекта [RecurrencePattern](https://msdn.microsoft.com/library/bb608903\(v=office.15\)).</span><span class="sxs-lookup"><span data-stu-id="cdbec-109">However, you can create a recurring appointment by using the [RecurrencePattern](https://msdn.microsoft.com/library/bb608903\(v=office.15\)) object.</span></span> <span data-ttu-id="cdbec-110">Чтобы программно создать повторяющуюся встречу, создайте объект **AppointmentItem**, вызовите метод [GetRecurrencePattern()](https://msdn.microsoft.com/library/bb652582\(v=office.15\)) объекта **AppointmentItem** и сохраните объект **AppointmentItem**.</span><span class="sxs-lookup"><span data-stu-id="cdbec-110">To create a recurring appointment programmatically, create an **AppointmentItem** object, call the [GetRecurrencePattern()](https://msdn.microsoft.com/library/bb652582\(v=office.15\)) method of the **AppointmentItem** object, and then save the **AppointmentItem** object.</span></span> <span data-ttu-id="cdbec-111">Это создает встречу, использующую шаблон повторения по умолчанию, которая происходит еженедельно (в день недели, для которого она создана) и не имеет даты окончания.</span><span class="sxs-lookup"><span data-stu-id="cdbec-111">This creates an appointment that uses the default recurrence pattern, which occurs weekly on the day of the week for which the appointment was created, and has no end date.</span></span> <span data-ttu-id="cdbec-112">Объект RecurrencePattern позволяет создавать повторяющиеся встречи с указанными интервалами: ежедневные, еженедельные, ежемесячные или ежегодные.</span><span class="sxs-lookup"><span data-stu-id="cdbec-112">The RecurrencePattern object allows you to create recurring appointments at specified intervals—daily, weekly, monthly, or yearly.</span></span> <span data-ttu-id="cdbec-113">Если не указать интервалы для объекта RecurrencePattern, Outlook будет использовать шаблон повторения по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="cdbec-113">If you do not specify intervals for the RecurrencePattern object, Outlook will use the default recurrence pattern.</span></span>

<span data-ttu-id="cdbec-114">При работе с элементами повторяющейся встречи следует удалить все предыдущие ссылки, получить новые ссылки на элемент повторяющейся встречи перед обращением к элементу или его изменением и удалить эти ссылки сразу после завершения работы и сохранения изменений.</span><span class="sxs-lookup"><span data-stu-id="cdbec-114">When you work with recurring appointment items, you should release any prior references, obtain new references to the recurring appointment item before you access or modify the item, and release these references as soon as you are finished and have saved the changes.</span></span> <span data-ttu-id="cdbec-115">Такой подход применяется к повторяющемуся объекту **AppointmentItem** и любому объекту [Exception](https://msdn.microsoft.com/library/bb610440\(v=office.15\)) или [RecurrencePattern](https://msdn.microsoft.com/library/bb608903\(v=office.15\)).</span><span class="sxs-lookup"><span data-stu-id="cdbec-115">This practice applies to the recurring **AppointmentItem** object, and any [Exception](https://msdn.microsoft.com/library/bb610440\(v=office.15\)) or [RecurrencePattern](https://msdn.microsoft.com/library/bb608903\(v=office.15\)) object.</span></span> <span data-ttu-id="cdbec-116">Чтобы удалить ссылку в Visual Basic, установите для существующего объекта значение Nothing.</span><span class="sxs-lookup"><span data-stu-id="cdbec-116">To release a reference in Visual Basic, set that existing object to Nothing.</span></span> <span data-ttu-id="cdbec-117">В C\# явным образом освободите память для этого объекта.</span><span class="sxs-lookup"><span data-stu-id="cdbec-117">In C\#, explicitly release the memory for that object.</span></span>

<span data-ttu-id="cdbec-p104">Следует отметить, что даже после удаления ссылок при попытке получения новой ссылки, когда имеется активная ссылка (удерживаемая другой надстройкой в Outlook) на один из вышеупомянутых объектов, новая ссылка будет продолжать указывать на устаревшую копию объекта. Поэтому важно удалять ссылки сразу же по окончании работы с повторяющейся встречей.</span><span class="sxs-lookup"><span data-stu-id="cdbec-p104">Note that even after you release your reference and attempt to obtain a new reference, if there is still an active reference (held by another add-in or Outlook) to one of the above objects, your new reference will still point to an out-of-date copy of the object. Therefore, it is important that you release your references as soon as you are finished with the recurring appointment.</span></span>

<span data-ttu-id="cdbec-120">В приведенном ниже примере метод CreateRecurringAppointment создает объект **AppointmentItem**.</span><span class="sxs-lookup"><span data-stu-id="cdbec-120">In the following example, CreateRecurringAppointment creates an **AppointmentItem** object.</span></span> <span data-ttu-id="cdbec-121">Затем вызывается метод GetRecurrencePattern.</span><span class="sxs-lookup"><span data-stu-id="cdbec-121">It then calls GetRecurrencePattern.</span></span> <span data-ttu-id="cdbec-122">Метод GetRecurrencePattern возвращает объект RecurrencePattern, и сохраняется объект AppointmentItem.</span><span class="sxs-lookup"><span data-stu-id="cdbec-122">GetRecurrencePattern returns a RecurrencePattern object, and the AppointmentItem is saved.</span></span> <span data-ttu-id="cdbec-123">При этом создается повторяющаяся встреча с использованием установленного по умолчанию шаблона повтора.</span><span class="sxs-lookup"><span data-stu-id="cdbec-123">This creates a recurring appointment that uses the default recurrence pattern.</span></span>

<span data-ttu-id="cdbec-124">Если вы используете Visual Studio для тестирования этого примера кода, сначала добавьте ссылку на компонент Microsoft Outlook 15.0 Object Library и задайте переменную Outlook при импорте пространства имен **Microsoft.Office.Interop.Outlook**.</span><span class="sxs-lookup"><span data-stu-id="cdbec-124">If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the Outlook variable when you import the **Microsoft.Office.Interop.Outlook** namespace.</span></span> <span data-ttu-id="cdbec-125">Инструкция **using** не должна находиться непосредственно перед функциями в примере кода, но ее нужно добавить перед объявлением общедоступного класса.</span><span class="sxs-lookup"><span data-stu-id="cdbec-125">The **using** statement must not occur directly before the functions in the code example but must be added before the public Class declaration.</span></span> <span data-ttu-id="cdbec-126">В приведенной ниже строке кода показано, как выполнить импорт и назначение на языке C\#.</span><span class="sxs-lookup"><span data-stu-id="cdbec-126">The following line of code shows how to do the import and assignment in C\#.</span></span>

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

## <a name="see-also"></a><span data-ttu-id="cdbec-127">См. также</span><span class="sxs-lookup"><span data-stu-id="cdbec-127">See also</span></span>

- [<span data-ttu-id="cdbec-128">Встречи</span><span class="sxs-lookup"><span data-stu-id="cdbec-128">Appointments</span></span>](appointments.md)


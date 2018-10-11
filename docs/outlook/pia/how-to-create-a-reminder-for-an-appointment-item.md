---
title: Создание напоминания для элемента встречи
TOCTitle: Create a reminder for an appointment item
ms:assetid: 85e772f0-65ac-4abc-8286-9099882a2400
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184623(v=office.15)
ms:contentKeyID: 55119814
ms.date: 07/24/2014
mtps_version: v=office.15
ms.openlocfilehash: 164e744e03ab0984265736673c71d2d0bf57bf45
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25405975"
---
# <a name="create-a-reminder-for-an-appointment-item"></a><span data-ttu-id="2ddea-102">Создание напоминания для элемента встречи</span><span class="sxs-lookup"><span data-stu-id="2ddea-102">Create a reminder for an appointment item</span></span>

<span data-ttu-id="2ddea-103">В этом примере показано, как использовать свойство [ReminderSet](https://msdn.microsoft.com/library/bb624262\(v=office.15\)), чтобы создать напоминание для элемента встречи.</span><span class="sxs-lookup"><span data-stu-id="2ddea-103">This example shows how to use the [ReminderSet](https://msdn.microsoft.com/library/bb624262\(v=office.15\)) property to create a reminder for an appointment item.</span></span>

## <a name="example"></a><span data-ttu-id="2ddea-104">Пример</span><span class="sxs-lookup"><span data-stu-id="2ddea-104">Example</span></span>

> [!NOTE] 
> <span data-ttu-id="2ddea-105">Приведенный ниже пример кода представляет собой фрагмент из книги [Программирование приложений для Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).</span><span class="sxs-lookup"><span data-stu-id="2ddea-105">The following code example is an excerpt from  [Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493)  , from Microsoft Press (ISBN 9780735622494, copyright Microsoft Press 2007, all rights reserved).</span></span>


<span data-ttu-id="2ddea-106">Outlook предоставляет способ создать напоминание о встрече, используя свойство [ReminderSet](https://msdn.microsoft.com/library/bb624262\(v=office.15\)) объекта [AppointmentItem](https://msdn.microsoft.com/library/bb645611\(v=office.15\)).</span><span class="sxs-lookup"><span data-stu-id="2ddea-106">Microsoft Outlook provides a way to set a reminder for an appointment by using the [ReminderSet](https://msdn.microsoft.com/library/bb624262\(v=office.15\)) property of the [AppointmentItem](https://msdn.microsoft.com/library/bb645611\(v=office.15\)) object.</span></span> <span data-ttu-id="2ddea-107">Это свойство указывает, создано ли напоминание о встрече.</span><span class="sxs-lookup"><span data-stu-id="2ddea-107">This property indicates whether a reminder has been created for the appointment.</span></span> <span data-ttu-id="2ddea-108">Задание для свойства ReminderSet значения true создает напоминание, а задание значения false удаляет напоминание.</span><span class="sxs-lookup"><span data-stu-id="2ddea-108">Setting the ReminderSet property to true creates a reminder, and setting it to false removes the reminder.</span></span>

<span data-ttu-id="2ddea-109">В следующем примере кода ReminderExample создает напоминание о закрытой встрече для дегустации вина в Напе (Калифорния) и определяет, что напоминание должно появиться за два часа до начала мероприятия.</span><span class="sxs-lookup"><span data-stu-id="2ddea-109">In the following code example,   creates a reminder on a private appointment for wine tasting in Napa, California, and sets the reminder to occur two hours before the appointment starts.</span></span> <span data-ttu-id="2ddea-110">Сначала ReminderExample создает объект Outlook **AppointmentItem**.</span><span class="sxs-lookup"><span data-stu-id="2ddea-110">First,   creates an Outlook AppointmentItem object.</span></span> <span data-ttu-id="2ddea-111">Затем свойство [Sensitivity](https://msdn.microsoft.com/library/bb623503\(v=office.15\)) для элемента устанавливается равным [olPrivate](https://msdn.microsoft.com/library/bb645125\(v=office.15\)).</span><span class="sxs-lookup"><span data-stu-id="2ddea-111">It then sets the [Sensitivity](https://msdn.microsoft.com/library/bb623503\(v=office.15\)) property for the item to [olPrivate](https://msdn.microsoft.com/library/bb645125\(v=office.15\)) .</span></span> <span data-ttu-id="2ddea-112">Это означает, что это личная встреча.</span><span class="sxs-lookup"><span data-stu-id="2ddea-112">This indicates that the appointment is a private appointment.</span></span> <span data-ttu-id="2ddea-113">После задания других свойств встречи, таких как времена [Start](https://msdn.microsoft.com/library/bb647263\(v=office.15\)) и [End](https://msdn.microsoft.com/library/bb623715\(v=office.15\)), ReminderExample устанавливает свойство [ReminderMinutesBeforeStart](https://msdn.microsoft.com/library/bb644528\(v=office.15\)), чтобы показать число минут, определяющих, за какое время до начала встречи будет появляться напоминание.</span><span class="sxs-lookup"><span data-stu-id="2ddea-113">After setting other properties of the appointment, such as Start and End times,   sets the ReminderMinutesBeforeStart property to indicate the number of minutes that the reminder will appear before the start of the appointment.</span></span> <span data-ttu-id="2ddea-114">В этом случае для свойства ReminderMinutesBeforeStart установлено значение 120 минут (два часа).</span><span class="sxs-lookup"><span data-stu-id="2ddea-114">In this case, ReminderMinutesBeforeStart is set to 120 minutes (two hours).</span></span>

<span data-ttu-id="2ddea-115">Если вы используете Visual Studio для тестирования этого примера кода, сначала добавьте ссылку на компонент Microsoft Outlook 15.0 Object Library и задайте переменную Outlook при импорте пространства имен **Microsoft.Office.Interop.Outlook**.</span><span class="sxs-lookup"><span data-stu-id="2ddea-115">If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the   variable when you import the Microsoft.Office.Interop.Outlook namespace.</span></span> <span data-ttu-id="2ddea-116">Инструкция **using** не должна идти непосредственно перед функциями в примере кода, но ее нужно добавить перед открытым объявлением Class.</span><span class="sxs-lookup"><span data-stu-id="2ddea-116">The using statement must not occur directly before the functions in the code example but must be added before the public   declaration.</span></span> <span data-ttu-id="2ddea-117">В следующей строке кода показано, как выполнить импорт и назначение в C\#.</span><span class="sxs-lookup"><span data-stu-id="2ddea-117">The following line of code shows how to do the import and assignment in C#.</span></span>

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

## <a name="see-also"></a><span data-ttu-id="2ddea-118">См. также</span><span class="sxs-lookup"><span data-stu-id="2ddea-118">See also</span></span>

- [<span data-ttu-id="2ddea-119">Встречи</span><span class="sxs-lookup"><span data-stu-id="2ddea-119">Appointments</span></span>](appointments.md)


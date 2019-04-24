---
title: Создание встречи-исключения в серии повторяющихся встреч
TOCTitle: Create an exception appointment in a recurring appointment series
ms:assetid: b7cd0975-4f44-453a-b878-ec55feeedc4e
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184635(v=office.15)
ms:contentKeyID: 55119813
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 70e491069fd3f178371e9e8e3e6bcd8dc08e729e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32356436"
---
# <a name="create-an-exception-appointment-in-a-recurring-appointment-series"></a><span data-ttu-id="3bb82-102">Создание встречи-исключения в серии повторяющихся встреч</span><span class="sxs-lookup"><span data-stu-id="3bb82-102">Create an exception appointment in a recurring appointment series</span></span>

<span data-ttu-id="3bb82-103">В этом примере создается исключение из стандартного шаблона повтора встреч с помощью объекта [Exception](https://msdn.microsoft.com/library/bb610440\(v=office.15\)).</span><span class="sxs-lookup"><span data-stu-id="3bb82-103">This example uses an [Exception](https://msdn.microsoft.com/library/bb610440\(v=office.15\)) object to create an exception to a standard recurrence pattern for an appointment.</span></span>

## <a name="example"></a><span data-ttu-id="3bb82-104">Пример</span><span class="sxs-lookup"><span data-stu-id="3bb82-104">Example</span></span>

> [!NOTE] 
> <span data-ttu-id="3bb82-105">Приведенный ниже пример кода представляет собой фрагмент из книги [Программирование приложений для Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).</span><span class="sxs-lookup"><span data-stu-id="3bb82-105">The following code example is an excerpt from [Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).</span></span>

<span data-ttu-id="3bb82-106">После удаления или изменения одного экземпляра повторяющейся встречи Outlook создает объект [Exception](https://msdn.microsoft.com/library/bb610440\(v=office.15\)).</span><span class="sxs-lookup"><span data-stu-id="3bb82-106">Once you delete or change one appointment instance of a recurring appointment, Outlook creates an [Exception](https://msdn.microsoft.com/library/bb610440\(v=office.15\)) object.</span></span> <span data-ttu-id="3bb82-107">Объект Exception позволяет создавать исключение из стандартного шаблона повторения.</span><span class="sxs-lookup"><span data-stu-id="3bb82-107">The Exception object allows you to create an exception to a standard recurrence pattern.</span></span> <span data-ttu-id="3bb82-108">Свойства объекта содержат изменения, внесенные в экземпляр встречи.</span><span class="sxs-lookup"><span data-stu-id="3bb82-108">The object’s properties contain the changes that were made to the appointment instance.</span></span> <span data-ttu-id="3bb82-109">Коллекция [Exceptions](https://msdn.microsoft.com/library/bb647601\(v=office.15\)) содержит все объекты Exception повторяющейся встречи и связана с объектом [RecurrencePattern](https://msdn.microsoft.com/library/bb608903\(v=office.15\)) встречи.</span><span class="sxs-lookup"><span data-stu-id="3bb82-109">The [Exceptions](https://msdn.microsoft.com/library/bb647601\(v=office.15\)) collection contains all of the Exception objects for a recurring appointment, and is associated with the appointment’s [RecurrencePattern](https://msdn.microsoft.com/library/bb608903\(v=office.15\)) object.</span></span>

<span data-ttu-id="3bb82-110">Чтобы получить объект [AppointmentItem](https://msdn.microsoft.com/library/bb645611\(v=office.15\)), представляющий собой исключение из исходного шаблона повторения встречи, используйте свойство [AppointmentItem](https://msdn.microsoft.com/library/bb645648\(v=office.15\)) объекта Exception.</span><span class="sxs-lookup"><span data-stu-id="3bb82-110">To get the [AppointmentItem](https://msdn.microsoft.com/library/bb645611\(v=office.15\)) object that represents the exception to the original recurrence pattern of the recurring appointment, use the [AppointmentItem](https://msdn.microsoft.com/library/bb645648\(v=office.15\)) property of the Exception.</span></span> <span data-ttu-id="3bb82-111">С помощью методов и свойств возвращенного объекта AppointmentItem можно задать свойства для исключения из встреч.</span><span class="sxs-lookup"><span data-stu-id="3bb82-111">By using the methods and properties of the returned AppointmentItem, you can set the properties of the appointment exception.</span></span>

<span data-ttu-id="3bb82-112">При работе с элементами повторяющейся встречи следует удалить все предыдущие ссылки, получить новые ссылки на элемент повторяющейся встречи перед обращением к элементу или его изменением и удалить эти ссылки сразу после завершения работы и сохранения изменений.</span><span class="sxs-lookup"><span data-stu-id="3bb82-112">When you work with recurring appointment items, you should release any prior references, obtain new references to the recurring appointment item before you access or modify the item, and release these references as soon as you are finished and have saved the changes.</span></span> <span data-ttu-id="3bb82-113">Такой подход применяется к повторяющемуся объекту **AppointmentItem** и любому объекту [Exception](https://msdn.microsoft.com/library/bb610440\(v=office.15\)) или [RecurrencePattern](https://msdn.microsoft.com/library/bb608903\(v=office.15\)).</span><span class="sxs-lookup"><span data-stu-id="3bb82-113">This practice applies to the recurring **AppointmentItem** object, and any [Exception](https://msdn.microsoft.com/library/bb610440\(v=office.15\)) or [RecurrencePattern](https://msdn.microsoft.com/library/bb608903\(v=office.15\)) object.</span></span> <span data-ttu-id="3bb82-114">Чтобы удалить ссылку в Visual Basic, установите для существующего объекта значение Nothing.</span><span class="sxs-lookup"><span data-stu-id="3bb82-114">To release a reference in Visual Basic, set that existing object to Nothing.</span></span> <span data-ttu-id="3bb82-115">В C\# явным образом освободите память для этого объекта.</span><span class="sxs-lookup"><span data-stu-id="3bb82-115">In C\#, explicitly release the memory for that object.</span></span>

<span data-ttu-id="3bb82-p104">Обратите внимание, что даже после высвобождения ссылки и попытки получения новой ссылки, если по-прежнему существует активная ссылка на любой из вышеупомянутых объектов, удерживаемая другой надстройкой или приложением Outlook, новая ссылка будет указывать на устаревшую копию объекта. В связи с этим важно высвобождать ссылки немедленно после завершения текущей встречи.</span><span class="sxs-lookup"><span data-stu-id="3bb82-p104">Note that even after you release your reference and attempt to obtain a new reference, if there is still an active reference, held by another add-in or Outlook, to one of the above objects, your new reference will still point to an out-of-date copy of the object. Therefore, it is important that you release your references as soon as you are finished with the recurring appointment.</span></span>

<span data-ttu-id="3bb82-118">В следующем примере кода CreateExceptionExample изменяет тему повторяющейся встречи, которая была создана в разделе [Поиск определенной встречи в серии повторяющихся встреч](how-to-find-a-specific-appointment-in-a-recurring-appointment-series.md), а затем использует свойство AppointmentItem объекта Exception, чтобы получить AppointmentItem, соответствующий исключению.</span><span class="sxs-lookup"><span data-stu-id="3bb82-118">In the following code example, CreateExceptionExample changes the subject of the recurring appointment that was created in the topic [Find a Specific Appointment in a Recurring Appointment Series](how-to-find-a-specific-appointment-in-a-recurring-appointment-series.md), and then uses the AppointmentItem property of the resulting Exception object to retrieve the AppointmentItem that corresponds to the appointment exception.</span></span> <span data-ttu-id="3bb82-119">Затем CreateExceptionExample изменяет время начала и окончания для исключения.</span><span class="sxs-lookup"><span data-stu-id="3bb82-119">CreateExceptionExample then changes the start and end times of the appointment exception.</span></span>

<span data-ttu-id="3bb82-120">Если вы используете Visual Studio для тестирования этого примера кода, сначала добавьте ссылку на компонент Microsoft Outlook 15.0 Object Library и задайте переменную Outlook при импорте пространства имен **Microsoft.Office.Interop.Outlook**.</span><span class="sxs-lookup"><span data-stu-id="3bb82-120">If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the Outlook variable when you import the **Microsoft.Office.Interop.Outlook** namespace.</span></span> <span data-ttu-id="3bb82-121">Инструкция **using** не должна находиться непосредственно перед функциями в примере кода, но ее нужно добавить перед объявлением общедоступного класса.</span><span class="sxs-lookup"><span data-stu-id="3bb82-121">The **using** statement must not occur directly before the functions in the code example but must be added before the public Class declaration.</span></span> <span data-ttu-id="3bb82-122">В приведенной ниже строке кода показано, как выполнить импорт и назначение на языке C\#.</span><span class="sxs-lookup"><span data-stu-id="3bb82-122">The following line of code shows how to do the import and assignment in C\#.</span></span>

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

## <a name="see-also"></a><span data-ttu-id="3bb82-123">См. также</span><span class="sxs-lookup"><span data-stu-id="3bb82-123">See also</span></span>

- [<span data-ttu-id="3bb82-124">Встречи</span><span class="sxs-lookup"><span data-stu-id="3bb82-124">Appointments</span></span>](appointments.md)


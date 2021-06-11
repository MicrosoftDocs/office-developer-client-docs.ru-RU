---
title: Поиск определенной встречи в серии повторяющихся встреч
TOCTitle: Find a specific appointment in a recurring appointment series
ms:assetid: 01f55f04-7245-4325-a354-50a6eb270a31
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184586(v=office.15)
ms:contentKeyID: 55119812
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 19502895996d4777f2d1a6887aa80883a5398a09
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32320254"
---
# <a name="find-a-specific-appointment-in-a-recurring-appointment-series"></a><span data-ttu-id="66955-102">Поиск определенной встречи в серии повторяющихся встреч</span><span class="sxs-lookup"><span data-stu-id="66955-102">Find a specific appointment in a recurring appointment series</span></span>

<span data-ttu-id="66955-103">В этом примере показывается способ получения объекта [AppointmentItem](https://msdn.microsoft.com/library/bb645611\(v=office.15\)), который представляет конкретную встречу в серии повторяющихся встреч.</span><span class="sxs-lookup"><span data-stu-id="66955-103">This example shows how to return an [AppointmentItem](https://msdn.microsoft.com/library/bb645611\(v=office.15\)) object that represents a specific appointment in a recurring appointment series.</span></span>

## <a name="example"></a><span data-ttu-id="66955-104">Пример</span><span class="sxs-lookup"><span data-stu-id="66955-104">Example</span></span>

> [!NOTE] 
> <span data-ttu-id="66955-105">Приведенный ниже пример кода представляет собой фрагмент из книги [Программирование приложений для Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).</span><span class="sxs-lookup"><span data-stu-id="66955-105">The following code example is an excerpt from [Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).</span></span>

<span data-ttu-id="66955-106">Чтобы найти экземпляр повторяющейся встречи, которая происходит в определенную дату и в определенное время, следует использовать метод [GetOccurrence(DateTime)](https://msdn.microsoft.com/library/bb622806\(v=office.15\)) объекта [RecurrencePattern](https://msdn.microsoft.com/library/bb608903\(v=office.15\)) для получения объекта **AppointmentItem**. </span><span class="sxs-lookup"><span data-stu-id="66955-106">To find an instance of a recurring appointment that occurs at a specified date and time, use the [GetOccurrence(DateTime)](https://msdn.microsoft.com/library/bb622806\(v=office.15\)) method of the [RecurrencePattern](https://msdn.microsoft.com/library/bb608903\(v=office.15\)) object to return an **AppointmentItem** object.</span></span>

<span data-ttu-id="66955-107">При работе с элементами повторяющейся встречи следует удалить все предыдущие ссылки, получить новые ссылки на элемент повторяющейся встречи перед обращением к элементу или его изменением и удалить эти ссылки сразу после завершения работы и сохранения изменений.</span><span class="sxs-lookup"><span data-stu-id="66955-107">When you work with recurring appointment items, you should release any prior references, obtain new references to the recurring appointment item before you access or modify the item, and release these references as soon as you are finished and have saved the changes.</span></span> <span data-ttu-id="66955-108">Такой подход применяется к повторяющемуся объекту **AppointmentItem** и любому объекту [Exception](https://msdn.microsoft.com/library/bb610440\(v=office.15\)) или [RecurrencePattern](https://msdn.microsoft.com/library/bb608903\(v=office.15\)).</span><span class="sxs-lookup"><span data-stu-id="66955-108">This practice applies to the recurring **AppointmentItem** object, and any [Exception](https://msdn.microsoft.com/library/bb610440\(v=office.15\)) or [RecurrencePattern](https://msdn.microsoft.com/library/bb608903\(v=office.15\)) object.</span></span> <span data-ttu-id="66955-109">Чтобы удалить ссылку в Visual Basic, установите для существующего объекта значение Nothing.</span><span class="sxs-lookup"><span data-stu-id="66955-109">To release a reference in Visual Basic, set that existing object to Nothing.</span></span> <span data-ttu-id="66955-110">В C\# явным образом освободите память для этого объекта.</span><span class="sxs-lookup"><span data-stu-id="66955-110">In C\#, explicitly release the memory for that object.</span></span>

<span data-ttu-id="66955-p102">Следует отметить, что даже после удаления ссылок при попытке получения новой ссылки, когда имеется активная ссылка (удерживаемая другой надстройкой в Outlook) на один из вышеупомянутых объектов, новая ссылка будет продолжать указывать на устаревшую копию объекта. Поэтому важно удалять ссылки сразу же по окончании работы с повторяющейся встречей.</span><span class="sxs-lookup"><span data-stu-id="66955-p102">Note that even after you release your reference and attempt to obtain a new reference, if there is still an active reference (held by another add-in or Outlook) to one of the above objects, your new reference will still point to an out-of-date copy of the object. Therefore, it is important that you release your references as soon as you are finished with the recurring appointment.</span></span>

<span data-ttu-id="66955-113">В представленном ниже примере кода CheckOccurrenceExample использует повторяющуюся встречу, созданную в примере кода в статье [Создание встречи, которая повторяется по недельному расписанию](how-to-create-a-recurring-appointment-that-has-a-weekly-pattern.md).</span><span class="sxs-lookup"><span data-stu-id="66955-113">In the following code example, CheckOccurrenceExample uses the recurring appointment that was created in the code example in [Create a Recurring Appointment That Has a Weekly Pattern](how-to-create-a-recurring-appointment-that-has-a-weekly-pattern.md).</span></span> <span data-ttu-id="66955-114">Затем вызывается метод GetOccurrence, чтобы определить, начинается ли повторяющаяся встреча в определенную дату и время.</span><span class="sxs-lookup"><span data-stu-id="66955-114">It then calls the GetOccurrence method to determine whether the recurring appointment starts on the specified date and time.</span></span> <span data-ttu-id="66955-115">Чтобы гарантировать продолжение выполнения процедуры, даже если предоставленные сведения не соответствуют дате начала и времени вхождения повторяющейся встречи, в примере используется блок try…catch.</span><span class="sxs-lookup"><span data-stu-id="66955-115">To ensure that the procedure will continue even if the provided information does not match the start date and time of an instance of the recurring appointment, the example uses a try…catch block.</span></span> <span data-ttu-id="66955-116">После вызова метода GetOccurrence для каждой встречи в серии процедура CheckOccurrenceExample проверяет переменную singleAppt, чтобы определить, является ли она пустой ссылкой (это указывает на сбой метода и на то, что объект **AppointmentItem** не был получен).</span><span class="sxs-lookup"><span data-stu-id="66955-116">After calling the GetOccurrence method on every appointment in the recurring appointment series, CheckOccurrenceExample tests the singleAppt variable to determine whether it is set to a null reference, indicating that the method failed and did not return an **AppointmentItem** object.</span></span>

<span data-ttu-id="66955-117">Если вы используете Visual Studio для тестирования этого примера кода, сначала добавьте ссылку на компонент Microsoft Outlook 15.0 Object Library и задайте переменную Outlook при импорте пространства имен **Microsoft.Office.Interop.Outlook**.</span><span class="sxs-lookup"><span data-stu-id="66955-117">If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the Outlook variable when you import the **Microsoft.Office.Interop.Outlook** namespace.</span></span> <span data-ttu-id="66955-118">Инструкция **using** не должна находиться непосредственно перед функциями в примере кода, но ее нужно добавить перед объявлением общедоступного класса.</span><span class="sxs-lookup"><span data-stu-id="66955-118">The **using** statement must not occur directly before the functions in the code example but must be added before the public Class declaration.</span></span> <span data-ttu-id="66955-119">В приведенной ниже строке кода показано, как выполнить импорт и назначение на языке C\#.</span><span class="sxs-lookup"><span data-stu-id="66955-119">The following line of code shows how to do the import and assignment in C\#.</span></span>

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

## <a name="see-also"></a><span data-ttu-id="66955-120">См. также</span><span class="sxs-lookup"><span data-stu-id="66955-120">See also</span></span>

- [<span data-ttu-id="66955-121">Встречи</span><span class="sxs-lookup"><span data-stu-id="66955-121">Appointments</span></span>](appointments.md)


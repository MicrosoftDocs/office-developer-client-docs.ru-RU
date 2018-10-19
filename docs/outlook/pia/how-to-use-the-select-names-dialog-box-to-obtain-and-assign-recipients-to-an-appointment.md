---
title: Получение и назначение получателей для встречи с помощью диалогового окна "Выбор имен"
TOCTitle: Use the Select Names dialog box to obtain and assign recipients to an appointment
ms:assetid: b9bcb341-1912-425c-8d75-ed5be233145a
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184636(v=office.15)
ms:contentKeyID: 55119878
ms.date: 07/24/2014
mtps_version: v=office.15
ms.openlocfilehash: 57a7c99efa2bd82e1bc3d3f0855a90b62109719c
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25407004"
---
# <a name="use-the-select-names-dialog-box-to-obtain-and-assign-recipients-to-an-appointment"></a><span data-ttu-id="6c67b-102">Получение и назначение получателей для встречи с помощью диалогового окна "Выбор имен"</span><span class="sxs-lookup"><span data-stu-id="6c67b-102">Use the Select Names dialog box to obtain and assign recipients to an appointment</span></span>

<span data-ttu-id="6c67b-103">В этом примере показано, как с помощью диалогового окна **Выбор имен** получить получателей и назначить их элементу встречи.</span><span class="sxs-lookup"><span data-stu-id="6c67b-103">This example shows how to use the **Select Names** dialog box to obtain and assign recipients to an appointment item.</span></span>

## <a name="example"></a><span data-ttu-id="6c67b-104">Пример</span><span class="sxs-lookup"><span data-stu-id="6c67b-104">Example</span></span>

> [!NOTE] 
> <span data-ttu-id="6c67b-105">Приведенный ниже пример кода взят из книги [Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493) ("Программирование приложений для Microsoft Office Outlook 2007").</span><span class="sxs-lookup"><span data-stu-id="6c67b-105">The following code example is an excerpt from  [Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493)  , from Microsoft Press (ISBN 9780735622494, copyright Microsoft Press 2007, all rights reserved).</span></span>

<span data-ttu-id="6c67b-p101">Чтобы показать диалоговое окно **Выбор имен**, вызовите метод [Display()](https://msdn.microsoft.com/library/bb646086\(v=office.15\)) объекта [SelectNamesDialog](https://msdn.microsoft.com/library/bb609866\(v=office.15\)) . После открытия окна **Выбор имен** выполнение кода приостанавливается до тех пор, пока пользователь не нажмет **ОК** или не закроет это окно. Воспользуйтесь свойством [Recipients](https://msdn.microsoft.com/library/bb652601\(v=office.15\)) объекта **SelectNamesDialog**, чтобы задать показ исходных получателей или выделить получателей в диалоговом окне. При этом появляется коллекция [Recipients](https://msdn.microsoft.com/library/bb646361\(v=office.15\)) , связанная с **SelectNamesDialog**. Чтобы добавить объект [Recipient](https://msdn.microsoft.com/library/bb624370\(v=office.15\)) в коллекцию **Recipients** окна **SelectNamesDialog**, воспользуйтесь методом [Add](https://msdn.microsoft.com/library/bb612668\(v=office.15\)) для коллекции и укажите свойство [Type](https://msdn.microsoft.com/library/bb611841\(v=office.15\)) объекта **Recipient**.</span><span class="sxs-lookup"><span data-stu-id="6c67b-p101">To display the **Select Names** dialog box, call the [Display()](https://msdn.microsoft.com/library/bb646086\(v=office.15\)) method of the [SelectNamesDialog](https://msdn.microsoft.com/library/bb609866\(v=office.15\)) object. Once the **Select Names** dialog box is displayed to the user, code execution halts until the user clicks **OK** or closes the dialog box. To set initial recipients to display in the dialog box, or to get the recipients selected in the dialog box, use the [Recipients](https://msdn.microsoft.com/library/bb652601\(v=office.15\)) property of the **SelectNamesDialog** object. This returns a [Recipients](https://msdn.microsoft.com/library/bb646361\(v=office.15\)) collection that is associated with the **SelectNamesDialog**. To add a [Recipient](https://msdn.microsoft.com/library/bb624370\(v=office.15\)) object to the **Recipients** collection for the **SelectNamesDialog**, use the [Add](https://msdn.microsoft.com/library/bb612668\(v=office.15\)) method for the collection and specify the [Type](https://msdn.microsoft.com/library/bb611841\(v=office.15\)) property of the **Recipient** object.</span></span>

<span data-ttu-id="6c67b-111">В приведенном ниже примере кода метод DemoSelectNamesDialogRecipients создает объект [AppointmentItem](https://msdn.microsoft.com/library/bb645611\(v=office.15\)) и задает ряд его свойств.</span><span class="sxs-lookup"><span data-stu-id="6c67b-111">In the following code example,   creates an AppointmentItem object and sets some of its properties.</span></span> <span data-ttu-id="6c67b-112">Затем создается окно **SelectNamesDialog** и с помощью метода [SetDefaultDisplayMode(OlDefaultSelectNamesDisplayMode)](https://msdn.microsoft.com/library/bb623783\(v=office.15\)) задается режим просмотра собрания для диалогового окна **Выбор имен**.</span><span class="sxs-lookup"><span data-stu-id="6c67b-112">It then creates a **SelectNamesDialog** and uses the [SetDefaultDisplayMode(OlDefaultSelectNamesDisplayMode)](https://msdn.microsoft.com/library/bb623783\(v=office.15\)) method to set a meeting display mode for the **Select Names** dialog box.</span></span> <span data-ttu-id="6c67b-113">В данном примере параметр **Resource**, помогающий выбрать получателей, заполняется строкой "Conf Room 36/2739".</span><span class="sxs-lookup"><span data-stu-id="6c67b-113">The example populates the **Resource** recipient selector with the string "Conf Room 36/2739".</span></span> <span data-ttu-id="6c67b-114">После показа пользователю диалогового окна код перечисляет элементы коллекции **Recipients**, связанной с данным экземпляром **SelectNamesDialog**, и добавляет этих получателей к созданной встрече.</span><span class="sxs-lookup"><span data-stu-id="6c67b-114">Once the dialog box is displayed to the user, the code enumerates the **Recipients** collection that is associated with this instance of **SelectNamesDialog** and adds those recipients to the appointment that was created.</span></span> <span data-ttu-id="6c67b-115">Напоследок пользователю показывается приглашение на собрание.</span><span class="sxs-lookup"><span data-stu-id="6c67b-115">Finally, the example displays the meeting request to the user.</span></span>

<span data-ttu-id="6c67b-116">Если вы используете Visual Studio для тестирования этого примера кода, сначала добавьте ссылку на компонент библиотеки объектов Microsoft Outlook 15.0 и задайте переменную Outlook при импорте пространства имен **Microsoft.Office.Interop.Outlook**.</span><span class="sxs-lookup"><span data-stu-id="6c67b-116">If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the   variable when you import the Microsoft.Office.Interop.Outlook namespace.</span></span> <span data-ttu-id="6c67b-117">Инструкция **using** не должна находиться непосредственно перед функциями в примере кода, но ее нужно добавить перед объявлением общедоступного класса.</span><span class="sxs-lookup"><span data-stu-id="6c67b-117">The using statement must not occur directly before the functions in the code example but must be added before the public   declaration.</span></span> <span data-ttu-id="6c67b-118">В приведенной ниже строке кода показано, как выполнить импорт и назначение на языке C\#.</span><span class="sxs-lookup"><span data-stu-id="6c67b-118">The following line of code shows how to do the import and assignment in C#.</span></span>

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```csharp
private void DemoSelectNamesDialogRecipients()
{
    Outlook.AppointmentItem appt = Application.CreateItem(
        Outlook.OlItemType.olAppointmentItem)
        as Outlook.AppointmentItem;
    appt.MeetingStatus = Outlook.OlMeetingStatus.olMeeting;
    appt.Subject = "Team Morale Event";
    appt.Start = DateTime.Parse("5/17/2007 11:00 AM");
    appt.End = DateTime.Parse("5/17/2007 12:00 PM");
    Outlook.SelectNamesDialog snd =
        Application.Session.GetSelectNamesDialog();
    snd.SetDefaultDisplayMode(
        Outlook.OlDefaultSelectNamesDisplayMode.olDefaultMeeting);
    Outlook.Recipient confRoom =
        snd.Recipients.Add("Conf Room 36/2739");
    // Explicitly specify Recipient.Type.
    confRoom.Type = (int)Outlook.OlMeetingRecipientType.olResource;
    snd.Recipients.ResolveAll();
    snd.Display();
    // Add Recipients to meeting request.
    Outlook.Recipients recips = snd.Recipients;
    if (recips.Count > 0)
    {
        foreach (Outlook.Recipient recip in recips)
        {
            appt.Recipients.Add(recip.Name);
        }
    }
    appt.Recipients.ResolveAll();
    appt.Display(false);
}
```

## <a name="see-also"></a><span data-ttu-id="6c67b-119">См. также</span><span class="sxs-lookup"><span data-stu-id="6c67b-119">See also</span></span>

- [<span data-ttu-id="6c67b-120">Получатели</span><span class="sxs-lookup"><span data-stu-id="6c67b-120">Recipients</span></span>](recipients.md)


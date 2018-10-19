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
# <a name="use-the-select-names-dialog-box-to-obtain-and-assign-recipients-to-an-appointment"></a>Получение и назначение получателей для встречи с помощью диалогового окна "Выбор имен"

В этом примере показано, как с помощью диалогового окна **Выбор имен** получить получателей и назначить их элементу встречи.

## <a name="example"></a>Пример

> [!NOTE] 
> Приведенный ниже пример кода взят из книги [Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493) ("Программирование приложений для Microsoft Office Outlook 2007").

Чтобы показать диалоговое окно **Выбор имен**, вызовите метод [Display()](https://msdn.microsoft.com/library/bb646086\(v=office.15\)) объекта [SelectNamesDialog](https://msdn.microsoft.com/library/bb609866\(v=office.15\)) . После открытия окна **Выбор имен** выполнение кода приостанавливается до тех пор, пока пользователь не нажмет **ОК** или не закроет это окно. Воспользуйтесь свойством [Recipients](https://msdn.microsoft.com/library/bb652601\(v=office.15\)) объекта **SelectNamesDialog**, чтобы задать показ исходных получателей или выделить получателей в диалоговом окне. При этом появляется коллекция [Recipients](https://msdn.microsoft.com/library/bb646361\(v=office.15\)) , связанная с **SelectNamesDialog**. Чтобы добавить объект [Recipient](https://msdn.microsoft.com/library/bb624370\(v=office.15\)) в коллекцию **Recipients** окна **SelectNamesDialog**, воспользуйтесь методом [Add](https://msdn.microsoft.com/library/bb612668\(v=office.15\)) для коллекции и укажите свойство [Type](https://msdn.microsoft.com/library/bb611841\(v=office.15\)) объекта **Recipient**.

В приведенном ниже примере кода метод DemoSelectNamesDialogRecipients создает объект [AppointmentItem](https://msdn.microsoft.com/library/bb645611\(v=office.15\)) и задает ряд его свойств. Затем создается окно **SelectNamesDialog** и с помощью метода [SetDefaultDisplayMode(OlDefaultSelectNamesDisplayMode)](https://msdn.microsoft.com/library/bb623783\(v=office.15\)) задается режим просмотра собрания для диалогового окна **Выбор имен**. В данном примере параметр **Resource**, помогающий выбрать получателей, заполняется строкой "Conf Room 36/2739". После показа пользователю диалогового окна код перечисляет элементы коллекции **Recipients**, связанной с данным экземпляром **SelectNamesDialog**, и добавляет этих получателей к созданной встрече. Напоследок пользователю показывается приглашение на собрание.

Если вы используете Visual Studio для тестирования этого примера кода, сначала добавьте ссылку на компонент библиотеки объектов Microsoft Outlook 15.0 и задайте переменную Outlook при импорте пространства имен **Microsoft.Office.Interop.Outlook**. Инструкция **using** не должна находиться непосредственно перед функциями в примере кода, но ее нужно добавить перед объявлением общедоступного класса. В приведенной ниже строке кода показано, как выполнить импорт и назначение на языке C\#.

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

## <a name="see-also"></a>См. также

- [Получатели](recipients.md)


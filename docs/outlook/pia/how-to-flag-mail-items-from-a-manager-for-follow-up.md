---
title: Пометка почтовых элементов от руководителя к исполнению
TOCTitle: Flag mail items from a manager for follow-up
ms:assetid: 5f7f3678-0f63-451e-ba08-cd973525aa1b
ms:mtpsurl: https://msdn.microsoft.com/library/Ff424470(v=office.15)
ms:contentKeyID: 55119898
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 06e6bdd91198cabeff689681f2999d6fd2cb725a
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/29/2019
ms.locfileid: "34542592"
---
# <a name="flag-mail-items-from-a-manager-for-follow-up"></a><span data-ttu-id="9fd4c-102">Пометка почтовых элементов от руководителя к исполнению</span><span class="sxs-lookup"><span data-stu-id="9fd4c-102">Flag mail items from a manager for follow-up</span></span>

<span data-ttu-id="9fd4c-103">В этом примере показывается способ пометки элементов электронной почты, полученных от руководителя пользователя для исполнения.</span><span class="sxs-lookup"><span data-stu-id="9fd4c-103">This example shows how to flag email items that were received from the user’s manager for follow-up.</span></span>

## <a name="example"></a><span data-ttu-id="9fd4c-104">Пример</span><span class="sxs-lookup"><span data-stu-id="9fd4c-104">Example</span></span>

> [!NOTE] 
> <span data-ttu-id="9fd4c-105">Приведенный ниже пример кода взят из книги [Программирование приложений для Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).</span><span class="sxs-lookup"><span data-stu-id="9fd4c-105">The following code example is an excerpt from [Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).</span></span>

<span data-ttu-id="9fd4c-p101">В Microsoft Outlook предусмотрена система пометки задач, в которой определенные элементы Outlook, такие как элементы почты или контактов, могут быть помечены для исполнения. При пометке элемента Outlook для исполнения сведения об этом элементе наряду с другими сведениями о задаче отображаются в **списке дел** и в модуле навигации календаря интерфейса пользователя Outlook. В обычной конфигурации окна обозревателя Outlook **список дел** отображается в виде вертикальной панели. В нем содержится элемент управления "Календарик", предстоящие встречи и элементы, помеченные для выполнения. Сам по себе **список дел** не является расширяемым, и параметры конфигурации для **списка дел** можно установить только с помощью интерфейса пользователя Outlook. Пометка элементов позволяет организовывать и устанавливать приоритеты задач и элементов для выполнения.</span><span class="sxs-lookup"><span data-stu-id="9fd4c-p101">Microsoft Outlook provides a task flagging system in which certain Outlook items such as mail items or contact items can be flagged for follow-up. When you flag an Outlook item for follow-up, information about that Outlook item, along with other task-based information, is displayed on the **To-Do Bar** and Calendar navigation module in the Outlook user interface. The **To-Do Bar** is displayed as a vertical pane in a typical configuration of the Outlook explorer window. It contains a date navigator control, upcoming appointments, and items that have been flagged for follow-up. The **To-Do Bar** itself is not extensible, and you can set configuration options for the **To-Do Bar** only through the Outlook user interface. Flagging items allows to you organize and prioritize tasks and to-do items.</span></span>

<span data-ttu-id="9fd4c-112">В примере кода ниже помечается группа элементов для исполнения в указанном интервале.</span><span class="sxs-lookup"><span data-stu-id="9fd4c-112">The following code example marks a group of items for a specified follow-up interval.</span></span> <span data-ttu-id="9fd4c-113">В примере возвращаются все элементы в папке "Входящие" текущего пользователя, полученные от руководителя текущего пользователя, с помощью запроса DASL, чтобы отфильтровать сообщения типа "IPM.NOTE" с именем руководителя в качестве отправителя.</span><span class="sxs-lookup"><span data-stu-id="9fd4c-113">The example gets all items in the current user’s Inbox that are from the current user’s manager by using a DAV Searching and Locating (DASL) query to filter for messages of type “IPM.NOTE” with the manager’s name as the sender.</span></span> <span data-ttu-id="9fd4c-114">Затем помечаются все элементы в соответствии со значением [OlImportance](https://msdn.microsoft.com/library/bb609592\(v=office.15\)) свойства [Importance](https://msdn.microsoft.com/library/bb611974\(v=office.15\)).</span><span class="sxs-lookup"><span data-stu-id="9fd4c-114">It then flags all items according to the [OlImportance](https://msdn.microsoft.com/library/bb609592\(v=office.15\)) value of the [Importance](https://msdn.microsoft.com/library/bb611974\(v=office.15\)) property.</span></span> <span data-ttu-id="9fd4c-115">С помощью метода [MarkAsTask(OlMarkInterval)](https://msdn.microsoft.com/library/bb609068\(v=office.15\)) все элементы высокой важности помечаются к исполнению сегодня, а все элементы обычной важности — к исполнению на текущей неделе.</span><span class="sxs-lookup"><span data-stu-id="9fd4c-115">All high-importance items are flagged for follow-up today and all normal-importance items are flagged for follow-up this week by using the [MarkAsTask(OlMarkInterval)](https://msdn.microsoft.com/library/bb609068\(v=office.15\)) method.</span></span>


> [!NOTE]
> <span data-ttu-id="9fd4c-116">Свойство **Importance** и метод **MarkAsTask** являются элементами объекта **Item**.</span><span class="sxs-lookup"><span data-stu-id="9fd4c-116">The **Importance** property and the **MarkAsTask** method are **Item** object members.</span></span>


<span data-ttu-id="9fd4c-117">Если вы используете Visual Studio для тестирования этого примера кода, сначала добавьте ссылку на компонент Microsoft Outlook 15.0 Object Library и задайте переменную Outlook при импорте пространства имен **Microsoft.Office.Interop.Outlook**.</span><span class="sxs-lookup"><span data-stu-id="9fd4c-117">If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the Outlook variable when you import the **Microsoft.Office.Interop.Outlook** namespace.</span></span> <span data-ttu-id="9fd4c-118">Инструкция **using** не должна находиться непосредственно перед функциями в примере кода, но ее нужно добавить перед объявлением общедоступного класса.</span><span class="sxs-lookup"><span data-stu-id="9fd4c-118">The **using** statement must not occur directly before the functions in the code example but must be added before the public Class declaration.</span></span> <span data-ttu-id="9fd4c-119">В приведенной ниже строке кода показано, как выполнить импорт и назначение на языке C\#.</span><span class="sxs-lookup"><span data-stu-id="9fd4c-119">The following line of code shows how to do the import and assignment in C\#.</span></span>

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```csharp
private void DemoTaskFlagging()
{
    const string PR_SENT_REPRESENTING_NAME =
        "http://schemas.microsoft.com/mapi/proptag/0x0042001E";
    const string PR_MESSAGE_CLASS =
        "http://schemas.microsoft.com/mapi/proptag/0x001A001E";
    Outlook.AddressEntry currentUser =
        Application.Session.CurrentUser.AddressEntry;
    if (currentUser.Type == "EX")
    {
        Outlook.ExchangeUser manager;
        try
        {
            manager = currentUser.
                GetExchangeUser().GetExchangeUserManager();
        }
        catch
        {
            Debug.WriteLine("Could not obtain user's manager.");
            return;
        }
        if (manager != null)
        {
            string displayName = manager.Name;
            string filter = "@SQL=" + "\""
                + PR_SENT_REPRESENTING_NAME + "\""
                + " = '" + displayName + "'" + " AND " + "\""
                + PR_MESSAGE_CLASS + "\"" + " = 'IPM.NOTE'";
            Outlook.Items items =
                Application.Session.GetDefaultFolder(
                Outlook.OlDefaultFolders.olFolderInbox).
                Items.Restrict(filter);
            foreach (Outlook.MailItem mail in items)
            {
                if (mail.Importance ==
                    Outlook.OlImportance.olImportanceHigh)
                {
                    mail.MarkAsTask(Outlook.OlMarkInterval.olMarkToday);
                    mail.Save();
                }
                if (mail.Importance ==
                    Outlook.OlImportance.olImportanceNormal)
                {
                    mail.MarkAsTask(Outlook.OlMarkInterval.olMarkThisWeek);
                    mail.Save();
                }
            }
        }
    }
}
```

## <a name="see-also"></a><span data-ttu-id="9fd4c-120">См. также</span><span class="sxs-lookup"><span data-stu-id="9fd4c-120">See also</span></span>

- [<span data-ttu-id="9fd4c-121">Задачи</span><span class="sxs-lookup"><span data-stu-id="9fd4c-121">Tasks</span></span>](tasks.md)


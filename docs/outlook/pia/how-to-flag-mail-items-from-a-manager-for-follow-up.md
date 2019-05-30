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
# <a name="flag-mail-items-from-a-manager-for-follow-up"></a>Пометка почтовых элементов от руководителя к исполнению

В этом примере показывается способ пометки элементов электронной почты, полученных от руководителя пользователя для исполнения.

## <a name="example"></a>Пример

> [!NOTE] 
> Приведенный ниже пример кода взят из книги [Программирование приложений для Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).

В Microsoft Outlook предусмотрена система пометки задач, в которой определенные элементы Outlook, такие как элементы почты или контактов, могут быть помечены для исполнения. При пометке элемента Outlook для исполнения сведения об этом элементе наряду с другими сведениями о задаче отображаются в **списке дел** и в модуле навигации календаря интерфейса пользователя Outlook. В обычной конфигурации окна обозревателя Outlook **список дел** отображается в виде вертикальной панели. В нем содержится элемент управления "Календарик", предстоящие встречи и элементы, помеченные для выполнения. Сам по себе **список дел** не является расширяемым, и параметры конфигурации для **списка дел** можно установить только с помощью интерфейса пользователя Outlook. Пометка элементов позволяет организовывать и устанавливать приоритеты задач и элементов для выполнения.

В примере кода ниже помечается группа элементов для исполнения в указанном интервале. В примере возвращаются все элементы в папке "Входящие" текущего пользователя, полученные от руководителя текущего пользователя, с помощью запроса DASL, чтобы отфильтровать сообщения типа "IPM.NOTE" с именем руководителя в качестве отправителя. Затем помечаются все элементы в соответствии со значением [OlImportance](https://msdn.microsoft.com/library/bb609592\(v=office.15\)) свойства [Importance](https://msdn.microsoft.com/library/bb611974\(v=office.15\)). С помощью метода [MarkAsTask(OlMarkInterval)](https://msdn.microsoft.com/library/bb609068\(v=office.15\)) все элементы высокой важности помечаются к исполнению сегодня, а все элементы обычной важности — к исполнению на текущей неделе.


> [!NOTE]
> Свойство **Importance** и метод **MarkAsTask** являются элементами объекта **Item**.


Если вы используете Visual Studio для тестирования этого примера кода, сначала добавьте ссылку на компонент Microsoft Outlook 15.0 Object Library и задайте переменную Outlook при импорте пространства имен **Microsoft.Office.Interop.Outlook**. Инструкция **using** не должна находиться непосредственно перед функциями в примере кода, но ее нужно добавить перед объявлением общедоступного класса. В приведенной ниже строке кода показано, как выполнить импорт и назначение на языке C\#.

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

## <a name="see-also"></a>См. также

- [Задачи](tasks.md)


---
title: Получение и перечисление выбранных бесед
TOCTitle: Get and enumerate selected conversations
ms:assetid: 835312ea-2b29-49a5-b128-f69cf8d4427c
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184621(v=office.15)
ms:contentKeyID: 55119833
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 2d71fc1d582abebc8cb00f4885ec5b5ba348228c
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28699375"
---
# <a name="get-and-enumerate-selected-conversations"></a>Получение и перечисление выбранных бесед

В этом примере показано, как получить и перечислить выбранные беседы с помощью метода [GetSelection(OlSelectionContents)](https://msdn.microsoft.com/library/ff185002\(v=office.15\)).

## <a name="example"></a>Пример

Microsoft Outlook можно настроить так, чтобы элементы в папке "Входящие" отображались по беседам. Если пользователь выбирает элемент в папке "Входящие", можно получить этот выбор программным образом, включая заголовки и элементы бесед. В примере кода в данном разделе показывается, как получить выбранный в папке "Входящие" элемент и как перечислить почтовые элементы для каждой из выбранных бесед.

Этот пример содержит один метод, DemoConversationHeadersFromSelection. Этот метод задает в качестве текущего представления папку "Входящие", а затем проверяет, является ли текущее представление табличным представлением, отображающим беседы, отсортированные по датам. Чтобы получить выбранные элементы, включая все выбранные объекты [ConversationHeader](https://msdn.microsoft.com/library/ff184727\(v=office.15\)), метод DemoConversationHeadersFromSelection использует метод **GetSelection** объекта [Selection](https://msdn.microsoft.com/library/bb612099\(v=office.15\)), задавая в качестве аргумента константу [olConversationHeaders](https://msdn.microsoft.com/library/ff184867\(v=office.15\)). Если выбраны заголовки бесед, метод DemoConversationHeadersFromSelection использует объект [SimpleItems](https://msdn.microsoft.com/library/ff184992\(v=office.15\)) для перечисления элементов в каждой выбранной беседе, а затем выводит темы элементов беседы, являющихся объектами [MailItem](https://msdn.microsoft.com/library/bb643865\(v=office.15\)).

Если вы используете Visual Studio для тестирования этого примера кода, сначала добавьте ссылку на компонент библиотеки объектов Microsoft Outlook 15.0 и задайте переменную Outlook при импорте пространства имен **Microsoft.Office.Interop.Outlook**. Инструкция **using** не должна находиться непосредственно перед функциями в примере кода, но ее нужно добавить перед объявлением общедоступного класса. В приведенной ниже строке кода показано, как выполнить импорт и назначение на языке C\#.

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```csharp
private void DemoConversationHeadersFromSelection()
{
    // Obtain Inbox.
    Outlook.Folder inbox =
        Application.Session.GetDefaultFolder(
        Outlook.OlDefaultFolders.olFolderInbox)
        as Outlook.Folder;
    // Set ActiveExplorer.CurrentFolder to Inbox.
    // Inbox must be current folder.
    Application.ActiveExplorer().CurrentFolder = inbox;
    // Ensure that current view is TableView.
    if (inbox.CurrentView.ViewType ==
        Outlook.OlViewType.olTableView)
    {
        Outlook.TableView view =
            inbox.CurrentView as Outlook.TableView;
        if (view.ShowConversationByDate == true)
        {
            Outlook.Selection selection =
                Application.ActiveExplorer().Selection;
            Debug.WriteLine("Selection.Count = " + selection.Count);
            // Call GetSelection to create a Selection object
            // that contains ConversationHeader objects.
            Outlook.Selection convHeaders =
                selection.GetSelection(
                Outlook.OlSelectionContents.olConversationHeaders)
                as Outlook.Selection;
            Debug.WriteLine("Selection.Count (ConversationHeaders) = " 
                + convHeaders.Count);
            if (convHeaders.Count >= 1)
            {
                foreach (Outlook.ConversationHeader convHeader in convHeaders)
                {
                    // Enumerate the items in the ConversationHeader.
                    Outlook.SimpleItems items = convHeader.GetItems();
                    for (int i = 1; i <= items.Count; i++)
                    {
                        // Enumerate only MailItems in this example.
                        if (items[i] is Outlook.MailItem)
                        {
                            Outlook.MailItem mail = 
                                items[i] as Outlook.MailItem;
                            Debug.WriteLine(mail.Subject 
                                + " Received:" + mail.ReceivedTime);
                        }
                    }
                }
            }
        }
    }
}
```

## <a name="see-also"></a>См. также

- [Беседы](conversations.md)


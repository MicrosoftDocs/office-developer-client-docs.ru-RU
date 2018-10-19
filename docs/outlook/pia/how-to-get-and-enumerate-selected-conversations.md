---
title: Получение и перечисление выбранных бесед
TOCTitle: Get and enumerate selected conversations
ms:assetid: 835312ea-2b29-49a5-b128-f69cf8d4427c
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184621(v=office.15)
ms:contentKeyID: 55119833
ms.date: 07/24/2014
mtps_version: v=office.15
ms.openlocfilehash: cf36003f183c9ddfe40cb2c27a9feab2962324d6
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25405597"
---
# <a name="get-and-enumerate-selected-conversations"></a><span data-ttu-id="ddf17-102">Получение и перечисление выбранных бесед</span><span class="sxs-lookup"><span data-stu-id="ddf17-102">Get and enumerate selected conversations</span></span>

<span data-ttu-id="ddf17-103">В этом примере показано, как получить и перечислить выбранные беседы с помощью метода [GetSelection(OlSelectionContents)](https://msdn.microsoft.com/library/ff185002\(v=office.15\)).</span><span class="sxs-lookup"><span data-stu-id="ddf17-103">This example obtains and enumerates selected conversations by using the [GetSelection(OlSelectionContents)](https://msdn.microsoft.com/library/ff185002\(v=office.15\)) method.</span></span>

## <a name="example"></a><span data-ttu-id="ddf17-104">Пример</span><span class="sxs-lookup"><span data-stu-id="ddf17-104">Example</span></span>

<span data-ttu-id="ddf17-p101">Microsoft Outlook можно настроить так, чтобы элементы в папке "Входящие" отображались по беседам. Если пользователь выбирает элемент в папке "Входящие", можно получить этот выбор программным образом, включая заголовки и элементы бесед. В примере кода в данном разделе показывается, как получить выбранный в папке "Входящие" элемент и как перечислить почтовые элементы для каждой из выбранных бесед.</span><span class="sxs-lookup"><span data-stu-id="ddf17-p101">Microsoft Outlook can be set to display items in the Inbox by conversation. If a user makes a selection in the Inbox, you can obtain the selection programmatically, including conversation headers and conversation items. The code example in this topic shows how to obtain a selection in the Inbox and enumerate the mail items in each conversation in the selection.</span></span>

<span data-ttu-id="ddf17-108">Этот пример содержит один метод, DemoConversationHeadersFromSelection.</span><span class="sxs-lookup"><span data-stu-id="ddf17-108">The example contains one method,  .</span></span> <span data-ttu-id="ddf17-109">Этот метод задает в качестве текущего представления папку "Входящие", а затем проверяет, является ли текущее представление табличным представлением, отображающим беседы, отсортированные по датам.</span><span class="sxs-lookup"><span data-stu-id="ddf17-109">The method sets the current view to the Inbox, and then checks whether the current view is a table view that displays conversations sorted by date.</span></span> <span data-ttu-id="ddf17-110">Чтобы получить выбранные элементы, включая все выбранные объекты [ConversationHeader](https://msdn.microsoft.com/library/ff184727\(v=office.15\)), метод DemoConversationHeadersFromSelection использует метод **GetSelection** объекта [Selection](https://msdn.microsoft.com/library/bb612099\(v=office.15\)), задавая в качестве аргумента константу [olConversationHeaders](https://msdn.microsoft.com/library/ff184867\(v=office.15\)).</span><span class="sxs-lookup"><span data-stu-id="ddf17-110">To obtain a selection, including any selected ConversationHeader objects,   uses the GetSelection method of the Selection object, specifying the olConversationHeaders constant as an argument.</span></span> <span data-ttu-id="ddf17-111">Если выбраны заголовки бесед, метод DemoConversationHeadersFromSelection использует объект [SimpleItems](https://msdn.microsoft.com/library/ff184992\(v=office.15\)) для перечисления элементов в каждой выбранной беседе, а затем выводит темы элементов беседы, являющихся объектами [MailItem](https://msdn.microsoft.com/library/bb643865\(v=office.15\)).</span><span class="sxs-lookup"><span data-stu-id="ddf17-111">If conversation headers are selected,   uses the SimpleItems object to enumerate items in each selected conversation, and then displays the subject of those conversation items that are MailItem objects.</span></span>

<span data-ttu-id="ddf17-112">Если вы используете Visual Studio для тестирования этого примера кода, сначала добавьте ссылку на компонент библиотеки объектов Microsoft Outlook 15.0 и задайте переменную Outlook при импорте пространства имен **Microsoft.Office.Interop.Outlook**.</span><span class="sxs-lookup"><span data-stu-id="ddf17-112">If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the   variable when you import the Microsoft.Office.Interop.Outlook namespace.</span></span> <span data-ttu-id="ddf17-113">Инструкция **using** не должна находиться непосредственно перед функциями в примере кода, но ее нужно добавить перед объявлением общедоступного класса.</span><span class="sxs-lookup"><span data-stu-id="ddf17-113">The using statement must not occur directly before the functions in the code example but must be added before the public   declaration.</span></span> <span data-ttu-id="ddf17-114">В приведенной ниже строке кода показано, как выполнить импорт и назначение на языке C\#.</span><span class="sxs-lookup"><span data-stu-id="ddf17-114">The following line of code shows how to do the import and assignment in C#.</span></span>

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

## <a name="see-also"></a><span data-ttu-id="ddf17-115">См. также</span><span class="sxs-lookup"><span data-stu-id="ddf17-115">See also</span></span>

- [<span data-ttu-id="ddf17-116">Беседы</span><span class="sxs-lookup"><span data-stu-id="ddf17-116">Conversations</span></span>](conversations.md)


---
title: Получение и отображение элементов в беседе
TOCTitle: Get and display items in a conversation
ms:assetid: 8f30a7cb-0949-46d7-bc51-2d93dbb22bf8
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184625(v=office.15)
ms:contentKeyID: 55119832
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 0fcfe76632c2fda742a85a571d655569dc2fcd33
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28705612"
---
# <a name="get-and-display-items-in-a-conversation"></a>Получение и отображение элементов в беседе

В этом примере показано, как получать и отображать почтовые элементы в беседе.

## <a name="example"></a>Пример

В представленном ниже примере кода DemoConversation получает объект [MailItem](https://msdn.microsoft.com/library/bb643865\(v=office.15\)), после чего определяет хранилище объекта **MailItem** с помощью свойства [Store](https://msdn.microsoft.com/library/bb609093\(v=office.15\)) объекта [Folder](https://msdn.microsoft.com/library/bb645774\(v=office.15\)). Затем DemoConversation проверяет, соответствует ли свойству [IsConversationEnabled](https://msdn.microsoft.com/library/ff185030\(v=office.15\)) значение **true**. Если значение равно **true**, в примере кода возвращается объект [Conversation](https://msdn.microsoft.com/library/ff184711\(v=office.15\)) с помощью метода [GetConversation()](https://msdn.microsoft.com/library/ff184974\(v=office.15\)). Если объект **Conversation** не является пустой ссылкой, в примере возвращается связанный объект [Table](https://msdn.microsoft.com/library/bb652856\(v=office.15\)), содержащий все элементы беседы, с помощью метода [GetTable()](https://msdn.microsoft.com/library/ff185184\(v=office.15\)). 

После этого в примере перечисляются все элементы в объекте **Table** и вызывается метод EnumerateConversation для каждого элемента, чтобы получить доступ к дочерним узлам каждого элемента. Метод EnumerateConversation использует объект **Conversation** и получает дочерние узлы с помощью метода [GetChildren(Object)](https://msdn.microsoft.com/library/ff184854\(v=office.15\)). Метод EnumerateConversation вызывается рекурсивно, пока не закончатся все дочерние узлы. Затем каждый элемент беседы демонстрируется пользователю.

Если для тестирования этого примера кода вы используете Visual Studio, сначала добавьте ссылку на компонент библиотеки объектов Microsoft Outlook 15.0 и укажите переменную Outlook при импорте пространства имен **Microsoft.Office.Interop.Outlook**. Не следует использовать инструкцию **using** непосредственно перед функциями в примере кода, но ее необходимо добавить перед объявлением общедоступного класса. В следующей строке кода показано, как выполнить импорт и назначение в C\#.

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```csharp
void DemoConversation()
{
    object selectedItem = 
        Application.ActiveExplorer().Selection[1];
    // For this example, you will work only with 
    //MailItem. Other item types such as
    //MeetingItem and PostItem can participate 
    //in Conversation.
    if (selectedItem is Outlook.MailItem)
    {
        // Cast selectedItem to MailItem.
        Outlook.MailItem mailItem =
            selectedItem as Outlook.MailItem; ;
        // Determine store of mailItem.
        Outlook.Folder folder = mailItem.Parent
            as Outlook.Folder;
        Outlook.Store store = folder.Store;
        if (store.IsConversationEnabled == true)
        {
            // Obtain a Conversation object.
            Outlook.Conversation conv =
                mailItem.GetConversation();
            // Check for null Conversation.
            if (conv != null)
            {
                // Obtain Table that contains rows 
                // for each item in Conversation.
                Outlook.Table table = conv.GetTable();
                Debug.WriteLine("Conversation Items Count: " +
                    table.GetRowCount().ToString());
                Debug.WriteLine("Conversation Items from Table:");
                while (!table.EndOfTable)
                {
                    Outlook.Row nextRow = table.GetNextRow();
                    Debug.WriteLine(nextRow["Subject"]
                        + " Modified: "
                        + nextRow["LastModificationTime"]);
                }
                Debug.WriteLine("Conversation Items from Root:");
                // Obtain root items and enumerate Conversation.
                Outlook.SimpleItems simpleItems 
                    = conv.GetRootItems();
                foreach (object item in simpleItems)
                {
                    // In this example, enumerate only MailItem type.
                    // Other types such as PostItem or MeetingItem
                    // can appear in Conversation.
                    if (item is Outlook.MailItem)
                    {
                        Outlook.MailItem mail = item
                            as Outlook.MailItem;
                        Outlook.Folder inFolder =
                            mail.Parent as Outlook.Folder;
                        string msg = mail.Subject
                            + " in folder " + inFolder.Name;
                        Debug.WriteLine(msg);
                    }
                    // Call EnumerateConversation 
                    // to access child nodes of root items.
                    EnumerateConversation(item, conv);
                }
            }
        }
    }
}

void EnumerateConversation(object item,
    Outlook.Conversation conversation)
{
    Outlook.SimpleItems items =
        conversation.GetChildren(item);
    if (items.Count > 0)
    {
        foreach (object myItem in items)
        {
            // In this example, enumerate only MailItem type.
            // Other types such as PostItem or MeetingItem
            // can appear in Conversation.
            if (myItem is Outlook.MailItem)
            {
                Outlook.MailItem mailItem =
                    myItem as Outlook.MailItem;
                Outlook.Folder inFolder =
                    mailItem.Parent as Outlook.Folder;
                string msg = mailItem.Subject
                    + " in folder " + inFolder.Name;
                Debug.WriteLine(msg);
            }
            // Continue recursion.
            EnumerateConversation(myItem, conversation);
        }
    }
}
```

## <a name="see-also"></a>См. также

- [Беседы](conversations.md)


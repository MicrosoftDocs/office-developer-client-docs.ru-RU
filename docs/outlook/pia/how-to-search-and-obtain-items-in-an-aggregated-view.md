---
title: Поиск и получение элементов в общем представлении
TOCTitle: Search and obtain items in an aggregated view
ms:assetid: 1a875dc8-dd52-4e9c-b292-5f6ba3d7a940
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184592(v=office.15)
ms:contentKeyID: 55119925
ms.date: 07/24/2014
mtps_version: v=office.15
ms.openlocfilehash: 540557973d395c23d26a87502ed6ba43176a0a3c
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25407578"
---
# <a name="search-and-obtain-items-in-an-aggregated-view"></a>Поиск и получение элементов в общем представлении

В этом примере показано, как искать элементы в разных папках и хранилищах и возвращать эти элементы в объединенном табличном представлении.

## <a name="example"></a>Пример

Метод [GetTable()](https://msdn.microsoft.com/library/ff184699\(v=office.15\)) объекта [TableView](https://msdn.microsoft.com/library/bb608854\(v=office.15\)) может возвратить в агрегированном представлении объект [Table](https://msdn.microsoft.com/library/bb652856\(v=office.15\)) , содержащий элементы из одной или нескольких папок одного хранилища или охватывающий несколько хранилищ. Это особенно полезно, если нужен доступ к элементам, возвращенным в результате поиска (например, при поиске всех почтовых элементов в хранилище). В данном разделе показан пример использования функции **Мгновенный поиск** для поиска всех элементов, полученных от руководителя текущего пользователя и помеченных как важные, и последующего отображения темы каждого результата поиска.

В следующем примере кода метод **GetItemsInView** проверяет, является ли учетная запись основного хранилища доставки текущего пользователя учетной записью Exchange, есть ли у текущего пользователя руководитель и работает ли **Мгновенный поиск** в хранилище по умолчанию этого сеанса. Так как поиск использует метод [Search](https://msdn.microsoft.com/library/bb610561\(v=office.15\)) объекта [Explorer](https://msdn.microsoft.com/library/bb623678\(v=office.15\)), и результаты поиска получаются с помощью метода **GetTable**, **GetItemsInView** создает объект **Explorer**, отображает папку "Входящие" в этом объекте и использует его для настройки поиска. 

**GetItemsInView** выполняет поиск во всех папках типа [MailItem](https://msdn.microsoft.com/library/bb643865\(v=office.15\)) для элементов, полученных от руководителя текущего пользователя и помеченных как важные. Затем **GetItemsInView** вызывает метод [Search](https://msdn.microsoft.com/library/bb610561\(v=office.15\)), все результаты поиска отображаются в проводнике, включая элементы из других папок и хранилищ, соответствующих условиям поиска. **GetItemsInView** получает объект **TableView**, содержащий это представление результатов поиска в проводнике. Используя метод **GetTable** этого объекта **TableView**, **GetItemsInView** далее получает объект **Table**, содержащий агрегированные элементы, возвращенные при поиске. Наконец, **GetItemsInView** отображает столбец темы каждой строки объекта **Table**, который представляет элемент в результатах поиска.

Если для тестирования этого примера кода вы используете Visual Studio, сначала добавьте ссылку на компонент библиотеки объектов Microsoft Outlook 15.0 и укажите переменную Outlook при импорте пространства имен **Microsoft.Office.Interop.Outlook**. Не следует использовать инструкцию **using** непосредственно перед функциями в примере кода, но ее необходимо добавить перед объявлением общедоступного класса. В следующей строке кода показано, как выполнить импорт и назначение в C\#.

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```csharp
private void GetItemsInView()
{
    Outlook.AddressEntry currentUser =
        Application.Session.CurrentUser.AddressEntry;

    // Check whether the current user uses the Exchange Server.
    if (currentUser.Type == "EX")
    {
        Outlook.ExchangeUser manager =
            currentUser.GetExchangeUser().GetExchangeUserManager();

        // Check whether the current user has a manager.
        if (manager != null)
        {
            string managerName = manager.Name;

            // Check whether Instant Search is enabled and 
            // operational in the default store.
            if (Application.Session.DefaultStore.IsInstantSearchEnabled)
            {
                Outlook.Folder inbox =
                    Application.Session.GetDefaultFolder(
                    Outlook.OlDefaultFolders.olFolderInbox);

                // Create a new explorer to display the Inbox as
                // the current folder.
                Outlook.Explorer explorer =
                    Application.Explorers.Add(inbox,
                    Outlook.OlFolderDisplayMode.olFolderDisplayNormal);

                // Make the new explorer visible.
                explorer.Display;

                // Search for items from the manager marked important, 
                // from all folders of the same item type as the current folder, 
                // which is the MailItem item type.
                string searchFor =
                    "from:" + "\"" + managerName 
                    + "\"" + " importance:high";
                explorer.Search(searchFor,
                    Outlook.OlSearchScope.olSearchScopeAllFolders);

                // Any search results are displayed in that new explorer
                // in an aggregated table view.
                Outlook.TableView tableView = 
                    explorer.CurrentView as Outlook.TableView;

                // Use GetTable of that table view to obtain items in that
                // aggregated view in a Table object.
                Outlook.Table table = tableView.GetTable();
                while (!table.EndOfTable)
                {
                    // Then display each row in the Table object
                    // that represents an item in the search results.
                    Outlook.Row nextRow = table.GetNextRow();
                    Debug.WriteLine(nextRow["Subject"]);
                }
            }
        }
    }
}
```

## <a name="see-also"></a>См. также

- [Поиск и фильтрация](search-and-filter.md)


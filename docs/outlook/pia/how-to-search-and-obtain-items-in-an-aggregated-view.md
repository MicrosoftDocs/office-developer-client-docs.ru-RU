---
title: Поиск и получение элементов в общем представлении
TOCTitle: Search and obtain items in an aggregated view
ms:assetid: 1a875dc8-dd52-4e9c-b292-5f6ba3d7a940
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184592(v=office.15)
ms:contentKeyID: 55119925
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 92f99069dae2976a00ac075f605754fe8704ae60
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32342765"
---
# <a name="search-and-obtain-items-in-an-aggregated-view"></a><span data-ttu-id="1065f-102">Поиск и получение элементов в общем представлении</span><span class="sxs-lookup"><span data-stu-id="1065f-102">Search and obtain items in an aggregated view</span></span>

<span data-ttu-id="1065f-103">В этом примере показано, как искать элементы в разных папках и хранилищах и возвращать эти элементы в объединенном табличном представлении.</span><span class="sxs-lookup"><span data-stu-id="1065f-103">This example shows how to search for items in multiple folders and stores and to return those items in an aggregated table view.</span></span>

## <a name="example"></a><span data-ttu-id="1065f-104">Пример</span><span class="sxs-lookup"><span data-stu-id="1065f-104">Example</span></span>

<span data-ttu-id="1065f-p101">Метод [GetTable()](https://msdn.microsoft.com/library/ff184699\(v=office.15\)) объекта [TableView](https://msdn.microsoft.com/library/bb608854\(v=office.15\)) может возвратить в агрегированном представлении объект [Table](https://msdn.microsoft.com/library/bb652856\(v=office.15\)) , содержащий элементы из одной или нескольких папок одного хранилища или охватывающий несколько хранилищ. Это особенно полезно, если нужен доступ к элементам, возвращенным в результате поиска (например, при поиске всех почтовых элементов в хранилище). В данном разделе показан пример использования функции **Мгновенный поиск** для поиска всех элементов, полученных от руководителя текущего пользователя и помеченных как важные, и последующего отображения темы каждого результата поиска.</span><span class="sxs-lookup"><span data-stu-id="1065f-p101">The [GetTable()](https://msdn.microsoft.com/library/ff184699\(v=office.15\)) method of the [TableView](https://msdn.microsoft.com/library/bb608854\(v=office.15\)) object can return, in an aggregated view, a [Table](https://msdn.microsoft.com/library/bb652856\(v=office.15\)) object that contains items from one or more folders in the same store or spanning over multiple stores. This is particularly useful when you want to access items returned from a search (for example, a search on all mail items in a store). This topic shows an example of how to use **Instant Search** to search for all items received from the manager of the current user that are marked important, and then display the subject of each search result.</span></span>

<span data-ttu-id="1065f-108">В следующем примере кода метод **GetItemsInView** проверяет, является ли учетная запись основного хранилища доставки текущего пользователя учетной записью Exchange, есть ли у текущего пользователя руководитель и работает ли **Мгновенный поиск** в хранилище по умолчанию этого сеанса.</span><span class="sxs-lookup"><span data-stu-id="1065f-108">In the following code example, the **GetItemsInView** method checks whether the current user’s primary delivery store account is an Exchange account, whether the current user has a manager, and whether **Instant Search** is operational in the default store of the session.</span></span> <span data-ttu-id="1065f-109">Так как поиск использует метод [Search](https://msdn.microsoft.com/library/bb610561\(v=office.15\)) объекта [Explorer](https://msdn.microsoft.com/library/bb623678\(v=office.15\)), и результаты поиска получаются с помощью метода **GetTable**, **GetItemsInView** создает объект **Explorer**, отображает папку "Входящие" в этом объекте и использует его для настройки поиска.</span><span class="sxs-lookup"><span data-stu-id="1065f-109">Because the search relies on the [Search](https://msdn.microsoft.com/library/bb610561\(v=office.15\)) method of the [Explorer](https://msdn.microsoft.com/library/bb623678\(v=office.15\)) object, and the search result is obtained by using the **GetTable** method, **GetItemsInView** creates an **Explorer** object, displays the Inbox in this object, and uses it to set up the search.</span></span> 

<span data-ttu-id="1065f-110">**GetItemsInView** выполняет поиск во всех папках типа [MailItem](https://msdn.microsoft.com/library/bb643865\(v=office.15\)) для элементов, полученных от руководителя текущего пользователя и помеченных как важные.</span><span class="sxs-lookup"><span data-stu-id="1065f-110">**GetItemsInView** searches all folders of the [MailItem](https://msdn.microsoft.com/library/bb643865\(v=office.15\)) type for items from the current user's manager that are marked as important.</span></span> <span data-ttu-id="1065f-111">Затем **GetItemsInView** вызывает метод [Search](https://msdn.microsoft.com/library/bb610561\(v=office.15\)), все результаты поиска отображаются в проводнике, включая элементы из других папок и хранилищ, соответствующих условиям поиска.</span><span class="sxs-lookup"><span data-stu-id="1065f-111">After **GetItemsInView** calls the [Search](https://msdn.microsoft.com/library/bb610561\(v=office.15\)) method, any search results are displayed in the Explorer, including items from other folders and stores that meet the search criteria.</span></span> <span data-ttu-id="1065f-112">**GetItemsInView** получает объект **TableView**, содержащий это представление результатов поиска в проводнике.</span><span class="sxs-lookup"><span data-stu-id="1065f-112">**GetItemsInView** gets a **TableView** object that contains this explorer view of the search results.</span></span> <span data-ttu-id="1065f-113">Используя метод **GetTable** этого объекта **TableView**, **GetItemsInView** далее получает объект **Table**, содержащий агрегированные элементы, возвращенные при поиске.</span><span class="sxs-lookup"><span data-stu-id="1065f-113">By using the **GetTable** method of this **TableView** object, **GetItemsInView** then gets a **Table** object that contains the aggregated items returned from the search.</span></span> <span data-ttu-id="1065f-114">Наконец, **GetItemsInView** отображает столбец темы каждой строки объекта **Table**, который представляет элемент в результатах поиска.</span><span class="sxs-lookup"><span data-stu-id="1065f-114">Finally **GetItemsInView** displays the subject column of each row of the **Table** object that represents an item in the search results.</span></span>

<span data-ttu-id="1065f-115">Если вы используете Visual Studio для тестирования этого примера кода, сначала добавьте ссылку на компонент Microsoft Outlook 15.0 Object Library и задайте переменную Outlook при импорте пространства имен **Microsoft.Office.Interop.Outlook**.</span><span class="sxs-lookup"><span data-stu-id="1065f-115">If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the Outlook variable when you import the **Microsoft.Office.Interop.Outlook** namespace.</span></span> <span data-ttu-id="1065f-116">Инструкция **using** не должна находиться непосредственно перед функциями в примере кода, но ее нужно добавить перед объявлением общедоступного класса.</span><span class="sxs-lookup"><span data-stu-id="1065f-116">The **using** statement must not occur directly before the functions in the code example but must be added before the public Class declaration.</span></span> <span data-ttu-id="1065f-117">В приведенной ниже строке кода показано, как выполнить импорт и назначение на языке C\#.</span><span class="sxs-lookup"><span data-stu-id="1065f-117">The following line of code shows how to do the import and assignment in C\#.</span></span>

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

## <a name="see-also"></a><span data-ttu-id="1065f-118">См. также</span><span class="sxs-lookup"><span data-stu-id="1065f-118">See also</span></span>

- [<span data-ttu-id="1065f-119">Поиск и фильтрация</span><span class="sxs-lookup"><span data-stu-id="1065f-119">Search and filter</span></span>](search-and-filter.md)


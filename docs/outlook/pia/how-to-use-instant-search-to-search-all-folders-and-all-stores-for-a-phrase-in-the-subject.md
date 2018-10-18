---
title: Поиск фразы в теме во всех папках и хранилищах с помощью быстрого поиска
TOCTitle: Use instant search to search all folders and all stores for a phrase in the subject
ms:assetid: d3152bfa-6e7d-4b68-8c7e-e2e155a92b49
ms:mtpsurl: https://msdn.microsoft.com/library/Ff424478(v=office.15)
ms:contentKeyID: 55119923
ms.date: 07/24/2014
mtps_version: v=office.15
ms.openlocfilehash: 3e6e8199df6c04ba5a78ed5611aaaf016a71226d
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25407018"
---
# <a name="use-instant-search-to-search-all-folders-and-all-stores-for-a-phrase-in-the-subject"></a><span data-ttu-id="b876a-102">Поиск фразы в теме во всех папках и хранилищах с помощью быстрого поиска</span><span class="sxs-lookup"><span data-stu-id="b876a-102">Use instant search to search all folders and all stores for a phrase in the subject</span></span>

<span data-ttu-id="b876a-103">В этом примере с помощью компонента мгновенного поиска выполняется поиск фразы в теме во всех папках и хранилищах с последующим отображением элементов в окне проводника.</span><span class="sxs-lookup"><span data-stu-id="b876a-103">This example uses Instant Search to search all folders and all stores for a phrase in the subject, and then displays the items in an explorer window.</span></span>

## <a name="example"></a><span data-ttu-id="b876a-104">Пример</span><span class="sxs-lookup"><span data-stu-id="b876a-104">Example</span></span>

> [!NOTE] 
> <span data-ttu-id="b876a-105">Приведенный ниже пример кода представляет собой фрагмент из книги [Программирование приложений для Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).</span><span class="sxs-lookup"><span data-stu-id="b876a-105">The following code example is an excerpt from  [Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493)  , from Microsoft Press (ISBN 9780735622494, copyright Microsoft Press 2007, all rights reserved).</span></span>

<span data-ttu-id="b876a-106">Быстрый поиск — это функция Microsoft Outlook, позволяющая выполнять поиск с помощью запросов, которые возвращают результаты на основе содержимого.</span><span class="sxs-lookup"><span data-stu-id="b876a-106">Instant Search is a feature of Microsoft Outlook that enables you to search by issuing queries that return results based on the content.</span></span> <span data-ttu-id="b876a-107">После обработки запроса результаты могут возвращаться в различные объекты, включая объект [Table](https://msdn.microsoft.com/library/bb652856\(v=office.15\)), коллекцию [Items](https://msdn.microsoft.com/library/bb645287\(v=office.15\)) и объект [Search](https://msdn.microsoft.com/library/bb612611\(v=office.15\)).</span><span class="sxs-lookup"><span data-stu-id="b876a-107">Once your query has been processed, the results can be returned in a variety of objects, including the [Table](https://msdn.microsoft.com/library/bb652856\(v=office.15\)) object, the [Items](https://msdn.microsoft.com/library/bb645287\(v=office.15\)) collection, and the [Search](https://msdn.microsoft.com/library/bb612611\(v=office.15\)) object.</span></span> <span data-ttu-id="b876a-108">Код, использующий быстрый поиск, можно написать с помощью расширенного синтаксиса запросов (AQS), предлагаемого панелью поиска Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="b876a-108">You can write code that uses Instant Search by using the Advanced Query Syntax (AQS) that is offered by Microsoft Windows Desktop Search.</span></span> <span data-ttu-id="b876a-109">AQS — один из трех языков запросов, поддерживаемых в Outlook.</span><span class="sxs-lookup"><span data-stu-id="b876a-109">AQS is one of three query languages that Outlook supports.</span></span> <span data-ttu-id="b876a-110">Он эффективен, но ограничен методом [Search(String, OlSearchScope)](https://msdn.microsoft.com/library/bb610561\(v=office.15\)) объекта [Explorer](https://msdn.microsoft.com/library/bb623678\(v=office.15\)).</span><span class="sxs-lookup"><span data-stu-id="b876a-110">It is powerful, but limited to the [Search(String, OlSearchScope)](https://msdn.microsoft.com/library/bb610561\(v=office.15\)) method of the [Explorer](https://msdn.microsoft.com/library/bb623678\(v=office.15\)) object.</span></span> <span data-ttu-id="b876a-111">С помощью языка AQS нельзя обеспечить ограничение для объектов **Table** или **Item**.</span><span class="sxs-lookup"><span data-stu-id="b876a-111">You cannot use AQS to provide a restriction for **Table** or **Item** objects.</span></span> <span data-ttu-id="b876a-112">Кроме того, результаты, возвращенные запросом AQS, могут отображаться только в пользовательском интерфейсе Outlook.</span><span class="sxs-lookup"><span data-stu-id="b876a-112">In addition, the results returned by an AQS query can be displayed only in the Outlook user interface.</span></span> <span data-ttu-id="b876a-113">В следующей таблице перечислены три языка запросов, поддерживаемые в Outlook, но в этой статье демонстрируется только использование языка AQS.</span><span class="sxs-lookup"><span data-stu-id="b876a-113">The following table lists the three query languages that Outlook supports; however, this topic will illustrate the use of only AQS.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="b876a-114">Язык запроса</span><span class="sxs-lookup"><span data-stu-id="b876a-114">Query language</span></span></p></th>
<th><p><span data-ttu-id="b876a-115">Описание</span><span class="sxs-lookup"><span data-stu-id="b876a-115">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b876a-116">AQS</span><span class="sxs-lookup"><span data-stu-id="b876a-116">AQS</span></span></p></td>
<td><p><span data-ttu-id="b876a-117">Язык AQS используется в панели поиска Windows, а также в качестве языка запросов для компонента мгновенного поиска в приложении Outlook.</span><span class="sxs-lookup"><span data-stu-id="b876a-117">AQS is used by Windows Desktop Search and is the query language for the Instant Search feature in Outlook.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b876a-118">DASL</span><span class="sxs-lookup"><span data-stu-id="b876a-118">DASL</span></span></p></td>
<td><p><span data-ttu-id="b876a-p102">Язык запросов поиска и обнаружения DAV (DASL) построен на основе реализации Microsoft Exchange для языка DASL в приложении Outlook. Язык DASL можно использовать для возврата результатов в объекте <b>Table</b>. </span><span class="sxs-lookup"><span data-stu-id="b876a-p102">DAV Search and Locating (DASL) query language is based on the Microsoft Exchange implementation of DASL in Outlook. DASL can be used to return results in the <b>Table</b> object.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b876a-121">Jet</span><span class="sxs-lookup"><span data-stu-id="b876a-121">Jet</span></span></p></td>
<td><p><span data-ttu-id="b876a-p103">Jet — это простой язык запросов для приложения Outlook, построенный на основе службы Microsoft Jet Expression Service. Язык Jet используется для создания строк фильтра для методов <b>Restrict</b> коллекции <b>Items</b> и объекта <b>Table</b>.</span><span class="sxs-lookup"><span data-stu-id="b876a-p103">Jet query language provides a simple query language for Outlook, and is based on the Microsoft Jet Expression Service. Jet is used to create filter strings for the <b>Restrict</b> methods of the <b>Items</b> collection and the <b>Table</b> object.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="b876a-124">В следующем примере кода процедура DemoInstantSearch получает все папки сообщений во всех хранилищах, для которых включена индексация с помощью свойства [IsInstantSearchEnabled](https://msdn.microsoft.com/library/bb609793\(v=office.15\)) объекта [Store](https://msdn.microsoft.com/library/bb609139\(v=office.15\)).</span><span class="sxs-lookup"><span data-stu-id="b876a-124">In the following code example,   gets all mail folders in all stores where indexing is enabled by using the IsInstantSearchEnabled property of the Store object.</span></span> <span data-ttu-id="b876a-125">После этого с помощью метода **Search** объекта **Explorer** выполняется фильтрация всех полученных за последний месяц элементов, содержащих фразу "Office 2007" целиком в строке темы.</span><span class="sxs-lookup"><span data-stu-id="b876a-125">It then uses the **Search** method of the **Explorer** object to filter for all items that contain the exact phrase "Office 2007" in the subject and that have been received in the last month.</span></span> <span data-ttu-id="b876a-126">В конце результаты поиска отображаются в отдельном окне проводника.</span><span class="sxs-lookup"><span data-stu-id="b876a-126">The results of the search are finally displayed in a separate explorer window.</span></span>

<span data-ttu-id="b876a-127">Если вы используете Visual Studio для тестирования этого примера кода, сначала добавьте ссылку на компонент Microsoft Outlook 15.0 Object Library и задайте переменную Outlook при импорте пространства имен **Microsoft.Office.Interop.Outlook**.</span><span class="sxs-lookup"><span data-stu-id="b876a-127">If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the   variable when you import the Microsoft.Office.Interop.Outlook namespace.</span></span> <span data-ttu-id="b876a-128">Инструкция **using** не должна идти непосредственно перед функциями в примере кода, но ее нужно добавить перед объявлением public Class.</span><span class="sxs-lookup"><span data-stu-id="b876a-128">The using statement must not occur directly before the functions in the code example but must be added before the public   declaration.</span></span> <span data-ttu-id="b876a-129">В следующей строке кода показано, как выполнить импорт и назначение в C\#.</span><span class="sxs-lookup"><span data-stu-id="b876a-129">The following line of code shows how to do the import and assignment in C#.</span></span>

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```csharp
private void DemoInstantSearch()
{
    if (Application.Session.DefaultStore.IsInstantSearchEnabled)
    {
        Outlook.Explorer explorer = Application.Explorers.Add(
            Application.Session.GetDefaultFolder(
            Outlook.OlDefaultFolders.olFolderInbox)
            as Outlook.Folder,
            Outlook.OlFolderDisplayMode.olFolderDisplayNormal);
        string filter = "subject:" +
            "\"" + "Office 2007" + "\"" +
            " received:(last month)";
        explorer.Search(filter,
            Outlook.OlSearchScope.olSearchScopeAllFolders);
        explorer.Display();
    }
}
```

## <a name="see-also"></a><span data-ttu-id="b876a-130">См. также</span><span class="sxs-lookup"><span data-stu-id="b876a-130">See also</span></span>

- [<span data-ttu-id="b876a-131">Поиск и фильтрация</span><span class="sxs-lookup"><span data-stu-id="b876a-131">Search and Filter</span></span>](search-and-filter.md)


---
title: Подписка на RSS-канал
TOCTitle: Subscribe to an RSS feed
ms:assetid: 7ecefbcd-1a34-48e8-afac-7d54e79fd159
ms:mtpsurl: https://msdn.microsoft.com/library/Ff424473(v=office.15)
ms:contentKeyID: 55119852
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: b92c733c5030ce12eb691bba57afb5ce6b9d1dad
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32335401"
---
# <a name="subscribe-to-an-rss-feed"></a><span data-ttu-id="b31b9-102">Подписка на RSS-канал</span><span class="sxs-lookup"><span data-stu-id="b31b9-102">Subscribe to an RSS feed</span></span>

<span data-ttu-id="b31b9-103">В этом примере показано, как подписаться на RSS-канал с помощью метода [OpenSharedFolder(String, Object, Object, Object)](https://msdn.microsoft.com/library/bb610157\(v=office.15\)).</span><span class="sxs-lookup"><span data-stu-id="b31b9-103">This example shows how to subscribe to an RSS feed by using the [OpenSharedFolder(String, Object, Object, Object)](https://msdn.microsoft.com/library/bb610157\(v=office.15\)) method.</span></span>

## <a name="example"></a><span data-ttu-id="b31b9-104">Пример</span><span class="sxs-lookup"><span data-stu-id="b31b9-104">Example</span></span>

> [!NOTE] 
> <span data-ttu-id="b31b9-105">Приведенный ниже пример кода представляет собой фрагмент из книги [Программирование приложений для Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).</span><span class="sxs-lookup"><span data-stu-id="b31b9-105">The following code example is an excerpt from [Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).</span></span>

<span data-ttu-id="b31b9-p101">В объектной модели Outlook поддерживается предоставление доступа к общим данным, таким как интернет-календари, RSS-каналы и данные в списках и библиотеках документов Microsoft SharePoint. При этом поддерживается подключение к этим общим источникам данных и настройка контекстов синхронизации для непрерывного опроса таких источников. В объектной модели Outlook реализован метод [OpenSharedFolder(String, Object, Object, Object)](https://msdn.microsoft.com/library/bb610157\(v=office.15\)) объекта [NameSpace](https://msdn.microsoft.com/library/bb645857\(v=office.15\)), обеспечивающий загрузку и синхронизацию для конкретного типа общих папок.</span><span class="sxs-lookup"><span data-stu-id="b31b9-p101">The Outlook object model supports providing access to shared data, such as Internet calendars, RSS feeds, and data from Microsoft SharePoint lists and document libraries. It enables connecting to these shared sources of data and setting up the synchronization contexts to continue to poll those shared resources. The Outlook object model provides the [OpenSharedFolder(String, Object, Object, Object)](https://msdn.microsoft.com/library/bb610157\(v=office.15\)) method of the [NameSpace](https://msdn.microsoft.com/library/bb645857\(v=office.15\)) object to download and synchronize with a particular type of shared folder.</span></span>

<span data-ttu-id="b31b9-p102">В следующем примере выполняется подписка AddRssFeed на новый RSS-канал с именем "Example RSS Feed". Для этого вызывается метод **OpenSharedFolder** с URL-адресом, указывающим на этот RSS-канал. Последним двум параметрам метода **OpenSharedFolder** присваиваются значения **true**, которые определяют необходимость загрузки вложений, а также использование в приложении Outlook частоты обновления, заданной в RSS-канале.</span><span class="sxs-lookup"><span data-stu-id="b31b9-p102">In the following example, AddRssFeed subscribes to a new RSS feed named “Example RSS Feed” by calling the **OpenSharedFolder** method with a URL that refers to the new RSS feed. The last two parameters of **OpenSharedFolder** method are set to **true** to indicate that attachments should be downloaded, and Outlook should use the refresh ratio provided in the RSS feed.</span></span>


> [!NOTE]
> <span data-ttu-id="b31b9-111">Необходимо указать правильный обработчик протокола для URL-адреса папки в методе **OpenSharedFolder**, чтобы подписаться на RSS-канал.</span><span class="sxs-lookup"><span data-stu-id="b31b9-111">You must specify the correct protocol handler for the folder URL in the **OpenSharedFolder** method to subscribe to an RSS feed.</span></span> <span data-ttu-id="b31b9-112">Например, необходимо использовать URL-адрес, который начинается с `feed://` вместо `https://`.</span><span class="sxs-lookup"><span data-stu-id="b31b9-112">For example, you must use a URL that begins with `feed://` instead of `https://`.</span></span> <span data-ttu-id="b31b9-113">Outlook не может открывать RSS-каналы, которые требуют проверки подлинности, если недоступна проверка подлинности диспетчера локальной сети Windows NT (NTLM), и не может загружать RSS-каналы из расположений Secure Sockets Layer (SSL).</span><span class="sxs-lookup"><span data-stu-id="b31b9-113">Outlook cannot open RSS feeds that require authentication unless Windows NT LAN Manager (NTLM) authentication is available, and it cannot load RSS feeds from Secure Sockets Layer (SSL) locations.</span></span>

<span data-ttu-id="b31b9-114">Если вы используете Visual Studio для тестирования этого примера кода, сначала добавьте ссылку на компонент Microsoft Outlook 15.0 Object Library и задайте переменную Outlook при импорте пространства имен **Microsoft.Office.Interop.Outlook**.</span><span class="sxs-lookup"><span data-stu-id="b31b9-114">If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the Outlook variable when you import the **Microsoft.Office.Interop.Outlook** namespace.</span></span> <span data-ttu-id="b31b9-115">Инструкция **using** не должна находиться непосредственно перед функциями в примере кода, но ее нужно добавить перед объявлением общедоступного класса.</span><span class="sxs-lookup"><span data-stu-id="b31b9-115">The **using** statement must not occur directly before the functions in the code example but must be added before the public Class declaration.</span></span> <span data-ttu-id="b31b9-116">В приведенной ниже строке кода показано, как выполнить импорт и назначение на языке C\#.</span><span class="sxs-lookup"><span data-stu-id="b31b9-116">The following line of code shows how to do the import and assignment in C\#.</span></span>

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```csharp
private void AddRssFeed()
{
    string feedUrl = "feed://example.org/rssfeed.xml";
    Outlook.Folder subscriptionFolder =
        Application.Session.OpenSharedFolder(feedUrl, "Example RSS Feed", true, true) as Outlook.Folder;
    Outlook.Explorer exp =
        Application.Explorers.Add(subscriptionFolder, Outlook.OlFolderDisplayMode.olFolderDisplayNormal);
    exp.Display();
}
```

## <a name="see-also"></a><span data-ttu-id="b31b9-117">См. также</span><span class="sxs-lookup"><span data-stu-id="b31b9-117">See also</span></span>

- [<span data-ttu-id="b31b9-118">Совместное использование групп</span><span class="sxs-lookup"><span data-stu-id="b31b9-118">Group sharing</span></span>](group-sharing.md)


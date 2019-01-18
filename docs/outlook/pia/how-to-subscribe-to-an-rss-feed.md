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
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28718191"
---
# <a name="subscribe-to-an-rss-feed"></a>Подписка на RSS-канал

В этом примере показано, как подписаться на RSS-канал с помощью метода [OpenSharedFolder(String, Object, Object, Object)](https://msdn.microsoft.com/library/bb610157\(v=office.15\)).

## <a name="example"></a>Пример

> [!NOTE] 
> Приведенный ниже пример кода представляет собой фрагмент из книги [Программирование приложений для Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).

В объектной модели Outlook поддерживается предоставление доступа к общим данным, таким как интернет-календари, RSS-каналы и данные в списках и библиотеках документов Microsoft SharePoint. При этом поддерживается подключение к этим общим источникам данных и настройка контекстов синхронизации для непрерывного опроса таких источников. В объектной модели Outlook реализован метод [OpenSharedFolder(String, Object, Object, Object)](https://msdn.microsoft.com/library/bb610157\(v=office.15\)) объекта [NameSpace](https://msdn.microsoft.com/library/bb645857\(v=office.15\)), обеспечивающий загрузку и синхронизацию для конкретного типа общих папок.

В следующем примере выполняется подписка AddRssFeed на новый RSS-канал с именем "Example RSS Feed". Для этого вызывается метод **OpenSharedFolder** с URL-адресом, указывающим на этот RSS-канал. Последним двум параметрам метода **OpenSharedFolder** присваиваются значения **true**, которые определяют необходимость загрузки вложений, а также использование в приложении Outlook частоты обновления, заданной в RSS-канале.


> [!NOTE]
> Необходимо указать правильный обработчик протокола для URL-адреса папки в методе **OpenSharedFolder**, чтобы подписаться на RSS-канал. Например, необходимо использовать URL-адрес, который начинается с `feed://` вместо `https://`. Outlook не может открывать RSS-каналы, которые требуют проверки подлинности, если недоступна проверка подлинности диспетчера локальной сети Windows NT (NTLM), и не может загружать RSS-каналы из расположений Secure Sockets Layer (SSL).

Если вы используете Visual Studio для тестирования этого примера кода, сначала добавьте ссылку на компонент Microsoft Outlook 15.0 Object Library и задайте переменную Outlook при импорте пространства имен **Microsoft.Office.Interop.Outlook**. Инструкция **using** не должна идти непосредственно перед функциями в примере кода, но ее нужно добавить перед открытым объявлением Class. В следующей строке кода показано, как выполнить импорт и назначение в C\#.

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

## <a name="see-also"></a>См. также

- [Совместное использование групп](group-sharing.md)


---
title: Поиск фразы в теме во всех папках и хранилищах с помощью быстрого поиска
TOCTitle: Use instant search to search all folders and all stores for a phrase in the subject
ms:assetid: d3152bfa-6e7d-4b68-8c7e-e2e155a92b49
ms:mtpsurl: https://msdn.microsoft.com/library/Ff424478(v=office.15)
ms:contentKeyID: 55119923
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 07b0ba7a1d488dc1c7e1fcf0e9ae487b04b88755
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28709441"
---
# <a name="use-instant-search-to-search-all-folders-and-all-stores-for-a-phrase-in-the-subject"></a>Поиск фразы в теме во всех папках и хранилищах с помощью быстрого поиска

В этом примере с помощью компонента мгновенного поиска выполняется поиск фразы в теме во всех папках и хранилищах с последующим отображением элементов в окне проводника.

## <a name="example"></a>Пример

> [!NOTE] 
> Приведенный ниже пример кода представляет собой фрагмент из книги [Программирование приложений для Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).

Быстрый поиск — это функция Microsoft Outlook, позволяющая выполнять поиск с помощью запросов, которые возвращают результаты на основе содержимого. После обработки запроса результаты могут возвращаться в различные объекты, включая объект [Table](https://msdn.microsoft.com/library/bb652856\(v=office.15\)), коллекцию [Items](https://msdn.microsoft.com/library/bb645287\(v=office.15\)) и объект [Search](https://msdn.microsoft.com/library/bb612611\(v=office.15\)). Код, использующий быстрый поиск, можно написать с помощью расширенного синтаксиса запросов (AQS), предлагаемого панелью поиска Microsoft Windows. AQS — один из трех языков запросов, поддерживаемых в Outlook. Он эффективен, но ограничен методом [Search(String, OlSearchScope)](https://msdn.microsoft.com/library/bb610561\(v=office.15\)) объекта [Explorer](https://msdn.microsoft.com/library/bb623678\(v=office.15\)). С помощью языка AQS нельзя обеспечить ограничение для объектов **Table** или **Item**. Кроме того, результаты, возвращенные запросом AQS, могут отображаться только в пользовательском интерфейсе Outlook. В следующей таблице перечислены три языка запросов, поддерживаемые в Outlook, но в этой статье демонстрируется только использование языка AQS.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Язык запроса</p></th>
<th><p>Описание</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>AQS</p></td>
<td><p>Язык AQS используется в панели поиска Windows, а также в качестве языка запросов для компонента мгновенного поиска в приложении Outlook.</p></td>
</tr>
<tr class="even">
<td><p>DASL</p></td>
<td><p>Язык запросов поиска и обнаружения DAV (DASL) построен на основе реализации Microsoft Exchange для языка DASL в приложении Outlook. Язык DASL можно использовать для возврата результатов в объекте <b>Table</b>. </p></td>
</tr>
<tr class="odd">
<td><p>Jet</p></td>
<td><p>Jet — это простой язык запросов для приложения Outlook, построенный на основе службы Microsoft Jet Expression Service. Язык Jet используется для создания строк фильтра для методов <b>Restrict</b> коллекции <b>Items</b> и объекта <b>Table</b>.</p></td>
</tr>
</tbody>
</table>


В следующем примере кода процедура DemoInstantSearch получает все папки сообщений во всех хранилищах, для которых включена индексация с помощью свойства [IsInstantSearchEnabled](https://msdn.microsoft.com/library/bb609793\(v=office.15\)) объекта [Store](https://msdn.microsoft.com/library/bb609139\(v=office.15\)). После этого с помощью метода **Search** объекта **Explorer** выполняется фильтрация всех полученных за последний месяц элементов, содержащих фразу "Office 2007" целиком в строке темы. В конце результаты поиска отображаются в отдельном окне проводника.

Если вы используете Visual Studio для тестирования этого примера кода, сначала добавьте ссылку на компонент Microsoft Outlook 15.0 Object Library и задайте переменную Outlook при импорте пространства имен **Microsoft.Office.Interop.Outlook**. Инструкция **using** не должна идти непосредственно перед функциями в примере кода, но ее нужно добавить перед объявлением public Class. В следующей строке кода показано, как выполнить импорт и назначение в C\#.

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

## <a name="see-also"></a>См. также

- [Поиск и фильтрация](search-and-filter.md)


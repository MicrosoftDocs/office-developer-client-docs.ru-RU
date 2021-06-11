---
title: Поддержка поиска в поставщиках магазинов сообщений
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 30a3fe28-31ca-4eb8-9353-f75f6d339dc7
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 545047e90346b0f8e4a88eabcb20573f663f6d02
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425388"
---
# <a name="supporting-searches-in-message-store-providers"></a><span data-ttu-id="786f9-103">Поддержка поиска в поставщиках магазинов сообщений</span><span class="sxs-lookup"><span data-stu-id="786f9-103">Supporting Searches in Message Store Providers</span></span>

  
  
<span data-ttu-id="786f9-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="786f9-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="786f9-105">Клиентские приложения часто имеют некоторые компоненты пользовательского интерфейса, посвященные поиску сообщений в хранилище сообщений.</span><span class="sxs-lookup"><span data-stu-id="786f9-105">Client applications frequently have some user interface components devoted to searching for messages in a message store.</span></span> <span data-ttu-id="786f9-106">Критерии поиска указаны в [интерфейсе IMAPIContainer : IMAPIProp](imapicontainerimapiprop.md) с помощью методов [IMAPIContainer::SetSearchCriteria](imapicontainer-setsearchcriteria.md) и [IMAPIContainer::GetSearchCriteria.](imapicontainer-getsearchcriteria.md)</span><span class="sxs-lookup"><span data-stu-id="786f9-106">Search criteria are specified in the [IMAPIContainer : IMAPIProp](imapicontainerimapiprop.md) interface by means of the [IMAPIContainer::SetSearchCriteria](imapicontainer-setsearchcriteria.md) and [IMAPIContainer::GetSearchCriteria](imapicontainer-getsearchcriteria.md) methods.</span></span> 
  
<span data-ttu-id="786f9-107">Клиенты используют свойство PR_FINDER_ENTRYID объекта хранения **сообщений** [(PidTagFinderEntryId)](pidtagfinderentryid-canonical-property.md)для идентификации корневой папки в хранилище сообщений, содержащем папки для результатов поиска.</span><span class="sxs-lookup"><span data-stu-id="786f9-107">Clients use the message store object's **PR_FINDER_ENTRYID** ([PidTagFinderEntryId](pidtagfinderentryid-canonical-property.md)) property to identify the root folder in the message store that contains folders for search results.</span></span> <span data-ttu-id="786f9-108">Папка результатов поиска часто является папкой на верхнем уровне магазина сообщений, которая не входит в дерево папок IPM и поэтому скрыта.</span><span class="sxs-lookup"><span data-stu-id="786f9-108">The search-results folder is often a folder at the top level of the message store that is not part of the IPM folder tree and is, therefore, hidden.</span></span>
  
<span data-ttu-id="786f9-109">Использует ли поставщик магазина сообщений постоянную папку результатов поиска или создает ее при  открываемом клиентом идентификаторе записи, хранящемся в свойстве PR_FINDER_ENTRYID, является деталью реализации.</span><span class="sxs-lookup"><span data-stu-id="786f9-109">Whether your message store provider uses a permanent search-results folder or creates one when a client opens the entry identifier stored in the **PR_FINDER_ENTRYID** property is an implementation detail.</span></span> <span data-ttu-id="786f9-110">Поставщику магазина сообщений несколько проще использовать постоянную папку, созданную при создании магазина сообщений, так как это позволяет избежать сложности проверки идентификатора записи при открываемой папке, чтобы узнать, следует ли создавать папку результатов поиска.</span><span class="sxs-lookup"><span data-stu-id="786f9-110">It is somewhat easier for your message store provider to use a permanent folder that is created when the message store is created, because doing so avoids the complication of checking the entry identifier whenever any folder is opened to see whether to create a search-results folder.</span></span> <span data-ttu-id="786f9-111">Однако не все поставщики магазинов сообщений могут это сделать; в частности, хранилища или хранилища сообщений только для чтения, которые предоставляют интерфейс MAPI в устаревшую базу данных, часто не допускаются или не могут создать постоянную папку результатов поиска в основном механизме хранения.</span><span class="sxs-lookup"><span data-stu-id="786f9-111">However, not all message store providers can do that; notably, read-only message stores or stores that provide a MAPI interface to a legacy database often are not allowed or are unable to create a permanent search-results folder in the underlying storage mechanism.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="786f9-112">См. также</span><span class="sxs-lookup"><span data-stu-id="786f9-112">See also</span></span>



[<span data-ttu-id="786f9-113">���������� ��������� ���������</span><span class="sxs-lookup"><span data-stu-id="786f9-113">Message Store Features</span></span>](message-store-features.md)


---
title: Поддержка поиска в поставщиках хранилищ сообщений
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
# <a name="supporting-searches-in-message-store-providers"></a><span data-ttu-id="a5908-103">Поддержка поиска в поставщиках хранилищ сообщений</span><span class="sxs-lookup"><span data-stu-id="a5908-103">Supporting Searches in Message Store Providers</span></span>

  
  
<span data-ttu-id="a5908-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a5908-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a5908-105">Для клиентских приложений часто используются некоторые компоненты пользовательского интерфейса, предназначенные для поиска сообщений в банке сообщений.</span><span class="sxs-lookup"><span data-stu-id="a5908-105">Client applications frequently have some user interface components devoted to searching for messages in a message store.</span></span> <span data-ttu-id="a5908-106">Условия поиска указываются в интерфейсе [IMAPIContainer: IMAPIProp](imapicontainerimapiprop.md) с помощью методов [IMAPIContainer:: сетсеарчкритериа](imapicontainer-setsearchcriteria.md) и [IMAPIContainer:: жетсеарчкритериа](imapicontainer-getsearchcriteria.md) .</span><span class="sxs-lookup"><span data-stu-id="a5908-106">Search criteria are specified in the [IMAPIContainer : IMAPIProp](imapicontainerimapiprop.md) interface by means of the [IMAPIContainer::SetSearchCriteria](imapicontainer-setsearchcriteria.md) and [IMAPIContainer::GetSearchCriteria](imapicontainer-getsearchcriteria.md) methods.</span></span> 
  
<span data-ttu-id="a5908-107">Клиенты используют свойство **пр_финдер_ентрид** ([PidTagFinderEntryId](pidtagfinderentryid-canonical-property.md)) объекта хранилища сообщений для определения корневой папки в хранилище сообщений, содержащей папки для результатов поиска.</span><span class="sxs-lookup"><span data-stu-id="a5908-107">Clients use the message store object's **PR_FINDER_ENTRYID** ([PidTagFinderEntryId](pidtagfinderentryid-canonical-property.md)) property to identify the root folder in the message store that contains folders for search results.</span></span> <span data-ttu-id="a5908-108">Папка результатов поиска часто является папкой на верхнем уровне хранилища сообщений, которая не является частью дерева папок IPM и, следовательно, скрыта.</span><span class="sxs-lookup"><span data-stu-id="a5908-108">The search-results folder is often a folder at the top level of the message store that is not part of the IPM folder tree and is, therefore, hidden.</span></span>
  
<span data-ttu-id="a5908-109">Содержит ли поставщик хранилища сообщений постоянную папку результатов поиска или создает ее, когда клиент открывает идентификатор записи, хранящийся в свойстве **пр_финдер_ентрид** , — это сведения о реализации.</span><span class="sxs-lookup"><span data-stu-id="a5908-109">Whether your message store provider uses a permanent search-results folder or creates one when a client opens the entry identifier stored in the **PR_FINDER_ENTRYID** property is an implementation detail.</span></span> <span data-ttu-id="a5908-110">Для поставщика хранилища сообщений проще всего использовать постоянную папку, созданную при создании хранилища сообщений, так как это позволяет избежать необходимости проверки идентификатора записи всякий раз, когда открывается любая папка, чтобы определить, следует ли создать Папка результатов поиска.</span><span class="sxs-lookup"><span data-stu-id="a5908-110">It is somewhat easier for your message store provider to use a permanent folder that is created when the message store is created, because doing so avoids the complication of checking the entry identifier whenever any folder is opened to see whether to create a search-results folder.</span></span> <span data-ttu-id="a5908-111">Однако не все поставщики хранилищ сообщений могут делать это. как правило, хранилища сообщений только для чтения или хранилища, которые предоставляют интерфейс MAPI для устаревшей базы данных, недопустимы или не могут создавать постоянные папки результатов поиска в базовом механизме хранения.</span><span class="sxs-lookup"><span data-stu-id="a5908-111">However, not all message store providers can do that; notably, read-only message stores or stores that provide a MAPI interface to a legacy database often are not allowed or are unable to create a permanent search-results folder in the underlying storage mechanism.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="a5908-112">См. также</span><span class="sxs-lookup"><span data-stu-id="a5908-112">See also</span></span>



[<span data-ttu-id="a5908-113">���������� ��������� ���������</span><span class="sxs-lookup"><span data-stu-id="a5908-113">Message Store Features</span></span>](message-store-features.md)


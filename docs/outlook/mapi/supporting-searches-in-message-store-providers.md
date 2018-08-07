---
title: Поддержка поиска для поставщиков хранилищ сообщений
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 30a3fe28-31ca-4eb8-9353-f75f6d339dc7
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 0cd8bbe14e6af020ec5c93cd46a24853d1c8401c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19812433"
---
# <a name="supporting-searches-in-message-store-providers"></a><span data-ttu-id="d1a80-103">Поддержка поиска для поставщиков хранилищ сообщений</span><span class="sxs-lookup"><span data-stu-id="d1a80-103">Supporting Searches in Message Store Providers</span></span>

  
  
<span data-ttu-id="d1a80-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="d1a80-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="d1a80-105">Клиентские приложения часто имеют некоторые компоненты пользовательского интерфейса посвящен поиск сообщений в хранилище сообщений.</span><span class="sxs-lookup"><span data-stu-id="d1a80-105">Client applications frequently have some user interface components devoted to searching for messages in a message store.</span></span> <span data-ttu-id="d1a80-106">Условия поиска в [IMAPIContainer: IMAPIProp](imapicontainerimapiprop.md) интерфейса с помощью методов [IMAPIContainer::SetSearchCriteria](imapicontainer-setsearchcriteria.md) и [IMAPIContainer::GetSearchCriteria](imapicontainer-getsearchcriteria.md) .</span><span class="sxs-lookup"><span data-stu-id="d1a80-106">Search criteria are specified in the [IMAPIContainer : IMAPIProp](imapicontainerimapiprop.md) interface by means of the [IMAPIContainer::SetSearchCriteria](imapicontainer-setsearchcriteria.md) and [IMAPIContainer::GetSearchCriteria](imapicontainer-getsearchcriteria.md) methods.</span></span> 
  
<span data-ttu-id="d1a80-107">Клиенты используют свойство **PR_FINDER_ENTRYID** ([PidTagFinderEntryId](pidtagfinderentryid-canonical-property.md)) объектов хранилища сообщений для идентификации в корневой папке в хранилище сообщений, содержащая папки для результатов поиска.</span><span class="sxs-lookup"><span data-stu-id="d1a80-107">Clients use the message store object's **PR_FINDER_ENTRYID** ([PidTagFinderEntryId](pidtagfinderentryid-canonical-property.md)) property to identify the root folder in the message store that contains folders for search results.</span></span> <span data-ttu-id="d1a80-108">Папка результатов поиска часто — это папка на верхнем уровне хранилища сообщений, который не является частью дерева папок IPM и следовательно, скрыт.</span><span class="sxs-lookup"><span data-stu-id="d1a80-108">The search-results folder is often a folder at the top level of the message store that is not part of the IPM folder tree and is, therefore, hidden.</span></span>
  
<span data-ttu-id="d1a80-109">Использует постоянное результатов поиска папок ли поставщика хранилища сообщений или создает один, если это клиент открывает идентификатор записи, хранящиеся в свойстве **PR_FINDER_ENTRYID** это данные реализации.</span><span class="sxs-lookup"><span data-stu-id="d1a80-109">Whether your message store provider uses a permanent search-results folder or creates one when a client opens the entry identifier stored in the **PR_FINDER_ENTRYID** property is an implementation detail.</span></span> <span data-ttu-id="d1a80-110">Несколько более поставщика хранилища сообщений для использования в постоянную папку, которая создается при создании хранилища сообщений, так как это так позволяет избежать сложность проверки идентификатор записи при открытии любую папку для просмотра, следует ли создать Папка результатов поиска.</span><span class="sxs-lookup"><span data-stu-id="d1a80-110">It is somewhat easier for your message store provider to use a permanent folder that is created when the message store is created, because doing so avoids the complication of checking the entry identifier whenever any folder is opened to see whether to create a search-results folder.</span></span> <span data-ttu-id="d1a80-111">Тем не менее не все поставщики хранилища сообщений для этого; Прежде всего хранилища, которые часто предоставляет интерфейс MAPI для прежних версий базы данных или только для чтения сообщения не разрешены или не удается создать папку постоянное результатов поиска в базовый механизм хранения.</span><span class="sxs-lookup"><span data-stu-id="d1a80-111">However, not all message store providers can do that; notably, read-only message stores or stores that provide a MAPI interface to a legacy database often are not allowed or are unable to create a permanent search-results folder in the underlying storage mechanism.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="d1a80-112">См. также</span><span class="sxs-lookup"><span data-stu-id="d1a80-112">See also</span></span>



[<span data-ttu-id="d1a80-113">���������� ��������� ���������</span><span class="sxs-lookup"><span data-stu-id="d1a80-113">Message Store Features</span></span>](message-store-features.md)


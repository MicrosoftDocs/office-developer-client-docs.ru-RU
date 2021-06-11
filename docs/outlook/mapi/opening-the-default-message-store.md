---
title: Открытие хранилища сообщений по умолчанию
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 670fb896-9aaf-4a96-83f7-76237409e956
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: d8e620516e2b3e61cd07f3a08af989cc4ed5b61e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436029"
---
# <a name="opening-the-default-message-store"></a><span data-ttu-id="4510f-103">Открытие хранилища сообщений по умолчанию</span><span class="sxs-lookup"><span data-stu-id="4510f-103">Opening the default message store</span></span>

<span data-ttu-id="4510f-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4510f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4510f-105">В любом конкретном сеансе один магазин сообщений действует как хранилище сообщений по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="4510f-105">In any particular session, one message store acts as the default message store.</span></span> <span data-ttu-id="4510f-106">Хранилище сообщений по умолчанию имеет следующие характеристики:</span><span class="sxs-lookup"><span data-stu-id="4510f-106">A default message store has the following characteristics:</span></span>
  
- <span data-ttu-id="4510f-107">Свойство **PR_DEFAULT_STORE** [(PidTagDefaultStore)](pidtagdefaultstore-canonical-property.md)имеет свойство TRUE.</span><span class="sxs-lookup"><span data-stu-id="4510f-107">The **PR_DEFAULT_STORE** ([PidTagDefaultStore](pidtagdefaultstore-canonical-property.md)) property is set to TRUE.</span></span>
    
- <span data-ttu-id="4510f-108">Флаг STATUS_DEFAULT_STORE установлен в **свойстве PR_RESOURCE_FLAGS** [(PidTagResourceFlags).](pidtagresourceflags-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="4510f-108">The STATUS_DEFAULT_STORE flag is set in the **PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md)) property.</span></span>
    
- <span data-ttu-id="4510f-109">MAPI автоматически создает подтрий IPM и корневые папки для результатов поиска, общих представлений и личных представлений при открытие магазина сообщений.</span><span class="sxs-lookup"><span data-stu-id="4510f-109">MAPI automatically creates the IPM subtree and the root folders for search-results, common views and personal views when the message store is opened.</span></span> <span data-ttu-id="4510f-110">Дополнительные сведения об этих папках см. в специальной папке [IPM Subtree](ipm-subtree.md) и [MAPI.](mapi-special-folders.md)</span><span class="sxs-lookup"><span data-stu-id="4510f-110">For more information about these folders, see [IPM Subtree](ipm-subtree.md) and [MAPI Special Folders](mapi-special-folders.md).</span></span> 
    
<span data-ttu-id="4510f-111">Чтобы получить идентификатор записи для магазина сообщений по умолчанию, необходимо вызвать [IMAPISession::GetMsgStoresTable,](imapisession-getmsgstorestable.md) чтобы открыть таблицу хранения сообщений и применить соответствующее ограничение в вызове [в HrQueryAllRows](hrqueryallrows.md).</span><span class="sxs-lookup"><span data-stu-id="4510f-111">To retrieve the entry identifier for the default message store, you must call [IMAPISession::GetMsgStoresTable](imapisession-getmsgstorestable.md) to open the message store table and apply an appropriate restriction in a call to [HrQueryAllRows](hrqueryallrows.md).</span></span> <span data-ttu-id="4510f-112">**HrQueryAllRows** возвращает набор строк с одной строкой, представляюной хранилище сообщений по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="4510f-112">**HrQueryAllRows** will return a row set with the one row that represents the default message store.</span></span> <span data-ttu-id="4510f-113">Ограничение, которое вы передаете **в HrQueryAllRows,** может принимать одну из следующих форм:</span><span class="sxs-lookup"><span data-stu-id="4510f-113">The restriction that you pass to **HrQueryAllRows** can take on one of the following forms:</span></span> 
  
1. <span data-ttu-id="4510f-114">Ограничение **AND,** использующее **структуру SAndRestriction** для объединения:</span><span class="sxs-lookup"><span data-stu-id="4510f-114">An **AND** restriction that uses an **SAndRestriction** structure to combine:</span></span> 
    
   - <span data-ttu-id="4510f-115">Существует ограничение, использующее **структуру SExistRestriction** для проверки наличия **свойства** PR_DEFAULT_STORE.</span><span class="sxs-lookup"><span data-stu-id="4510f-115">An exists restriction that uses an **SExistRestriction** structure to test for the existence of the **PR_DEFAULT_STORE** property.</span></span> 
    
   - <span data-ttu-id="4510f-116">Ограничение свойства, использующее [структуру SPropertyRestriction](spropertyrestriction.md) для проверки значения TRUE в **свойстве** PR_DEFAULT_STORE.</span><span class="sxs-lookup"><span data-stu-id="4510f-116">A property restriction that uses an [SPropertyRestriction](spropertyrestriction.md) structure to check for the TRUE value in the **PR_DEFAULT_STORE** property.</span></span> 
    
2. <span data-ttu-id="4510f-117">Ограничение bitmask, использующее структуру [SBitMaskRestriction](sbitmaskrestriction.md) для применения STATUS_DEFAULT_STORE в качестве маски PR_RESOURCE_FLAGS **свойства.**</span><span class="sxs-lookup"><span data-stu-id="4510f-117">A bitmask restriction that uses an [SBitMaskRestriction](sbitmaskrestriction.md) structure for applying STATUS_DEFAULT_STORE as a mask against the **PR_RESOURCE_FLAGS** property.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="4510f-118">См. также</span><span class="sxs-lookup"><span data-stu-id="4510f-118">See also</span></span>

- [<span data-ttu-id="4510f-119">SExistRestriction</span><span class="sxs-lookup"><span data-stu-id="4510f-119">SExistRestriction</span></span>](sexistrestriction.md)
- [<span data-ttu-id="4510f-120">SAndRestriction</span><span class="sxs-lookup"><span data-stu-id="4510f-120">SAndRestriction</span></span>](sandrestriction.md)


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
# <a name="opening-the-default-message-store"></a><span data-ttu-id="667a5-103">Открытие хранилища сообщений по умолчанию</span><span class="sxs-lookup"><span data-stu-id="667a5-103">Opening the default message store</span></span>

<span data-ttu-id="667a5-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="667a5-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="667a5-105">В каждом конкретном сеансе одно хранилище сообщений действует как хранилище сообщений по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="667a5-105">In any particular session, one message store acts as the default message store.</span></span> <span data-ttu-id="667a5-106">Хранилище сообщений по умолчанию имеет следующие характеристики:</span><span class="sxs-lookup"><span data-stu-id="667a5-106">A default message store has the following characteristics:</span></span>
  
- <span data-ttu-id="667a5-107">Для свойства **PR_DEFAULT_STORE** ([PidTagDefaultStore](pidtagdefaultstore-canonical-property.md)) задано значение true.</span><span class="sxs-lookup"><span data-stu-id="667a5-107">The **PR_DEFAULT_STORE** ([PidTagDefaultStore](pidtagdefaultstore-canonical-property.md)) property is set to TRUE.</span></span>
    
- <span data-ttu-id="667a5-108">Флаг STATUS_DEFAULT_STORE задается в свойстве **PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="667a5-108">The STATUS_DEFAULT_STORE flag is set in the **PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md)) property.</span></span>
    
- <span data-ttu-id="667a5-109">MAPI автоматически создает поддерево IPM и корневые папки для результатов поиска, общих представлений и персональных представлений при открытии хранилища сообщений.</span><span class="sxs-lookup"><span data-stu-id="667a5-109">MAPI automatically creates the IPM subtree and the root folders for search-results, common views and personal views when the message store is opened.</span></span> <span data-ttu-id="667a5-110">Дополнительные сведения об этих папках можно найти в разделе [IPM subtree](ipm-subtree.md) и [специальные папки MAPI](mapi-special-folders.md).</span><span class="sxs-lookup"><span data-stu-id="667a5-110">For more information about these folders, see [IPM Subtree](ipm-subtree.md) and [MAPI Special Folders](mapi-special-folders.md).</span></span> 
    
<span data-ttu-id="667a5-111">Чтобы получить идентификатор записи для хранилища сообщений по умолчанию, необходимо вызвать [IMAPISession:: жетмсгсторестабле](imapisession-getmsgstorestable.md) , чтобы открыть таблицу "хранилище сообщений" и применить соответствующее ограничение в вызове [хркуеряллровс](hrqueryallrows.md).</span><span class="sxs-lookup"><span data-stu-id="667a5-111">To retrieve the entry identifier for the default message store, you must call [IMAPISession::GetMsgStoresTable](imapisession-getmsgstorestable.md) to open the message store table and apply an appropriate restriction in a call to [HrQueryAllRows](hrqueryallrows.md).</span></span> <span data-ttu-id="667a5-112">**Хркуеряллровс** будет возвращать набор строк с одной строкой, представляющей хранилище сообщений по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="667a5-112">**HrQueryAllRows** will return a row set with the one row that represents the default message store.</span></span> <span data-ttu-id="667a5-113">Ограничение, которое передается в **хркуеряллровс** , может принимать одну из следующих форм:</span><span class="sxs-lookup"><span data-stu-id="667a5-113">The restriction that you pass to **HrQueryAllRows** can take on one of the following forms:</span></span> 
  
1. <span data-ttu-id="667a5-114">Ограничение **, в котором** используется структура **сандрестриктион** для объединения:</span><span class="sxs-lookup"><span data-stu-id="667a5-114">An **AND** restriction that uses an **SAndRestriction** structure to combine:</span></span> 
    
   - <span data-ttu-id="667a5-115">Ограничение EXISTS, использующее структуру **сексистрестриктион** для проверки существования свойства **PR_DEFAULT_STORE** .</span><span class="sxs-lookup"><span data-stu-id="667a5-115">An exists restriction that uses an **SExistRestriction** structure to test for the existence of the **PR_DEFAULT_STORE** property.</span></span> 
    
   - <span data-ttu-id="667a5-116">Ограничение свойства, использующее структуру [спропертирестриктион](spropertyrestriction.md) для проверки истинности значения свойства **PR_DEFAULT_STORE** .</span><span class="sxs-lookup"><span data-stu-id="667a5-116">A property restriction that uses an [SPropertyRestriction](spropertyrestriction.md) structure to check for the TRUE value in the **PR_DEFAULT_STORE** property.</span></span> 
    
2. <span data-ttu-id="667a5-117">Ограничение битовой маски, использующее структуру [сбитмаскрестриктион](sbitmaskrestriction.md) для применения STATUS_DEFAULT_STORE в качестве маски к свойству **PR_RESOURCE_FLAGS** .</span><span class="sxs-lookup"><span data-stu-id="667a5-117">A bitmask restriction that uses an [SBitMaskRestriction](sbitmaskrestriction.md) structure for applying STATUS_DEFAULT_STORE as a mask against the **PR_RESOURCE_FLAGS** property.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="667a5-118">См. также</span><span class="sxs-lookup"><span data-stu-id="667a5-118">See also</span></span>

- [<span data-ttu-id="667a5-119">SExistRestriction</span><span class="sxs-lookup"><span data-stu-id="667a5-119">SExistRestriction</span></span>](sexistrestriction.md)
- [<span data-ttu-id="667a5-120">SAndRestriction</span><span class="sxs-lookup"><span data-stu-id="667a5-120">SAndRestriction</span></span>](sandrestriction.md)


---
title: Открытие хранилище сообщений по умолчанию
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 670fb896-9aaf-4a96-83f7-76237409e956
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 1eb4e150be68ea01060c7afaed489c8759b576db
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19810048"
---
# <a name="opening-the-default-message-store"></a><span data-ttu-id="db872-103">Открытие хранилище сообщений по умолчанию</span><span class="sxs-lookup"><span data-stu-id="db872-103">Opening the default message store</span></span>

<span data-ttu-id="db872-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="db872-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="db872-105">В любой определенным сеансом единое хранилище сообщений действует как хранилище сообщений по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="db872-105">In any particular session, one message store acts as the default message store.</span></span> <span data-ttu-id="db872-106">Хранилище сообщений по умолчанию имеет следующие характеристики:</span><span class="sxs-lookup"><span data-stu-id="db872-106">A default message store has the following characteristics:</span></span>
  
- <span data-ttu-id="db872-107">Свойство **PR_DEFAULT_STORE** ([PidTagDefaultStore](pidtagdefaultstore-canonical-property.md)) имеет значение TRUE.</span><span class="sxs-lookup"><span data-stu-id="db872-107">The **PR_DEFAULT_STORE** ([PidTagDefaultStore](pidtagdefaultstore-canonical-property.md)) property is set to TRUE.</span></span>
    
- <span data-ttu-id="db872-108">Флаг STATUS_DEFAULT_STORE установлен в свойстве **PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="db872-108">The STATUS_DEFAULT_STORE flag is set in the **PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md)) property.</span></span>
    
- <span data-ttu-id="db872-109">MAPI автоматически создает поддерева IPM и корневые папки для результатов поиска, общие и личные представления при открытии хранилища сообщений.</span><span class="sxs-lookup"><span data-stu-id="db872-109">MAPI automatically creates the IPM subtree and the root folders for search-results, common views and personal views when the message store is opened.</span></span> <span data-ttu-id="db872-110">Дополнительные сведения об этих папок можно [Поддерева](ipm-subtree.md) IPM и [Специальные папки MAPI](mapi-special-folders.md).</span><span class="sxs-lookup"><span data-stu-id="db872-110">For more information about these folders, see [IPM Subtree](ipm-subtree.md) and [MAPI Special Folders](mapi-special-folders.md).</span></span> 
    
<span data-ttu-id="db872-111">Чтобы получить идентификатор записи для хранилища сообщений по умолчанию, необходимо вызвать [IMAPISession::GetMsgStoresTable](imapisession-getmsgstorestable.md) для открытия в таблице хранилища сообщений и применить соответствующее ограничение в вызове [HrQueryAllRows](hrqueryallrows.md).</span><span class="sxs-lookup"><span data-stu-id="db872-111">To retrieve the entry identifier for the default message store, you must call [IMAPISession::GetMsgStoresTable](imapisession-getmsgstorestable.md) to open the message store table and apply an appropriate restriction in a call to [HrQueryAllRows](hrqueryallrows.md).</span></span> <span data-ttu-id="db872-112">**HrQueryAllRows** возвращает строку набор с одной строкой, который представляет хранилище сообщений по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="db872-112">**HrQueryAllRows** will return a row set with the one row that represents the default message store.</span></span> <span data-ttu-id="db872-113">Ограничение, которое передается **HrQueryAllRows** может принимать одно из следующих форм:</span><span class="sxs-lookup"><span data-stu-id="db872-113">The restriction that you pass to **HrQueryAllRows** can take on one of the following forms:</span></span> 
  
1. <span data-ttu-id="db872-114">**И** ограничение, которое использует структуру **SAndRestriction** для объединения:</span><span class="sxs-lookup"><span data-stu-id="db872-114">An **AND** restriction that uses an **SAndRestriction** structure to combine:</span></span> 
    
   - <span data-ttu-id="db872-115">Существует ограничение, которое использует структуру **SExistRestriction** для проверки наличия свойство **PR_DEFAULT_STORE** .</span><span class="sxs-lookup"><span data-stu-id="db872-115">An exists restriction that uses an **SExistRestriction** structure to test for the existence of the **PR_DEFAULT_STORE** property.</span></span> 
    
   - <span data-ttu-id="db872-116">Ограничение свойство, которое использует структуру [SPropertyRestriction](spropertyrestriction.md) для проверки для значение TRUE в свойстве **PR_DEFAULT_STORE** .</span><span class="sxs-lookup"><span data-stu-id="db872-116">A property restriction that uses an [SPropertyRestriction](spropertyrestriction.md) structure to check for the TRUE value in the **PR_DEFAULT_STORE** property.</span></span> 
    
2. <span data-ttu-id="db872-117">Ограничение Битовая маска, которое использует структуру [SBitMaskRestriction](sbitmaskrestriction.md) применения STATUS_DEFAULT_STORE как маска со свойством **PR_RESOURCE_FLAGS** .</span><span class="sxs-lookup"><span data-stu-id="db872-117">A bitmask restriction that uses an [SBitMaskRestriction](sbitmaskrestriction.md) structure for applying STATUS_DEFAULT_STORE as a mask against the **PR_RESOURCE_FLAGS** property.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="db872-118">См. также</span><span class="sxs-lookup"><span data-stu-id="db872-118">See also</span></span>

- [<span data-ttu-id="db872-119">SExistRestriction</span><span class="sxs-lookup"><span data-stu-id="db872-119">SExistRestriction</span></span>](sexistrestriction.md)
- [<span data-ttu-id="db872-120">SAndRestriction</span><span class="sxs-lookup"><span data-stu-id="db872-120">SAndRestriction</span></span>](sandrestriction.md)


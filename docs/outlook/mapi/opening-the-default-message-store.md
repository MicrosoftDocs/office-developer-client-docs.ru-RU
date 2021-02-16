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
# <a name="opening-the-default-message-store"></a><span data-ttu-id="a8cfc-103">Открытие хранилища сообщений по умолчанию</span><span class="sxs-lookup"><span data-stu-id="a8cfc-103">Opening the default message store</span></span>

<span data-ttu-id="a8cfc-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a8cfc-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a8cfc-105">В любом конкретном сеансе одно хранилище сообщений действует как хранилище сообщений по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="a8cfc-105">In any particular session, one message store acts as the default message store.</span></span> <span data-ttu-id="a8cfc-106">Хранилище сообщений по умолчанию имеет следующие характеристики:</span><span class="sxs-lookup"><span data-stu-id="a8cfc-106">A default message store has the following characteristics:</span></span>
  
- <span data-ttu-id="a8cfc-107">Свойству **PR_DEFAULT_STORE** ([PidTagDefaultStore)](pidtagdefaultstore-canonical-property.md)задается true.</span><span class="sxs-lookup"><span data-stu-id="a8cfc-107">The **PR_DEFAULT_STORE** ([PidTagDefaultStore](pidtagdefaultstore-canonical-property.md)) property is set to TRUE.</span></span>
    
- <span data-ttu-id="a8cfc-108">Флаг STATUS_DEFAULT_STORE устанавливается в свойстве **PR_RESOURCE_FLAGS** ([PidTagResourceFlags).](pidtagresourceflags-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="a8cfc-108">The STATUS_DEFAULT_STORE flag is set in the **PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md)) property.</span></span>
    
- <span data-ttu-id="a8cfc-109">MAPI автоматически создает поддерево IPM и корневые папки для результатов поиска, общих представлений и личных представлений при открытом хранилище сообщений.</span><span class="sxs-lookup"><span data-stu-id="a8cfc-109">MAPI automatically creates the IPM subtree and the root folders for search-results, common views and personal views when the message store is opened.</span></span> <span data-ttu-id="a8cfc-110">Дополнительные сведения об этих папках см. в поддеревье [IPM](ipm-subtree.md) и [специальных папках MAPI.](mapi-special-folders.md)</span><span class="sxs-lookup"><span data-stu-id="a8cfc-110">For more information about these folders, see [IPM Subtree](ipm-subtree.md) and [MAPI Special Folders](mapi-special-folders.md).</span></span> 
    
<span data-ttu-id="a8cfc-111">Чтобы получить идентификатор записи для хранения сообщений по умолчанию, необходимо вызвать [IMAPISession::GetMsgStoresTable,](imapisession-getmsgstorestable.md) чтобы открыть таблицу хранения сообщений и применить соответствующее ограничение в вызове [HrQueryAllRows.](hrqueryallrows.md)</span><span class="sxs-lookup"><span data-stu-id="a8cfc-111">To retrieve the entry identifier for the default message store, you must call [IMAPISession::GetMsgStoresTable](imapisession-getmsgstorestable.md) to open the message store table and apply an appropriate restriction in a call to [HrQueryAllRows](hrqueryallrows.md).</span></span> <span data-ttu-id="a8cfc-112">**HrQueryAllRows** возвращает набор строк с одной строкой, которая представляет хранилище сообщений по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="a8cfc-112">**HrQueryAllRows** will return a row set with the one row that represents the default message store.</span></span> <span data-ttu-id="a8cfc-113">Ограничение, которое вы передаете **в HrQueryAllRows,** может приниматься в одной из следующих форм:</span><span class="sxs-lookup"><span data-stu-id="a8cfc-113">The restriction that you pass to **HrQueryAllRows** can take on one of the following forms:</span></span> 
  
1. <span data-ttu-id="a8cfc-114">Ограничение **AND,** использующее **структуру SAndRestriction** для объединения:</span><span class="sxs-lookup"><span data-stu-id="a8cfc-114">An **AND** restriction that uses an **SAndRestriction** structure to combine:</span></span> 
    
   - <span data-ttu-id="a8cfc-115">Существует ограничение, использующее **структуру SExistRestriction** для проверки наличия PR_DEFAULT_STORE **свойства.**</span><span class="sxs-lookup"><span data-stu-id="a8cfc-115">An exists restriction that uses an **SExistRestriction** structure to test for the existence of the **PR_DEFAULT_STORE** property.</span></span> 
    
   - <span data-ttu-id="a8cfc-116">Ограничение свойств, использующее [структуру SPropertyRestriction](spropertyrestriction.md) для проверки значения TRUE в PR_DEFAULT_STORE **свойства.**</span><span class="sxs-lookup"><span data-stu-id="a8cfc-116">A property restriction that uses an [SPropertyRestriction](spropertyrestriction.md) structure to check for the TRUE value in the **PR_DEFAULT_STORE** property.</span></span> 
    
2. <span data-ttu-id="a8cfc-117">Ограничение битовых масок, использующее структуру [SBitMaskRestriction](sbitmaskrestriction.md) для применения  STATUS_DEFAULT_STORE к свойству PR_RESOURCE_FLAGS.</span><span class="sxs-lookup"><span data-stu-id="a8cfc-117">A bitmask restriction that uses an [SBitMaskRestriction](sbitmaskrestriction.md) structure for applying STATUS_DEFAULT_STORE as a mask against the **PR_RESOURCE_FLAGS** property.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="a8cfc-118">См. также</span><span class="sxs-lookup"><span data-stu-id="a8cfc-118">See also</span></span>

- [<span data-ttu-id="a8cfc-119">SExistRestriction</span><span class="sxs-lookup"><span data-stu-id="a8cfc-119">SExistRestriction</span></span>](sexistrestriction.md)
- [<span data-ttu-id="a8cfc-120">SAndRestriction</span><span class="sxs-lookup"><span data-stu-id="a8cfc-120">SAndRestriction</span></span>](sandrestriction.md)


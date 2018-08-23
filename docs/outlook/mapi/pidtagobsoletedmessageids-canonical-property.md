---
title: Каноническое свойство PidTagObsoletedMessageIds
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagObsoletedMessageIds
api_type:
- HeaderDef
ms.assetid: bc979398-f1ad-4496-b982-428b95719369
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 1717e30679fb3f6721690db75fb5dd402048eb09
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22575051"
---
# <a name="pidtagobsoletedmessageids-canonical-property"></a><span data-ttu-id="6f156-103">Каноническое свойство PidTagObsoletedMessageIds</span><span class="sxs-lookup"><span data-stu-id="6f156-103">PidTagObsoletedMessageIds Canonical Property</span></span>

  
  
<span data-ttu-id="6f156-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6f156-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6f156-105">Содержит идентификаторы сообщений, которые заменяет это сообщение.</span><span class="sxs-lookup"><span data-stu-id="6f156-105">Contains the identifiers of messages that this message supersedes.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="6f156-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="6f156-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="6f156-107">PR_OBSOLETED_IPMS</span><span class="sxs-lookup"><span data-stu-id="6f156-107">PR_OBSOLETED_IPMS</span></span>  <br/> |
|<span data-ttu-id="6f156-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="6f156-108">Identifier:</span></span>  <br/> |<span data-ttu-id="6f156-109">0x001F</span><span class="sxs-lookup"><span data-stu-id="6f156-109">0x001F</span></span>  <br/> |
|<span data-ttu-id="6f156-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="6f156-110">Data type:</span></span>  <br/> |<span data-ttu-id="6f156-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="6f156-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="6f156-112">Область:</span><span class="sxs-lookup"><span data-stu-id="6f156-112">Area:</span></span>  <br/> |<span data-ttu-id="6f156-113">Сервер</span><span class="sxs-lookup"><span data-stu-id="6f156-113">Server</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="6f156-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="6f156-114">Remarks</span></span>

<span data-ttu-id="6f156-115">Идентификаторы, содержащихся в это свойство является основным требованием стандартных поиска с использованием формата свойство **PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="6f156-115">The identifiers contained in this property are standard search keys using the format of the **PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md)) property.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="6f156-116">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="6f156-116">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="6f156-117">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="6f156-117">Header files</span></span>

<span data-ttu-id="6f156-118">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="6f156-118">Mapidefs.h</span></span>
  
> <span data-ttu-id="6f156-119">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="6f156-119">Provides data type definitions.</span></span>
    
<span data-ttu-id="6f156-120">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="6f156-120">Mapitags.h</span></span>
  
> <span data-ttu-id="6f156-121">Содержит определения свойств указано, что связанными свойствами.</span><span class="sxs-lookup"><span data-stu-id="6f156-121">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="6f156-122">См. также</span><span class="sxs-lookup"><span data-stu-id="6f156-122">See also</span></span>



[<span data-ttu-id="6f156-123">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="6f156-123">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="6f156-124">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="6f156-124">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="6f156-125">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="6f156-125">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="6f156-126">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="6f156-126">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)


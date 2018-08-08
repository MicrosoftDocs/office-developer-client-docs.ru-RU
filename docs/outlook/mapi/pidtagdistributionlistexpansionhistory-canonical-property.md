---
title: Каноническое свойство PidTagDistributionListExpansionHistory
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagDistributionListExpansionHistory
api_type:
- HeaderDef
ms.assetid: fc1e0162-d655-4761-92e7-b469579c270b
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 3989532388d9c88c293427a4ce7109579a832ad1
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19811089"
---
# <a name="pidtagdistributionlistexpansionhistory-canonical-property"></a><span data-ttu-id="3c2f2-103">Каноническое свойство PidTagDistributionListExpansionHistory</span><span class="sxs-lookup"><span data-stu-id="3c2f2-103">PidTagDistributionListExpansionHistory Canonical Property</span></span>

  
  
<span data-ttu-id="3c2f2-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="3c2f2-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="3c2f2-105">Содержит журнал, в котором показано, как в список рассылки дополнены во время передачи сообщений.</span><span class="sxs-lookup"><span data-stu-id="3c2f2-105">Contains a history showing how a distribution list has been expanded during message transmission.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="3c2f2-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="3c2f2-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="3c2f2-107">PR_DL_EXPANSION_HISTORY</span><span class="sxs-lookup"><span data-stu-id="3c2f2-107">PR_DL_EXPANSION_HISTORY</span></span>  <br/> |
|<span data-ttu-id="3c2f2-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="3c2f2-108">Identifier:</span></span>  <br/> |<span data-ttu-id="3c2f2-109">0x0013</span><span class="sxs-lookup"><span data-stu-id="3c2f2-109">0x0013</span></span>  <br/> |
|<span data-ttu-id="3c2f2-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="3c2f2-110">Data type:</span></span>  <br/> |<span data-ttu-id="3c2f2-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="3c2f2-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="3c2f2-112">Область:</span><span class="sxs-lookup"><span data-stu-id="3c2f2-112">Area:</span></span>  <br/> |<span data-ttu-id="3c2f2-113">Конверт MAPI</span><span class="sxs-lookup"><span data-stu-id="3c2f2-113">MAPI envelope</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="3c2f2-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="3c2f2-114">Remarks</span></span>

<span data-ttu-id="3c2f2-115">Это свойство доступно для получения клиентских приложений, если установлен поставщика транспорта.</span><span class="sxs-lookup"><span data-stu-id="3c2f2-115">This property is available to receiving client applications if the transport provider has set it.</span></span> <span data-ttu-id="3c2f2-116">Это также доступны для клиента, если содержимое сообщения, возвращаемых в отчет.</span><span class="sxs-lookup"><span data-stu-id="3c2f2-116">It is also available to the sending client if the message content is returned with a report.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="3c2f2-117">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="3c2f2-117">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="3c2f2-118">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="3c2f2-118">Header files</span></span>

<span data-ttu-id="3c2f2-119">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="3c2f2-119">Mapidefs.h</span></span>
  
> <span data-ttu-id="3c2f2-120">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="3c2f2-120">Provides data type definitions.</span></span>
    
<span data-ttu-id="3c2f2-121">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="3c2f2-121">Mapitags.h</span></span>
  
> <span data-ttu-id="3c2f2-122">Содержит определения свойства в списке альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="3c2f2-122">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="3c2f2-123">См. также</span><span class="sxs-lookup"><span data-stu-id="3c2f2-123">See also</span></span>



[<span data-ttu-id="3c2f2-124">Каноническое свойство PidTagDistributionListExpansionProhibited</span><span class="sxs-lookup"><span data-stu-id="3c2f2-124">PidTagDistributionListExpansionProhibited Canonical Property</span></span>](pidtagdistributionlistexpansionprohibited-canonical-property.md)


[<span data-ttu-id="3c2f2-125">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="3c2f2-125">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="3c2f2-126">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="3c2f2-126">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="3c2f2-127">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="3c2f2-127">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="3c2f2-128">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="3c2f2-128">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)


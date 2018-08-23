---
title: Каноническое свойство PidTagProviderSubmitTime
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagProviderSubmitTime
api_type:
- COM
ms.assetid: 9e5161d9-fefe-4a12-b7f7-5600f1d2e95b
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: e08b56fcfea38bf65e8628acfa481716554e2c01
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22571614"
---
# <a name="pidtagprovidersubmittime-canonical-property"></a><span data-ttu-id="4f484-103">Каноническое свойство PidTagProviderSubmitTime</span><span class="sxs-lookup"><span data-stu-id="4f484-103">PidTagProviderSubmitTime Canonical Property</span></span>

  
  
<span data-ttu-id="4f484-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4f484-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4f484-105">Содержит дату и время, для поставщика транспорта сообщение системы обмена сообщениями.</span><span class="sxs-lookup"><span data-stu-id="4f484-105">Contains the date and time a transport provider passed a message to its underlying messaging system.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="4f484-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="4f484-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="4f484-107">PR_PROVIDER_SUBMIT_TIME</span><span class="sxs-lookup"><span data-stu-id="4f484-107">PR_PROVIDER_SUBMIT_TIME</span></span>  <br/> |
|<span data-ttu-id="4f484-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="4f484-108">Identifier:</span></span>  <br/> |<span data-ttu-id="4f484-109">0x0048</span><span class="sxs-lookup"><span data-stu-id="4f484-109">0x0048</span></span>  <br/> |
|<span data-ttu-id="4f484-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="4f484-110">Data type:</span></span>  <br/> |<span data-ttu-id="4f484-111">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="4f484-111">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="4f484-112">Область:</span><span class="sxs-lookup"><span data-stu-id="4f484-112">Area:</span></span>  <br/> |<span data-ttu-id="4f484-113">Конверт MAPI</span><span class="sxs-lookup"><span data-stu-id="4f484-113">MAPI envelope</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="4f484-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="4f484-114">Remarks</span></span>

<span data-ttu-id="4f484-115">Это свойство задается исходящей поставщика транспорта во время отправки сообщения.</span><span class="sxs-lookup"><span data-stu-id="4f484-115">This property is set by the outgoing transport provider at the time a message is sent.</span></span>
  
<span data-ttu-id="4f484-116">Это свойство соответствует атрибуту X.400 конверт отправки каждого сообщения.</span><span class="sxs-lookup"><span data-stu-id="4f484-116">This property corresponds to an X.400 submission envelope per-message attribute.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="4f484-117">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="4f484-117">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="4f484-118">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="4f484-118">Header files</span></span>

<span data-ttu-id="4f484-119">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="4f484-119">Mapidefs.h</span></span>
  
> <span data-ttu-id="4f484-120">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="4f484-120">Provides data type definitions.</span></span>
    
<span data-ttu-id="4f484-121">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="4f484-121">Mapitags.h</span></span>
  
> <span data-ttu-id="4f484-122">Содержит определения свойства в списке альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="4f484-122">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="4f484-123">См. также</span><span class="sxs-lookup"><span data-stu-id="4f484-123">See also</span></span>



[<span data-ttu-id="4f484-124">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="4f484-124">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="4f484-125">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="4f484-125">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="4f484-126">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="4f484-126">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="4f484-127">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="4f484-127">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)


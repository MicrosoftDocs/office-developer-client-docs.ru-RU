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
ms.openlocfilehash: 162451d000c0b3da42c8fbef5f64459bc5ae23b1
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19811600"
---
# <a name="pidtagprovidersubmittime-canonical-property"></a><span data-ttu-id="2718c-103">Каноническое свойство PidTagProviderSubmitTime</span><span class="sxs-lookup"><span data-stu-id="2718c-103">PidTagProviderSubmitTime Canonical Property</span></span>

  
  
<span data-ttu-id="2718c-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="2718c-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="2718c-105">Содержит дату и время, для поставщика транспорта сообщение системы обмена сообщениями.</span><span class="sxs-lookup"><span data-stu-id="2718c-105">Contains the date and time a transport provider passed a message to its underlying messaging system.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="2718c-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="2718c-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="2718c-107">PR_PROVIDER_SUBMIT_TIME</span><span class="sxs-lookup"><span data-stu-id="2718c-107">PR_PROVIDER_SUBMIT_TIME</span></span>  <br/> |
|<span data-ttu-id="2718c-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="2718c-108">Identifier:</span></span>  <br/> |<span data-ttu-id="2718c-109">0x0048</span><span class="sxs-lookup"><span data-stu-id="2718c-109">0x0048</span></span>  <br/> |
|<span data-ttu-id="2718c-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="2718c-110">Data type:</span></span>  <br/> |<span data-ttu-id="2718c-111">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="2718c-111">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="2718c-112">Область:</span><span class="sxs-lookup"><span data-stu-id="2718c-112">Area:</span></span>  <br/> |<span data-ttu-id="2718c-113">Конверт MAPI</span><span class="sxs-lookup"><span data-stu-id="2718c-113">MAPI envelope</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="2718c-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="2718c-114">Remarks</span></span>

<span data-ttu-id="2718c-115">Это свойство задается исходящей поставщика транспорта во время отправки сообщения.</span><span class="sxs-lookup"><span data-stu-id="2718c-115">This property is set by the outgoing transport provider at the time a message is sent.</span></span>
  
<span data-ttu-id="2718c-116">Это свойство соответствует атрибуту X.400 конверт отправки каждого сообщения.</span><span class="sxs-lookup"><span data-stu-id="2718c-116">This property corresponds to an X.400 submission envelope per-message attribute.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="2718c-117">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="2718c-117">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="2718c-118">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="2718c-118">Header files</span></span>

<span data-ttu-id="2718c-119">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="2718c-119">Mapidefs.h</span></span>
  
> <span data-ttu-id="2718c-120">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="2718c-120">Provides data type definitions.</span></span>
    
<span data-ttu-id="2718c-121">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="2718c-121">Mapitags.h</span></span>
  
> <span data-ttu-id="2718c-122">Содержит определения свойства в списке альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="2718c-122">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="2718c-123">См. также</span><span class="sxs-lookup"><span data-stu-id="2718c-123">See also</span></span>



[<span data-ttu-id="2718c-124">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="2718c-124">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="2718c-125">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="2718c-125">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="2718c-126">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="2718c-126">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="2718c-127">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="2718c-127">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)


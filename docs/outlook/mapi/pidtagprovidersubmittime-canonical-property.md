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
ms.openlocfilehash: c5e840250da7ba3b95150f2e83e1eb08b0c61ab5
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409022"
---
# <a name="pidtagprovidersubmittime-canonical-property"></a><span data-ttu-id="8ee75-103">Каноническое свойство PidTagProviderSubmitTime</span><span class="sxs-lookup"><span data-stu-id="8ee75-103">PidTagProviderSubmitTime Canonical Property</span></span>

  
  
<span data-ttu-id="8ee75-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8ee75-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8ee75-105">Содержит дату и время передачи сообщения поставщиком транспорта в свою систему обмена сообщениями.</span><span class="sxs-lookup"><span data-stu-id="8ee75-105">Contains the date and time a transport provider passed a message to its underlying messaging system.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="8ee75-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="8ee75-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="8ee75-107">PR_PROVIDER_SUBMIT_TIME</span><span class="sxs-lookup"><span data-stu-id="8ee75-107">PR_PROVIDER_SUBMIT_TIME</span></span>  <br/> |
|<span data-ttu-id="8ee75-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="8ee75-108">Identifier:</span></span>  <br/> |<span data-ttu-id="8ee75-109">0x0048</span><span class="sxs-lookup"><span data-stu-id="8ee75-109">0x0048</span></span>  <br/> |
|<span data-ttu-id="8ee75-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="8ee75-110">Data type:</span></span>  <br/> |<span data-ttu-id="8ee75-111">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="8ee75-111">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="8ee75-112">Область:</span><span class="sxs-lookup"><span data-stu-id="8ee75-112">Area:</span></span>  <br/> |<span data-ttu-id="8ee75-113">Конверт MAPI</span><span class="sxs-lookup"><span data-stu-id="8ee75-113">MAPI envelope</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="8ee75-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="8ee75-114">Remarks</span></span>

<span data-ttu-id="8ee75-115">Это свойство задается поставщиком исходяющих транспортных данных во время отправленного сообщения.</span><span class="sxs-lookup"><span data-stu-id="8ee75-115">This property is set by the outgoing transport provider at the time a message is sent.</span></span>
  
<span data-ttu-id="8ee75-116">Это свойство соответствует атрибуту конверта отправки X.400 для каждого сообщения.</span><span class="sxs-lookup"><span data-stu-id="8ee75-116">This property corresponds to an X.400 submission envelope per-message attribute.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="8ee75-117">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="8ee75-117">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="8ee75-118">Файлы заголовок</span><span class="sxs-lookup"><span data-stu-id="8ee75-118">Header files</span></span>

<span data-ttu-id="8ee75-119">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="8ee75-119">Mapidefs.h</span></span>
  
> <span data-ttu-id="8ee75-120">Предоставляет определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="8ee75-120">Provides data type definitions.</span></span>
    
<span data-ttu-id="8ee75-121">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="8ee75-121">Mapitags.h</span></span>
  
> <span data-ttu-id="8ee75-122">Содержит определения свойств, перечисленных в качестве альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="8ee75-122">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="8ee75-123">См. также</span><span class="sxs-lookup"><span data-stu-id="8ee75-123">See also</span></span>



[<span data-ttu-id="8ee75-124">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="8ee75-124">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="8ee75-125">Канонические свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="8ee75-125">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="8ee75-126">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="8ee75-126">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="8ee75-127">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="8ee75-127">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)


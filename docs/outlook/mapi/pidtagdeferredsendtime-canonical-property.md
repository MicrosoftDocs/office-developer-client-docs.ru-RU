---
title: Каноническое свойство PidTagDeferredSendTime
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagDeferredSendTime
api_type:
- HeaderDef
ms.assetid: ee206c2d-8371-4d19-b42b-78f6479e13ca
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: f636c0a49d6ad96ab157d00780fa6ffc5c8f3236
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22588274"
---
# <a name="pidtagdeferredsendtime-canonical-property"></a><span data-ttu-id="33dcf-103">Каноническое свойство PidTagDeferredSendTime</span><span class="sxs-lookup"><span data-stu-id="33dcf-103">PidTagDeferredSendTime Canonical Property</span></span>

  
  
<span data-ttu-id="33dcf-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="33dcf-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="33dcf-105">Указывает время, когда это клиент, предоставляемых отложите отправки сообщения.</span><span class="sxs-lookup"><span data-stu-id="33dcf-105">Indicates a time when a client would like to defer sending a message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="33dcf-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="33dcf-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="33dcf-107">PR_DEFERRED_SEND_TIME</span><span class="sxs-lookup"><span data-stu-id="33dcf-107">PR_DEFERRED_SEND_TIME</span></span>  <br/> |
|<span data-ttu-id="33dcf-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="33dcf-108">Identifier:</span></span>  <br/> |<span data-ttu-id="33dcf-109">0x3FEF</span><span class="sxs-lookup"><span data-stu-id="33dcf-109">0x3FEF</span></span>  <br/> |
|<span data-ttu-id="33dcf-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="33dcf-110">Data type:</span></span>  <br/> |<span data-ttu-id="33dcf-111">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="33dcf-111">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="33dcf-112">Область:</span><span class="sxs-lookup"><span data-stu-id="33dcf-112">Area:</span></span>  <br/> |<span data-ttu-id="33dcf-113">Состояние MAPI</span><span class="sxs-lookup"><span data-stu-id="33dcf-113">MAPI status</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="33dcf-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="33dcf-114">Remarks</span></span>

<span data-ttu-id="33dcf-115">Если присутствуют **PR_DEFERRED_SEND_UNITS** ([PidTagDeferredSendUnits](pidtagdeferredsendunits-canonical-property.md)) и **PR_DEFERRED_SEND_NUMBER** ([PidTagDeferredSendNumber](pidtagdeferredsendnumber-canonical-property.md)) свойства, значение этого свойства — это пересчитывать с помощью следующей формулы и Старое значение игнорируется.</span><span class="sxs-lookup"><span data-stu-id="33dcf-115">If the **PR_DEFERRED_SEND_UNITS** ([PidTagDeferredSendUnits](pidtagdeferredsendunits-canonical-property.md)) and **PR_DEFERRED_SEND_NUMBER** ([PidTagDeferredSendNumber](pidtagdeferredsendnumber-canonical-property.md)) properties are present, the value of this property is recomputed by using the following formula and the old value is ignored.</span></span>
  
 <span data-ttu-id="33dcf-116">**PR_DEFERRED_SEND_TIME** = **PR_CLIENT_SUBMIT_TIME** ([PidTagClientSubmitTime](pidtagclientsubmittime-canonical-property.md)) + **PR_DEFERRED_SEND_NUMBER** \* TimeOf (**PR_DEFERRED_SEND_UNITS**)</span><span class="sxs-lookup"><span data-stu-id="33dcf-116">**PR_DEFERRED_SEND_TIME** = **PR_CLIENT_SUBMIT_TIME** ([PidTagClientSubmitTime](pidtagclientsubmittime-canonical-property.md)) + **PR_DEFERRED_SEND_NUMBER** \* TimeOf(**PR_DEFERRED_SEND_UNITS**)</span></span>
  
<span data-ttu-id="33dcf-117">Если значение **PR_DEFERRED_SEND_TIME** является более ранней, чем текущая время (в формате UTC), сообщение отправляется немедленно.</span><span class="sxs-lookup"><span data-stu-id="33dcf-117">If **PR_DEFERRED_SEND_TIME** value is earlier than the current time (in UTC), the message is sent immediately.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="33dcf-118">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="33dcf-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="33dcf-119">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="33dcf-119">Protocol specifications</span></span>

<span data-ttu-id="33dcf-120">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="33dcf-120">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="33dcf-121">Задает свойства и операции, допустимые для объектов сообщения электронной почты.</span><span class="sxs-lookup"><span data-stu-id="33dcf-121">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="33dcf-122">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="33dcf-122">Header files</span></span>

<span data-ttu-id="33dcf-123">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="33dcf-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="33dcf-124">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="33dcf-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="33dcf-125">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="33dcf-125">Mapitags.h</span></span>
  
> <span data-ttu-id="33dcf-126">Содержит определения свойства в списке альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="33dcf-126">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="33dcf-127">См. также</span><span class="sxs-lookup"><span data-stu-id="33dcf-127">See also</span></span>



[<span data-ttu-id="33dcf-128">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="33dcf-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="33dcf-129">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="33dcf-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="33dcf-130">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="33dcf-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="33dcf-131">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="33dcf-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)


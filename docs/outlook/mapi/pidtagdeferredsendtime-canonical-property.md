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
ms.openlocfilehash: 2d6374c2fd3c277e2bb976930e9e105cc839b1e8
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359880"
---
# <a name="pidtagdeferredsendtime-canonical-property"></a><span data-ttu-id="05ede-103">Каноническое свойство PidTagDeferredSendTime</span><span class="sxs-lookup"><span data-stu-id="05ede-103">PidTagDeferredSendTime Canonical Property</span></span>

  
  
<span data-ttu-id="05ede-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="05ede-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="05ede-105">Указывает время, когда клиент хотел бы отложить отправку сообщения.</span><span class="sxs-lookup"><span data-stu-id="05ede-105">Indicates a time when a client would like to defer sending a message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="05ede-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="05ede-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="05ede-107">PR_DEFERRED_SEND_TIME</span><span class="sxs-lookup"><span data-stu-id="05ede-107">PR_DEFERRED_SEND_TIME</span></span>  <br/> |
|<span data-ttu-id="05ede-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="05ede-108">Identifier:</span></span>  <br/> |<span data-ttu-id="05ede-109">0x3FEF</span><span class="sxs-lookup"><span data-stu-id="05ede-109">0x3FEF</span></span>  <br/> |
|<span data-ttu-id="05ede-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="05ede-110">Data type:</span></span>  <br/> |<span data-ttu-id="05ede-111">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="05ede-111">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="05ede-112">Область:</span><span class="sxs-lookup"><span data-stu-id="05ede-112">Area:</span></span>  <br/> |<span data-ttu-id="05ede-113">Состояние MAPI</span><span class="sxs-lookup"><span data-stu-id="05ede-113">MAPI status</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="05ede-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="05ede-114">Remarks</span></span>

<span data-ttu-id="05ede-115">Если **свойства PR_DEFERRED_SEND_UNITS** [(PidTagDeferredSendUnits)](pidtagdeferredsendunits-canonical-property.md)и **PR_DEFERRED_SEND_NUMBER** [(PidTagDeferredSendNumber)](pidtagdeferredsendnumber-canonical-property.md)присутствуют, значение этого свойства будет откормлено с помощью следующей формулы, а старое значение игнорируется.</span><span class="sxs-lookup"><span data-stu-id="05ede-115">If the **PR_DEFERRED_SEND_UNITS** ([PidTagDeferredSendUnits](pidtagdeferredsendunits-canonical-property.md)) and **PR_DEFERRED_SEND_NUMBER** ([PidTagDeferredSendNumber](pidtagdeferredsendnumber-canonical-property.md)) properties are present, the value of this property is recomputed by using the following formula and the old value is ignored.</span></span>
  
 <span data-ttu-id="05ede-116">**PR_DEFERRED_SEND_TIME**  =  **PR_CLIENT_SUBMIT_TIME** [(PidTagClientSubmitTime](pidtagclientsubmittime-canonical-property.md)) + **PR_DEFERRED_SEND_NUMBER** \* TimeOf **(PR_DEFERRED_SEND_UNITS)**</span><span class="sxs-lookup"><span data-stu-id="05ede-116">**PR_DEFERRED_SEND_TIME** = **PR_CLIENT_SUBMIT_TIME** ([PidTagClientSubmitTime](pidtagclientsubmittime-canonical-property.md)) + **PR_DEFERRED_SEND_NUMBER** \* TimeOf(**PR_DEFERRED_SEND_UNITS**)</span></span>
  
<span data-ttu-id="05ede-117">Если **PR_DEFERRED_SEND_TIME** ниже текущего времени (в UTC), сообщение отправляется немедленно.</span><span class="sxs-lookup"><span data-stu-id="05ede-117">If **PR_DEFERRED_SEND_TIME** value is earlier than the current time (in UTC), the message is sent immediately.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="05ede-118">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="05ede-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="05ede-119">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="05ede-119">Protocol specifications</span></span>

<span data-ttu-id="05ede-120">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="05ede-120">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="05ede-121">Указывает свойства и операции, допустимые для объектов сообщений электронной почты.</span><span class="sxs-lookup"><span data-stu-id="05ede-121">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="05ede-122">Файлы заголовки</span><span class="sxs-lookup"><span data-stu-id="05ede-122">Header files</span></span>

<span data-ttu-id="05ede-123">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="05ede-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="05ede-124">Предоставляет определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="05ede-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="05ede-125">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="05ede-125">Mapitags.h</span></span>
  
> <span data-ttu-id="05ede-126">Содержит определения свойств, перечисленных в качестве альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="05ede-126">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="05ede-127">См. также</span><span class="sxs-lookup"><span data-stu-id="05ede-127">See also</span></span>



[<span data-ttu-id="05ede-128">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="05ede-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="05ede-129">Канонические свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="05ede-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="05ede-130">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="05ede-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="05ede-131">Сопоставление имен MAPI с каноническими именами свойств</span><span class="sxs-lookup"><span data-stu-id="05ede-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)


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
# <a name="pidtagdeferredsendtime-canonical-property"></a><span data-ttu-id="01cf7-103">Каноническое свойство PidTagDeferredSendTime</span><span class="sxs-lookup"><span data-stu-id="01cf7-103">PidTagDeferredSendTime Canonical Property</span></span>

  
  
<span data-ttu-id="01cf7-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="01cf7-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="01cf7-105">Указывает время, когда клиент хочет отложить отправку сообщения.</span><span class="sxs-lookup"><span data-stu-id="01cf7-105">Indicates a time when a client would like to defer sending a message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="01cf7-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="01cf7-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="01cf7-107">PR_DEFERRED_SEND_TIME</span><span class="sxs-lookup"><span data-stu-id="01cf7-107">PR_DEFERRED_SEND_TIME</span></span>  <br/> |
|<span data-ttu-id="01cf7-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="01cf7-108">Identifier:</span></span>  <br/> |<span data-ttu-id="01cf7-109">0x3FEF</span><span class="sxs-lookup"><span data-stu-id="01cf7-109">0x3FEF</span></span>  <br/> |
|<span data-ttu-id="01cf7-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="01cf7-110">Data type:</span></span>  <br/> |<span data-ttu-id="01cf7-111">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="01cf7-111">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="01cf7-112">Область:</span><span class="sxs-lookup"><span data-stu-id="01cf7-112">Area:</span></span>  <br/> |<span data-ttu-id="01cf7-113">Состояние MAPI</span><span class="sxs-lookup"><span data-stu-id="01cf7-113">MAPI status</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="01cf7-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="01cf7-114">Remarks</span></span>

<span data-ttu-id="01cf7-115">Если имеются свойства **PR_DEFERRED_SEND_UNITS** ([PidTagDeferredSendUnits)](pidtagdeferredsendunits-canonical-property.md)и **PR_DEFERRED_SEND_NUMBER** ([PidTagDeferredSendNumber),](pidtagdeferredsendnumber-canonical-property.md)значение этого свойства перекомпилется с помощью следующей формулы, а старое значение игнорируется.</span><span class="sxs-lookup"><span data-stu-id="01cf7-115">If the **PR_DEFERRED_SEND_UNITS** ([PidTagDeferredSendUnits](pidtagdeferredsendunits-canonical-property.md)) and **PR_DEFERRED_SEND_NUMBER** ([PidTagDeferredSendNumber](pidtagdeferredsendnumber-canonical-property.md)) properties are present, the value of this property is recomputed by using the following formula and the old value is ignored.</span></span>
  
 <span data-ttu-id="01cf7-116">**PR_DEFERRED_SEND_TIME**  =  **PR_CLIENT_SUBMIT_TIME** ([PidTagClientSubmitTime](pidtagclientsubmittime-canonical-property.md)) + **PR_DEFERRED_SEND_NUMBER** \* TimeOf(**PR_DEFERRED_SEND_UNITS)**</span><span class="sxs-lookup"><span data-stu-id="01cf7-116">**PR_DEFERRED_SEND_TIME** = **PR_CLIENT_SUBMIT_TIME** ([PidTagClientSubmitTime](pidtagclientsubmittime-canonical-property.md)) + **PR_DEFERRED_SEND_NUMBER** \* TimeOf(**PR_DEFERRED_SEND_UNITS**)</span></span>
  
<span data-ttu-id="01cf7-117">Если **PR_DEFERRED_SEND_TIME** значение раньше текущего времени (в UTC), сообщение отправляется немедленно.</span><span class="sxs-lookup"><span data-stu-id="01cf7-117">If **PR_DEFERRED_SEND_TIME** value is earlier than the current time (in UTC), the message is sent immediately.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="01cf7-118">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="01cf7-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="01cf7-119">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="01cf7-119">Protocol specifications</span></span>

<span data-ttu-id="01cf7-120">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="01cf7-120">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="01cf7-121">Указывает свойства и операции, которые разрешены для объектов сообщений электронной почты.</span><span class="sxs-lookup"><span data-stu-id="01cf7-121">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="01cf7-122">Файлы заголовок</span><span class="sxs-lookup"><span data-stu-id="01cf7-122">Header files</span></span>

<span data-ttu-id="01cf7-123">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="01cf7-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="01cf7-124">Предоставляет определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="01cf7-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="01cf7-125">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="01cf7-125">Mapitags.h</span></span>
  
> <span data-ttu-id="01cf7-126">Содержит определения свойств, перечисленных в качестве альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="01cf7-126">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="01cf7-127">См. также</span><span class="sxs-lookup"><span data-stu-id="01cf7-127">See also</span></span>



[<span data-ttu-id="01cf7-128">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="01cf7-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="01cf7-129">Канонические свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="01cf7-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="01cf7-130">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="01cf7-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="01cf7-131">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="01cf7-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)


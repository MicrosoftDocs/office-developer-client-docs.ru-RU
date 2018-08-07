---
title: Каноническое свойство PidTagOriginallyIntendedRecipEmailAddress
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagOriginallyIntendedRecipEmailAddress
api_type:
- COM
ms.assetid: 6a85b695-731a-4401-9c9c-fda6bc308558
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: e24ae5f56a043d810eb805720606fd5b44d60cba
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19811445"
---
# <a name="pidtagoriginallyintendedrecipemailaddress-canonical-property"></a><span data-ttu-id="ea687-103">Каноническое свойство PidTagOriginallyIntendedRecipEmailAddress</span><span class="sxs-lookup"><span data-stu-id="ea687-103">PidTagOriginallyIntendedRecipEmailAddress Canonical Property</span></span>

  
  
<span data-ttu-id="ea687-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="ea687-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="ea687-105">Содержит адрес электронной почты, изначально требуемого получателя сообщения автоматически переадресовано.</span><span class="sxs-lookup"><span data-stu-id="ea687-105">Contains the email address of the originally intended recipient of an autoforwarded message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="ea687-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="ea687-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="ea687-107">PR_ORIGINALLY_INTENDED_RECIP_EMAIL_ADDRESS, PR_ORIGINALLY_INTENDED_RECIP_EMAIL_ADDRESS_A, PR_ORIGINALLY_INTENDED_RECIP_EMAIL_ADDRESS_W</span><span class="sxs-lookup"><span data-stu-id="ea687-107">PR_ORIGINALLY_INTENDED_RECIP_EMAIL_ADDRESS, PR_ORIGINALLY_INTENDED_RECIP_EMAIL_ADDRESS_A, PR_ORIGINALLY_INTENDED_RECIP_EMAIL_ADDRESS_W</span></span>  <br/> |
|<span data-ttu-id="ea687-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="ea687-108">Identifier:</span></span>  <br/> |<span data-ttu-id="ea687-109">0x007C</span><span class="sxs-lookup"><span data-stu-id="ea687-109">0x007C</span></span>  <br/> |
|<span data-ttu-id="ea687-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="ea687-110">Data type:</span></span>  <br/> |<span data-ttu-id="ea687-111">PT_STRING8 PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="ea687-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="ea687-112">Область:</span><span class="sxs-lookup"><span data-stu-id="ea687-112">Area:</span></span>  <br/> |<span data-ttu-id="ea687-113">Сервер</span><span class="sxs-lookup"><span data-stu-id="ea687-113">Server</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ea687-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="ea687-114">Remarks</span></span>

<span data-ttu-id="ea687-115">Эти свойства являются примерами свойства адреса для получателя, изначально предполагаемая сообщения.</span><span class="sxs-lookup"><span data-stu-id="ea687-115">These properties are examples of the address properties for the originally intended message recipient.</span></span> <span data-ttu-id="ea687-116">Им должен иметь значение агентом автоматическое перенаправление сообщения.</span><span class="sxs-lookup"><span data-stu-id="ea687-116">They must be set by the automatic agent that has forwarded the message.</span></span>
  
<span data-ttu-id="ea687-117">Эти свойства соответствуют атрибут каждого получателя отчета X.400.</span><span class="sxs-lookup"><span data-stu-id="ea687-117">These properties correspond to the X.400 report per-recipient attribute.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="ea687-118">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="ea687-118">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="ea687-119">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="ea687-119">Header files</span></span>

<span data-ttu-id="ea687-120">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="ea687-120">Mapidefs.h</span></span>
  
> <span data-ttu-id="ea687-121">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="ea687-121">Provides data type definitions.</span></span>
    
<span data-ttu-id="ea687-122">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="ea687-122">Mapitags.h</span></span>
  
> <span data-ttu-id="ea687-123">Содержит определения свойств указано, что связанными свойствами.</span><span class="sxs-lookup"><span data-stu-id="ea687-123">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="ea687-124">См. также</span><span class="sxs-lookup"><span data-stu-id="ea687-124">See also</span></span>



[<span data-ttu-id="ea687-125">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="ea687-125">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="ea687-126">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="ea687-126">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="ea687-127">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="ea687-127">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="ea687-128">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="ea687-128">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)


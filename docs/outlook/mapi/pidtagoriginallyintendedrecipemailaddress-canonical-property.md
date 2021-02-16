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
ms.openlocfilehash: 4a0e7325618a38addefe562c8207066dfea620f9
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33411374"
---
# <a name="pidtagoriginallyintendedrecipemailaddress-canonical-property"></a><span data-ttu-id="701b9-103">Каноническое свойство PidTagOriginallyIntendedRecipEmailAddress</span><span class="sxs-lookup"><span data-stu-id="701b9-103">PidTagOriginallyIntendedRecipEmailAddress Canonical Property</span></span>

  
  
<span data-ttu-id="701b9-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="701b9-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="701b9-105">Содержит адрес электронной почты исходного получателя автоматически переназначаемого сообщения.</span><span class="sxs-lookup"><span data-stu-id="701b9-105">Contains the email address of the originally intended recipient of an autoforwarded message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="701b9-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="701b9-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="701b9-107">PR_ORIGINALLY_INTENDED_RECIP_EMAIL_ADDRESS, PR_ORIGINALLY_INTENDED_RECIP_EMAIL_ADDRESS_A, PR_ORIGINALLY_INTENDED_RECIP_EMAIL_ADDRESS_W</span><span class="sxs-lookup"><span data-stu-id="701b9-107">PR_ORIGINALLY_INTENDED_RECIP_EMAIL_ADDRESS, PR_ORIGINALLY_INTENDED_RECIP_EMAIL_ADDRESS_A, PR_ORIGINALLY_INTENDED_RECIP_EMAIL_ADDRESS_W</span></span>  <br/> |
|<span data-ttu-id="701b9-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="701b9-108">Identifier:</span></span>  <br/> |<span data-ttu-id="701b9-109">0x007C</span><span class="sxs-lookup"><span data-stu-id="701b9-109">0x007C</span></span>  <br/> |
|<span data-ttu-id="701b9-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="701b9-110">Data type:</span></span>  <br/> |<span data-ttu-id="701b9-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="701b9-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="701b9-112">Область:</span><span class="sxs-lookup"><span data-stu-id="701b9-112">Area:</span></span>  <br/> |<span data-ttu-id="701b9-113">Server</span><span class="sxs-lookup"><span data-stu-id="701b9-113">Server</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="701b9-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="701b9-114">Remarks</span></span>

<span data-ttu-id="701b9-115">Эти свойства являются примерами свойств адреса для исходного получателя сообщения.</span><span class="sxs-lookup"><span data-stu-id="701b9-115">These properties are examples of the address properties for the originally intended message recipient.</span></span> <span data-ttu-id="701b9-116">Их должен установить автоматический агент, который переадил сообщение.</span><span class="sxs-lookup"><span data-stu-id="701b9-116">They must be set by the automatic agent that has forwarded the message.</span></span>
  
<span data-ttu-id="701b9-117">Эти свойства соответствуют атрибуту отчета X.400 для каждого получателя.</span><span class="sxs-lookup"><span data-stu-id="701b9-117">These properties correspond to the X.400 report per-recipient attribute.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="701b9-118">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="701b9-118">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="701b9-119">Файлы заголовок</span><span class="sxs-lookup"><span data-stu-id="701b9-119">Header files</span></span>

<span data-ttu-id="701b9-120">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="701b9-120">Mapidefs.h</span></span>
  
> <span data-ttu-id="701b9-121">Предоставляет определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="701b9-121">Provides data type definitions.</span></span>
    
<span data-ttu-id="701b9-122">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="701b9-122">Mapitags.h</span></span>
  
> <span data-ttu-id="701b9-123">Содержит определения свойств, перечисленных как связанные свойства.</span><span class="sxs-lookup"><span data-stu-id="701b9-123">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="701b9-124">См. также</span><span class="sxs-lookup"><span data-stu-id="701b9-124">See also</span></span>



[<span data-ttu-id="701b9-125">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="701b9-125">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="701b9-126">Канонические свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="701b9-126">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="701b9-127">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="701b9-127">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="701b9-128">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="701b9-128">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)


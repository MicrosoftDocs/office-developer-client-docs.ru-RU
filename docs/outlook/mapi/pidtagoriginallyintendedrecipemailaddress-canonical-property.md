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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32342544"
---
# <a name="pidtagoriginallyintendedrecipemailaddress-canonical-property"></a><span data-ttu-id="6a34d-103">Каноническое свойство PidTagOriginallyIntendedRecipEmailAddress</span><span class="sxs-lookup"><span data-stu-id="6a34d-103">PidTagOriginallyIntendedRecipEmailAddress Canonical Property</span></span>

  
  
<span data-ttu-id="6a34d-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6a34d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6a34d-105">Содержит адрес электронной почты изначально предполагаемого получателя сообщения с пересылкой.</span><span class="sxs-lookup"><span data-stu-id="6a34d-105">Contains the email address of the originally intended recipient of an autoforwarded message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="6a34d-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="6a34d-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="6a34d-107">ПР_ОРИГИНАЛЛИ_ИНТЕНДЕД_РЕЦИП_ЕМАИЛ_АДДРЕСС, ПР_ОРИГИНАЛЛИ_ИНТЕНДЕД_РЕЦИП_ЕМАИЛ_АДДРЕСС_А, PR_ORIGINALLY_INTENDED_RECIP_EMAIL_ADDRESS_W</span><span class="sxs-lookup"><span data-stu-id="6a34d-107">PR_ORIGINALLY_INTENDED_RECIP_EMAIL_ADDRESS, PR_ORIGINALLY_INTENDED_RECIP_EMAIL_ADDRESS_A, PR_ORIGINALLY_INTENDED_RECIP_EMAIL_ADDRESS_W</span></span>  <br/> |
|<span data-ttu-id="6a34d-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="6a34d-108">Identifier:</span></span>  <br/> |<span data-ttu-id="6a34d-109">0x007C</span><span class="sxs-lookup"><span data-stu-id="6a34d-109">0x007C</span></span>  <br/> |
|<span data-ttu-id="6a34d-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="6a34d-110">Data type:</span></span>  <br/> |<span data-ttu-id="6a34d-111">PT_STRING8, ПТ_УНИКОДЕ</span><span class="sxs-lookup"><span data-stu-id="6a34d-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="6a34d-112">Область:</span><span class="sxs-lookup"><span data-stu-id="6a34d-112">Area:</span></span>  <br/> |<span data-ttu-id="6a34d-113">Сервер</span><span class="sxs-lookup"><span data-stu-id="6a34d-113">Server</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="6a34d-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="6a34d-114">Remarks</span></span>

<span data-ttu-id="6a34d-115">Эти свойства являются примерами свойств адреса изначально назначенного получателя сообщения.</span><span class="sxs-lookup"><span data-stu-id="6a34d-115">These properties are examples of the address properties for the originally intended message recipient.</span></span> <span data-ttu-id="6a34d-116">Они должны быть заданы автоматическим агентом, который перенаправлял сообщение.</span><span class="sxs-lookup"><span data-stu-id="6a34d-116">They must be set by the automatic agent that has forwarded the message.</span></span>
  
<span data-ttu-id="6a34d-117">Эти свойства соответствуют атрибуту отчета X. 400 отчета по получателю.</span><span class="sxs-lookup"><span data-stu-id="6a34d-117">These properties correspond to the X.400 report per-recipient attribute.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="6a34d-118">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="6a34d-118">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="6a34d-119">Файлы заГоловков</span><span class="sxs-lookup"><span data-stu-id="6a34d-119">Header files</span></span>

<span data-ttu-id="6a34d-120">MAPIDEFS. h</span><span class="sxs-lookup"><span data-stu-id="6a34d-120">Mapidefs.h</span></span>
  
> <span data-ttu-id="6a34d-121">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="6a34d-121">Provides data type definitions.</span></span>
    
<span data-ttu-id="6a34d-122">Мапитагс. h</span><span class="sxs-lookup"><span data-stu-id="6a34d-122">Mapitags.h</span></span>
  
> <span data-ttu-id="6a34d-123">Содержит определения свойств, перечисленных как связанные свойства.</span><span class="sxs-lookup"><span data-stu-id="6a34d-123">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="6a34d-124">См. также</span><span class="sxs-lookup"><span data-stu-id="6a34d-124">See also</span></span>



[<span data-ttu-id="6a34d-125">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="6a34d-125">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="6a34d-126">Каноническое свойство MAPI</span><span class="sxs-lookup"><span data-stu-id="6a34d-126">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="6a34d-127">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="6a34d-127">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="6a34d-128">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="6a34d-128">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)


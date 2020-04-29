---
title: Каноническое свойство PidTagSensitivity
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagSensitivity
api_type:
- COM
ms.assetid: 5b678475-f2a8-4831-ad68-11654e09c821
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: eab8ce71d28a672d7069a1c16da5cd2cc2e149f7
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32342506"
---
# <a name="pidtagsensitivity-canonical-property"></a><span data-ttu-id="23dae-103">Каноническое свойство PidTagSensitivity</span><span class="sxs-lookup"><span data-stu-id="23dae-103">PidTagSensitivity Canonical Property</span></span>

  
  
<span data-ttu-id="23dae-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="23dae-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="23dae-105">Содержит значение, указывающее на отправителя сообщения о конфиденциальности сообщения.</span><span class="sxs-lookup"><span data-stu-id="23dae-105">Contains a value that indicates the message sender's opinion of the sensitivity of a message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="23dae-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="23dae-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="23dae-107">PR_SENSITIVITY</span><span class="sxs-lookup"><span data-stu-id="23dae-107">PR_SENSITIVITY</span></span>  <br/> |
|<span data-ttu-id="23dae-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="23dae-108">Identifier:</span></span>  <br/> |<span data-ttu-id="23dae-109">0x0036</span><span class="sxs-lookup"><span data-stu-id="23dae-109">0x0036</span></span>  <br/> |
|<span data-ttu-id="23dae-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="23dae-110">Data type:</span></span>  <br/> |<span data-ttu-id="23dae-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="23dae-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="23dae-112">Область:</span><span class="sxs-lookup"><span data-stu-id="23dae-112">Area:</span></span>  <br/> |<span data-ttu-id="23dae-113">Общий обмен сообщениями</span><span class="sxs-lookup"><span data-stu-id="23dae-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="23dae-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="23dae-114">Remarks</span></span>

<span data-ttu-id="23dae-115">Рекомендуется предоставлять объектам сообщений это свойство.</span><span class="sxs-lookup"><span data-stu-id="23dae-115">It is recommended that message objects expose this property.</span></span>
  
<span data-ttu-id="23dae-116">Это свойство может иметь только одно из следующих значений:</span><span class="sxs-lookup"><span data-stu-id="23dae-116">This property can have exactly one of the following values:</span></span>
  
<span data-ttu-id="23dae-117">SENSITIVITY_NONE</span><span class="sxs-lookup"><span data-stu-id="23dae-117">SENSITIVITY_NONE</span></span> 
  
> <span data-ttu-id="23dae-118">Сообщение не имеет особой чувствительности.</span><span class="sxs-lookup"><span data-stu-id="23dae-118">The message has no special sensitivity.</span></span>
    
<span data-ttu-id="23dae-119">SENSITIVITY_PERSONAL</span><span class="sxs-lookup"><span data-stu-id="23dae-119">SENSITIVITY_PERSONAL</span></span> 
  
> <span data-ttu-id="23dae-120">Сообщение является личным.</span><span class="sxs-lookup"><span data-stu-id="23dae-120">The message is personal.</span></span>
    
<span data-ttu-id="23dae-121">SENSITIVITY_PRIVATE</span><span class="sxs-lookup"><span data-stu-id="23dae-121">SENSITIVITY_PRIVATE</span></span> 
  
> <span data-ttu-id="23dae-122">Сообщение является частным.</span><span class="sxs-lookup"><span data-stu-id="23dae-122">The message is private.</span></span>
    
<span data-ttu-id="23dae-123">SENSITIVITY_COMPANY_CONFIDENTIAL</span><span class="sxs-lookup"><span data-stu-id="23dae-123">SENSITIVITY_COMPANY_CONFIDENTIAL</span></span> 
  
> <span data-ttu-id="23dae-124">Сообщение предназначено для конфиденциальной компании.</span><span class="sxs-lookup"><span data-stu-id="23dae-124">The message is designated company confidential.</span></span>
    
## <a name="related-resources"></a><span data-ttu-id="23dae-125">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="23dae-125">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="23dae-126">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="23dae-126">Protocol specifications</span></span>

<span data-ttu-id="23dae-127">[[MS — ОКСПРОПС]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="23dae-127">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="23dae-128">Содержит ссылки на соответствующие спецификации протоколов Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="23dae-128">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="23dae-129">[[MS — ОКСКМСГ]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="23dae-129">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="23dae-130">Обрабатывает объекты сообщений и вложений.</span><span class="sxs-lookup"><span data-stu-id="23dae-130">Handles message and attachment objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="23dae-131">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="23dae-131">Header files</span></span>

<span data-ttu-id="23dae-132">MAPIDEFS. h</span><span class="sxs-lookup"><span data-stu-id="23dae-132">Mapidefs.h</span></span>
  
> <span data-ttu-id="23dae-133">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="23dae-133">Provides data type definitions.</span></span>
    
<span data-ttu-id="23dae-134">Мапитагс. h</span><span class="sxs-lookup"><span data-stu-id="23dae-134">Mapitags.h</span></span>
  
> <span data-ttu-id="23dae-135">Содержит определения свойств, перечисленных как альтернативные имена.</span><span class="sxs-lookup"><span data-stu-id="23dae-135">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="23dae-136">См. также</span><span class="sxs-lookup"><span data-stu-id="23dae-136">See also</span></span>



[<span data-ttu-id="23dae-137">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="23dae-137">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="23dae-138">Каноническое свойство MAPI</span><span class="sxs-lookup"><span data-stu-id="23dae-138">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="23dae-139">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="23dae-139">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="23dae-140">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="23dae-140">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)


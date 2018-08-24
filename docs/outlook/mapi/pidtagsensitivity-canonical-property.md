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
ms.openlocfilehash: f30a5848e07de03e61d3a63188aa7b608504ff24
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22573735"
---
# <a name="pidtagsensitivity-canonical-property"></a><span data-ttu-id="c8dd8-103">Каноническое свойство PidTagSensitivity</span><span class="sxs-lookup"><span data-stu-id="c8dd8-103">PidTagSensitivity Canonical Property</span></span>

  
  
<span data-ttu-id="c8dd8-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c8dd8-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c8dd8-105">Содержит значение, которое указывает мнение отправителя сообщения о конфиденциальности сообщения.</span><span class="sxs-lookup"><span data-stu-id="c8dd8-105">Contains a value that indicates the message sender's opinion of the sensitivity of a message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="c8dd8-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="c8dd8-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="c8dd8-107">PR_SENSITIVITY</span><span class="sxs-lookup"><span data-stu-id="c8dd8-107">PR_SENSITIVITY</span></span>  <br/> |
|<span data-ttu-id="c8dd8-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="c8dd8-108">Identifier:</span></span>  <br/> |<span data-ttu-id="c8dd8-109">0x0036</span><span class="sxs-lookup"><span data-stu-id="c8dd8-109">0x0036</span></span>  <br/> |
|<span data-ttu-id="c8dd8-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="c8dd8-110">Data type:</span></span>  <br/> |<span data-ttu-id="c8dd8-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="c8dd8-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="c8dd8-112">Область:</span><span class="sxs-lookup"><span data-stu-id="c8dd8-112">Area:</span></span>  <br/> |<span data-ttu-id="c8dd8-113">Общие системы обмена сообщениями</span><span class="sxs-lookup"><span data-stu-id="c8dd8-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c8dd8-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="c8dd8-114">Remarks</span></span>

<span data-ttu-id="c8dd8-115">Рекомендуется, что сообщение объекты предоставляют это свойство.</span><span class="sxs-lookup"><span data-stu-id="c8dd8-115">It is recommended that message objects expose this property.</span></span>
  
<span data-ttu-id="c8dd8-116">Это свойство может иметь только один из следующих значений:</span><span class="sxs-lookup"><span data-stu-id="c8dd8-116">This property can have exactly one of the following values:</span></span>
  
<span data-ttu-id="c8dd8-117">SENSITIVITY_NONE</span><span class="sxs-lookup"><span data-stu-id="c8dd8-117">SENSITIVITY_NONE</span></span> 
  
> <span data-ttu-id="c8dd8-118">Сообщение имеет нет специальных знаков.</span><span class="sxs-lookup"><span data-stu-id="c8dd8-118">The message has no special sensitivity.</span></span>
    
<span data-ttu-id="c8dd8-119">SENSITIVITY_PERSONAL</span><span class="sxs-lookup"><span data-stu-id="c8dd8-119">SENSITIVITY_PERSONAL</span></span> 
  
> <span data-ttu-id="c8dd8-120">Личные сообщения.</span><span class="sxs-lookup"><span data-stu-id="c8dd8-120">The message is personal.</span></span>
    
<span data-ttu-id="c8dd8-121">SENSITIVITY_PRIVATE</span><span class="sxs-lookup"><span data-stu-id="c8dd8-121">SENSITIVITY_PRIVATE</span></span> 
  
> <span data-ttu-id="c8dd8-122">Сообщение является частной.</span><span class="sxs-lookup"><span data-stu-id="c8dd8-122">The message is private.</span></span>
    
<span data-ttu-id="c8dd8-123">SENSITIVITY_COMPANY_CONFIDENTIAL</span><span class="sxs-lookup"><span data-stu-id="c8dd8-123">SENSITIVITY_COMPANY_CONFIDENTIAL</span></span> 
  
> <span data-ttu-id="c8dd8-124">Сообщение является определенных служебное, конфиденциальное.</span><span class="sxs-lookup"><span data-stu-id="c8dd8-124">The message is designated company confidential.</span></span>
    
## <a name="related-resources"></a><span data-ttu-id="c8dd8-125">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="c8dd8-125">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="c8dd8-126">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="c8dd8-126">Protocol specifications</span></span>

<span data-ttu-id="c8dd8-127">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c8dd8-127">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c8dd8-128">Содержит ссылки на связанные спецификаций протокола Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="c8dd8-128">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="c8dd8-129">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c8dd8-129">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c8dd8-130">Обрабатывает объекты сообщения и вложения.</span><span class="sxs-lookup"><span data-stu-id="c8dd8-130">Handles message and attachment objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="c8dd8-131">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="c8dd8-131">Header files</span></span>

<span data-ttu-id="c8dd8-132">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="c8dd8-132">Mapidefs.h</span></span>
  
> <span data-ttu-id="c8dd8-133">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="c8dd8-133">Provides data type definitions.</span></span>
    
<span data-ttu-id="c8dd8-134">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="c8dd8-134">Mapitags.h</span></span>
  
> <span data-ttu-id="c8dd8-135">Содержит определения свойства в списке альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="c8dd8-135">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="c8dd8-136">См. также</span><span class="sxs-lookup"><span data-stu-id="c8dd8-136">See also</span></span>



[<span data-ttu-id="c8dd8-137">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="c8dd8-137">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="c8dd8-138">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="c8dd8-138">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="c8dd8-139">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="c8dd8-139">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="c8dd8-140">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="c8dd8-140">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)


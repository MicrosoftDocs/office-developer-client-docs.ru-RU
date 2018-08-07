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
ms.openlocfilehash: 93be3351749ac3e9d285fb214f746d58b55fb5b2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19811898"
---
# <a name="pidtagsensitivity-canonical-property"></a><span data-ttu-id="33936-103">Каноническое свойство PidTagSensitivity</span><span class="sxs-lookup"><span data-stu-id="33936-103">PidTagSensitivity Canonical Property</span></span>

  
  
<span data-ttu-id="33936-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="33936-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="33936-105">Содержит значение, которое указывает мнение отправителя сообщения о конфиденциальности сообщения.</span><span class="sxs-lookup"><span data-stu-id="33936-105">Contains a value that indicates the message sender's opinion of the sensitivity of a message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="33936-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="33936-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="33936-107">PR_SENSITIVITY</span><span class="sxs-lookup"><span data-stu-id="33936-107">PR_SENSITIVITY</span></span>  <br/> |
|<span data-ttu-id="33936-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="33936-108">Identifier:</span></span>  <br/> |<span data-ttu-id="33936-109">0x0036</span><span class="sxs-lookup"><span data-stu-id="33936-109">0x0036</span></span>  <br/> |
|<span data-ttu-id="33936-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="33936-110">Data type:</span></span>  <br/> |<span data-ttu-id="33936-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="33936-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="33936-112">Область:</span><span class="sxs-lookup"><span data-stu-id="33936-112">Area:</span></span>  <br/> |<span data-ttu-id="33936-113">Общие системы обмена сообщениями</span><span class="sxs-lookup"><span data-stu-id="33936-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="33936-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="33936-114">Remarks</span></span>

<span data-ttu-id="33936-115">Рекомендуется, что сообщение объекты предоставляют это свойство.</span><span class="sxs-lookup"><span data-stu-id="33936-115">It is recommended that message objects expose this property.</span></span>
  
<span data-ttu-id="33936-116">Это свойство может иметь только один из следующих значений:</span><span class="sxs-lookup"><span data-stu-id="33936-116">This property can have exactly one of the following values:</span></span>
  
<span data-ttu-id="33936-117">SENSITIVITY_NONE</span><span class="sxs-lookup"><span data-stu-id="33936-117">SENSITIVITY_NONE</span></span> 
  
> <span data-ttu-id="33936-118">Сообщение имеет нет специальных знаков.</span><span class="sxs-lookup"><span data-stu-id="33936-118">The message has no special sensitivity.</span></span>
    
<span data-ttu-id="33936-119">SENSITIVITY_PERSONAL</span><span class="sxs-lookup"><span data-stu-id="33936-119">SENSITIVITY_PERSONAL</span></span> 
  
> <span data-ttu-id="33936-120">Личные сообщения.</span><span class="sxs-lookup"><span data-stu-id="33936-120">The message is personal.</span></span>
    
<span data-ttu-id="33936-121">SENSITIVITY_PRIVATE</span><span class="sxs-lookup"><span data-stu-id="33936-121">SENSITIVITY_PRIVATE</span></span> 
  
> <span data-ttu-id="33936-122">Сообщение является частной.</span><span class="sxs-lookup"><span data-stu-id="33936-122">The message is private.</span></span>
    
<span data-ttu-id="33936-123">SENSITIVITY_COMPANY_CONFIDENTIAL</span><span class="sxs-lookup"><span data-stu-id="33936-123">SENSITIVITY_COMPANY_CONFIDENTIAL</span></span> 
  
> <span data-ttu-id="33936-124">Сообщение является определенных служебное, конфиденциальное.</span><span class="sxs-lookup"><span data-stu-id="33936-124">The message is designated company confidential.</span></span>
    
## <a name="related-resources"></a><span data-ttu-id="33936-125">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="33936-125">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="33936-126">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="33936-126">Protocol specifications</span></span>

<span data-ttu-id="33936-127">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="33936-127">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="33936-128">Содержит ссылки на связанные спецификаций протокола Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="33936-128">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="33936-129">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="33936-129">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="33936-130">Обрабатывает объекты сообщения и вложения.</span><span class="sxs-lookup"><span data-stu-id="33936-130">Handles message and attachment objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="33936-131">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="33936-131">Header files</span></span>

<span data-ttu-id="33936-132">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="33936-132">Mapidefs.h</span></span>
  
> <span data-ttu-id="33936-133">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="33936-133">Provides data type definitions.</span></span>
    
<span data-ttu-id="33936-134">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="33936-134">Mapitags.h</span></span>
  
> <span data-ttu-id="33936-135">Содержит определения свойства в списке альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="33936-135">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="33936-136">См. также</span><span class="sxs-lookup"><span data-stu-id="33936-136">See also</span></span>



[<span data-ttu-id="33936-137">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="33936-137">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="33936-138">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="33936-138">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="33936-139">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="33936-139">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="33936-140">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="33936-140">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)


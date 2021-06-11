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
# <a name="pidtagsensitivity-canonical-property"></a><span data-ttu-id="a48a5-103">Каноническое свойство PidTagSensitivity</span><span class="sxs-lookup"><span data-stu-id="a48a5-103">PidTagSensitivity Canonical Property</span></span>

  
  
<span data-ttu-id="a48a5-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a48a5-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a48a5-105">Содержит значение, которое указывает на мнение отправитель сообщения о чувствительности сообщения.</span><span class="sxs-lookup"><span data-stu-id="a48a5-105">Contains a value that indicates the message sender's opinion of the sensitivity of a message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="a48a5-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="a48a5-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="a48a5-107">PR_SENSITIVITY</span><span class="sxs-lookup"><span data-stu-id="a48a5-107">PR_SENSITIVITY</span></span>  <br/> |
|<span data-ttu-id="a48a5-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="a48a5-108">Identifier:</span></span>  <br/> |<span data-ttu-id="a48a5-109">0x0036</span><span class="sxs-lookup"><span data-stu-id="a48a5-109">0x0036</span></span>  <br/> |
|<span data-ttu-id="a48a5-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="a48a5-110">Data type:</span></span>  <br/> |<span data-ttu-id="a48a5-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="a48a5-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="a48a5-112">Область:</span><span class="sxs-lookup"><span data-stu-id="a48a5-112">Area:</span></span>  <br/> |<span data-ttu-id="a48a5-113">Общие сообщения</span><span class="sxs-lookup"><span data-stu-id="a48a5-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a48a5-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="a48a5-114">Remarks</span></span>

<span data-ttu-id="a48a5-115">Рекомендуется, чтобы объекты сообщений выставили это свойство.</span><span class="sxs-lookup"><span data-stu-id="a48a5-115">It is recommended that message objects expose this property.</span></span>
  
<span data-ttu-id="a48a5-116">Это свойство может иметь одно из следующих значений:</span><span class="sxs-lookup"><span data-stu-id="a48a5-116">This property can have exactly one of the following values:</span></span>
  
<span data-ttu-id="a48a5-117">SENSITIVITY_NONE</span><span class="sxs-lookup"><span data-stu-id="a48a5-117">SENSITIVITY_NONE</span></span> 
  
> <span data-ttu-id="a48a5-118">Сообщение не имеет особой чувствительности.</span><span class="sxs-lookup"><span data-stu-id="a48a5-118">The message has no special sensitivity.</span></span>
    
<span data-ttu-id="a48a5-119">SENSITIVITY_PERSONAL</span><span class="sxs-lookup"><span data-stu-id="a48a5-119">SENSITIVITY_PERSONAL</span></span> 
  
> <span data-ttu-id="a48a5-120">Сообщение личное.</span><span class="sxs-lookup"><span data-stu-id="a48a5-120">The message is personal.</span></span>
    
<span data-ttu-id="a48a5-121">SENSITIVITY_PRIVATE</span><span class="sxs-lookup"><span data-stu-id="a48a5-121">SENSITIVITY_PRIVATE</span></span> 
  
> <span data-ttu-id="a48a5-122">Сообщение закрыто.</span><span class="sxs-lookup"><span data-stu-id="a48a5-122">The message is private.</span></span>
    
<span data-ttu-id="a48a5-123">SENSITIVITY_COMPANY_CONFIDENTIAL</span><span class="sxs-lookup"><span data-stu-id="a48a5-123">SENSITIVITY_COMPANY_CONFIDENTIAL</span></span> 
  
> <span data-ttu-id="a48a5-124">Сообщение назначено конфиденциальной компанией.</span><span class="sxs-lookup"><span data-stu-id="a48a5-124">The message is designated company confidential.</span></span>
    
## <a name="related-resources"></a><span data-ttu-id="a48a5-125">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="a48a5-125">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="a48a5-126">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="a48a5-126">Protocol specifications</span></span>

<span data-ttu-id="a48a5-127">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="a48a5-127">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="a48a5-128">Содержит ссылки на связанные Exchange Server протоколы.</span><span class="sxs-lookup"><span data-stu-id="a48a5-128">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="a48a5-129">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="a48a5-129">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="a48a5-130">Обрабатывает объекты сообщений и вложений.</span><span class="sxs-lookup"><span data-stu-id="a48a5-130">Handles message and attachment objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="a48a5-131">Файлы заголовки</span><span class="sxs-lookup"><span data-stu-id="a48a5-131">Header files</span></span>

<span data-ttu-id="a48a5-132">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="a48a5-132">Mapidefs.h</span></span>
  
> <span data-ttu-id="a48a5-133">Предоставляет определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="a48a5-133">Provides data type definitions.</span></span>
    
<span data-ttu-id="a48a5-134">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="a48a5-134">Mapitags.h</span></span>
  
> <span data-ttu-id="a48a5-135">Содержит определения свойств, перечисленных в качестве альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="a48a5-135">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="a48a5-136">См. также</span><span class="sxs-lookup"><span data-stu-id="a48a5-136">See also</span></span>



[<span data-ttu-id="a48a5-137">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="a48a5-137">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="a48a5-138">Канонические свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="a48a5-138">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="a48a5-139">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="a48a5-139">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="a48a5-140">Сопоставление имен MAPI с каноническими именами свойств</span><span class="sxs-lookup"><span data-stu-id="a48a5-140">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)


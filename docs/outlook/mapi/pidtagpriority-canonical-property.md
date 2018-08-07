---
title: Каноническое свойство PidTagPriority
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagPriority
api_type:
- COM
ms.assetid: 0f3a628f-5f8e-4716-98cc-868bd3400ba9
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 67f482e347db1b69a248c542f2cb172c41d6f9f1
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19811559"
---
# <a name="pidtagpriority-canonical-property"></a><span data-ttu-id="686d0-103">Каноническое свойство PidTagPriority</span><span class="sxs-lookup"><span data-stu-id="686d0-103">PidTagPriority Canonical Property</span></span>

  
  
<span data-ttu-id="686d0-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="686d0-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="686d0-105">Содержит относительный приоритет сообщения.</span><span class="sxs-lookup"><span data-stu-id="686d0-105">Contains the relative priority of a message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="686d0-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="686d0-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="686d0-107">PR_PRIORITY</span><span class="sxs-lookup"><span data-stu-id="686d0-107">PR_PRIORITY</span></span>  <br/> |
|<span data-ttu-id="686d0-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="686d0-108">Identifier:</span></span>  <br/> |<span data-ttu-id="686d0-109">0x0026</span><span class="sxs-lookup"><span data-stu-id="686d0-109">0x0026</span></span>  <br/> |
|<span data-ttu-id="686d0-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="686d0-110">Data type:</span></span>  <br/> |<span data-ttu-id="686d0-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="686d0-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="686d0-112">Область:</span><span class="sxs-lookup"><span data-stu-id="686d0-112">Area:</span></span>  <br/> |<span data-ttu-id="686d0-113">Электронная почта</span><span class="sxs-lookup"><span data-stu-id="686d0-113">Email</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="686d0-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="686d0-114">Remarks</span></span>

<span data-ttu-id="686d0-115">Не следует путать это свойство и свойство **PR_IMPORTANCE** ([PidTagImportance](pidtagimportance-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="686d0-115">This property and the **PR_IMPORTANCE** ([PidTagImportance](pidtagimportance-canonical-property.md)) property should not be confused.</span></span> <span data-ttu-id="686d0-116">Importance указывает значение для пользователей, а приоритет указывает порядок или скорость, при которой сообщения направляются программным обеспечением системы обмена сообщениями.</span><span class="sxs-lookup"><span data-stu-id="686d0-116">Importance indicates a value to users, while priority indicates the order or speed at which the message should be sent by the messaging system software.</span></span> <span data-ttu-id="686d0-117">Более высокий приоритет обычно указывает выше затрат.</span><span class="sxs-lookup"><span data-stu-id="686d0-117">Higher priority usually indicates a higher cost.</span></span> <span data-ttu-id="686d0-118">Важность выше обычно связан с другой дисплей с помощью пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="686d0-118">Higher importance usually is associated with a different display by the user interface.</span></span>
  
<span data-ttu-id="686d0-119">Приоритет сообщения отчета должен совпадать с приоритетом исходное сообщение об.</span><span class="sxs-lookup"><span data-stu-id="686d0-119">The priority of a report message should be the same as the priority of the original message being reported.</span></span>
  
<span data-ttu-id="686d0-120">Это свойство может иметь только один из следующих значений:</span><span class="sxs-lookup"><span data-stu-id="686d0-120">This property can have exactly one of the following values:</span></span>
  
<span data-ttu-id="686d0-121">PRIO_NONURGENT</span><span class="sxs-lookup"><span data-stu-id="686d0-121">PRIO_NONURGENT</span></span> 
  
> <span data-ttu-id="686d0-122">Сообщение не является срочным.</span><span class="sxs-lookup"><span data-stu-id="686d0-122">The message is not urgent.</span></span>
    
<span data-ttu-id="686d0-123">PRIO_NORMAL</span><span class="sxs-lookup"><span data-stu-id="686d0-123">PRIO_NORMAL</span></span> 
  
> <span data-ttu-id="686d0-124">Сообщение имеет обычным приоритетом.</span><span class="sxs-lookup"><span data-stu-id="686d0-124">The message has normal priority.</span></span>
    
<span data-ttu-id="686d0-125">PRIO_URGENT</span><span class="sxs-lookup"><span data-stu-id="686d0-125">PRIO_URGENT</span></span> 
  
> <span data-ttu-id="686d0-126">Сообщение является срочным.</span><span class="sxs-lookup"><span data-stu-id="686d0-126">The message is urgent.</span></span>
    
## <a name="related-resources"></a><span data-ttu-id="686d0-127">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="686d0-127">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="686d0-128">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="686d0-128">Protocol specifications</span></span>

<span data-ttu-id="686d0-129">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="686d0-129">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="686d0-130">Содержит ссылки на связанные спецификаций протокола Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="686d0-130">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="686d0-131">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="686d0-131">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="686d0-132">Задает свойства и операции, допустимые для объектов сообщения электронной почты.</span><span class="sxs-lookup"><span data-stu-id="686d0-132">Specifies the properties and operations that are permissible on email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="686d0-133">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="686d0-133">Header files</span></span>

<span data-ttu-id="686d0-134">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="686d0-134">Mapidefs.h</span></span>
  
> <span data-ttu-id="686d0-135">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="686d0-135">Provides data type definitions.</span></span>
    
<span data-ttu-id="686d0-136">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="686d0-136">Mapitags.h</span></span>
  
> <span data-ttu-id="686d0-137">Содержит определения свойства в списке альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="686d0-137">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="686d0-138">См. также</span><span class="sxs-lookup"><span data-stu-id="686d0-138">See also</span></span>



[<span data-ttu-id="686d0-139">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="686d0-139">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="686d0-140">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="686d0-140">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="686d0-141">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="686d0-141">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="686d0-142">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="686d0-142">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)


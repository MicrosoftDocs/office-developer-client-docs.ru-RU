---
title: Каноническое свойство PidTagImportance
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagImportance
api_type:
- HeaderDef
ms.assetid: 274dd444-a863-4b53-bdbc-3763c375c43c
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 6bef8b05f2fbf94b74ee126b80dfc6ae0c5e9d11
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25400833"
---
# <a name="pidtagimportance-canonical-property"></a><span data-ttu-id="a0ece-103">Каноническое свойство PidTagImportance</span><span class="sxs-lookup"><span data-stu-id="a0ece-103">PidTagImportance Canonical Property</span></span>

  
  
<span data-ttu-id="a0ece-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a0ece-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a0ece-105">Содержит значение, которое указывает мнение отправителя сообщения о важность сообщения.</span><span class="sxs-lookup"><span data-stu-id="a0ece-105">Contains a value that indicates the message sender's opinion of the importance of a message.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="a0ece-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="a0ece-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="a0ece-107">PR_IMPORTANCE</span><span class="sxs-lookup"><span data-stu-id="a0ece-107">PR_IMPORTANCE</span></span>  <br/> |
|<span data-ttu-id="a0ece-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="a0ece-108">Identifier:</span></span>  <br/> |<span data-ttu-id="a0ece-109">0x0017</span><span class="sxs-lookup"><span data-stu-id="a0ece-109">0x0017</span></span>  <br/> |
|<span data-ttu-id="a0ece-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="a0ece-110">Data type:</span></span>  <br/> |<span data-ttu-id="a0ece-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="a0ece-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="a0ece-112">Область:</span><span class="sxs-lookup"><span data-stu-id="a0ece-112">Area:</span></span>  <br/> |<span data-ttu-id="a0ece-113">Общие системы обмена сообщениями</span><span class="sxs-lookup"><span data-stu-id="a0ece-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a0ece-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="a0ece-114">Remarks</span></span>

<span data-ttu-id="a0ece-115">Не следует путать это свойство и свойство **PR_PRIORITY** ([PidTagPriority](pidtagpriority-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="a0ece-115">This property and the **PR_PRIORITY** ([PidTagPriority](pidtagpriority-canonical-property.md)) property should not be confused.</span></span> <span data-ttu-id="a0ece-116">Importance указывает значение для пользователей, а приоритет указывает порядок или скорость, при которой сообщения направляются программным обеспечением системы обмена сообщениями.</span><span class="sxs-lookup"><span data-stu-id="a0ece-116">Importance indicates a value to users, while priority indicates the order or speed at which the message should be sent by the messaging system software.</span></span> <span data-ttu-id="a0ece-117">Более высокий приоритет обычно указывает выше затрат.</span><span class="sxs-lookup"><span data-stu-id="a0ece-117">Higher priority usually indicates a higher cost.</span></span> <span data-ttu-id="a0ece-118">Важность выше обычно связан с другой дисплей с помощью пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="a0ece-118">Higher importance usually is associated with a different display by the user interface.</span></span> 
  
<span data-ttu-id="a0ece-119">Это свойство может иметь только один из следующих значений:</span><span class="sxs-lookup"><span data-stu-id="a0ece-119">This property can have exactly one of the following values:</span></span>
  
<span data-ttu-id="a0ece-120">IMPORTANCE_LOW</span><span class="sxs-lookup"><span data-stu-id="a0ece-120">IMPORTANCE_LOW</span></span> 
  
> <span data-ttu-id="a0ece-121">Сообщение имеет Низкая важность.</span><span class="sxs-lookup"><span data-stu-id="a0ece-121">The message has low importance.</span></span>
    
<span data-ttu-id="a0ece-122">IMPORTANCE_HIGH</span><span class="sxs-lookup"><span data-stu-id="a0ece-122">IMPORTANCE_HIGH</span></span> 
  
> <span data-ttu-id="a0ece-123">Сообщение имеет высокой важности.</span><span class="sxs-lookup"><span data-stu-id="a0ece-123">The message has high importance.</span></span>
    
<span data-ttu-id="a0ece-124">IMPORTANCE_NORMAL</span><span class="sxs-lookup"><span data-stu-id="a0ece-124">IMPORTANCE_NORMAL</span></span> 
  
> <span data-ttu-id="a0ece-125">Сообщение имеет обычную.</span><span class="sxs-lookup"><span data-stu-id="a0ece-125">The message has normal importance.</span></span>
    
## <a name="related-resources"></a><span data-ttu-id="a0ece-126">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="a0ece-126">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="a0ece-127">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="a0ece-127">Protocol specifications</span></span>

<span data-ttu-id="a0ece-128">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="a0ece-128">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="a0ece-129">Содержит ссылки на связанные спецификаций протокола Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="a0ece-129">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="a0ece-130">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="a0ece-130">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="a0ece-131">Обрабатывает объекты сообщения и вложения.</span><span class="sxs-lookup"><span data-stu-id="a0ece-131">Handles message and attachment objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="a0ece-132">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="a0ece-132">Header files</span></span>

<span data-ttu-id="a0ece-133">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="a0ece-133">Mapidefs.h</span></span>
  
> <span data-ttu-id="a0ece-134">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="a0ece-134">Provides data type definitions.</span></span>
    
<span data-ttu-id="a0ece-135">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="a0ece-135">Mapitags.h</span></span>
  
> <span data-ttu-id="a0ece-136">Содержит определения свойства в списке альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="a0ece-136">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="a0ece-137">См. также</span><span class="sxs-lookup"><span data-stu-id="a0ece-137">See also</span></span>



[<span data-ttu-id="a0ece-138">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="a0ece-138">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="a0ece-139">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="a0ece-139">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="a0ece-140">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="a0ece-140">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="a0ece-141">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="a0ece-141">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)


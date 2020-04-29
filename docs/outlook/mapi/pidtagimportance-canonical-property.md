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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32327925"
---
# <a name="pidtagimportance-canonical-property"></a><span data-ttu-id="ab02a-103">Каноническое свойство PidTagImportance</span><span class="sxs-lookup"><span data-stu-id="ab02a-103">PidTagImportance Canonical Property</span></span>

  
  
<span data-ttu-id="ab02a-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ab02a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ab02a-105">Содержит значение, указывающее на отправителя сообщения о важности сообщения.</span><span class="sxs-lookup"><span data-stu-id="ab02a-105">Contains a value that indicates the message sender's opinion of the importance of a message.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="ab02a-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="ab02a-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="ab02a-107">PR_IMPORTANCE</span><span class="sxs-lookup"><span data-stu-id="ab02a-107">PR_IMPORTANCE</span></span>  <br/> |
|<span data-ttu-id="ab02a-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="ab02a-108">Identifier:</span></span>  <br/> |<span data-ttu-id="ab02a-109">0x0017</span><span class="sxs-lookup"><span data-stu-id="ab02a-109">0x0017</span></span>  <br/> |
|<span data-ttu-id="ab02a-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="ab02a-110">Data type:</span></span>  <br/> |<span data-ttu-id="ab02a-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="ab02a-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="ab02a-112">Область:</span><span class="sxs-lookup"><span data-stu-id="ab02a-112">Area:</span></span>  <br/> |<span data-ttu-id="ab02a-113">Общий обмен сообщениями</span><span class="sxs-lookup"><span data-stu-id="ab02a-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ab02a-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="ab02a-114">Remarks</span></span>

<span data-ttu-id="ab02a-115">Это свойство и свойство **PR_PRIORITY** ([PidTagPriority](pidtagpriority-canonical-property.md)) не следует путать.</span><span class="sxs-lookup"><span data-stu-id="ab02a-115">This property and the **PR_PRIORITY** ([PidTagPriority](pidtagpriority-canonical-property.md)) property should not be confused.</span></span> <span data-ttu-id="ab02a-116">Важность указывает на значение для пользователей, а Priority указывает порядок или скорость, при которой сообщение должно быть отправлено программным обеспечением системы обмена сообщениями.</span><span class="sxs-lookup"><span data-stu-id="ab02a-116">Importance indicates a value to users, while priority indicates the order or speed at which the message should be sent by the messaging system software.</span></span> <span data-ttu-id="ab02a-117">Более высокий приоритет обычно указывает на более высокую стоимость.</span><span class="sxs-lookup"><span data-stu-id="ab02a-117">Higher priority usually indicates a higher cost.</span></span> <span data-ttu-id="ab02a-118">Более высокая важность обычно связана с другим отображением пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="ab02a-118">Higher importance usually is associated with a different display by the user interface.</span></span> 
  
<span data-ttu-id="ab02a-119">Это свойство может иметь только одно из следующих значений:</span><span class="sxs-lookup"><span data-stu-id="ab02a-119">This property can have exactly one of the following values:</span></span>
  
<span data-ttu-id="ab02a-120">IMPORTANCE_LOW</span><span class="sxs-lookup"><span data-stu-id="ab02a-120">IMPORTANCE_LOW</span></span> 
  
> <span data-ttu-id="ab02a-121">Сообщение имеет низкую важность.</span><span class="sxs-lookup"><span data-stu-id="ab02a-121">The message has low importance.</span></span>
    
<span data-ttu-id="ab02a-122">IMPORTANCE_HIGH</span><span class="sxs-lookup"><span data-stu-id="ab02a-122">IMPORTANCE_HIGH</span></span> 
  
> <span data-ttu-id="ab02a-123">Сообщение имеет высокую важность.</span><span class="sxs-lookup"><span data-stu-id="ab02a-123">The message has high importance.</span></span>
    
<span data-ttu-id="ab02a-124">IMPORTANCE_NORMAL</span><span class="sxs-lookup"><span data-stu-id="ab02a-124">IMPORTANCE_NORMAL</span></span> 
  
> <span data-ttu-id="ab02a-125">Сообщение имеет обычную важность.</span><span class="sxs-lookup"><span data-stu-id="ab02a-125">The message has normal importance.</span></span>
    
## <a name="related-resources"></a><span data-ttu-id="ab02a-126">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="ab02a-126">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="ab02a-127">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="ab02a-127">Protocol specifications</span></span>

<span data-ttu-id="ab02a-128">[[MS — ОКСПРОПС]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ab02a-128">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="ab02a-129">Содержит ссылки на соответствующие спецификации протоколов Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="ab02a-129">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="ab02a-130">[[MS — ОКСКМСГ]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ab02a-130">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="ab02a-131">Обрабатывает объекты сообщений и вложений.</span><span class="sxs-lookup"><span data-stu-id="ab02a-131">Handles message and attachment objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="ab02a-132">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="ab02a-132">Header files</span></span>

<span data-ttu-id="ab02a-133">MAPIDEFS. h</span><span class="sxs-lookup"><span data-stu-id="ab02a-133">Mapidefs.h</span></span>
  
> <span data-ttu-id="ab02a-134">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="ab02a-134">Provides data type definitions.</span></span>
    
<span data-ttu-id="ab02a-135">Мапитагс. h</span><span class="sxs-lookup"><span data-stu-id="ab02a-135">Mapitags.h</span></span>
  
> <span data-ttu-id="ab02a-136">Содержит определения свойств, перечисленных как альтернативные имена.</span><span class="sxs-lookup"><span data-stu-id="ab02a-136">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="ab02a-137">См. также</span><span class="sxs-lookup"><span data-stu-id="ab02a-137">See also</span></span>



[<span data-ttu-id="ab02a-138">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="ab02a-138">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="ab02a-139">Каноническое свойство MAPI</span><span class="sxs-lookup"><span data-stu-id="ab02a-139">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="ab02a-140">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="ab02a-140">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="ab02a-141">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="ab02a-141">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)


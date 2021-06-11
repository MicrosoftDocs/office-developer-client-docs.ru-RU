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
ms.openlocfilehash: b9c0f5ebeae21d6d683bbb5def727d29a34bcdb6
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32339433"
---
# <a name="pidtagpriority-canonical-property"></a><span data-ttu-id="3a274-103">Каноническое свойство PidTagPriority</span><span class="sxs-lookup"><span data-stu-id="3a274-103">PidTagPriority Canonical Property</span></span>

  
  
<span data-ttu-id="3a274-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3a274-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3a274-105">Содержит относительный приоритет сообщения.</span><span class="sxs-lookup"><span data-stu-id="3a274-105">Contains the relative priority of a message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="3a274-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="3a274-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="3a274-107">PR_PRIORITY</span><span class="sxs-lookup"><span data-stu-id="3a274-107">PR_PRIORITY</span></span>  <br/> |
|<span data-ttu-id="3a274-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="3a274-108">Identifier:</span></span>  <br/> |<span data-ttu-id="3a274-109">0x0026</span><span class="sxs-lookup"><span data-stu-id="3a274-109">0x0026</span></span>  <br/> |
|<span data-ttu-id="3a274-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="3a274-110">Data type:</span></span>  <br/> |<span data-ttu-id="3a274-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="3a274-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="3a274-112">Область:</span><span class="sxs-lookup"><span data-stu-id="3a274-112">Area:</span></span>  <br/> |<span data-ttu-id="3a274-113">Электронная почта</span><span class="sxs-lookup"><span data-stu-id="3a274-113">Email</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="3a274-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="3a274-114">Remarks</span></span>

<span data-ttu-id="3a274-115">Это свойство и **PR_IMPORTANCE** [(PidTagImportance)](pidtagimportance-canonical-property.md)не следует путать.</span><span class="sxs-lookup"><span data-stu-id="3a274-115">This property and the **PR_IMPORTANCE** ([PidTagImportance](pidtagimportance-canonical-property.md)) property should not be confused.</span></span> <span data-ttu-id="3a274-116">Значение указывает значение для пользователей, в то время как приоритет указывает порядок или скорость отправки сообщения программным обеспечением системы обмена сообщениями.</span><span class="sxs-lookup"><span data-stu-id="3a274-116">Importance indicates a value to users, while priority indicates the order or speed at which the message should be sent by the messaging system software.</span></span> <span data-ttu-id="3a274-117">Более высокий приоритет обычно указывает на более высокую стоимость.</span><span class="sxs-lookup"><span data-stu-id="3a274-117">Higher priority usually indicates a higher cost.</span></span> <span data-ttu-id="3a274-118">Более высокое значение обычно связано с другим отображением пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="3a274-118">Higher importance usually is associated with a different display by the user interface.</span></span>
  
<span data-ttu-id="3a274-119">Приоритет сообщения отчетов должен быть таким же, как и приоритет исходного сообщения.</span><span class="sxs-lookup"><span data-stu-id="3a274-119">The priority of a report message should be the same as the priority of the original message being reported.</span></span>
  
<span data-ttu-id="3a274-120">Это свойство может иметь одно из следующих значений:</span><span class="sxs-lookup"><span data-stu-id="3a274-120">This property can have exactly one of the following values:</span></span>
  
<span data-ttu-id="3a274-121">PRIO_NONURGENT</span><span class="sxs-lookup"><span data-stu-id="3a274-121">PRIO_NONURGENT</span></span> 
  
> <span data-ttu-id="3a274-122">Сообщение не является срочным.</span><span class="sxs-lookup"><span data-stu-id="3a274-122">The message is not urgent.</span></span>
    
<span data-ttu-id="3a274-123">PRIO_NORMAL</span><span class="sxs-lookup"><span data-stu-id="3a274-123">PRIO_NORMAL</span></span> 
  
> <span data-ttu-id="3a274-124">Сообщение имеет обычный приоритет.</span><span class="sxs-lookup"><span data-stu-id="3a274-124">The message has normal priority.</span></span>
    
<span data-ttu-id="3a274-125">PRIO_URGENT</span><span class="sxs-lookup"><span data-stu-id="3a274-125">PRIO_URGENT</span></span> 
  
> <span data-ttu-id="3a274-126">Сообщение является срочным.</span><span class="sxs-lookup"><span data-stu-id="3a274-126">The message is urgent.</span></span>
    
## <a name="related-resources"></a><span data-ttu-id="3a274-127">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="3a274-127">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="3a274-128">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="3a274-128">Protocol specifications</span></span>

<span data-ttu-id="3a274-129">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="3a274-129">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="3a274-130">Содержит ссылки на связанные Exchange Server протоколы.</span><span class="sxs-lookup"><span data-stu-id="3a274-130">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="3a274-131">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="3a274-131">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="3a274-132">Указывает свойства и операции, допустимые на объектах сообщений электронной почты.</span><span class="sxs-lookup"><span data-stu-id="3a274-132">Specifies the properties and operations that are permissible on email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="3a274-133">Файлы заголовки</span><span class="sxs-lookup"><span data-stu-id="3a274-133">Header files</span></span>

<span data-ttu-id="3a274-134">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="3a274-134">Mapidefs.h</span></span>
  
> <span data-ttu-id="3a274-135">Предоставляет определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="3a274-135">Provides data type definitions.</span></span>
    
<span data-ttu-id="3a274-136">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="3a274-136">Mapitags.h</span></span>
  
> <span data-ttu-id="3a274-137">Содержит определения свойств, перечисленных в качестве альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="3a274-137">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="3a274-138">См. также</span><span class="sxs-lookup"><span data-stu-id="3a274-138">See also</span></span>



[<span data-ttu-id="3a274-139">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="3a274-139">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="3a274-140">Канонические свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="3a274-140">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="3a274-141">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="3a274-141">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="3a274-142">Сопоставление имен MAPI с каноническими именами свойств</span><span class="sxs-lookup"><span data-stu-id="3a274-142">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)


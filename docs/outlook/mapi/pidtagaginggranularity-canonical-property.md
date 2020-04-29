---
title: Каноническое свойство PidTagAgingGranularity
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagAgingGranularity
api_type:
- HeaderDef
ms.assetid: b79ec87d-d97c-4e6c-899b-78ebf1b485a7
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: b4006b62758b32598a64eaa4eb333c7ce5b12605
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32325587"
---
# <a name="pidtagaginggranularity-canonical-property"></a><span data-ttu-id="490c0-103">Каноническое свойство PidTagAgingGranularity</span><span class="sxs-lookup"><span data-stu-id="490c0-103">PidTagAgingGranularity Canonical Property</span></span>

  
  
<span data-ttu-id="490c0-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="490c0-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="490c0-105">Представляет единицу времени, используемую для определения промежутка времени, в течение которого элемент остается в папке, прежде чем элемент будет архивирован.</span><span class="sxs-lookup"><span data-stu-id="490c0-105">Represents the unit of time that is used in determining the length of time an item remains in a folder before the item is archived.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="490c0-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="490c0-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="490c0-107">PR_AGING_GRANULARITY</span><span class="sxs-lookup"><span data-stu-id="490c0-107">PR_AGING_GRANULARITY</span></span>  <br/> |
|<span data-ttu-id="490c0-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="490c0-108">Identifier:</span></span>  <br/> |<span data-ttu-id="490c0-109">0x36EE</span><span class="sxs-lookup"><span data-stu-id="490c0-109">0x36EE</span></span>  <br/> |
|<span data-ttu-id="490c0-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="490c0-110">Data type:</span></span>  <br/> |<span data-ttu-id="490c0-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="490c0-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="490c0-112">Область:</span><span class="sxs-lookup"><span data-stu-id="490c0-112">Area:</span></span>  <br/> |<span data-ttu-id="490c0-113">Разное</span><span class="sxs-lookup"><span data-stu-id="490c0-113">Miscellaneous</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="490c0-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="490c0-114">Remarks</span></span>

<span data-ttu-id="490c0-115">Возможные значения для **PR_AGING_GRANULARITY** могут быть одним из следующих.</span><span class="sxs-lookup"><span data-stu-id="490c0-115">The possible values for **PR_AGING_GRANULARITY** can be one of the following.</span></span> 
  
|<span data-ttu-id="490c0-116">**Name**</span><span class="sxs-lookup"><span data-stu-id="490c0-116">**Name**</span></span>|<span data-ttu-id="490c0-117">**Value**</span><span class="sxs-lookup"><span data-stu-id="490c0-117">**Value**</span></span>|<span data-ttu-id="490c0-118">**Описание**</span><span class="sxs-lookup"><span data-stu-id="490c0-118">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="490c0-119">**AG_MONTHS**</span><span class="sxs-lookup"><span data-stu-id="490c0-119">**AG_MONTHS**</span></span> <br/> |<span data-ttu-id="490c0-120">нуль</span><span class="sxs-lookup"><span data-stu-id="490c0-120">0</span></span>  <br/> |<span data-ttu-id="490c0-121">**PR_AGING_PERIOD** задается в виде числа месяцев.</span><span class="sxs-lookup"><span data-stu-id="490c0-121">**PR_AGING_PERIOD** is defined in number of months.</span></span>  <br/> |
|<span data-ttu-id="490c0-122">**AG_WEEKS**</span><span class="sxs-lookup"><span data-stu-id="490c0-122">**AG_WEEKS**</span></span> <br/> |<span data-ttu-id="490c0-123">1,1</span><span class="sxs-lookup"><span data-stu-id="490c0-123">1</span></span>  <br/> |<span data-ttu-id="490c0-124">**PR_AGING_PERIOD** определяется в течение нескольких недель.</span><span class="sxs-lookup"><span data-stu-id="490c0-124">**PR_AGING_PERIOD** is defined in number of weeks.</span></span>  <br/> |
|<span data-ttu-id="490c0-125">**AG_DAYS**</span><span class="sxs-lookup"><span data-stu-id="490c0-125">**AG_DAYS**</span></span> <br/> |<span data-ttu-id="490c0-126">2</span><span class="sxs-lookup"><span data-stu-id="490c0-126">2</span></span>  <br/> |<span data-ttu-id="490c0-127">**PR_AGING_PERIOD** определено в днях.</span><span class="sxs-lookup"><span data-stu-id="490c0-127">**PR_AGING_PERIOD** is defined in number of days.</span></span>  <br/> |
   
<span data-ttu-id="490c0-128">Время, в течение которого элемент остается в папке, прежде чем его архивировать, будут определяться двумя свойствами, [PR_AGING_PERIOD](pidtagagingperiod-canonical-property.md) и **PR_AGING_GRANULARITY**.</span><span class="sxs-lookup"><span data-stu-id="490c0-128">The length of time that an item remains in a folder before the item is archived is determined by two properties, [PR_AGING_PERIOD](pidtagagingperiod-canonical-property.md) and **PR_AGING_GRANULARITY**.</span></span> <span data-ttu-id="490c0-129">**PR_AGING_PERIOD** представляет количество единиц времени, в течение которых элемент остается в папке, прежде чем он будет архивирован.</span><span class="sxs-lookup"><span data-stu-id="490c0-129">**PR_AGING_PERIOD** represents the number of time units that the item remains in the folder before it is archived.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="490c0-130">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="490c0-130">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="490c0-131">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="490c0-131">Protocol specifications</span></span>

<span data-ttu-id="490c0-132">[[MS — ОКСПРОПС]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="490c0-132">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="490c0-133">Содержит ссылки на соответствующие спецификации протоколов Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="490c0-133">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="490c0-134">[[MS — ОКСКФКСИКС]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="490c0-134">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="490c0-135">Определяет основные структуры данных, используемые в удаленных операциях.</span><span class="sxs-lookup"><span data-stu-id="490c0-135">Defines the basic data structures that are used in remote operations.</span></span>
    
<span data-ttu-id="490c0-136">[[MS — ОКСОМСГ]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="490c0-136">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="490c0-137">Задает свойства и операции, допустимые для объектов сообщений электронной почты.</span><span class="sxs-lookup"><span data-stu-id="490c0-137">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="490c0-138">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="490c0-138">Header files</span></span>

<span data-ttu-id="490c0-139">MAPIDEFS. h</span><span class="sxs-lookup"><span data-stu-id="490c0-139">Mapidefs.h</span></span>
  
> <span data-ttu-id="490c0-140">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="490c0-140">Provides data type definitions.</span></span>
    
<span data-ttu-id="490c0-141">Мапитагс. h</span><span class="sxs-lookup"><span data-stu-id="490c0-141">Mapitags.h</span></span>
  
> <span data-ttu-id="490c0-142">Содержит определения свойств, перечисленных как альтернативные имена.</span><span class="sxs-lookup"><span data-stu-id="490c0-142">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="490c0-143">См. также</span><span class="sxs-lookup"><span data-stu-id="490c0-143">See also</span></span>



[<span data-ttu-id="490c0-144">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="490c0-144">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="490c0-145">Каноническое свойство MAPI</span><span class="sxs-lookup"><span data-stu-id="490c0-145">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="490c0-146">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="490c0-146">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="490c0-147">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="490c0-147">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)


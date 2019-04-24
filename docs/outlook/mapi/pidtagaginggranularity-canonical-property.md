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
# <a name="pidtagaginggranularity-canonical-property"></a><span data-ttu-id="19b2e-103">Каноническое свойство PidTagAgingGranularity</span><span class="sxs-lookup"><span data-stu-id="19b2e-103">PidTagAgingGranularity Canonical Property</span></span>

  
  
<span data-ttu-id="19b2e-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="19b2e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="19b2e-105">Представляет единицу времени, используемую для определения промежутка времени, в течение которого элемент остается в папке, прежде чем элемент будет архивирован.</span><span class="sxs-lookup"><span data-stu-id="19b2e-105">Represents the unit of time that is used in determining the length of time an item remains in a folder before the item is archived.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="19b2e-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="19b2e-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="19b2e-107">ПР_АГИНГ_ГРАНУЛАРИТИ</span><span class="sxs-lookup"><span data-stu-id="19b2e-107">PR_AGING_GRANULARITY</span></span>  <br/> |
|<span data-ttu-id="19b2e-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="19b2e-108">Identifier:</span></span>  <br/> |<span data-ttu-id="19b2e-109">0x36EE</span><span class="sxs-lookup"><span data-stu-id="19b2e-109">0x36EE</span></span>  <br/> |
|<span data-ttu-id="19b2e-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="19b2e-110">Data type:</span></span>  <br/> |<span data-ttu-id="19b2e-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="19b2e-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="19b2e-112">Область:</span><span class="sxs-lookup"><span data-stu-id="19b2e-112">Area:</span></span>  <br/> |<span data-ttu-id="19b2e-113">Разное</span><span class="sxs-lookup"><span data-stu-id="19b2e-113">Miscellaneous</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="19b2e-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="19b2e-114">Remarks</span></span>

<span data-ttu-id="19b2e-115">Возможные значения для параметра **пр_агинг_грануларити** могут быть одним из следующих.</span><span class="sxs-lookup"><span data-stu-id="19b2e-115">The possible values for **PR_AGING_GRANULARITY** can be one of the following.</span></span> 
  
|<span data-ttu-id="19b2e-116">**Name**</span><span class="sxs-lookup"><span data-stu-id="19b2e-116">**Name**</span></span>|<span data-ttu-id="19b2e-117">**Value**</span><span class="sxs-lookup"><span data-stu-id="19b2e-117">**Value**</span></span>|<span data-ttu-id="19b2e-118">**Описание**</span><span class="sxs-lookup"><span data-stu-id="19b2e-118">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="19b2e-119">**АГ_МОНСС**</span><span class="sxs-lookup"><span data-stu-id="19b2e-119">**AG_MONTHS**</span></span> <br/> |<span data-ttu-id="19b2e-120">нуль</span><span class="sxs-lookup"><span data-stu-id="19b2e-120">0</span></span>  <br/> |<span data-ttu-id="19b2e-121">**Пр_агинг_период** определяется в виде числа месяцев.</span><span class="sxs-lookup"><span data-stu-id="19b2e-121">**PR_AGING_PERIOD** is defined in number of months.</span></span>  <br/> |
|<span data-ttu-id="19b2e-122">**АГ_ВИКС**</span><span class="sxs-lookup"><span data-stu-id="19b2e-122">**AG_WEEKS**</span></span> <br/> |<span data-ttu-id="19b2e-123">1,1</span><span class="sxs-lookup"><span data-stu-id="19b2e-123">1</span></span>  <br/> |<span data-ttu-id="19b2e-124">**Пр_агинг_период** определяется в виде количества недель.</span><span class="sxs-lookup"><span data-stu-id="19b2e-124">**PR_AGING_PERIOD** is defined in number of weeks.</span></span>  <br/> |
|<span data-ttu-id="19b2e-125">**АГ_ДАЙС**</span><span class="sxs-lookup"><span data-stu-id="19b2e-125">**AG_DAYS**</span></span> <br/> |<span data-ttu-id="19b2e-126">2</span><span class="sxs-lookup"><span data-stu-id="19b2e-126">2</span></span>  <br/> |<span data-ttu-id="19b2e-127">**Пр_агинг_период** определяется в виде количества дней.</span><span class="sxs-lookup"><span data-stu-id="19b2e-127">**PR_AGING_PERIOD** is defined in number of days.</span></span>  <br/> |
   
<span data-ttu-id="19b2e-128">Период времени, в течение которого элемент остается в папке до архивации элемента, определяется двумя свойствами, [пр_агинг_период](pidtagagingperiod-canonical-property.md) и **пр_агинг_грануларити**.</span><span class="sxs-lookup"><span data-stu-id="19b2e-128">The length of time that an item remains in a folder before the item is archived is determined by two properties, [PR_AGING_PERIOD](pidtagagingperiod-canonical-property.md) and **PR_AGING_GRANULARITY**.</span></span> <span data-ttu-id="19b2e-129">**Пр_агинг_период** представляет количество единиц времени, в течение которых элемент остается в папке, прежде чем он будет архивирован.</span><span class="sxs-lookup"><span data-stu-id="19b2e-129">**PR_AGING_PERIOD** represents the number of time units that the item remains in the folder before it is archived.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="19b2e-130">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="19b2e-130">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="19b2e-131">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="19b2e-131">Protocol specifications</span></span>

<span data-ttu-id="19b2e-132">[[MS — ОКСПРОПС]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="19b2e-132">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="19b2e-133">Содержит ссылки на соответствующие спецификации протоколов Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="19b2e-133">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="19b2e-134">[[MS — ОКСКФКСИКС]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="19b2e-134">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="19b2e-135">Определяет основные структуры данных, используемые в удаленных операциях.</span><span class="sxs-lookup"><span data-stu-id="19b2e-135">Defines the basic data structures that are used in remote operations.</span></span>
    
<span data-ttu-id="19b2e-136">[[MS — ОКСОМСГ]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="19b2e-136">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="19b2e-137">Задает свойства и операции, допустимые для объектов сообщений электронной почты.</span><span class="sxs-lookup"><span data-stu-id="19b2e-137">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="19b2e-138">Файлы заГоловков</span><span class="sxs-lookup"><span data-stu-id="19b2e-138">Header files</span></span>

<span data-ttu-id="19b2e-139">MAPIDEFS. h</span><span class="sxs-lookup"><span data-stu-id="19b2e-139">Mapidefs.h</span></span>
  
> <span data-ttu-id="19b2e-140">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="19b2e-140">Provides data type definitions.</span></span>
    
<span data-ttu-id="19b2e-141">Мапитагс. h</span><span class="sxs-lookup"><span data-stu-id="19b2e-141">Mapitags.h</span></span>
  
> <span data-ttu-id="19b2e-142">Содержит определения свойств, перечисленных как альтернативные имена.</span><span class="sxs-lookup"><span data-stu-id="19b2e-142">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="19b2e-143">См. также</span><span class="sxs-lookup"><span data-stu-id="19b2e-143">See also</span></span>



[<span data-ttu-id="19b2e-144">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="19b2e-144">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="19b2e-145">Каноническое свойство MAPI</span><span class="sxs-lookup"><span data-stu-id="19b2e-145">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="19b2e-146">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="19b2e-146">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="19b2e-147">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="19b2e-147">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)


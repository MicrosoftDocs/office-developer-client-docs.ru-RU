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
# <a name="pidtagaginggranularity-canonical-property"></a><span data-ttu-id="42bae-103">Каноническое свойство PidTagAgingGranularity</span><span class="sxs-lookup"><span data-stu-id="42bae-103">PidTagAgingGranularity Canonical Property</span></span>

  
  
<span data-ttu-id="42bae-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="42bae-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="42bae-105">Представляет единицу времени, используемую для определения продолжительности времени, в течение которое элемент остается в папке, прежде чем элемент будет архивироваться.</span><span class="sxs-lookup"><span data-stu-id="42bae-105">Represents the unit of time that is used in determining the length of time an item remains in a folder before the item is archived.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="42bae-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="42bae-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="42bae-107">PR_AGING_GRANULARITY</span><span class="sxs-lookup"><span data-stu-id="42bae-107">PR_AGING_GRANULARITY</span></span>  <br/> |
|<span data-ttu-id="42bae-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="42bae-108">Identifier:</span></span>  <br/> |<span data-ttu-id="42bae-109">0x36EE</span><span class="sxs-lookup"><span data-stu-id="42bae-109">0x36EE</span></span>  <br/> |
|<span data-ttu-id="42bae-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="42bae-110">Data type:</span></span>  <br/> |<span data-ttu-id="42bae-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="42bae-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="42bae-112">Область:</span><span class="sxs-lookup"><span data-stu-id="42bae-112">Area:</span></span>  <br/> |<span data-ttu-id="42bae-113">Разное</span><span class="sxs-lookup"><span data-stu-id="42bae-113">Miscellaneous</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="42bae-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="42bae-114">Remarks</span></span>

<span data-ttu-id="42bae-115">Возможные значения **для** PR_AGING_GRANULARITY могут быть одним из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="42bae-115">The possible values for **PR_AGING_GRANULARITY** can be one of the following.</span></span> 
  
|<span data-ttu-id="42bae-116">**Name**</span><span class="sxs-lookup"><span data-stu-id="42bae-116">**Name**</span></span>|<span data-ttu-id="42bae-117">**Value**</span><span class="sxs-lookup"><span data-stu-id="42bae-117">**Value**</span></span>|<span data-ttu-id="42bae-118">**Описание**</span><span class="sxs-lookup"><span data-stu-id="42bae-118">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="42bae-119">**AG_MONTHS**</span><span class="sxs-lookup"><span data-stu-id="42bae-119">**AG_MONTHS**</span></span> <br/> |<span data-ttu-id="42bae-120">0</span><span class="sxs-lookup"><span data-stu-id="42bae-120">0</span></span>  <br/> |<span data-ttu-id="42bae-121">**PR_AGING_PERIOD** определяется в течение нескольких месяцев.</span><span class="sxs-lookup"><span data-stu-id="42bae-121">**PR_AGING_PERIOD** is defined in number of months.</span></span>  <br/> |
|<span data-ttu-id="42bae-122">**AG_WEEKS**</span><span class="sxs-lookup"><span data-stu-id="42bae-122">**AG_WEEKS**</span></span> <br/> |<span data-ttu-id="42bae-123">1 </span><span class="sxs-lookup"><span data-stu-id="42bae-123">1</span></span>  <br/> |<span data-ttu-id="42bae-124">**PR_AGING_PERIOD** определяется в течение нескольких недель.</span><span class="sxs-lookup"><span data-stu-id="42bae-124">**PR_AGING_PERIOD** is defined in number of weeks.</span></span>  <br/> |
|<span data-ttu-id="42bae-125">**AG_DAYS**</span><span class="sxs-lookup"><span data-stu-id="42bae-125">**AG_DAYS**</span></span> <br/> |<span data-ttu-id="42bae-126">2 </span><span class="sxs-lookup"><span data-stu-id="42bae-126">2</span></span>  <br/> |<span data-ttu-id="42bae-127">**PR_AGING_PERIOD** определяется в днях.</span><span class="sxs-lookup"><span data-stu-id="42bae-127">**PR_AGING_PERIOD** is defined in number of days.</span></span>  <br/> |
   
<span data-ttu-id="42bae-128">Период времени, в течение который элемент остается в папке до архива [элемента,](pidtagagingperiod-canonical-property.md) определяется двумя свойствами: PR_AGING_PERIOD и **PR_AGING_GRANULARITY.**</span><span class="sxs-lookup"><span data-stu-id="42bae-128">The length of time that an item remains in a folder before the item is archived is determined by two properties, [PR_AGING_PERIOD](pidtagagingperiod-canonical-property.md) and **PR_AGING_GRANULARITY**.</span></span> <span data-ttu-id="42bae-129">**PR_AGING_PERIOD** представляет количество единиц времени, в которые элемент остается в папке, прежде чем он будет архивироваться.</span><span class="sxs-lookup"><span data-stu-id="42bae-129">**PR_AGING_PERIOD** represents the number of time units that the item remains in the folder before it is archived.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="42bae-130">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="42bae-130">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="42bae-131">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="42bae-131">Protocol specifications</span></span>

<span data-ttu-id="42bae-132">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="42bae-132">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="42bae-133">Содержит ссылки на связанные Exchange Server протоколы.</span><span class="sxs-lookup"><span data-stu-id="42bae-133">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="42bae-134">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="42bae-134">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="42bae-135">Определяет основные структуры данных, используемые в удаленных операциях.</span><span class="sxs-lookup"><span data-stu-id="42bae-135">Defines the basic data structures that are used in remote operations.</span></span>
    
<span data-ttu-id="42bae-136">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="42bae-136">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="42bae-137">Указывает свойства и операции, которые разрешены для объектов сообщений электронной почты.</span><span class="sxs-lookup"><span data-stu-id="42bae-137">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="42bae-138">Файлы заголовок</span><span class="sxs-lookup"><span data-stu-id="42bae-138">Header files</span></span>

<span data-ttu-id="42bae-139">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="42bae-139">Mapidefs.h</span></span>
  
> <span data-ttu-id="42bae-140">Предоставляет определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="42bae-140">Provides data type definitions.</span></span>
    
<span data-ttu-id="42bae-141">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="42bae-141">Mapitags.h</span></span>
  
> <span data-ttu-id="42bae-142">Содержит определения свойств, перечисленных в качестве альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="42bae-142">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="42bae-143">См. также</span><span class="sxs-lookup"><span data-stu-id="42bae-143">See also</span></span>



[<span data-ttu-id="42bae-144">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="42bae-144">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="42bae-145">Канонические свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="42bae-145">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="42bae-146">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="42bae-146">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="42bae-147">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="42bae-147">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)


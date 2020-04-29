---
title: Каноническое свойство PidTagAgingPeriod
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagAgingPeriod
api_type:
- HeaderDef
ms.assetid: 762020d1-4bc8-d60d-0f66-3929aae24bfb
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: d42b58bf4fd445f34064b179c873c8bc15b11b3f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360118"
---
# <a name="pidtagagingperiod-canonical-property"></a><span data-ttu-id="14513-103">Каноническое свойство PidTagAgingPeriod</span><span class="sxs-lookup"><span data-stu-id="14513-103">PidTagAgingPeriod Canonical Property</span></span>

  
  
<span data-ttu-id="14513-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="14513-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="14513-105">Представляет количество единиц времени, которые используются для определения времени, в течение которого элемент остается в папке, прежде чем элемент будет архивирован.</span><span class="sxs-lookup"><span data-stu-id="14513-105">Represents the number of time units that are used to determine the length of time that an item remains in a folder before the item is archived.</span></span>
  
## 

|||
|:-----|:-----|
|<span data-ttu-id="14513-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="14513-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="14513-107">PR_AGING_PERIOD</span><span class="sxs-lookup"><span data-stu-id="14513-107">PR_AGING_PERIOD</span></span>  <br/> |
|<span data-ttu-id="14513-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="14513-108">Identifier:</span></span>  <br/> |<span data-ttu-id="14513-109">0x36EC</span><span class="sxs-lookup"><span data-stu-id="14513-109">0x36EC</span></span>  <br/> |
|<span data-ttu-id="14513-110">Тип свойства:</span><span class="sxs-lookup"><span data-stu-id="14513-110">Property type:</span></span>  <br/> |<span data-ttu-id="14513-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="14513-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="14513-112">Область:</span><span class="sxs-lookup"><span data-stu-id="14513-112">Area:</span></span>  <br/> |<span data-ttu-id="14513-113">Разное</span><span class="sxs-lookup"><span data-stu-id="14513-113">Miscellaneous</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="14513-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="14513-114">Remarks</span></span>

<span data-ttu-id="14513-115">Время, в течение которого элемент остается в папке, прежде чем его архивировать, будут определяться двумя свойствами, **PR_AGING_PERIOD** и **[PR_AGING_GRANULARITY](pidtagaginggranularity-canonical-property.md)**.</span><span class="sxs-lookup"><span data-stu-id="14513-115">The length of time that an item remains in a folder before the item is archived is determined by two properties, **PR_AGING_PERIOD** and **[PR_AGING_GRANULARITY](pidtagaginggranularity-canonical-property.md)**.</span></span> <span data-ttu-id="14513-116">**PR_AGING_GRANULARITY** представляет единицу времени, в которой выражается **PR_AGING_PERIOD** при определении продолжительности времени.</span><span class="sxs-lookup"><span data-stu-id="14513-116">**PR_AGING_GRANULARITY** represents the time unit in which **PR_AGING_PERIOD** is expressed, when determining this length of time.</span></span> 
  
<span data-ttu-id="14513-117">Возможные значения для **PR_AGING_GRANULARITY** могут быть одним из следующих.</span><span class="sxs-lookup"><span data-stu-id="14513-117">The possible values for **PR_AGING_GRANULARITY** can be one of the following.</span></span> 
  
****

|<span data-ttu-id="14513-118">**Название**</span><span class="sxs-lookup"><span data-stu-id="14513-118">**Name**</span></span>|<span data-ttu-id="14513-119">**Описание**</span><span class="sxs-lookup"><span data-stu-id="14513-119">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="14513-120">**AG_MONTHS**</span><span class="sxs-lookup"><span data-stu-id="14513-120">**AG_MONTHS**</span></span> <br/> |<span data-ttu-id="14513-121">**PR_AGING_PERIOD** задается в виде числа месяцев.</span><span class="sxs-lookup"><span data-stu-id="14513-121">**PR_AGING_PERIOD** is defined in number of months.</span></span>  <br/> |
|<span data-ttu-id="14513-122">**AG_WEEKS**</span><span class="sxs-lookup"><span data-stu-id="14513-122">**AG_WEEKS**</span></span> <br/> |<span data-ttu-id="14513-123">**PR_AGING_PERIOD** определяется в течение нескольких недель.</span><span class="sxs-lookup"><span data-stu-id="14513-123">**PR_AGING_PERIOD** is defined in number of weeks.</span></span>  <br/> |
|<span data-ttu-id="14513-124">**AG_DAYS**</span><span class="sxs-lookup"><span data-stu-id="14513-124">**AG_DAYS**</span></span> <br/> |<span data-ttu-id="14513-125">**PR_AGING_PERIOD** определено в днях.</span><span class="sxs-lookup"><span data-stu-id="14513-125">**PR_AGING_PERIOD** is defined in number of days.</span></span>  <br/> |
   
<span data-ttu-id="14513-126">Например, если папка архивирует элемент только после того, как она находится в папке за две недели, **PR_AGING_GRANULARITY** **AG_WEEKS** , а **PR_AGING_PERIOD** — 2.</span><span class="sxs-lookup"><span data-stu-id="14513-126">For example, if a folder archives an item only after the item has been in the folder for two weeks, then **PR_AGING_GRANULARITY** is **AG_WEEKS** and **PR_AGING_PERIOD** is 2.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="14513-127">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="14513-127">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="14513-128">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="14513-128">Protocol specifications</span></span>

<span data-ttu-id="14513-129">[[MS — ОКСПРОПС]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="14513-129">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="14513-130">Задает определения свойств.</span><span class="sxs-lookup"><span data-stu-id="14513-130">Provides property set definitions.</span></span>
    
<span data-ttu-id="14513-131">[[MS — ОКСКФКСИКС]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="14513-131">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="14513-132">Определяет основные структуры данных, используемые в удаленных операциях.</span><span class="sxs-lookup"><span data-stu-id="14513-132">Defines the basic data structures that are used in remote operations.</span></span>
    
<span data-ttu-id="14513-133">[[MS — ОКСОМСГ]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="14513-133">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="14513-134">Задает свойства и операции, разрешенные для объектов сообщений электронной почты.</span><span class="sxs-lookup"><span data-stu-id="14513-134">Specifies the properties and operations that are permitted for email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="14513-135">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="14513-135">Header files</span></span>

<span data-ttu-id="14513-136">MAPIDEFS. h</span><span class="sxs-lookup"><span data-stu-id="14513-136">Mapidefs.h</span></span>
  
> <span data-ttu-id="14513-137">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="14513-137">Provides data type definitions.</span></span>
    
<span data-ttu-id="14513-138">Мапитагс. h</span><span class="sxs-lookup"><span data-stu-id="14513-138">Mapitags.h</span></span>
  
> <span data-ttu-id="14513-139">Содержит определения свойств, перечисленных как альтернативные имена.</span><span class="sxs-lookup"><span data-stu-id="14513-139">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="14513-140">См. также</span><span class="sxs-lookup"><span data-stu-id="14513-140">See also</span></span>



[<span data-ttu-id="14513-141">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="14513-141">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="14513-142">Каноническое свойство MAPI</span><span class="sxs-lookup"><span data-stu-id="14513-142">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="14513-143">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="14513-143">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="14513-144">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="14513-144">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)


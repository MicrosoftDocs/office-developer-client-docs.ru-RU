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
ms.openlocfilehash: caaa01982ff9e66fe7e17df4eaf37dcd25281d4e
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22569556"
---
# <a name="pidtagagingperiod-canonical-property"></a><span data-ttu-id="1cd8c-103">Каноническое свойство PidTagAgingPeriod</span><span class="sxs-lookup"><span data-stu-id="1cd8c-103">PidTagAgingPeriod Canonical Property</span></span>

  
  
<span data-ttu-id="1cd8c-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1cd8c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1cd8c-105">Представляет номер единицы времени, которые используются для определения продолжительность времени, элемент остается в папке для архивации элемента.</span><span class="sxs-lookup"><span data-stu-id="1cd8c-105">Represents the number of time units that are used to determine the length of time that an item remains in a folder before the item is archived.</span></span>
  
## 

|||
|:-----|:-----|
|<span data-ttu-id="1cd8c-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="1cd8c-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="1cd8c-107">PR_AGING_PERIOD</span><span class="sxs-lookup"><span data-stu-id="1cd8c-107">PR_AGING_PERIOD</span></span>  <br/> |
|<span data-ttu-id="1cd8c-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="1cd8c-108">Identifier:</span></span>  <br/> |<span data-ttu-id="1cd8c-109">0x36EC</span><span class="sxs-lookup"><span data-stu-id="1cd8c-109">0x36EC</span></span>  <br/> |
|<span data-ttu-id="1cd8c-110">Тип свойства:</span><span class="sxs-lookup"><span data-stu-id="1cd8c-110">Property type:</span></span>  <br/> |<span data-ttu-id="1cd8c-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="1cd8c-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="1cd8c-112">Область:</span><span class="sxs-lookup"><span data-stu-id="1cd8c-112">Area:</span></span>  <br/> |<span data-ttu-id="1cd8c-113">Разное</span><span class="sxs-lookup"><span data-stu-id="1cd8c-113">Miscellaneous</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="1cd8c-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="1cd8c-114">Remarks</span></span>

<span data-ttu-id="1cd8c-115">Продолжительность времени, элемент остается в папке для архивации элемента, определяется два свойства **PR_AGING_PERIOD** и **[PR_AGING_GRANULARITY](pidtagaginggranularity-canonical-property.md)**.</span><span class="sxs-lookup"><span data-stu-id="1cd8c-115">The length of time that an item remains in a folder before the item is archived is determined by two properties, **PR_AGING_PERIOD** and **[PR_AGING_GRANULARITY](pidtagaginggranularity-canonical-property.md)**.</span></span> <span data-ttu-id="1cd8c-116">**PR_AGING_GRANULARITY** представляет единицы времени, в которой выражается **PR_AGING_PERIOD** , при определении этот промежуток времени.</span><span class="sxs-lookup"><span data-stu-id="1cd8c-116">**PR_AGING_GRANULARITY** represents the time unit in which **PR_AGING_PERIOD** is expressed, when determining this length of time.</span></span> 
  
<span data-ttu-id="1cd8c-117">Возможные значения для **PR_AGING_GRANULARITY** может иметь одно из следующих.</span><span class="sxs-lookup"><span data-stu-id="1cd8c-117">The possible values for **PR_AGING_GRANULARITY** can be one of the following.</span></span> 
  
****

|<span data-ttu-id="1cd8c-118">**Имя**</span><span class="sxs-lookup"><span data-stu-id="1cd8c-118">**Name**</span></span>|<span data-ttu-id="1cd8c-119">**Описание**</span><span class="sxs-lookup"><span data-stu-id="1cd8c-119">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="1cd8c-120">**AG_MONTHS**</span><span class="sxs-lookup"><span data-stu-id="1cd8c-120">**AG_MONTHS**</span></span> <br/> |<span data-ttu-id="1cd8c-121">**PR_AGING_PERIOD** определен в число месяцев.</span><span class="sxs-lookup"><span data-stu-id="1cd8c-121">**PR_AGING_PERIOD** is defined in number of months.</span></span>  <br/> |
|<span data-ttu-id="1cd8c-122">**AG_WEEKS**</span><span class="sxs-lookup"><span data-stu-id="1cd8c-122">**AG_WEEKS**</span></span> <br/> |<span data-ttu-id="1cd8c-123">**PR_AGING_PERIOD** определен в число недель.</span><span class="sxs-lookup"><span data-stu-id="1cd8c-123">**PR_AGING_PERIOD** is defined in number of weeks.</span></span>  <br/> |
|<span data-ttu-id="1cd8c-124">**AG_DAYS**</span><span class="sxs-lookup"><span data-stu-id="1cd8c-124">**AG_DAYS**</span></span> <br/> |<span data-ttu-id="1cd8c-125">**PR_AGING_PERIOD** определен в днях.</span><span class="sxs-lookup"><span data-stu-id="1cd8c-125">**PR_AGING_PERIOD** is defined in number of days.</span></span>  <br/> |
   
<span data-ttu-id="1cd8c-126">Например если архивы папки, элемента только после элемента в папке, в течение двух недель, а затем **PR_AGING_GRANULARITY** — **AG_WEEKS** и **PR_AGING_PERIOD** : 2.</span><span class="sxs-lookup"><span data-stu-id="1cd8c-126">For example, if a folder archives an item only after the item has been in the folder for two weeks, then **PR_AGING_GRANULARITY** is **AG_WEEKS** and **PR_AGING_PERIOD** is 2.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="1cd8c-127">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="1cd8c-127">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="1cd8c-128">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="1cd8c-128">Protocol specifications</span></span>

<span data-ttu-id="1cd8c-129">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="1cd8c-129">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="1cd8c-130">Содержит определения набора свойств.</span><span class="sxs-lookup"><span data-stu-id="1cd8c-130">Provides property set definitions.</span></span>
    
<span data-ttu-id="1cd8c-131">[[MS-OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="1cd8c-131">[[MS-OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="1cd8c-132">Определяет структуры основных данных, которые используются для удаленных операций.</span><span class="sxs-lookup"><span data-stu-id="1cd8c-132">Defines the basic data structures that are used in remote operations.</span></span>
    
<span data-ttu-id="1cd8c-133">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="1cd8c-133">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="1cd8c-134">Задает свойства и операции, которые разрешены для объектов сообщения электронной почты.</span><span class="sxs-lookup"><span data-stu-id="1cd8c-134">Specifies the properties and operations that are permitted for email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="1cd8c-135">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="1cd8c-135">Header files</span></span>

<span data-ttu-id="1cd8c-136">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="1cd8c-136">Mapidefs.h</span></span>
  
> <span data-ttu-id="1cd8c-137">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="1cd8c-137">Provides data type definitions.</span></span>
    
<span data-ttu-id="1cd8c-138">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="1cd8c-138">Mapitags.h</span></span>
  
> <span data-ttu-id="1cd8c-139">Содержит определения свойства в списке альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="1cd8c-139">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="1cd8c-140">См. также</span><span class="sxs-lookup"><span data-stu-id="1cd8c-140">See also</span></span>



[<span data-ttu-id="1cd8c-141">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="1cd8c-141">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="1cd8c-142">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="1cd8c-142">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="1cd8c-143">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="1cd8c-143">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="1cd8c-144">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="1cd8c-144">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)


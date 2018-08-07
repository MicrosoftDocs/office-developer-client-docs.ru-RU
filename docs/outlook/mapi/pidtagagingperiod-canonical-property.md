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
ms.openlocfilehash: 1fd1b06bbaa10c2d7c71ee4c161fd6a980da1865
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19810813"
---
# <a name="pidtagagingperiod-canonical-property"></a><span data-ttu-id="1f2c3-103">Каноническое свойство PidTagAgingPeriod</span><span class="sxs-lookup"><span data-stu-id="1f2c3-103">PidTagAgingPeriod Canonical Property</span></span>

  
  
<span data-ttu-id="1f2c3-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="1f2c3-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="1f2c3-105">Представляет номер единицы времени, которые используются для определения продолжительность времени, элемент остается в папке для архивации элемента.</span><span class="sxs-lookup"><span data-stu-id="1f2c3-105">Represents the number of time units that are used to determine the length of time that an item remains in a folder before the item is archived.</span></span>
  
## 

|||
|:-----|:-----|
|<span data-ttu-id="1f2c3-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="1f2c3-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="1f2c3-107">PR_AGING_PERIOD</span><span class="sxs-lookup"><span data-stu-id="1f2c3-107">PR_AGING_PERIOD</span></span>  <br/> |
|<span data-ttu-id="1f2c3-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="1f2c3-108">Identifier:</span></span>  <br/> |<span data-ttu-id="1f2c3-109">0x36EC</span><span class="sxs-lookup"><span data-stu-id="1f2c3-109">0x36EC</span></span>  <br/> |
|<span data-ttu-id="1f2c3-110">Тип свойства:</span><span class="sxs-lookup"><span data-stu-id="1f2c3-110">Property type:</span></span>  <br/> |<span data-ttu-id="1f2c3-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="1f2c3-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="1f2c3-112">Область:</span><span class="sxs-lookup"><span data-stu-id="1f2c3-112">Area:</span></span>  <br/> |<span data-ttu-id="1f2c3-113">Разное</span><span class="sxs-lookup"><span data-stu-id="1f2c3-113">Miscellaneous</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="1f2c3-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="1f2c3-114">Remarks</span></span>

<span data-ttu-id="1f2c3-115">Продолжительность времени, элемент остается в папке для архивации элемента, определяется два свойства **PR_AGING_PERIOD** и **[PR_AGING_GRANULARITY](pidtagaginggranularity-canonical-property.md)**.</span><span class="sxs-lookup"><span data-stu-id="1f2c3-115">The length of time that an item remains in a folder before the item is archived is determined by two properties, **PR_AGING_PERIOD** and **[PR_AGING_GRANULARITY](pidtagaginggranularity-canonical-property.md)**.</span></span> <span data-ttu-id="1f2c3-116">**PR_AGING_GRANULARITY** представляет единицы времени, в которой выражается **PR_AGING_PERIOD** , при определении этот промежуток времени.</span><span class="sxs-lookup"><span data-stu-id="1f2c3-116">**PR_AGING_GRANULARITY** represents the time unit in which **PR_AGING_PERIOD** is expressed, when determining this length of time.</span></span> 
  
<span data-ttu-id="1f2c3-117">Возможные значения для **PR_AGING_GRANULARITY** может иметь одно из следующих.</span><span class="sxs-lookup"><span data-stu-id="1f2c3-117">The possible values for **PR_AGING_GRANULARITY** can be one of the following.</span></span> 
  
****

|<span data-ttu-id="1f2c3-118">**Имя**</span><span class="sxs-lookup"><span data-stu-id="1f2c3-118">**Name**</span></span>|<span data-ttu-id="1f2c3-119">**Описание**</span><span class="sxs-lookup"><span data-stu-id="1f2c3-119">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="1f2c3-120">**AG_MONTHS**</span><span class="sxs-lookup"><span data-stu-id="1f2c3-120">**AG_MONTHS**</span></span> <br/> |<span data-ttu-id="1f2c3-121">**PR_AGING_PERIOD** определен в число месяцев.</span><span class="sxs-lookup"><span data-stu-id="1f2c3-121">**PR_AGING_PERIOD** is defined in number of months.</span></span>  <br/> |
|<span data-ttu-id="1f2c3-122">**AG_WEEKS**</span><span class="sxs-lookup"><span data-stu-id="1f2c3-122">**AG_WEEKS**</span></span> <br/> |<span data-ttu-id="1f2c3-123">**PR_AGING_PERIOD** определен в число недель.</span><span class="sxs-lookup"><span data-stu-id="1f2c3-123">**PR_AGING_PERIOD** is defined in number of weeks.</span></span>  <br/> |
|<span data-ttu-id="1f2c3-124">**AG_DAYS**</span><span class="sxs-lookup"><span data-stu-id="1f2c3-124">**AG_DAYS**</span></span> <br/> |<span data-ttu-id="1f2c3-125">**PR_AGING_PERIOD** определен в днях.</span><span class="sxs-lookup"><span data-stu-id="1f2c3-125">**PR_AGING_PERIOD** is defined in number of days.</span></span>  <br/> |
   
<span data-ttu-id="1f2c3-126">Например если архивы папки, элемента только после элемента в папке, в течение двух недель, а затем **PR_AGING_GRANULARITY** — **AG_WEEKS** и **PR_AGING_PERIOD** : 2.</span><span class="sxs-lookup"><span data-stu-id="1f2c3-126">For example, if a folder archives an item only after the item has been in the folder for two weeks, then **PR_AGING_GRANULARITY** is **AG_WEEKS** and **PR_AGING_PERIOD** is 2.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="1f2c3-127">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="1f2c3-127">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="1f2c3-128">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="1f2c3-128">Protocol specifications</span></span>

<span data-ttu-id="1f2c3-129">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="1f2c3-129">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="1f2c3-130">Содержит определения набора свойств.</span><span class="sxs-lookup"><span data-stu-id="1f2c3-130">Provides property set definitions.</span></span>
    
<span data-ttu-id="1f2c3-131">[[MS-OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="1f2c3-131">[[MS-OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="1f2c3-132">Определяет структуры основных данных, которые используются для удаленных операций.</span><span class="sxs-lookup"><span data-stu-id="1f2c3-132">Defines the basic data structures that are used in remote operations.</span></span>
    
<span data-ttu-id="1f2c3-133">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="1f2c3-133">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="1f2c3-134">Задает свойства и операции, которые разрешены для объектов сообщения электронной почты.</span><span class="sxs-lookup"><span data-stu-id="1f2c3-134">Specifies the properties and operations that are permitted for email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="1f2c3-135">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="1f2c3-135">Header files</span></span>

<span data-ttu-id="1f2c3-136">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="1f2c3-136">Mapidefs.h</span></span>
  
> <span data-ttu-id="1f2c3-137">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="1f2c3-137">Provides data type definitions.</span></span>
    
<span data-ttu-id="1f2c3-138">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="1f2c3-138">Mapitags.h</span></span>
  
> <span data-ttu-id="1f2c3-139">Содержит определения свойства в списке альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="1f2c3-139">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="1f2c3-140">См. также</span><span class="sxs-lookup"><span data-stu-id="1f2c3-140">See also</span></span>



[<span data-ttu-id="1f2c3-141">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="1f2c3-141">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="1f2c3-142">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="1f2c3-142">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="1f2c3-143">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="1f2c3-143">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="1f2c3-144">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="1f2c3-144">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)


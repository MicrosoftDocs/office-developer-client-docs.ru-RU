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
# <a name="pidtagagingperiod-canonical-property"></a><span data-ttu-id="d9b95-103">Каноническое свойство PidTagAgingPeriod</span><span class="sxs-lookup"><span data-stu-id="d9b95-103">PidTagAgingPeriod Canonical Property</span></span>

  
  
<span data-ttu-id="d9b95-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d9b95-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d9b95-105">Представляет количество единиц времени, которые используются для определения времени, в течение которого элемент остается в папке, прежде чем элемент будет архивирован.</span><span class="sxs-lookup"><span data-stu-id="d9b95-105">Represents the number of time units that are used to determine the length of time that an item remains in a folder before the item is archived.</span></span>
  
## 

|||
|:-----|:-----|
|<span data-ttu-id="d9b95-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="d9b95-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="d9b95-107">ПР_АГИНГ_ПЕРИОД</span><span class="sxs-lookup"><span data-stu-id="d9b95-107">PR_AGING_PERIOD</span></span>  <br/> |
|<span data-ttu-id="d9b95-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="d9b95-108">Identifier:</span></span>  <br/> |<span data-ttu-id="d9b95-109">0x36EC</span><span class="sxs-lookup"><span data-stu-id="d9b95-109">0x36EC</span></span>  <br/> |
|<span data-ttu-id="d9b95-110">Тип свойства:</span><span class="sxs-lookup"><span data-stu-id="d9b95-110">Property type:</span></span>  <br/> |<span data-ttu-id="d9b95-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="d9b95-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="d9b95-112">Область:</span><span class="sxs-lookup"><span data-stu-id="d9b95-112">Area:</span></span>  <br/> |<span data-ttu-id="d9b95-113">Разное</span><span class="sxs-lookup"><span data-stu-id="d9b95-113">Miscellaneous</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d9b95-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="d9b95-114">Remarks</span></span>

<span data-ttu-id="d9b95-115">Период времени, в течение которого элемент остается в папке до архивации элемента, определяется двумя свойствами, **пр_агинг_период** и **[пр_агинг_грануларити](pidtagaginggranularity-canonical-property.md)**.</span><span class="sxs-lookup"><span data-stu-id="d9b95-115">The length of time that an item remains in a folder before the item is archived is determined by two properties, **PR_AGING_PERIOD** and **[PR_AGING_GRANULARITY](pidtagaginggranularity-canonical-property.md)**.</span></span> <span data-ttu-id="d9b95-116">**Пр_агинг_грануларити** представляет единицу времени, в которой выражается **пр_агинг_период** при определении продолжительности времени.</span><span class="sxs-lookup"><span data-stu-id="d9b95-116">**PR_AGING_GRANULARITY** represents the time unit in which **PR_AGING_PERIOD** is expressed, when determining this length of time.</span></span> 
  
<span data-ttu-id="d9b95-117">Возможные значения для параметра **пр_агинг_грануларити** могут быть одним из следующих.</span><span class="sxs-lookup"><span data-stu-id="d9b95-117">The possible values for **PR_AGING_GRANULARITY** can be one of the following.</span></span> 
  
****

|<span data-ttu-id="d9b95-118">**Имя**</span><span class="sxs-lookup"><span data-stu-id="d9b95-118">**Name**</span></span>|<span data-ttu-id="d9b95-119">**Описание**</span><span class="sxs-lookup"><span data-stu-id="d9b95-119">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="d9b95-120">**АГ_МОНСС**</span><span class="sxs-lookup"><span data-stu-id="d9b95-120">**AG_MONTHS**</span></span> <br/> |<span data-ttu-id="d9b95-121">**Пр_агинг_период** определяется в виде числа месяцев.</span><span class="sxs-lookup"><span data-stu-id="d9b95-121">**PR_AGING_PERIOD** is defined in number of months.</span></span>  <br/> |
|<span data-ttu-id="d9b95-122">**АГ_ВИКС**</span><span class="sxs-lookup"><span data-stu-id="d9b95-122">**AG_WEEKS**</span></span> <br/> |<span data-ttu-id="d9b95-123">**Пр_агинг_период** определяется в виде количества недель.</span><span class="sxs-lookup"><span data-stu-id="d9b95-123">**PR_AGING_PERIOD** is defined in number of weeks.</span></span>  <br/> |
|<span data-ttu-id="d9b95-124">**АГ_ДАЙС**</span><span class="sxs-lookup"><span data-stu-id="d9b95-124">**AG_DAYS**</span></span> <br/> |<span data-ttu-id="d9b95-125">**Пр_агинг_период** определяется в виде количества дней.</span><span class="sxs-lookup"><span data-stu-id="d9b95-125">**PR_AGING_PERIOD** is defined in number of days.</span></span>  <br/> |
   
<span data-ttu-id="d9b95-126">Например, если папка заархивировать элемент только после того, как он находился в папке за две недели, то **пр_агинг_грануларити** — **Аг_викс** , а **пр_агинг_период** — 2.</span><span class="sxs-lookup"><span data-stu-id="d9b95-126">For example, if a folder archives an item only after the item has been in the folder for two weeks, then **PR_AGING_GRANULARITY** is **AG_WEEKS** and **PR_AGING_PERIOD** is 2.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="d9b95-127">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="d9b95-127">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="d9b95-128">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="d9b95-128">Protocol specifications</span></span>

<span data-ttu-id="d9b95-129">[[MS — ОКСПРОПС]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d9b95-129">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="d9b95-130">Задает определения свойств.</span><span class="sxs-lookup"><span data-stu-id="d9b95-130">Provides property set definitions.</span></span>
    
<span data-ttu-id="d9b95-131">[[MS — ОКСКФКСИКС]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d9b95-131">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="d9b95-132">Определяет основные структуры данных, используемые в удаленных операциях.</span><span class="sxs-lookup"><span data-stu-id="d9b95-132">Defines the basic data structures that are used in remote operations.</span></span>
    
<span data-ttu-id="d9b95-133">[[MS — ОКСОМСГ]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d9b95-133">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="d9b95-134">Задает свойства и операции, разрешенные для объектов сообщений электронной почты.</span><span class="sxs-lookup"><span data-stu-id="d9b95-134">Specifies the properties and operations that are permitted for email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="d9b95-135">Файлы заГоловков</span><span class="sxs-lookup"><span data-stu-id="d9b95-135">Header files</span></span>

<span data-ttu-id="d9b95-136">MAPIDEFS. h</span><span class="sxs-lookup"><span data-stu-id="d9b95-136">Mapidefs.h</span></span>
  
> <span data-ttu-id="d9b95-137">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="d9b95-137">Provides data type definitions.</span></span>
    
<span data-ttu-id="d9b95-138">Мапитагс. h</span><span class="sxs-lookup"><span data-stu-id="d9b95-138">Mapitags.h</span></span>
  
> <span data-ttu-id="d9b95-139">Содержит определения свойств, перечисленных как альтернативные имена.</span><span class="sxs-lookup"><span data-stu-id="d9b95-139">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="d9b95-140">См. также</span><span class="sxs-lookup"><span data-stu-id="d9b95-140">See also</span></span>



[<span data-ttu-id="d9b95-141">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="d9b95-141">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="d9b95-142">Каноническое свойство MAPI</span><span class="sxs-lookup"><span data-stu-id="d9b95-142">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="d9b95-143">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="d9b95-143">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="d9b95-144">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="d9b95-144">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)


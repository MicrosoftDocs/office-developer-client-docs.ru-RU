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
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25390438"
---
# <a name="pidtagaginggranularity-canonical-property"></a><span data-ttu-id="2ced9-103">Каноническое свойство PidTagAgingGranularity</span><span class="sxs-lookup"><span data-stu-id="2ced9-103">PidTagAgingGranularity Canonical Property</span></span>

  
  
<span data-ttu-id="2ced9-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2ced9-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2ced9-105">Представляет единицы времени, который используется при определении длина отображения элемента в папке перед заархивированы элемента.</span><span class="sxs-lookup"><span data-stu-id="2ced9-105">Represents the unit of time that is used in determining the length of time an item remains in a folder before the item is archived.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="2ced9-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="2ced9-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="2ced9-107">PR_AGING_GRANULARITY</span><span class="sxs-lookup"><span data-stu-id="2ced9-107">PR_AGING_GRANULARITY</span></span>  <br/> |
|<span data-ttu-id="2ced9-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="2ced9-108">Identifier:</span></span>  <br/> |<span data-ttu-id="2ced9-109">0x36EE</span><span class="sxs-lookup"><span data-stu-id="2ced9-109">0x36EE</span></span>  <br/> |
|<span data-ttu-id="2ced9-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="2ced9-110">Data type:</span></span>  <br/> |<span data-ttu-id="2ced9-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="2ced9-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="2ced9-112">Область:</span><span class="sxs-lookup"><span data-stu-id="2ced9-112">Area:</span></span>  <br/> |<span data-ttu-id="2ced9-113">Разное</span><span class="sxs-lookup"><span data-stu-id="2ced9-113">Miscellaneous</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="2ced9-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="2ced9-114">Remarks</span></span>

<span data-ttu-id="2ced9-115">Возможные значения для **PR_AGING_GRANULARITY** может иметь одно из следующих.</span><span class="sxs-lookup"><span data-stu-id="2ced9-115">The possible values for **PR_AGING_GRANULARITY** can be one of the following.</span></span> 
  
|<span data-ttu-id="2ced9-116">**Имя**</span><span class="sxs-lookup"><span data-stu-id="2ced9-116">**Name**</span></span>|<span data-ttu-id="2ced9-117">**Значение**</span><span class="sxs-lookup"><span data-stu-id="2ced9-117">**Value**</span></span>|<span data-ttu-id="2ced9-118">**Описание**</span><span class="sxs-lookup"><span data-stu-id="2ced9-118">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="2ced9-119">**AG_MONTHS**</span><span class="sxs-lookup"><span data-stu-id="2ced9-119">**AG_MONTHS**</span></span> <br/> |<span data-ttu-id="2ced9-120">0</span><span class="sxs-lookup"><span data-stu-id="2ced9-120">0</span></span>  <br/> |<span data-ttu-id="2ced9-121">**PR_AGING_PERIOD** определен в число месяцев.</span><span class="sxs-lookup"><span data-stu-id="2ced9-121">**PR_AGING_PERIOD** is defined in number of months.</span></span>  <br/> |
|<span data-ttu-id="2ced9-122">**AG_WEEKS**</span><span class="sxs-lookup"><span data-stu-id="2ced9-122">**AG_WEEKS**</span></span> <br/> |<span data-ttu-id="2ced9-123">1</span><span class="sxs-lookup"><span data-stu-id="2ced9-123">1</span></span>  <br/> |<span data-ttu-id="2ced9-124">**PR_AGING_PERIOD** определен в число недель.</span><span class="sxs-lookup"><span data-stu-id="2ced9-124">**PR_AGING_PERIOD** is defined in number of weeks.</span></span>  <br/> |
|<span data-ttu-id="2ced9-125">**AG_DAYS**</span><span class="sxs-lookup"><span data-stu-id="2ced9-125">**AG_DAYS**</span></span> <br/> |<span data-ttu-id="2ced9-126">2</span><span class="sxs-lookup"><span data-stu-id="2ced9-126">2</span></span>  <br/> |<span data-ttu-id="2ced9-127">**PR_AGING_PERIOD** определен в днях.</span><span class="sxs-lookup"><span data-stu-id="2ced9-127">**PR_AGING_PERIOD** is defined in number of days.</span></span>  <br/> |
   
<span data-ttu-id="2ced9-128">Продолжительность времени, элемент остается в папке для архивации элемента, определяется два свойства [PR_AGING_PERIOD](pidtagagingperiod-canonical-property.md) и **PR_AGING_GRANULARITY**.</span><span class="sxs-lookup"><span data-stu-id="2ced9-128">The length of time that an item remains in a folder before the item is archived is determined by two properties, [PR_AGING_PERIOD](pidtagagingperiod-canonical-property.md) and **PR_AGING_GRANULARITY**.</span></span> <span data-ttu-id="2ced9-129">**PR_AGING_PERIOD** представляет число единицы времени, которые элемент находится в папке перед архивации.</span><span class="sxs-lookup"><span data-stu-id="2ced9-129">**PR_AGING_PERIOD** represents the number of time units that the item remains in the folder before it is archived.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="2ced9-130">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="2ced9-130">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="2ced9-131">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="2ced9-131">Protocol specifications</span></span>

<span data-ttu-id="2ced9-132">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="2ced9-132">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="2ced9-133">Содержит ссылки на связанные спецификаций протокола Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="2ced9-133">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="2ced9-134">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="2ced9-134">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="2ced9-135">Определяет структуры основных данных, которые используются для удаленных операций.</span><span class="sxs-lookup"><span data-stu-id="2ced9-135">Defines the basic data structures that are used in remote operations.</span></span>
    
<span data-ttu-id="2ced9-136">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="2ced9-136">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="2ced9-137">Задает свойства и операции, допустимые для объектов сообщения электронной почты.</span><span class="sxs-lookup"><span data-stu-id="2ced9-137">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="2ced9-138">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="2ced9-138">Header files</span></span>

<span data-ttu-id="2ced9-139">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="2ced9-139">Mapidefs.h</span></span>
  
> <span data-ttu-id="2ced9-140">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="2ced9-140">Provides data type definitions.</span></span>
    
<span data-ttu-id="2ced9-141">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="2ced9-141">Mapitags.h</span></span>
  
> <span data-ttu-id="2ced9-142">Содержит определения свойства в списке альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="2ced9-142">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="2ced9-143">См. также</span><span class="sxs-lookup"><span data-stu-id="2ced9-143">See also</span></span>



[<span data-ttu-id="2ced9-144">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="2ced9-144">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="2ced9-145">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="2ced9-145">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="2ced9-146">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="2ced9-146">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="2ced9-147">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="2ced9-147">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)


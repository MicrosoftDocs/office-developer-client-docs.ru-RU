---
title: Каноническое свойство PidLidMeetingType
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidMeetingType
api_type:
- COM
ms.assetid: 290b290c-7836-4a7e-bf1a-8d0225a07e56
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: e61ce7798c9e41dbb707d0d5773b116f7cce02d6
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19810416"
---
# <a name="pidlidmeetingtype-canonical-property"></a><span data-ttu-id="8a3c6-103">Каноническое свойство PidLidMeetingType</span><span class="sxs-lookup"><span data-stu-id="8a3c6-103">PidLidMeetingType Canonical Property</span></span>

  
  
<span data-ttu-id="8a3c6-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="8a3c6-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="8a3c6-105">Указывает тип приглашения на собрание или приглашения обновления.</span><span class="sxs-lookup"><span data-stu-id="8a3c6-105">Indicates the type of meeting request or meeting update.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="8a3c6-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="8a3c6-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="8a3c6-107">dispidMeetingType</span><span class="sxs-lookup"><span data-stu-id="8a3c6-107">dispidMeetingType</span></span>  <br/> |
|<span data-ttu-id="8a3c6-108">Набор свойств:</span><span class="sxs-lookup"><span data-stu-id="8a3c6-108">Property set:</span></span>  <br/> |<span data-ttu-id="8a3c6-109">PSETID_Meeting</span><span class="sxs-lookup"><span data-stu-id="8a3c6-109">PSETID_Meeting</span></span>  <br/> |
|<span data-ttu-id="8a3c6-110">Длинный идентификатор (КРЫШКА):</span><span class="sxs-lookup"><span data-stu-id="8a3c6-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="8a3c6-111">0x00000026</span><span class="sxs-lookup"><span data-stu-id="8a3c6-111">0x00000026</span></span>  <br/> |
|<span data-ttu-id="8a3c6-112">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="8a3c6-112">Data type:</span></span>  <br/> |<span data-ttu-id="8a3c6-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="8a3c6-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="8a3c6-114">Область:</span><span class="sxs-lookup"><span data-stu-id="8a3c6-114">Area:</span></span>  <br/> |<span data-ttu-id="8a3c6-115">Meetings (собрания);</span><span class="sxs-lookup"><span data-stu-id="8a3c6-115">Meetings</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="8a3c6-116">Замечания</span><span class="sxs-lookup"><span data-stu-id="8a3c6-116">Remarks</span></span>

<span data-ttu-id="8a3c6-117">Значение этого свойства необходимо присвоить одно из следующих:</span><span class="sxs-lookup"><span data-stu-id="8a3c6-117">The value of this property must be set to one of the following:</span></span>
  
|<span data-ttu-id="8a3c6-118">**Свойство**</span><span class="sxs-lookup"><span data-stu-id="8a3c6-118">**Property**</span></span>|<span data-ttu-id="8a3c6-119">**Значение**</span><span class="sxs-lookup"><span data-stu-id="8a3c6-119">**Value**</span></span>|<span data-ttu-id="8a3c6-120">**Описание**</span><span class="sxs-lookup"><span data-stu-id="8a3c6-120">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="8a3c6-121">mtgEmpty</span><span class="sxs-lookup"><span data-stu-id="8a3c6-121">mtgEmpty</span></span>  <br/> |<span data-ttu-id="8a3c6-122">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8a3c6-122">0x00000000</span></span>  <br/> |<span data-ttu-id="8a3c6-123">Не определено.</span><span class="sxs-lookup"><span data-stu-id="8a3c6-123">Unspecified.</span></span>  <br/> |
|<span data-ttu-id="8a3c6-124">mtgRequest</span><span class="sxs-lookup"><span data-stu-id="8a3c6-124">mtgRequest</span></span>  <br/> |<span data-ttu-id="8a3c6-125">0x00000001</span><span class="sxs-lookup"><span data-stu-id="8a3c6-125">0x00000001</span></span>  <br/> |<span data-ttu-id="8a3c6-126">Начальное собрание.</span><span class="sxs-lookup"><span data-stu-id="8a3c6-126">Initial meeting request.</span></span>  <br/> |
|<span data-ttu-id="8a3c6-127">mtgFull</span><span class="sxs-lookup"><span data-stu-id="8a3c6-127">mtgFull</span></span>  <br/> |<span data-ttu-id="8a3c6-128">0x00010000</span><span class="sxs-lookup"><span data-stu-id="8a3c6-128">0x00010000</span></span>  <br/> |<span data-ttu-id="8a3c6-129">Полное обновление.</span><span class="sxs-lookup"><span data-stu-id="8a3c6-129">Full update.</span></span>  <br/> |
|<span data-ttu-id="8a3c6-130">mtgInfo</span><span class="sxs-lookup"><span data-stu-id="8a3c6-130">mtgInfo</span></span>  <br/> |<span data-ttu-id="8a3c6-131">0x00020000</span><span class="sxs-lookup"><span data-stu-id="8a3c6-131">0x00020000</span></span>  <br/> |<span data-ttu-id="8a3c6-132">Информационные обновления.</span><span class="sxs-lookup"><span data-stu-id="8a3c6-132">Informational update.</span></span>  <br/> |
|<span data-ttu-id="8a3c6-133">mtgOutOfDate</span><span class="sxs-lookup"><span data-stu-id="8a3c6-133">mtgOutOfDate</span></span>  <br/> |<span data-ttu-id="8a3c6-134">0x00080000</span><span class="sxs-lookup"><span data-stu-id="8a3c6-134">0x00080000</span></span>  <br/> |<span data-ttu-id="8a3c6-135">Файлы более новых приглашения на собрание или обновление собрания было получено после этой команды.</span><span class="sxs-lookup"><span data-stu-id="8a3c6-135">A newer meeting request or meeting update was received after this one.</span></span>  <br/> |
|<span data-ttu-id="8a3c6-136">mtgDelegatorCopy</span><span class="sxs-lookup"><span data-stu-id="8a3c6-136">mtgDelegatorCopy</span></span>  <br/> |<span data-ttu-id="8a3c6-137">0x00100000</span><span class="sxs-lookup"><span data-stu-id="8a3c6-137">0x00100000</span></span>  <br/> |<span data-ttu-id="8a3c6-138">Это значение на копии сотрудника при объекты собрании значками делегат.</span><span class="sxs-lookup"><span data-stu-id="8a3c6-138">This is set on the delegator's copy when a delegate handles meeting-related objects.</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="8a3c6-139">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="8a3c6-139">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="8a3c6-140">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="8a3c6-140">Protocol specifications</span></span>

<span data-ttu-id="8a3c6-141">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="8a3c6-141">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="8a3c6-142">Содержит определения набора свойств и ссылки на связанные спецификаций протокола Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="8a3c6-142">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="8a3c6-143">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="8a3c6-143">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="8a3c6-144">Задает свойства и операции для встречи, приглашения на собрание и ответы.</span><span class="sxs-lookup"><span data-stu-id="8a3c6-144">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="8a3c6-145">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="8a3c6-145">Header files</span></span>

<span data-ttu-id="8a3c6-146">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="8a3c6-146">Mapidefs.h</span></span>
  
> <span data-ttu-id="8a3c6-147">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="8a3c6-147">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="8a3c6-148">См. также</span><span class="sxs-lookup"><span data-stu-id="8a3c6-148">See also</span></span>



[<span data-ttu-id="8a3c6-149">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="8a3c6-149">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="8a3c6-150">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="8a3c6-150">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="8a3c6-151">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="8a3c6-151">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="8a3c6-152">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="8a3c6-152">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)


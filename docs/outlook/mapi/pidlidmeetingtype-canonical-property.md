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
ms.openlocfilehash: d2b00c67984d090274a17028ee74e46bee482e2b
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25399636"
---
# <a name="pidlidmeetingtype-canonical-property"></a><span data-ttu-id="8308f-103">Каноническое свойство PidLidMeetingType</span><span class="sxs-lookup"><span data-stu-id="8308f-103">PidLidMeetingType Canonical Property</span></span>

  
  
<span data-ttu-id="8308f-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8308f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8308f-105">Указывает тип приглашения на собрание или приглашения обновления.</span><span class="sxs-lookup"><span data-stu-id="8308f-105">Indicates the type of meeting request or meeting update.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="8308f-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="8308f-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="8308f-107">dispidMeetingType</span><span class="sxs-lookup"><span data-stu-id="8308f-107">dispidMeetingType</span></span>  <br/> |
|<span data-ttu-id="8308f-108">Набор свойств:</span><span class="sxs-lookup"><span data-stu-id="8308f-108">Property set:</span></span>  <br/> |<span data-ttu-id="8308f-109">PSETID_Meeting</span><span class="sxs-lookup"><span data-stu-id="8308f-109">PSETID_Meeting</span></span>  <br/> |
|<span data-ttu-id="8308f-110">Длинный идентификатор (КРЫШКА):</span><span class="sxs-lookup"><span data-stu-id="8308f-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="8308f-111">0x00000026</span><span class="sxs-lookup"><span data-stu-id="8308f-111">0x00000026</span></span>  <br/> |
|<span data-ttu-id="8308f-112">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="8308f-112">Data type:</span></span>  <br/> |<span data-ttu-id="8308f-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="8308f-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="8308f-114">Область:</span><span class="sxs-lookup"><span data-stu-id="8308f-114">Area:</span></span>  <br/> |<span data-ttu-id="8308f-115">Meetings (собрания);</span><span class="sxs-lookup"><span data-stu-id="8308f-115">Meetings</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="8308f-116">Замечания</span><span class="sxs-lookup"><span data-stu-id="8308f-116">Remarks</span></span>

<span data-ttu-id="8308f-117">Значение этого свойства необходимо присвоить одно из следующих:</span><span class="sxs-lookup"><span data-stu-id="8308f-117">The value of this property must be set to one of the following:</span></span>
  
|<span data-ttu-id="8308f-118">**Свойство**</span><span class="sxs-lookup"><span data-stu-id="8308f-118">**Property**</span></span>|<span data-ttu-id="8308f-119">**Значение**</span><span class="sxs-lookup"><span data-stu-id="8308f-119">**Value**</span></span>|<span data-ttu-id="8308f-120">**Описание**</span><span class="sxs-lookup"><span data-stu-id="8308f-120">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="8308f-121">mtgEmpty</span><span class="sxs-lookup"><span data-stu-id="8308f-121">mtgEmpty</span></span>  <br/> |<span data-ttu-id="8308f-122">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8308f-122">0x00000000</span></span>  <br/> |<span data-ttu-id="8308f-123">Не определено.</span><span class="sxs-lookup"><span data-stu-id="8308f-123">Unspecified.</span></span>  <br/> |
|<span data-ttu-id="8308f-124">mtgRequest</span><span class="sxs-lookup"><span data-stu-id="8308f-124">mtgRequest</span></span>  <br/> |<span data-ttu-id="8308f-125">0x00000001</span><span class="sxs-lookup"><span data-stu-id="8308f-125">0x00000001</span></span>  <br/> |<span data-ttu-id="8308f-126">Начальное собрание.</span><span class="sxs-lookup"><span data-stu-id="8308f-126">Initial meeting request.</span></span>  <br/> |
|<span data-ttu-id="8308f-127">mtgFull</span><span class="sxs-lookup"><span data-stu-id="8308f-127">mtgFull</span></span>  <br/> |<span data-ttu-id="8308f-128">0x00010000</span><span class="sxs-lookup"><span data-stu-id="8308f-128">0x00010000</span></span>  <br/> |<span data-ttu-id="8308f-129">Полное обновление.</span><span class="sxs-lookup"><span data-stu-id="8308f-129">Full update.</span></span>  <br/> |
|<span data-ttu-id="8308f-130">mtgInfo</span><span class="sxs-lookup"><span data-stu-id="8308f-130">mtgInfo</span></span>  <br/> |<span data-ttu-id="8308f-131">0x00020000</span><span class="sxs-lookup"><span data-stu-id="8308f-131">0x00020000</span></span>  <br/> |<span data-ttu-id="8308f-132">Информационные обновления.</span><span class="sxs-lookup"><span data-stu-id="8308f-132">Informational update.</span></span>  <br/> |
|<span data-ttu-id="8308f-133">mtgOutOfDate</span><span class="sxs-lookup"><span data-stu-id="8308f-133">mtgOutOfDate</span></span>  <br/> |<span data-ttu-id="8308f-134">0x00080000</span><span class="sxs-lookup"><span data-stu-id="8308f-134">0x00080000</span></span>  <br/> |<span data-ttu-id="8308f-135">Файлы более новых приглашения на собрание или обновление собрания было получено после этой команды.</span><span class="sxs-lookup"><span data-stu-id="8308f-135">A newer meeting request or meeting update was received after this one.</span></span>  <br/> |
|<span data-ttu-id="8308f-136">mtgDelegatorCopy</span><span class="sxs-lookup"><span data-stu-id="8308f-136">mtgDelegatorCopy</span></span>  <br/> |<span data-ttu-id="8308f-137">0x00100000</span><span class="sxs-lookup"><span data-stu-id="8308f-137">0x00100000</span></span>  <br/> |<span data-ttu-id="8308f-138">Это значение на копии сотрудника при объекты собрании значками делегат.</span><span class="sxs-lookup"><span data-stu-id="8308f-138">This is set on the delegator's copy when a delegate handles meeting-related objects.</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="8308f-139">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="8308f-139">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="8308f-140">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="8308f-140">Protocol specifications</span></span>

<span data-ttu-id="8308f-141">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="8308f-141">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="8308f-142">Содержит определения набора свойств и ссылки на связанные спецификаций протокола Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="8308f-142">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="8308f-143">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="8308f-143">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="8308f-144">Задает свойства и операции для встречи, приглашения на собрание и ответы.</span><span class="sxs-lookup"><span data-stu-id="8308f-144">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="8308f-145">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="8308f-145">Header files</span></span>

<span data-ttu-id="8308f-146">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="8308f-146">Mapidefs.h</span></span>
  
> <span data-ttu-id="8308f-147">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="8308f-147">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="8308f-148">См. также</span><span class="sxs-lookup"><span data-stu-id="8308f-148">See also</span></span>



[<span data-ttu-id="8308f-149">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="8308f-149">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="8308f-150">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="8308f-150">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="8308f-151">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="8308f-151">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="8308f-152">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="8308f-152">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)


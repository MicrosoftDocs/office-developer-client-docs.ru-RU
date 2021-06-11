---
title: Каноническое свойство PidTagRuleActions
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagRuleActions
api_type:
- COM
ms.assetid: 3ec4259a-8fe9-46c3-82b8-42c6907b8515
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: ab246414f7caaf76f462d9b80e762fe614c77c21
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32278902"
---
# <a name="pidtagruleactions-canonical-property"></a><span data-ttu-id="a99bf-103">Каноническое свойство PidTagRuleActions</span><span class="sxs-lookup"><span data-stu-id="a99bf-103">PidTagRuleActions Canonical Property</span></span>

  
  
<span data-ttu-id="a99bf-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a99bf-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a99bf-105">Содержит набор действий, связанных с правилом.</span><span class="sxs-lookup"><span data-stu-id="a99bf-105">Contains the set of actions associated with the rule.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="a99bf-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="a99bf-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="a99bf-107">PR_RULE_ACTIONS</span><span class="sxs-lookup"><span data-stu-id="a99bf-107">PR_RULE_ACTIONS</span></span>  <br/> |
|<span data-ttu-id="a99bf-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="a99bf-108">Identifier:</span></span>  <br/> |<span data-ttu-id="a99bf-109">0x6680</span><span class="sxs-lookup"><span data-stu-id="a99bf-109">0x6680</span></span>  <br/> |
|<span data-ttu-id="a99bf-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="a99bf-110">Data type:</span></span>  <br/> |<span data-ttu-id="a99bf-111">PT_ACTIONS</span><span class="sxs-lookup"><span data-stu-id="a99bf-111">PT_ACTIONS</span></span>  <br/> |
|<span data-ttu-id="a99bf-112">Область:</span><span class="sxs-lookup"><span data-stu-id="a99bf-112">Area:</span></span>  <br/> |<span data-ttu-id="a99bf-113">Правила стороне сервера</span><span class="sxs-lookup"><span data-stu-id="a99bf-113">Server Side Rules</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a99bf-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="a99bf-114">Remarks</span></span>

<span data-ttu-id="a99bf-115">Действия выражаются в качестве действия правила, а буфер значения свойства содержит структуру буфера данных действий правила, упакованную в [пакет [MS-OXORULE].](https://msdn.microsoft.com/library/70ac9436-501e-43e2-9163-20d2b546b886%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="a99bf-115">The actions are expressed as a rule action and the property value buffer contains the rule action data buffer structure packaged as specified in [[MS-OXORULE]](https://msdn.microsoft.com/library/70ac9436-501e-43e2-9163-20d2b546b886%28Office.15%29.aspx).</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="a99bf-116">Справочные материалы по MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="a99bf-116">MFCMAPI reference</span></span>

<span data-ttu-id="a99bf-117">Пример кода MFCMAPI указан в приведенной ниже таблице.</span><span class="sxs-lookup"><span data-stu-id="a99bf-117">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="a99bf-118">**Файл**</span><span class="sxs-lookup"><span data-stu-id="a99bf-118">**File**</span></span>|<span data-ttu-id="a99bf-119">**Функция**</span><span class="sxs-lookup"><span data-stu-id="a99bf-119">**Function**</span></span>|<span data-ttu-id="a99bf-120">**Примечание**</span><span class="sxs-lookup"><span data-stu-id="a99bf-120">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="a99bf-121">ImportProcs.cpp</span><span class="sxs-lookup"><span data-stu-id="a99bf-121">ImportProcs.cpp</span></span>  <br/> |<span data-ttu-id="a99bf-122">PropCopyMore, HrCopyActions</span><span class="sxs-lookup"><span data-stu-id="a99bf-122">PropCopyMore, HrCopyActions</span></span>  <br/> |<span data-ttu-id="a99bf-123">Эти функции демонстрируют, как PT_ACTIONS свойства для копирования другого свойства.</span><span class="sxs-lookup"><span data-stu-id="a99bf-123">These functions demonstrate how to parse a PT_ACTIONS property for the purposes of copying to another property.</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="a99bf-124">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="a99bf-124">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="a99bf-125">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="a99bf-125">Protocol specifications</span></span>

<span data-ttu-id="a99bf-126">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="a99bf-126">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="a99bf-127">Содержит ссылки на связанные Exchange Server протоколы.</span><span class="sxs-lookup"><span data-stu-id="a99bf-127">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="a99bf-128">[[MS-OXORULE]](https://msdn.microsoft.com/library/70ac9436-501e-43e2-9163-20d2b546b886%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="a99bf-128">[[MS-OXORULE]](https://msdn.microsoft.com/library/70ac9436-501e-43e2-9163-20d2b546b886%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="a99bf-129">Манипулирует входящие сообщения электронной почты на сервере.</span><span class="sxs-lookup"><span data-stu-id="a99bf-129">Manipulates incoming email messages on a server.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="a99bf-130">Файлы заголовки</span><span class="sxs-lookup"><span data-stu-id="a99bf-130">Header files</span></span>

<span data-ttu-id="a99bf-131">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="a99bf-131">Mapidefs.h</span></span>
  
> <span data-ttu-id="a99bf-132">Предоставляет определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="a99bf-132">Provides data type definitions.</span></span>
    
<span data-ttu-id="a99bf-133">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="a99bf-133">Mapitags.h</span></span>
  
> <span data-ttu-id="a99bf-134">Содержит определения свойств, перечисленных в качестве альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="a99bf-134">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="a99bf-135">См. также</span><span class="sxs-lookup"><span data-stu-id="a99bf-135">See also</span></span>



[<span data-ttu-id="a99bf-136">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="a99bf-136">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="a99bf-137">Канонические свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="a99bf-137">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="a99bf-138">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="a99bf-138">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="a99bf-139">Сопоставление имен MAPI с каноническими именами свойств</span><span class="sxs-lookup"><span data-stu-id="a99bf-139">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)


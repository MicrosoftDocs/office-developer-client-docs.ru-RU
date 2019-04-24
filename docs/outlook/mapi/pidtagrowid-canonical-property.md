---
title: Каноническое свойство PidTagRowid
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagRowid
api_type:
- COM
ms.assetid: 0fdcb55a-2971-4c7d-b61e-7ada2d19d0e6
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 8d58342e0460352bd9d260cb6e73de358cb2fc23
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359537"
---
# <a name="pidtagrowid-canonical-property"></a><span data-ttu-id="8c79e-103">Каноническое свойство PidTagRowid</span><span class="sxs-lookup"><span data-stu-id="8c79e-103">PidTagRowid Canonical Property</span></span>

  
  
<span data-ttu-id="8c79e-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8c79e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8c79e-105">Содержит уникальный идентификатор получателя в таблице получателей или таблице состояния.</span><span class="sxs-lookup"><span data-stu-id="8c79e-105">Contains a unique identifier for a recipient in a recipient table or status table.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="8c79e-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="8c79e-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="8c79e-107">ПР_РОВИД</span><span class="sxs-lookup"><span data-stu-id="8c79e-107">PR_ROWID</span></span>  <br/> |
|<span data-ttu-id="8c79e-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="8c79e-108">Identifier:</span></span>  <br/> |<span data-ttu-id="8c79e-109">0x3000</span><span class="sxs-lookup"><span data-stu-id="8c79e-109">0x3000</span></span>  <br/> |
|<span data-ttu-id="8c79e-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="8c79e-110">Data type:</span></span>  <br/> |<span data-ttu-id="8c79e-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="8c79e-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="8c79e-112">Область:</span><span class="sxs-lookup"><span data-stu-id="8c79e-112">Area:</span></span>  <br/> |<span data-ttu-id="8c79e-113">Общие протоколы MAPI</span><span class="sxs-lookup"><span data-stu-id="8c79e-113">MAPI common</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="8c79e-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="8c79e-114">Remarks</span></span>

<span data-ttu-id="8c79e-115">Это временное значение, которое является допустимым только в течение всего времени существования объекта, владеющего таблицей.</span><span class="sxs-lookup"><span data-stu-id="8c79e-115">This property is a temporary value that is valid only for the life of the object that owns the table.</span></span> <span data-ttu-id="8c79e-116">Он отображается в виде столбца таблицы, но не хранится.</span><span class="sxs-lookup"><span data-stu-id="8c79e-116">It appears as a column of the table but is not stored.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="8c79e-117">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="8c79e-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="8c79e-118">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="8c79e-118">Protocol specifications</span></span>

<span data-ttu-id="8c79e-119">[[MS — ОКСПРОПС]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="8c79e-119">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="8c79e-120">Содержит ссылки на соответствующие спецификации протоколов Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="8c79e-120">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="8c79e-121">[[MS — ОКСКФКСИКС]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="8c79e-121">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="8c79e-122">Обрабатывает порядок и потоки для передачи данных между клиентом и сервером.</span><span class="sxs-lookup"><span data-stu-id="8c79e-122">Handles the order and flow for data transfers between a client and server.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="8c79e-123">Файлы заГоловков</span><span class="sxs-lookup"><span data-stu-id="8c79e-123">Header files</span></span>

<span data-ttu-id="8c79e-124">MAPIDEFS. h</span><span class="sxs-lookup"><span data-stu-id="8c79e-124">Mapidefs.h</span></span>
  
> <span data-ttu-id="8c79e-125">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="8c79e-125">Provides data type definitions.</span></span>
    
<span data-ttu-id="8c79e-126">Мапитагс. h</span><span class="sxs-lookup"><span data-stu-id="8c79e-126">Mapitags.h</span></span>
  
> <span data-ttu-id="8c79e-127">Содержит определения свойств, перечисленных как альтернативные имена.</span><span class="sxs-lookup"><span data-stu-id="8c79e-127">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="8c79e-128">См. также</span><span class="sxs-lookup"><span data-stu-id="8c79e-128">See also</span></span>



[<span data-ttu-id="8c79e-129">IMessage::GetRecipientTable</span><span class="sxs-lookup"><span data-stu-id="8c79e-129">IMessage::GetRecipientTable</span></span>](imessage-getrecipienttable.md)
  
[<span data-ttu-id="8c79e-130">IMessage::ModifyRecipients</span><span class="sxs-lookup"><span data-stu-id="8c79e-130">IMessage::ModifyRecipients</span></span>](imessage-modifyrecipients.md)


[<span data-ttu-id="8c79e-131">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="8c79e-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="8c79e-132">Каноническое свойство MAPI</span><span class="sxs-lookup"><span data-stu-id="8c79e-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="8c79e-133">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="8c79e-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="8c79e-134">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="8c79e-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)


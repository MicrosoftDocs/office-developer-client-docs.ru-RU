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
ms.openlocfilehash: efa778f51ac047c911deb6a3c4d5d9e718dc33fb
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22565041"
---
# <a name="pidtagrowid-canonical-property"></a><span data-ttu-id="7aba3-103">Каноническое свойство PidTagRowid</span><span class="sxs-lookup"><span data-stu-id="7aba3-103">PidTagRowid Canonical Property</span></span>

  
  
<span data-ttu-id="7aba3-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7aba3-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7aba3-105">Содержит уникальный идентификатор для получателя в таблице получателей или таблице состояния.</span><span class="sxs-lookup"><span data-stu-id="7aba3-105">Contains a unique identifier for a recipient in a recipient table or status table.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="7aba3-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="7aba3-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="7aba3-107">PR_ROWID</span><span class="sxs-lookup"><span data-stu-id="7aba3-107">PR_ROWID</span></span>  <br/> |
|<span data-ttu-id="7aba3-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="7aba3-108">Identifier:</span></span>  <br/> |<span data-ttu-id="7aba3-109">0x3000</span><span class="sxs-lookup"><span data-stu-id="7aba3-109">0x3000</span></span>  <br/> |
|<span data-ttu-id="7aba3-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="7aba3-110">Data type:</span></span>  <br/> |<span data-ttu-id="7aba3-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="7aba3-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="7aba3-112">Область:</span><span class="sxs-lookup"><span data-stu-id="7aba3-112">Area:</span></span>  <br/> |<span data-ttu-id="7aba3-113">Распространенные MAPI</span><span class="sxs-lookup"><span data-stu-id="7aba3-113">MAPI common</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="7aba3-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="7aba3-114">Remarks</span></span>

<span data-ttu-id="7aba3-115">Это свойство является значением временной, который действителен только в течение времени жизни объекта, который несет ответственность за таблицы.</span><span class="sxs-lookup"><span data-stu-id="7aba3-115">This property is a temporary value that is valid only for the life of the object that owns the table.</span></span> <span data-ttu-id="7aba3-116">Отображается как столбец в таблице, но не сохраняется.</span><span class="sxs-lookup"><span data-stu-id="7aba3-116">It appears as a column of the table but is not stored.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="7aba3-117">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="7aba3-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="7aba3-118">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="7aba3-118">Protocol specifications</span></span>

<span data-ttu-id="7aba3-119">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="7aba3-119">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="7aba3-120">Содержит ссылки на связанные спецификаций протокола Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="7aba3-120">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="7aba3-121">[[MS-OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="7aba3-121">[[MS-OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="7aba3-122">Обрабатывает порядок и поток для передачи данных между клиентом и сервером.</span><span class="sxs-lookup"><span data-stu-id="7aba3-122">Handles the order and flow for data transfers between a client and server.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="7aba3-123">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="7aba3-123">Header files</span></span>

<span data-ttu-id="7aba3-124">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="7aba3-124">Mapidefs.h</span></span>
  
> <span data-ttu-id="7aba3-125">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="7aba3-125">Provides data type definitions.</span></span>
    
<span data-ttu-id="7aba3-126">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="7aba3-126">Mapitags.h</span></span>
  
> <span data-ttu-id="7aba3-127">Содержит определения свойства в списке альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="7aba3-127">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="7aba3-128">См. также</span><span class="sxs-lookup"><span data-stu-id="7aba3-128">See also</span></span>



[<span data-ttu-id="7aba3-129">IMessage::GetRecipientTable</span><span class="sxs-lookup"><span data-stu-id="7aba3-129">IMessage::GetRecipientTable</span></span>](imessage-getrecipienttable.md)
  
[<span data-ttu-id="7aba3-130">IMessage::ModifyRecipients</span><span class="sxs-lookup"><span data-stu-id="7aba3-130">IMessage::ModifyRecipients</span></span>](imessage-modifyrecipients.md)


[<span data-ttu-id="7aba3-131">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="7aba3-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="7aba3-132">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="7aba3-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="7aba3-133">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="7aba3-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="7aba3-134">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="7aba3-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)


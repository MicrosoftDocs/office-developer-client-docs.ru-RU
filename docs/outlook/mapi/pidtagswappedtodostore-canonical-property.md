---
title: Каноническое свойство PidTagSwappedToDoStore
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagSwappedToDoStore
api_type:
- COM
ms.assetid: 1edae9ac-fc9a-4bfe-b053-99de848c5144
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 41aa97a52176cf68775d6fd507d3d042888092cc
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25393861"
---
# <a name="pidtagswappedtodostore-canonical-property"></a><span data-ttu-id="7aa71-103">Каноническое свойство PidTagSwappedToDoStore</span><span class="sxs-lookup"><span data-stu-id="7aa71-103">PidTagSwappedToDoStore Canonical Property</span></span>

  
  
<span data-ttu-id="7aa71-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7aa71-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7aa71-105">Определяет необходимость для передачи после обработки сообщения электронной почты.</span><span class="sxs-lookup"><span data-stu-id="7aa71-105">Determines the need for post-transmit processing of an email.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="7aa71-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="7aa71-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="7aa71-107">PR_SWAPPED_TODO_STORE</span><span class="sxs-lookup"><span data-stu-id="7aa71-107">PR_SWAPPED_TODO_STORE</span></span>  <br/> |
|<span data-ttu-id="7aa71-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="7aa71-108">Identifier:</span></span>  <br/> |<span data-ttu-id="7aa71-109">0x0E2C</span><span class="sxs-lookup"><span data-stu-id="7aa71-109">0x0E2C</span></span>  <br/> |
|<span data-ttu-id="7aa71-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="7aa71-110">Data type:</span></span>  <br/> |<span data-ttu-id="7aa71-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="7aa71-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="7aa71-112">Область:</span><span class="sxs-lookup"><span data-stu-id="7aa71-112">Area:</span></span>  <br/> |<span data-ttu-id="7aa71-113">MAPI передаваемого</span><span class="sxs-lookup"><span data-stu-id="7aa71-113">MAPI non-transmittable</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="7aa71-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="7aa71-114">Remarks</span></span>

<span data-ttu-id="7aa71-115">Если это свойство установлено на черновик сообщения, выберите его значение должно быть присвоено значение свойства **PR_STORE_ENTRYID** ([PidTagStoreEntryId](pidtagstoreentryid-canonical-property.md)) сообщения.</span><span class="sxs-lookup"><span data-stu-id="7aa71-115">If this property is set on a draft message, then its value must be set to the value of **PR_STORE_ENTRYID** ([PidTagStoreEntryId](pidtagstoreentryid-canonical-property.md)) property of the message.</span></span>
  
<span data-ttu-id="7aa71-116">Дополнительные сведения см в [[MS-OXOFLAG]](https://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx) раздел «после передачи обработки сообщения пометкой.»</span><span class="sxs-lookup"><span data-stu-id="7aa71-116">For more information, see [[MS-OXOFLAG]](https://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx) section "Post-Transmit Processing of a Flagged Message."</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="7aa71-117">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="7aa71-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="7aa71-118">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="7aa71-118">Protocol specifications</span></span>

<span data-ttu-id="7aa71-119">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="7aa71-119">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="7aa71-120">Содержит ссылки на связанные спецификаций протокола Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="7aa71-120">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="7aa71-121">[[MS-OXOFLAG]](https://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="7aa71-121">[[MS-OXOFLAG]](https://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="7aa71-122">Задает свойства и операции, связанные с флагов.</span><span class="sxs-lookup"><span data-stu-id="7aa71-122">Specifies the properties and operations related to flagging.</span></span>
    
<span data-ttu-id="7aa71-123">[[MS-OXORMDR]](https://msdn.microsoft.com/library/5454ebcc-e5d1-4da8-a598-d393b101caab%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="7aa71-123">[[MS-OXORMDR]](https://msdn.microsoft.com/library/5454ebcc-e5d1-4da8-a598-d393b101caab%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="7aa71-124">Задает свойства и модель взаимодействия для электронной почты и других объектов напоминания.</span><span class="sxs-lookup"><span data-stu-id="7aa71-124">Specifies the properties and the interaction model for email and other object reminders.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="7aa71-125">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="7aa71-125">Header files</span></span>

<span data-ttu-id="7aa71-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="7aa71-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="7aa71-127">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="7aa71-127">Provides data type definitions.</span></span>
    
<span data-ttu-id="7aa71-128">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="7aa71-128">Mapitags.h</span></span>
  
> <span data-ttu-id="7aa71-129">Содержит определения свойства в списке альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="7aa71-129">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="7aa71-130">См. также</span><span class="sxs-lookup"><span data-stu-id="7aa71-130">See also</span></span>



[<span data-ttu-id="7aa71-131">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="7aa71-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="7aa71-132">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="7aa71-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="7aa71-133">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="7aa71-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="7aa71-134">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="7aa71-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)


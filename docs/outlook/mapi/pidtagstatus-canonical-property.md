---
title: Каноническое свойство PidTagStatus
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagStatus
api_type:
- COM
ms.assetid: 8b947660-eafe-47e1-9595-bd3ab7d455bf
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: de2342ef4d3e9d06f198e06dc19c65b7b144624f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32278794"
---
# <a name="pidtagstatus-canonical-property"></a><span data-ttu-id="3c1d4-103">Каноническое свойство PidTagStatus</span><span class="sxs-lookup"><span data-stu-id="3c1d4-103">PidTagStatus Canonical Property</span></span>

  
  
<span data-ttu-id="3c1d4-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3c1d4-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3c1d4-105">Содержит 32-битную битмаку флагов, определяя состояние папки.</span><span class="sxs-lookup"><span data-stu-id="3c1d4-105">Contains a 32-bit bitmask of flags that define folder status.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="3c1d4-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="3c1d4-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="3c1d4-107">PR_STATUS</span><span class="sxs-lookup"><span data-stu-id="3c1d4-107">PR_STATUS</span></span>  <br/> |
|<span data-ttu-id="3c1d4-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="3c1d4-108">Identifier:</span></span>  <br/> |<span data-ttu-id="3c1d4-109">0x360B</span><span class="sxs-lookup"><span data-stu-id="3c1d4-109">0x360B</span></span>  <br/> |
|<span data-ttu-id="3c1d4-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="3c1d4-110">Data type:</span></span>  <br/> |<span data-ttu-id="3c1d4-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="3c1d4-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="3c1d4-112">Область:</span><span class="sxs-lookup"><span data-stu-id="3c1d4-112">Area:</span></span>  <br/> |<span data-ttu-id="3c1d4-113">Контейнер MAPI</span><span class="sxs-lookup"><span data-stu-id="3c1d4-113">MAPI container</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="3c1d4-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="3c1d4-114">Remarks</span></span>

<span data-ttu-id="3c1d4-115">Это свойство для папок аналогично **свойству PR_MSG_STATUS** [(PidTagMessageStatus)](pidtagmessagestatus-canonical-property.md)для сообщений.</span><span class="sxs-lookup"><span data-stu-id="3c1d4-115">This property for folders is analogous to the **PR_MSG_STATUS** ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md)) property for messages.</span></span> <span data-ttu-id="3c1d4-116">Его флаги предоставляются только для клиентского приложения и не влияют на хранилище сообщений.</span><span class="sxs-lookup"><span data-stu-id="3c1d4-116">Its flags are provided for the client application only and do not affect the message store.</span></span> <span data-ttu-id="3c1d4-117">Клиенты могут использовать или игнорировать эти параметры.</span><span class="sxs-lookup"><span data-stu-id="3c1d4-117">Clients can use or ignore these settings.</span></span> <span data-ttu-id="3c1d4-118">Клиент также может определить собственные значения для битов этого свойства, вызываемых клиентом.</span><span class="sxs-lookup"><span data-stu-id="3c1d4-118">The client can also define its own values for the client-definable bits of this property.</span></span>
  
<span data-ttu-id="3c1d4-119">Для bitmask можно установить один или несколько следующих флагов:</span><span class="sxs-lookup"><span data-stu-id="3c1d4-119">One or more of the following flags can be set for the bitmask:</span></span>
  
<span data-ttu-id="3c1d4-120">FLDSTATUS_DELMARKED</span><span class="sxs-lookup"><span data-stu-id="3c1d4-120">FLDSTATUS_DELMARKED</span></span> 
  
> <span data-ttu-id="3c1d4-121">Папка помечена для удаления.</span><span class="sxs-lookup"><span data-stu-id="3c1d4-121">The folder is marked for deletion.</span></span> <span data-ttu-id="3c1d4-122">Клиентская заявка задает этот флаг.</span><span class="sxs-lookup"><span data-stu-id="3c1d4-122">The client application sets this flag.</span></span>
    
<span data-ttu-id="3c1d4-123">FLDSTATUS_HIDDEN</span><span class="sxs-lookup"><span data-stu-id="3c1d4-123">FLDSTATUS_HIDDEN</span></span> 
  
> <span data-ttu-id="3c1d4-124">Папка скрыта.</span><span class="sxs-lookup"><span data-stu-id="3c1d4-124">The folder is hidden.</span></span>
    
<span data-ttu-id="3c1d4-125">FLDSTATUS_HIGHLIGHTED</span><span class="sxs-lookup"><span data-stu-id="3c1d4-125">FLDSTATUS_HIGHLIGHTED</span></span> 
  
> <span data-ttu-id="3c1d4-126">Папка выделена, например, в обратном видео.</span><span class="sxs-lookup"><span data-stu-id="3c1d4-126">The folder is highlighted, for example, shown in reverse video.</span></span>
    
<span data-ttu-id="3c1d4-127">FLDSTATUS_TAGGED</span><span class="sxs-lookup"><span data-stu-id="3c1d4-127">FLDSTATUS_TAGGED</span></span> 
  
> <span data-ttu-id="3c1d4-128">Папка помечена.</span><span class="sxs-lookup"><span data-stu-id="3c1d4-128">The folder is tagged.</span></span>
    
<span data-ttu-id="3c1d4-129">Поставщики магазинов сообщений устанавливают это свойство в папке до одного или более этих значений, и клиенты интерпретируют состояние, соответствующее их приложениям.</span><span class="sxs-lookup"><span data-stu-id="3c1d4-129">Message store providers set this property on a folder to one or more of these values and clients interpret the status as appropriate for their applications.</span></span> <span data-ttu-id="3c1d4-130">Например, клиент может использовать состояние папки, чтобы визуально различать папки в таблице иерархии, отображая папки с одинаковым состоянием таким же образом.</span><span class="sxs-lookup"><span data-stu-id="3c1d4-130">For example, a client can use the folder status to visually differentiate between folders in a hierarchy table, displaying folders with the same status in the same way.</span></span> <span data-ttu-id="3c1d4-131">Выделенные папки можно показывать в обратном видео, помеченные папки и папки с меткой для удаления можно показывать содержательным значком, а скрытые папки можно скрыть.</span><span class="sxs-lookup"><span data-stu-id="3c1d4-131">Highlighted folders can be shown in reverse video, tagged folders and folders marked for deletion can be shown with a meaningful icon, and hidden folders can be concealed.</span></span>
  
<span data-ttu-id="3c1d4-132">Биты от 16 до 31 ("0x10000" через "0x80000000") этого свойства доступны для использования клиентского приложения IPM.</span><span class="sxs-lookup"><span data-stu-id="3c1d4-132">Bits 16 through 31 ("0x10000" through "0x80000000") of this property are available for use by the IPM client application.</span></span> <span data-ttu-id="3c1d4-133">Все остальные биты зарезервированы для использования MAPI; те, которые не определены в предыдущем списке, сначала должны быть задатки нулю, а не изменены.</span><span class="sxs-lookup"><span data-stu-id="3c1d4-133">All other bits are reserved for use by MAPI; those not defined in the preceding list should be initially set to zero and not altered.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="3c1d4-134">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="3c1d4-134">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="3c1d4-135">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="3c1d4-135">Protocol specifications</span></span>

<span data-ttu-id="3c1d4-136">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="3c1d4-136">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="3c1d4-137">Содержит ссылки на связанные Exchange Server протоколы.</span><span class="sxs-lookup"><span data-stu-id="3c1d4-137">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="3c1d4-138">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="3c1d4-138">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="3c1d4-139">Обрабатывает объекты сообщений и вложений.</span><span class="sxs-lookup"><span data-stu-id="3c1d4-139">Handles message and attachment objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="3c1d4-140">Файлы заголовки</span><span class="sxs-lookup"><span data-stu-id="3c1d4-140">Header files</span></span>

<span data-ttu-id="3c1d4-141">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="3c1d4-141">Mapidefs.h</span></span>
  
> <span data-ttu-id="3c1d4-142">Предоставляет определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="3c1d4-142">Provides data type definitions.</span></span>
    
<span data-ttu-id="3c1d4-143">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="3c1d4-143">Mapitags.h</span></span>
  
> <span data-ttu-id="3c1d4-144">Содержит определения свойств, перечисленных в качестве альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="3c1d4-144">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="3c1d4-145">См. также</span><span class="sxs-lookup"><span data-stu-id="3c1d4-145">See also</span></span>



[<span data-ttu-id="3c1d4-146">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="3c1d4-146">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="3c1d4-147">Канонические свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="3c1d4-147">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="3c1d4-148">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="3c1d4-148">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="3c1d4-149">Сопоставление имен MAPI с каноническими именами свойств</span><span class="sxs-lookup"><span data-stu-id="3c1d4-149">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)


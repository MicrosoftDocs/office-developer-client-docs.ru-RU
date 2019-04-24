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
# <a name="pidtagstatus-canonical-property"></a><span data-ttu-id="deaed-103">Каноническое свойство PidTagStatus</span><span class="sxs-lookup"><span data-stu-id="deaed-103">PidTagStatus Canonical Property</span></span>

  
  
<span data-ttu-id="deaed-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="deaed-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="deaed-105">Содержит 32 — битовую маску для флагов, определяющих состояние папки.</span><span class="sxs-lookup"><span data-stu-id="deaed-105">Contains a 32-bit bitmask of flags that define folder status.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="deaed-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="deaed-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="deaed-107">ПР_СТАТУС</span><span class="sxs-lookup"><span data-stu-id="deaed-107">PR_STATUS</span></span>  <br/> |
|<span data-ttu-id="deaed-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="deaed-108">Identifier:</span></span>  <br/> |<span data-ttu-id="deaed-109">0x360B</span><span class="sxs-lookup"><span data-stu-id="deaed-109">0x360B</span></span>  <br/> |
|<span data-ttu-id="deaed-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="deaed-110">Data type:</span></span>  <br/> |<span data-ttu-id="deaed-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="deaed-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="deaed-112">Область:</span><span class="sxs-lookup"><span data-stu-id="deaed-112">Area:</span></span>  <br/> |<span data-ttu-id="deaed-113">Контейнер MAPI</span><span class="sxs-lookup"><span data-stu-id="deaed-113">MAPI container</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="deaed-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="deaed-114">Remarks</span></span>

<span data-ttu-id="deaed-115">Это свойство для папок аналогично свойству **пр_мсг_статус** ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md)) для сообщений.</span><span class="sxs-lookup"><span data-stu-id="deaed-115">This property for folders is analogous to the **PR_MSG_STATUS** ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md)) property for messages.</span></span> <span data-ttu-id="deaed-116">Его флаги предоставляются только для клиентского приложения и не влияют на хранилище сообщений.</span><span class="sxs-lookup"><span data-stu-id="deaed-116">Its flags are provided for the client application only and do not affect the message store.</span></span> <span data-ttu-id="deaed-117">Клиенты могут использовать или игнорировать эти параметры.</span><span class="sxs-lookup"><span data-stu-id="deaed-117">Clients can use or ignore these settings.</span></span> <span data-ttu-id="deaed-118">Клиент также может определить собственные значения для задаваемых клиентом битов этого свойства.</span><span class="sxs-lookup"><span data-stu-id="deaed-118">The client can also define its own values for the client-definable bits of this property.</span></span>
  
<span data-ttu-id="deaed-119">Для битовой маски можно задать один или несколько из следующих флагов:</span><span class="sxs-lookup"><span data-stu-id="deaed-119">One or more of the following flags can be set for the bitmask:</span></span>
  
<span data-ttu-id="deaed-120">ФЛДСТАТУС_ДЕЛМАРКЕД</span><span class="sxs-lookup"><span data-stu-id="deaed-120">FLDSTATUS_DELMARKED</span></span> 
  
> <span data-ttu-id="deaed-121">Папка помечена для удаления.</span><span class="sxs-lookup"><span data-stu-id="deaed-121">The folder is marked for deletion.</span></span> <span data-ttu-id="deaed-122">Клиентское приложение устанавливает этот флаг.</span><span class="sxs-lookup"><span data-stu-id="deaed-122">The client application sets this flag.</span></span>
    
<span data-ttu-id="deaed-123">ФЛДСТАТУС_ХИДДЕН</span><span class="sxs-lookup"><span data-stu-id="deaed-123">FLDSTATUS_HIDDEN</span></span> 
  
> <span data-ttu-id="deaed-124">Папка скрыта.</span><span class="sxs-lookup"><span data-stu-id="deaed-124">The folder is hidden.</span></span>
    
<span data-ttu-id="deaed-125">ФЛДСТАТУС_ХИГХЛИГХТЕД</span><span class="sxs-lookup"><span data-stu-id="deaed-125">FLDSTATUS_HIGHLIGHTED</span></span> 
  
> <span data-ttu-id="deaed-126">Папка выделяется, например, в обратном видеоролике.</span><span class="sxs-lookup"><span data-stu-id="deaed-126">The folder is highlighted, for example, shown in reverse video.</span></span>
    
<span data-ttu-id="deaed-127">ФЛДСТАТУС_ТАГЖЕД</span><span class="sxs-lookup"><span data-stu-id="deaed-127">FLDSTATUS_TAGGED</span></span> 
  
> <span data-ttu-id="deaed-128">Папка размечена.</span><span class="sxs-lookup"><span data-stu-id="deaed-128">The folder is tagged.</span></span>
    
<span data-ttu-id="deaed-129">Поставщики хранилища сообщений присвойте этому свойству папки одно или несколько из этих значений, и клиенты интерпретируют состояние в соответствии с их приложениями.</span><span class="sxs-lookup"><span data-stu-id="deaed-129">Message store providers set this property on a folder to one or more of these values and clients interpret the status as appropriate for their applications.</span></span> <span data-ttu-id="deaed-130">Например, клиент может использовать состояние папки для визуального различения папок в иерархической таблице, отображая папки с одинаковым состоянием аналогичным образом.</span><span class="sxs-lookup"><span data-stu-id="deaed-130">For example, a client can use the folder status to visually differentiate between folders in a hierarchy table, displaying folders with the same status in the same way.</span></span> <span data-ttu-id="deaed-131">Выделенные папки можно отобразить в обратном видеоролике, папках с тегами и папках, помеченных для удаления, можно отобразить с осмысленным значком, а скрытые папки можно скрыть.</span><span class="sxs-lookup"><span data-stu-id="deaed-131">Highlighted folders can be shown in reverse video, tagged folders and folders marked for deletion can be shown with a meaningful icon, and hidden folders can be concealed.</span></span>
  
<span data-ttu-id="deaed-132">Биты с 16 по 31 ("0x10000", "0x80000000") этого свойства доступны для использования клиентским приложением IPM.</span><span class="sxs-lookup"><span data-stu-id="deaed-132">Bits 16 through 31 ("0x10000" through "0x80000000") of this property are available for use by the IPM client application.</span></span> <span data-ttu-id="deaed-133">Все остальные биты зарезервированы для использования MAPI; для тех, которые не определены в предыдущем списке, необходимо сначала установить нулевое значение и не изменять.</span><span class="sxs-lookup"><span data-stu-id="deaed-133">All other bits are reserved for use by MAPI; those not defined in the preceding list should be initially set to zero and not altered.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="deaed-134">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="deaed-134">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="deaed-135">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="deaed-135">Protocol specifications</span></span>

<span data-ttu-id="deaed-136">[[MS — ОКСПРОПС]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="deaed-136">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="deaed-137">Содержит ссылки на соответствующие спецификации протоколов Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="deaed-137">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="deaed-138">[[MS — ОКСКМСГ]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="deaed-138">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="deaed-139">Обрабатывает объекты сообщений и вложений.</span><span class="sxs-lookup"><span data-stu-id="deaed-139">Handles message and attachment objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="deaed-140">Файлы заГоловков</span><span class="sxs-lookup"><span data-stu-id="deaed-140">Header files</span></span>

<span data-ttu-id="deaed-141">MAPIDEFS. h</span><span class="sxs-lookup"><span data-stu-id="deaed-141">Mapidefs.h</span></span>
  
> <span data-ttu-id="deaed-142">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="deaed-142">Provides data type definitions.</span></span>
    
<span data-ttu-id="deaed-143">Мапитагс. h</span><span class="sxs-lookup"><span data-stu-id="deaed-143">Mapitags.h</span></span>
  
> <span data-ttu-id="deaed-144">Содержит определения свойств, перечисленных как альтернативные имена.</span><span class="sxs-lookup"><span data-stu-id="deaed-144">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="deaed-145">См. также</span><span class="sxs-lookup"><span data-stu-id="deaed-145">See also</span></span>



[<span data-ttu-id="deaed-146">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="deaed-146">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="deaed-147">Каноническое свойство MAPI</span><span class="sxs-lookup"><span data-stu-id="deaed-147">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="deaed-148">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="deaed-148">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="deaed-149">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="deaed-149">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)


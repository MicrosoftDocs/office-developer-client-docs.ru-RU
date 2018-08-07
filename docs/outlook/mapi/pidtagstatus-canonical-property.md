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
ms.openlocfilehash: 01a65306e5e0d34ed6f1ce7231227224868ff5cb
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19811962"
---
# <a name="pidtagstatus-canonical-property"></a><span data-ttu-id="b9c5e-103">Каноническое свойство PidTagStatus</span><span class="sxs-lookup"><span data-stu-id="b9c5e-103">PidTagStatus Canonical Property</span></span>

  
  
<span data-ttu-id="b9c5e-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="b9c5e-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="b9c5e-105">Содержит Битовая 32-разрядная версия флаги, описывающие состояние папки.</span><span class="sxs-lookup"><span data-stu-id="b9c5e-105">Contains a 32-bit bitmask of flags that define folder status.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="b9c5e-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="b9c5e-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="b9c5e-107">PR_STATUS</span><span class="sxs-lookup"><span data-stu-id="b9c5e-107">PR_STATUS</span></span>  <br/> |
|<span data-ttu-id="b9c5e-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="b9c5e-108">Identifier:</span></span>  <br/> |<span data-ttu-id="b9c5e-109">0x360B</span><span class="sxs-lookup"><span data-stu-id="b9c5e-109">0x360B</span></span>  <br/> |
|<span data-ttu-id="b9c5e-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="b9c5e-110">Data type:</span></span>  <br/> |<span data-ttu-id="b9c5e-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="b9c5e-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="b9c5e-112">Область:</span><span class="sxs-lookup"><span data-stu-id="b9c5e-112">Area:</span></span>  <br/> |<span data-ttu-id="b9c5e-113">Контейнер MAPI</span><span class="sxs-lookup"><span data-stu-id="b9c5e-113">MAPI container</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b9c5e-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="b9c5e-114">Remarks</span></span>

<span data-ttu-id="b9c5e-115">Это свойство для папок является аналогом свойство **PR_MSG_STATUS** ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md)) для сообщений.</span><span class="sxs-lookup"><span data-stu-id="b9c5e-115">This property for folders is analogous to the **PR_MSG_STATUS** ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md)) property for messages.</span></span> <span data-ttu-id="b9c5e-116">Флаги предоставляются для в клиентском приложении и не влияют на хранилище сообщений.</span><span class="sxs-lookup"><span data-stu-id="b9c5e-116">Its flags are provided for the client application only and do not affect the message store.</span></span> <span data-ttu-id="b9c5e-117">Клиенты могут использовать или эти параметры игнорируются.</span><span class="sxs-lookup"><span data-stu-id="b9c5e-117">Clients can use or ignore these settings.</span></span> <span data-ttu-id="b9c5e-118">Клиент можно также определить собственные значения для клиента определенный бит этого свойства.</span><span class="sxs-lookup"><span data-stu-id="b9c5e-118">The client can also define its own values for the client-definable bits of this property.</span></span>
  
<span data-ttu-id="b9c5e-119">Для Битовая маска, которая может быть установлено одно или несколько из следующих флагов:</span><span class="sxs-lookup"><span data-stu-id="b9c5e-119">One or more of the following flags can be set for the bitmask:</span></span>
  
<span data-ttu-id="b9c5e-120">FLDSTATUS_DELMARKED</span><span class="sxs-lookup"><span data-stu-id="b9c5e-120">FLDSTATUS_DELMARKED</span></span> 
  
> <span data-ttu-id="b9c5e-121">Папка помечается для удаления.</span><span class="sxs-lookup"><span data-stu-id="b9c5e-121">The folder is marked for deletion.</span></span> <span data-ttu-id="b9c5e-122">Клиентское приложение задает этот флаг.</span><span class="sxs-lookup"><span data-stu-id="b9c5e-122">The client application sets this flag.</span></span>
    
<span data-ttu-id="b9c5e-123">FLDSTATUS_HIDDEN</span><span class="sxs-lookup"><span data-stu-id="b9c5e-123">FLDSTATUS_HIDDEN</span></span> 
  
> <span data-ttu-id="b9c5e-124">Папка является скрытым.</span><span class="sxs-lookup"><span data-stu-id="b9c5e-124">The folder is hidden.</span></span>
    
<span data-ttu-id="b9c5e-125">FLDSTATUS_HIGHLIGHTED</span><span class="sxs-lookup"><span data-stu-id="b9c5e-125">FLDSTATUS_HIGHLIGHTED</span></span> 
  
> <span data-ttu-id="b9c5e-126">Папка будет выделена, например, показано в обратном порядке видео.</span><span class="sxs-lookup"><span data-stu-id="b9c5e-126">The folder is highlighted, for example, shown in reverse video.</span></span>
    
<span data-ttu-id="b9c5e-127">FLDSTATUS_TAGGED</span><span class="sxs-lookup"><span data-stu-id="b9c5e-127">FLDSTATUS_TAGGED</span></span> 
  
> <span data-ttu-id="b9c5e-128">Папка тегами.</span><span class="sxs-lookup"><span data-stu-id="b9c5e-128">The folder is tagged.</span></span>
    
<span data-ttu-id="b9c5e-129">Этому свойству присвоено поставщиков хранилища сообщений в папке один или несколько из следующих значений и клиентов интерпретации состояния в зависимости от своих приложений.</span><span class="sxs-lookup"><span data-stu-id="b9c5e-129">Message store providers set this property on a folder to one or more of these values and clients interpret the status as appropriate for their applications.</span></span> <span data-ttu-id="b9c5e-130">Например клиент может использовать состояние папки позволяет визуально различать папок в иерархии таблицы, отображение папок в одном состоянии так же, как.</span><span class="sxs-lookup"><span data-stu-id="b9c5e-130">For example, a client can use the folder status to visually differentiate between folders in a hierarchy table, displaying folders with the same status in the same way.</span></span> <span data-ttu-id="b9c5e-131">Выделенный папок можно будет отображаться в обратном видео, помеченных папки и папки, помеченные для удаления могут отображаться со значком удобной для восприятия и скрытые папки можно скрытых.</span><span class="sxs-lookup"><span data-stu-id="b9c5e-131">Highlighted folders can be shown in reverse video, tagged folders and folders marked for deletion can be shown with a meaningful icon, and hidden folders can be concealed.</span></span>
  
<span data-ttu-id="b9c5e-132">Бит 16 до 31 («0x10000» через «0x80000000») этого свойства доступны для использования клиентским приложением IPM.</span><span class="sxs-lookup"><span data-stu-id="b9c5e-132">Bits 16 through 31 ("0x10000" through "0x80000000") of this property are available for use by the IPM client application.</span></span> <span data-ttu-id="b9c5e-133">Все другие биты, зарезервированы для использования с MAPI; не определенных в предыдущем списке следует сначала задать нулевое значение и не изменяется.</span><span class="sxs-lookup"><span data-stu-id="b9c5e-133">All other bits are reserved for use by MAPI; those not defined in the preceding list should be initially set to zero and not altered.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="b9c5e-134">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="b9c5e-134">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="b9c5e-135">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="b9c5e-135">Protocol specifications</span></span>

<span data-ttu-id="b9c5e-136">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b9c5e-136">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="b9c5e-137">Содержит ссылки на связанные спецификаций протокола Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="b9c5e-137">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="b9c5e-138">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b9c5e-138">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="b9c5e-139">Обрабатывает объекты сообщения и вложения.</span><span class="sxs-lookup"><span data-stu-id="b9c5e-139">Handles message and attachment objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="b9c5e-140">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="b9c5e-140">Header files</span></span>

<span data-ttu-id="b9c5e-141">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="b9c5e-141">Mapidefs.h</span></span>
  
> <span data-ttu-id="b9c5e-142">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="b9c5e-142">Provides data type definitions.</span></span>
    
<span data-ttu-id="b9c5e-143">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="b9c5e-143">Mapitags.h</span></span>
  
> <span data-ttu-id="b9c5e-144">Содержит определения свойства в списке альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="b9c5e-144">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="b9c5e-145">См. также</span><span class="sxs-lookup"><span data-stu-id="b9c5e-145">See also</span></span>



[<span data-ttu-id="b9c5e-146">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="b9c5e-146">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="b9c5e-147">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="b9c5e-147">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="b9c5e-148">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="b9c5e-148">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="b9c5e-149">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="b9c5e-149">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)


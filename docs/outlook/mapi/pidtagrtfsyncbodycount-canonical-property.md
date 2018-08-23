---
title: Каноническое свойство PidTagRtfSyncBodyCount
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagRtfSyncBodyCount
api_type:
- COM
ms.assetid: b7267be4-8d5c-4dc7-86b2-651e03e84f9b
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: b88c036b3bc9b29962204ea0b90bd460ee1cf90f
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22585173"
---
# <a name="pidtagrtfsyncbodycount-canonical-property"></a><span data-ttu-id="da6ea-103">Каноническое свойство PidTagRtfSyncBodyCount</span><span class="sxs-lookup"><span data-stu-id="da6ea-103">PidTagRtfSyncBodyCount Canonical Property</span></span>

  
  
<span data-ttu-id="da6ea-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="da6ea-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="da6ea-105">Содержит число значительные символов из текста сообщения.</span><span class="sxs-lookup"><span data-stu-id="da6ea-105">Contains a count of the significant characters of the message text.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="da6ea-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="da6ea-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="da6ea-107">PR_RTF_SYNC_BODY_COUNT</span><span class="sxs-lookup"><span data-stu-id="da6ea-107">PR_RTF_SYNC_BODY_COUNT</span></span>  <br/> |
|<span data-ttu-id="da6ea-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="da6ea-108">Identifier:</span></span>  <br/> |<span data-ttu-id="da6ea-109">0x1007</span><span class="sxs-lookup"><span data-stu-id="da6ea-109">0x1007</span></span>  <br/> |
|<span data-ttu-id="da6ea-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="da6ea-110">Data type:</span></span>  <br/> |<span data-ttu-id="da6ea-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="da6ea-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="da6ea-112">Область:</span><span class="sxs-lookup"><span data-stu-id="da6ea-112">Area:</span></span>  <br/> |<span data-ttu-id="da6ea-113">Сообщение MAPI</span><span class="sxs-lookup"><span data-stu-id="da6ea-113">MAPI message</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="da6ea-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="da6ea-114">Remarks</span></span>

<span data-ttu-id="da6ea-115">Функция [RTFSync](rtfsync.md) вычисляет число символов в текст, используя только те, которые считаются важными к сообщению.</span><span class="sxs-lookup"><span data-stu-id="da6ea-115">The [RTFSync](rtfsync.md) function computes the count of characters in the text using only those that it considers to be significant to the message.</span></span> <span data-ttu-id="da6ea-116">Например некоторые пробелов и других допускающие игнорирование символы опускаются из числа.</span><span class="sxs-lookup"><span data-stu-id="da6ea-116">For example, some white space and other ignorable characters are omitted from the count.</span></span> 
  
<span data-ttu-id="da6ea-117">Это свойство является свойством дополнительный форматированный текст (RTF).</span><span class="sxs-lookup"><span data-stu-id="da6ea-117">This property is a Rich Text Format (RTF) auxiliary property.</span></span> <span data-ttu-id="da6ea-118">Эти свойства, используемые функцией **RTFSync** и не предназначен для непосредственного использования в клиентских приложениях.</span><span class="sxs-lookup"><span data-stu-id="da6ea-118">These properties are used by the **RTFSync** function and are not intended to be used directly by client applications.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="da6ea-119">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="da6ea-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="da6ea-120">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="da6ea-120">Protocol specifications</span></span>

<span data-ttu-id="da6ea-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="da6ea-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="da6ea-122">Содержит ссылки на связанные спецификаций протокола Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="da6ea-122">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="da6ea-123">[[MS-OXTNEF]](http://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="da6ea-123">[[MS-OXTNEF]](http://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="da6ea-124">Кодирует и декодирует объекты сообщения и вложения в представление эффективным потока.</span><span class="sxs-lookup"><span data-stu-id="da6ea-124">Encodes and decodes message and attachment objects to an efficient stream representation.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="da6ea-125">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="da6ea-125">Header files</span></span>

<span data-ttu-id="da6ea-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="da6ea-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="da6ea-127">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="da6ea-127">Provides data type definitions.</span></span>
    
<span data-ttu-id="da6ea-128">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="da6ea-128">Mapitags.h</span></span>
  
> <span data-ttu-id="da6ea-129">Содержит определения свойства в списке альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="da6ea-129">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="da6ea-130">См. также</span><span class="sxs-lookup"><span data-stu-id="da6ea-130">See also</span></span>



[<span data-ttu-id="da6ea-131">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="da6ea-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="da6ea-132">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="da6ea-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="da6ea-133">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="da6ea-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="da6ea-134">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="da6ea-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)


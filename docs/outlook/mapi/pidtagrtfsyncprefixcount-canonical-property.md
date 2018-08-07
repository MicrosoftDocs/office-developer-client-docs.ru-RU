---
title: Каноническое свойство PidTagRtfSyncPrefixCount
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagRtfSyncPrefixCount
api_type:
- COM
ms.assetid: c2b15ac5-9e89-4ee2-812d-102d0b2ac56e
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: c9a62365b46e85cc8f5d22fd31de3b5c6bd3f76a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19811764"
---
# <a name="pidtagrtfsyncprefixcount-canonical-property"></a><span data-ttu-id="f7d4a-103">Каноническое свойство PidTagRtfSyncPrefixCount</span><span class="sxs-lookup"><span data-stu-id="f7d4a-103">PidTagRtfSyncPrefixCount Canonical Property</span></span>

  
  
<span data-ttu-id="f7d4a-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="f7d4a-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="f7d4a-105">Содержит число допускающие игнорирование символы, отображаемые перед значительные символов сообщения.</span><span class="sxs-lookup"><span data-stu-id="f7d4a-105">Contains a count of the ignorable characters that appear before the significant characters of the message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="f7d4a-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="f7d4a-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="f7d4a-107">PR_RTF_SYNC_PREFIX_COUNT</span><span class="sxs-lookup"><span data-stu-id="f7d4a-107">PR_RTF_SYNC_PREFIX_COUNT</span></span>  <br/> |
|<span data-ttu-id="f7d4a-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="f7d4a-108">Identifier:</span></span>  <br/> |<span data-ttu-id="f7d4a-109">0x1010</span><span class="sxs-lookup"><span data-stu-id="f7d4a-109">0x1010</span></span>  <br/> |
|<span data-ttu-id="f7d4a-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="f7d4a-110">Data type:</span></span>  <br/> |<span data-ttu-id="f7d4a-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="f7d4a-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="f7d4a-112">Область:</span><span class="sxs-lookup"><span data-stu-id="f7d4a-112">Area:</span></span>  <br/> |<span data-ttu-id="f7d4a-113">Сообщение MAPI</span><span class="sxs-lookup"><span data-stu-id="f7d4a-113">MAPI message</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f7d4a-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="f7d4a-114">Remarks</span></span>

<span data-ttu-id="f7d4a-115">Количество символов префикса не включает пробелы.</span><span class="sxs-lookup"><span data-stu-id="f7d4a-115">The count of prefix characters does not include white space.</span></span>
  
<span data-ttu-id="f7d4a-116">Это свойство является свойством дополнительный форматированный текст (RTF).</span><span class="sxs-lookup"><span data-stu-id="f7d4a-116">This property is a Rich Text Format (RTF) auxiliary property.</span></span> <span data-ttu-id="f7d4a-117">Дополнительные свойства RTF используется функцией [RTFSync](rtfsync.md) и не предназначен для непосредственного использования в клиентских приложениях.</span><span class="sxs-lookup"><span data-stu-id="f7d4a-117">RTF auxiliary properties are used by the [RTFSync](rtfsync.md) function and are not intended to be used directly by client applications.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="f7d4a-118">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="f7d4a-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="f7d4a-119">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="f7d4a-119">Protocol specifications</span></span>

<span data-ttu-id="f7d4a-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f7d4a-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="f7d4a-121">Содержит ссылки на связанные спецификаций протокола Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="f7d4a-121">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="f7d4a-122">[[MS-OXTNEF]](http://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f7d4a-122">[[MS-OXTNEF]](http://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="f7d4a-123">Кодирует и декодирует объекты сообщения и вложения в представление эффективным потока.</span><span class="sxs-lookup"><span data-stu-id="f7d4a-123">Encodes and decodes message and attachment objects to an efficient stream representation.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="f7d4a-124">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="f7d4a-124">Header files</span></span>

<span data-ttu-id="f7d4a-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="f7d4a-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="f7d4a-126">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="f7d4a-126">Provides data type definitions.</span></span>
    
<span data-ttu-id="f7d4a-127">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="f7d4a-127">Mapitags.h</span></span>
  
> <span data-ttu-id="f7d4a-128">Содержит определения свойства в списке альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="f7d4a-128">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="f7d4a-129">См. также</span><span class="sxs-lookup"><span data-stu-id="f7d4a-129">See also</span></span>



[<span data-ttu-id="f7d4a-130">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="f7d4a-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="f7d4a-131">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="f7d4a-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="f7d4a-132">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="f7d4a-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="f7d4a-133">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="f7d4a-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)


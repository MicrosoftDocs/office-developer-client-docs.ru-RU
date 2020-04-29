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
ms.openlocfilehash: 61683534504b7451f126591af149d11306cff1bd
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357864"
---
# <a name="pidtagrtfsyncprefixcount-canonical-property"></a><span data-ttu-id="f3260-103">Каноническое свойство PidTagRtfSyncPrefixCount</span><span class="sxs-lookup"><span data-stu-id="f3260-103">PidTagRtfSyncPrefixCount Canonical Property</span></span>

  
  
<span data-ttu-id="f3260-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f3260-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f3260-105">Содержит количество игнорируемых символов, которые отображаются перед значащими символами сообщения.</span><span class="sxs-lookup"><span data-stu-id="f3260-105">Contains a count of the ignorable characters that appear before the significant characters of the message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="f3260-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="f3260-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="f3260-107">PR_RTF_SYNC_PREFIX_COUNT</span><span class="sxs-lookup"><span data-stu-id="f3260-107">PR_RTF_SYNC_PREFIX_COUNT</span></span>  <br/> |
|<span data-ttu-id="f3260-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="f3260-108">Identifier:</span></span>  <br/> |<span data-ttu-id="f3260-109">0x1010</span><span class="sxs-lookup"><span data-stu-id="f3260-109">0x1010</span></span>  <br/> |
|<span data-ttu-id="f3260-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="f3260-110">Data type:</span></span>  <br/> |<span data-ttu-id="f3260-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="f3260-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="f3260-112">Область:</span><span class="sxs-lookup"><span data-stu-id="f3260-112">Area:</span></span>  <br/> |<span data-ttu-id="f3260-113">Сообщение MAPI</span><span class="sxs-lookup"><span data-stu-id="f3260-113">MAPI message</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f3260-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="f3260-114">Remarks</span></span>

<span data-ttu-id="f3260-115">Количество символов префикса не включает пробелы.</span><span class="sxs-lookup"><span data-stu-id="f3260-115">The count of prefix characters does not include white space.</span></span>
  
<span data-ttu-id="f3260-116">Это свойство является дополнительным свойством в формате RTF.</span><span class="sxs-lookup"><span data-stu-id="f3260-116">This property is a Rich Text Format (RTF) auxiliary property.</span></span> <span data-ttu-id="f3260-117">Дополнительные свойства RTF используются функцией [ртфсинк](rtfsync.md) и не предназначены для непосредственного использования клиентскими приложениями.</span><span class="sxs-lookup"><span data-stu-id="f3260-117">RTF auxiliary properties are used by the [RTFSync](rtfsync.md) function and are not intended to be used directly by client applications.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="f3260-118">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="f3260-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="f3260-119">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="f3260-119">Protocol specifications</span></span>

<span data-ttu-id="f3260-120">[[MS — ОКСПРОПС]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f3260-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="f3260-121">Содержит ссылки на соответствующие спецификации протоколов Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="f3260-121">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="f3260-122">[[MS — ОКСТНЕФ]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f3260-122">[[MS-OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="f3260-123">Кодирует и декодирует объекты сообщений и вложений в эффективное потоковое представление.</span><span class="sxs-lookup"><span data-stu-id="f3260-123">Encodes and decodes message and attachment objects to an efficient stream representation.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="f3260-124">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="f3260-124">Header files</span></span>

<span data-ttu-id="f3260-125">MAPIDEFS. h</span><span class="sxs-lookup"><span data-stu-id="f3260-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="f3260-126">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="f3260-126">Provides data type definitions.</span></span>
    
<span data-ttu-id="f3260-127">Мапитагс. h</span><span class="sxs-lookup"><span data-stu-id="f3260-127">Mapitags.h</span></span>
  
> <span data-ttu-id="f3260-128">Содержит определения свойств, перечисленных как альтернативные имена.</span><span class="sxs-lookup"><span data-stu-id="f3260-128">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="f3260-129">См. также</span><span class="sxs-lookup"><span data-stu-id="f3260-129">See also</span></span>



[<span data-ttu-id="f3260-130">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="f3260-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="f3260-131">Каноническое свойство MAPI</span><span class="sxs-lookup"><span data-stu-id="f3260-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="f3260-132">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="f3260-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="f3260-133">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="f3260-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)


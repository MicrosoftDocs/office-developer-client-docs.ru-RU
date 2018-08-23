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
ms.openlocfilehash: 32344d81d929b0f78a5f883cd9860d838ba25bb8
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22568443"
---
# <a name="pidtagrtfsyncprefixcount-canonical-property"></a><span data-ttu-id="cdc0c-103">Каноническое свойство PidTagRtfSyncPrefixCount</span><span class="sxs-lookup"><span data-stu-id="cdc0c-103">PidTagRtfSyncPrefixCount Canonical Property</span></span>

  
  
<span data-ttu-id="cdc0c-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="cdc0c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="cdc0c-105">Содержит число допускающие игнорирование символы, отображаемые перед значительные символов сообщения.</span><span class="sxs-lookup"><span data-stu-id="cdc0c-105">Contains a count of the ignorable characters that appear before the significant characters of the message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="cdc0c-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="cdc0c-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="cdc0c-107">PR_RTF_SYNC_PREFIX_COUNT</span><span class="sxs-lookup"><span data-stu-id="cdc0c-107">PR_RTF_SYNC_PREFIX_COUNT</span></span>  <br/> |
|<span data-ttu-id="cdc0c-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="cdc0c-108">Identifier:</span></span>  <br/> |<span data-ttu-id="cdc0c-109">0x1010</span><span class="sxs-lookup"><span data-stu-id="cdc0c-109">0x1010</span></span>  <br/> |
|<span data-ttu-id="cdc0c-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="cdc0c-110">Data type:</span></span>  <br/> |<span data-ttu-id="cdc0c-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="cdc0c-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="cdc0c-112">Область:</span><span class="sxs-lookup"><span data-stu-id="cdc0c-112">Area:</span></span>  <br/> |<span data-ttu-id="cdc0c-113">Сообщение MAPI</span><span class="sxs-lookup"><span data-stu-id="cdc0c-113">MAPI message</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="cdc0c-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="cdc0c-114">Remarks</span></span>

<span data-ttu-id="cdc0c-115">Количество символов префикса не включает пробелы.</span><span class="sxs-lookup"><span data-stu-id="cdc0c-115">The count of prefix characters does not include white space.</span></span>
  
<span data-ttu-id="cdc0c-116">Это свойство является свойством дополнительный форматированный текст (RTF).</span><span class="sxs-lookup"><span data-stu-id="cdc0c-116">This property is a Rich Text Format (RTF) auxiliary property.</span></span> <span data-ttu-id="cdc0c-117">Дополнительные свойства RTF используется функцией [RTFSync](rtfsync.md) и не предназначен для непосредственного использования в клиентских приложениях.</span><span class="sxs-lookup"><span data-stu-id="cdc0c-117">RTF auxiliary properties are used by the [RTFSync](rtfsync.md) function and are not intended to be used directly by client applications.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="cdc0c-118">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="cdc0c-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="cdc0c-119">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="cdc0c-119">Protocol specifications</span></span>

<span data-ttu-id="cdc0c-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="cdc0c-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="cdc0c-121">Содержит ссылки на связанные спецификаций протокола Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="cdc0c-121">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="cdc0c-122">[[MS-OXTNEF]](http://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="cdc0c-122">[[MS-OXTNEF]](http://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="cdc0c-123">Кодирует и декодирует объекты сообщения и вложения в представление эффективным потока.</span><span class="sxs-lookup"><span data-stu-id="cdc0c-123">Encodes and decodes message and attachment objects to an efficient stream representation.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="cdc0c-124">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="cdc0c-124">Header files</span></span>

<span data-ttu-id="cdc0c-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="cdc0c-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="cdc0c-126">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="cdc0c-126">Provides data type definitions.</span></span>
    
<span data-ttu-id="cdc0c-127">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="cdc0c-127">Mapitags.h</span></span>
  
> <span data-ttu-id="cdc0c-128">Содержит определения свойства в списке альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="cdc0c-128">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="cdc0c-129">См. также</span><span class="sxs-lookup"><span data-stu-id="cdc0c-129">See also</span></span>



[<span data-ttu-id="cdc0c-130">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="cdc0c-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="cdc0c-131">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="cdc0c-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="cdc0c-132">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="cdc0c-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="cdc0c-133">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="cdc0c-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)


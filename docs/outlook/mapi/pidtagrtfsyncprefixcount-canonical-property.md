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
# <a name="pidtagrtfsyncprefixcount-canonical-property"></a><span data-ttu-id="98b1b-103">Каноническое свойство PidTagRtfSyncPrefixCount</span><span class="sxs-lookup"><span data-stu-id="98b1b-103">PidTagRtfSyncPrefixCount Canonical Property</span></span>

  
  
<span data-ttu-id="98b1b-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="98b1b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="98b1b-105">Содержит количество игнорируемых символов, которые отображаются перед значительными символами сообщения.</span><span class="sxs-lookup"><span data-stu-id="98b1b-105">Contains a count of the ignorable characters that appear before the significant characters of the message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="98b1b-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="98b1b-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="98b1b-107">PR_RTF_SYNC_PREFIX_COUNT</span><span class="sxs-lookup"><span data-stu-id="98b1b-107">PR_RTF_SYNC_PREFIX_COUNT</span></span>  <br/> |
|<span data-ttu-id="98b1b-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="98b1b-108">Identifier:</span></span>  <br/> |<span data-ttu-id="98b1b-109">0x1010</span><span class="sxs-lookup"><span data-stu-id="98b1b-109">0x1010</span></span>  <br/> |
|<span data-ttu-id="98b1b-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="98b1b-110">Data type:</span></span>  <br/> |<span data-ttu-id="98b1b-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="98b1b-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="98b1b-112">Область:</span><span class="sxs-lookup"><span data-stu-id="98b1b-112">Area:</span></span>  <br/> |<span data-ttu-id="98b1b-113">Сообщение MAPI</span><span class="sxs-lookup"><span data-stu-id="98b1b-113">MAPI message</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="98b1b-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="98b1b-114">Remarks</span></span>

<span data-ttu-id="98b1b-115">Количество символов префикса не включает пробел.</span><span class="sxs-lookup"><span data-stu-id="98b1b-115">The count of prefix characters does not include white space.</span></span>
  
<span data-ttu-id="98b1b-116">Это свойство является вспомогательным свойством RTF.</span><span class="sxs-lookup"><span data-stu-id="98b1b-116">This property is a Rich Text Format (RTF) auxiliary property.</span></span> <span data-ttu-id="98b1b-117">Вспомогательные свойства RTF используются функцией [RTFSync](rtfsync.md) и не предназначены для непосредственного использования клиентских приложений.</span><span class="sxs-lookup"><span data-stu-id="98b1b-117">RTF auxiliary properties are used by the [RTFSync](rtfsync.md) function and are not intended to be used directly by client applications.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="98b1b-118">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="98b1b-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="98b1b-119">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="98b1b-119">Protocol specifications</span></span>

<span data-ttu-id="98b1b-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="98b1b-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="98b1b-121">Содержит ссылки на связанные Exchange Server протоколы.</span><span class="sxs-lookup"><span data-stu-id="98b1b-121">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="98b1b-122">[[MS-OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="98b1b-122">[[MS-OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="98b1b-123">Кодирует и декодирует объекты сообщений и вложений в эффективное представление потока.</span><span class="sxs-lookup"><span data-stu-id="98b1b-123">Encodes and decodes message and attachment objects to an efficient stream representation.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="98b1b-124">Файлы заголовок</span><span class="sxs-lookup"><span data-stu-id="98b1b-124">Header files</span></span>

<span data-ttu-id="98b1b-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="98b1b-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="98b1b-126">Предоставляет определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="98b1b-126">Provides data type definitions.</span></span>
    
<span data-ttu-id="98b1b-127">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="98b1b-127">Mapitags.h</span></span>
  
> <span data-ttu-id="98b1b-128">Содержит определения свойств, перечисленных в качестве альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="98b1b-128">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="98b1b-129">См. также</span><span class="sxs-lookup"><span data-stu-id="98b1b-129">See also</span></span>



[<span data-ttu-id="98b1b-130">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="98b1b-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="98b1b-131">Канонические свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="98b1b-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="98b1b-132">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="98b1b-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="98b1b-133">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="98b1b-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)


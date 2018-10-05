---
title: Каноническое свойство PidTagRtfSyncBodyTag
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagRtfSyncBodyTag
api_type:
- COM
ms.assetid: 2dab5018-4214-4162-93bc-e5565f3ac24c
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 24ef1d4e3e936426aea8216119e8ada9f6122e95
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25387512"
---
# <a name="pidtagrtfsyncbodytag-canonical-property"></a><span data-ttu-id="9847d-103">Каноническое свойство PidTagRtfSyncBodyTag</span><span class="sxs-lookup"><span data-stu-id="9847d-103">PidTagRtfSyncBodyTag Canonical Property</span></span>

  
  
<span data-ttu-id="9847d-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9847d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9847d-105">Содержит значительные символов, которые отображаются в начале текста сообщения.</span><span class="sxs-lookup"><span data-stu-id="9847d-105">Contains significant characters that appear at the beginning of the message text.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="9847d-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="9847d-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="9847d-107">PR_RTF_SYNC_BODY_TAG, PR_RTF_SYNC_BODY_TAG_A, PR_RTF_SYNC_BODY_TAG_W</span><span class="sxs-lookup"><span data-stu-id="9847d-107">PR_RTF_SYNC_BODY_TAG, PR_RTF_SYNC_BODY_TAG_A, PR_RTF_SYNC_BODY_TAG_W</span></span>  <br/> |
|<span data-ttu-id="9847d-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="9847d-108">Identifier:</span></span>  <br/> |<span data-ttu-id="9847d-109">0x1008</span><span class="sxs-lookup"><span data-stu-id="9847d-109">0x1008</span></span>  <br/> |
|<span data-ttu-id="9847d-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="9847d-110">Data type:</span></span>  <br/> |<span data-ttu-id="9847d-111">PT_STRING8 PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="9847d-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="9847d-112">Область:</span><span class="sxs-lookup"><span data-stu-id="9847d-112">Area:</span></span>  <br/> |<span data-ttu-id="9847d-113">Сообщение MAPI</span><span class="sxs-lookup"><span data-stu-id="9847d-113">MAPI message</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="9847d-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="9847d-114">Remarks</span></span>

<span data-ttu-id="9847d-115">Функция [RTFSync](rtfsync.md) используется тег текст в начало текста сообщения.</span><span class="sxs-lookup"><span data-stu-id="9847d-115">The [RTFSync](rtfsync.md) function uses the text tag to indicate the beginning of the message text.</span></span> <span data-ttu-id="9847d-116">При изменении текста тега используется для поиска в начало текста.</span><span class="sxs-lookup"><span data-stu-id="9847d-116">When the text is modified, the tag is used to find the beginning of the previous text.</span></span> 
  
<span data-ttu-id="9847d-117">Эти свойства доступны дополнительные свойства текст в формате RTF.</span><span class="sxs-lookup"><span data-stu-id="9847d-117">These properties are Rich Text Format auxiliary properties.</span></span> <span data-ttu-id="9847d-118">Они используются функцией **RTFSync** и не предназначен для непосредственного использования в клиентских приложениях.</span><span class="sxs-lookup"><span data-stu-id="9847d-118">They are used by the **RTFSync** function and are not intended to be used directly by client applications.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="9847d-119">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="9847d-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="9847d-120">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="9847d-120">Protocol specifications</span></span>

<span data-ttu-id="9847d-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="9847d-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="9847d-122">Содержит ссылки на связанные спецификаций протокола Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="9847d-122">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="9847d-123">[[MS-OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="9847d-123">[[MS-OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="9847d-124">Кодирует и декодирует объекты сообщения и вложения в представление эффективным потока.</span><span class="sxs-lookup"><span data-stu-id="9847d-124">Encodes and decodes message and attachment objects to an efficient stream representation.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="9847d-125">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="9847d-125">Header files</span></span>

<span data-ttu-id="9847d-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="9847d-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="9847d-127">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="9847d-127">Provides data type definitions.</span></span>
    
<span data-ttu-id="9847d-128">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="9847d-128">Mapitags.h</span></span>
  
> <span data-ttu-id="9847d-129">Содержит определения свойства в списке альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="9847d-129">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="9847d-130">См. также</span><span class="sxs-lookup"><span data-stu-id="9847d-130">See also</span></span>



[<span data-ttu-id="9847d-131">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="9847d-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="9847d-132">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="9847d-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="9847d-133">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="9847d-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="9847d-134">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="9847d-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)


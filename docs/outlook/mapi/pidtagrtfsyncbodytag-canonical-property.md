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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32331180"
---
# <a name="pidtagrtfsyncbodytag-canonical-property"></a><span data-ttu-id="1bbac-103">Каноническое свойство PidTagRtfSyncBodyTag</span><span class="sxs-lookup"><span data-stu-id="1bbac-103">PidTagRtfSyncBodyTag Canonical Property</span></span>

  
  
<span data-ttu-id="1bbac-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1bbac-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1bbac-105">Содержит значительные символы, которые отображаются в начале текста сообщения.</span><span class="sxs-lookup"><span data-stu-id="1bbac-105">Contains significant characters that appear at the beginning of the message text.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="1bbac-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="1bbac-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="1bbac-107">PR_RTF_SYNC_BODY_TAG, PR_RTF_SYNC_BODY_TAG_A, PR_RTF_SYNC_BODY_TAG_W</span><span class="sxs-lookup"><span data-stu-id="1bbac-107">PR_RTF_SYNC_BODY_TAG, PR_RTF_SYNC_BODY_TAG_A, PR_RTF_SYNC_BODY_TAG_W</span></span>  <br/> |
|<span data-ttu-id="1bbac-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="1bbac-108">Identifier:</span></span>  <br/> |<span data-ttu-id="1bbac-109">0x1008</span><span class="sxs-lookup"><span data-stu-id="1bbac-109">0x1008</span></span>  <br/> |
|<span data-ttu-id="1bbac-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="1bbac-110">Data type:</span></span>  <br/> |<span data-ttu-id="1bbac-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="1bbac-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="1bbac-112">Область:</span><span class="sxs-lookup"><span data-stu-id="1bbac-112">Area:</span></span>  <br/> |<span data-ttu-id="1bbac-113">Сообщение MAPI</span><span class="sxs-lookup"><span data-stu-id="1bbac-113">MAPI message</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="1bbac-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="1bbac-114">Remarks</span></span>

<span data-ttu-id="1bbac-115">Функция [RTFSync использует](rtfsync.md) текстовый тег, чтобы указать начало текста сообщения.</span><span class="sxs-lookup"><span data-stu-id="1bbac-115">The [RTFSync](rtfsync.md) function uses the text tag to indicate the beginning of the message text.</span></span> <span data-ttu-id="1bbac-116">При внесении изменений в текст тег используется для поиска начала предыдущего текста.</span><span class="sxs-lookup"><span data-stu-id="1bbac-116">When the text is modified, the tag is used to find the beginning of the previous text.</span></span> 
  
<span data-ttu-id="1bbac-117">Эти свойства являются вспомогательными свойствами формата rich Text.</span><span class="sxs-lookup"><span data-stu-id="1bbac-117">These properties are Rich Text Format auxiliary properties.</span></span> <span data-ttu-id="1bbac-118">Они используются функцией **RTFSync** и не предназначены для непосредственного использования клиентских приложений.</span><span class="sxs-lookup"><span data-stu-id="1bbac-118">They are used by the **RTFSync** function and are not intended to be used directly by client applications.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="1bbac-119">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="1bbac-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="1bbac-120">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="1bbac-120">Protocol specifications</span></span>

<span data-ttu-id="1bbac-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="1bbac-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="1bbac-122">Содержит ссылки на связанные Exchange Server протоколы.</span><span class="sxs-lookup"><span data-stu-id="1bbac-122">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="1bbac-123">[[MS-OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="1bbac-123">[[MS-OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="1bbac-124">Кодирует и декодирует объекты сообщений и вложений в эффективное представление потока.</span><span class="sxs-lookup"><span data-stu-id="1bbac-124">Encodes and decodes message and attachment objects to an efficient stream representation.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="1bbac-125">Файлы заголовки</span><span class="sxs-lookup"><span data-stu-id="1bbac-125">Header files</span></span>

<span data-ttu-id="1bbac-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="1bbac-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="1bbac-127">Предоставляет определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="1bbac-127">Provides data type definitions.</span></span>
    
<span data-ttu-id="1bbac-128">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="1bbac-128">Mapitags.h</span></span>
  
> <span data-ttu-id="1bbac-129">Содержит определения свойств, перечисленных в качестве альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="1bbac-129">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="1bbac-130">См. также</span><span class="sxs-lookup"><span data-stu-id="1bbac-130">See also</span></span>



[<span data-ttu-id="1bbac-131">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="1bbac-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="1bbac-132">Канонические свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="1bbac-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="1bbac-133">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="1bbac-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="1bbac-134">Сопоставление имен MAPI с каноническими именами свойств</span><span class="sxs-lookup"><span data-stu-id="1bbac-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)


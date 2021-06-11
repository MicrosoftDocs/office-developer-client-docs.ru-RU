---
title: Каноническое свойство PidTagJunkAddRecipientsToSafeSendersList
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagJunkAddRecipientsToSafeSendersList
api_type:
- HeaderDef
ms.assetid: 78543caa-e6ec-4ac7-bfdd-70c56f8fd955
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 3a87beaa3873b5ccb449e5b1497262bad5bf1497
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32282370"
---
# <a name="pidtagjunkaddrecipientstosafesenderslist-canonical-property"></a><span data-ttu-id="5f70d-103">Каноническое свойство PidTagJunkAddRecipientsToSafeSendersList</span><span class="sxs-lookup"><span data-stu-id="5f70d-103">PidTagJunkAddRecipientsToSafeSendersList Canonical Property</span></span>

  
  
<span data-ttu-id="5f70d-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5f70d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5f70d-105">Указывает, следует ли добавлять получателей почты в список безопасных отправителей.</span><span class="sxs-lookup"><span data-stu-id="5f70d-105">Indicates whether or not the mail recipients are to be added to the safe senders list.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="5f70d-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="5f70d-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="5f70d-107">PR_JUNK_ADD_RECIPS_TO_SSL</span><span class="sxs-lookup"><span data-stu-id="5f70d-107">PR_JUNK_ADD_RECIPS_TO_SSL</span></span>  <br/> |
|<span data-ttu-id="5f70d-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="5f70d-108">Identifier:</span></span>  <br/> |<span data-ttu-id="5f70d-109">0x6103</span><span class="sxs-lookup"><span data-stu-id="5f70d-109">0x6103</span></span>  <br/> |
|<span data-ttu-id="5f70d-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="5f70d-110">Data type:</span></span>  <br/> |<span data-ttu-id="5f70d-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="5f70d-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="5f70d-112">Область:</span><span class="sxs-lookup"><span data-stu-id="5f70d-112">Area:</span></span>  <br/> |<span data-ttu-id="5f70d-113">Спам</span><span class="sxs-lookup"><span data-stu-id="5f70d-113">Spam</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="5f70d-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="5f70d-114">Remarks</span></span>

<span data-ttu-id="5f70d-115">Если это свойство присутствует, необходимо установить 0 или 1.</span><span class="sxs-lookup"><span data-stu-id="5f70d-115">If present, this property must be set to 0 or 1.</span></span> <span data-ttu-id="5f70d-116">Значение 1 указывает, что получатели почты должны быть добавлены в список безопасных отправителей.</span><span class="sxs-lookup"><span data-stu-id="5f70d-116">A value of 1 indicates that the mail recipients are to be added to the safe senders list.</span></span> <span data-ttu-id="5f70d-117">Значение 0 указывает, что получатели почты не должны добавляться в список безопасных отправителей.</span><span class="sxs-lookup"><span data-stu-id="5f70d-117">A value of 0 indicates that the mail recipients are not to be added to the safe senders list.</span></span>
  
<span data-ttu-id="5f70d-118">Если это свойство имеет значение 1, smTP-адреса получателей электронной почты должны быть добавлены в пункт доверенных отправителей условия правила нежелательной почты.</span><span class="sxs-lookup"><span data-stu-id="5f70d-118">If this property is present with a value of 1, the SMTP addresses of the email recipients must be added to trusted senders clause of the Junk E-Mail Rule condition.</span></span> <span data-ttu-id="5f70d-119">Если это свойство 0, никаких действий не требуется.</span><span class="sxs-lookup"><span data-stu-id="5f70d-119">If this property is 0, no action is required.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="5f70d-120">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="5f70d-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="5f70d-121">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="5f70d-121">Protocol specifications</span></span>

<span data-ttu-id="5f70d-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="5f70d-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="5f70d-123">Содержит ссылки на связанные Exchange Server протоколы.</span><span class="sxs-lookup"><span data-stu-id="5f70d-123">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="5f70d-124">[[MS-OXCSPAM]](https://msdn.microsoft.com/library/522f8587-4aed-4cd6-831b-40bd87862189%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="5f70d-124">[[MS-OXCSPAM]](https://msdn.microsoft.com/library/522f8587-4aed-4cd6-831b-40bd87862189%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="5f70d-125">Включает обработку списков разрешить или блокировать и определение нежелательных сообщений электронной почты.</span><span class="sxs-lookup"><span data-stu-id="5f70d-125">Enables the handling of allow/block lists and the determination of junk email messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="5f70d-126">Файлы заголовки</span><span class="sxs-lookup"><span data-stu-id="5f70d-126">Header files</span></span>

<span data-ttu-id="5f70d-127">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="5f70d-127">Mapidefs.h</span></span>
  
> <span data-ttu-id="5f70d-128">Предоставляет определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="5f70d-128">Provides data type definitions.</span></span>
    
<span data-ttu-id="5f70d-129">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="5f70d-129">Mapitags.h</span></span>
  
> <span data-ttu-id="5f70d-130">Содержит определения свойств, перечисленных в качестве альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="5f70d-130">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="5f70d-131">См. также</span><span class="sxs-lookup"><span data-stu-id="5f70d-131">See also</span></span>



[<span data-ttu-id="5f70d-132">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="5f70d-132">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="5f70d-133">Канонические свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="5f70d-133">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="5f70d-134">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="5f70d-134">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="5f70d-135">Сопоставление имен MAPI с каноническими именами свойств</span><span class="sxs-lookup"><span data-stu-id="5f70d-135">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)


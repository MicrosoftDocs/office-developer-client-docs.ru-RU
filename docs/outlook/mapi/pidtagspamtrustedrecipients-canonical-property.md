---
title: Каноническое свойство PidTagSpamTrustedRecipients
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 59f43316-3ff6-4ed0-bc29-b31039192b08
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 3a852ff8b4e3ff0df59c4c84f53802fa29d63a80
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19811922"
---
# <a name="pidtagspamtrustedrecipients-canonical-property"></a><span data-ttu-id="1f56f-103">Каноническое свойство PidTagSpamTrustedRecipients</span><span class="sxs-lookup"><span data-stu-id="1f56f-103">PidTagSpamTrustedRecipients Canonical Property</span></span>
 
<span data-ttu-id="1f56f-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="1f56f-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="1f56f-105">Содержит список адресов электронной почты и доменов, которые представляют надежных получателей, разделенных точкой с запятой.</span><span class="sxs-lookup"><span data-stu-id="1f56f-105">Contains a semicolon-delimited list of email addresses and domains that represent the trusted recipients.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="1f56f-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="1f56f-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="1f56f-107">PR_SPAM_TRUSTED_RECIPIENTS_W</span><span class="sxs-lookup"><span data-stu-id="1f56f-107">PR_SPAM_TRUSTED_RECIPIENTS_W</span></span>  <br/> |
|<span data-ttu-id="1f56f-108">Длинный идентификатор (КРЫШКА):</span><span class="sxs-lookup"><span data-stu-id="1f56f-108">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="1f56f-109">0x0419</span><span class="sxs-lookup"><span data-stu-id="1f56f-109">0x0419</span></span>  <br/> |
|<span data-ttu-id="1f56f-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="1f56f-110">Data type:</span></span>  <br/> |<span data-ttu-id="1f56f-111">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="1f56f-111">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="1f56f-112">Область:</span><span class="sxs-lookup"><span data-stu-id="1f56f-112">Area:</span></span>  <br/> |<span data-ttu-id="1f56f-113">Нежелательной почты</span><span class="sxs-lookup"><span data-stu-id="1f56f-113">Spam</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="1f56f-114">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="1f56f-114">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="1f56f-115">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="1f56f-115">Protocol specifications</span></span>

<span data-ttu-id="1f56f-116">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="1f56f-116">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="1f56f-117">Содержит определения набора свойств и ссылки на связанные спецификаций протокола Microsoft Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="1f56f-117">Provides property set definitions and references to related Microsoft Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="1f56f-118">[[MS-OXCSPAM]](http://msdn.microsoft.com/library/522f8587-4aed-4cd6-831b-40bd87862189%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="1f56f-118">[[MS-OXCSPAM]](http://msdn.microsoft.com/library/522f8587-4aed-4cd6-831b-40bd87862189%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="1f56f-119">Включает обработку списки разрешенных и запрещенных и определение нежелательных сообщений электронной почты.</span><span class="sxs-lookup"><span data-stu-id="1f56f-119">Enables the handling of allow/block lists and the determination of junk email messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="1f56f-120">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="1f56f-120">Header files</span></span>

<span data-ttu-id="1f56f-121">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="1f56f-121">Mapidefs.h</span></span>
  
> <span data-ttu-id="1f56f-122">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="1f56f-122">Provides data type definitions.</span></span>
    
<span data-ttu-id="1f56f-123">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="1f56f-123">Mapitags.h</span></span>
  
> <span data-ttu-id="1f56f-124">Содержит определения свойства, указанные как альтернативные имена.</span><span class="sxs-lookup"><span data-stu-id="1f56f-124">Contains definitions of properties that are listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="1f56f-125">См. также</span><span class="sxs-lookup"><span data-stu-id="1f56f-125">See also</span></span>

- [<span data-ttu-id="1f56f-126">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="1f56f-126">MAPI Properties</span></span>](mapi-properties.md) 
- [<span data-ttu-id="1f56f-127">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="1f56f-127">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)  
- [<span data-ttu-id="1f56f-128">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="1f56f-128">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)  
- [<span data-ttu-id="1f56f-129">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="1f56f-129">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)


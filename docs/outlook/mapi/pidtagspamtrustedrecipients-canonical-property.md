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
ms.openlocfilehash: 521bdb280776be28d3526471888834bbd7da0b9f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359453"
---
# <a name="pidtagspamtrustedrecipients-canonical-property"></a><span data-ttu-id="0ca4d-103">Каноническое свойство PidTagSpamTrustedRecipients</span><span class="sxs-lookup"><span data-stu-id="0ca4d-103">PidTagSpamTrustedRecipients Canonical Property</span></span>
 
<span data-ttu-id="0ca4d-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0ca4d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0ca4d-105">Содержит список адресов и доменов электронной почты, которые представляют доверенных получателей.</span><span class="sxs-lookup"><span data-stu-id="0ca4d-105">Contains a semicolon-delimited list of email addresses and domains that represent the trusted recipients.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="0ca4d-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="0ca4d-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="0ca4d-107">PR_SPAM_TRUSTED_RECIPIENTS_W</span><span class="sxs-lookup"><span data-stu-id="0ca4d-107">PR_SPAM_TRUSTED_RECIPIENTS_W</span></span>  <br/> |
|<span data-ttu-id="0ca4d-108">Long ID (LID):</span><span class="sxs-lookup"><span data-stu-id="0ca4d-108">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="0ca4d-109">0x0419</span><span class="sxs-lookup"><span data-stu-id="0ca4d-109">0x0419</span></span>  <br/> |
|<span data-ttu-id="0ca4d-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="0ca4d-110">Data type:</span></span>  <br/> |<span data-ttu-id="0ca4d-111">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="0ca4d-111">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="0ca4d-112">Область:</span><span class="sxs-lookup"><span data-stu-id="0ca4d-112">Area:</span></span>  <br/> |<span data-ttu-id="0ca4d-113">Спам</span><span class="sxs-lookup"><span data-stu-id="0ca4d-113">Spam</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="0ca4d-114">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="0ca4d-114">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="0ca4d-115">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="0ca4d-115">Protocol specifications</span></span>

<span data-ttu-id="0ca4d-116">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="0ca4d-116">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="0ca4d-117">Предоставляет определения набора свойств и ссылки на связанные Microsoft Exchange Server протоколы.</span><span class="sxs-lookup"><span data-stu-id="0ca4d-117">Provides property set definitions and references to related Microsoft Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="0ca4d-118">[[MS-OXCSPAM]](https://msdn.microsoft.com/library/522f8587-4aed-4cd6-831b-40bd87862189%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="0ca4d-118">[[MS-OXCSPAM]](https://msdn.microsoft.com/library/522f8587-4aed-4cd6-831b-40bd87862189%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="0ca4d-119">Включает обработку списков разрешить или блокировать и определение нежелательных сообщений электронной почты.</span><span class="sxs-lookup"><span data-stu-id="0ca4d-119">Enables the handling of allow/block lists and the determination of junk email messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="0ca4d-120">Файлы заголовки</span><span class="sxs-lookup"><span data-stu-id="0ca4d-120">Header files</span></span>

<span data-ttu-id="0ca4d-121">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="0ca4d-121">Mapidefs.h</span></span>
  
> <span data-ttu-id="0ca4d-122">Предоставляет определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="0ca4d-122">Provides data type definitions.</span></span>
    
<span data-ttu-id="0ca4d-123">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="0ca4d-123">Mapitags.h</span></span>
  
> <span data-ttu-id="0ca4d-124">Содержит определения свойств, перечисленных в качестве альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="0ca4d-124">Contains definitions of properties that are listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="0ca4d-125">См. также</span><span class="sxs-lookup"><span data-stu-id="0ca4d-125">See also</span></span>

- [<span data-ttu-id="0ca4d-126">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="0ca4d-126">MAPI Properties</span></span>](mapi-properties.md) 
- [<span data-ttu-id="0ca4d-127">Канонические свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="0ca4d-127">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)  
- [<span data-ttu-id="0ca4d-128">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="0ca4d-128">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)  
- [<span data-ttu-id="0ca4d-129">Сопоставление имен MAPI с каноническими именами свойств</span><span class="sxs-lookup"><span data-stu-id="0ca4d-129">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)


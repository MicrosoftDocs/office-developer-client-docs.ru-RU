---
title: Каноническое свойство PidTagOriginalAuthorName
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagOriginalAuthorNam
api_type:
- COM
ms.assetid: beb23742-d844-4d90-9b13-1ad376d4206c
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 4b2f47f503caa32a1bdcd287e2fa5e894d667573
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19811426"
---
# <a name="pidtagoriginalauthorname-canonical-property"></a><span data-ttu-id="be51e-103">Каноническое свойство PidTagOriginalAuthorName</span><span class="sxs-lookup"><span data-stu-id="be51e-103">PidTagOriginalAuthorName Canonical Property</span></span>

  
  
<span data-ttu-id="be51e-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="be51e-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="be51e-105">Содержит отображаемое имя автора первая версия сообщения, то есть, сообщение перед пересылку и ответ.</span><span class="sxs-lookup"><span data-stu-id="be51e-105">Contains the display name of the author of the first version of a message, that is, the message before being forwarded or replied to.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="be51e-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="be51e-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="be51e-107">PR_ORIGINAL_AUTHOR_NAME, PR_ORIGINAL_AUTHOR_NAME_A, PR_ORIGINAL_AUTHOR_NAME_W</span><span class="sxs-lookup"><span data-stu-id="be51e-107">PR_ORIGINAL_AUTHOR_NAME, PR_ORIGINAL_AUTHOR_NAME_A, PR_ORIGINAL_AUTHOR_NAME_W</span></span>  <br/> |
|<span data-ttu-id="be51e-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="be51e-108">Identifier:</span></span>  <br/> |<span data-ttu-id="be51e-109">0x004D</span><span class="sxs-lookup"><span data-stu-id="be51e-109">0x004D</span></span>  <br/> |
|<span data-ttu-id="be51e-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="be51e-110">Data type:</span></span>  <br/> |<span data-ttu-id="be51e-111">PT_UNICODE PT_STRING8</span><span class="sxs-lookup"><span data-stu-id="be51e-111">PT_UNICODE, PT_STRING8</span></span>  <br/> |
|<span data-ttu-id="be51e-112">Область:</span><span class="sxs-lookup"><span data-stu-id="be51e-112">Area:</span></span>  <br/> |<span data-ttu-id="be51e-113">Электронная почта</span><span class="sxs-lookup"><span data-stu-id="be51e-113">Email</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="be51e-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="be51e-114">Remarks</span></span>

<span data-ttu-id="be51e-115">Эти свойства являются примерами свойства адреса для автора сообщения.</span><span class="sxs-lookup"><span data-stu-id="be51e-115">These properties are examples of the address properties for the author of a message.</span></span> <span data-ttu-id="be51e-116">В первой отправки сообщения в клиентском приложении необходимо задать эти свойства значение **PR_SENDER_NAME** ([PidTagSenderName](pidtagsendername-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="be51e-116">At first submission of the message, the client application should set these properties to the value of **PR_SENDER_NAME** ([PidTagSenderName](pidtagsendername-canonical-property.md)).</span></span> <span data-ttu-id="be51e-117">Никогда не изменяется при сообщение будет переслано или ответ.</span><span class="sxs-lookup"><span data-stu-id="be51e-117">It is never changed when the message is forwarded or replied to.</span></span>
  
<span data-ttu-id="be51e-118">Исходные свойства author разрешить для хранения данных из других доменов обмена мгновенными сообщениями.</span><span class="sxs-lookup"><span data-stu-id="be51e-118">The original author properties allow for preservation of information from outside the local messaging domain.</span></span> <span data-ttu-id="be51e-119">При получении сообщения из другой домен обмена мгновенными сообщениями, например, из Интернета, эти свойства предусмотрена возможность убедитесь, что исходные данные не потеряны.</span><span class="sxs-lookup"><span data-stu-id="be51e-119">When a message arrives from another messaging domain, such as from the Internet, these properties provide a way to ensure that original information is not lost.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="be51e-120">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="be51e-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="be51e-121">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="be51e-121">Protocol specifications</span></span>

<span data-ttu-id="be51e-122">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="be51e-122">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="be51e-123">Содержит ссылки на связанные спецификаций протокола Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="be51e-123">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="be51e-124">[[MS-OXCICAL]](http://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="be51e-124">[[MS-OXCICAL]](http://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="be51e-125">Преобразование между IETF RFC2445, RFC2446 и RFC2447 и встречи и собрания объекты.</span><span class="sxs-lookup"><span data-stu-id="be51e-125">Converts between IETF RFC2445, RFC2446, and RFC2447, and appointment and meeting objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="be51e-126">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="be51e-126">Header files</span></span>

<span data-ttu-id="be51e-127">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="be51e-127">Mapidefs.h</span></span>
  
> <span data-ttu-id="be51e-128">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="be51e-128">Provides data type definitions.</span></span>
    
<span data-ttu-id="be51e-129">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="be51e-129">Mapitags.h</span></span>
  
> <span data-ttu-id="be51e-130">Содержит определения свойства в списке альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="be51e-130">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="be51e-131">См. также</span><span class="sxs-lookup"><span data-stu-id="be51e-131">See also</span></span>



[<span data-ttu-id="be51e-132">Каноническое свойство PidTagDisplayName</span><span class="sxs-lookup"><span data-stu-id="be51e-132">PidTagDisplayName Canonical Property</span></span>](pidtagdisplayname-canonical-property.md)


[<span data-ttu-id="be51e-133">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="be51e-133">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="be51e-134">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="be51e-134">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="be51e-135">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="be51e-135">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="be51e-136">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="be51e-136">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)


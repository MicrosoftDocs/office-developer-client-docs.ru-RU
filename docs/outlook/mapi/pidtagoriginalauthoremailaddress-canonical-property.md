---
title: Каноническое свойство PidTagOriginalAuthorEmailAddress
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagOriginalAuthorEmailAddress
api_type:
- COM
ms.assetid: 67cda756-ba71-4f29-a601-55359e44d93b
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 1954e1760fead9cbe13f0f2394f8095cab7f26ce
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19811435"
---
# <a name="pidtagoriginalauthoremailaddress-canonical-property"></a><span data-ttu-id="97471-103">Каноническое свойство PidTagOriginalAuthorEmailAddress</span><span class="sxs-lookup"><span data-stu-id="97471-103">PidTagOriginalAuthorEmailAddress Canonical Property</span></span>

  
  
<span data-ttu-id="97471-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="97471-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="97471-105">Содержит адрес электронной почты автора первая версия сообщения, то есть, сообщение перед пересылку и ответ.</span><span class="sxs-lookup"><span data-stu-id="97471-105">Contains the email address of the author of the first version of a message, that is, the message before being forwarded or replied to.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="97471-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="97471-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="97471-107">PR_ORIGINAL_AUTHOR_EMAIL_ADDRESS, PR_ORIGINAL_AUTHOR_EMAIL_ADDRESS_A, PR_ORIGINAL_AUTHOR_EMAIL_ADDRESS_W</span><span class="sxs-lookup"><span data-stu-id="97471-107">PR_ORIGINAL_AUTHOR_EMAIL_ADDRESS, PR_ORIGINAL_AUTHOR_EMAIL_ADDRESS_A, PR_ORIGINAL_AUTHOR_EMAIL_ADDRESS_W</span></span>  <br/> |
|<span data-ttu-id="97471-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="97471-108">Identifier:</span></span>  <br/> |<span data-ttu-id="97471-109">0x007A</span><span class="sxs-lookup"><span data-stu-id="97471-109">0x007A</span></span>  <br/> |
|<span data-ttu-id="97471-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="97471-110">Data type:</span></span>  <br/> |<span data-ttu-id="97471-111">PT_STRING8 PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="97471-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="97471-112">Область:</span><span class="sxs-lookup"><span data-stu-id="97471-112">Area:</span></span>  <br/> |<span data-ttu-id="97471-113">Сервер</span><span class="sxs-lookup"><span data-stu-id="97471-113">Server</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="97471-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="97471-114">Remarks</span></span>

<span data-ttu-id="97471-115">Эти свойства являются примерами свойства адреса для автора сообщения.</span><span class="sxs-lookup"><span data-stu-id="97471-115">These properties are examples of the address properties for the author of a message.</span></span> <span data-ttu-id="97471-116">В первой отправки сообщения клиентское приложение следует задать эти свойства, значение свойства **PR_SENDER_EMAIL_ADDRESS** ([PidTagSenderEmailAddress](pidtagsenderemailaddress-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="97471-116">At first submission of the message, the client application should set these properties to the value of the **PR_SENDER_EMAIL_ADDRESS** ([PidTagSenderEmailAddress](pidtagsenderemailaddress-canonical-property.md)) property.</span></span> <span data-ttu-id="97471-117">Никогда не изменяется при сообщение будет переслано или ответ.</span><span class="sxs-lookup"><span data-stu-id="97471-117">It is never changed when the message is forwarded or replied to.</span></span>
  
<span data-ttu-id="97471-118">Исходные свойства author разрешить для хранения данных из других доменов обмена мгновенными сообщениями.</span><span class="sxs-lookup"><span data-stu-id="97471-118">The original author properties allow for preservation of information from outside the local messaging domain.</span></span> <span data-ttu-id="97471-119">При получении сообщения из другой домен обмена мгновенными сообщениями, например, из Интернета, эти свойства предусмотрена возможность убедитесь, что исходные данные не потеряны.</span><span class="sxs-lookup"><span data-stu-id="97471-119">When a message arrives from another messaging domain, such as from the Internet, these properties provide a way to ensure that original information is not lost.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="97471-120">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="97471-120">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="97471-121">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="97471-121">Header files</span></span>

<span data-ttu-id="97471-122">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="97471-122">Mapidefs.h</span></span>
  
> <span data-ttu-id="97471-123">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="97471-123">Provides data type definitions.</span></span>
    
<span data-ttu-id="97471-124">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="97471-124">Mapitags.h</span></span>
  
> <span data-ttu-id="97471-125">Содержит определения свойств указано, что связанными свойствами.</span><span class="sxs-lookup"><span data-stu-id="97471-125">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="97471-126">См. также</span><span class="sxs-lookup"><span data-stu-id="97471-126">See also</span></span>



[<span data-ttu-id="97471-127">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="97471-127">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="97471-128">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="97471-128">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="97471-129">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="97471-129">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="97471-130">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="97471-130">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)


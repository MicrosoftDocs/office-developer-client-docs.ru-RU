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
ms.openlocfilehash: 7918c5d5b585ffb199bfbc140edfb8286b499b40
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436169"
---
# <a name="pidtagoriginalauthoremailaddress-canonical-property"></a><span data-ttu-id="18919-103">Каноническое свойство PidTagOriginalAuthorEmailAddress</span><span class="sxs-lookup"><span data-stu-id="18919-103">PidTagOriginalAuthorEmailAddress Canonical Property</span></span>

  
  
<span data-ttu-id="18919-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="18919-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="18919-105">Содержит адрес электронной почты автора первой версии сообщения, то есть сообщение перед пересылкой или ответом.</span><span class="sxs-lookup"><span data-stu-id="18919-105">Contains the email address of the author of the first version of a message, that is, the message before being forwarded or replied to.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="18919-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="18919-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="18919-107">ПР_ОРИГИНАЛ_АУСОР_ЕМАИЛ_АДДРЕСС, ПР_ОРИГИНАЛ_АУСОР_ЕМАИЛ_АДДРЕСС_А, ПР_ОРИГИНАЛ_АУСОР_ЕМАИЛ_АДДРЕСС_В</span><span class="sxs-lookup"><span data-stu-id="18919-107">PR_ORIGINAL_AUTHOR_EMAIL_ADDRESS, PR_ORIGINAL_AUTHOR_EMAIL_ADDRESS_A, PR_ORIGINAL_AUTHOR_EMAIL_ADDRESS_W</span></span>  <br/> |
|<span data-ttu-id="18919-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="18919-108">Identifier:</span></span>  <br/> |<span data-ttu-id="18919-109">0x007A</span><span class="sxs-lookup"><span data-stu-id="18919-109">0x007A</span></span>  <br/> |
|<span data-ttu-id="18919-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="18919-110">Data type:</span></span>  <br/> |<span data-ttu-id="18919-111">PT_STRING8, ПТ_УНИКОДЕ</span><span class="sxs-lookup"><span data-stu-id="18919-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="18919-112">Область:</span><span class="sxs-lookup"><span data-stu-id="18919-112">Area:</span></span>  <br/> |<span data-ttu-id="18919-113">Сервер</span><span class="sxs-lookup"><span data-stu-id="18919-113">Server</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="18919-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="18919-114">Remarks</span></span>

<span data-ttu-id="18919-115">Эти свойства являются примерами свойств адреса для автора сообщения.</span><span class="sxs-lookup"><span data-stu-id="18919-115">These properties are examples of the address properties for the author of a message.</span></span> <span data-ttu-id="18919-116">При первой отправке сообщения клиентское приложение должно задать для этих свойств значение свойства **пр_сендер_емаил_аддресс** ([PidTagSenderEmailAddress](pidtagsenderemailaddress-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="18919-116">At first submission of the message, the client application should set these properties to the value of the **PR_SENDER_EMAIL_ADDRESS** ([PidTagSenderEmailAddress](pidtagsenderemailaddress-canonical-property.md)) property.</span></span> <span data-ttu-id="18919-117">Он никогда не изменяется при пересылке сообщения или ответе на него.</span><span class="sxs-lookup"><span data-stu-id="18919-117">It is never changed when the message is forwarded or replied to.</span></span>
  
<span data-ttu-id="18919-118">Исходные свойства автора допускают сохранение данных извне локального домена обмена сообщениями.</span><span class="sxs-lookup"><span data-stu-id="18919-118">The original author properties allow for preservation of information from outside the local messaging domain.</span></span> <span data-ttu-id="18919-119">Когда сообщение поступает из другого домена обмена сообщениями (например, из Интернета), эти свойства предоставляют способ гарантировать, что исходные данные не будут потеряны.</span><span class="sxs-lookup"><span data-stu-id="18919-119">When a message arrives from another messaging domain, such as from the Internet, these properties provide a way to ensure that original information is not lost.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="18919-120">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="18919-120">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="18919-121">Файлы заГоловков</span><span class="sxs-lookup"><span data-stu-id="18919-121">Header files</span></span>

<span data-ttu-id="18919-122">MAPIDEFS. h</span><span class="sxs-lookup"><span data-stu-id="18919-122">Mapidefs.h</span></span>
  
> <span data-ttu-id="18919-123">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="18919-123">Provides data type definitions.</span></span>
    
<span data-ttu-id="18919-124">Мапитагс. h</span><span class="sxs-lookup"><span data-stu-id="18919-124">Mapitags.h</span></span>
  
> <span data-ttu-id="18919-125">Содержит определения свойств, перечисленных как связанные свойства.</span><span class="sxs-lookup"><span data-stu-id="18919-125">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="18919-126">См. также</span><span class="sxs-lookup"><span data-stu-id="18919-126">See also</span></span>



[<span data-ttu-id="18919-127">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="18919-127">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="18919-128">Каноническое свойство MAPI</span><span class="sxs-lookup"><span data-stu-id="18919-128">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="18919-129">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="18919-129">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="18919-130">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="18919-130">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)


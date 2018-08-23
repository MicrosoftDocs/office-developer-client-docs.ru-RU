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
ms.openlocfilehash: bd019378a8db7b2e356f0c8b2f30a59e685b9e8a
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22595435"
---
# <a name="pidtagoriginalauthoremailaddress-canonical-property"></a><span data-ttu-id="8342b-103">Каноническое свойство PidTagOriginalAuthorEmailAddress</span><span class="sxs-lookup"><span data-stu-id="8342b-103">PidTagOriginalAuthorEmailAddress Canonical Property</span></span>

  
  
<span data-ttu-id="8342b-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8342b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8342b-105">Содержит адрес электронной почты автора первая версия сообщения, то есть, сообщение перед пересылку и ответ.</span><span class="sxs-lookup"><span data-stu-id="8342b-105">Contains the email address of the author of the first version of a message, that is, the message before being forwarded or replied to.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="8342b-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="8342b-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="8342b-107">PR_ORIGINAL_AUTHOR_EMAIL_ADDRESS, PR_ORIGINAL_AUTHOR_EMAIL_ADDRESS_A, PR_ORIGINAL_AUTHOR_EMAIL_ADDRESS_W</span><span class="sxs-lookup"><span data-stu-id="8342b-107">PR_ORIGINAL_AUTHOR_EMAIL_ADDRESS, PR_ORIGINAL_AUTHOR_EMAIL_ADDRESS_A, PR_ORIGINAL_AUTHOR_EMAIL_ADDRESS_W</span></span>  <br/> |
|<span data-ttu-id="8342b-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="8342b-108">Identifier:</span></span>  <br/> |<span data-ttu-id="8342b-109">0x007A</span><span class="sxs-lookup"><span data-stu-id="8342b-109">0x007A</span></span>  <br/> |
|<span data-ttu-id="8342b-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="8342b-110">Data type:</span></span>  <br/> |<span data-ttu-id="8342b-111">PT_STRING8 PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="8342b-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="8342b-112">Область:</span><span class="sxs-lookup"><span data-stu-id="8342b-112">Area:</span></span>  <br/> |<span data-ttu-id="8342b-113">Сервер</span><span class="sxs-lookup"><span data-stu-id="8342b-113">Server</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="8342b-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="8342b-114">Remarks</span></span>

<span data-ttu-id="8342b-115">Эти свойства являются примерами свойства адреса для автора сообщения.</span><span class="sxs-lookup"><span data-stu-id="8342b-115">These properties are examples of the address properties for the author of a message.</span></span> <span data-ttu-id="8342b-116">В первой отправки сообщения клиентское приложение следует задать эти свойства, значение свойства **PR_SENDER_EMAIL_ADDRESS** ([PidTagSenderEmailAddress](pidtagsenderemailaddress-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="8342b-116">At first submission of the message, the client application should set these properties to the value of the **PR_SENDER_EMAIL_ADDRESS** ([PidTagSenderEmailAddress](pidtagsenderemailaddress-canonical-property.md)) property.</span></span> <span data-ttu-id="8342b-117">Никогда не изменяется при сообщение будет переслано или ответ.</span><span class="sxs-lookup"><span data-stu-id="8342b-117">It is never changed when the message is forwarded or replied to.</span></span>
  
<span data-ttu-id="8342b-118">Исходные свойства author разрешить для хранения данных из других доменов обмена мгновенными сообщениями.</span><span class="sxs-lookup"><span data-stu-id="8342b-118">The original author properties allow for preservation of information from outside the local messaging domain.</span></span> <span data-ttu-id="8342b-119">При получении сообщения из другой домен обмена мгновенными сообщениями, например, из Интернета, эти свойства предусмотрена возможность убедитесь, что исходные данные не потеряны.</span><span class="sxs-lookup"><span data-stu-id="8342b-119">When a message arrives from another messaging domain, such as from the Internet, these properties provide a way to ensure that original information is not lost.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="8342b-120">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="8342b-120">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="8342b-121">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="8342b-121">Header files</span></span>

<span data-ttu-id="8342b-122">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="8342b-122">Mapidefs.h</span></span>
  
> <span data-ttu-id="8342b-123">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="8342b-123">Provides data type definitions.</span></span>
    
<span data-ttu-id="8342b-124">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="8342b-124">Mapitags.h</span></span>
  
> <span data-ttu-id="8342b-125">Содержит определения свойств указано, что связанными свойствами.</span><span class="sxs-lookup"><span data-stu-id="8342b-125">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="8342b-126">См. также</span><span class="sxs-lookup"><span data-stu-id="8342b-126">See also</span></span>



[<span data-ttu-id="8342b-127">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="8342b-127">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="8342b-128">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="8342b-128">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="8342b-129">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="8342b-129">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="8342b-130">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="8342b-130">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)


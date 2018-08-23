---
title: Каноническое свойство PidTagOriginalAuthorAddressType
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagOriginalAuthorAddressType
api_type:
- COM
ms.assetid: 7cdedb1a-e441-469b-be50-2f18203eb30d
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: bc3c06c38f8ff8121a8503341cdd1084c036e52d
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22589975"
---
# <a name="pidtagoriginalauthoraddresstype-canonical-property"></a><span data-ttu-id="7b430-103">Каноническое свойство PidTagOriginalAuthorAddressType</span><span class="sxs-lookup"><span data-stu-id="7b430-103">PidTagOriginalAuthorAddressType Canonical Property</span></span>

  
  
<span data-ttu-id="7b430-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7b430-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7b430-105">Содержит тип адреса автора первая версия сообщения, то есть, сообщение перед пересылку и ответ.</span><span class="sxs-lookup"><span data-stu-id="7b430-105">Contains the address type of the author of the first version of a message, that is, the message before being forwarded or replied to.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="7b430-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="7b430-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="7b430-107">PR_ORIGINAL_AUTHOR_ADDRTYPE, PR_ORIGINAL_AUTHOR_ADDRTYPE_A, PR_ORIGINAL_AUTHOR_ADDRTYPE_W</span><span class="sxs-lookup"><span data-stu-id="7b430-107">PR_ORIGINAL_AUTHOR_ADDRTYPE, PR_ORIGINAL_AUTHOR_ADDRTYPE_A, PR_ORIGINAL_AUTHOR_ADDRTYPE_W</span></span>  <br/> |
|<span data-ttu-id="7b430-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="7b430-108">Identifier:</span></span>  <br/> |<span data-ttu-id="7b430-109">0x0079</span><span class="sxs-lookup"><span data-stu-id="7b430-109">0x0079</span></span>  <br/> |
|<span data-ttu-id="7b430-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="7b430-110">Data type:</span></span>  <br/> |<span data-ttu-id="7b430-111">PT_STRING8 PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="7b430-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="7b430-112">Область:</span><span class="sxs-lookup"><span data-stu-id="7b430-112">Area:</span></span>  <br/> |<span data-ttu-id="7b430-113">Сервер</span><span class="sxs-lookup"><span data-stu-id="7b430-113">Server</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="7b430-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="7b430-114">Remarks</span></span>

<span data-ttu-id="7b430-115">Эти свойства являются примерами свойства адреса для автора сообщения.</span><span class="sxs-lookup"><span data-stu-id="7b430-115">These properties are examples of the address properties for the author of a message.</span></span> <span data-ttu-id="7b430-116">В первой отправки сообщения клиентское приложение следует этому свойству присвоено значение свойства **PR_SENDER_ADDRTYPE** ([PidTagSenderAddressType](pidtagsenderaddresstype-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="7b430-116">At first submission of the message, the client application should set this property to the value of the **PR_SENDER_ADDRTYPE** ([PidTagSenderAddressType](pidtagsenderaddresstype-canonical-property.md)) property.</span></span> <span data-ttu-id="7b430-117">Никогда не изменяется при сообщение будет переслано или ответ.</span><span class="sxs-lookup"><span data-stu-id="7b430-117">It is never changed when the message is forwarded or replied to.</span></span>
  
<span data-ttu-id="7b430-118">Исходные свойства author разрешить для хранения данных из других доменов обмена мгновенными сообщениями.</span><span class="sxs-lookup"><span data-stu-id="7b430-118">The original author properties allow for preservation of information from outside the local messaging domain.</span></span> <span data-ttu-id="7b430-119">При получении сообщения из другой домен обмена мгновенными сообщениями, например, из Интернета, эти свойства предусмотрена возможность убедитесь, что исходные данные не потеряны.</span><span class="sxs-lookup"><span data-stu-id="7b430-119">When a message arrives from another messaging domain, such as from the Internet, these properties provide a way to ensure that original information is not lost.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="7b430-120">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="7b430-120">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="7b430-121">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="7b430-121">Header files</span></span>

<span data-ttu-id="7b430-122">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="7b430-122">Mapidefs.h</span></span>
  
> <span data-ttu-id="7b430-123">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="7b430-123">Provides data type definitions.</span></span>
    
<span data-ttu-id="7b430-124">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="7b430-124">Mapitags.h</span></span>
  
> <span data-ttu-id="7b430-125">Содержит определения свойств указано, что связанными свойствами.</span><span class="sxs-lookup"><span data-stu-id="7b430-125">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="7b430-126">См. также</span><span class="sxs-lookup"><span data-stu-id="7b430-126">See also</span></span>



[<span data-ttu-id="7b430-127">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="7b430-127">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="7b430-128">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="7b430-128">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="7b430-129">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="7b430-129">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="7b430-130">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="7b430-130">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)


---
title: Каноническое свойство PidTagOriginalAuthorSearchKey
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagOriginalAuthorSearchKey
api_type:
- COM
ms.assetid: 4a10cf99-c5e6-4a24-b531-3aebb7800bfe
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: e5b283376d018b7b2675e05f994d586126437590
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19811429"
---
# <a name="pidtagoriginalauthorsearchkey-canonical-property"></a><span data-ttu-id="5bf89-103">Каноническое свойство PidTagOriginalAuthorSearchKey</span><span class="sxs-lookup"><span data-stu-id="5bf89-103">PidTagOriginalAuthorSearchKey Canonical Property</span></span>

  
  
<span data-ttu-id="5bf89-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="5bf89-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="5bf89-105">Содержит ключ поиска автора первая версия сообщения, то есть, сообщение перед пересылку и ответ.</span><span class="sxs-lookup"><span data-stu-id="5bf89-105">Contains the search key of the author of the first version of a message, that is, the message before being forwarded or replied to.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="5bf89-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="5bf89-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="5bf89-107">PR_ORIGINAL_AUTHOR_SEARCH_KEY</span><span class="sxs-lookup"><span data-stu-id="5bf89-107">PR_ORIGINAL_AUTHOR_SEARCH_KEY</span></span>  <br/> |
|<span data-ttu-id="5bf89-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="5bf89-108">Identifier:</span></span>  <br/> |<span data-ttu-id="5bf89-109">0x0056</span><span class="sxs-lookup"><span data-stu-id="5bf89-109">0x0056</span></span>  <br/> |
|<span data-ttu-id="5bf89-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="5bf89-110">Data type:</span></span>  <br/> |<span data-ttu-id="5bf89-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="5bf89-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="5bf89-112">Область:</span><span class="sxs-lookup"><span data-stu-id="5bf89-112">Area:</span></span>  <br/> |<span data-ttu-id="5bf89-113">Сервер</span><span class="sxs-lookup"><span data-stu-id="5bf89-113">Server</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="5bf89-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="5bf89-114">Remarks</span></span>

<span data-ttu-id="5bf89-115">Это свойство является одним из свойств адреса для автора сообщения.</span><span class="sxs-lookup"><span data-stu-id="5bf89-115">This property is one of the address properties for the author of a message.</span></span> <span data-ttu-id="5bf89-116">В первой отправки сообщения клиентское приложение следует этому свойству присвоено значение значение свойства[PidTagSenderSearchKey](pidtagsendersearchkey-canonical-property.md) **PR_SENDER_SEARCH_KEY**.</span><span class="sxs-lookup"><span data-stu-id="5bf89-116">At first submission of the message, the client application should set this property to the value of the **PR_SENDER_SEARCH_KEY**[PidTagSenderSearchKey](pidtagsendersearchkey-canonical-property.md) property.</span></span> <span data-ttu-id="5bf89-117">Никогда не изменяется при сообщение будет переслано или ответ.</span><span class="sxs-lookup"><span data-stu-id="5bf89-117">It is never changed when the message is forwarded or replied to.</span></span> 
  
<span data-ttu-id="5bf89-118">Исходные свойства author разрешить для хранения данных из других доменов обмена мгновенными сообщениями.</span><span class="sxs-lookup"><span data-stu-id="5bf89-118">The original author properties allow for preservation of information from outside the local messaging domain.</span></span> <span data-ttu-id="5bf89-119">При получении сообщения из другой домен обмена мгновенными сообщениями, например, из Интернета, эти свойства предусмотрена возможность убедитесь, что исходные данные не потеряны.</span><span class="sxs-lookup"><span data-stu-id="5bf89-119">When a message arrives from another messaging domain, such as from the Internet, these properties provide a way to ensure that original information is not lost.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="5bf89-120">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="5bf89-120">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="5bf89-121">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="5bf89-121">Header files</span></span>

<span data-ttu-id="5bf89-122">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="5bf89-122">Mapidefs.h</span></span>
  
> <span data-ttu-id="5bf89-123">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="5bf89-123">Provides data type definitions.</span></span>
    
<span data-ttu-id="5bf89-124">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="5bf89-124">Mapitags.h</span></span>
  
> <span data-ttu-id="5bf89-125">Содержит определения свойств указано, что связанными свойствами.</span><span class="sxs-lookup"><span data-stu-id="5bf89-125">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="5bf89-126">См. также</span><span class="sxs-lookup"><span data-stu-id="5bf89-126">See also</span></span>



[<span data-ttu-id="5bf89-127">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="5bf89-127">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="5bf89-128">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="5bf89-128">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="5bf89-129">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="5bf89-129">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="5bf89-130">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="5bf89-130">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)


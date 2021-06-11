---
title: Каноническое свойство PidTagOriginalSenderSearchKey
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagOriginalSenderSearchKey
api_type:
- COM
ms.assetid: 164eb9dd-e553-459e-99c1-3da0284bb01f
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 97ab08d3da3725187ef2d5c70bec80e9142bdd21
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32342604"
---
# <a name="pidtagoriginalsendersearchkey-canonical-property"></a><span data-ttu-id="86864-103">Каноническое свойство PidTagOriginalSenderSearchKey</span><span class="sxs-lookup"><span data-stu-id="86864-103">PidTagOriginalSenderSearchKey Canonical Property</span></span>

  
  
<span data-ttu-id="86864-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="86864-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="86864-105">Содержит ключ поиска отправитель первой версии сообщения, то есть сообщение перед отправкой или ответом на него.</span><span class="sxs-lookup"><span data-stu-id="86864-105">Contains the search key for the sender of the first version of a message, that is, the message before being forwarded or replied to.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="86864-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="86864-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="86864-107">PR_ORIGINAL_SENDER_SEARCH_KEY</span><span class="sxs-lookup"><span data-stu-id="86864-107">PR_ORIGINAL_SENDER_SEARCH_KEY</span></span>  <br/> |
|<span data-ttu-id="86864-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="86864-108">Identifier:</span></span>  <br/> |<span data-ttu-id="86864-109">0x005C</span><span class="sxs-lookup"><span data-stu-id="86864-109">0x005C</span></span>  <br/> |
|<span data-ttu-id="86864-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="86864-110">Data type:</span></span>  <br/> |<span data-ttu-id="86864-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="86864-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="86864-112">Область:</span><span class="sxs-lookup"><span data-stu-id="86864-112">Area:</span></span>  <br/> |<span data-ttu-id="86864-113">Общие сообщения</span><span class="sxs-lookup"><span data-stu-id="86864-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="86864-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="86864-114">Remarks</span></span>

<span data-ttu-id="86864-115">Это свойство является одним из свойств адресов исходного отправитель сообщения.</span><span class="sxs-lookup"><span data-stu-id="86864-115">This property is one of the address properties for the original sender of a message.</span></span> <span data-ttu-id="86864-116">При первой отправке сообщения клиентская заявка должна установить это свойство к значению **свойства PR_SENDER_SEARCH_KEY** [(PidTagSenderSearchKey).](pidtagsendersearchkey-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="86864-116">At first submission of the message, the client application should set this property to the value of the **PR_SENDER_SEARCH_KEY** ([PidTagSenderSearchKey](pidtagsendersearchkey-canonical-property.md)) property.</span></span> <span data-ttu-id="86864-117">Он никогда не меняется, когда сообщение переададовыв или отвечает на него.</span><span class="sxs-lookup"><span data-stu-id="86864-117">It is never changed when the message is forwarded or replied to.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="86864-118">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="86864-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="86864-119">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="86864-119">Protocol specifications</span></span>

<span data-ttu-id="86864-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="86864-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="86864-121">Содержит ссылки на связанные Exchange Server протоколы.</span><span class="sxs-lookup"><span data-stu-id="86864-121">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="86864-122">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="86864-122">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="86864-123">Указывает свойства и операции, допустимые на объектах сообщений электронной почты.</span><span class="sxs-lookup"><span data-stu-id="86864-123">Specifies the properties and operations that are permissible on email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="86864-124">Файлы заголовки</span><span class="sxs-lookup"><span data-stu-id="86864-124">Header files</span></span>

<span data-ttu-id="86864-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="86864-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="86864-126">Предоставляет определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="86864-126">Provides data type definitions.</span></span>
    
<span data-ttu-id="86864-127">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="86864-127">Mapitags.h</span></span>
  
> <span data-ttu-id="86864-128">Содержит определения свойств, перечисленных в качестве альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="86864-128">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="86864-129">См. также</span><span class="sxs-lookup"><span data-stu-id="86864-129">See also</span></span>



[<span data-ttu-id="86864-130">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="86864-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="86864-131">Канонические свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="86864-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="86864-132">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="86864-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="86864-133">Сопоставление имен MAPI с каноническими именами свойств</span><span class="sxs-lookup"><span data-stu-id="86864-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)


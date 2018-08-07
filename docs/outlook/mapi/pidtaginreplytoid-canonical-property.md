---
title: Каноническое свойство PidTagInReplyToId
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagInReplyToId
api_type:
- HeaderDef
ms.assetid: d435a65a-de01-4fb0-bc54-a87a2c4462ac
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 2e8ed4af81de6e48af3e427f2d2d2f94572d241f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19811234"
---
# <a name="pidtaginreplytoid-canonical-property"></a><span data-ttu-id="4cea8-103">Каноническое свойство PidTagInReplyToId</span><span class="sxs-lookup"><span data-stu-id="4cea8-103">PidTagInReplyToId Canonical Property</span></span>

  
  
<span data-ttu-id="4cea8-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="4cea8-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="4cea8-105">Содержит значение свойства **PR_INTERNET_MESSAGE_ID** ([PidTagInternetMessageId](pidtaginternetmessageid-canonical-property.md)) исходного сообщения.</span><span class="sxs-lookup"><span data-stu-id="4cea8-105">Contains the original message's **PR_INTERNET_MESSAGE_ID** ([PidTagInternetMessageId](pidtaginternetmessageid-canonical-property.md)) property value.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="4cea8-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="4cea8-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="4cea8-107">PR_IN_REPLY_TO_ID, PR_IN_REPLY_TO_ID_A, PR_IN_REPLY_TO_ID_W</span><span class="sxs-lookup"><span data-stu-id="4cea8-107">PR_IN_REPLY_TO_ID, PR_IN_REPLY_TO_ID_A, PR_IN_REPLY_TO_ID_W</span></span>  <br/> |
|<span data-ttu-id="4cea8-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="4cea8-108">Identifier:</span></span>  <br/> |<span data-ttu-id="4cea8-109">0x1042</span><span class="sxs-lookup"><span data-stu-id="4cea8-109">0x1042</span></span>  <br/> |
|<span data-ttu-id="4cea8-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="4cea8-110">Data type:</span></span>  <br/> |<span data-ttu-id="4cea8-111">PT_STRING8 PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="4cea8-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="4cea8-112">Область:</span><span class="sxs-lookup"><span data-stu-id="4cea8-112">Area:</span></span>  <br/> |<span data-ttu-id="4cea8-113">Общие системы обмена сообщениями</span><span class="sxs-lookup"><span data-stu-id="4cea8-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="4cea8-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="4cea8-114">Remarks</span></span>

<span data-ttu-id="4cea8-115">Эти свойства необходимо установить на все ответы на сообщение.</span><span class="sxs-lookup"><span data-stu-id="4cea8-115">These properties must be set on all message replies.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="4cea8-116">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="4cea8-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="4cea8-117">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="4cea8-117">Protocol specifications</span></span>

<span data-ttu-id="4cea8-118">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="4cea8-118">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="4cea8-119">Содержит ссылки на связанные спецификаций протокола Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="4cea8-119">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="4cea8-120">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="4cea8-120">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="4cea8-121">Задает свойства и операции, допустимые для объектов сообщения электронной почты.</span><span class="sxs-lookup"><span data-stu-id="4cea8-121">Specifies the properties and operations that are permissible on email message objects.</span></span>
    
<span data-ttu-id="4cea8-122">[[MS-OXCMAIL]](http://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="4cea8-122">[[MS-OXCMAIL]](http://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="4cea8-123">Преобразование conventions стандартных электронной почты Интернета объекты сообщений.</span><span class="sxs-lookup"><span data-stu-id="4cea8-123">Converts from Internet standard email conventions to message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="4cea8-124">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="4cea8-124">Header files</span></span>

<span data-ttu-id="4cea8-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="4cea8-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="4cea8-126">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="4cea8-126">Provides data type definitions.</span></span>
    
<span data-ttu-id="4cea8-127">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="4cea8-127">Mapitags.h</span></span>
  
> <span data-ttu-id="4cea8-128">Содержит определения свойства в списке альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="4cea8-128">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="4cea8-129">См. также</span><span class="sxs-lookup"><span data-stu-id="4cea8-129">See also</span></span>



[<span data-ttu-id="4cea8-130">Каноническое свойство PidTagInternetMessageId</span><span class="sxs-lookup"><span data-stu-id="4cea8-130">PidTagInternetMessageId Canonical Property</span></span>](pidtaginternetmessageid-canonical-property.md)


[<span data-ttu-id="4cea8-131">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="4cea8-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="4cea8-132">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="4cea8-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="4cea8-133">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="4cea8-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="4cea8-134">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="4cea8-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)


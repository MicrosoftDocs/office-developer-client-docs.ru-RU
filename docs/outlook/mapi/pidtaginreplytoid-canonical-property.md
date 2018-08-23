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
ms.openlocfilehash: 6f3ae69243da185430836903da9e7b0644c5db90
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22594784"
---
# <a name="pidtaginreplytoid-canonical-property"></a><span data-ttu-id="1b482-103">Каноническое свойство PidTagInReplyToId</span><span class="sxs-lookup"><span data-stu-id="1b482-103">PidTagInReplyToId Canonical Property</span></span>

  
  
<span data-ttu-id="1b482-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1b482-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1b482-105">Содержит значение свойства **PR_INTERNET_MESSAGE_ID** ([PidTagInternetMessageId](pidtaginternetmessageid-canonical-property.md)) исходного сообщения.</span><span class="sxs-lookup"><span data-stu-id="1b482-105">Contains the original message's **PR_INTERNET_MESSAGE_ID** ([PidTagInternetMessageId](pidtaginternetmessageid-canonical-property.md)) property value.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="1b482-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="1b482-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="1b482-107">PR_IN_REPLY_TO_ID, PR_IN_REPLY_TO_ID_A, PR_IN_REPLY_TO_ID_W</span><span class="sxs-lookup"><span data-stu-id="1b482-107">PR_IN_REPLY_TO_ID, PR_IN_REPLY_TO_ID_A, PR_IN_REPLY_TO_ID_W</span></span>  <br/> |
|<span data-ttu-id="1b482-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="1b482-108">Identifier:</span></span>  <br/> |<span data-ttu-id="1b482-109">0x1042</span><span class="sxs-lookup"><span data-stu-id="1b482-109">0x1042</span></span>  <br/> |
|<span data-ttu-id="1b482-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="1b482-110">Data type:</span></span>  <br/> |<span data-ttu-id="1b482-111">PT_STRING8 PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="1b482-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="1b482-112">Область:</span><span class="sxs-lookup"><span data-stu-id="1b482-112">Area:</span></span>  <br/> |<span data-ttu-id="1b482-113">Общие системы обмена сообщениями</span><span class="sxs-lookup"><span data-stu-id="1b482-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="1b482-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="1b482-114">Remarks</span></span>

<span data-ttu-id="1b482-115">Эти свойства необходимо установить на все ответы на сообщение.</span><span class="sxs-lookup"><span data-stu-id="1b482-115">These properties must be set on all message replies.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="1b482-116">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="1b482-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="1b482-117">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="1b482-117">Protocol specifications</span></span>

<span data-ttu-id="1b482-118">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="1b482-118">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="1b482-119">Содержит ссылки на связанные спецификаций протокола Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="1b482-119">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="1b482-120">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="1b482-120">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="1b482-121">Задает свойства и операции, допустимые для объектов сообщения электронной почты.</span><span class="sxs-lookup"><span data-stu-id="1b482-121">Specifies the properties and operations that are permissible on email message objects.</span></span>
    
<span data-ttu-id="1b482-122">[[MS-OXCMAIL]](http://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="1b482-122">[[MS-OXCMAIL]](http://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="1b482-123">Преобразование conventions стандартных электронной почты Интернета объекты сообщений.</span><span class="sxs-lookup"><span data-stu-id="1b482-123">Converts from Internet standard email conventions to message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="1b482-124">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="1b482-124">Header files</span></span>

<span data-ttu-id="1b482-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="1b482-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="1b482-126">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="1b482-126">Provides data type definitions.</span></span>
    
<span data-ttu-id="1b482-127">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="1b482-127">Mapitags.h</span></span>
  
> <span data-ttu-id="1b482-128">Содержит определения свойства в списке альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="1b482-128">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="1b482-129">См. также</span><span class="sxs-lookup"><span data-stu-id="1b482-129">See also</span></span>



[<span data-ttu-id="1b482-130">Каноническое свойство PidTagInternetMessageId</span><span class="sxs-lookup"><span data-stu-id="1b482-130">PidTagInternetMessageId Canonical Property</span></span>](pidtaginternetmessageid-canonical-property.md)


[<span data-ttu-id="1b482-131">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="1b482-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="1b482-132">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="1b482-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="1b482-133">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="1b482-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="1b482-134">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="1b482-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)


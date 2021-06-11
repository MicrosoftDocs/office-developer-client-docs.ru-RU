---
title: Каноническое свойство PidTagOriginalSentRepresentingSearchKey
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagOriginalSentRepresentingSearchKey
api_type:
- COM
ms.assetid: 0fb1b803-f8b4-4d6d-8e2a-836daa98ac63
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: ee23e2f25370a253b914779b3bfd0ab82fd08c7e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32340980"
---
# <a name="pidtagoriginalsentrepresentingsearchkey-canonical-property"></a><span data-ttu-id="be6f1-103">Каноническое свойство PidTagOriginalSentRepresentingSearchKey</span><span class="sxs-lookup"><span data-stu-id="be6f1-103">PidTagOriginalSentRepresentingSearchKey Canonical Property</span></span>

  
  
<span data-ttu-id="be6f1-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="be6f1-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="be6f1-105">Содержит ключ поиска пользователя обмена сообщениями, от имени которого было отправлено исходное сообщение.</span><span class="sxs-lookup"><span data-stu-id="be6f1-105">Contains the search key of the messaging user on whose behalf the original message was sent.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="be6f1-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="be6f1-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="be6f1-107">PR_ORIGINAL_SENT_REPRESENTING_SEARCH_KEY</span><span class="sxs-lookup"><span data-stu-id="be6f1-107">PR_ORIGINAL_SENT_REPRESENTING_SEARCH_KEY</span></span>  <br/> |
|<span data-ttu-id="be6f1-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="be6f1-108">Identifier:</span></span>  <br/> |<span data-ttu-id="be6f1-109">0x005F</span><span class="sxs-lookup"><span data-stu-id="be6f1-109">0x005F</span></span>  <br/> |
|<span data-ttu-id="be6f1-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="be6f1-110">Data type:</span></span>  <br/> |<span data-ttu-id="be6f1-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="be6f1-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="be6f1-112">Область:</span><span class="sxs-lookup"><span data-stu-id="be6f1-112">Area:</span></span>  <br/> |<span data-ttu-id="be6f1-113">Общие сообщения</span><span class="sxs-lookup"><span data-stu-id="be6f1-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="be6f1-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="be6f1-114">Remarks</span></span>

<span data-ttu-id="be6f1-115">Это свойство является одним из свойств адресов для исходного представленного отправитель сообщения.</span><span class="sxs-lookup"><span data-stu-id="be6f1-115">This property is one of the address properties for the original represented sender of a message.</span></span> <span data-ttu-id="be6f1-116">Он используется в потоке беседы.</span><span class="sxs-lookup"><span data-stu-id="be6f1-116">It is used in a conversation thread.</span></span>
  
<span data-ttu-id="be6f1-117">Клиентская заявка, отправляя сообщение от имени другого **клиента,** должна установить это свойство к значению свойства [PR_SENT_REPRESENTING_SEARCH_KEY (PidTagSentRepresentingSearchKey)](pidtagsentrepresentingsearchkey-canonical-property.md)при первой отправке сообщения.</span><span class="sxs-lookup"><span data-stu-id="be6f1-117">A client application sending a message on behalf of another client should set this property to the value of the **PR_SENT_REPRESENTING_SEARCH_KEY** ([PidTagSentRepresentingSearchKey](pidtagsentrepresentingsearchkey-canonical-property.md)) property at the first submission of the message.</span></span> <span data-ttu-id="be6f1-118">После набора его не следует менять.</span><span class="sxs-lookup"><span data-stu-id="be6f1-118">Once set, it should never be changed.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="be6f1-119">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="be6f1-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="be6f1-120">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="be6f1-120">Protocol specifications</span></span>

<span data-ttu-id="be6f1-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="be6f1-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="be6f1-122">Содержит ссылки на связанные Exchange Server протоколы.</span><span class="sxs-lookup"><span data-stu-id="be6f1-122">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="be6f1-123">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="be6f1-123">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="be6f1-124">Указывает свойства и операции, допустимые на объектах сообщений электронной почты.</span><span class="sxs-lookup"><span data-stu-id="be6f1-124">Specifies the properties and operations that are permissible on email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="be6f1-125">Файлы заголовки</span><span class="sxs-lookup"><span data-stu-id="be6f1-125">Header files</span></span>

<span data-ttu-id="be6f1-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="be6f1-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="be6f1-127">Предоставляет определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="be6f1-127">Provides data type definitions.</span></span>
    
<span data-ttu-id="be6f1-128">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="be6f1-128">Mapitags.h</span></span>
  
> <span data-ttu-id="be6f1-129">Содержит определения свойств, перечисленных в качестве альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="be6f1-129">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="be6f1-130">См. также</span><span class="sxs-lookup"><span data-stu-id="be6f1-130">See also</span></span>



[<span data-ttu-id="be6f1-131">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="be6f1-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="be6f1-132">Канонические свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="be6f1-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="be6f1-133">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="be6f1-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="be6f1-134">Сопоставление имен MAPI с каноническими именами свойств</span><span class="sxs-lookup"><span data-stu-id="be6f1-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)


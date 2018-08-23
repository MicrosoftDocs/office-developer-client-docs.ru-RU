---
title: Каноническое свойство PidTagOriginalSentRepresentingAddressType
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagOriginalSentRepresentingAddressType
api_type:
- COM
ms.assetid: 93f40161-d4e5-4ef9-a55f-cee62529fc04
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: ce3678c5137caec2e9f80c7fc15cde0ae99441ae
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22572531"
---
# <a name="pidtagoriginalsentrepresentingaddresstype-canonical-property"></a><span data-ttu-id="117a7-103">Каноническое свойство PidTagOriginalSentRepresentingAddressType</span><span class="sxs-lookup"><span data-stu-id="117a7-103">PidTagOriginalSentRepresentingAddressType Canonical Property</span></span>

  
  
<span data-ttu-id="117a7-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="117a7-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="117a7-105">Содержит тип адреса обмена сообщениями пользователя, от чьего имени исходное сообщение было отправлено.</span><span class="sxs-lookup"><span data-stu-id="117a7-105">Contains the address type of the messaging user on whose behalf the original message was sent.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="117a7-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="117a7-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="117a7-107">PR_ORIGINAL_SENT_REPRESENTING_ADDRTYPE, PR_ORIGINAL_SENT_REPRESENTING_ADDRTYPE_A, PR_ORIGINAL_SENT_REPRESENTING_ADDRTYPE_W</span><span class="sxs-lookup"><span data-stu-id="117a7-107">PR_ORIGINAL_SENT_REPRESENTING_ADDRTYPE, PR_ORIGINAL_SENT_REPRESENTING_ADDRTYPE_A, PR_ORIGINAL_SENT_REPRESENTING_ADDRTYPE_W</span></span>  <br/> |
|<span data-ttu-id="117a7-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="117a7-108">Identifier:</span></span>  <br/> |<span data-ttu-id="117a7-109">0x0068</span><span class="sxs-lookup"><span data-stu-id="117a7-109">0x0068</span></span>  <br/> |
|<span data-ttu-id="117a7-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="117a7-110">Data type:</span></span>  <br/> |<span data-ttu-id="117a7-111">PT_STRING8 PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="117a7-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="117a7-112">Область:</span><span class="sxs-lookup"><span data-stu-id="117a7-112">Area:</span></span>  <br/> |<span data-ttu-id="117a7-113">Общие системы обмена сообщениями</span><span class="sxs-lookup"><span data-stu-id="117a7-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="117a7-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="117a7-114">Remarks</span></span>

<span data-ttu-id="117a7-115">Эти свойства — это тип для представленного отправителю сообщения.</span><span class="sxs-lookup"><span data-stu-id="117a7-115">These properties are the type for the original represented sender of a message.</span></span> <span data-ttu-id="117a7-116">Они используются в потоке беседы.</span><span class="sxs-lookup"><span data-stu-id="117a7-116">They are used in a conversation thread.</span></span>
  
<span data-ttu-id="117a7-117">Клиентское приложение отправку сообщения от имени другого клиента эти свойства присвоено значение свойства **PR_SENT_REPRESENTING_ADDRTYPE** ([PidTagSentRepresentingAddressType](pidtagsentrepresentingaddresstype-canonical-property.md)) в первой отправки сообщения.</span><span class="sxs-lookup"><span data-stu-id="117a7-117">A client application sending a message on behalf of another client should set these properties to the value of the **PR_SENT_REPRESENTING_ADDRTYPE** ([PidTagSentRepresentingAddressType](pidtagsentrepresentingaddresstype-canonical-property.md)) property at the first submission of the message.</span></span> <span data-ttu-id="117a7-118">После установки, оно должно быть задано.</span><span class="sxs-lookup"><span data-stu-id="117a7-118">Once set, it should never be changed.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="117a7-119">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="117a7-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="117a7-120">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="117a7-120">Protocol specifications</span></span>

<span data-ttu-id="117a7-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="117a7-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="117a7-122">Содержит ссылки на связанные спецификаций протокола Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="117a7-122">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="117a7-123">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="117a7-123">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="117a7-124">Задает свойства и операции, допустимые для объектов сообщения электронной почты.</span><span class="sxs-lookup"><span data-stu-id="117a7-124">Specifies the properties and operations that are permissible on email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="117a7-125">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="117a7-125">Header files</span></span>

<span data-ttu-id="117a7-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="117a7-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="117a7-127">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="117a7-127">Provides data type definitions.</span></span>
    
<span data-ttu-id="117a7-128">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="117a7-128">Mapitags.h</span></span>
  
> <span data-ttu-id="117a7-129">Содержит определения свойства в списке альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="117a7-129">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="117a7-130">См. также</span><span class="sxs-lookup"><span data-stu-id="117a7-130">See also</span></span>



[<span data-ttu-id="117a7-131">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="117a7-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="117a7-132">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="117a7-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="117a7-133">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="117a7-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="117a7-134">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="117a7-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)


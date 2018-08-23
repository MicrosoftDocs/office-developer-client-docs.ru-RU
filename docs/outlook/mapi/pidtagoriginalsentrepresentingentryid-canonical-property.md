---
title: Каноническое свойство PidTagOriginalSentRepresentingEntryId
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagOriginalSentRepresentingEntryId
api_type:
- COM
ms.assetid: ece3df57-47f3-4d27-854f-b511c920ac75
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: bac1d53b890df056ff15cd6d3ad665f50e3ce3f6
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22580959"
---
# <a name="pidtagoriginalsentrepresentingentryid-canonical-property"></a><span data-ttu-id="e1116-103">Каноническое свойство PidTagOriginalSentRepresentingEntryId</span><span class="sxs-lookup"><span data-stu-id="e1116-103">PidTagOriginalSentRepresentingEntryId Canonical Property</span></span>

  
  
<span data-ttu-id="e1116-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e1116-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e1116-105">Содержит идентификатор записи обмена сообщениями пользователя, от чьего имени исходное сообщение было отправлено.</span><span class="sxs-lookup"><span data-stu-id="e1116-105">Contains the entry identifier of the messaging user on whose behalf the original message was sent.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="e1116-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="e1116-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="e1116-107">PR_ORIGINAL_SENT_REPRESENTING_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="e1116-107">PR_ORIGINAL_SENT_REPRESENTING_ENTRYID</span></span>  <br/> |
|<span data-ttu-id="e1116-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="e1116-108">Identifier:</span></span>  <br/> |<span data-ttu-id="e1116-109">0x005E</span><span class="sxs-lookup"><span data-stu-id="e1116-109">0x005E</span></span>  <br/> |
|<span data-ttu-id="e1116-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="e1116-110">Data type:</span></span>  <br/> |<span data-ttu-id="e1116-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="e1116-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="e1116-112">Область:</span><span class="sxs-lookup"><span data-stu-id="e1116-112">Area:</span></span>  <br/> |<span data-ttu-id="e1116-113">Общие системы обмена сообщениями</span><span class="sxs-lookup"><span data-stu-id="e1116-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e1116-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="e1116-114">Remarks</span></span>

<span data-ttu-id="e1116-115">Это свойство является одним из свойств адреса для представленного отправителю сообщения.</span><span class="sxs-lookup"><span data-stu-id="e1116-115">This property is one of the address properties for the original represented sender of a message.</span></span> <span data-ttu-id="e1116-116">Он используется в потоке беседы.</span><span class="sxs-lookup"><span data-stu-id="e1116-116">It is used in a conversation thread.</span></span>
  
<span data-ttu-id="e1116-117">Клиентское приложение отправку сообщения от имени другого клиента этому свойству присвоено значение свойства **PR_SENT_REPRESENTING_ENTRYID** ([PidTagSentRepresentingEntryId](pidtagsentrepresentingentryid-canonical-property.md)) в первой отправки сообщения.</span><span class="sxs-lookup"><span data-stu-id="e1116-117">A client application sending a message on behalf of another client should set this property to the value of the **PR_SENT_REPRESENTING_ENTRYID** ([PidTagSentRepresentingEntryId](pidtagsentrepresentingentryid-canonical-property.md)) property at the first submission of the message.</span></span> <span data-ttu-id="e1116-118">После установки, оно должно быть задано.</span><span class="sxs-lookup"><span data-stu-id="e1116-118">Once set, it should never be changed.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="e1116-119">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="e1116-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="e1116-120">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="e1116-120">Protocol specifications</span></span>

<span data-ttu-id="e1116-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e1116-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e1116-122">Содержит ссылки на связанные спецификаций протокола Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="e1116-122">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="e1116-123">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e1116-123">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e1116-124">Задает свойства и операции, допустимые для объектов сообщения электронной почты.</span><span class="sxs-lookup"><span data-stu-id="e1116-124">Specifies the properties and operations that are permissible on email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="e1116-125">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="e1116-125">Header files</span></span>

<span data-ttu-id="e1116-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="e1116-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="e1116-127">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="e1116-127">Provides data type definitions.</span></span>
    
<span data-ttu-id="e1116-128">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="e1116-128">Mapitags.h</span></span>
  
> <span data-ttu-id="e1116-129">Содержит определения свойства в списке альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="e1116-129">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="e1116-130">См. также</span><span class="sxs-lookup"><span data-stu-id="e1116-130">See also</span></span>



[<span data-ttu-id="e1116-131">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="e1116-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="e1116-132">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="e1116-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="e1116-133">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="e1116-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="e1116-134">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="e1116-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)


---
title: Каноническое свойство PidTagOriginalSentRepresentingEmailAddress
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_type:
- COM
ms.assetid: e2c3d2c3-5451-45cb-b0ec-bdbf5b39a0ba
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: bfb771c4c5972a770910936b6220c9e11b24e355
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19811457"
---
# <a name="pidtagoriginalsentrepresentingemailaddress-canonical-property"></a><span data-ttu-id="2182e-103">Каноническое свойство PidTagOriginalSentRepresentingEmailAddress</span><span class="sxs-lookup"><span data-stu-id="2182e-103">PidTagOriginalSentRepresentingEmailAddress Canonical Property</span></span>

  
  
<span data-ttu-id="2182e-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="2182e-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="2182e-105">Содержит адрес электронной почты, обмена мгновенными сообщениями пользователя, от чьего имени исходное сообщение было отправлено.</span><span class="sxs-lookup"><span data-stu-id="2182e-105">Contains the email address of the messaging user on whose behalf the original message was sent.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="2182e-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="2182e-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="2182e-107">PR_ORIGINAL_SENT_REPRESENTING_EMAIL_ADDRESS, PR_ORIGINAL_SENT_REPRESENTING_EMAIL_ADDRESS_A, PR_ORIGINAL_SENT_REPRESENTING_EMAIL_ADDRESS_W</span><span class="sxs-lookup"><span data-stu-id="2182e-107">PR_ORIGINAL_SENT_REPRESENTING_EMAIL_ADDRESS, PR_ORIGINAL_SENT_REPRESENTING_EMAIL_ADDRESS_A, PR_ORIGINAL_SENT_REPRESENTING_EMAIL_ADDRESS_W</span></span>  <br/> |
|<span data-ttu-id="2182e-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="2182e-108">Identifier:</span></span>  <br/> |<span data-ttu-id="2182e-109">0x0069</span><span class="sxs-lookup"><span data-stu-id="2182e-109">0x0069</span></span>  <br/> |
|<span data-ttu-id="2182e-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="2182e-110">Data type:</span></span>  <br/> |<span data-ttu-id="2182e-111">PT_STRING8 PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="2182e-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="2182e-112">Область:</span><span class="sxs-lookup"><span data-stu-id="2182e-112">Area:</span></span>  <br/> |<span data-ttu-id="2182e-113">Общие системы обмена сообщениями</span><span class="sxs-lookup"><span data-stu-id="2182e-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="2182e-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="2182e-114">Remarks</span></span>

<span data-ttu-id="2182e-115">Эти свойства являются примерами свойства адреса для исходного представленного отправителя сообщения.</span><span class="sxs-lookup"><span data-stu-id="2182e-115">These properties are examples of the address properties for the original represented sender of a message.</span></span> <span data-ttu-id="2182e-116">Он используется в потоке беседы.</span><span class="sxs-lookup"><span data-stu-id="2182e-116">It is used in a conversation thread.</span></span>
  
<span data-ttu-id="2182e-117">Клиентское приложение отправку сообщения от имени другого клиента эти свойства присвоено значение свойства **PR_SENT_REPRESENTING_EMAIL_ADDRESS** ([PidTagSentRepresentingEmailAddress](pidtagsentrepresentingemailaddress-canonical-property.md)) в первой отправки сообщения.</span><span class="sxs-lookup"><span data-stu-id="2182e-117">A client application sending a message on behalf of another client should set these properties to the value of the **PR_SENT_REPRESENTING_EMAIL_ADDRESS** ([PidTagSentRepresentingEmailAddress](pidtagsentrepresentingemailaddress-canonical-property.md)) property at the first submission of the message.</span></span> <span data-ttu-id="2182e-118">После установки, оно должно быть задано.</span><span class="sxs-lookup"><span data-stu-id="2182e-118">Once set, it should never be changed.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="2182e-119">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="2182e-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="2182e-120">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="2182e-120">Protocol specifications</span></span>

<span data-ttu-id="2182e-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="2182e-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="2182e-122">Содержит ссылки на связанные спецификаций протокола Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="2182e-122">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="2182e-123">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="2182e-123">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="2182e-124">Задает свойства и операции, допустимые для объектов сообщения электронной почты.</span><span class="sxs-lookup"><span data-stu-id="2182e-124">Specifies the properties and operations that are permissible on email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="2182e-125">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="2182e-125">Header files</span></span>

<span data-ttu-id="2182e-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="2182e-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="2182e-127">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="2182e-127">Provides data type definitions.</span></span>
    
<span data-ttu-id="2182e-128">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="2182e-128">Mapitags.h</span></span>
  
> <span data-ttu-id="2182e-129">Содержит определения свойства в списке альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="2182e-129">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="2182e-130">См. также</span><span class="sxs-lookup"><span data-stu-id="2182e-130">See also</span></span>



[<span data-ttu-id="2182e-131">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="2182e-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="2182e-132">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="2182e-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="2182e-133">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="2182e-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="2182e-134">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="2182e-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)


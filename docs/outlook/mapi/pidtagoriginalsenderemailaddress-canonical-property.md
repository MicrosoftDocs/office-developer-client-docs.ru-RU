---
title: Каноническое свойство PidTagOriginalSenderEmailAddress
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagOriginalSenderEmailAddress
api_type:
- COM
ms.assetid: cc86505c-e264-435f-ae21-4a10f0bbf082
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 927710f3530fd95cc1c1ba548870c1058ad7a819
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22567435"
---
# <a name="pidtagoriginalsenderemailaddress-canonical-property"></a><span data-ttu-id="e7438-103">Каноническое свойство PidTagOriginalSenderEmailAddress</span><span class="sxs-lookup"><span data-stu-id="e7438-103">PidTagOriginalSenderEmailAddress Canonical Property</span></span>

  
  
<span data-ttu-id="e7438-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e7438-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e7438-105">Содержит адрес электронной почты отправителя первая версия сообщения, то есть, сообщение перед пересылку и ответ.</span><span class="sxs-lookup"><span data-stu-id="e7438-105">Contains the email address of the sender of the first version of a message, that is, the message before being forwarded or replied to.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="e7438-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="e7438-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="e7438-107">PR_ORIGINAL_SENDER_EMAIL_ADDRESS, PR_ORIGINAL_SENDER_EMAIL_ADDRESS_A, PR_ORIGINAL_SENDER_EMAIL_ADDRESS_W</span><span class="sxs-lookup"><span data-stu-id="e7438-107">PR_ORIGINAL_SENDER_EMAIL_ADDRESS, PR_ORIGINAL_SENDER_EMAIL_ADDRESS_A, PR_ORIGINAL_SENDER_EMAIL_ADDRESS_W</span></span>  <br/> |
|<span data-ttu-id="e7438-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="e7438-108">Identifier:</span></span>  <br/> |<span data-ttu-id="e7438-109">0x0067</span><span class="sxs-lookup"><span data-stu-id="e7438-109">0x0067</span></span>  <br/> |
|<span data-ttu-id="e7438-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="e7438-110">Data type:</span></span>  <br/> |<span data-ttu-id="e7438-111">PT_STRING8 PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="e7438-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="e7438-112">Область:</span><span class="sxs-lookup"><span data-stu-id="e7438-112">Area:</span></span>  <br/> |<span data-ttu-id="e7438-113">Общие системы обмена сообщениями</span><span class="sxs-lookup"><span data-stu-id="e7438-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e7438-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="e7438-114">Remarks</span></span>

<span data-ttu-id="e7438-115">Эти свойства являются примерами свойства адреса для исходного отправителя сообщения.</span><span class="sxs-lookup"><span data-stu-id="e7438-115">These properties are examples of the address properties for the original sender of a message.</span></span> <span data-ttu-id="e7438-116">В первой отправки сообщения клиентское приложение следует этому свойству присвоено значение значение **PR_SENDER_EMAIL_ADDRESS** ([PidTagSenderEmailAddress](pidtagsenderemailaddress-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="e7438-116">At first submission of the message, the client application should set this property to the value of **PR_SENDER_EMAIL_ADDRESS** ([PidTagSenderEmailAddress](pidtagsenderemailaddress-canonical-property.md)).</span></span> <span data-ttu-id="e7438-117">Никогда не изменяется при сообщение будет переслано или ответ.</span><span class="sxs-lookup"><span data-stu-id="e7438-117">It is never changed when the message is forwarded or replied to.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="e7438-118">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="e7438-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="e7438-119">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="e7438-119">Protocol specifications</span></span>

<span data-ttu-id="e7438-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e7438-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e7438-121">Содержит ссылки на связанные спецификаций протокола Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="e7438-121">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="e7438-122">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e7438-122">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e7438-123">Задает свойства и операции, допустимые для объектов сообщения электронной почты.</span><span class="sxs-lookup"><span data-stu-id="e7438-123">Specifies the properties and operations that are permissible on email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="e7438-124">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="e7438-124">Header files</span></span>

<span data-ttu-id="e7438-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="e7438-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="e7438-126">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="e7438-126">Provides data type definitions.</span></span>
    
<span data-ttu-id="e7438-127">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="e7438-127">Mapitags.h</span></span>
  
> <span data-ttu-id="e7438-128">Содержит определения свойства в списке альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="e7438-128">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="e7438-129">См. также</span><span class="sxs-lookup"><span data-stu-id="e7438-129">See also</span></span>



[<span data-ttu-id="e7438-130">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="e7438-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="e7438-131">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="e7438-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="e7438-132">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="e7438-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="e7438-133">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="e7438-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)


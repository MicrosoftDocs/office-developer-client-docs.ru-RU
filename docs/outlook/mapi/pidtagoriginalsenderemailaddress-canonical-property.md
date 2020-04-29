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
ms.openlocfilehash: ed3d84667d7be9c06d0ddf4d896b8888694edc12
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32355274"
---
# <a name="pidtagoriginalsenderemailaddress-canonical-property"></a><span data-ttu-id="2721b-103">Каноническое свойство PidTagOriginalSenderEmailAddress</span><span class="sxs-lookup"><span data-stu-id="2721b-103">PidTagOriginalSenderEmailAddress Canonical Property</span></span>

  
  
<span data-ttu-id="2721b-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2721b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2721b-105">Содержит адрес электронной почты отправителя первой версии сообщения, то есть сообщение перед пересылкой или ответом.</span><span class="sxs-lookup"><span data-stu-id="2721b-105">Contains the email address of the sender of the first version of a message, that is, the message before being forwarded or replied to.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="2721b-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="2721b-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="2721b-107">PR_ORIGINAL_SENDER_EMAIL_ADDRESS, PR_ORIGINAL_SENDER_EMAIL_ADDRESS_A PR_ORIGINAL_SENDER_EMAIL_ADDRESS_W</span><span class="sxs-lookup"><span data-stu-id="2721b-107">PR_ORIGINAL_SENDER_EMAIL_ADDRESS, PR_ORIGINAL_SENDER_EMAIL_ADDRESS_A, PR_ORIGINAL_SENDER_EMAIL_ADDRESS_W</span></span>  <br/> |
|<span data-ttu-id="2721b-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="2721b-108">Identifier:</span></span>  <br/> |<span data-ttu-id="2721b-109">0x0067</span><span class="sxs-lookup"><span data-stu-id="2721b-109">0x0067</span></span>  <br/> |
|<span data-ttu-id="2721b-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="2721b-110">Data type:</span></span>  <br/> |<span data-ttu-id="2721b-111">PT_STRING8 PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="2721b-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="2721b-112">Область:</span><span class="sxs-lookup"><span data-stu-id="2721b-112">Area:</span></span>  <br/> |<span data-ttu-id="2721b-113">Общий обмен сообщениями</span><span class="sxs-lookup"><span data-stu-id="2721b-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="2721b-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="2721b-114">Remarks</span></span>

<span data-ttu-id="2721b-115">Эти свойства являются примерами свойств адреса для исходного отправителя сообщения.</span><span class="sxs-lookup"><span data-stu-id="2721b-115">These properties are examples of the address properties for the original sender of a message.</span></span> <span data-ttu-id="2721b-116">При первой отправке сообщения клиентскому приложению следует присвоить этому свойству значение **PR_SENDER_EMAIL_ADDRESS** ([PidTagSenderEmailAddress](pidtagsenderemailaddress-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="2721b-116">At first submission of the message, the client application should set this property to the value of **PR_SENDER_EMAIL_ADDRESS** ([PidTagSenderEmailAddress](pidtagsenderemailaddress-canonical-property.md)).</span></span> <span data-ttu-id="2721b-117">Он никогда не изменяется при пересылке сообщения или ответе на него.</span><span class="sxs-lookup"><span data-stu-id="2721b-117">It is never changed when the message is forwarded or replied to.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="2721b-118">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="2721b-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="2721b-119">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="2721b-119">Protocol specifications</span></span>

<span data-ttu-id="2721b-120">[[MS — ОКСПРОПС]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="2721b-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="2721b-121">Содержит ссылки на соответствующие спецификации протоколов Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="2721b-121">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="2721b-122">[[MS — ОКСОМСГ]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="2721b-122">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="2721b-123">Задает свойства и операции, допустимые для объектов сообщений электронной почты.</span><span class="sxs-lookup"><span data-stu-id="2721b-123">Specifies the properties and operations that are permissible on email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="2721b-124">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="2721b-124">Header files</span></span>

<span data-ttu-id="2721b-125">MAPIDEFS. h</span><span class="sxs-lookup"><span data-stu-id="2721b-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="2721b-126">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="2721b-126">Provides data type definitions.</span></span>
    
<span data-ttu-id="2721b-127">Мапитагс. h</span><span class="sxs-lookup"><span data-stu-id="2721b-127">Mapitags.h</span></span>
  
> <span data-ttu-id="2721b-128">Содержит определения свойств, перечисленных как альтернативные имена.</span><span class="sxs-lookup"><span data-stu-id="2721b-128">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="2721b-129">См. также</span><span class="sxs-lookup"><span data-stu-id="2721b-129">See also</span></span>



[<span data-ttu-id="2721b-130">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="2721b-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="2721b-131">Каноническое свойство MAPI</span><span class="sxs-lookup"><span data-stu-id="2721b-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="2721b-132">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="2721b-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="2721b-133">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="2721b-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)


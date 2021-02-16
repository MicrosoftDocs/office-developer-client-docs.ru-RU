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
ms.openlocfilehash: 2530e27993163505b28fa7d08fd5caf4cc9b03be
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341190"
---
# <a name="pidtagoriginalsentrepresentingemailaddress-canonical-property"></a><span data-ttu-id="b307a-103">Каноническое свойство PidTagOriginalSentRepresentingEmailAddress</span><span class="sxs-lookup"><span data-stu-id="b307a-103">PidTagOriginalSentRepresentingEmailAddress Canonical Property</span></span>

  
  
<span data-ttu-id="b307a-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b307a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b307a-105">Содержит адрес электронной почты пользователя обмена сообщениями, от имени которого было отправлено исходное сообщение.</span><span class="sxs-lookup"><span data-stu-id="b307a-105">Contains the email address of the messaging user on whose behalf the original message was sent.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="b307a-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="b307a-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="b307a-107">PR_ORIGINAL_SENT_REPRESENTING_EMAIL_ADDRESS, PR_ORIGINAL_SENT_REPRESENTING_EMAIL_ADDRESS_A, PR_ORIGINAL_SENT_REPRESENTING_EMAIL_ADDRESS_W</span><span class="sxs-lookup"><span data-stu-id="b307a-107">PR_ORIGINAL_SENT_REPRESENTING_EMAIL_ADDRESS, PR_ORIGINAL_SENT_REPRESENTING_EMAIL_ADDRESS_A, PR_ORIGINAL_SENT_REPRESENTING_EMAIL_ADDRESS_W</span></span>  <br/> |
|<span data-ttu-id="b307a-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="b307a-108">Identifier:</span></span>  <br/> |<span data-ttu-id="b307a-109">0x0069</span><span class="sxs-lookup"><span data-stu-id="b307a-109">0x0069</span></span>  <br/> |
|<span data-ttu-id="b307a-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="b307a-110">Data type:</span></span>  <br/> |<span data-ttu-id="b307a-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="b307a-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="b307a-112">Область:</span><span class="sxs-lookup"><span data-stu-id="b307a-112">Area:</span></span>  <br/> |<span data-ttu-id="b307a-113">Общие сообщения</span><span class="sxs-lookup"><span data-stu-id="b307a-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b307a-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="b307a-114">Remarks</span></span>

<span data-ttu-id="b307a-115">Эти свойства являются примерами свойств адреса для исходного представленного отправитель сообщения.</span><span class="sxs-lookup"><span data-stu-id="b307a-115">These properties are examples of the address properties for the original represented sender of a message.</span></span> <span data-ttu-id="b307a-116">Он используется в цепочке беседы.</span><span class="sxs-lookup"><span data-stu-id="b307a-116">It is used in a conversation thread.</span></span>
  
<span data-ttu-id="b307a-117">Клиентские приложения, отправляющие сообщение от имени другого клиента, должны установить для этих свойств значение свойства **PR_SENT_REPRESENTING_EMAIL_ADDRESS** [(PidTagSentRepresentingEmailAddress)](pidtagsentrepresentingemailaddress-canonical-property.md)при первой отправке сообщения.</span><span class="sxs-lookup"><span data-stu-id="b307a-117">A client application sending a message on behalf of another client should set these properties to the value of the **PR_SENT_REPRESENTING_EMAIL_ADDRESS** ([PidTagSentRepresentingEmailAddress](pidtagsentrepresentingemailaddress-canonical-property.md)) property at the first submission of the message.</span></span> <span data-ttu-id="b307a-118">После этого его не следует менять.</span><span class="sxs-lookup"><span data-stu-id="b307a-118">Once set, it should never be changed.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="b307a-119">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="b307a-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="b307a-120">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="b307a-120">Protocol specifications</span></span>

<span data-ttu-id="b307a-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b307a-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="b307a-122">Содержит ссылки на связанные Exchange Server протоколы.</span><span class="sxs-lookup"><span data-stu-id="b307a-122">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="b307a-123">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b307a-123">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="b307a-124">Указывает свойства и операции, допустимые для объектов сообщений электронной почты.</span><span class="sxs-lookup"><span data-stu-id="b307a-124">Specifies the properties and operations that are permissible on email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="b307a-125">Файлы заголовок</span><span class="sxs-lookup"><span data-stu-id="b307a-125">Header files</span></span>

<span data-ttu-id="b307a-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="b307a-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="b307a-127">Предоставляет определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="b307a-127">Provides data type definitions.</span></span>
    
<span data-ttu-id="b307a-128">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="b307a-128">Mapitags.h</span></span>
  
> <span data-ttu-id="b307a-129">Содержит определения свойств, перечисленных в качестве альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="b307a-129">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="b307a-130">См. также</span><span class="sxs-lookup"><span data-stu-id="b307a-130">See also</span></span>



[<span data-ttu-id="b307a-131">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="b307a-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="b307a-132">Канонические свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="b307a-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="b307a-133">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="b307a-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="b307a-134">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="b307a-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)


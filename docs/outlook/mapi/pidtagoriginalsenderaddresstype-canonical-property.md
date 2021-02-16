---
title: Каноническое свойство PidTagOriginalSenderAddressType
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagOriginalSenderAddressType
api_type:
- COM
ms.assetid: bd777f19-cbb1-4497-8a0b-e05b491c6957
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: d593b5ae1c2341ae0972ba68bcf42dde64e9a2f1
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32342681"
---
# <a name="pidtagoriginalsenderaddresstype-canonical-property"></a><span data-ttu-id="7a489-103">Каноническое свойство PidTagOriginalSenderAddressType</span><span class="sxs-lookup"><span data-stu-id="7a489-103">PidTagOriginalSenderAddressType Canonical Property</span></span>

  
  
<span data-ttu-id="7a489-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7a489-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7a489-105">Содержит тип адреса отправитель первой версии сообщения, то есть сообщение перед переадаемой или ответом.</span><span class="sxs-lookup"><span data-stu-id="7a489-105">Contains the address type of the sender of the first version of a message, that is, the message before being forwarded or replied to.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="7a489-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="7a489-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="7a489-107">PR_ORIGINAL_SENDER_ADDRTYPE, PR_ORIGINAL_SENDER_ADDRTYPE_A, PR_ORIGINAL_SENDER_ADDRTYPE_W</span><span class="sxs-lookup"><span data-stu-id="7a489-107">PR_ORIGINAL_SENDER_ADDRTYPE, PR_ORIGINAL_SENDER_ADDRTYPE_A, PR_ORIGINAL_SENDER_ADDRTYPE_W</span></span>  <br/> |
|<span data-ttu-id="7a489-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="7a489-108">Identifier:</span></span>  <br/> |<span data-ttu-id="7a489-109">0x0066</span><span class="sxs-lookup"><span data-stu-id="7a489-109">0x0066</span></span>  <br/> |
|<span data-ttu-id="7a489-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="7a489-110">Data type:</span></span>  <br/> |<span data-ttu-id="7a489-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="7a489-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="7a489-112">Область:</span><span class="sxs-lookup"><span data-stu-id="7a489-112">Area:</span></span>  <br/> |<span data-ttu-id="7a489-113">Общие сообщения</span><span class="sxs-lookup"><span data-stu-id="7a489-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="7a489-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="7a489-114">Remarks</span></span>

<span data-ttu-id="7a489-115">Эти свойства являются примерами свойств адреса исходного отправитель сообщения.</span><span class="sxs-lookup"><span data-stu-id="7a489-115">These properties are examples of the address properties for the original sender of a message.</span></span> <span data-ttu-id="7a489-116">При первой отправке сообщения клиентский приложение должно установить для этих свойств значение **PR_SENDER_ADDRTYPE** ([PidTagSenderAddressType).](pidtagsenderaddresstype-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="7a489-116">At first submission of the message, the client application should set these properties to the value of **PR_SENDER_ADDRTYPE** ([PidTagSenderAddressType](pidtagsenderaddresstype-canonical-property.md)).</span></span> <span data-ttu-id="7a489-117">Оно никогда не меняется, когда сообщение переадовыно или отвечает на него.</span><span class="sxs-lookup"><span data-stu-id="7a489-117">It is never changed when the message is forwarded or replied to.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="7a489-118">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="7a489-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="7a489-119">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="7a489-119">Protocol specifications</span></span>

<span data-ttu-id="7a489-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="7a489-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="7a489-121">Содержит ссылки на связанные Exchange Server протоколы.</span><span class="sxs-lookup"><span data-stu-id="7a489-121">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="7a489-122">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="7a489-122">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="7a489-123">Указывает свойства и операции, которые разрешены для объектов сообщений электронной почты.</span><span class="sxs-lookup"><span data-stu-id="7a489-123">Specifies the properties and operations that are permissible on email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="7a489-124">Файлы заголовок</span><span class="sxs-lookup"><span data-stu-id="7a489-124">Header files</span></span>

<span data-ttu-id="7a489-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="7a489-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="7a489-126">Предоставляет определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="7a489-126">Provides data type definitions.</span></span>
    
<span data-ttu-id="7a489-127">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="7a489-127">Mapitags.h</span></span>
  
> <span data-ttu-id="7a489-128">Содержит определения свойств, перечисленных в качестве альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="7a489-128">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="7a489-129">См. также</span><span class="sxs-lookup"><span data-stu-id="7a489-129">See also</span></span>



[<span data-ttu-id="7a489-130">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="7a489-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="7a489-131">Канонические свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="7a489-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="7a489-132">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="7a489-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="7a489-133">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="7a489-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)


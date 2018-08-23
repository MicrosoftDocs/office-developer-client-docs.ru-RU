---
title: Каноническое свойство PidTagReceivedByAddressType
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagReceivedByAddressType
api_type:
- COM
ms.assetid: 0eef299d-6923-4dae-9a18-91ea82ea0f3e
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: cd7a287a2240d372edf6cca6bac522266c0ca620
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22581169"
---
# <a name="pidtagreceivedbyaddresstype-canonical-property"></a><span data-ttu-id="5f2b4-103">Каноническое свойство PidTagReceivedByAddressType</span><span class="sxs-lookup"><span data-stu-id="5f2b4-103">PidTagReceivedByAddressType Canonical Property</span></span>

  
  
<span data-ttu-id="5f2b4-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5f2b4-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5f2b4-105">Содержит тип адреса электронной почты, таких как SMTP, для обмена сообщениями пользователя, который получает сообщение.</span><span class="sxs-lookup"><span data-stu-id="5f2b4-105">Contains the email address type, such as SMTP, for the messaging user who actually receives the message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="5f2b4-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="5f2b4-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="5f2b4-107">PR_RECEIVED_BY_ADDRTYPE, PR_RECEIVED_BY_ADDRTYPE_A, PR_RECEIVED_BY_ADDRTYPE_W</span><span class="sxs-lookup"><span data-stu-id="5f2b4-107">PR_RECEIVED_BY_ADDRTYPE, PR_RECEIVED_BY_ADDRTYPE_A, PR_RECEIVED_BY_ADDRTYPE_W</span></span>  <br/> |
|<span data-ttu-id="5f2b4-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="5f2b4-108">Identifier:</span></span>  <br/> |<span data-ttu-id="5f2b4-109">0x0075</span><span class="sxs-lookup"><span data-stu-id="5f2b4-109">0x0075</span></span>  <br/> |
|<span data-ttu-id="5f2b4-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="5f2b4-110">Data type:</span></span>  <br/> |<span data-ttu-id="5f2b4-111">PT_STRING8 PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="5f2b4-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="5f2b4-112">Область:</span><span class="sxs-lookup"><span data-stu-id="5f2b4-112">Area:</span></span>  <br/> |<span data-ttu-id="5f2b4-113">Конверт MAPI</span><span class="sxs-lookup"><span data-stu-id="5f2b4-113">MAPI envelope</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="5f2b4-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="5f2b4-114">Remarks</span></span>

<span data-ttu-id="5f2b4-115">Эти свойства являются примерами свойства адреса для обмена мгновенными сообщениями пользователя, который получает сообщение.</span><span class="sxs-lookup"><span data-stu-id="5f2b4-115">These properties are examples of the address properties for the messaging user who actually receives the message.</span></span> <span data-ttu-id="5f2b4-116">Им должен иметь значение входящих поставщика транспорта.</span><span class="sxs-lookup"><span data-stu-id="5f2b4-116">They must be set by the incoming transport provider.</span></span>
  
<span data-ttu-id="5f2b4-117">Строка тип адреса может содержать только прописные буквы от A до Z и чисел нулевой до девяти.</span><span class="sxs-lookup"><span data-stu-id="5f2b4-117">The address type string can contain only the uppercase alphabetic characters A through Z and the numbers zero through nine.</span></span> <span data-ttu-id="5f2b4-118">Эти свойства уточнения свойство **PR_RECEIVED_BY_EMAIL_ADDRESS** ([PidTagReceivedByEmailAddress](pidtagreceivedbyemailaddress-canonical-property.md)), указав тип адреса, например SMTP, таким образом, указывающее, как адрес должен быть создан.</span><span class="sxs-lookup"><span data-stu-id="5f2b4-118">These properties qualify the **PR_RECEIVED_BY_EMAIL_ADDRESS** ([PidTagReceivedByEmailAddress](pidtagreceivedbyemailaddress-canonical-property.md)) property by specifying an address type, such as SMTP, thereby indicating how the address should be constructed.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="5f2b4-119">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="5f2b4-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="5f2b4-120">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="5f2b4-120">Protocol specifications</span></span>

<span data-ttu-id="5f2b4-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="5f2b4-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="5f2b4-122">Содержит ссылки на связанные спецификаций протокола Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="5f2b4-122">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="5f2b4-123">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="5f2b4-123">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="5f2b4-124">Задает свойства и операции, допустимые в сообщениях электронной почты.</span><span class="sxs-lookup"><span data-stu-id="5f2b4-124">Specifies the properties and operations that are permissible on email messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="5f2b4-125">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="5f2b4-125">Header files</span></span>

<span data-ttu-id="5f2b4-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="5f2b4-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="5f2b4-127">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="5f2b4-127">Provides data type definitions.</span></span>
    
<span data-ttu-id="5f2b4-128">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="5f2b4-128">Mapitags.h</span></span>
  
> <span data-ttu-id="5f2b4-129">Содержит определения свойства в списке альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="5f2b4-129">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="5f2b4-130">См. также</span><span class="sxs-lookup"><span data-stu-id="5f2b4-130">See also</span></span>



[<span data-ttu-id="5f2b4-131">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="5f2b4-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="5f2b4-132">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="5f2b4-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="5f2b4-133">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="5f2b4-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="5f2b4-134">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="5f2b4-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)


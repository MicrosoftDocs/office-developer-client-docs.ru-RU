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
ms.openlocfilehash: 00c07069ed174fe55556dfe48398d65b4e64100e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359229"
---
# <a name="pidtagreceivedbyaddresstype-canonical-property"></a><span data-ttu-id="f4a25-103">Каноническое свойство PidTagReceivedByAddressType</span><span class="sxs-lookup"><span data-stu-id="f4a25-103">PidTagReceivedByAddressType Canonical Property</span></span>

  
  
<span data-ttu-id="f4a25-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f4a25-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f4a25-105">Содержит тип адреса электронной почты, например SMTP, для пользователя обмена сообщениями, который получает сообщение.</span><span class="sxs-lookup"><span data-stu-id="f4a25-105">Contains the email address type, such as SMTP, for the messaging user who actually receives the message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="f4a25-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="f4a25-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="f4a25-107">PR_RECEIVED_BY_ADDRTYPE, PR_RECEIVED_BY_ADDRTYPE_A, PR_RECEIVED_BY_ADDRTYPE_W</span><span class="sxs-lookup"><span data-stu-id="f4a25-107">PR_RECEIVED_BY_ADDRTYPE, PR_RECEIVED_BY_ADDRTYPE_A, PR_RECEIVED_BY_ADDRTYPE_W</span></span>  <br/> |
|<span data-ttu-id="f4a25-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="f4a25-108">Identifier:</span></span>  <br/> |<span data-ttu-id="f4a25-109">0x0075</span><span class="sxs-lookup"><span data-stu-id="f4a25-109">0x0075</span></span>  <br/> |
|<span data-ttu-id="f4a25-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="f4a25-110">Data type:</span></span>  <br/> |<span data-ttu-id="f4a25-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="f4a25-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="f4a25-112">Область:</span><span class="sxs-lookup"><span data-stu-id="f4a25-112">Area:</span></span>  <br/> |<span data-ttu-id="f4a25-113">Конверт MAPI</span><span class="sxs-lookup"><span data-stu-id="f4a25-113">MAPI envelope</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f4a25-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="f4a25-114">Remarks</span></span>

<span data-ttu-id="f4a25-115">Эти свойства являются примерами свойств адресов для пользователя обмена сообщениями, который получает сообщение.</span><span class="sxs-lookup"><span data-stu-id="f4a25-115">These properties are examples of the address properties for the messaging user who actually receives the message.</span></span> <span data-ttu-id="f4a25-116">Они должны быть установлены поставщиком входящих транспортных средств.</span><span class="sxs-lookup"><span data-stu-id="f4a25-116">They must be set by the incoming transport provider.</span></span>
  
<span data-ttu-id="f4a25-117">Строка типа адресов может содержать только алфавитные символы верхнего регистра A через Z и число от нуля до девяти.</span><span class="sxs-lookup"><span data-stu-id="f4a25-117">The address type string can contain only the uppercase alphabetic characters A through Z and the numbers zero through nine.</span></span> <span data-ttu-id="f4a25-118">Эти свойства квалифицируют **свойство PR_RECEIVED_BY_EMAIL_ADDRESS** [(PidTagReceivedByEmailAddress),](pidtagreceivedbyemailaddress-canonical-property.md)указав тип адреса, например SMTP, указав тем самым, как должен быть построен адрес.</span><span class="sxs-lookup"><span data-stu-id="f4a25-118">These properties qualify the **PR_RECEIVED_BY_EMAIL_ADDRESS** ([PidTagReceivedByEmailAddress](pidtagreceivedbyemailaddress-canonical-property.md)) property by specifying an address type, such as SMTP, thereby indicating how the address should be constructed.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="f4a25-119">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="f4a25-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="f4a25-120">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="f4a25-120">Protocol specifications</span></span>

<span data-ttu-id="f4a25-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f4a25-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="f4a25-122">Содержит ссылки на связанные Exchange Server протоколы.</span><span class="sxs-lookup"><span data-stu-id="f4a25-122">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="f4a25-123">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f4a25-123">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="f4a25-124">Указывает свойства и операции, допустимые в сообщениях электронной почты.</span><span class="sxs-lookup"><span data-stu-id="f4a25-124">Specifies the properties and operations that are permissible on email messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="f4a25-125">Файлы заголовки</span><span class="sxs-lookup"><span data-stu-id="f4a25-125">Header files</span></span>

<span data-ttu-id="f4a25-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="f4a25-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="f4a25-127">Предоставляет определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="f4a25-127">Provides data type definitions.</span></span>
    
<span data-ttu-id="f4a25-128">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="f4a25-128">Mapitags.h</span></span>
  
> <span data-ttu-id="f4a25-129">Содержит определения свойств, перечисленных в качестве альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="f4a25-129">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="f4a25-130">См. также</span><span class="sxs-lookup"><span data-stu-id="f4a25-130">See also</span></span>



[<span data-ttu-id="f4a25-131">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="f4a25-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="f4a25-132">Канонические свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="f4a25-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="f4a25-133">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="f4a25-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="f4a25-134">Сопоставление имен MAPI с каноническими именами свойств</span><span class="sxs-lookup"><span data-stu-id="f4a25-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)


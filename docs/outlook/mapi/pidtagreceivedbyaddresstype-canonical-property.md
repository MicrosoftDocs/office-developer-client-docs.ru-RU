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
# <a name="pidtagreceivedbyaddresstype-canonical-property"></a><span data-ttu-id="36a74-103">Каноническое свойство PidTagReceivedByAddressType</span><span class="sxs-lookup"><span data-stu-id="36a74-103">PidTagReceivedByAddressType Canonical Property</span></span>

  
  
<span data-ttu-id="36a74-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="36a74-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="36a74-105">Содержит тип адреса электронной почты, например, SMTP, для пользователя обмена сообщениями, который действительно получает сообщение.</span><span class="sxs-lookup"><span data-stu-id="36a74-105">Contains the email address type, such as SMTP, for the messaging user who actually receives the message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="36a74-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="36a74-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="36a74-107">ПР_РЕЦЕИВЕД_БИ_АДДРТИПЕ, ПР_РЕЦЕИВЕД_БИ_АДДРТИПЕ_А, ПР_РЕЦЕИВЕД_БИ_АДДРТИПЕ_В</span><span class="sxs-lookup"><span data-stu-id="36a74-107">PR_RECEIVED_BY_ADDRTYPE, PR_RECEIVED_BY_ADDRTYPE_A, PR_RECEIVED_BY_ADDRTYPE_W</span></span>  <br/> |
|<span data-ttu-id="36a74-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="36a74-108">Identifier:</span></span>  <br/> |<span data-ttu-id="36a74-109">0x0075</span><span class="sxs-lookup"><span data-stu-id="36a74-109">0x0075</span></span>  <br/> |
|<span data-ttu-id="36a74-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="36a74-110">Data type:</span></span>  <br/> |<span data-ttu-id="36a74-111">PT_STRING8, ПТ_УНИКОДЕ</span><span class="sxs-lookup"><span data-stu-id="36a74-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="36a74-112">Область:</span><span class="sxs-lookup"><span data-stu-id="36a74-112">Area:</span></span>  <br/> |<span data-ttu-id="36a74-113">Конверт MAPI</span><span class="sxs-lookup"><span data-stu-id="36a74-113">MAPI envelope</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="36a74-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="36a74-114">Remarks</span></span>

<span data-ttu-id="36a74-115">Эти свойства являются примерами свойств адресов для пользователя обмена сообщениями, который действительно получает сообщение.</span><span class="sxs-lookup"><span data-stu-id="36a74-115">These properties are examples of the address properties for the messaging user who actually receives the message.</span></span> <span data-ttu-id="36a74-116">Они должны быть заданы входящим поставщиком транспорта.</span><span class="sxs-lookup"><span data-stu-id="36a74-116">They must be set by the incoming transport provider.</span></span>
  
<span data-ttu-id="36a74-117">Строка типа адреса может содержать только прописные буквы от A до Z и цифры от нуля до девяти.</span><span class="sxs-lookup"><span data-stu-id="36a74-117">The address type string can contain only the uppercase alphabetic characters A through Z and the numbers zero through nine.</span></span> <span data-ttu-id="36a74-118">Эти свойства квалифицируют свойство **пр_рецеивед_би_емаил_аддресс** ([PidTagReceivedByEmailAddress](pidtagreceivedbyemailaddress-canonical-property.md)), указывая тип адреса, например SMTP, таким образом указывая, как должен быть создан адрес.</span><span class="sxs-lookup"><span data-stu-id="36a74-118">These properties qualify the **PR_RECEIVED_BY_EMAIL_ADDRESS** ([PidTagReceivedByEmailAddress](pidtagreceivedbyemailaddress-canonical-property.md)) property by specifying an address type, such as SMTP, thereby indicating how the address should be constructed.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="36a74-119">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="36a74-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="36a74-120">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="36a74-120">Protocol specifications</span></span>

<span data-ttu-id="36a74-121">[[MS — ОКСПРОПС]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="36a74-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="36a74-122">Содержит ссылки на соответствующие спецификации протоколов Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="36a74-122">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="36a74-123">[[MS — ОКСОМСГ]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="36a74-123">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="36a74-124">Задает свойства и операции, допустимые для сообщений электронной почты.</span><span class="sxs-lookup"><span data-stu-id="36a74-124">Specifies the properties and operations that are permissible on email messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="36a74-125">Файлы заГоловков</span><span class="sxs-lookup"><span data-stu-id="36a74-125">Header files</span></span>

<span data-ttu-id="36a74-126">MAPIDEFS. h</span><span class="sxs-lookup"><span data-stu-id="36a74-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="36a74-127">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="36a74-127">Provides data type definitions.</span></span>
    
<span data-ttu-id="36a74-128">Мапитагс. h</span><span class="sxs-lookup"><span data-stu-id="36a74-128">Mapitags.h</span></span>
  
> <span data-ttu-id="36a74-129">Содержит определения свойств, перечисленных как альтернативные имена.</span><span class="sxs-lookup"><span data-stu-id="36a74-129">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="36a74-130">См. также</span><span class="sxs-lookup"><span data-stu-id="36a74-130">See also</span></span>



[<span data-ttu-id="36a74-131">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="36a74-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="36a74-132">Каноническое свойство MAPI</span><span class="sxs-lookup"><span data-stu-id="36a74-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="36a74-133">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="36a74-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="36a74-134">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="36a74-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)


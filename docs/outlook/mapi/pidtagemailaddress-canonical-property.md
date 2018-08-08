---
title: Каноническое свойство PidTagEmailAddress
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagEmailAddress
api_type:
- HeaderDef
ms.assetid: bbd1e187-172e-4612-9efe-7c8e52967dfe
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: cb8b7d0fca6b30f75bd35d1e4e48fa359100ad18
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19811093"
---
# <a name="pidtagemailaddress-canonical-property"></a><span data-ttu-id="9d1fe-103">Каноническое свойство PidTagEmailAddress</span><span class="sxs-lookup"><span data-stu-id="9d1fe-103">PidTagEmailAddress Canonical Property</span></span>

  
  
<span data-ttu-id="9d1fe-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="9d1fe-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="9d1fe-105">Содержит адрес электронной почты пользователя обмена мгновенными сообщениями.</span><span class="sxs-lookup"><span data-stu-id="9d1fe-105">Contains the messaging user's email address.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="9d1fe-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="9d1fe-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="9d1fe-107">PR_EMAIL_ADDRESS, PR_EMAIL_ADDRESS_A, PR_EMAIL_ADDRESS_W</span><span class="sxs-lookup"><span data-stu-id="9d1fe-107">PR_EMAIL_ADDRESS, PR_EMAIL_ADDRESS_A, PR_EMAIL_ADDRESS_W</span></span>  <br/> |
|<span data-ttu-id="9d1fe-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="9d1fe-108">Identifier:</span></span>  <br/> |<span data-ttu-id="9d1fe-109">0x3003</span><span class="sxs-lookup"><span data-stu-id="9d1fe-109">0x3003</span></span>  <br/> |
|<span data-ttu-id="9d1fe-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="9d1fe-110">Data type:</span></span>  <br/> |<span data-ttu-id="9d1fe-111">PT_STRING8 PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="9d1fe-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="9d1fe-112">Область:</span><span class="sxs-lookup"><span data-stu-id="9d1fe-112">Area:</span></span>  <br/> |<span data-ttu-id="9d1fe-113">Распространенные MAPI</span><span class="sxs-lookup"><span data-stu-id="9d1fe-113">MAPI common</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="9d1fe-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="9d1fe-114">Remarks</span></span>

<span data-ttu-id="9d1fe-115">Эти свойства являются примерами свойств базовый адрес для всех пользователей, обмена мгновенными сообщениями.</span><span class="sxs-lookup"><span data-stu-id="9d1fe-115">These properties are examples of the base address properties for all messaging users.</span></span> <span data-ttu-id="9d1fe-116">Он является строкой символом null, формат которых имеет значение только для системы обмена сообщениями.</span><span class="sxs-lookup"><span data-stu-id="9d1fe-116">It is a null-terminated string whose format has meaning only for the underlying messaging system.</span></span> 
  
<span data-ttu-id="9d1fe-117">Эти свойства используются в сочетании со свойствами **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)) в адресацию сообщений и **PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="9d1fe-117">These properties are used in conjunction with the **PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md)) and **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)) properties in addressing messages.</span></span> <span data-ttu-id="9d1fe-118">Формат строки определяется **PR_ADDRTYPE**.</span><span class="sxs-lookup"><span data-stu-id="9d1fe-118">The string format is qualified by **PR_ADDRTYPE**.</span></span> 
  
<span data-ttu-id="9d1fe-119">Допустимые значения для этого свойства:</span><span class="sxs-lookup"><span data-stu-id="9d1fe-119">Valid values for this property include:</span></span> 
  
```cpp
network/postoffice/user 
Bruce@XYZZY.COM 
/c=US/a=att/p=Microsoft/o=Finance/ou=Purchasing/s=Furthur/g=Joe 
 
```

## <a name="related-resources"></a><span data-ttu-id="9d1fe-120">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="9d1fe-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="9d1fe-121">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="9d1fe-121">Protocol specifications</span></span>

<span data-ttu-id="9d1fe-122">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="9d1fe-122">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="9d1fe-123">Содержит ссылки на связанные спецификаций протокола Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="9d1fe-123">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="9d1fe-124">[[MS-OXOABK]](http://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="9d1fe-124">[[MS-OXOABK]](http://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="9d1fe-125">Задает свойства и операции для списков пользователей, контактов, групп и ресурсов.</span><span class="sxs-lookup"><span data-stu-id="9d1fe-125">Specifies the properties and operations for lists of users, contacts, groups, and resources.</span></span>
    
<span data-ttu-id="9d1fe-126">[[MS-OXCMAIL]](http://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="9d1fe-126">[[MS-OXCMAIL]](http://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="9d1fe-127">Преобразование conventions стандартных электронной почты Интернета объекты сообщений.</span><span class="sxs-lookup"><span data-stu-id="9d1fe-127">Converts from Internet standard email conventions to message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="9d1fe-128">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="9d1fe-128">Header files</span></span>

<span data-ttu-id="9d1fe-129">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="9d1fe-129">Mapidefs.h</span></span>
  
> <span data-ttu-id="9d1fe-130">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="9d1fe-130">Provides data type definitions.</span></span>
    
<span data-ttu-id="9d1fe-131">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="9d1fe-131">Mapitags.h</span></span>
  
> <span data-ttu-id="9d1fe-132">Содержит определения свойства в списке альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="9d1fe-132">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="9d1fe-133">См. также</span><span class="sxs-lookup"><span data-stu-id="9d1fe-133">See also</span></span>



[<span data-ttu-id="9d1fe-134">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="9d1fe-134">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="9d1fe-135">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="9d1fe-135">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="9d1fe-136">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="9d1fe-136">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="9d1fe-137">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="9d1fe-137">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)


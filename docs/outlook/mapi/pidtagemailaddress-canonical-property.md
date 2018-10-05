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
ms.openlocfilehash: efcb72d872836adce544f3a90cf093de1f3713a7
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25393882"
---
# <a name="pidtagemailaddress-canonical-property"></a><span data-ttu-id="7aa16-103">Каноническое свойство PidTagEmailAddress</span><span class="sxs-lookup"><span data-stu-id="7aa16-103">PidTagEmailAddress Canonical Property</span></span>

  
  
<span data-ttu-id="7aa16-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7aa16-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7aa16-105">Содержит адрес электронной почты пользователя обмена мгновенными сообщениями.</span><span class="sxs-lookup"><span data-stu-id="7aa16-105">Contains the messaging user's email address.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="7aa16-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="7aa16-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="7aa16-107">PR_EMAIL_ADDRESS, PR_EMAIL_ADDRESS_A, PR_EMAIL_ADDRESS_W</span><span class="sxs-lookup"><span data-stu-id="7aa16-107">PR_EMAIL_ADDRESS, PR_EMAIL_ADDRESS_A, PR_EMAIL_ADDRESS_W</span></span>  <br/> |
|<span data-ttu-id="7aa16-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="7aa16-108">Identifier:</span></span>  <br/> |<span data-ttu-id="7aa16-109">0x3003</span><span class="sxs-lookup"><span data-stu-id="7aa16-109">0x3003</span></span>  <br/> |
|<span data-ttu-id="7aa16-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="7aa16-110">Data type:</span></span>  <br/> |<span data-ttu-id="7aa16-111">PT_STRING8 PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="7aa16-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="7aa16-112">Область:</span><span class="sxs-lookup"><span data-stu-id="7aa16-112">Area:</span></span>  <br/> |<span data-ttu-id="7aa16-113">Распространенные MAPI</span><span class="sxs-lookup"><span data-stu-id="7aa16-113">MAPI common</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="7aa16-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="7aa16-114">Remarks</span></span>

<span data-ttu-id="7aa16-115">Эти свойства являются примерами свойств базовый адрес для всех пользователей, обмена мгновенными сообщениями.</span><span class="sxs-lookup"><span data-stu-id="7aa16-115">These properties are examples of the base address properties for all messaging users.</span></span> <span data-ttu-id="7aa16-116">Он является строкой символом null, формат которых имеет значение только для системы обмена сообщениями.</span><span class="sxs-lookup"><span data-stu-id="7aa16-116">It is a null-terminated string whose format has meaning only for the underlying messaging system.</span></span> 
  
<span data-ttu-id="7aa16-117">Эти свойства используются в сочетании со свойствами **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)) в адресацию сообщений и **PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="7aa16-117">These properties are used in conjunction with the **PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md)) and **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)) properties in addressing messages.</span></span> <span data-ttu-id="7aa16-118">Формат строки определяется **PR_ADDRTYPE**.</span><span class="sxs-lookup"><span data-stu-id="7aa16-118">The string format is qualified by **PR_ADDRTYPE**.</span></span> 
  
<span data-ttu-id="7aa16-119">Допустимые значения для этого свойства:</span><span class="sxs-lookup"><span data-stu-id="7aa16-119">Valid values for this property include:</span></span> 
  
```cpp
network/postoffice/user 
Bruce@XYZZY.COM 
/c=US/a=att/p=Microsoft/o=Finance/ou=Purchasing/s=Furthur/g=Joe 
 
```

## <a name="related-resources"></a><span data-ttu-id="7aa16-120">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="7aa16-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="7aa16-121">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="7aa16-121">Protocol specifications</span></span>

<span data-ttu-id="7aa16-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="7aa16-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="7aa16-123">Содержит ссылки на связанные спецификаций протокола Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="7aa16-123">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="7aa16-124">[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="7aa16-124">[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="7aa16-125">Задает свойства и операции для списков пользователей, контактов, групп и ресурсов.</span><span class="sxs-lookup"><span data-stu-id="7aa16-125">Specifies the properties and operations for lists of users, contacts, groups, and resources.</span></span>
    
<span data-ttu-id="7aa16-126">[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="7aa16-126">[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="7aa16-127">Преобразование conventions стандартных электронной почты Интернета объекты сообщений.</span><span class="sxs-lookup"><span data-stu-id="7aa16-127">Converts from Internet standard email conventions to message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="7aa16-128">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="7aa16-128">Header files</span></span>

<span data-ttu-id="7aa16-129">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="7aa16-129">Mapidefs.h</span></span>
  
> <span data-ttu-id="7aa16-130">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="7aa16-130">Provides data type definitions.</span></span>
    
<span data-ttu-id="7aa16-131">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="7aa16-131">Mapitags.h</span></span>
  
> <span data-ttu-id="7aa16-132">Содержит определения свойства в списке альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="7aa16-132">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="7aa16-133">См. также</span><span class="sxs-lookup"><span data-stu-id="7aa16-133">See also</span></span>



[<span data-ttu-id="7aa16-134">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="7aa16-134">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="7aa16-135">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="7aa16-135">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="7aa16-136">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="7aa16-136">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="7aa16-137">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="7aa16-137">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

